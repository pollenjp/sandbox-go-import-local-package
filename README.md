# pollenjp/sandbox-go-import-local-package

I don't have [go-proj1](https://github.com/pollenjp/go-proj1) and [go-proj2](https://github.com/pollenjp/go-proj2) repositories.

You can build `go-proj2` without making `go-proj1` public, because [/go-proj2/go.mod](/go-proj2/go.mod) has `replace` directive.

```go.mod
module github.com/pollenjp/go-proj2

go 1.19

require github.com/pollenjp/go-proj1 v0.0.0-00010101000000-000000000000

replace github.com/pollenjp/go-proj1 => ../go-proj1
```

```sh
cd go-proj2
go run .
```

output

```txt
Hello, World! from go-proj2
Hello, World! from go-proj1
```
