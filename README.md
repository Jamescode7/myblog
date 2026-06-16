# Seunghwa Dev Log

Hugo와 PaperMod로 구성한 개발자 기술 블로그입니다.

목표는 단순한 일기형 블로그가 아니라, 5년 뒤에도 검색 가능한 개발 문제 해결 데이터베이스를 만드는 것입니다.

## Stack

- GitHub Pages
- Hugo
- PaperMod
- GitHub Actions

## Local Development

```bash
hugo server -D
```

초안 글까지 확인하려면 `-D` 옵션을 사용합니다.

## New Post

```bash
hugo new content posts/my-post.md
hugo new content troubleshooting/my-issue.md
```

기본 글 구조는 다음 흐름을 따릅니다.

- 문제
- 환경
- 원인 분석
- 해결 방법
- 결과
- 배운 점

## Sections

- `content/posts`: Django, DevOps, SEO, API 등 일반 기술 글
- `content/troubleshooting`: 문제 해결 기록
- `content/project`: 프로젝트 구축과 설계 기록
- `content/notes`: 짧은 메모와 학습 기록

## Deployment

GitHub 저장소의 Settings > Pages에서 Source를 `GitHub Actions`로 설정합니다.

`main` 브랜치에 push하면 `.github/workflows/hugo.yaml` 워크플로가 Hugo 사이트를 빌드하고 GitHub Pages에 배포합니다.

## Before Publishing

1. `hugo.yaml`의 `baseURL`과 GitHub URL이 실제 저장소 주소와 일치하는지 확인합니다.
2. 초안 글의 `draft: true`를 `false`로 바꿉니다.
3. 글마다 `description`, `categories`, `tags`, `slug`를 검색 의도에 맞게 다듬습니다.
