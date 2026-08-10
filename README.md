# Talk template

Personal starting point for slide decks, built on [reveal.js](https://revealjs.com).
This repo began as a plain snapshot of reveal.js `v6.0.1` (upstream commit
[`a3b94069`](https://github.com/hakimel/reveal.js/commit/a3b940695648aa1c5b0680bc9a5b905cf43020e5)),
with everything reveal.js needs to maintain itself as an OSS project (tests, examples,
React bindings, CI workflows, npm-publish tooling) stripped back out.

## Getting started

```
npm install
npm start
```

This starts a Vite dev server; edit `index.html` for slide content.

To produce a static `dist/` build (already checked in, but regenerate after
changing `js/`, `css/`, or `plugin/`):

```
npm run build
```

## Pulling in reveal.js updates

The original reveal.js repo is wired up as the `upstream` remote:

```
git remote -v
```

To bring in changes made upstream since this template was created:

```
git fetch upstream
git diff a3b940695648aa1c5b0680bc9a5b905cf43020e5 upstream/master -- js/ css/ plugin/
```

Review the diff and cherry-pick or manually apply whatever's relevant —
this repo's history is a single commit, so there's no shared ancestor to
merge/rebase against directly.

---

<div align="center">
  Built on reveal.js, MIT licensed | Copyright © 2011-2026 Hakim El Hattab, https://hakim.se
</div>
