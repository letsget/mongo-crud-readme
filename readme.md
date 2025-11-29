### запрос(ы) для вставки данных минимум о двух книгах в коллекцию books

```javascript
awat db.books.insertMany([
  {
    title: "War and Peace",
    description: "A book about war and peace",
    authors: "Lev Tolstoy"
  },
  {
    title: "Master and Margarita", 
    description: "A book about love and dark forces",
    authors: "Mikhail Bulgakov"
  }
])
```

### запрос для поиска полей документов коллекции books по полю title

```javascript
await db.books.find( { title: "Crime and Punishment"})
 // поиск книги по названию "преступление и наказание"
```

### запрос для редактирования полей: description и authors коллекции books по _id записи

```javascript
await db.books.updateOne(
    { _id: ObjectId("test-id") },
    {
        $set: { 'description': 'updated description', authors: 'Jack London' },
    }
)
```

