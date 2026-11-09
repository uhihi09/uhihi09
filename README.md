# 배준하 · Junha Bae

병목을 찾아 수치로 개선하는 백엔드 개발자입니다.<br>
FastAPI와 Spring Boot로 서버를 만들고, 운영 로그로 지연을 계측해서 고칩니다.

대구소프트웨어마이스터고 인공지능소프트웨어과 2학년<br>
[Portfolio](https://uhihi09.github.io/portfolio/) · [Baekjoon](https://solved.ac/profile/uhihi) · [junhabae0729@gmail.com](mailto:junhabae0729@gmail.com)

## 지금 하는 일

- **바다** AI 전화 훈련 앱의 실시간 음성통화 서버를 운영합니다. 11월에는 웨어러블 생체신호(HRV·EDA·PPG) 분석 API를 운영 서버에 붙였습니다.
- **두깨비** DUCAMI 10기 부장으로, 동아리 온라인 저지를 처음부터 다시 만드는 일을 이끌고 있습니다. 12월 마무리가 목표입니다.
- **논문** 머신러닝 기반 리눅스 스케줄러 정책 선택 연구를 투고 준비 중입니다.

## 프로젝트

### 바다 — 콜포비아 극복 AI 전화 훈련 앱

2026.03 – 진행 중 · 2학년 나르샤 · 백엔드 팀장 (6명) · [서버 코드](https://github.com/ChickenMayoDeopbab/BADA_FASTAPI_SERVER) · [Google Play](https://play.google.com/store/apps/details?id=com.chickenmayodeopbab.bada.play)

STT → LLM → TTS를 하나의 WebSocket 세션에서 스트리밍하는 FastAPI 실시간 음성통화 서버를 설계하고 운영합니다.

- 통화 첫 턴 응답 2,437ms → 1,320ms. 구간별 지연을 계측해 78%가 LLM 첫 토큰 대기임을 찾고, 연결 직후 LLM을 미리 깨웠습니다.
- 학교 GPU 서버에 Qwen3-TTS 워커 풀을 만들고 ElevenLabs 폴백을 두어, 동시 통화를 1 → 4로 늘렸습니다.

### GrowMoney — 청소년 경제 학습 플랫폼

2025.07 – 2025.12 · 1학년 나르샤 · 개발팀장 (7명) · [GitHub](https://github.com/Team-Oh-Yes)

Spring Boot 백엔드 API와 MySQL 스키마를 설계하고, 팀원들에게 Git 워크플로우를 가르쳤습니다.

- JPA N+1을 Fetch Join으로 풀어 쿼리 100+ → 1~3개, 응답 320ms → 64ms.
- GitHub Actions 자동 배포로 배포 시간 30분 → 3분.

### 머신러닝 기반 리눅스 스케줄러 정책 선택 — 개인 연구

2025.11 – 진행 중 · 투고 준비 중 · [논문 초안](https://junha-research.notion.site)

결정 트리로 워크로드를 분류하고, 커널 수정 없이 nice 값과 스케줄링 클래스를 바꿔 정책을 적용합니다.

- 16개 합성 워크로드 실험에서 분류 정확도 85%, 작업 완료 시간 3.8s → 2.75s (28% 단축).

### 그 외

- **A&K Systems** 실리콘밸리 온라인 인턴십, 백엔드 인턴 (2026.01 – 2026.02). 기술 문서 PDF를 교육용 슬라이드로 바꾸는 AI 파이프라인에서 이미지 검색을 파일명 일치에서 sentence-transformers 시맨틱 검색으로 바꿨습니다.
- **[harness-cli](https://github.com/uhihi09/harness-cli)** AI 코딩 에이전트용 하네스(plan → construct → test, 검증 게이트)를 명령 하나로 까는 CLI. v0.6.0
- **알고리즘** 백준 Gold 4, 750문제

## 기술

- **Backend** FastAPI (Python), Spring Boot · JPA (Java)
- **Data** PostgreSQL, MySQL, Redis
- **Infra** Docker, GitHub Actions, AWS (EC2, S3)
- **Realtime / AI** WebSocket 스트리밍, STT·LLM·TTS 연동, scikit-learn

## 활동 · 수상 · 자격

DUCAMI 코딩 교육봉사 동아리 10기 부장 · 1학년 GitHub 멘토링 · 중학생 대상 Python 진로체험 강사

- 2026.06 제8회 교육 공공데이터 AI활용대회 우수상
- 2025.11 SQLD 취득 · TOPCIT 3수준
- 2025.10 대구-광주 달빛연합 SW융합 학생 해커톤 창의상
- 2025.07 청춘어람 프로젝트 Newrrow 최우수상
- 2025.07 교내 노벨 엔지니어링 해커톤 장려상
