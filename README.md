# 3rdshot

Astro 정적 사이트 + `public/` HTML 페이지. Railway 배포용으로 설정되어 있습니다.

## 로컬 개발

```bash
npm install
npm run dev
```

## HTML 페이지 추가

`public/` 폴더에 HTML 파일을 넣으면 빌드 후 그대로 제공됩니다.

| 파일 | URL |
|------|-----|
| `public/about.html` | `/about.html` |
| `public/foo/bar.html` | `/foo/bar.html` |

CSS, JS, 이미지도 `public/` 아래에 두면 됩니다.

## 빌드 & 미리보기

```bash
npm run build
npm run preview
```

## Railway 배포

1. GitHub에 푸시하거나 Railway CLI로 배포합니다.

```bash
railway login
railway init
railway up
```

2. Railway는 `npm run build` 후 `npm run start`로 `dist/`를 서빙합니다.

### GitHub 연동 시

- Root Directory: 프로젝트 루트
- Build Command: `npm run build`
- Start Command: `npm run start`

Node.js 22 이상이 필요합니다 (`package.json`의 `engines` 참고).
