# Start from the latest golang base image
FROM golang:latest

# Set the Current Working Directory inside the container
WORKDIR /app

# Copy everything from the current directory to the Working Directory inside the container
COPY . .

# Initialize Go modules
RUN go mod init go-app
RUN go mod tidy

# Build the Go app
RUN go build -o main .

# This container exposes port 8080 to the outside world
EXPOSE 8080

# Run the binary program produced by `go build`
CMD ["./main"]
