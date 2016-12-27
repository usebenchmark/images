FROM grpc/go

RUN go get -u google.golang.org/grpc
RUN go get -u github.com/golang/protobuf/protoc-gen-go

RUN mkdir -p /go/src/app
RUN mkdir -p /go/src/vendor

WORKDIR /go/src/app

CMD ["go-wrapper", "run"]

ONBUILD COPY main.go /go/src/app
ONBUILD RUN go-wrapper download
ONBUILD RUN go-wrapper install
