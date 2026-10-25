
## 💼 Experience

### 이연에프엔씨 \| AI전략실 인턴

`2026.07 ~ 2026.09`

### 244개 매장 영업시간 수집·ERP DB 반영 자동화

- 2개 브랜드 244개 매장의 영업시간을 수집하고, ERP 매장코드와 Naver Place ID를 연결하는 VIEW 기반 데이터 연계 구조 구현
- 휴무·24시간 영업·익일 마감 등 예외를 정규화하고, 변경 감지 및 매장 단위 Transaction으로 206개 매장 DB 반영, 저장 오류 0건
- 네이버 플레이스 확인·엑셀 작성·SQL 갱신이 필요했던 수작업을 약 5분 내 주기적으로 실행 가능한 자동화 프로세스로 전환

### [HMR 8개 판매채널 주문 통합 데이터 파이프라인](https://github.com/Huk9uri/hmr-agent-crawling)

- 서로 다른 8개 판매채널의 API 응답을 Adapter Pattern 기반 공통 주문 스키마로 정규화하고, 신규·변경 주문의 적재 및 갱신 파이프라인 구현
- 순차 수집 구조를 최대 4개 채널 병렬 실행으로 개선하고, 실패 채널을 지연 재시도 Queue로 분리해 다른 채널의 처리 지연 방지
- 채널별 독립 Transaction으로 장애 영향을 격리하고, SQL Server Application Lock으로 정기·수동 실행 간 동일 채널 중복 적재 방지

### AI Agent 기반 Crawler Guard

- 외부 사이트 DOM 변경으로 인한 장기 수집 장애를 계기로, 실제 수집 전 파싱 이상을 탐지·차단하는 Preflight Guard 개발
- Git Worktree 기반 격리 환경에서 AI Agent의 Parser·Selector 수정 범위를 제한하고, Snapshot·현재 HTML 검증 및 담당자 승인 후 운영 반영
- 검증된 Snapshot만 Baseline으로 사용하는 구조와 실행 상태 관리·보고서 자동화를 구현해 운영 안정성과 장애 추적성 강화

### [FC다움 API 기반 가맹점 품질점검 데이터 연동](https://github.com/Huk9uri/fcdaum-crawling)

- 한촌설렁탕·육수당 가맹점의 품질점검 데이터를 **FC다움 API로 수집하고, MSSQL에 적재·갱신하는 데이터 파이프라인 구현**
- 페이지네이션 기반 전체 데이터 수집과 신규·변경 데이터 판별 로직을 구현하고, **과거 데이터 Backfill 및 매장 단위 데이터 정합성 검증**
- 점검 상태·마감 여부 등 업무 규칙을 DB VIEW로 구현하고, **매장명 표준화·실시간 마감 상태 조회·DB 정의서 작성**을 통해 운영 데이터 활용성 개선

### [데이터 수집 통합 모니터링 시스템](https://github.com/Huk9uri/collection-monitoring-platform)

- HMR 주문·매장 영업시간·리뷰 등 서로 다른 수집기의 실행 이력과 DB 적재 상태를 통합하는 모니터링 시스템 구축
- 수집기별 Adapter로 실행 결과를 공통 상태 모델로 정규화하고, 수집 성공·결과 0건·부분 실패·미실행·실패를 구분
- FastAPI 기반 읽기 전용 API와 React Dashboard를 구현해 분산된 로그·DB 확인 작업을 단일 화면으로 통합

### [Brand Analyze | POS·검색 데이터 기반 매장별 키워드 추천 자동화](https://github.com/Huk9uri/brand-keyword-analyze)

- POS·ERP 판매 데이터와 네이버 검색광고 API·DataLab·플레이스 검색 순위를 연계해 실제 판매 메뉴의 검색 수요와 매장 노출 현황을 분석하는 파이프라인 개발
- 최근 30일 판매 실적·검색량·검색 순위를 비교해 판매 중이지만 검색 결과 상위 20개에 노출되지 않는 키워드 후보 발굴, LLM으로 매장별 추천 이유 생성
- 131개 매장 대상 651건의 키워드 추천 결과 생성, SQLite 기반 결과 저장·재실행 시 재사용 및 Gmail 보고서 발송 기능 구현


### 핫셀러 \| 개발사업부 인턴

`2026.01 ~ 2026.03`

#### KeywordLog \| 브랜드 검색·평판 분석 시스템

-   마케팅 담당자가 매일 약 30분씩 수동 확인하던 검색 순위와
    블로그·카페·지식인 브랜드 언급 데이터를 **자동 수집**
-   OpenAI로 게시글의 감성·주제·광고성 여부를 분석하고 마케팅팀 피드백을
    반영해 **KPI·누적 시계열 중심 대시보드로 개선**
-   자사·경쟁사의 검색 순위·점유율 변화를 비교해 **방어/개선 및 신규
    타겟 키워드를 추천**하고 후속 대응 판단 지원

------------------------------------------------------------------------

## 🚀 Selected Work

### Bidvisor \| Frontend Leader · SSAFY Team Project

**공공입찰 데이터와 AI 문서 분석을 활용한 입찰 의사결정 지원 플랫폼**

-   팀 개발 전 pages/features 중심 디렉터리 구조와 **컴포넌트·상태관리
    기준을 설계·문서화**해 프론트엔드 개발 규칙 통일
-   OpenAI 자격요건 분석의 최대 1분 응답 지연에 TanStack Query 캐싱과 DB
    저장을 적용해 **동일 공고의 반복 API 호출·대기 제거**

`React` `TypeScript` `TanStack Query` `Zustand` `OpenAI API`

### SaveHeart \| Android / Wear OS · SSAFY Team Project

**Galaxy Watch 기반 이상 징후 감지 및 긴급 신고 서비스**

-   Wear ↔ Mobile 통신을 위해 MessageClient의 기능별 **Path 규약과 단일
    Listener 구조를 직접 설계·문서화**
-   Android 백그라운드 제약으로 BroadcastReceiver가 동작하지 않는 문제를
    분석해 **Listener → ForegroundService 직접 실행 구조로 변경**

`Android` `Wear OS` `MessageClient` `Room` `ForegroundService`

> SSAFY 프로젝트는 GitLab을 통해 협업했습니다.
------------------------------------------------------------------------

## 🛠 Tech Stack

### Backend / Data

`Python` `FastAPI` `Java` `Spring Boot` `PostgreSQL` `MySQL`

### Frontend

`React` `TypeScript` `TanStack Query` `Zustand`

### Automation / AI

`Requests` `Playwright` `OpenAI API` `Codex CLI`

### Tools

`Git` `GitHub` `Jira` `Postman`

------------------------------------------------------------------------

## 🚶‍♂️ Journey

### 명지대학교 \| 경영정보학과

`2018.03 ~ 2024.02` 
- 비즈니스 데이터 분석, ERP, 프로그래밍 학습

### 멀티캠퍼스 \| 백엔드(Java) 개발자 부트캠프

`2023.09 ~ 2024.01` 
- Java·Spring 기반 서버 구조 및 REST API 개발 학습

### 삼성 청년 소프트웨어 아카데미 (SSAFY) 12기

`2024.07 ~ 2025.06` 
- React·TypeScript 기반 Frontend와 Java·Spring Boot 기반 Backend 개발
- 팀 프로젝트에서 UI 구조 설계, 데이터 흐름 정리 및 기능 단위 협업
- 공공입찰 분석 플랫폼, 스마트 약속 관리 앱, Wear OS 기반 긴급 알림 시스템 개발

------------------------------------------------------------------------

