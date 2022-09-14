---
layout: section
---

# Getting Started

```shell {1|2|3|5,6|8|all}
npm create vite@latest
npm create vite@latest my-react-app -- --template react
npx degit SafdarJamal/vite-template-react#main my-vite-react-cra

cd {project}
npm install

npm run dev
```

<a v-click="6" href="https://github.com/nordcloud/pat-frontend-template/blob/master/docs/CRA_MIGRATION_GUIDE.md" target="_blank" />

---
layout: bullets
---

# Getting Started at Goodway

- We've created a getting started guide in the [Coding Standards](https://github.com/GoodwayGroup/coding-standards/blob/master/vite.md) to help teams get up and running quickly
- Brian updated the Goodway Generator with some sub-generators to have Goodway Standard frontend checks and conveniences easily added.

```sh {1|2|3|4|all}
yo goodway:husky
yo goodway:configmap
yo goodway:changelog
yo goodway:conventionalCommits
```
