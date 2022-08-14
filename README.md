# What do I call these?
# How do I break down each image/folder structure and explain the tools + why?
# How do I explain how to run them? (I use Docker GUI at this point)

# Build the Container
To do this, we will build the image so we can run it.

# We are building this on the latest, so ensure we update the kali-rolling image.
`docker pull kalilinux/kali-rolling:latest` 
# Build your Dockerfile.
`docker build -t kali-info .`