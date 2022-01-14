# Hello gRPC (Go version)

|[Home](https://grpc.io/)|[Docs](https://grpc.io/docs/languages/go/)|[Repository](https://github.com/grpc/grpc-go)|
|---|---|---|

### TL:DR;

0. scarica i componenti necessari
    - `go install google.golang.org/protobuf/cmd/protoc-gen-go`
    - `go install google.golang.org/grpc/cmd/protoc-gen-go-grpc`
    - Protoc compiler: [docs](https://grpc.io/docs/protoc-installation/), [download](https://github.com/protocolbuffers/protobuf/releases)
1. crea il file `hello.proto`
2. compila il file `.proto`
   - `protoc --go_out=proto --go_opt=paths=source_relative --go-grpc_out=proto --go-grpc_opt=paths=source_relative hello.proto`
   - vengono generati due file `Go` all'interno della cartella *proto*, necessari alla compilazione
3. crea il package server e il relativo `main.go`
4. crea il package client e il relativo `main.go`

### Eseguire l'applicazione `server`

```bash
$>  go run .\server\main.go
```

### Eseguire l'applicazione `client`

```bash
$>  go run .\client\main.go -name Marco
```



                 
