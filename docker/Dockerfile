FROM ubuntu:22.04

ENV TZ=Europe/Belgrade
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt update
RUN apt-get update && \
    apt-get install -y \
    python3 \
    python3-pip \
    nano \
    libsm6 \
    libxext6 \
    libxrender-dev \
    libgl1-mesa-glx unzip \
    curl cron ffmpeg \
    ssh openssh-client \
    vim \
    git

WORKDIR /cameltrack
ENV PYTHONPATH="/cameltrack"

RUN pip install uv
RUN uv init
RUN uv sync

CMD ["bash"]