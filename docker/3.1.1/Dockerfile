FROM ubuntu:16.04

RUN apt update
RUN apt install -y cron

COPY task.sh /usr/local/bin/
COPY cron-example /etc/cron.d/

RUN chmod 0644 /etc/cron.d/cron-example
RUN chmod 755  /usr/local/bin/task.sh

CMD ["cron", "-f"]