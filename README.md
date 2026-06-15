# 토닥 · TODAK — 랜딩 페이지

임신부터 육아까지, 우리 아이의 모든 순간을 차분하게 기록하는 육아 다이어리 **토닥(TODAK)**의 소개/사전등록 랜딩 페이지입니다. 정적 사이트(HTML + Tailwind CDN)로 별도 빌드 없이 동작합니다.

## 구성
```
todak/
├─ index.html        # 전체 페이지 (단일 파일)
├─ assets/           # 사진 (Unsplash, 자유 이용)
│  ├─ hero-home.jpg  # 히어로 배경 (따뜻한 거실)
│  ├─ mom.jpg        # 소개 — 아기를 안은 엄마
│  ├─ baby.jpg       # 소개 — 신생아의 손
│  ├─ preg.jpg       # 기능 — 임신 다이어리
│  ├─ voice.jpg      # 기능 — 스마트 음성 기록
│  ├─ memory.jpg     # 기능 — AI 추억 카드
│  └─ couple.jpg     # 기능 — 공동 육아
├─ robots.txt
├─ .nojekyll         # GitHub Pages가 파일을 그대로 서빙하도록
└─ README.md
```

## 로컬에서 보기
```bash
# 방법 1) 파일 더블클릭 — index.html 열기
# 방법 2) 로컬 서버 (권장)
python -m http.server 8000
# → 브라우저에서 http://localhost:8000
```

## 내용 수정
- 텍스트/레이아웃: `index.html`
- 사진 교체: `assets/` 안의 같은 파일명으로 덮어쓰기 (자동 반영)
- 기능 탭 이미지/문구: `index.html` 하단 `<script>`의 `OFFERS` 배열

## 배포 (GitHub Pages)
1. GitHub 저장소에 푸시
2. 저장소 **Settings → Pages → Source: `main` 브랜치 `/ (root)`** 선택
3. 잠시 후 `https://<사용자명>.github.io/<저장소명>/` 에 게시

## 사전등록 폼 연동 (선택)
현재 사전등록 폼은 데모(클라이언트 검증만)입니다. 실제 이메일 수집을 하려면
Formspree / Google Forms / Tally 등으로 `index.html`의 `<form id="registerForm">`
action을 연결하세요.

## 출처
- 사진: [Unsplash](https://unsplash.com) (Unsplash License, 자유 이용)
- 폰트: Lora · Nanum Myeongjo · Raleway · Noto Sans KR (Google Fonts)
