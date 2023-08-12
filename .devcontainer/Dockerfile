FROM python:3.8

ARG USERNAME=devuser
ARG USER_UID=1000
ARG USER_GID=$USER_UID

RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m -s /bin/bash $USERNAME

WORKDIR /app

COPY ./requirements.txt /app
COPY ./requirements-dev.txt /app

RUN pip install -r requirements.txt
RUN pip install -r requirements-dev.txt
