# gridnine.github.io

정적 HTML로 만든 GitHub Pages 사이트입니다. 빌드 과정은 없고, `main` 브랜치 루트의 파일이 그대로 배포됩니다.

## 파일 구성

| 파일 | 역할 |
| --- | --- |
| `index.html` | 메인 페이지 |
| `404.html` | 없는 주소로 들어왔을 때 보여줄 페이지 |
| `.nojekyll` | Jekyll 처리를 끄고 파일을 그대로 배포 |

## `gridnine.github.io` 주소로 열기

GitHub Pages의 `<이름>.github.io` 주소는 **저장소를 가진 계정/조직 이름**으로 정해집니다.
지금 저장소는 `seongsik` 계정 소유라서, 그대로 두면 주소가
`https://seongsik.github.io/gridnine.github.io/` 가 됩니다.

`https://gridnine.github.io` 로 열려면:

1. **`gridnine` 조직 만들기** — GitHub 우측 상단 `+` → *New organization* → Free 플랜 → 이름에 `gridnine` 입력
   (이미 다른 사람이 쓰고 있는 이름이면 불가능합니다.)
2. **저장소 옮기기** — 이 저장소의 *Settings → General → Danger Zone → Transfer ownership* → 새 소유자 `gridnine`
   (저장소 이름은 `gridnine.github.io` 그대로 둡니다.)
3. **Pages 켜기** — 옮긴 저장소의 *Settings → Pages*
   - Source: **Deploy from a branch**
   - Branch: **main** / **(root)** → Save
4. 1~2분 뒤 `https://gridnine.github.io` 접속 확인. *Enforce HTTPS* 도 켜 둡니다.

> 조직 대신 `gridnine` 이라는 개인 계정을 새로 만들어도 되지만, 조직으로 만들면 지금 계정(`seongsik`)으로 그대로 관리할 수 있어 더 편합니다.

## 나중에 직접 산 도메인 연결하기 (선택)

1. 저장소 루트에 `CNAME` 파일을 만들고 도메인 한 줄 입력 (예: `www.example.com`)
2. 도메인 업체 DNS 설정
   - `www` 서브도메인: `CNAME` 레코드 → `gridnine.github.io`
   - 루트 도메인(`example.com`): `A` 레코드 4개 → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
3. *Settings → Pages → Custom domain* 에 같은 도메인 입력 후 *Enforce HTTPS* 체크
