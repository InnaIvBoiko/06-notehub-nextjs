# NoteHub

A multi-page note-taking app built with Next.js (App Router). Browse, search, create, delete, and view the details of
your notes, with SSR + CSR powered by TanStack Query.

- **Live demo:** https://06-notehub-nextjs-wheat-seven.vercel.app/
- **Repository:** https://github.com/InnaIvBoiko/06-notehub-nextjs

## Tech stack

- [Next.js](https://nextjs.org) (App Router)
- [TypeScript](https://www.typescriptlang.org)
- [TanStack Query](https://tanstack.com/query) (React Query)
- [Axios](https://axios-http.com)
- [Formik](https://formik.org) + [Yup](https://github.com/jquense/yup) for note creation
- CSS Modules

## Routes

| Route         | Description                                                             |
| ------------- | ----------------------------------------------------------------------- |
| `/`           | Home page with general information about the app.                       |
| `/notes`      | Note list with search and note creation (SSR prefetch + CSR hydration). |
| `/notes/[id]` | Details of a single note (SSR prefetch + CSR hydration).                |

## Project structure

- `app/` — routes, layouts, loading/error boundaries.
- `components/` — shared, route-agnostic UI components, each in its own folder with a `.tsx` and `.module.css` file.
- `lib/api/` — Axios client and API request modules.
- `types/` — shared TypeScript types.

## Getting started

1. Install dependencies:

    ```bash
    npm install
    ```

2. Create a `.env` file based on `.env.example` and set your NoteHub API token:

    ```bash
    NEXT_PUBLIC_NOTEHUB_TOKEN=your_token_here
    ```

3. Run the development server:

    ```bash
    npm run dev
    ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Scripts

- `npm run dev` — start the development server.
- `npm run build` — build the app for production.
- `npm run start` — start the production server.
- `npm run lint` — run ESLint.
- `npm run format` — format the code with Prettier.
- `npm run format:check` — check code formatting with Prettier.
