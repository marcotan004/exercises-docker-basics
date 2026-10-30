FROM ubuntu:24.04

WORKDIR /usr/src/app

RUN apt-get update
RUN apt install -y curl

COPY script.sh .

RUN chmod +x script.sh

# When running docker run the command will be ./hello.sh
CMD ["./script.sh"]