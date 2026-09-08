<a href="https://druxtjs.org">
  <img src="banner.svg" alt="DruxtJS: The Fully Decoupled Drupal Framework">
</a>

# DruxtJS

[![npm](https://img.shields.io/npm/v/druxt?label=druxt&color=00a4d3)](https://www.npmjs.com/package/druxt)
[![License](https://img.shields.io/badge/license-MIT-blue)](https://github.com/druxt/druxt.js/blob/develop/LICENSE)
[![Discord](https://img.shields.io/badge/chat-Discord-5865F2?logo=discord&logoColor=white)](https://discord.druxtjs.org)

> Druxt = DRUpal + nUXT.

Druxt connects a [Drupal](https://www.drupal.org) backend to a
[Nuxt](https://v2.nuxt.com) frontend. Drupal stays the editorial system your
authors already know. Nuxt renders the site. Druxt does the work between them:
it reads Drupal's JSON:API and turns routes, content entities, menus, blocks
and views into Vue components you can theme.

You choose how much of it to use. `druxt-site` gives you a whole decoupled site
out of the box, driven by your Drupal display configuration. Or install single
modules and add decoupled routing, entity rendering or menus to a Nuxt project
you already have.

## Start here

```sh
npx giget@1 gh:druxt/quickstart#develop my-druxt-site
cd my-druxt-site
npm run setup
npm run dev
```

That gives you Drupal 11 and Nuxt 2 in one repository, already talking to each
other. `npm run setup` needs PHP 8.3 or newer and Composer on your `PATH`, and
stops with an error if either is missing. The backend runs on local PHP and
SQLite, so Docker is not required. The
[getting started tutorial](https://druxtjs.org/tutorials/getting-started) walks
the same steps and explains each one.

## Documentation

| Section | What you will find |
| ------- | ------------------ |
| [Tutorials](https://druxtjs.org/tutorials) | Learn by building: a first site, theming, a login flow, deployment, a custom module |
| [How-to guides](https://druxtjs.org/how-to) | Solve one problem: CORS, proxying, multilingual, Storybook, deployment, upgrades |
| [Explanation](https://druxtjs.org/explanation) | How it works: routing, schemas, component resolution, request topology |
| [Reference](https://druxtjs.org/api) | Generated API documentation for every module and component |

Coming from one side of the stack only? Start with
[Drupal for Nuxt developers](https://druxtjs.org/explanation/drupal-for-nuxt-developers)
or [Nuxt for Drupal developers](https://druxtjs.org/explanation/nuxt-for-drupal-developers).

## What is here

### The framework

| Repository | Role |
| ---------- | ---- |
| [druxt.js](https://github.com/druxt/druxt.js) | The monorepo. Nine Nuxt modules: [druxt](https://druxtjs.org/modules/druxt), [blocks](https://druxtjs.org/modules/blocks), [breadcrumb](https://druxtjs.org/modules/breadcrumb), [entity](https://druxtjs.org/modules/entity), [menu](https://druxtjs.org/modules/menu), [router](https://druxtjs.org/modules/router), [schema](https://druxtjs.org/modules/schema), [site](https://druxtjs.org/modules/site), [views](https://druxtjs.org/modules/views) |
| [druxt_drupal](https://github.com/druxt/druxt_drupal) | The Drupal module, mirrored from [drupal.org/project/druxt](https://www.drupal.org/project/druxt) |
| [druxt-auth](https://github.com/druxt/druxt-auth) | OAuth authentication, versioned separately from the monorepo |

### Starter kits

Every one is a GitHub template. Press "Use this template", or use the `giget`
command above.

| Template | Use it when |
| -------- | ----------- |
| [quickstart](https://github.com/druxt/quickstart) | You want the standard pairing: Drupal and Nuxt side by side |
| [quickstart-druxt-site-tome](https://github.com/druxt/quickstart-druxt-site-tome) | You want content in git and no database, via [Tome](https://www.drupal.org/project/tome) |
| [quickstart-druxt-serverless](https://github.com/druxt/quickstart-druxt-serverless) | You want a fully static build with no live Drupal in production |
| [module-template](https://github.com/druxt/module-template) | You are writing your own Druxt module |

### Demos

| Demo | What it shows |
| ---- | ------------- |
| [demo.druxtjs.org](https://demo.druxtjs.org) | The framework's own demo site |
| [umami.demo.druxtjs.org](https://umami.demo.druxtjs.org) | Drupal's Umami food magazine, rendered by Druxt, in English and Spanish |

## The Drupal side

Druxt is not a fork of anything. It builds on modules the Drupal community
already maintains, and contributes back to them.

| Module | Why Druxt needs it |
| ------ | ------------------ |
| [druxt](https://www.drupal.org/project/druxt) | Exposes the resources the frontend asks for, and the display configuration behind them |
| [decoupled_router](https://www.drupal.org/project/decoupled_router) | Translates a path into a route, which is what makes decoupled routing possible |
| [jsonapi_menu_items](https://www.drupal.org/project/jsonapi_menu_items) | Serves whole menu trees over JSON:API |
| [jsonapi_views](https://www.drupal.org/project/jsonapi_views) | Serves Views results over JSON:API |

[Simple OAuth](https://www.drupal.org/project/simple_oauth) pairs with
`druxt-auth` when you need authenticated users.

## Community modules

[github.com/druxt-contrib](https://github.com/druxt-contrib) holds integrations
that sit outside the core framework:
[Layout Builder](https://github.com/druxt-contrib/druxt-layout-builder),
[Layout Paragraphs](https://github.com/druxt-contrib/druxt-layout-paragraphs)
and [Config Pages](https://github.com/druxt-contrib/druxt-config-pages).

## Project status

The npm packages are 0.x and run on Vue 2.7 and Nuxt 2. That is deliberate
rather than neglected, and the plan is public:

- **1.0.0** is a stability release for the current stack. Bug fixes,
  documentation and examples. No new features.
- **2.0.0** is the rewrite: Nuxt 4, Vue 3, TypeScript, and the `@druxt`
  namespace.

[Support and versioning](https://druxtjs.org/explanation/support-and-versioning)
sets out what that means for a site you are building today.

## Getting help

- [Discord](https://discord.druxtjs.org) for questions and conversation
- [Issues](https://github.com/druxt/druxt.js/issues) for bugs and feature requests
- [Contributing guide](https://github.com/druxt/druxt.js/blob/develop/CONTRIBUTING.md)
  if you want to send a patch

## Maintainer

Druxt is built by [Stuart Clark](https://stuar.tc), a Drupal and JavaScript
engineer in Ballarat, Australia. He writes about decoupled Drupal at
[stuar.tc](https://stuar.tc) and is
[Deciphered](https://www.drupal.org/u/deciphered) on drupal.org.

MIT licensed.
