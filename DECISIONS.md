# Decisions

One line per real design choice.

- 2026-11-08: Domain is Course feedback, because it is small (3 tables, 2 roles) and I can finish it.
- 2026-11-08: Vue Router for page navigation, because the app has several pages (login, lectures, results).
- 2026-11-08: Pinia to store the logged-in user and token, so every page can read it.
- 2026-11-08: Vitest for component tests, because the guideline requires it.
- 2026-11-08: One repository with `frontend/` and `backend/` folders, as the guideline requires.
- 2026-11-08: Unique pair (lectureId, studentId) on Feedback, so a student can rate a lecture only once.
- 2026-11-08: Anonymous feedback means the results API never returns `studentId`.