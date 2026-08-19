# 부자아저씨 가난한아빠 - 망포지구 대시보드 (Railway 배포)

기흥역세권과 동일한 방식(GitHub → Railway 자동 배포)으로 망포지구 매물현황 대시보드를 서빙합니다.

## 최초 설정 (한 번만)

1. **GitHub 새 리포지토리 생성**
   이름: `richfather-mangpo-dashboard`

2. **이 폴더(railway-static-mangpo) 전체를 리포지토리에 업로드**
   - `server.js`, `package.json`, `.gitignore`
   - `public/index.html` ← 오늘자(8/19) 망포지구 대시보드
   - `public/character.jpg` ← 캐릭터 이미지
   - **주의**: `public` 폴더 "안에" index.html과 character.jpg가 들어가야 합니다 (최상위 X)

3. **Railway에서 새 프로젝트 생성**
   - "New Project" → "Deploy from GitHub repo" → `richfather-mangpo-dashboard` 선택
   - 자동으로 `npm install` → `npm start` 실행됨
   - Settings → Networking → "Generate Domain" 눌러서 주소 생성

4. **도메인 확정되면 Claude에게 알려주기**
   → HTML 안의 og:url / og:image를 그 도메인으로 맞춰서 다시 드립니다 (카톡 미리보기용)

## 앞으로 매일 업데이트하는 방법

1. Claude에게 오늘자 망포지구 매물 데이터를 보내서 새 `index.html`을 받습니다 (파일명 이미 index.html로 드려요)
2. GitHub 리포지토리 → `public` 폴더 → `index.html` 옆 **"Add file" → "Upload files"**로 덮어쓰기
   (또는 index.html 열어서 연필 아이콘으로 내용 전체 교체)
3. **Commit changes**
4. Railway가 자동 감지해서 재배포 (몇십 초 소요)

## 참고
- `character.jpg`는 최초 1회만 올리면 됩니다 (이미지 자체가 안 바뀌는 한)
- 기흥역세권(`richfather-giheung-dashboard`)과는 **완전히 별개의 리포지토리 + Railway 프로젝트**입니다. 헷갈리지 않게 이름을 다르게 유지하세요.
