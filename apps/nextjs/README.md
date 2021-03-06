# Prisma + tRPC

Try in CodeSandbox: [https://githubbox.com/trpc/trpc/tree/main/examples/next-prisma-starter](https://codesandbox.io/s/github/trpc/trpc/tree/main/examples/next-prisma-starter?file=/src/pages/index.tsx)


## Features

- đ§ââī¸ E2E typesafety with [tRPC](https://trpc.io)
- âĄ Full-stack React with Next.js
- âĄ Database with Prisma
- âī¸ VSCode extensions
- đ¨ ESLint + Prettier
- đ CI setup using GitHub Actions:
  - â E2E testing with [Playwright](https://playwright.dev/)
  - â Linting


## Setup

```bash
npx create-next-app --example https://github.com/trpc/trpc --example-path examples/next-prisma-starter trpc-prisma-starter
cd trpc-prisma-starter
yarn
yarn dev
```

## Files of note

<table>
  <thead>
    <tr>
      <th>Path</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="./prisma/schema.prisma"><code>./prisma/schema.prisma</code></a></td>
      <td>Prisma schema</td>
    </tr>
    <tr>
      <td><a href="./src/api/trpc/[trpc].tsx"><code>./src/api/trpc/[trpc].tsx</code></a></td>
      <td>tRPC response handler</td>
    </tr>
    <tr>
      <td><a href="./src/routers"><code>./src/routers</code></a></td>
      <td>Your app's different tRPC-routers</td>
    </tr>
  </tbody>
</table>

## Commands

```bash
yarn dx # runs prisma studio + next
yarn build # runs `prisma generate` + `prisma migrate` + `next build`
yarn test-dev # runs e2e tests on dev
yarn test-start # runs e2e tests on `next start` - build required before
yarn dev-nuke # resets local db
```

## âšī¸ How to switch from SQLite to Postgres

How to switch to postgres

- Remove migrations: `rm -rf ./prisma/migrations`
- Update: `./prisma/schema.prisma` (see commented code)

---

Created by [@alexdotjs](https://twitter.com/alexdotjs).
