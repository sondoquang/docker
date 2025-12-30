# 1. DOCKER IMAGE OVERVIEW

 * Là đơn vị độc lập đã bao gồm code, môi trường, thư viện, cấu hình 

## Core Concepts:
* Layers
* Base Image: phiên bản nhó nhất của hệ điều hành
* Parent Image
* Image Tags: chỉ định version cho image name
* Image ID: dãy mã hash để phân biệt giữa nhiều image khác nhau


# 2. PULLING IMAGES FROM DOCKER HUB
* Tải về từ Docker Hub 
* Command line: `docker pull <image_name>:<tag>`
  * `image_name`: Tên của image, nếu trên Docker Hub sẽ là tên của repository ( vd: ubuntu, nginx)
  * `image_id`: Là label version của image


# 3. CÁC LỆNH SỬ DỤNG TRONG DOCKER IMAGE ( COMMAND LINE )
## 1. Listing images:
* `docker images` : xem toàn bộ images đang có
* `docker image ls` : ý nghĩa tương tự ( tuân theo cú pháp phân cấp của Docker CLI )
## 2. Removing images:
* Cách viết ngắn gọn:
  * `docker rmi <image_name>:<tag>`
  * `docker rmi <image_id>`
* Cách viết chính quy:
  * `docker image rm <image_name>:<tag>`
  * `docker image rm <image_id>`


# 4. INSPECT IMAGES AND IMAGE TAGGING

* `docker inspect <image_name>:<tag>`

* To tag an existing image:
* `docker tag <source_image>:<tag > <target_image>:<tag>`: ứng dụng khi cần upload images lên docker registry

# 5. CLEANING UP
* `docker system prune ( có đưa ra cảnh báo )`
* `docker system prune -f ( thêm cờ -f để tự dộng đồng ý )`
* Dùng để dọn dẹp toàn bộ tại nguyên không cần thiết trong Docker, bao gồm các container đã dừng, các mạng không sử dụng, các image  không còn liên kết, và các volume không sử dụng