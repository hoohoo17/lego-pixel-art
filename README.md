# 레고 픽셀아트 변환기

이미지를 업로드하면 레고 브릭 픽셀아트로 변환해주는 웹 서비스.

## 기능
- 이미지 드래그&드롭 / 클릭 업로드
- 해상도 선택 (16×16 ~ 64×64)
- 밝기 / 채도 조절
- 소량 색상 자동 통합 (기준 개수 설정)
- 레고 픽셀아트 미리보기 (스터드 효과)
- 조립 설명서 (번호 표시)
- 구매 목록 자동 계산 (200 / 330 / 660 단위)
- PNG 다운로드

## 배포 방법

### GitHub Pages (무료, 권장)
```bash
# 1. GitHub 저장소 생성
git init
git add .
git commit -m "init"
git remote add origin https://github.com/<유저명>/<저장소명>.git
git push -u origin main

# 2. GitHub → Settings → Pages → Branch: main → Save
# 3. https://<유저명>.github.io/<저장소명> 접속
```

### Netlify (무료)
```
netlify.com → New site from Git → 저장소 선택 → Deploy
또는 폴더 자체를 netlify.com/drop 에 드래그
```

### Vercel (무료)
```bash
npm i -g vercel
vercel --prod
```

### 로컬 실행
```bash
# Python
python3 -m http.server 3000

# Node
npx serve .
```

## 파일 구조
```
lego-pixel-art/
└── index.html   ← 전체 앱 (단일 파일, 외부 의존성 없음)
```

## 팔레트 커스터마이징
`index.html` 상단의 `PALETTE` 객체 수정:
```js
const PALETTE = {
  '번호': {hex: '#색상코드', warm: true/false},
  ...
};
```
