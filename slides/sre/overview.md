## what is Grpc?

* use Protocol Buffers(PB) as:
* Interface Definition Language(IDL)
* Undelaying message interchange format


## what is Grpc?

* Client app can directly call methods on a server application on a different machine as if was a local object.
* Defines a service.
* Specifies methods with their parameters and returning parameters.


## what is Grpc?

* The Server: implements that gRPC interface and runs a gRPC server to handle client calls.
* The client: has a stub(which refers to a client in some language) that provides the same methods as the server.


## what is Grpc?
![grpc](https://grpc.io/img/landing-2.svg)


## Protocol Buffers(PB)

* Google mature open source mechanism for serializing structured data.
1. Define the structure for the data you want to serialize in proto file.
    * PB data is structured as messages.
    * PB message is a small logical records of information cointaining a series of fields(name-value pairs).


## Protocol Buffers(PB)

1. Use the PB copiler protoc to generate data access classes in any supported language.
    * Provides:
        * Data Accessors for each field.
        * Methods to serialize/parse the whole struct to/from raw bytes.


## Protocol Buffers(PB)

* gRPC uses protoc with a special pluging to generate code from you proto file.
* Generates:
    * gRPC server and client code.
    * PB Code for populating, serializing, and retriving you message types.
* Proto3 is the current PB version which supports many programing languages and include other features over Proto2.


## gRPC Concepts

* The PB IDL is used to describe  service interface and the structure of the paylod messages.

```proto
service HelloService{
    rpc SayHello(HelloRequest) returns (HelloResponse);
}

message HelloRequest {
    string greeting = 1
}
message HelloResponse {
    string reply = 1
}
```


## gRPC Concepts

* gRPC lets you define four kinds of service methods:


## gRPC Concepts

* Unary RPCs:
* The client send a single request to the server and gets a single response back.
* is like a normal function call. 

```proto
rpc SayHello(HelloRequest) returns (HelloResponse);
```


## gRPC Concepts

* Server streaming RPCS:
* The client send a request to the server and gets a stream to read a sequence of messages back.
* The client read from de streaming until there are no more messages.
* gRPC guarantees message ordering within an individual RPC call.

```proto
rpc LotsOfReplies(HelloRequest) returns (stream HelloResponse);
```


## gRPC Concepts

* Client streaming RPCS:
* The client write a secuense of messages and sends them to the server using a provider stream.
* The client waits for the server response.
* Again gRPC guarantees message ordering within an individual RPC call.

```proto
rpc LotsOfGreeting(stream HelloRequest) returns (HelloResponse);
```


## gRPC Concepts

* Bidirectional streaming RPCS:
* Both sides send a sequence of messages using read-write stream.
* Each stream operates independly, client and servers can write in whatever order they like.
* The order in each stream is preserved. 

```proto
rpc BidiHello(stream HelloRequest) returns (stream HelloResponse);
```


## gRPC Concepts
* Using de API surface on the server side:
* Implement methods declared by the service.
* Run gRPC server which decode incoming requests, executes service methods and encodes service response.


## gRPC Concepts
* Using de API surface on the client side:
* The client has a local object know as stub(or client) which implements the same methods as the service. the client can just call the methods on the local object, wrapping the parameters for the call in the appropiate PB message type.










