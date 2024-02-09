
Dockerfile:5
--------------------
   4 |     
   5 | >>> RUN apt-get update \
   6 | >>>     && apt-get install -y openjdk-11-jre wget \
   7 | >>>     && wget https://archive.apache.org/dist/directory/studio/${APACHE_DIRECTORY_STUDIO_VERSION}/ApacheDirectoryStudio-${APACHE_DIRECTORY_STUDIO_VERSION}-linux.gtk.x86_64.tar.gz \
   8 | >>>     && tar -xzf ApacheDirectoryStudio-${APACHE_DIRECTORY_STUDIO_VERSION}-linux.gtk.x86_64.tar.gz \
   9 | >>>     && rm ApacheDirectoryStudio-${APACHE_DIRECTORY_STUDIO_VERSION}-linux.gtk.x86_64.tar.gz
  10 |     
--------------------
ERROR: failed to solve: process "/bin/sh -c apt-get update     && apt-get install -y openjdk-11-jre wget     && wget https://archive.apache.org/dist/directory/studio/${APACHE_DIRECTORY_STUDIO_VERSION}/ApacheDirectoryStudio-${APACHE_DIRECTORY_STUDIO_VERSION}-linux.gtk.x86_64.tar.gz     && tar -xzf ApacheDirectoryStudio-${APACHE_DIRECTORY_STUDIO_VERSION}-linux.gtk.x86_64.tar.gz     && rm ApacheDirectoryStudio-${APACHE_DIRECTORY_STUDIO_VERSION}-linux.gtk.x86_64.tar.gz" did not complete successfully: exit code: 8

