# To Reproduce

1. `npx create-next-app@latest --experimental-app`
2. `npm install next@canary` (currently is `13.0.3-canary.1`)
3. `npm run build` (this finishes successfully)
4. Add a `/app/blog/[slug]/page.tsx` file as defined in the [docs](https://beta.nextjs.org/docs/api-reference/file-conventions/page).
5. `npm run build` (this fails)

# Error

```
Type error: Page "app/blog/[slug]/page.tsx" does not match the required types of a Next.js Page.
  Invalid configuration:
    The exported page component isn't correctly typed.
        Expected "{ params: { slug: string; }; searchParams: { id: string; }; }", got "PageProps".
```