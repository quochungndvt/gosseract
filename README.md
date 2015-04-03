# Gosseract-OCR [![Build Status](https://travis-ci.org/otiai10/gosseract.svg?branch=master)](https://travis-ci.org/otiai10/gosseract) [![GoDoc](https://godoc.org/github.com/otiai10/gosseract?status.png)](https://godoc.org/github.com/otiai10/gosseract)

[Tesseract-OCR](https://code.google.com/p/tesseract-ocr/) command wrapper for Golang

# example
```go
package main

import (
	"fmt"
	"github.com/otiai10/gosseract"
)

func main() {
		// the simplest way
    txt := gosseract.Must(gosseract.Params{
			Src: "your/img/file.png",
		})
    fmt.Println(txt)
}
```

# docs

- `func Exec(params Params) (string, error)`
- `func Must(params Params) string` alias for `Exec`

Client

- `NewClient() *Client`
- `(c *Client) Src(srcPath string) error`
- `(c *Client) Img(img image.Image) error`
- `(c *Client) Digest(digestPath string) error`
- `(c *Client) Dest(destPath string) error`

# installation


1. install [tesseract-ocr](https://code.google.com/p/tesseract-ocr/)
2. `go get github.com/otiai10/gosseract`
3. `go get github.com/otiai10/mint`
4. test↓

# test

```
go test ./... -v -bench .
```

# issues
- https://github.com/otiai10/gosseract/issues?state=open
