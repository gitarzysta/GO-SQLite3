# GO-MySQL
This is very simple example to learn how GO deal with the template engine in  GO. I used *html/template* package that is already 
built in inside of default package of GO. Connect to database SQLite3, grab the data and passing to the template, so that we can display 
the data to the user.

Here's the struct of User

```go
type user struct {
	ID        int64
	Username  string
	FirstName string
	LastName  string
	Password  []byte
}
```

To create the table using SQLite3:

```
sqlite3 website.db 'CREATE TABLE IF NOT EXISTS users (id integer primary key, username text, first_name text, last_name text, password text);'
```

