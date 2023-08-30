FROM python:latest

WORKDIR /code
RUN apt update
RUN apt install -y \
  build-essential \
  python3.11 \
  python3.11-distutils \
  python3.11-lib2to3 \
  python3.11-venv \
  python3-pip \
  python3-dev \
  python3.11-dev

RUN python -m pip install --upgrade pip
RUN python -m pip list -o | tail -n +3 | awk '{print $1}' | xargs -n1 python -m pip install -U
