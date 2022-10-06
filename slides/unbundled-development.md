---
layout: bullets
---

# Unbundled Local Development

<v-clicks>

- Takes advantage of native browser ESM (Ecmascript Module) import/exports
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
