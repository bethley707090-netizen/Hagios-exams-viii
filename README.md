Hagios International School — Classroom Quiz
A simple objective-question (multiple choice) quiz app for classroom use.

Roles
Students — pick a teacher's quiz from a list, answer, and submit. Scores are saved automatically.
Teachers — sign in with a name + passcode (set up by the admin) to write their own multiple-choice questions and view results for their own quiz only.
Admin — signs in with a passcode to create/remove teacher accounts and view results across all teachers.
Important: where this runs
This file (classroom-quiz.jsx) was built as a Claude.ai artifact and uses Claude's built-in window.storage API to save teachers, questions, and results. That storage API only exists inside Claude's own artifact runtime.

This means:

✅ It works if published from Claude (Share → Publish & copy link) — that gives you a working public URL, no separate hosting needed.
❌ It will not work if you deploy this .jsx file as-is on GitHub Pages, Netlify, Vercel, or any other host — window.storage won't exist there, and saving/loading data will fail.
If you specifically need it hosted outside Claude (e.g. on the school's own web server), the storage logic (the window.storage.get / window.storage.set calls) would need to be swapped for a real backend — such as Firebase, Supabase, or a small custom server with a database. That's a separate build from what's here.

Default admin passcode
changeme123 — sign in as admin and change this immediately after first use.

Security note
Passcodes are stored in plain text, not encrypted. This is "keeps honest people honest" protection suitable for an internal school tool — not for sensitive or high-stakes data.
