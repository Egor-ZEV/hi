FROM ubuntu:latest

ENV APACHE_DIRECTORY_STUDIO_VERSION=2.0.0.v20211010-M19

WORKDIR /ApacheDirectoryStudio-${APACHE_DIRECTORY_STUDIO_VERSION}

CMD ["./ApacheDirectoryStudio"]                             
