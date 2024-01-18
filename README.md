# paginator
[![go report card](https://goreportcard.com/badge/github.com/Squirrel-Entreprise/paginator "go report card")](https://goreportcard.com/report/github.com/Squirrel-Entreprise/paginator)
[![GoDoc](https://godoc.org/github.com/Squirrel-Entreprise/paginator?status.svg)](https://godoc.org/github.com/Squirrel-Entreprise/paginator)

## Usage

```bash
go get github.com/Squirrel-Entreprise/paginator
```

```go
type Post struct {
    ID    int
    Title string
    Body  string
}

var posts []Post
db = db.Where("id > ?", 0)

pagination.Paging(&pagination.Param{
    DB:      db,
    Page:    1,
    Limit:   10,
    OrderBy: []string{"id desc"},
}, &posts)
```