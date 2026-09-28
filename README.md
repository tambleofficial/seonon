# 선온 브로우 에디터 로그 — 블로그형 눈썹 디자인 기록

## GitHub → Cloudflare Pages 배포

이 ZIP의 **내용물 전체**를 해당 사이트만을 위한 GitHub 저장소의 최상위에 올립니다. Cloudflare Pages에서 **Workers & Pages → Pages → Connect to Git**로 저장소를 연결하세요. Framework preset `None`, Build command **비움**, Build output directory `.`, Production branch `main`입니다. 첫 화면은 완성된 포스팅이며 글은 `/blog/글주소/`에 저장됩니다. 각 ZIP은 독립적으로 배포할 수 있습니다.

## 다음 글 쓰기

`content/example-post.json`을 복사해 `content/posts/new-post.json`을 만들고 파일명과 `slug`를 모두 `new-post`로 맞춥니다. `title`, `summary`, `category`, `date`(YYYY-MM-DD), `body`(문단 배열), `image`, `image2`를 수정합니다. 사진은 `assets/images/`의 WebP 파일명에서 확장자를 뺀 값으로 지정합니다. `comments`에는 편집자가 미리 작성한 댓글만 넣을 수 있습니다. 방문자의 댓글 작성 기능은 없습니다.

`main`에 push하면 GitHub Actions가 `index.html`과 `/blog/new-post/index.html`을 재생성해 커밋합니다. 저장소에서 Actions의 쓰기 권한이 비활성화됐다면 `python3 scripts/build.py`를 실행해 생성된 파일을 직접 커밋하세요. Cloudflare Pages는 저장소의 변경사항을 배포합니다.

사이트 이름과 컬러는 `site.json`, 레이아웃은 `assets/style.css`, 원고는 `content/posts/*.json`에서 바꿀 수 있습니다. 공감은 방문자 브라우저에만 보관됩니다. 검색과 카테고리 목록은 현재 글 안에서 동작합니다.

사진과 프로필은 제작한 연출 이미지이며 상호, 인물, 상담 장면과 평가는 창작된 콘텐츠입니다. 실제 방문이나 시술 결과로 소개하지 마세요. 실제 업체에 관한 글을 게시할 경우 사실 관계와 사진 사용 권한을 확인하세요.
