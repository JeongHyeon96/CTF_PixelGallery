# CTF_PixelGallery_TeamEN

> Team EN이 제작한 CTF(해킹 문제 풀이) 스타일 웹 갤러리 프로젝트입니다.

---

## 🎯 프로젝트 소개

**Pixel Gallery**는 실제 웹 해킹 시나리오를 반영한 CTF 스타일의 워게임 플랫폼입니다.  
WordPress, FTP, SSH 환경을 활용해 다양한 취약점을 학습할 수 있도록 문제를 구성하였습니다.

이 프로젝트는 정보보안 교육, CTF 연습, 또는 모의 해킹 연습을 목적으로 개발되었습니다.

---

## 🔧 주요 기능

- 🕵️ **웹사이트 소스코드와 숨겨진 힌트 분석**
  - HTML 주석, base64, QR코드, brainfuck 등의 암호 해석 포함
- 📷 **스테가노그래피 (이미지 속 정보 추출) 활용**
  - 이미지에 숨겨진 정보를 `stegseek`으로 분석하여 단서 확보
- 🔎 **디렉토리 브루트포싱 및 워드프레스 구조 분석**
  - gobuster를 활용하여 `wp-content` 등 주요 경로 탐색
- 📑 **워드리스트를 이용한 파일 및 경로 추적**
  - `.secretmsg.txt`, `r3ward.txt` 등의 힌트 파일 획득
- 🎮 **웹 기반 점프 게임에서 힌트 추출**
  - 점수 달성 시 수상한 숫자(HEX)를 통해 추가 경로 추리
- 🔐 **SSH 계정 크래킹 및 접속**
  - `hydra` 툴로 사용자 계정과 비밀번호 조합 탐색
- 🗂️ **파일 탐색을 통한 플래그 수집**
  - 특정 디렉토리 내 `memo.txt`, `userflag1.txt` 등의 파일 분석
- 🧪 **SQL Injection 취약점 활용**
  - 로그인 페이지에서 `' OR 1=1 --` 입력으로 우회
- 📤 **FTP 익명 접속 및 웹쉘 업로드**
  - `webshell.php` 업로드 후 웹 명령 실행(RCE 시나리오)
- 🧩 **포트 스캐닝 및 knock 패턴을 통한 포트 오픈**
  - `knock.sh` 스크립트로 숨겨진 21번 포트(FTP) 열기
- 🧬 **웹쉘과 경로 조작으로 플래그 획득**
  - 업로드한 웹쉘을 통해 시스템 내 파일 탐색 및 출력
- ⚙️ **트리거를 통한 루트 권한 획득**
  - nc로 특정 포트(8888)에 연결하여 트리거 실행 → `root_me` 실행

---

## 🧠 팀원 및 역할

| 이름       | GitHub ID         | 역할 설명                               |
|------------|------------------|----------------------------------------|
| 김정현     | [JeongHyeon96](https://github.com/JeongHyeon96) | 워드프레스, FTP 서버, SQLI, 웹쉘 취약점페이지 구성     |
| 조범근    | (GitHub ID)       | hydra툴을 사용할 수 있도록 취약한 웹사이트 구성, WorkThrough 작성, 전체적인 시나리오 구성          |
| 김병욱    | (GitHub ID)       | SSH ROOT 권한 상승 및 트리거 설계 등    |

> 전체 역할 정리는 [docs/team_roles.md](docs/team_roles.md) 참고

---

## 📂 디렉토리 구조

```bash
CTF_PixelGallery_TeamEN/
│
├── README.md
├── docs/
│   ├── architecture.png        # 시스템 구성도
│   ├── team_roles.md           # 팀원 역할 문서
│   └── walkthroughs/
│       ├── junghyun01.md 등    # 문제별 풀이 정리
│
├── src/
│   ├── wordpress/              # 워드프레스 관련 구성
│   ├── ftp_server/             # FTP 관련 문제
│   └── ssh_challenges/         # SSH 탈출 및 권한 상승
│
├── api/                        # PHP API 코드
│   └── check.php
│
├── html/                       # 메인 및 문제 페이지들
│   ├── main.html
│   └── junghyun01.html 등
│
├── assets/
│   └── css/
│       └── hacker.css          # 공통 CSS
│
└── LICENSE                     # 오픈소스 라이선스 (MIT 등)


---

## 💾 가상머신 다운로드

프로젝트 테스트를 위해 사용된 OVA 파일은 아래 링크를 통해 다운로드하실 수 있습니다:

👉 [PixelGallery_VM.ova 다운로드](https://drive.google.com/file/d/1_gizfkVfZi1t7p3K2RI9asCyjgrrKsUH/view?usp=sharing)

---

## 🚀 실행 방법
Oracle VM VirtualBox 환경 
OVA 파일 가져오기 -> 네트워크: 호스트전용 -> nmap 스캐닝으로 시작

---

## 📸 스크린샷
추후 추가 예정입니다.

---

## 📄 라이선스
Wordpress

---
🙌 즐겁게 해킹하세요!
