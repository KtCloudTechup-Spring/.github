# 🚀 TechUp Challenger Hub

---

## 1. 프로젝트 개요

**TechUp Challenger Hub**는  
부트캠프, 스터디, 학습 과정에서 발생하는 **분산된 커뮤니케이션 문제를 해결하기 위한 통합 커뮤니티 플랫폼**입니다.

과정별 커뮤니티, 게시판, 실시간 채팅을 하나의 서비스로 제공하여  
학습자 간 정보 공유와 협업 효율을 높이는 것을 목표로 합니다.

---

## 2. 프로젝트 소개

부트캠프 및 학습 과정에서는 다음과 같은 문제가 반복적으로 발생합니다.

- 학습 정보가 여러 툴(Slack, Notion, Discord 등)에 흩어짐
- 게시글, 댓글, 실시간 대화가 하나의 흐름으로 이어지지 않음
- 개인이 참여한 활동을 체계적으로 관리하기 어려움

**TechUp Challenger Hub**는  
👉 *과정별 커뮤니티 + 게시판 + 실시간 채팅*을 결합하여  
이러한 문제를 해결하는 **학습 협업 플랫폼**입니다.

---

## 3. 프로젝트 목표

- 과정·주제별 커뮤니티 분리로 정보 탐색 효율 향상
- 게시글 + 댓글 + 좋아요 기반 비동기 소통 지원
- WebSocket 기반 실시간 채팅으로 즉각적인 의견 교환
- Redis Pub/Sub을 활용한 **확장 가능한 실시간 채팅 구조 설계**
- 개인 활동 이력 관리 기능 제공

---

## 4. 주요 기능

### 🔐 사용자 인증
- 회원가입 / 로그인 / 로그아웃
- JWT 기반 인증 및 인가
- HttpOnly 쿠키 사용

### 📝 게시판
- 커뮤니티별 게시글 CRUD
- 게시글 이미지 업로드 (AWS S3)
- 게시글 검색 (제목 / 작성자)
- 정렬 기능
  - 최신순
  - 인기순(좋아요 기준)

### ❤️ 댓글 & 좋아요
- 댓글 작성 / 삭제
- 게시글 좋아요 / 좋아요 취소
- 좋아요 수, 댓글 수 집계

### 👤 마이페이지
- 개인정보 수정
- 내가 작성한 게시글 목록 조회

### 💬 실시간 채팅
- WebSocket(STOMP) 기반 양방향 채팅
- 채팅 메시지 DB 영속화
- Redis Pub/Sub을 이용한 **멀티 서버 메시지 동기화**
- 참여 중인 채팅방 조회

---

## 5. 팀원 소개

| 이름 | 역할 |
|------|------|
| 김민기 | Backend 개발, WebSocket, Redis, AWS Infra |
| (추가 가능) | Frontend / Design |

---

## 6. 기술 스택

### Frontend
- Next.js
- TypeScript
- Tailwind CSS
- STOMP.js / SockJS

### Backend
- Spring Boot 3
- Spring Security
- JWT
- Spring Data JPA
- Spring WebSocket (STOMP)

### Database & Cache
- MySQL (AWS RDS)
- Redis (Pub/Sub)

### Infra
- AWS EC2
- AWS S3
- AWS RDS
- Nginx
- Docker (Redis)

### Collaboration
- GitHub
- Notion

---

## 7. 문서 자료

- 📄 프로젝트 계획서
- 📄 중간 발표 자료
- 📊 ERD
- 🏗 시스템 아키텍처 다이어그램

---

## 8. 실행 가이드

### Backend 실행

```bash
./gradlew bootRun
