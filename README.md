## Summary

### Setup

```
npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn-starter/tree/master/learn-starter"
```

### Navigate between pages

> Next. js ships with its own built-in page-based routing system, whereas the typical SPA relies on client-side routing, typically using a library like react-router.

Client-side routing, react-routing-dom counterpart? `Link`

Code-splitting done automatically, no need to worry about having 99939299 pages.

Next.js automatically prefetches.

> Next.js automatically optimizes your application for the best performance by code splitting, client-side navigation, and prefetching (in production).

### Assets, metadata, and CSS.

> Next.js has built-in support for CSS and Sass.

note `npm install sass` (for sass enjoyer)

`Image` normal stuffs + optimization.

`Head` normal stuffs - scripts, they go `next/script` ; - html tag, they go dir `pages/_document.js`

By default includes styled-jsx too. => try tailwind someday

> This is what CSS Modules does: It automatically generates unique class names. As long as you use CSS Modules, you don’t have to worry about class name collisions.

#### Global Styles

dir `pages/_app.js`, import css module. Tho global css file can be stored anywhere anyhow (?)

#### TailwindCSS

`npm install tailwindcss postcss-preset-env postcss-flexbugs-fixes`
`postcss.config.js`
`tailwind.config.js`


