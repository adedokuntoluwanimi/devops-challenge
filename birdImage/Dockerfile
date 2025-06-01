# Using golang:<version> alpine as base image 
FROM golang:1.22.5-alpine
# Setting the work directory
WORKDIR /birdapp
# Copying available packages
COPY  go.mod ./
# Installing app dependencies
RUN go mod tidy
# Copying the rest of the application
COPY . .
# Compiling into an executable file
RUN go build -o birdapp
# Port to be exposed
EXPOSE 4200
# Command to be executed
CMD ["./birdapp"]




