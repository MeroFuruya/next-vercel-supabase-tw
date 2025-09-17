# Next.js + Vercel + Supabase + Tailwind CSS

|     | command                                                                                                                                                  | description                                                                                                                                                                                                                                                                                            |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1   |                                                                                                                                                          | Create and clone a GitHub repository                                                                                                                                                                                                                                                                   |
| 2   | `asdf set pnpm <pnpm-version>`                                                                                                                           | Set the pnpm version for the project                                                                                                                                                                                                                                                                   |
| 3   | `asdf set nodejs <nodejs-version>`                                                                                                                       | Set the Node.js version for the project                                                                                                                                                                                                                                                                |
| 4   | `npx create-next-app@latest . -e with-supabase --disable-git --ts --tailwind --use-pnpm --app --no-src-dir --eslint --no-turbopack --import-alias "@/*"` | Create a new Next.js project with TypeScript, Tailwind CSS, and pnpm                                                                                                                                                                                                                                   |
| 5   | `code .vscode/settings.json`                                                                                                                             | Create [VSCode settings](.vscode/settings.json)                                                                                                                                                                                                                                                        |
| 6   | `pnpm add -D prettier cspell eslint-config-prettier eslint-plugin-prettier @cspell/eslint-plugin`                                                        | Add Prettier and cspell to the project                                                                                                                                                                                                                                                                 |
| 7   | `code eslint.config.mjs`                                                                                                                                 | Add [Prettier](https://github.com/prettier/eslint-plugin-prettier?tab=readme-ov-file#configuration-new-eslintconfigjs) and [cspell](https://github.com/streetsidesoftware/cspell/tree/main/packages/cspell-eslint-plugin#configuration-new-eslintconfigjs) to [`eslint.config.mjs`](eslint.config.mjs) |
| 8   | `code .github/dependabot.yml`                                                                                                                            | Add [Dependabot configuration](.github/dependabot.yml)                                                                                                                                                                                                                                                 |
| 9   | `code .github/workflows/ci.yml`                                                                                                                          | Add [GitHub Actions CI workflow](.github/workflows/ci.yml)                                                                                                                                                                                                                                             |
| 10  | `code .prettierrc`                                                                                                                                       | Add [Prettier configuration](.prettierrc.json)                                                                                                                                                                                                                                                         |
| 11  | `code .env.example`                                                                                                                                      | Add [example environment variables](.env.example)                                                                                                                                                                                                                                                      |
| 12  | `echo '!.env.example' >> .gitignore`                                                                                                                     | And include `.env.example` in [.gitignore](.gitignore)                                                                                                                                                                                                                                                 |
| 12  | `code cspell.json`                                                                                                                                       | Add [cspell configuration](cspell.json). add extra languages if needed ([_documentation_](https://cspell.org/docs/dictionaries/))                                                                                                                                                                      |
| 13  |                                                                                                                                                          | Setup Github Repository rules (branch protection, required reviews, etc)                                                                                                                                                                                                                               |
| 14  |                                                                                                                                                          | Setup [Vercel project](https://vercel.com/new) and link the GitHub repository                                                                                                                                                                                                                          |
| 15  |                                                                                                                                                          | Setup [Supabase project](https://app.supabase.com/projects) and link the GitHub repository                                                                                                                                                                                                             |


## GitHub Rules
|                                           |                     |
| ----------------------------------------- | ------------------- |
| Name                                      | default             |
| enforcement status                        | active              |
| Bypass                                    | +Dependabot         |
| Target                                    | Default branch      |
| Restrict creations                        | `false`             |
| Restrict updates                          | `false`             |
| Restrict deletions                        | `true`              |
| Require linear history                    | `false`             |
| Require deployments to succeed            | `true`              |
| Require signed commits                    | `true`              |
| Require a pull request before merging     | `true`              |
| Require status checks to pass             | `true`              |
| Require status checks to pass - checks    | ci (GitHub Actions) |
| Block force pushes                        | `true`              |
| Automatically request Copilot code review | `true`              |


|                                           |              |
| ----------------------------------------- | ------------ |
| Name                                      | all          |
| enforcement status                        | active       |
| Bypass                                    |              |
| Target                                    | All branches |
| Restrict creations                        | `false`      |
| Restrict updates                          | `false`      |
| Restrict deletions                        | `false`      |
| Require linear history                    | `false`      |
| Require deployments to succeed            | `false`      |
| Require signed commits                    | `true`       |
| Require a pull request before merging     | `false`      |
| Require status checks to pass             | `false`      |
| Block force pushes                        | `true`       |
| Automatically request Copilot code review | `false`      |


