# 홈페이지 수정 안내

GitHub에서 아래 파일을 열고 연필 버튼으로 수정한 뒤 `Commit changes`로 저장하세요.
`main`에 저장하면 Actions의 **Build and deploy al-folio**가 자동 실행됩니다.
작업이 성공한 뒤 홈페이지를 새로고침하면 반영됩니다.

## 수정 위치

| 내용 | 파일 |
| --- | --- |
| 이름·사이트 소개 | `_config.yml`의 `first_name`, `last_name`, `description` |
| 첫 화면 소개·직함 | `_pages/about.md`의 본문과 `subtitle` |
| 프로필 사진 | `assets/img/`에 사진 업로드 후 about.md의 `image: false`를 `image: 파일명.jpg`로 변경 |
| GitHub·Scholar·ORCID 등 | `_data/socials.yml` |
| 논문 | `_bibliography/papers.bib` |
| 프로젝트 | `_projects/프로젝트이름.md` |
| 학력·경력·수상·기술 | `_data/cv.yml` |
| 메뉴 이름·순서 | `_pages/` 각 파일의 `title`, `nav_order` |
| CV 다운로드 | `assets/pdf/cv.pdf` 업로드 후 `_pages/cv.md`의 `cv_pdf: /assets/pdf/cv.pdf` 설정 |

## 소셜 링크

GitHub만 연결되어 있습니다. 나머지는 앞의 `#`를 지우고 본인 값을 입력하면 나타납니다.
Google Scholar는 주소의 `user=` 뒤 ID, ORCID는 본인의 ORCID 번호를 입력합니다.
이메일·소셜 계정·학력 등 제공되지 않은 정보는 비워 두었습니다.

## 논문 추가

`templates/paper.bib.example`을 참고해 실제 논문의 BibTeX를 `_bibliography/papers.bib`에 넣으세요.
Google Scholar 또는 출판사에서 BibTeX를 가져올 수 있습니다.
학술지 논문은 `@article`, 학회 논문은 `@inproceedings`를 사용하세요.
`selected = {true}`를 넣고 about.md의 `selected_papers: true`를 켜면 첫 화면에도 표시됩니다.
예시 파일은 홈페이지에 공개되지 않습니다.

## 프로젝트 추가

`templates/project.md.example`을 복사해 `_projects/프로젝트이름.md`로 만드세요.
제목·설명·본문을 채우면 Projects에 카드가 자동 생성됩니다.
`importance`가 작을수록 앞에 표시됩니다. 사진을 올린 뒤 `img` 줄의 주석을 해제할 수 있습니다.

## CV 작성

`_data/cv.yml`의 각 `[]`를 실제 항목 목록으로 바꾸세요.
형식은 `templates/cv-sections.yml.example`을 참고하세요. 들여쓰기는 공백으로 유지합니다.
Education, Experience, Publications, Projects, Awards, Skills, Interests를 준비했습니다.
CV와 Publications는 별도 자료이므로 CV에도 논문을 넣으려면 해당 항목을 작성하세요.
PDF는 실제 파일을 업로드한 뒤에만 링크를 켜세요.

## 배포 설정

Settings → Pages → Source는 **GitHub Actions**를 사용합니다.
`_config.yml`의 `url: https://dhseo0608.github.io`, `baseurl: ""`는 그대로 두세요.
별도의 `gh-pages` 브랜치는 필요하지 않습니다.
빌드가 실패하면 Actions에서 빨간 표시의 작업 로그를 확인하세요. 기존 성공 배포는 유지됩니다.

## 기존 테스트 페이지 보존

기존 HTML은 `backup/index-test.html`, 원래 README는 `backup/README-original.md`에 보존했습니다.
변경 전 Git 커밋은 `1984caa`입니다. 이 백업 폴더는 홈페이지 배포에서 제외됩니다.
첫 화면은 이제 `_pages/about.md`가 담당하므로 루트에 `index.html`을 다시 추가하지 마세요.
