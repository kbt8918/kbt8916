# NLM-07: 백그라운드 위치 제한 | Android Developers

> 원본 URL: https://developer.android.com/
> 출처: developer.android.com (Android 공식 문서)
> 수집일: 2026-05-23
> NotebookLM 소스 유형: web_page

---

Android 8.0(API 26) 이상에서 앱이 백그라운드 상태일 때 위치 업데이트를 제한하는 정책 및 대응 방법.

주요 내용:
- Android 8.0(API 26)부터 백그라운드 앱의 위치 업데이트 수신 빈도 제한
- 백그라운드 상태: 시간당 몇 번만 위치 업데이트 수신 가능
- 포그라운드 상태: 이전 버전과 동일하게 위치 업데이트 수신
- 백그라운드에서 자주 위치 파악이 필요할 경우: 지오펜싱(Geofencing API) 또는 Fused Location Provider(FLP) 일괄 처리 권장
- 자주 업데이트 시: `startForegroundService()` 호출 후 포그라운드 서비스로 전환 필요 (사용자 권한 부여 필수)
- Wi-Fi Manager, Location Manager 백그라운드: 캐시된 결과 반환 또는 제한적 업데이트

프로젝트 적용 포인트:
- 부모님이 스마트폰 화면을 끄거나 브라우저가 백그라운드로 전환되면 30초 위치 갱신이 지연/차단될 위험
- 비기능 요구사항(위치 오차 50m 이내, 30초 갱신)은 화면 켜짐 상태(포그라운드) 전제로 설계
- 2차 출시: 안전구역 이탈 감지는 Geofencing API 활용 검토
