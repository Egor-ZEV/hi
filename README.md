➜  dockers_Apache docker images
REPOSITORY                TAG       IMAGE ID       CREATED          SIZE
apache-directory-studio   latest    5bac6f6ce69d   12 seconds ago   77.9MB
osixia/openldap           latest    31d1d6e16394   2 years ago      257MB
➜  dockers_Apache docker run -d -it --name apache-container ap 
Unable to find image 'ap:latest' locally
docker: Error response from daemon: pull access denied for ap, repository does not exist or may require 'docker login': denied: requested access to the resource is denied.
See 'docker run --help'.
➜  dockers_Apache docker run -d -it --name apache-container apache-directory-studio
d963ae5b809d993b129648fffa2a779511c246d84cc4b91d899fc6b4b84314f5
docker: Error response from daemon: failed to create task for container: failed to create shim task: OCI runtime create failed: runc create failed: unable to start container process: exec: "./ApacheDirectoryStudio": stat ./ApacheDirectoryStudio: no such file or directory: unknown.
➜  dockers_Apache docker run -d -it --name apache-container apache-directory-studio
