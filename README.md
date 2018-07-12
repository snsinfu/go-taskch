taskch - Simple goroutine manager
---------------------------------

[![GoDoc][godoc-badge]][godoc-url]
[![Build Status][travis-badge]][travis-url]
[![MIT License][license-badge]][license-url]

[travis-badge]: https://travis-ci.org/snsinfu/go-taskch.svg?branch=master
[travis-url]: https://travis-ci.org/snsinfu/go-taskch
[godoc-badge]: https://img.shields.io/badge/go-documentation-blue.svg
[godoc-url]: https://godoc.org/github.com/snsinfu/go-taskch
[license-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[license-url]: https://raw.githubusercontent.com/snsinfu/go-taskch/master/LICENSE

This repository contains a Go package `taskch` which allows multiple goroutines
to be joined.

```go
import "github.com/snsinfu/go-taskch"

func doTasks() error {
	tasks := taskch.New()
	
	tasks.Go(func() error {
		return nil
	})
	
	tasks.Go(func() error {
		return nil
	})
	
	return tasks.Wait()
}
```

## License

MIT License.
