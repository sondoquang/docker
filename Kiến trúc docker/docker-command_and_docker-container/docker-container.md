# Docker Container

1. Là phiên bản chạy của Docker Images, chứa đầy đủ các component để chạy- vd: code, runtime, system utilities, library, configuration file
2. Docker Container giống như là một ngôi nhà thực tế - được xây dựng từ bảng thiết kế, có thể ở, sử dụng, và thay đổi nội thất bên trong
## Docker Image như là bảng thiết kế --> ( thiết kế  ) --> Ngôi nhà

## **Các lệnh để chạy container từ một docker image**
* docker run <image_name>
* docker run --name <container_name> <image_name>
* docker run -it ubuntu bash ( cho phép tường tác với ubuntu trên terminal và thâm nhập vào container ubuntu )
* Example: docker run hello-world 

## Liệt kê ra các containers:
1. docker ps ( liệt kê tất cả các container đang chạy)
2. docker ps -a ( liệt kê tất cả các container kể cả không chạy )

## Xóa containers:
1. docker rm <container_id-or-name>  ( Xóa các container đã dừng)
2. docker rm -f <container_id-or-name> ( Xóa các container đang running ) ( f - force)

## Start, Stop and Restart container
1. docker stop <container_id-or-name>
2. docker start <container_id-or-name> ( sẽ không làm gì nếu container đang chạy )
3. docker restart <container_id-or-name> ( Dừng và khởi động lại container )

***Lưu ý: container_id và container_name lấy trong docker desktop***

## *Chú ý:*
- Thực chất "image_name" sẽ bao gồm cả image name và image tag
- Nó sẽ có thể biểu diễn: image_name:image_tag