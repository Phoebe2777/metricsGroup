# Python 3.12 development environment
FROM python:3.12.8-bookworm

# Install R and basic development tools
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        r-base \
        r-base-dev \
        git \
        curl \
        build-essential && \
    rm -rf /var/lib/apt/lists/*

# Verify both languages are available
RUN python --version && R --version
