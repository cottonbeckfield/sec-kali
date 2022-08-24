## Build the Container
To do this, we will build the image so we can run it.

We are building this on the latest, so ensure we update the kali-rolling image.
`docker pull kalilinux/kali-rolling:latest` 

### Build your Dockerfile.
`docker build -t kali-info:1.0 .`