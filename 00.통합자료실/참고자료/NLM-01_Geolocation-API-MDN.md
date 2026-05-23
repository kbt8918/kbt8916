# NLM-01: Geolocation API 사용하기 - MDN Web Docs

> 원본 URL: https://developer.mozilla.org/ko/docs/Web/API/Geolocation_API/Using_the_Geolocation_API
> 출처: developer.mozilla.org
> 수집일: 2026-05-23
> NotebookLM 소스 유형: web_page

---

브라우저에서 Geolocation API를 사용하여 사용자의 현재 위치를 가져오는 방법을 설명하는 MDN 공식 문서.

주요 내용:
- `navigator.geolocation.getCurrentPosition()` — 현재 위치 1회 조회
- `navigator.geolocation.watchPosition()` — 위치 변화 지속 감지
- `PositionOptions`: `enableHighAccuracy`, `timeout`, `maximumAge` 설정
- HTTPS 환경에서만 동작 (보안 컨텍스트 필수)
- 위치 권한 요청 흐름 및 오류 처리 (`PERMISSION_DENIED`, `POSITION_UNAVAILABLE`, `TIMEOUT`)

프로젝트 적용 포인트:
- 부모님 스마트폰 브라우저에서 30초 간격 GPS 전송 시 `watchPosition` 활용
- HTTPS 필수 조건 — Vercel 배포로 자동 충족
