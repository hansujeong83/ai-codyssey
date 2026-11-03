# AI Codyssey

깃허브와 코디세이를 연동하기 위해 만들어진 Repository입니다.

## Docker 실습 미션
이 저장소는 AI Codyssey Docker 실습 내용을 정리하기 위한 저장소입니다.

---

## 1단계: Docker 설치 확인

### 실행 명령어

```bash
docker --version
```

### 문제 원인
Docker Desktop 실행 시 `Virtual Machine Platform is not enabled` 메시지가 표시되었다.

### 조치
관리자 PowerShell에서 아래 명령어를 실행했다.

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
```

이후 Windows를 재부팅했다.

### 실행 결과 확인

```powershell
docker ps
docker info
```

`docker ps` 명령어가 정상 실행되었고, 실행 중인 컨테이너는 없었다.

`docker info` 결과에서 `Server` 정보가 출력되어 Docker 엔진이 정상적으로 동작함을 확인했다.

### 결과
`Virtual Machine Platform` 기능을 활성화한 뒤 재부팅하여 Docker가 정상 실행되는 것을 확인했다.
## 2단계: Docker 실행 테스트

### 실행 명령어

```powershell
docker run hello-world
```

### 실행 결과
Docker가 `hello-world` 이미지를 내려받은 뒤 컨테이너를 실행했고, `Hello from Docker!` 메시지가 출력되었다.

### 결과
Docker 컨테이너가 정상적으로 실행되는 것을 확인했다.
## 2단계: Docker 실행 테스트

### 실행 명령어

```powershell
docker run hello-world
```

### 실행 결과

`Hello from Docker!` 메시지가 출력되었고, Docker가 `hello-world` 이미지를 내려받아 컨테이너를 정상적으로 실행한 것을 확인했다.

### 결과

Docker 설치 및 실행 환경이 정상적으로 동작함을 확인했다.

## 3단계: 실행 결과 확인

```powershell
docker ps -a
docker images
```

`hello-world` 컨테이너와 이미지가 목록에 표시되는 것을 확인했다.
## 3단계: 컨테이너와 이미지 확인

### 실행 명령어

```powershell
docker ps -a
docker images
```

### 실행 결과

`hello-world` 컨테이너와 `hello-world` 이미지가 목록에 표시되는 것을 확인했다.

### 결과

Docker가 정상적으로 컨테이너를 생성하고 이미지를 내려받아 관리할 수 있음을 확인했다.
