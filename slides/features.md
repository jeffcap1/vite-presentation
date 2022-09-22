---
layout: section
---

# Features

---
layout: bullets
---

# [Esbuild](https://esbuild.github.io/)

<img v-click='3' src="/esbuild-timing-line.jpg" />
<img v-click='1' src="/esbuild-other-platforms-timings.jpg" />
<ul>
	<li v-click='2'>For context, three.js is 585kb minified and 150kb gzip</li>
	<li v-click='4'>10 to 100x faster than current JS based bundlers</li>
</ul>

<!--
This is a replacement for Webpack
Esbuild is written in Go and compiled to native code making it incredible fast when compared to any javascript based compiler.
-->

---
layout: statement
---

# Wow, that's impressive
# What is the configuration like?

---
layout: two-cols
---

# Webpack Config

<div class="mr-2 overflow-y-scroll h-100">
	<WebpackConfigCRA v-click />
</div>

::right::

# Vite Config

<div class="ml-2 overflow-y-scroll h-100">
	<ViteConfig v-click />
</div>

---
layout: bullets
---

# Unbundled Local Development

<v-clicks>

- Pre-bundles modules and converts commonJS to ESM
- Rewrites imports to use the pre-bundled version making it browser importable
- Strongly caches dependencies
- Only needs to compile your code changes

</v-clicks>

<!--
- Why pre-bundle:
	+ lodash-es has over 600 internal modules!
	+ When we do import { debounce } from 'lodash-es', the browser fires off 600+ HTTP requests at the same time!
- Explain briefly and then show Vite pictures
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

# Bundled in Production

<v-clicks>

- Vite bundles to production using a preconfigured version of Rollup
- Uses Rollup instead of esbuild since it's more mature and feature rich
- Http/2 and esm are still ineffecient with multiple round trips to server
- Ensures website still works with new and old browsers
- Enables tree shaking, lazy loading, and common chunks

</v-clicks>

<!--
- esbuild is great for bundling library code
- missing some important features for apps like coe spliting and css
- remember back to the lodash-es example with over 600 internal modules, we wouldn't want that in production.
-->

---
layout: bullets
---

# Other Great Features

<v-clicks>

- Tiny Bundle Size
- Easy Code Splitting
- Hot Module Replacement (HMR)
- Typescript support out of the box
- Great plugin API - Allows tools to be built on top

</v-clicks>

<!--
Uses Rollup for production builds
Updates can be made in vite.config.js and are well defined
-->

---

# Built-in support for

- <mdi-language-jsx class="text-[#366FD7]" /> JSX
- <vscode-icons-file-type-typescript-official /> Typescript
- <vscode-icons-file-type-css /> CSS
- <vscode-icons-file-type-scss/> CSS preprocessors (Sass, Scss, Less, etc.)
- <vscode-icons-file-type-image /> Static files like images
- <vscode-icons-file-type-json /> JSON files

<!--
No loaders needed!
CSS – Can support scss, sass, less, styl and .stylus by default.
If the project contains a postcss file it will automatically be used during builds.
-->
