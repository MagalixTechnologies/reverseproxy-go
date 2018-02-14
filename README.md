# reverseproxy

This is patched version of std net/http/httputil ReverseProxy struct.

The standard version of package doesn't allow to obtain how much time request
to API took. In this version `ModifyResponse` returns also `time.Duration`.

Previous signature of ModifyResponse:

```go
	ModifyResponse func(*http.Response) error
```

Current signature of ModifyResponse:
```go
	ModifyResponse func(*http.Response, time.Duration) error
```
