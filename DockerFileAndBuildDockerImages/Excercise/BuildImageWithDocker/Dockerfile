
# Base image , sẽ sử dụng để tạo docker image mới
FROM ubuntu:latest

# WORKDIR - giúp chúng ta thiết lập thư mục làm việc trong môi trường tạo docker image
# /ap sẽ là thư mục làm việc của mình trong môi trường tạo docker image - xem như đứng trong thư mục này
WORKDIR /app

# Copy file script.sh vào thư mục /app ( tức là môi trường tạo docker image )
COPY script.sh /app/script.sh

# Setup câu lệnh mặc định khi chạy docker container từ docker image ( được build / tạo từ Dockerfile )
CMD ["bash", "script.sh"]

# Step by step để thực hiện ví dụ này:

# 1. Tạo docker image qua lênh docker build -f <image-name>:<image-tag> . ( . ở đây là workdir tạo trong docker file )
# 2. Sử dụng lênh docker run <image-name>:<image-tag> ( image name và image tag tạo trong docker file )
# 3. cmd return về dòng echo trong script.sh là thành công