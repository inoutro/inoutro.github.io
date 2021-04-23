


# docker 사용을 위한 명령어 정리

## 1. image
    - docker images : 깔려있는 image 리스트 확인
    - docker pull [옵션] [이미지 명] [태그 명] : 이미지 다운로드 (태그 설정 안하면 latest 버전 설치) - 이미지 검색 : https://hub.docker.com/
        - ex) docker pull ubuntu:18.04

## 2. create
    - docker create [옵션] 이미지 [커맨드] : docker container 설치
        - ex) docker create -it --name container_name ubuntu:18.04 bash

## 3. status
    - docker ps : 현재 실행중인 컨테이너 확인
    - docker ps -a : 실행중이지 않은 컨테이너도 확인

## 4. run
    - docker start container_name : 실행되지 않던 컨테이너 실행
    - docker attach contatiner_name : 실행중인 컨테이너에 접속

## 5. all-in-one
    - docker run [옵션] 이미지 [명령] : 새로운 컨테이너 생성 후 실행
        - ex) docker run -it --name container_name ubuntu:18.04 bash
    - docker exec -it container_name bash : 실행중인 컨테이너 접속

## 6. stop
    - docker stop container_name : 컨테이너 stop
    - docker restart container_name : 컨테이너 재시작

## 7. remove
    - docker rm container_name : 컨테이너 삭제

## 8. commit
    - docker commit container_name ubuntu:18.04-python3.8

## 9. volume
    - docker run -v /home/:/app -it container_name bash : 로컬의 /home 디렉토리를 컨테이너 /app에 마운트