# The Usul al-Fiqh Challenge

## Play locally
Open `index.html` in a modern browser.

## Publish as a shareable website (free)
1. Create a GitHub repository.
2. Upload `index.html` to the repository root.
3. In Settings → Pages, choose Deploy from a branch, select `main` and `/ (root)`, then Save.
4. GitHub Pages will provide a public URL to share with students.

You can also drag the folder into Netlify Drop (https://app.netlify.com/drop).

## Add future weeks
- Open the game and expand **Week Manager**.
- Download `week-template.json`.
- Copy the template and add questions. Each question needs:
  - `q`: question text
  - `options`: array of answer choices
  - `answer`: zero-based index of the correct option (0 = first option)
  - `explanation`: feedback shown after answering
  - `pages`: textbook page reference
- Import the JSON through Week Manager.
- Export all weeks to back up your course data.
- To distribute new weeks to all students, update and redeploy the site files. Browser-local imports are stored only on the device that imported them.

## Important
This first version is a static website. Each student's progress is local to their browser. It does not yet provide a shared online leaderboard, teacher dashboard, accounts, or synchronized scores. Those features need a backend/database.


## Week 2 and mixed question types

The updated game supports multiple-choice questions (the original format), written short-answer questions (`type: "short_answer"`), and fill-in table questions (`type: "table"`). Import `week-2.json` from the Week Manager. Written answers are checked against accepted variants; table cells are checked against their accepted terms.
