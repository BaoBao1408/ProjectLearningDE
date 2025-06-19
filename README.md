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

1. 🔍 Kiểm tra tài khoản và khu vực cloud đang dùng
ibmcloud target
2. 📦 Xem các namespace Container Registry được cấp quyền
ibmcloud cr namespaces
→ Thường có namespace riêng của bạn dạng: sn-labs-yourname
3. 🌍 Đặt vùng (region) phù hợp, ví dụ us-south
ibmcloud cr region-set us-south
4. 🔐 Đăng nhập Docker CLI với IBM Cloud Registry
ibmcloud cr login
5. 🧾 Tạo biến môi trường lưu namespace cá nhân
export MY_NAMESPACE=sn-labs-$USERNAME
6. 🏷 Gắn tag mới cho image để đẩy lên cloud
docker tag myimage:v1 us.icr.io/$MY_NAMESPACE/hello-world:1
7. ☁️ Push image lên IBM Cloud Container Registry
docker push us.icr.io/$MY_NAMESPACE/hello-world:1
8. 🔎 Xác minh image đã được đẩy thành công
ibmcloud cr images
hoặc giới hạn theo namespace
ibmcloud cr images --restrict $MY_NAMESPACE



