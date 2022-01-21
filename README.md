This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Problem

Even configuring "pageExtension" to be `page.tsx` or `page.tsx` in `next.config.js` file, I still get an error to a file which wasn't supposed to be treated as a page:

```
error - ./pages/about/ui/Header/index.ts
Error: error: Using `export * from '...'` in a page is disallowed. Please use `export { default } from '...'` instead.
Read more: https://nextjs.org/docs/messages/export-all-in-page

  |
1 | export * from "./Header";
  | ^^^^^^^^^^^^^^^^^^^^^^^^^
```

## Reproduce

1. Clone this repository
2. Install dependencies
3. Run `yarn dev`;
4. Access `http://localhost:3000/about`
5. See the error

## Note

This was working fine at v12.0.4, after 0.5 it starts the problem
