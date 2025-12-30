# Dockerfile

1. Dockerfile là gì ?

- Là một file văn bản chứa dòng lệnh ( instructions ) để tự động hóa trong quá trình tạo Docker Images. Nó định nghĩa môi trường, dependencies và cách chúng ta chạy ứng dụng

2. Cấu trúc cơ bản:

- Mỗi dòng trong docker là một instruction
- Mỗi instruction tạo ra mộ layer trong image
- Dockerfile thường bắt đồng bằng FROM để chỉ đụng base image
