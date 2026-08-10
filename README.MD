# Docker Server Project

A small learning project for getting hands-on with Docker containerization.

## What's here

- **`main.go`** — a minimal Go HTTP server that responds with "Hello from Docker!" on port `8991`.
- **`Dockerfile`** — packages the compiled `goserver` binary into a `debian:stable-slim` image.
- **`main.py`** / **`books/`** — a small unrelated Python word-counting script, used as a side exercise.

## Goal

The point of this repo isn't the app itself — it's learning how to:

- Build a Go binary and containerize it with a `Dockerfile`
- Set environment variables (`PORT`) inside a container
- Build and run Docker images locally

## Usage

Build the Go binary, then build and run the image:

```bash
go build -o goserver main.go
docker build -t docker-server-project .
docker run -p 8991:8991 docker-server-project
```

Visit [http://localhost:8991](http://localhost:8991) to see the server response.
