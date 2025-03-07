<p align="center">
  <br />
  <a href="https://nodejs.org">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="./public/static/images/logos/nodejs-new-pantone-white.svg">
      <img src="./public/static/images/logos/nodejs-new-pantone-black.svg" width="200px">
    </picture>
  </a>
</p>

<p align="center">
  <a href="https://nodejs.org">Node.js</a> Website built using Next.js with TypeScript, SCSS and MDXv2
</p>

<p align="center">
  <a title="MIT License" href="LICENSE">
    <img src="https://img.shields.io/badge/license-MIT-blue" alt="MIT License" />
  </a>
  <a title="Localised" href="https://crowdin.com/project/nodejs-website">
    <img src="https://badges.crowdin.net/nodejs-website/localized.svg" alt="Crowdin Badge" />
  </a>
  <a title="Vercel" href="https://vercel.com">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/powered%20by-Vercel%20%E2%96%B2-white">
      <img src="https://img.shields.io/badge/powered%20by-Vercel%20%E2%96%B2-black" alt="Powered by Vercel">
    </picture>
  </a>

  <br />

  <img src="https://github.com/nodejs/nodejs.org/actions/workflows/build.yml/badge.svg" alt="Build and Analysis Checks" />

  <br />
  <br />
</p>

## What is this repo?

[Nodejs.org](https://nodejs.org/) by the [OpenJS Foundation](https://openjsf.org/) is the official website for the Node.js® JavaScript runtime. This repo is the source code for the website. It is built using [Next.js](https://nextjs.org), a React Framework.

### Quick-Start Locally

```bash
npm ci
npx turbo serve

# listening at localhost:3000
```

### Structure of this Repository

- Page templates are in `/layouts`
- Global styles are in `/styles`
- Public files are in `/public`
- i18n configuration is on `i18n/config.json`
- Global static files are in `/public/static`
  - Legacy static files are in `/public/static/legacy`
- All content is in `/pages`
  - Initial development usually happens in English: `/pages/en`
  - `/i18n/locales/{{locale}}.json` is where global localization information lives.
  - All content is in Markdown and is per locale.
  - The top of each Markdown file is a block of YAML (Frontmatter) for page-specific localization information passed to various templates.
  - The bulk of the Markdown content for each page is referenced as `{children}` on their respective JSX Layout (`layouts/`)

## Contributing

This project adopts the Node.js [Code of Conduct][].

Any person who wants to contribute to the Website is welcome! Please read [Contribution Guidelines][] and see the [Figma Design][] to understand better the structure of this repository.

### To translate content into other languages

If you want to help translate to other languages or improve existing translations, it is optional to work from GitHub. You can and should do it through Crowdin; this is the correct workflow.

Crowdin is an online tool that facilitates the user experience for the translator; here is more information:

Website translations are handled via [Crowdin](https://crowdin.com/project/nodejs-website).

To help with localization, please read the [Translation](TRANSLATION.md) guide.

### Deployment

Full setup is in <https://github.com/nodejs/build/tree/master/ansible/www-standalone> minus secrets and certificates. The webhook is set up on GitHub for this project and talks to a small Node server on the host, which does the work. See the [github-webhook](https://github.com/rvagg/github-webhook) package for this.

## Relevant Links

[Code of Conduct][]

[Contribution Guidelines][]

[Collaborator Guide][]

[Figma Design][]

[Content vs Code][]

[Dependency Pinning][]

[code of conduct]: https://github.com/nodejs/admin/blob/main/CODE_OF_CONDUCT.md
[contribution guidelines]: ./CONTRIBUTING.md
[content vs code]: ./CONTENT_VS_CODE.md
[dependency pinning]: ./DEPENDENCY_PINNING.md
[collaborator guide]: ./COLLABORATOR_GUIDE.md
[figma design]: https://www.figma.com/file/lOxAGGg5KXb6nwie7zXkz6/NJ---Design-System?node-id=22%3A6086
