FROM ruby:3.4

ENV DISPLAY=host.docker.internal:0.0

RUN apt-get update && apt-get install -y telnet openjdk-21-jdk-headless && rm -rf /var/lib/apt/lists/*
