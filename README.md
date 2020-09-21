# grpcdemo

## Generating Ruby proto files

Install gRPC Tools first

```
gem install grpc-tools
```

Generate files

```
grpc_tools_ruby_protoc -I proto --ruby_out=grpc-client/lib --grpc_out=grpc-client/lib proto/helloworld.proto
```

## Running the server

Make sure you have the latest rust build tools.

Build the project first

```
cd grpc-server
cargo build
```

Then run the grpc-server binary

```
cd grpc-server
cargo run --bin grpc-server
``` 

## Running the ruby client

```
ruby grpc-client/greeter-client.rb
```