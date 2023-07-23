# Stage 1: Build
FROM golang:latest AS builder

# Set the working directory inside the container
WORKDIR /app

# Copy the application source code to the container's working directory
COPY . .

# Build the Go application
RUN go build -o go-app .

# Stage 2: Run
FROM alpine:latest

# Copy the binary from the builder stage to the final stage
COPY --from=builder /app/go-app /app/go-app

# Expose the port that the application listens on
EXPOSE 8080

# Command to run the application in the final stage
CMD ["/app/go-app"]
