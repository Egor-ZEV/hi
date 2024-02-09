FROM openjdk:latest

ENV APACHE_DIRECTORY_STUDIO_VERSION=2.0.0.v20211010-M19

RUN apt-get update \
    && apt-get install -y wget \
    && wget https://archive.apache.org/dist/directory/studio/${APACHE_DIRECTORY_STUDIO_VERSION}/ApacheDirectoryStudio-${APACHE_DIRECTORY_STUDIO_VERSION}-linux.gtk.x86_64.tar.gz \
    && tar -xzf ApacheDirectoryStudio-${APACHE_DIRECTORY_STUDIO_VERSION}-linux.gtk.x86_64.tar.gz \
    && rm ApacheDirectoryStudio-${APACHE_DIRECTORY_STUDIO_VERSION}-linux.gtk.x86_64.tar.gz

WORKDIR /ApacheDirectoryStudio-${APACHE_DIRECTORY_STUDIO_VERSION}

CMD ["./ApacheDirectoryStudio"]
