D:\Git\mooc-docker>wsl
panuli@LAPTOP-I5QKNJTG:/mnt/d/Git/mooc-docker$ docker run -d nginx
Unable to find image 'nginx:latest' locally
latest: Pulling from library/nginx
afb6ec6fdc1c: Pull complete
b90c53a0b692: Pull complete
11fa52a0fdc0: Pull complete
Digest: sha256:30dfa439718a17baafefadf16c5e7c9d0a1cde97b4fd84f63b69e13513be7097
Status: Downloaded newer image for nginx:latest
20d52cd185b1be60ec0ec37da53aceb8c319be14374bb3a838b4f2466af55043
panuli@LAPTOP-I5QKNJTG:/mnt/d/Git/mooc-docker$ docker container ls  

CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
20d52cd185b1        nginx               "nginx -g 'daemon of…"   56 seconds ago      Up 54 seconds       80/tcp              tender_hodgkin  

panuli@LAPTOP-I5QKNJTG:/mnt/d/Git/mooc-docker$ docker run -d --name db -p 8091-8094:8091-8094 -p 11210:11210 couchbase
Unable to find image 'couchbase:latest' locally
latest: Pulling from library/couchbase
e92ed755c008: Pull complete
b9fd7cb1ff8f: Pull complete
ee690f2d57a1: Pull complete
53e3366ec435: Pull complete
7f93bd3ca98a: Pull complete
57a7a0cfb170: Pull complete
8ef6b4690dba: Pull complete
b195a0a56ba7: Pull complete
6c5ea1499610: Pull complete
e386ee257b62: Pull complete
c0177a2d2805: Pull complete
a38311719d6f: Pull complete
8b8b7b5edf67: Pull complete
Digest: sha256:059365e37a618f31a1b379e6047e6c1ad4eb4076456d9931cdee462112cd5fb8
Status: Downloaded newer image for couchbase:latest
f4530e13dc584a59e30a4c98b97564c9bef1bf493ecc7f2d409adb9fb44198ff
panuli@LAPTOP-I5QKNJTG:/mnt/d/Git/mooc-docker$
panuli@LAPTOP-I5QKNJTG:/mnt/d/Git/mooc-docker$ docker run -d nginx
73462f000cd68ce6b9e96c2c6171cd6e4afa0da872c7385136dfd424e2fbf76d  

Run 'docker container COMMAND --help' for more information on a command.
panuli@LAPTOP-I5QKNJTG:/mnt/d/Git/mooc-docker$ docker container ls
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                                                                                                              NAMES
73462f000cd6        nginx               "nginx -g 'daemon of…"   38 seconds ago      Up 37 seconds       80/tcp                                                                                                             gallant_satoshi
f4530e13dc58        couchbase           "/entrypoint.sh couc…"   59 seconds ago      Up 47 seconds       8095-8096/tcp, 0.0.0.0:8091-8094->8091-8094/tcp, 11207/tcp, 11211/tcp, 0.0.0.0:11210->11210/tcp, 18091-18096/tcp   db
20d52cd185b1        nginx               "nginx -g 'daemon of…"   5 minutes ago       Up 5 minutes        80/tcp                                                                                                             tender_hodgkin
panuli@LAPTOP-I5QKNJTG:/mnt/d/Git/mooc-docker$ docker stop f45 20d
f45
20d
panuli@LAPTOP-I5QKNJTG:/mnt/d/Git/mooc-docker$ docker container ls
CONTAINER ID        IMAGE               COMMAND                  CREATED              STATUS              PORTS               NAMES
73462f000cd6        nginx               "nginx -g 'daemon of…"   About a minute ago   Up About a minute   80/tcp              gallant_satoshi
panuli@LAPTOP-I5QKNJTG:/mnt/d/Git/mooc-docker$