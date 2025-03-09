#wildberies 
```go
package main

import "time"

// Вводные:
// Функция executeTask может зависнуть.
// В ней не предусмотрен механизм отмены.
// Она не принимает Context или канал с событием отмены как аргумент.

func main() {

  // Задача:
  // Для функции executeTask написать обертку executeTaskWithTimeout.
  // Функция executeTaskWithTimeout принимает аргументом тайм-аут,
  // через который функция executeTask будет отменена.
  // Если executeTask была отменена по тайм-ауту, нужно вернуть ошибку

  executeTask()
}

func executeTask() {
  time.Sleep(10 * time.Second)
}
```
#### Решение
```go
//Ответ
func executeTaskWithTimeout(ctx context.Context, timeout time.Duration) error {
  timeoutCtx, cancel := context.WithTimeout(ctx, timeout)
  defer cancel()

  done := make(chan struct{})

  go func() {
    executeTask()
    close(done)
  }()

  select {
  case <-done:
    return nil
    case <-timeoutCtx.Done():
      return timeoutCtx.Err()
  }
}
```

