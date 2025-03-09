В Go обработка ошибок отличается от стандартной реализации с иерархией `Exception`, принятой в других языках. Ошибки в Go обычно передаются как один из результатов функции или метода. Ошибка представляет собой интерфейс:
```go
type error intereface{
	Error() string
}
```
Таким образом, чтобы реализовать свою ошибку, достаточно создать тип, который удовлетворяет этому интерфейсу:
```go
type NotEnoughMoney struct{

}

func(e *NotEnoughMoney) Error() string}{
	return "Client has no money on balance"
}
```
Однако в большинстве случаев вы не занимаетесь этой хуйней, а используете пакет `errors`, который предоставляет удобные методы для их создания:
```go

type db interface{
	Save(id int) error
}

func SaveToDb(db db, userId int) error{
	if userId < 0{
		return errors.New("invalid user id")
	}
	return db.Save(userId)
}
```