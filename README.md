# Summary

## Setup

```
npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn-starter/tree/master/learn-starter"
```

---

## Navigate between pages

> Next. js ships with its own built-in page-based routing system, whereas the typical SPA relies on client-side routing, typically using a library like react-router.

Client-side routing, react-routing-dom counterpart? `Link`

Code-splitting done automatically, no need to worry about having 99939299 pages.

Next.js automatically prefetches.

> Next.js automatically optimizes your application for the best performance by code splitting, client-side navigation, and prefetching (in production).

---
## Assets, metadata, and CSS.

> Next.js has built-in support for CSS and Sass.

note `npm install sass` (for sass enjoyer)

`Image` normal stuffs + optimization.

`Head` normal stuffs - scripts, they go `next/script` ; - html tag, they go dir `pages/_document.js`

By default includes styled-jsx too. => try tailwind someday

> This is what CSS Modules does: It automatically generates unique class names. As long as you use CSS Modules, you don’t have to worry about class name collisions.

### Global Styles

dir `pages/_app.js`, import css module. Tho global css file can be stored anywhere anyhow (?)

### TailwindCSS

```
npm install tailwindcss postcss-preset-env postcss-flexbugs-fixes
```
`postcss.config.js`

`tailwind.config.js`

```jsx
className="rounded-full"
```
---

## Pre-rendering and data fetching

React : no pre-rendering, relaying on client js to generate html, normal stuff

1. Static : pre-render at build time

2. Server-side : on each request

Can choose which one to use for each page

parsing md => `npm install gray-matter`
render md => `npm install remark@13 remark-html@13`

> Next.js polyfills fetch() on both the client and server. You don't need to import it.

`getStaticProps` only runs on the server-side, not even bundled. can ONLY exported from a page

need to pass context to `getServerSideProps`

User-specific pages such as dashboard aren't related to SEO therefore client-side fetch is ok

Try <b>useSWR</b> hook for client-side rendering

---
## Dynamic Routes








