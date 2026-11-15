# Repository Guidelines

## Project Structure & Module Organization

The Vite/React website lives in `src/`. Page composition belongs in `src/pages/`, reusable UI in `src/components/<ComponentName>/`, global CSS in `src/styles/`, and imported artwork in `src/images/`. Static files served unchanged belong in `public/`. The repository also contains teaching materials: chapter exercises in `Notebooks/ChapXX/`, course notebooks in `CM20315/` and `CM52059/`, specialist examples in `Trees/` and `Blogs/`, presentation decks in `Slides/`, and downloadable figure archives in `PDFFigures/`. Keep large generated outputs out of source directories.

## Build, Test, and Development Commands

- `npm install` installs the locked dependencies from `package-lock.json`.
- `npm run dev` starts Vite at `http://localhost:3000`.
- `npm run build` creates the production site in `dist/`.
- `npm run preview` serves the production build locally on port 3000.
- `npm run lint` checks JavaScript and JSX with ESLint and permits no warnings.
- `npm run format` applies Prettier and organizes imports across the repository.

Use `npm run deploy` only when intentionally publishing the built `dist/` directory to GitHub Pages.

## Coding Style & Naming Conventions

Follow `.editorconfig` and Prettier: four-space indentation, LF endings, semicolons, double quotes, trailing commas, and a 100-character line width. Use ES modules and the `@/` alias for imports from `src`. React components and their directories use PascalCase (`HeroSection`); component entry points are `index.jsx`, while styled-component definitions use `<Name>Elements.jsx`. Functions, hooks, and props use camelCase.

## Testing Guidelines

No automated test framework or coverage threshold is currently configured. Before submitting website changes, run `npm run lint` and `npm run build`, then inspect affected routes and responsive layouts with `npm run preview`. For notebook changes, restart the kernel, run all cells in order, verify outputs, and avoid committing incidental execution noise or embedded secrets.

## Commit & Pull Request Guidelines

History favors short, imperative summaries such as `Fix terminal state` or scoped Conventional Commit messages such as `docs: correct ...`. Describe one logical change per commit. Pull requests should explain the motivation, list affected notebooks or UI areas, and record validation performed. Link relevant issues and include before/after screenshots for visible website changes. Do not mix broad notebook re-execution with unrelated code edits.
