# syntax = docker/dockerfile:1.4

FROM tiangolo/uvicorn-gunicorn-fastapi:python3.9-slim AS builder

WORKDIR /app

COPY requirements.txt ./

COPY ./app ./app

# install Docker tools (cli, buildx, compose)
COPY --from=gloursdocker/docker / /
