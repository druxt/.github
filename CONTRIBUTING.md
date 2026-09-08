# Contributing

Contributions are welcome across every repository in the
[druxt](https://github.com/druxt) and
[druxt-contrib](https://github.com/druxt-contrib) organizations.

A repository with its own `CONTRIBUTING.md` overrides this page. Read that one
first; this is the default for repositories that have none.

## Before you start

- **Ask first if you are unsure.** The [Discord](https://discord.druxtjs.org) is
  the fastest way to find out whether something is a bug, a missing feature or a
  configuration problem.
- **Open an issue for anything non-trivial.** A short discussion before the code
  saves rework, particularly on the framework itself.
- **Check the docs.** [Contributing](https://druxtjs.org/how-to/contributing)
  covers the development environment for the main monorepo, which is where most
  framework changes belong.

## Which repository

| You want to change | Go to |
| ------------------ | ----- |
| A Nuxt module: routing, entities, menus, blocks, views, schema | [druxt/druxt.js](https://github.com/druxt/druxt.js) |
| Authentication | [druxt/druxt-auth](https://github.com/druxt/druxt-auth) |
| The Drupal module | [drupal.org/project/druxt](https://www.drupal.org/project/druxt), not the GitHub mirror |
| Another Drupal module Druxt depends on | That module's queue on drupal.org |
| A starter kit | The starter kit's own repository |
| The documentation | [druxt/druxt.js](https://github.com/druxt/druxt.js), under `docs/` |

Drupal-side work belongs on drupal.org. The GitHub copies of Drupal modules are
mirrors, and a pull request against a mirror cannot be merged into the project.

## Sending a change

- Branch from `develop` unless the repository says otherwise.
- Use [Conventional Commits](https://www.conventionalcommits.org) for commit
  messages and for the pull request title. These repositories squash on merge,
  so the title becomes the commit subject and a non-conventional one breaks the
  commit lint on the target branch.
- Add tests where the repository has them, and say why if you have not.
- Keep the change focused. An unrelated fix in the same pull request is harder
  to review and harder to revert.

## Reporting a bug

Open an issue on the repository the bug is in, and include the versions of
Druxt, Nuxt, Drupal and Node you are running, plus the steps to reproduce.

Security problems are the exception: do not open a public issue. Follow
[SECURITY.md](SECURITY.md).

## Code of conduct

Participation is covered by the [Code of Conduct](CODE_OF_CONDUCT.md).
