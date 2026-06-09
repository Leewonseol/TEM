# TheoEd Mission — Homepage

**TheoEd Mission (TEM)** 영문 홈페이지의 정적(static) 단일 페이지 빌드입니다.
별도의 빌드 도구 없이 그대로 GitHub Pages 등 어떤 정적 호스팅에도 올릴 수 있습니다.

## 구조

| 경로 | 설명 |
|---|---|
| `index.html` | 페이지 전체. 모든 CSS와 마크업이 인라인되어 있습니다. |
| `jpg/ATA_version.jpg` | 히어로 섹션에서 사용하는 메인 이미지. |
| `assets/fonts/` | 페이지에서 `@font-face`로 로드하는 woff2 폰트 파일들. |
| `assets/img/` | 네비게이션 엠블럼, 신념 섹션 마크, 후원 QR 등 인라인되지 않은 작은 이미지들. |
| `png/` | 디자인 시스템 엠블럼 원본(`emblem-gold.png`, `emblem-navy.png`)과 QR 원본. |

> 이전 빌드에 포함되어 있던 `homepage.css`, `colors_and_type.css`는 더 이상 필요하지 않아 제거되었습니다. (스타일은 모두 `index.html`에 인라인) 또한 이전 “standalone” 번들러 래퍼(런타임에 base64 자산을 blob URL로 풀던 자바스크립트)도 제거하고 일반 HTML로 변환했습니다.

## 섹션 구성

Hero (창세기 49:22) · Mission (Source / Growth / Impact) · Why TEM ·
Four Orientations · Belief quote · Core Strategy (Teaching Pool, Partnership,
Contextualized Curriculum, Excellence Standard) · Get Involved (Pray / Give / Serve) ·
Faculty Learning Community · Contact footer.

## 로컬에서 미리보기

```bash
python3 -m http.server 8000
# 그리고 브라우저에서 http://localhost:8000/ 열기
```

`file://`로 직접 열어도 동작하지만 폰트가 CORS로 막힐 수 있으므로 위 방법을 권장합니다.

## GitHub Pages 배포

1. **Settings → Pages → Build and deployment**
   - Source: `Deploy from a branch`
   - Branch: `main` (또는 배포하려는 브랜치) / `(root)` → **Save**
2. 기본 URL: `https://<github-username>.github.io/TEM/`

### 커스텀 도메인

도메인 등록업체에서 먼저 DNS를 설정한 뒤에 GitHub의 “Custom domain → Save”가 통과됩니다.

| 케이스 | 레코드 | 값 |
|---|---|---|
| 루트 도메인 (`example.com`) | `A` × 4 | `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` |
| 서브도메인 (`www.example.com`) | `CNAME` | `<github-username>.github.io` |

웹 UI에서 Save가 계속 실패할 경우, 저장소 루트에 도메인 한 줄만 적힌 `CNAME` 파일을 직접 커밋하면 GitHub이 자동으로 Pages 설정에 반영합니다.

## 변경 / 출시 전 확인

- 히어로 이미지(`jpg/ATA_version.jpg`) 교체 시 동일 경로로 덮어쓰면 됩니다.
- `assets/img/` 안의 후원 QR(가장 큰 PNG)을 실제 QR로 교체하세요.
- 영문 카피, 특히 성경 인용 구절을 검토하세요 (원본 한국어 자료에서 번역됨).
