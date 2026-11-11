# Study Plan 앱 설정 (한 번만)

앱 주소: https://kyehyeonkim12-ops.github.io/PLANNER/

## 1. GitHub Pages 켜기
저장소 Settings → Pages → Source: "Deploy from a branch"
→ Branch: `ccr-c07c7f34-4kz9ps`, 폴더: `/docs` → Save.
1~2분 뒤 위 주소가 열려요.

## 2. 구글 클라우드에서 Client ID 만들기
1. https://console.cloud.google.com 에서 새 프로젝트 만들기 (이름 예: Study Plan)
2. "API 및 서비스 → 라이브러리"에서 **Google Drive API**, **Google Calendar API** 사용 설정
3. "OAuth 동의 화면": User Type **외부** → 앱 이름 Study Plan, 지원 이메일·개발자 이메일에 내 이메일
   → 범위는 건너뛰기 → **테스트 사용자**에 내 구글 이메일 추가
4. "사용자 인증 정보 → 사용자 인증 정보 만들기 → OAuth 클라이언트 ID"
   - 유형: **웹 애플리케이션**
   - 승인된 JavaScript 원본: `https://kyehyeonkim12-ops.github.io`
   - 승인된 리디렉션 URI: `https://kyehyeonkim12-ops.github.io/PLANNER/`
5. 만들어진 클라이언트 ID(…apps.googleusercontent.com)를 `docs/config.js`의 `clientId`에 넣기

## 3. 폰·패드에 설치
- 안드로이드(Chrome): 앱 주소 열기 → 메뉴 → "앱 설치" 또는 "홈 화면에 추가"
- 아이패드(Safari): 앱 주소 열기 → 공유 → "홈 화면에 추가"
- 앱을 열고 "구글 연결" → 같은 구글 계정으로 로그인
  ("Google에서 확인하지 않은 앱" 경고가 나오면: 고급 → Study Plan(으)로 이동)

## 4. 기존 데이터 옮기기
claude.ai 플래너 → 설정 → DATA → 내보내기 (자동 복사)
→ 앱 → 설정 → DATA에 붙여넣기 → 가져오기
