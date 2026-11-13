# Typoo ⌨️ · Learn to touch type

A free web app that teaches teens to type blind with all ten fingers.
It is one file (`index.html`). It needs no install, no account and no server.

## Features

- **27 lessons in 6 stages**: Home Row → Top Row → Bottom Row → Capitals & Sentences → Numbers → Speed Lab.
- **AZERTY (Belgian) and QWERTY** layouts, each with its own lesson order. The app detects the layout.
- **Dutch or English** practice words.
- **Keebo the robot coach** gives tips, cheers and corrections.
- **Gamification**: XP and levels, 1–3 stars per lesson, daily goal (10 min), day streak, 19 badges.
- **Race Keebo**: a typing race against the bot at a speed you pick.
- **Word Rain**: an arcade game. Type the falling words before they land.
- **Smart Practice**: drills that use your weakest keys.
- **Blind mode**: hide the key labels, or hide the full keyboard.
- **Backup code**: copy progress and restore it on another device.

## Teaching method

1. Fingers start on the home row. The bumps on F and J are the anchor.
2. Two new keys per lesson, then a review lesson per row.
3. An on-screen keyboard and hands show which finger to use. Each finger has its own colour.
4. A wrong key stops the cursor. The learner must type the correct key. This trains accuracy.
5. A lesson passes at 90% accuracy. Speed only matters for the 2nd and 3rd star.
6. Short daily sessions, with a streak, build the habit.

## Share with the kids (Chromebooks)

The stable app is on GitHub Pages: https://vincent-sobry.github.io/typoo/

1. Send the link to the kids. They can bookmark it in Chrome.
2. Progress is saved in the browser of each Chromebook (local storage). Nothing is sent to a server.

## Versions and releases

TL;DR: `main` is the stable app for the kids. New work goes to `dev` first and is tested on a preview link.

| Branch | Link | Use |
|---|---|---|
| `main` | https://vincent-sobry.github.io/typoo/ | Stable. The kids use this link. |
| `dev` | https://vincent-sobry.github.io/typoo/dev/ | Preview. Test new work here. |

The preview shows a red "DEV PREVIEW" label. It saves progress under its own key (`typo.dev.v1`), so tests never change the kids' progress (`typo.v1`).

### Flow

1. **Build:** make a branch from `dev` for each feature or fix. Open a pull request into `dev`.
2. **Test:** merge the pull request. After 1–2 minutes, test on the preview link.
3. **Collect:** keep merged features on `dev` until the batch is ready.
4. **Release:** open one pull request from `dev` into `main`. After the merge, create a release with a new version tag (for example `v1.1`) and a short changelog.
5. **Hotfix:** an urgent fix goes in a pull request straight into `main`. Then merge `main` back into `dev`.

### Deploy

The workflow `.github/workflows/pages.yml` publishes `main` at the root and `dev` in `/dev/`. It runs after each push to `main` or `dev`. In **Settings → Pages**, **Source** must be *GitHub Actions*.
