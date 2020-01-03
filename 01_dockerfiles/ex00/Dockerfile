FROM alpine

LABEL maintainer="gmolin@student.hive.fi"

RUN apk update && apk upgrade && apk add emacs 

ENTRYPOINT emacs


# How to build it?
# docker build -t ex00 .

# How to run it?
# docker run --rm -it ex00