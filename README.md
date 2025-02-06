실행 순서

$ git clone https://github.com/thebluesoul/simple_web.git simple_web_docs

$ cd simple_web_docs/

simple_web_docs$ ll
합계 20
drwxrwxr-x  3 ubuntu ubuntu 4096  2월  6 20:17 ./
drwxrwxr-x 28 ubuntu ubuntu 4096  2월  6 20:17 ../
drwxrwxr-x  8 ubuntu ubuntu 4096  2월  6 20:17 .git/
-rw-rw-r--  1 ubuntu ubuntu   13  2월  6 20:17 REAME.md
-rw-rw-r--  1 ubuntu ubuntu  199  2월  6 20:17 docker-compose.yml
simple_web_docs$ sudo su

# docker-compose up -d
Creating network "simple_web_docs_default" with the default driver
Pulling web (nginx:latest)...
latest: Pulling from library/nginx
c29f5b76f736: Pull complete
e19db8451adb: Pull complete
24ff42a0d907: Pull complete
c558df217949: Pull complete
976e8f6b25dd: Pull complete
6c78b0ba1a32: Pull complete
84cade77a831: Pull complete
Digest: sha256:91734281c0ebfc6f1aea979cffeed5079cfe786228a71cc6f1f46a228cde6e34
Status: Downloaded newer image for nginx:latest
Creating nginx_server ... done
#
# docker-compose ps -a
    Name                  Command               State                  Ports                
--------------------------------------------------------------------------------------------
nginx_server   /docker-entrypoint.sh ngin ...   Up      0.0.0.0:8000->80/tcp,:::8000->80/tcp
#
