# NLM-06: 모바일 웹에서 현재위치 정확도 높이는 법 - 카카오맵 API (지도/로컬)

> 원본 URL: https://devtalk.kakao.com/
> 출처: 카카오 데브톡 포럼
> 수집일: 2026-05-23
> NotebookLM 소스 유형: web_page

---

모바일 웹 환경에서 Geolocation API의 위치 정확도를 높이는 방법에 대한 카카오 개발자 포럼 Q&A.

주요 내용:
- `enableHighAccuracy: true` 옵션으로 GPS 우선 사용
- Wi-Fi/기지국 기반 위치 vs GPS 정확도 차이
- 실내에서 GPS 정확도 저하 문제 및 대응
- `accuracy` 값(미터 단위)으로 정확도 확인 방법
- 모바일 브라우저별 Geolocation 동작 차이

프로젝트 적용 포인트:
- `enableHighAccuracy: true` + `timeout: 10000` 설정 권장
- 정확도 50m 이내 비기능 요구사항 달성을 위한 설정값
- 실외(야외) 환경에서 주로 사용하는 부모님 대상 — GPS 충분히 정확
