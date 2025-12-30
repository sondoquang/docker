## Docker Host:

- Cung cấp các môi trường hoàn chỉnh để thực thi và chạy các ứng dụng. Nó bao gồm Docker deamon, Images, Containers, Networks và Volumes
- Là máy ( vật lý hoặc ảo ) mà Docker Deamon đang chạy trên đó

## Docker deamon:

- Chịu trách nhiệm chạy containers, build images và xủ lý các hoạt động khác của Docker mà chúng ta gọi từ CLI

## Docker Object: Images, containers, networks, volumns

- Ví dụ chạy docker run ...
  - Nhận yêu cầu của CLI (client)
  - Kiểm tra xem image có sẵn chưa
  - Nếu chưa có thì oull từ registry về luôn rồi khởi tạo container nhờ ( docker deamon )
  - Nếu có rồi thì khởi tạo container luôn
  - Gửi trả thông tin về cho CLI ( client)
