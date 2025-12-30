## Restart Policy
1. Giúp docker container tự động khởi động lại trong các tính huống lỗi, crash, hoặc khi Docker daemon khổi động lại'
2. Đảm bảo ứng dụng có độ sẵn sàng cao ( high availability )

## Các thiết lập:
* Sử dụng flah --restart trong câu lệnh docker run, ví dụ docker run --restart always ubuntu:latest bash

## Khi nào cần dùng :
* Production environment: Tự động phục hồi khi container bị crash
* Long-running service: Database, web server, API services
* System reboot: Container tự động khởi dộng sau khi server restart
* Unexpected failures: Xử lý lỗi không mong muốn


## Options:
1. no ( mặc định không thêm flag --restart vào )
   * Container không tự khởi động lại
   *Command line*
   * docker run --restart no ubuntu bash
   * docker run ubuntu bash
2. always
   * Container luôn luôn khởi động lại khi dừng
   * Nếu chúng ta chủ  động cho nó dừng  bằng docker stop thì container sẽ tự khởi động lại.
   *Command line*
   * docker run --restart always ubuntu bash
3. on-failure[:max-retries]
   * Chỉ khới dộng lại khi container thoát với lỗi (exit code <> 0)
   * Có thể giới hạn số lần retry , vd: on-failure:5 ( tối đa 5 lần )
   * Docker daemon restart: Container không tự động khởi động
   *Command line*
   * docker run --restart on-failure:5 ubuntu bash
4. unless-stopped
   * Giống với always nhưng không tự khởi động lại nếu container đã được dừng thủ công với docker stop
   *Command line*
   * docker run  --restart unless-stopped ubuntu bash