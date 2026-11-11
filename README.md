# Codyssey Pre-course

## 1. 프로젝트 개요

Codyssey 입학연수 과정에서 Ubuntu, Linux, Docker, Git 및 GitHub의 기본 사용법을 학습하고 실습한 프로젝트입니다.

## 2. 실습 환경

- Windows + WSL2
- Ubuntu 26.04 LTS
- Docker Engine
- Git 2.53.0
- GitHub

## 3. 주요 실습 내용

### Linux 기본 명령어
- 디렉터리 생성 및 이동
- 파일 생성, 복사, 이동, 삭제
- 파일 및 디렉터리 권한 확인
- 터미널 실행 기록 저장

### Docker
- Docker 설치 및 Hello World 실행
- Ubuntu 컨테이너 생성 및 관리
- Dockerfile을 이용한 NGINX 웹 서버 구축
- 8080, 8081 포트 매핑
- 바인드 마운트로 HTML 파일 변경 반영
- Docker 볼륨 데이터 영속성 검증

### Git 및 GitHub
- Git 사용자 정보 설정
- 로컬 Git 저장소 생성
- .gitignore 작성
- 첫 커밋 생성
- GitHub 원격 저장소 연결 및 Push

## 4. Docker 웹 서버 실행

프로젝트 폴더에서 다음 명령어를 실행합니다.

```bash
cd my-web
sudo docker build -t codyssey-web:1.0 .
sudo docker run -d -p 8080:80 --name codyssey-web codyssey-web:1.0
```

웹 브라우저에서 http://localhost:8080 접속

참고: 동일한 이름의 컨테이너가 이미 존재하면 새 컨테이너를 생성하기 전에 기존 컨테이너 상태를 확인해야 합니다.

## 5. Docker 볼륨 실습 결과

`codyssey-data` 볼륨을 생성하고 컨테이너 A에서 파일을 저장했습니다.

이후 컨테이너 A를 삭제하고 동일한 볼륨을 연결한 컨테이너 B에서 파일을 확인했습니다.

결과:

```text
Codyssey Volume Success
```

컨테이너를 삭제해도 볼륨에 저장된 데이터가 유지되는 것을 확인했습니다.

## 6. 프로젝트 저장소

https://github.com/sukwonji77-svg/codyssey-pre-course

## Git Branch Practice
Practicing Git branches and pull requests.
