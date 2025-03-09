С помощью дженеиков можно компиляровать унивесральный функции струтуры под несколько типов. Пример использования:
``` go
func New[T any](data ...T) []T { // функция скомпилируеться под все типы и будет работать со всеми типами

array := make([]T, 0, 100)

array = append(array, data...)

return array

}
```
Можно ограничить использование типов:
```go
func Sum[T int | float32](data... T) T{ //будет компилироваться только под int и float32

var res T

for _, value := range data{

res += value

}

return res

}
```