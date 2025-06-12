# Docker Image

## Image 다운로드


```bash
docker pull "이미지명"
ex) docker pull nginx
```

이미지를 다운로드 할 때 Dockerhub이라는 곳에서 이미지를 다운 받음

[Docker Hub Container Image Library | App Containerization](https://hub.docker.com/)

→ Dockerhub: 이미지를 저장 및 다운받을 수 있는 저장소 역할

<br>

특정 버전 이미지 다운로드

```bash
docker pull "이미지명:태그명"
```
<br>

## Image 조회 / 삭제


### 다운로드 받은 모든 이미지 조회

```bash
docker image ls
```


- `REPOSITORY`: 이미지명
- `TAG`: 이미지 태그
- `IMAGE` ID: 이미지 ID
- `CREATED`: 이미지가 생성된 날짜(다운받은 날짜 X)
- `SIZE`: 이미지 크기

<br>

### 이미지 삭제

```bash
docker image rm "이미지 ID 또는 이미지명"
```
<br>

만약 다른 컨테이너에서 사용중이라 지우지 못한다는 에러가 뜬다면 다음 명령어를 치면됨

```bash
docker image rm -f "이미지ID"
```
- `-f` : 중단된 컨테이너 이미지만 삭제할 수 있음

<br>

### 사용하고 있지 않은 이미지 전체 삭제

```bash
docker image rm $(docker images -q)
```

중단된 컨테이너도 다 삭제하려면 `-f` 붙이면 됨
