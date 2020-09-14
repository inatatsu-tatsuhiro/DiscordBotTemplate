FROM python:3.8
RUN apt-get update && apt-get install -y \
    wget \
    xz-utils \
    opus-tools

WORKDIR /tmp

RUN wget https://johnvansickle.com/ffmpeg/releases/ffmpeg-release-amd64-static.tar.xz \
    && tar Jxvf ./ffmpeg-release-amd64-static.tar.xz \
    && cp ./ffmpeg*amd64-static/ffmpeg /usr/local/bin

COPY requirements.txt /app/
WORKDIR /app
RUN pip install --upgrade pip && pip install -r requirements.txt

ENV DISCORD_TOKEN 'discord your token'

CMD python main.py
