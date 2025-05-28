[Team8 Weather 프로젝트 - 즐겨찾기 기능 통합 안내]

📁 이 폴더에는 '날씨 검색 + 즐겨찾기 그룹 기능'이 통합된 Flask 코드가 포함되어 있습니다.

1. 주요 기능
- 기본 검색 (도시명 입력 시 현재 날씨 제공)
- 즐겨찾기 그룹 기능
   - 요일+시간+지역 조합을 그룹으로 저장
   - 그룹 이름 설정 가능
   - 그룹별 여러 요일/시간/지역 조합 저장 가능
   - 조회 시 요일/시간대별 날씨 정보 출력
   - 그룹 삭제 기능

2. 파일 구성
- app.py            : Flask 서버 전체 로직
- templates/index.html : 화면 UI 및 JavaScript 포함
- requirements.txt  : 필요한 패키지 목록
- favorites.json    : (처음엔 없어도 됨, 서버 실행 중 자동 생성됨)

3. 반영 방법
- 기존 프로젝트(app.py, index.html)를 교체
   - 기존 기능 유지됨 (기본 검색 기능 포함)
- 기존 기능만 쓰고 싶을 경우, 즐겨찾기 관련 라우터(`/groups`, `/add-group` 등)는 생략 가능
- 서버 실행 : python app.py

4. API 키
- 현재 내장된 키는 OpenWeather 무료 키로, 분당 요청 제한 있음.
- 고속 API 키로 변경 시, app.py 상단의 API_KEY 값만 바꿔주면 됨.

