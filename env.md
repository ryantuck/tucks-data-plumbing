# Environment

## Per-project .env files with direnv and dotenv

`direnv` loads/unloads env vars based on `.envrc` file in working directory: https://direnv.net/

It can be used with `dotenv` which is a common tool that loads env vars from `.env` file: https://www.npmjs.com/package/dotenv

### Install

```
brew install direnv
npm install -g dotenv
```

### Setup

Define env vars in `.env`:

```
HELLO=world
```

Direnv config file `.envrc` just runs dotenv to load stuff:

```
dotenv
```

After creation/updates, you gotta allow it:

```
direnv allow
```
