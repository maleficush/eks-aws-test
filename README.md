eksctl create cluster \
--vpc-public-subnets subnet-078f72bcc89832f0a,subnet-06f623b41bd514511,subnet-01a427bfc1fb2462a \
--name eks-work-cluster \
--region ap-northeast-2 \
--version 1.23 \
--nodegroup-name eks-work-nodegroup \
--node-type t2.small \
--nodes 2 \
--nodes-min 2 \
--nodes-max 5

eksctl delete cluster --name eks-work-cluster




# 『클라우드 네이티브를 위한 쿠버네티스 실전 프로젝트: 아마존 EKS로 배우는 데브옵스 및 IaC 기반 서비스 배포와 관리』

동양북스 『클라우드 네이티브를 위한 쿠버네티스 실전 프로젝트』의 깃허브 저장소입니다.

<img src="./readme/cover.jpg" width="400" height="544">

## 구매하기
[교보문고](https://bit.ly/35muioQ) | [YES24](https://bit.ly/3vvGMVW) | [알라딘](https://bit.ly/3gAcLyt) | [인터파크](https://bit.ly/3pSAY7z) | [반디앤루니스](https://bit.ly/3iLJyU3)

## 책 소개
**애플리케이션 엔지니어도 쉽게 배우는 실전 쿠버네티스 프로젝트를 만난다!**

클라우드 컴퓨팅, 컨테이너, 쿠버네티스라는 세 가지 인프라 관련 기술이 등장하면서 최신 서비스 개발 환경은 클라우드 네이티브와 데브옵스(DevOps)를 향해 빠르게 움직이고 있다. 이제는 애플리케이션 엔지니어도 세 가지 기술을 어느 정도 이해해 더 나은 개발 효율을 추구해야 할 시대다. 하지만 애플리케이션 엔지니어가 인프라 엔지니어처럼 최신 인프라 기술을 심도 있게 배우는 것은 부담되는 일이다. 핵심만 빠르게 이해하고 실제 서비스 배포 환경의 운용 기술을 익히는 요령이 필요하다.

이 책은 전 세계에서 가장 점유율이 높은 클라우드 컴퓨팅 서비스인 아마존 웹 서비스에서 쿠버네티스 기반으로 애플리케이션 서비스를 직접 구축하는 과정을 설명한다. 이를 통해 애플리케이션 엔지니어에게 필요한 컨테이너 기반의 개발 프로세스와 쿠버네티스 운용 방법의 핵심을 자연스럽게 익힐 수 있다. 또한 기존에 EC2(Elastic Computing Cloud) 기반으로 클라우드 컴퓨팅을 활용했던 아마존 웹 서비스 엔지니어라면 Amazon EKS 기반의 쿠버네티스 운용 방법에 대한 기초를 익힐 수 있다.

클라우드 네이티브와 데브옵스 기반의 서비스에서 개발 환경에 입문했다면 이 책과 함께 효율적인 개발 환경을 어떻게 구축하고 운용하는지 직접 경험해보기 바란다.
## db-docker-compose 디렉터리에 대하여

db-docker-compose 디렉터리는 개발 환경에서 애플리케이션을 테스트하기 위해 사용한다. docker-compose용 설정 파일과 데이터베이스 사용자를 위한 데이터베이스 생성용 스크립트를 저장하고 있다. 해당 디렉터리는 이 책에서 ㅈ빅접 사용하지 않지만 개발 환경에서 애플리케이션을 동작시킬 때 사용하기 바란다.

사용 방법은 아래와 같다. db-docker-comopse 디렉터리에 복사하여 실행하자.

### 데이터베이스 실행

```
$ docker-compose up -d
```

### 데이터베이스 정지

```
$ docker-compose down
```

### 데이터베이스 사용자 생성

```
$ ./createuser.sh
```

### 데이터베이스 생성

```
$ ./createdb.sh
```

## 기타 사항
정오표는 [이곳](./readme/errata/errata.md)을 참고하기 바란다.
