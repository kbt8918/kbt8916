# NLM-02: WebSocket보다 SSE가 더 적합했던 이유 – 실시간 입찰 시스템

> 원본 URL: https://miloserdov.org/ (티스토리 블로그 — 진공청소ㄱl)
> 출처: 티스토리 블로그
> 수집일: 2026-05-23
> NotebookLM 소스 유형: web_page

---

실시간 입찰 시스템 구현 사례에서 WebSocket 대신 SSE(Server-Sent Events)를 선택한 이유를 분석한 기술 블로그.

주요 내용:
- SSE는 단방향(서버→클라이언트) 통신에 최적화
- WebSocket은 양방향 통신 필요 시 적합, 구현 복잡도 높음
- SSE는 HTTP/1.1 기반으로 별도 프로토콜 업그레이드 불필요
- Vercel/AWS Lambda 등 서버리스 환경에서 SSE가 더 호환성 높음
- 자동 재연결 기능 내장 (`EventSource` API)

프로젝트 적용 포인트:
- M1~M4 단계에서 Vercel Lambda WebSocket 미지원 문제를 SSE로 해결
- 위치 갱신(서버→클라이언트 단방향)은 SSE로 충분
