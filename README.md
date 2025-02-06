# Simple Web Deployment with Docker Compose

This guide provides step-by-step instructions to clone, set up, and run a simple web server using Docker Compose with Nginx.

## Prerequisites
- Docker installed
- Docker Compose installed

## Installation and Setup

1. Clone the repository:
   ```sh
   git clone https://github.com/thebluesoul/simple_web.git simple_web_docs
   ```

2. Navigate to the project directory:
   ```sh
   cd simple_web_docs/
   ```

3. Verify the contents of the directory:
   ```sh
   ls -l
   ```
   Expected output:
   ```sh
   total 20
   drwxrwxr-x  3 ubuntu ubuntu 4096  Feb 6 20:17 ./
   drwxrwxr-x 28 ubuntu ubuntu 4096  Feb 6 20:17 ../
   drwxrwxr-x  8 ubuntu ubuntu 4096  Feb 6 20:17 .git/
   -rw-rw-r--  1 ubuntu ubuntu   13  Feb 6 20:17 README.md
   -rw-rw-r--  1 ubuntu ubuntu  199  Feb 6 20:17 docker-compose.yml
   ```

4. Switch to superuser (optional if necessary):
   ```sh
   sudo su
   ```

5. Start the service with Docker Compose:
   ```sh
   docker-compose up -d
   ```

   Expected output:
   ```sh
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
   ```

6. Verify that the container is running:
   ```sh
   docker-compose ps -a
   ```
   Expected output:
   ```sh
   Name                  Command               State                  Ports                
   --------------------------------------------------------------------------------------------
   nginx_server   /docker-entrypoint.sh ngin ...   Up      0.0.0.0:8000->80/tcp,:::8000->80/tcp
   ```

## Accessing the Web Server
Once the container is running, you can access the web server by opening a browser and navigating to:
   ```
   http://localhost:8000
   ```

## Stopping the Service
To stop the service, run:
   ```sh
   docker-compose down -v
   ```

## License
This project is licensed under the MIT License.
