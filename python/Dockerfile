# マイナーバージョン以下を指定をしないと、コンテナ image を build した時点での最新の python stable version が installされる
FROM python:3

ENV PYTHONBURRERED=1
RUN apt-get update
RUN apt-get -y install locales && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TERM xterm

RUN mkdir /workspace
WORKDIR /workspace
ADD ./python/requirements.txt /workspace/
RUN pip install --upgrade pip
RUN pip install -U setuptools
RUN pip install -r requirements.txt
ADD . /workspace/

