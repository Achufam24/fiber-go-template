<h1 align="center">
    <img align="center" width="132px" src=".github/images/fiber_logo.svg" alt="Fiber logo" /><br/>
    Fiber backend template<br/>
    for <a href="https://github.com/create-go-app">Create Go App CLI</a>
</h1>

> Fiber is an `Express` inspired web framework build on top of `Fasthttp`, the fastest HTTP engine for Go. Designed to ease things up for fast development with zero memory allocation and performance in mind.
>
> People switching from Node.js to Go often end up in a bad learning curve to start building their webapps, this project is meant to ease things up for fast development, but with zero memory allocation and performance in mind.
>
> 📚 [Documentation](https://docs.gofiber.io/)

## Requirements

- Go `v1.11+` with Go Modules ([golang/download](https://golang.org/dl/))

### Optional

- Docker `v19.x` ([docker/onboarding](https://hub.docker.com/?overlay=onboarding))

## Used packages

- [gofiber/fiber](https://github.com/gofiber/fiber) `v1.12.1`
- [go-yaml/yaml](https://github.com/go-yaml/yaml) `v2.3.0`
- [stretchr/testify](https://github.com/stretchr/testify) `v1.6.1`

## Template structure

```console
foo@bar:~/net_http-go-template$ tree .
.
├── .dockerignore
├── .editorconfig
├── .gitignore
├── Dockerfile
├── LICENSE
├── README.md
├── Taskfile.yml
├── go.mod
├── go.sum
├── cmd
│   └── apiserver
│       └── main.go
├── configs
│   └── apiserver.yml
├── static
│   └── index.html
└── pkg
    └── apiserver
        ├── config.go
        ├── config_test.go
        ├── error_checker.go
        ├── error_checker_test.go
        ├── new_server.go
        ├── new_server_test.go
        └── routes.go

6 directories, 17 files
```

### Configs

All server/database/logging/static configs included in one YAML file `./configs/apiserver.yml`:

```yaml
# Server config
server:
  host: 127.0.0.1
  port: 8080

# Database config
database:
  host: 127.0.0.1
  port: 5432
  username: postgres
  password: 1234

# Static files config
static:
  prefix: /public
  path: ./static
```

### TODO

- [x] Add tests
- [ ] Add jmoiron/sqlx (Postgres)

> You're feel free to send ideas to [issue](https://github.com/create-go-app/net_http-go-template/issues/new/choose) 😉

## License

MIT &copy; [Vic Shóstak](https://github.com/koddr) & [True web artisans](https://1wa.co/).
