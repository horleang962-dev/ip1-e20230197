# AI Log

One entry per meaningful AI use.

## 2026-11-08 · Choosing a project domain
Tool: Claude
Asked: which domain in the project guideline is the smallest and easiest for me
Kept: Course feedback, because it has only 3 tables and mostly simple CRUD
Rejected: Restaurant orders, because it has 3 roles and a changing queue, which is too big for me
Checked by: read the domain table in the PDF and compared the roles and tables myself

## 2026-11-08 · UI design prompts for Google Stitch
Tool: Claude
Asked: write prompts to generate the screens for Course feedback on a laptop
Kept: the style prompt and the 6 screens (login, register, lectures, rate, my lectures, results)
Rejected: the "7 screens" wording, because there are only 6, so I changed it
Checked by: compared the generated screens with the roles and features in my spec

## 2026-11-08 · Project setup in WebStorm
Tool: Claude
Asked: how to create the Vue project and what options to choose
Kept: TypeScript, Router, Pinia, Vitest, Linter, Prettier; no JSX and no end-to-end tests
Rejected: nothing yet
Checked by: ran `npm install` and `npm run dev`, and the Vue welcome page opened