# ProjectLearningDE
DE of Quoc Bao

📚 1. Tài liệu hướng dẫn chính thức
🔗 Docker chính thức:
https://docs.docker.com/get-started/
https://docs.docker.com/engine/reference/builder/ — Giải thích từng lệnh trong Dockerfile.

# Clone Node.js Docker App Project
cd /home/project
git clone https://github.com/ibm-developer-skills-network/CC201.git
cd CC201/labs/1_ContainersAndDocker/
# Build image
docker build . -t myimage:v1

# Xem image đã tạo
docker images

# Remove image
docker image rm myimage:v1

# Chạy container
# Pull hello-world image
docker pull hello-world

# Run hello-world container
docker run hello-world

# Kiểm tra container
docker ps -a

# View Project Structure
ls
Dockerfile  app.js  package.json

# Xoá container
docker container rm <container_id>

# Verify the Image is Created
docker images

# Run a Container from Your Image
docker run -p 3000:3000 myimage:v1

# Stop container (if it's running in background)
docker stop <container_id>


