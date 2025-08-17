# Weverse 커뮤니티 & 샵 프로젝트 🎶🛒
Idol-Community(Next.js+Springboot)

**Spring Boot + JPA** 기반으로 구현한 팬 커뮤니티 & 커머스 통합 플랫폼 프로젝트입니다.  
아티스트와 팬이 소통하고, 콘텐츠 공유·상품 구매까지 가능한 환경을 학습 목적으로 구현했습니다.

---

## 📌 주요 기능

- **아티스트 커뮤니티**
  - 게시글(Story) 작성/조회/댓글
  - 팬레터, 게시판 기능
- **팬-아티스트 상호작용**
  - DM(Direct Message) / 이벤트 / 멤버십
- **Weverse Shop**
  - 상품 목록 / 상품 상세 조회
  - 옵션별 가격, 재고 조회
  - 공지사항 및 배너 노출
- **관리자 기능(확장 예정)**
  - 아티스트, 그룹, 상품, 카테고리 관리

---

## 🛠 기술 스택

- **Backend**: Spring Boot 3.x, Spring Data JPA, Hibernate
- **DB**: MySQL 8.x
- **Build**: Gradle
- **Test**: JUnit5
- **ORM 편의**: Lombok
- **보안**: Spring Security (JWT 인증 확장 예정)

---

## 📂 프로젝트 구조

<img width="408" height="624" alt="image" src="https://github.com/user-attachments/assets/43af5df1-874e-4f61-804d-62c496210ba0" />


---

## 🔗 API 엔드포인트 예시

| 메서드 | 경로                    | 설명                     |
|--------|--------------------------|--------------------------|
| GET    | `/api/main/artist`       | 메인 아티스트 목록 조회   |
| GET    | `/api/shop/main`         | 샵 메인 데이터(배너/상품) |
| GET    | `/api/shop/product/{id}` | 상품 상세 조회           |
| GET    | `/api/story/{id}`        | 스토리 상세/댓글 조회     |
| POST   | `/api/story`             | 스토리 등록              |

---

## 🗄 DB 주요 테이블

- **Artist, Group**: 아티스트/그룹 정보
- **Product, ProductCategory, ProductImage, ProductOption**: 상품/카테고리/옵션 구조
- **Story, StoryComment**: 게시글/댓글
- **User**: 사용자
- **Media**: 스트리밍, 업로드 동영상
- **Notice**: 샵 공지사항

---

## ▶ 실행 방법

1. **환경 준비**
   - JDK 
   - MySQL (DB명: `weverse_db`)
   - Gradle 

2. **DB 설정**
   - `application.yml`에 DB 계정/비밀번호 설정
   - `spring.jpa.hibernate.ddl-auto=update` 로 스키마 자동 생성

3. **빌드 & 실행**
   - junit test
   - front 실행
