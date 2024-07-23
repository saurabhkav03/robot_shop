FROM golang

WORKDIR /go/src/app

COPY dispatch.go /go/src/app

#This line initializes a new Go module named dispatch in the working directory. The go mod init dispatch command creates a go.mod file, which is the file that defines the module's dependencies.
#The && go get part of the command fetches the necessary dependencies for the module. 
RUN go mod init dispatch && go get
RUN go install

#The dispatch command runs the binary that was installed by the previous go install command. This binary is the entry point of the Go application.
CMD dispatch