# Docker

The `Dockerfile` does a multistage build:

- Stage 1 - build the app (size about 450MB)
- Stage 2 - copy the app into non-priviledged nginx container (size down to 26MB)

## Build Container

Run: `docker build --no-cache -t wordles-with-friends:test .`

## Run Container

Run: `docker run -it --rm -p 8080:8080 wordles-with-friends:test`

In web browser go to <http://localhost:8080/wordles-with-friends> to see the app
