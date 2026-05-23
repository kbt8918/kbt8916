# NLM-03: [REDIS] Node.js에서 redis 모듈 사용법 (캐싱 & 세션 스토어)

> 원본 URL: https://inpa.tistory.com/
> 출처: inpa.tistory.com (Inpa Dev)
> 수집일: 2026-05-23
> NotebookLM 소스 유형: web_page

---

Node.js 환경에서 Redis 클라이언트 모듈을 사용하는 방법을 정리한 기술 블로그.

주요 내용:
- `redis` npm 패키지 설치 및 연결 설정
- `SET` / `GET` / `DEL` 기본 명령어
- TTL(Time To Live) 설정으로 자동 만료 구현
- 캐싱 패턴: cache-aside(look-aside) 전략
- 세션 스토어로 Redis 활용 방법

프로젝트 적용 포인트:
- 실시간 위치 데이터 캐싱 (30초 TTL) — 부모님 최신 위치를 Redis에 저장
- DB 조회 없이 빠른 위치 응답 제공
- `SET location:{userId} {lat,lng} EX 30` 패턴 적용 예정
