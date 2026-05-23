# NLM-05: [Supabase] Realtime 사용하기

> 원본 URL: https://rlawo32.tistory.com/
> 출처: rlawo32.tistory.com (성장을 기록하는 곳)
> 수집일: 2026-05-23
> NotebookLM 소스 유형: web_page

---

Supabase Realtime 기능을 사용하여 DB 변경 사항을 실시간으로 구독하는 방법.

주요 내용:
- `supabase.channel()` — 채널 생성 및 구독
- `postgres_changes` 이벤트: INSERT, UPDATE, DELETE 감지
- Row Level Security(RLS)와 Realtime 연동 주의사항
- 브라우저에서 직접 Supabase Realtime 구독 가능
- 연결 해제(`unsubscribe`) 처리

프로젝트 적용 포인트:
- 위치 데이터 INSERT 시 가족 화면에 실시간 갱신 트리거 가능
- SSE 대신 Supabase Realtime으로 위치 구독 대안 검토
- RLS 설정으로 가족 그룹 내 구성원만 위치 데이터 수신
