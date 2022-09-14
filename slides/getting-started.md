---
layout: section
---

# Getting Started

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# Code

Use code snippets and get the highlighting directly![^1]

```ts {2,3|5}
function add(
  a: Ref<number> | number,
  b: Ref<number> | number
) {
  return computed(() => unref(a) + unref(b))
}
```

<arrow v-click="3" x1="400" y1="420" x2="230" y2="330" color="#564" width="3" arrowSize="1" />

[^1]: [Learn More](https://sli.dev/guide/syntax.html#line-highlighting)

<style>
.footnotes-sep {
  @apply mt-20 opacity-10;
}
.footnotes {
  @apply text-sm opacity-75;
}
.footnote-backref {
  display: none;
}
</style>

---
layout: bullets
---

# Getting Started at Goodway

- We've created a getting started guide in the [Coding Standards](https://github.com/GoodwayGroup/coding-standards/blob/master/vite.md) to help teams get up and running quickly
- Brian updated the Goodway Generator with some sub-generators to have Goodway Standard frontend checks and conveniences easily added.
