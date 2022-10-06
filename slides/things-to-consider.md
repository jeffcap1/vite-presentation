---
layout: bullets
---

# Things to Consider

<v-clicks>

- JSX files require a .jsx file extension
- Requires Node 14.18+ and Node 16+
- Only supports ESM imports
  + Your files must use esm module export/import
  + If a package uses commonJS Vite will try to convert it
- Need to switch <code>process &#46; env &#46; REACT_APP_XXXX</code> to <code>import &#46; meta &#46; env &#46; VITE_XXXX</code>
- Less documentation and examples than Webpack since it is newer
- More to stay on top of since they are moving and making changes fast.
- StoryShots currently does not work since only Jest is supported, but there is an open Vitest feature request.

</v-clicks>
