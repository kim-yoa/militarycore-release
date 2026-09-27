# 🎖️ MilitaryCore Releases (밀리터리코어 공식 배포 저장소)

![Minecraft](https://img.shields.io/badge/Minecraft-1.21.11-brightgreen)
![NeoForge](https://img.shields.io/badge/NeoForge-21.11.45-orange)
![Version](https://img.shields.io/badge/Latest-v1.2.1--b116-blue)

**MilitaryCore**의 공식 빌드 파일 배포 및 패치노트 전용 공개(Public) 저장소입니다.  
최신 버전의 클라이언트 및 서버 모드 파일은 우측 **[Releases](https://github.com/kim-yoa/militarycore-release/releases)** 탭에서 누구나 자유롭게 다운로드하실 수 있습니다.

---

## 📥 다운로드 안내 (Downloads)

👉 **[최신 버전 (v1.2.1) 릴리즈 다운로드 바로가기](https://github.com/kim-yoa/militarycore-release/releases)**

| 구분 | 파일명 | 용량 | 다운로드 대상 |
| :--- | :--- | :--- | :--- |
| **클라이언트용 (Client)** | `militarycore-client-1.2.1-b116.jar` | **~104 MB** | **모든 플레이어** (마인크래프트 `mods/` 폴더에 설치) |
| **서버용 (Server)** | `militarycore-server-1.2.1-b116.jar` | **~193 KB** | **서버 관리자/호스팅** (서버 `mods/` 폴더에 설치) |

---

## 📖 v1.2.1 주요 업데이트 내역

### 1. 커스텀 책 GUI 및 책과 깃펜 텍스처 탑재
- **커스텀 책 GUI 리소스 오버라이드**: 게임 내 책(Book & Quill / Written Book) 인터페이스에 맞춤형 GUI 텍스처 반영
- **커스텀 책과 깃펜(Book and Quill) 아이템 텍스처 적용**: 고해상도 32x32 맞춤형 아이템 텍스처 적용

---

## 🎬 v1.2.0 주요 업데이트 내역

### 1. GPU 하드웨어 가속(HW Decoder) 탑재
- C/C++ 네이티브 FFmpeg 비디오 엔진 도입으로 그래픽카드 하드웨어 가속 지원
  - **Windows**: DirectX 11 (`D3D11VA`) GPU 가속 디코딩
  - **macOS**: Apple Silicon (`VideoToolbox`) 하드웨어 가속 디코딩
- CPU 점유율을 대폭 낮추고 1080p FHD 영상의 60fps 무지연 재생 지원

### 2. 쉐이더(Shader) 환경 및 오디오 싱크 밀림 방지
- **오디오 마스터 클록 실시간 동기화 (Hard Catch-up)**: 쉐이더나 순간적인 렉으로 프레임 드랍이 발생해도 오디오와 화면 싱크가 절대 밀리지 않고 즉시 따라붙음
- **GPU 텍스처 중복 업로드 방지 (FPS 독립화)**: 실제 영상 프레임(PTS) 갱신 시에만 GPU로 전송하여 GPU 대역폭 병목 최소화

### 3. 사운드 설정 실시간 연동
- 마인크래프트 `설정 ➔ 음악 및 소리`의 **주 음량** 및 **주크박스/소리 블록** 슬라이더와 실시간 동기화

### 4. 서버 / 클라이언트 분리 경량화
- **서버용**: 미디어/디코더 라이브러리를 제외한 170KB 초경량 빌드로 서버 메모리 부하 제로
- **클라이언트용**: 플랫폼별 네이티브 바이너리가 번들링되어 별도 프로그램 설치 없이 즉시 실행 가능

---

## 📜 기본 명령어 요약

- `/screen create [너비] [높이]` : 대형 전광판 설치
- `/screen list` : 전광판 목록 확인 및 클릭 조작
- `/screen select [번호|all]` : 조작할 전광판 선택
- `/screen sync [기준번호] [대상번호...]` : 스크린 간 화면 복제 동기화 (예: `/screen sync 1 2 3`)
- `/screen unsync [번호|all]` : 스크린 동기화 해제 및 독립 상태로 분리
- `/video play [영상명]` : 전광판에 비디오 재생 (예: `/video play 전우`)
- `/video stop` : 비디오 재생 중지
- `/slide open [슬라이드명]` : PT 발표 슬라이드 쇼 열기
- `/militarycore time info` : KST 현실 시간 및 일출/일몰 태양주기 정보 확인

---

## 📄 라이선스 (License)
All Rights Reserved © kimyoa.
