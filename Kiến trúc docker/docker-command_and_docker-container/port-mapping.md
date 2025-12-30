## PORT MAPPING

1. docker run -p <host_port>:<container_port> <image_name>


## WORKING WITH CONTAINER LOGS

1. Xem log đến thời điểm hiện tại
   * Command line: docker logs <container_id>
2. Xem log được update liên tục khi  container đang chạy ==> muốn monitor realtime
   * Command line: docker logs -f <container_i-or-name>


## CLEANING UP
* Một số container đã dừng ( exited ) vì hoàn thành công việc hoặc bị lỗi.
* Những container này không tụ biến mất, mà vẫn chiếm dụng lượng ổ cứng và tài nguyên metadata của Docker

*Command line*
* docker container prune ( có hói xác nhận xóa hay không )
* docker container prune -f ( thêm cờ -f để auto đồng ý )


## EXECUTING COMMANDS IN RUNNING CONTAINERS
* Command line: docker exec -it <container_id-or-name> <command>