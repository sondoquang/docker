# Lệnh Build Docker Images

- **_`Command line`_**: `docker build -t <image_name>:<image_tag> .`
- `"."` Thư mục hiện tại đang đứng khi chạy lệnh trên - là build context ( Mặc định sẽ tìm Dockerfile trong build context)

  - **Build context**: toàn bộ nội dung của thư mục mà chúng ta chỉ định, bao gồm:
  - Tất cả file va thư mục con bên trong
  - Trừ những thứ được liệt kê trong file .dockerignore
  - **_Chỉ có thể copy các file trong build context_**

**_`Command line`_**: `docker build -f <path_to_Dockerfile> -t <image_name>:<image_tag> <path_build_context>.`
