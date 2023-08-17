# DOCKER Căn bản
## Cài đặt
- Tải file cài đặt tương ứng: https://www.docker.com/
- Cài đặt mặc định
- Lưu ý: Windows cần cài thêm nhân Linux, làm theo chỉ dẫn của Docker

## HOW TO USE
### Getting started
- Bước 1: Clone repo chứa dockerfile
  *docker run --name repo alpine/git clone https://github.com/docker/getting-started.git*
- Bước 2: Build
    *cd getting-started*
    *docker build -t docker101tutorial .*
- Bước 3: Run
  *docker run -d -p 8080:80 --name docker-tutorial docker101tutorial*
Lưu ý: port **8080** là port máy chạy docker, port **80** là port của docker image
- Bước 4 (option): Chia sẻ docker image
  *docker tag docker101tutorial winngo88/docker101tutorial*
  *docker push winngo88/docker101tutorial*

### Usecase
- NodeJS:
  - Port mặc định của Node là 3000, khi map port Docker ta ngoài cần lưu ý
- Python:
  - Lỗi load model hdf5 file: fix bằng cách cài *pip install h5py*
- Truy cập Docker image: *docker run --rm -it --entrypoint bash image_name*


## Tham khảo
HỎI DÂN IT
https://www.youtube.com/watch?v=Y3zqsFpUzMk&list=PLncHg6Kn2JT4kLKJ_7uy0x4AdNrCHbe0n