FROM ruby:3.3

ENV DISPLAY=host.docker.internal:0.0

RUN apt-get update && apt-get install -y telnet openjdk-17-jdk-headless && rm -rf /var/lib/apt/lists/*
