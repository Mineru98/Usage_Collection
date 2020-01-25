# Docker

## Install - [설치]

```shell
sudo apt-get update
sudo apt-get install docker.io
sudo ln -sf /usr/bin/docker.io /usr/local/bin/docker
```

## 현재 유저 권한 유지

```shell
sudo usermod -aG docker [username]
# log out
exit
```

## Docker Image Install

```shell
sudo docker pull [image name]:[version]
```

## Docker Image Run & Start

### run

```shell
sudo docker run -i -t [Image Id] /bin/bash //쉘에 들어가서 작업을 할 수 있다.
sudo docker run -d [Image Id] //쉘을 데몬처럼 사용하는 방식으로 -d 옵션은 백그라운드로 작업 된다.
sudo docker run -d --name [NAMES] [Image Id] // --name 옵션은 이미지 실행 이름을 지정
sudo docker run -d --name [NAMES] -p [OUT PORT]:[IN PORT] [IMAGE Id] // OUT PORT는 실행하는 host의 port이고 IN PORT는 컨테이너 host의 port이다.
```

### start

```shell
sudo docker ps -a //이 명령어을 입력 후 NAMES 나 CONTAINER ID를 알아내서 실행
sudo docker start [NAMES or CONTAINER ID]
```

### attach

```shell
sudo docker ps -a //이 명령어을 입력 후 NAMES 나 CONTAINER ID를 알아내서 실행
sudo docker attach [NAMES or CONTAINER ID]
// enter를 입력하면 컨테이너로 들어가짐
// ctrl + p + q 를 입력하면 컨테이너를 정지하지 않고 빠져나올 수 있음.
// exit나 ctrl + d를 입력하면 컨테이너를 정지하면서 빠져나옴.
```

## 컨테이너 프로세스 호출

```shell
sudo docker exec [NAMES] [COMMAND]
```

## Error

```shell
sudo docker pull ubuntu:latest
docker: Error response from daemon: Get https://registry-1.docker.io/v2/: Service Unavailable.
```

이런 경우 첫번째로는 아래 코드를 입력하면 해결이 됨.

```shell
sudo service docker restart
```

혹은 `/etc/resolv.conf`가 잘못 링크가 되어있어서 error가 생기는 경우가 있는데
이럴경우에는 먼저 `sudo vi /etc/resolv.conf`를 한 뒤 파일 내용을 수정 후 저장하고 나올 때 error가 발생하면 `rm /etc/resolv.conf`를 하고 `sudo vi /etc/resolv.conf`를 한 뒤 `nameserver 8.8.8.8`을 입력해주고 저장 한 뒤 `sudo service docker restart`를 한 뒤 다시 한번 `docker pull` 명령을 실행해 본다.
