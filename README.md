# 이우진

운영 데이터를 연결한 LLM 파이프라인을 설계하고 배포까지 검증하는 백엔드 개발자입니다.

포트폴리오 `[NOTION_URL]` · [이메일](mailto:lebind12@naver.com)

## 대표 프로젝트

### [BenchMark](https://github.com/lebind12/benchmarkV3) · [라이브 데모](https://benchmark-v3-steel.vercel.app)

경기 기록과 외부 근거를 모아 축구 팬을 위한 프리뷰와 방송용 정보 화면을 제공합니다.

- 운영 경기·계정 데이터는 읽고, 프리뷰 실행 기록과 결과는 `preview_dev`에 저장합니다.
- LangGraph에서 근거 조사와 섹션 작성을 분리하고 모델 호출에 재시도 예산을 적용했습니다. [구현 문서](https://github.com/lebind12/benchmarkV3/tree/main/docs/portfolio)
- FastAPI · LangGraph · Supabase(PostgreSQL) · Vertex AI · Vue

### [TourDoum](https://github.com/lebind12/TourDoum)

여행 예약 상태를 추적하고 예약과 알림 이벤트를 같은 트랜잭션에 기록하는 플랫폼입니다.

- Outbox Publisher는 `SKIP LOCKED`로 처리할 이벤트를 가져오고 실패 시 백오프를 적용합니다.
- 로컬 단일 Pod에서 예약 생성 [416 RPS, p95 1.25초](https://github.com/lebind12/TourDoum/blob/develop/docs/notes/2026-05-08-qa-k6-1-phase1-rerun3-be131.md)를 기록했습니다. Outbox 배치를 50개에서 200개로 늘리자 [이벤트 처리량이 초당 70건에서 147건으로 증가](https://github.com/lebind12/TourDoum/blob/develop/docs/notes/2026-05-08-qa-stage-latency-trend.md)했습니다.
- Java 21 · Spring Boot 3 · JPA · Redis · k6

### [System Design Practice](https://github.com/lebind12/system-design-practice)

시스템 설계 실습 11개를 구현했습니다. 요청 제한 알고리즘 4종을 비교하고, 인스턴스 2개에서 Redis로 할당량을 공유하는 방식을 검증했습니다. [처리율 제한 실험](https://github.com/lebind12/system-design-practice/tree/main/rate-limiter)

## 그 밖의 작업

| 프로젝트 | 내용 | 기술 |
| --- | --- | --- |
| [JPA_Visualize](https://github.com/lebind12/JPA_Visualize) | N+1과 OSIV 사례의 SQL, 쿼리 수, 실행 시간 비교 | Spring Data JPA · MySQL · React · Testcontainers |
| [Code Playground](https://github.com/lebind12/code-playground) | 알고리즘 풀이 게임의 개인 제출과 채점 큐 개발 중 | Django Channels · FastAPI · RabbitMQ |

## 기술

Java · Spring Boot · JPA / Python · FastAPI · Django / PostgreSQL · MySQL · Redis · RabbitMQ / Docker · k6 · Azure Bicep

## 경력·교육

- 메트릭스튜디오 백엔드 · 2021.09–2022.08 · AWS Lambda · DynamoDB · OpenSearch · SQS
- SSAFY 13기 · K-Digital AI 데브코스 · 42 Seoul · 숭실대학교 컴퓨터학부
