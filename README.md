<h1 align="center">Pixel P.I.</h1>

<p align="center"><b>Ask anything. Catch every lie.</b></p>

<p align="center">A detective game where you type your own questions to suspects, in your own words.<br>
In Early Access on Steam · Windows, macOS and Linux · solo-developed</p>

<p align="center"><a href="https://store.steampowered.com/app/2448910/Pixel_PI/"><b>Steam</b></a> · <a href="https://store.steampowered.com/app/3758740/">Free demo</a> · <a href="https://pixelpigame.com/">Website</a> · <a href="https://crischu.itch.io/pixel-pi">itch.io</a> · <a href="https://discord.gg/RnbczNqnQ8">Discord</a></p>

<p align="center"><img src="assets/hero_ask_question.gif" alt="Typing &quot;where were u when she died&quot; to the main suspect, and his statement decrypting"></p>

> This repository is a showcase of the game and how it was made. The game's source code is private.

## The idea

Most detective games give you a menu of questions. You click through them, and the game does the
thinking for you.

In Pixel P.I. there's no menu. You play **Pixel**, a hacker detective who has lost two years of
memories. All she has is a list of old police case IDs, and a floating robot called **Ethan** who
says he was her partner. She hacks the police database to reopen each case. Every interview is
there, but the statements are encrypted: **each one decrypts only when you ask the question the
police asked**, phrased however you like.

So the questions are yours, and so is the "aha".

## How you play

### Ask anything

Type a question in your own words. If the police asked something like it, the statement decrypts.
If they didn't, the database tells you so, and you try another angle.

![An off-topic question gets "This question was not asked by the interviewer"; then "so what do you do for work?" unlocks the answer](assets/free_phrasing_and_no_match.gif)

Some statements have **two layers**: the second one only opens once you know more about the case.

### Debunk

Found a clue that contradicts a statement? Pick it, then explain **in your own words** why the
statement is false. If you're right, the statement is struck through as DEBUNKED, the witness has
to correct it, and the case opens up.

![The tutorial alibi debunk: choosing the clue, writing the explanation, "Debunk successful!" and the corrected statement](assets/debunk_alibi.gif)

### Follow the clues

Clues and evidence cards unlock through answers, debunks and the story. A handbook (alibi, motive,
personal information, debunks…) helps you keep track, and general clue cards like Pixel's notebook
fill in her world.

![The victim's death report decrypting, then the general clues and Pixel's notebook](assets/clues_and_notebook.gif)

When you think you know who did it, you accuse. It can't be undone.

## The cases

Four cases are out, and two more are coming.

| | Case | The setup |
|---|---|---|
| 1 | **The Axe Murderer** (tutorial) | Bernie, a journalist investigating the city's black market, is killed with an axe on her way home from the supermarket. |
| 2 | **The Broken Case** | John, the owner of a trading card store, is killed. Days earlier his neighbour William had reported him to the police, then withdrew the report. |
| 3 | **The Remorseful Doctor** | Danton, a heart surgeon who used to work for the Zeus Health Alliance, is found dead in his bedroom with a gun in his hand. |
| 4 | **The ABCD Murder** | Barbara, a senior engineer, is found dead in the ABC Brain Components lab. Her team and the IT admin are under pressure. |
| 5 | *Melody of an Unsung Tragedy* | In development |
| 6 | *The Final Case* | Planned |

![One question each to William (case 2), Celine (case 3) and Dan (case 4)](assets/interviews_cases_2_3_4.gif)

The world is near-future Saint Remy, in the Republic of Waveland, around 2089: brain implants,
holographic calls and quantum computers, all presented as a retro hacker's desktop with draggable
windows, a CRT filter and glitching encrypted text.

## Screenshots

<table>
<tr>
<td><img src="assets/screenshot_01_title_screen.png" alt="Title screen"></td>
<td><img src="assets/screenshot_02_case_select.png" alt="Case select"></td>
</tr>
<tr>
<td><img src="assets/screenshot_03_opening_ethan.png" alt="The opening, with Ethan"></td>
<td><img src="assets/screenshot_04_case1_statement_unlocked.png" alt="A statement unlocking in the interview database"></td>
</tr>
<tr>
<td><img src="assets/screenshot_05_case1_clue_death_report.png" alt="The death report clue"></td>
<td><img src="assets/screenshot_06_case1_debunk.png" alt="A successful debunk"></td>
</tr>
<tr>
<td><img src="assets/screenshot_07_case1_handbook.png" alt="The handbook"></td>
<td><img src="assets/screenshot_08_case2_william.png" alt="Case 2: William's interview"></td>
</tr>
<tr>
<td><img src="assets/screenshot_09_case3_celine.png" alt="Case 3: Celine's interview"></td>
<td><img src="assets/screenshot_10_case4_dan.png" alt="Case 4: Dan's interview"></td>
</tr>
</table>

**Gameplay video** (58 s, no sound): [assets/pixel_pi_gameplay.mp4](assets/pixel_pi_gameplay.mp4)

## In numbers

![Pixel P.I. in numbers: 200+ copies sold, ~1,000 wishlists, 10 Steam reviews (9 positive), $5.99, 13 achievements, 3 platforms; 4 of 6 cases out, 15 interviews, 321 statements to unlock, 66 case clue cards plus 16 general clues, 500+ story dialogue lines, 1 developer](assets/numbers.png)

## How it's built

The game is a **Unity** client (C#, URP, Steamworks) for Windows, macOS and Linux. While you play,
a small **game server** in the cloud answers your interview questions and checks your debunks, and
**Steam** takes care of the store, sign-in, achievements, stats and cloud saves.

Cases are **content, not code**. I plan the story in a wiki, write each case in my own case editor,
check every interview with a consistency script, and a one-window build pipeline ships the demo
and the full game to Steam for all three platforms.

![How it's built: the dev machine (story wiki, case editor, consistency check, editor tools, Unity project, build pipeline), the game server and Steam online, and the Unity client on the player's PC](assets/architecture.png)

## Tools I built for it

A game like this is mostly writing, so most of the tooling is about writing cases well and
shipping them safely.

![Tools built for the game: Case GUI Editor, Case editor v1, Story wiki, Consistency check, Police reports, UI kit builders, FX tools, Build pipeline, Automated QA, Capture rigs, Reveal Lab, Case generator (experiment)](assets/tools.png)

## Timeline

![Development timeline: first prototype in 2024, the current project from September 2024, the free demo in May 2025, Early Access in August 2025, case 3 in October 2025, case 4 in June 2026, the v0.4.0 build in October 2026, cases 5 and 6 next](assets/timeline.png)

## Credits

![Credits: coding, writing, pixel art and music arrangement by Cristian Desivo; music arranges public-domain classical pieces, some from Xavier Durot's scores; some backgrounds are CraftPix assets; sound effects are third-party; playtesting by Daniy, proofreading by Ash S. TuDust](assets/made_by.png)

## Play it

- **Steam:** [full game](https://store.steampowered.com/app/2448910/Pixel_PI/) · [free demo](https://store.steampowered.com/app/3758740/)
- **Website:** [pixelpigame.com](https://pixelpigame.com/) · **itch.io:** [crischu.itch.io/pixel-pi](https://crischu.itch.io/pixel-pi) · **Discord:** [discord.gg/RnbczNqnQ8](https://discord.gg/RnbczNqnQ8)

---

Made by **Cristian Desivo** (Crischu on Steam). More of my work: [case studies](https://github.com/crisdesivo/case-studies) · [cristiandesivo.com](https://cristiandesivo.com/)
