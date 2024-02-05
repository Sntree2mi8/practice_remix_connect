.PHONY: install generate all

all: install generate

install:
	go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.3.0
	go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.32.0
	go install github.com/bufbuild/buf/cmd/buf@v1.29.0

generate-go:
	buf generate --template buf.gen.go.yaml src

generate-ts:
	npx buf generate --template buf.gen.ts.yaml src
