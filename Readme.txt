# Docker "Hello World" from ARM Assembly on Raspberry Pi 

# Create a simple hello world binary
vi hw.S
as -o hw.o hw.S
ld -s -o hw hw.o
./helloworld

# Build the Docker container
docker build -t ernestgwilsonii/docker-raspberry-pi-arm-assembly-hello-world -f Dockerfile.armhf .

# Verify the size
docker images

# Run the image
docker run ernestgwilsonii/docker-raspberry-pi-arm-assembly-hello-world

# Upload to Docker Hub
#docker login
#docker push ernestgwilsonii/docker-raspberry-pi-arm-assembly-hello-world

