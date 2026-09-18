# Learn CSS

CSS 기초부터 레이아웃, 애니메이션, 스타일 도구까지 단계별로 학습한 실습 저장소입니다. HTML과 CSS로 자기소개 페이지, 프로필 카드, 강의 목록, 대시보드 등을 만들고, Sass·Bootstrap·Tailwind CSS를 활용한 스타일링을 연습합니다.

## 사용 기술

- **HTML / CSS**: 선택자, 박스 모델, Position, Flexbox, Grid, 반응형 레이아웃, 애니메이션
- **Sass (SCSS)**: 변수, 믹스인, 모듈을 활용한 스타일 관리
- **Bootstrap 5.3.8 / Bootstrap Icons**: CDN 기반 컴포넌트 실습
- **Tailwind CSS 4**: 유틸리티 클래스와 사용자 정의 테마 실습
- **Node.js / npm**: Sass 및 Tailwind CSS 빌드 도구 실행

## 날짜별 학습 내용

| 폴더 | 주요 학습 내용 | 실습 파일 |
| --- | --- | --- |
| `dav01` | CSS 적용 방법, 기본·속성 선택자, 가상 클래스와 가상 요소 | [CSS 기초](dav01/index.html), [선택자](dav01/selector1.html), [자기소개](dav01/profile/index.html) |
| `day02` | 선택자, 상속, 배경과 그라디언트, 웹 폰트, 텍스트 스타일 | [CSS 속성](day02/index.html), [선택자 실습](day02/selector3.html) |
| `day03` | 박스 모델, Position, 카드와 자기소개 페이지 구성 | [박스 모델](day03/index.html), [프로필 카드](day03/card.html), [자기소개](day03/practice.html) |
| `day04` | Position, 겹침 순서, 모달 배치, Flexbox | [요소 겹치기](day04/index.html), [Position](day04/position1.html), [Flexbox](day04/flex1.html) |
| `day05` | Flexbox·Grid 레이아웃, 반응형 대시보드, 전환과 변형 효과 | [Grid](day05/grid.html), [대시보드](day05/dashboars.html), [강의 목록](day05/practice2.html) |
| `day06` | 키프레임 애니메이션, CSS 변수, 캐스케이드 레이어, 컨테이너 쿼리, 스크롤 효과 | [애니메이션](day06/index.html), [CSS 기능 실습](day06/index2.html), [강의 카드](day06/practice2.html) |
| `day07` | Sass 변수·믹스인·모듈, 컴포넌트별 스타일 분리 | [SCSS 강의 카드](day07/index.html) |
| `day08` | Bootstrap 기본 스타일, 컴포넌트, 아이콘, 페이지 구성 | [기본 실습](day08/basic.html), [컴포넌트](day08/index.html), [스터디 페이지](day08/prectice2.html) |
| `day09` | Tailwind CSS 기본 문법, 테마 설정, 카드 UI | [기본 실습](day09/index.html), [프로필 카드](day09/profileCard.html), [영화 카드](day09/profileCard%20copy.html) |
| `day10` | Tailwind CSS를 활용한 인기 콘텐츠 목록 UI | [Trending Now](day10/index.html), [다른 버전](day10/index%20copy.html) |

> 첫날 폴더 이름은 실제 저장된 이름인 `dav01`을 사용합니다. 실습 링크도 현재 파일명을 기준으로 작성했습니다.

## 폴더 구조

```text
learn-css/
├── dav01/             # CSS 입문 및 선택자 실습
├── day02/             # CSS 속성, 폰트, 배경
├── day03/             # 박스 모델 및 프로필 카드
├── day04/             # Position 및 Flexbox
├── day05/             # Grid 및 레이아웃 실습
├── day06/             # 애니메이션 및 CSS 기능 실습
├── day07/
│   ├── scss/          # 원본 SCSS: abstracts, components
│   ├── css/           # 컴파일된 CSS
│   └── index.html
├── day08/             # Bootstrap 실습
├── day09/
│   ├── src/input.css  # Tailwind 입력 CSS
│   └── index.html
├── day10/
│   ├── src/input.css  # Tailwind 입력 CSS
│   └── index.html
├── reset.css          # 공통 기본 스타일 초기화
├── package.json       # 의존성 및 실행 스크립트
└── package-lock.json  # 의존성 버전 잠금
```

이미지, 폰트, 개별 스타일 파일은 각 실습 폴더의 `assets`, `style` 등에 보관합니다.

## 실행 방법

### HTML 예제 열기

저장소를 내려받은 뒤 원하는 날짜의 HTML 파일을 브라우저로 열거나, VS Code의 Live Server로 실행합니다. 루트에 공통 시작 페이지는 없으므로 위 표에서 실습 파일을 선택하세요.

Bootstrap CDN, Google Fonts, 외부 이미지를 사용하는 예제는 인터넷 연결이 필요합니다.

### 빌드 도구 설치

Sass를 수정하거나 Tailwind 예제를 실행하려면 Node.js와 npm이 설치된 환경에서 프로젝트 루트에 다음 명령을 실행합니다.

```bash
npm install
```

### Sass 실습 — day07

```bash
npm run sass
```

`day07/scss`의 변경 사항을 감시하고 `day07/css`에 CSS를 생성합니다. 실행한 상태에서 SCSS를 수정하고 `day07/index.html`에서 확인합니다.

### Tailwind CSS 실습 — day09

```bash
npm run tw
```

`day09/src/input.css`를 입력으로 사용해 `day09/dist/output.css`를 생성합니다. 빌드 후 `day09/index.html` 또는 같은 폴더의 카드 예제를 엽니다.

### Tailwind CSS 실습 — day10

현재 `npm run tw`는 `day09`만 빌드하므로, `day10`은 별도로 실행합니다.

```bash
npx @tailwindcss/cli -i ./day10/src/input.css -o ./day10/dist/output.css --watch
```

빌드 후 `day10/index.html`을 엽니다. 두 날짜의 Tailwind 예제는 각 폴더의 `dist/output.css`를 참조하므로, 해당 CSS를 먼저 생성해야 스타일이 적용됩니다.

감시 모드로 실행한 명령은 터미널에서 `Ctrl+C`로 종료합니다.

## 학습 방법

1. 날짜별 HTML 파일과 연결된 CSS 또는 SCSS를 함께 확인합니다.
2. 속성값과 클래스를 수정하며 화면 변화를 비교합니다.
3. 카드, 강의 목록, 대시보드 예제를 통해 배운 속성을 조합해 봅니다.
4. 브라우저 너비를 바꾸며 반응형 레이아웃을 확인합니다.

학습 과정의 코드와 주석을 포함한 저장소입니다. `day06`에는 컨테이너 쿼리, 스크롤 기반 애니메이션, 앵커 위치 지정 등의 실습이 포함되어 있어 브라우저의 기능 지원에 따라 표현이 달라질 수 있습니다.
