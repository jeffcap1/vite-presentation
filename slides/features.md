---
layout: section
---

# Features

---

# [Esbuild](https://esbuild.github.io/)

<ul v-click='3'>
	<li>10 to 100x faster than current JS based bundlers</li>
</ul>
<img v-click='2' src="/esbuild-timing-line.jpg" />
<img v-click='1' src="/esbuild-other-platforms-timings.jpg" />

<!--
This is a replacement for Webpack
Esbuild is written in Go and compiled to native code making it incredible fast when compared to any javascript based compiler.
-->

---

# Unbundled Local Development

<v-clicks>

- Pre-bundles modules and converts commonJS to ESM
- Rewrites imports to use the pre-bundled version making it browser importable
- Strongly caches dependencies
- Only needs to compile your code changes

</v-clicks>

<!--
Why pre-bundle: lodash-es has over 600 internal modules! When we do import { debounce } from 'lodash-es', the browser fires off 600+ HTTP requests at the same time!
Explain briefly and then show Vite pictures
-->

---

# Current Local Dev Flow
![Bundler based dev server](/bundle-based-dev-server.svg)

---

# New Local Dev Flow
![ESM based dev server](/esm-based-dev-server.svg)

---
layout: bullets
---

# Other Great Features

<v-clicks>

- Tiny Bundle Size
- Easy Code Splitting
- Hot Module Replacement (HMR)
- Typscript support out of the box
- Great plugin API - Allows tools to be built on top

</v-clicks>

<!--
Uses Rollup for production builds
Updates can be made in vite.config.js and are well defined
-->

---

<!-- Image slide that shows different file types ?? -->
# Built-in support for

- <mdi-language-jsx class="text-[#366FD7]" /> JSX
- <vscode-icons-file-type-typescript-official /> Typescript
- <vscode-icons-file-type-css /> CSS
- <vscode-icons-file-type-scss/> CSS preprocessors like Sass and Less
- <vscode-icons-file-type-image /> Static files like images
- <vscode-icons-file-type-json /> JSON files

<!--
No loaders needed!
CSS – Can support scss, sass, less, styl and .stylus by default.
If the project contains a postcss file it will automatically be used during builds.
-->
