# 배포 방법 (GitHub + Netlify)

## 폴더 구조
site/
├─ index.html
├─ detail.html
└─ assets/
   ├─ data/
   │  └─ tracks.js
   └─ thumbs/
      ├─ t001.png
      ├─ t002.png
      ├─ t003.png
      ├─ t004.png
      └─ t005.png

## 사용 방법
1) 위 폴더 전체를 VS Code에서 엽니다.
2) Netlify에 연결된 GitHub 저장소에 넣을 경우:
   - `index.html`와 `detail.html`를 루트에 그대로 둡니다.
   - `assets/` 폴더도 함께 업로드합니다.
   - 터미널에서:
     git add .
     git commit -m "가로형 포스터 그리드 + 3분할 상세 레이아웃 적용"
     git push
   - Netlify가 자동 배포합니다.

3) 썸네일/데이터 추가
   - 새로운 곡은 `assets/thumbs/`에 `t006.png` 형태로 넣고
   - `assets/data/tracks.js` 안의 `window.TRACKS` 배열에 항목을 추가하세요.
   - id는 고유해야 하며, `thumb` 경로는 `./assets/thumbs/아이디.png` 형식입니다.

4) 표시 형식
   - 첫 페이지 라벨은 '가수 — 제목' 형식으로 자동 표시합니다.
   - 상세 페이지는 PC(6:4 분할), 모바일(메뉴→유튜브→콘텐츠)로 자동 전환합니다.
