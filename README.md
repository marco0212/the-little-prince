<h1 align="center">
  Welcome to <a href="https://www.clap.company/">CLAP</a> 👋
</h1>

## Table of Contents

- [Requirements](#requirements)
- [Install](#install)
- [Run Apps](#run-apps)
- [Service URLs](#service-urls)

## Requirements

- [Node.js](https://nodejs.org/en/) The minimum Node.js version is `v18.17`.

아래 명령어를 통해 Node.js와 Node.js의 패키지 매니저인 Yarn을 설치합니다.

```bash
brew install node
npm install -g yarn
```

아래는 선택사항으로, Node.js의 버전을 관리해주는 `nvm` 패키지를 설치합니다. `nvm`은 version management 도구 입니다.

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.2/install.sh | bash
nvm install
```

## Install

```bash
yarn install
```

## Run Apps

```bash
yarn dev
```

### Set local env

로컬 환경에서 개발 편의성을 위해 로그인하지 않아도 요청 유저를 임의로 설정할 수 있도록 지원하고 있습니다.
이를 위해서 우선 `.env.local`를 생성합니다.

```
touch .env.local
```

생성된 `.env.local` 파일에 아래 내용을 추가하고 저장합니다.

```
NEXT_PUBLIC_DEV_USER_EMAIL="{로그인을 원하는 계정 이메일}”
NEXT_PUBLIC_ENABLE_MSW=true
```

## Service URLs

### `local`

| Name        | Port   | URL                   |
| ----------- | ------ | --------------------- |
| `web`       | `3000` | http://localhost:3000 |
| `storybook` | `6006` | http://localhost:6006 |

### `development`

| Name        | URL                                      |
| ----------- | ---------------------------------------- |
| `web`       | https://dev.clap.company                 |
| `server`    | https://dev.clap.company/api             |
| `storybook` | https://quirky-wilson-de436d.netlify.app |

### `production`

| Name     | URL                          |
| -------- | ---------------------------- |
| `web`    | https://www.clap.company     |
| `server` | https://www.clap.company/api |
