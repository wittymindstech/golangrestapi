# golangrestapi
Go Lang API

For below error while docker build:

Step 7/9 : RUN go build -o /docker-gs-ping
 ---> Running in 42401eeae526
main.go:7:2: no required module provides package github.com/labstack/echo/v4; to add it:
	go get github.com/labstack/echo/v4
main.go:8:2: no required module provides package github.com/labstack/echo/v4/middleware; to add it:
	go get github.com/labstack/echo/v4/middleware
The command '/bin/sh -c go build -o /docker-gs-ping' returned a non-zero code: 1


Download go module manually:

go get github.com/labstack/echo/v4
go get github.com/labstack/echo/v4/middleware

And then run docker build again


