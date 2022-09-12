---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# apply any windi css classes to the current slide
class: 'text-center'
image: /pexels-kelly-2618118.jpg
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slide Deck for Vite Brown Bag
# persist drawings in exports and build
drawings:
  persist: false
# use UnoCSS (experimental)
css: unocss
---

<div class='flex flex-col justify-center items-center'>
  <img src="/vite-logo.png" class="h-90 shadow" />

  <div class='bg-black/60 w-screen center p10'>
    <h1 class='text-xxl'>Vite</h1>
    <p>The future is <strong>FAST</strong></p>
  </div>
</div>

---
layout: section
---

# What is Vite?

---

---
layout: bullets
---

- What is the meaning behind the name, Vite?
<v-clicks>
  + It the French word for “Fast”
- Created by Evan You, the creator of VueJS
</v-clicks>

<v-click>
  <img src='/vite-concept.png' class='w-150 mt-5 mx-auto' />
</v-click>

<!--
-->

---

# Features

<v-clicks>

- Built on top of [Esbuild](https://esbuild.github.io/)
  + 10 - 100x faster than current JavaScript-based bundlers
- Supports Hot Module Replacement (HMR) out of the box
- Built-in support for:
  + JSX
  + Typescript
  + CSS and CSS preprocessor like Sass and Less
  + Static assets such as images and JSON files
- Unbundled local development
  + Pre-bundles modules and converts commonJS to ESM
  + Rewrites imports to use the pre-bundled version making it browser importable
  + Strongly caches dependencies
- Replacement for webpack
- Great plugin API allowing tools to be built on top it or add functionality
- Only needs to compile your code changes

</v-clicks>

<!--
Esbuild is written in Go and compiled to native code making it incredible fast when compared to any javascript based compiler.
Uses Rollup for production builds
CSS – Can support scss, sass, less, styl and .stylus by default.
If the project contains a postcss file it will automatically be used during builds.
-->

---
class: 'text-center'
---


# Why switch to Vite?

<v-click>

  <img src='/christmas-vaction-sled.gif' class='m-auto' />

</v-click>

---

# Dev EX

<v-clicks>

- Incredibly fast dev server startup time 
- Fast production builds that stay consistent even as the project grows
- Has a single vite.config.js file with specific sections for vite, rollups production build, and testing configurations
- Vite is opinionated reducing the configuration needed to get started
  + Almost no decisions needed to get started

</v-clicks>

<!--
Dev server startup is typically around 300-500 ms 
Production builds have been around 40-45 seconds for RMN
-->

---

# Built With Vite

<v-clicks>

- [Vitest](https://vitest.dev/) – Vite replacement for Jest
  + 99% identical to the Jest API
  + Uses Vite for fast iterations
  + Smart retest only re-tests only files affected by change
- [Astro](https://astro.build/) – Meta Website Framework
  + Creates MPA’s that can either be SSG or SSR sites
  + Uses an islands architecture to create small or no js bundles
  + Can run Svelte, React, Solid, Vue, Lit, and many other frameworks and even include them on the same page!
- [AwesomeVite](https://github.com/vitejs/awesome-vite) – Community driven starter projects
  + CLI tool to quickly scaffold different types of projects 
- [Slidev](https://sli.dev/) - Slide/Presentation tool
  + Easily create a presentation using Markdown/Vite/VueJS/Tailwind and other tech
  + What these slides are built with!

</v-clicks>

---

# Who’s Using Vite?

- Laravel – Uses Vite by default in their projects
- Shopify – Hydrogen frontend framework uses Vite
- Ruby – Uses Vite to improve the Rails DX
- Nuxt, VitePress, SvelteKit, SolidStart – All use Vite by default as their bundler
- Storybook – Has an adapter to use in Vite projects
- More projects are switching each day and startups are being built on Vite

---

# Getting Started

<div v-click-hide>
```shell
npm create vite@latest
```
</div>

<v-click>
```shell
npm create vite@latest --template react
```
</v-click>

---

# RMN Experience

---

# Things to Consider

- Only supports ESM imports
  + If a package uses commonJS Vite will try to convert it
  + JSX files require a .jsx file extension
- Less documentation and examples than Webpack since it is newer
- More to stay on top of since they are moving and making changes fast.
