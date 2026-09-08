# Security Policy

This policy covers every repository in the [druxt](https://github.com/druxt) and
[druxt-contrib](https://github.com/druxt-contrib) organizations. A repository
with its own `SECURITY.md` overrides this one.

## Reporting a vulnerability

Please **do not** open a public issue for a security vulnerability, in any
repository.

Report it through GitHub's private vulnerability reporting on the main
repository, whichever project the problem is in:

**[github.com/druxt/druxt.js/security/advisories/new](https://github.com/druxt/druxt.js/security/advisories/new)**

That form is private. It is the right place even when the affected code lives in
a starter kit, a contrib module or the Drupal module, because it is the channel
the maintainers watch.

If GitHub Security Advisories are unavailable to you, find a maintainer through
the community [Discord](https://discord.druxtjs.org) and continue in a direct
message. Do not post vulnerability details in a public channel.

Include if you can:

- What the issue is and what an attacker could do with it
- Steps to reproduce, or a proof of concept
- Which versions are affected
- Any mitigation you have found

You should get a first response within 72 hours. Coordinated disclosure is
appreciated: please give the maintainers time to assess and patch before public
discussion.

## What counts

The Drupal side of Druxt sits behind Drupal's own permission system, and the
Nuxt side talks to it over JSON:API. Reports that interest us most:

- A way to read or write data that Drupal's permissions should have refused
- Anything that leaks a token, a key or a consumer secret, including through a
  build artifact or a generated static site
- A CORS, proxy or authentication configuration that a starter kit ships
  insecurely by default

Drupal core issues belong on [drupal.org's security
team](https://www.drupal.org/drupal-security-team), not here.

## Versions

Druxt's npm packages are 0.x and only the current release line receives fixes.
[Support and versioning](https://druxtjs.org/explanation/support-and-versioning)
sets out what that means in practice.
