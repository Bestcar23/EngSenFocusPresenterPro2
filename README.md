# EngFocusPresenter - Vercel Static Deploy

이 폴더는 **빌드가 전혀 필요 없는 Vercel 정적 배포용 프로젝트**입니다.

## 포함 파일
- `index.html`
- `assets/` : 이미 빌드된 JS/CSS 파일
- `vercel.json` : 설치/빌드 없이 루트 파일을 바로 서빙하도록 설정
- `README.md`
- `.gitignore`

## 이번 반영 사항
1. 지문 번호 버튼에서 `3-10`, `3-12`처럼 길이가 긴 항목도 **줄바꿈 없이 내용 길이에 맞게 폭이 자동 조정**되도록 수정
2. 같은 그룹(예: `3-*`, `4-*`)은 같은 색을 쓰고, 그룹 간 차이가 더 잘 보이도록 **색상 대비를 강화**
3. 글자 크기 조절 버튼 표시를 `-0.4`, `-0.2`, `+0.2`, `+0.4` 대신 **`-`, `기본`, `+` 형태**로 단순화

## GitHub 업로드 방법
1. 이 ZIP 파일을 압축 해제합니다.
2. 압축 해제 후 보이는 파일들을 GitHub 저장소 **루트**에 업로드합니다.
3. 저장소 최상위에 아래 항목이 바로 보여야 합니다.
   - `index.html`
   - `assets/`
   - `vercel.json`
   - `README.md`

## Vercel 연동 방법
1. Vercel에서 **Add New → Project**를 선택합니다.
2. GitHub 저장소를 Import 합니다.
3. Framework Preset은 **Other**로 두거나, `vercel.json` 설정을 그대로 사용합니다.
4. Build Command / Install Command / Output Directory는 별도 입력하지 않아도 됩니다.
5. Deploy를 누르면 됩니다.

## 핵심
- 이 프로젝트는 **정적 파일만** 포함합니다.
- `package.json`이 없으므로 npm 설치가 일어나지 않습니다.
- `vercel.json`에서 `framework: null`, `installCommand: ""`, `buildCommand: ""`, `outputDirectory: "."`로 설정되어 있어 빌드 오류 가능성을 크게 줄입니다.
