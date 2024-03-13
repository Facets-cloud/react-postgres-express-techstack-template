<h1 align="center">
  React, Postgres and Express techstack template
  <br>
  <a href="http://www.typescriptlang.org/"><img src="https://img.shields.io/badge/%3C%2F%3E-TypeScript-%230074c1.svg?style=flat-square" height="20"></a>
  <a href="https://github.com/kriasoft/react-postgres-express-techstack-template/stargazers"><img src="https://img.shields.io/github/stars/kriasoft/react-postgres-express-techstack-template.svg?style=social&label=Star&maxAge=3600" height="20"></a>
</h1>

High-performance GraphQL API server, database dev tools, and React front-end.

## Features

- [Monorepo](https://yarnpkg.com/features/workspaces) project structure powered by [Npm](https://yarnpkg.com/).
- [GraphQL API](https://graphql.org/) powered by [GraphQL Yoga](https://the-guild.dev/graphql/yoga-server), [Pothos GraphQL](https://pothos-graphql.dev/), and [μWebSockets](https://github.com/uNetworking/uWebSockets.js).
- Authentication and authorization powered by [Google Identity Platform](https://cloud.google.com/identity-platform).
- Database tooling — seed files, migrations, [Knex.js](https://knexjs.org/) REPL shell, etc.
- Front-end boilerplate pre-configured with [TypeScript](https://www.typescriptlang.org/), [Vite](https://vitejs.dev/), [React](https://beta.reactjs.org/).
- The ongoing design and development is supported by these wonderful companies:

<a href="https://reactstarter.com/s/1"><img src="https://reactstarter.com/s/1.png" height="60" /></a>&nbsp;&nbsp;<a href="https://reactstarter.com/s/2"><img src="https://reactstarter.com/s/2.png" height="60" /></a>&nbsp;&nbsp;<a href="https://reactstarter.com/s/3"><img src="https://reactstarter.com/s/3.png" height="60" /></a>

---

This project was bootstrapped with [GraphQL Starter Kit](https://github.com/kriasoft/graphql-starter-kit).

## Directory Structure

`├──`[`.github`](.github) — GitHub configuration including CI/CD workflows.<br>
`├──`[`.vscode`](.vscode) — VSCode settings including code snippets, recommended extensions etc.<br>
`├──`[`code`](./code) — front-end application ([Vite](https://vitejs.dev/), [Vitest](https://vitest.dev/), [React](https://reactjs.org/)), Backend Application([PostgreSQL](https://www.postgresql.org/), [ExpressJs](https://expressjs.com/).<br>
`└── ...` — add more packages such as `worker`, `admin`, `mobile`, etc.

## Requirements

- [Node.js](https://nodejs.org/) v20 or newer with [Corepack](https://nodejs.org/api/corepack.html) enabled.
- Local or remote instance of [PostgreSQL](https://www.postgresql.org/).
- [VS Code](https://code.visualstudio.com/) editor with [recommended extensions](.vscode/extensions.json).

## Getting Started

Just [clone](https://github.com/Facets-cloud/graphql-starter-kit/generate) the repo
and, install project dependencies and bootstrap the PostgreSQL database:

```bash
$ git clone https://github.com/Facets-cloud/react-postgres-express-techstack-template

.git example
$ cd ./example                  # Change current directory to the newly created one
$ corepack enable               # Ensure npm is installed
$ npm install                  # Install project dependencies
$ npm db create                # Create a new database if doesn't exist
$ npm db migrate --seed        # Migrate and seed the database
```

From there on, you can launch the app by running:

```bash
$ npm workspace server start   # Or, `npm server:start`
$ npm workspace app start      # Or, `npm app:start`
```

The GraphQL API server should become available at [http://localhost:8080/](http://localhost:8080/).<br>
While the front-end server should be running at [http://localhost:5173/](http://localhost:5173/).

**IMPORTANT**: Tap `Shift`+`Cmd`+`P` in VSCode, run the **TypeScript: Select TypeScript Version** command and select the workspace version.

## How to Update

In the case when you kept the original GraphQL Starter Kit git history, you can
always pull and merge updates from the "seed" repository back into your
project by running:

```bash
$ git fetch seed                # Fetch GraphQL Starter Kit (seed) repository
$ git checkout main             # Switch to the main branch (or, master branch)
$ git merge seed/main           # Merge upstream/master into the local branch
```

In order to update Yarn and other dependencies to the latest versions, run:

```bash
$ npm set version latest       # Upgrade Yarn CLI to the latest version
$ npm upgrade-interactive      # Bump Node.js dependencies using an interactive mode
$ npm install                  # Install the updated Node.js dependencies
$ npm dlx @yarnpkg/sdks vscode # Update VSCode settings
```
