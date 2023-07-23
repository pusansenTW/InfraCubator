# Use the official Golang image as the base image
FROM golang:latest

# Set the working directory inside the container
WORKDIR /app

# Copy the application source code to the container's working directory
COPY . .

# Build the Go application inside the container
RUN go build -o go-app .

# Expose the port that the application listens on
EXPOSE 8080

# Command to run the application when the container starts
CMD ["./go-app"]
