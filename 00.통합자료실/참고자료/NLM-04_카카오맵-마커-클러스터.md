# NLM-04: [React/Vite] 카카오맵 API 마커 표시, 클러스터 라이브러리 사용해보기

> 원본 URL: https://nninyeong.tistory.com/
> 출처: nninyeong.tistory.com
> 수집일: 2026-05-23
> NotebookLM 소스 유형: web_page

---

React + Vite 환경에서 카카오맵 API를 사용하여 마커를 표시하고 클러스터 라이브러리를 연동하는 방법.

주요 내용:
- `kakao.maps.Marker` 생성 및 지도에 표시
- 커스텀 마커 이미지(`MarkerImage`) 설정
- `MarkerClusterer`로 다수 마커 클러스터링
- React에서 카카오맵 SDK 스크립트 로드 방법 (`useEffect` + `script` 태그)
- 마커 클릭 이벤트 핸들링

프로젝트 적용 포인트:
- S-03 위치 지도 화면에서 부모님 위치 마커 표시
- 실시간 갱신 시 마커 위치 업데이트 (`setPosition`)
- 다중 부모님 계정(2차) 지원 시 클러스터링 활용 가능
