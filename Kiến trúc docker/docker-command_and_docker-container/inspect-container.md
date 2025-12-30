# INSPECT CONTAINERS

* Command line
  * docker inspect <container_id-or-name>


# RUN CONTAINERS IN DIFFERENT MODES

1. Detached Mode - Run a container in the background
   * Command line: docker run -d <image_name>
2. Interactive Mode - Tun a container and interact with -it:
   * Command line: docker run -it <image_name> ( /bin/bash or bash )

    *Việc chạy container kết hợp -it giúp tương tác trực tiếp của terminal và container*