# 기여 규칙

## 브랜치 이름
- `feature/기능`, `fix/버그`, `docs/문서`, `chore/설정` 중 하나로 시작한다
- main 에서 바로 commit 하지 않는다. 작업 전 `git switch main && git pull` 후 branch 를 만든다
- branch 는 반나절 안에 PR 로 합치고 지운다

## 커밋 머리말
- `feat:` 기능, `fix:` 버그, `docs:` 문서, `style:` 포맷, `refactor:` 구조 변경, `chore:` 설정
- 한 commit 에는 한 가지 변경만 담는다
- commit 전에 `git diff --staged` 로 메시지와 실제 변경이 맞는지 본다

## PR
- PR 을 열면 템플릿(무엇을 / 왜 / 확인한 것)이 자동으로 채워진다. 빈칸 없이 쓴다
- 관련 Issue 가 있으면 본문에 `Closes #번호` 를 적는다
- 리뷰 반영은 같은 branch 에 commit 을 더해 push 한다

## 리뷰 시간
- PR 이 올라오면 30분 안에 한 명이 확인한다
- 리뷰 한 번은 10분을 넘기지 않는다. 사소한 의견은 `nit:` 을 붙인다
- 리뷰어는 직접 실행해 보고 Approve 한다

## 비밀값 관리
- API 키 같은 값은 `.env` 에만 둔다. `.env` 는 `.gitignore` 에 있다
- 필요한 변수 이름은 `.env.example` 에 값 없이 적어 공유한다
- 실수로 올렸다면 커밋을 지우기보다 키부터 폐기하고 새로 발급한다