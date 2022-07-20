FROM python:3.8-bullseye

ENV TERM=xterm
ENV DEBIAN_FRONTEND=noninteractive

ADD pip.conf /etc/pip.conf
ADD sources.list /etc/apt/sources.list

RUN \
  export TZ="Asia/Shanghai"; \
  ln -snf /usr/share/zoneinfo/$TZ /etc/localtime; \
  echo $TZ > /etc/timezone; \
  apt-get update -y; \
  apt-get install dialog apt-utils -y; \
  apt-get install -y wget net-tools vim iputils-ping telnet; \
  pip install -U pip; \
  pip install -U setuptools wheel;\
  apt-get clean
