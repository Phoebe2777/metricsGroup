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

# Install Python packages
COPY environment/requirements.txt /tmp/requirements.txt

RUN python -m pip install --no-cache-dir \
    -r /tmp/requirements.txt
    
# Check Python package dependencies
RUN python -m pip check
