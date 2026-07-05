# 🚀 Start Here — Build a 3D Game as a Family (No Coding Experience Needed)

This guide takes you from **"we have nothing"** to **"our own 3D game is live on
the internet"** in about 20 minutes — and then shows you how to keep building it
with Claude, one idea at a time.

It's written for **parents and kids building together**. You don't need to know
how to code. You don't need to install anything. Everything can be done **100%
free** in a web browser.

**What you'll have at the end:**
- 🌍 Your own copy of a real 3D game (a sunny courtyard with a fountain,
  trees, and floating crystals) — [see the live demo](https://markjeromecruz.github.io/threejs-claude-starter/)
- 🔗 A public link you can send to grandparents, cousins, and friends
- 🤖 A way to change the game just by *describing what you want* to Claude

**Who does what:** online accounts need a grown-up — GitHub requires users to be
13+, and Claude requires 18+. So the setup is: **the grown-up owns the accounts
and drives the keyboard; the kid is the Game Designer** who decides what gets
built. You'll create two free accounts along the way — **GitHub** (stores and
publishes the game) and **Claude** (builds it). That's exactly how the family
game this template came from was made.

> 💻 **Use a computer, not a phone or tablet, to build.** Some GitHub buttons
> hide on small screens. We recommend the free **Google Chrome** browser — the
> keyboard shortcuts in this guide assume it. Safari works too; where it's
> different, we call it out.

---

## Part 1 — Create your free GitHub account (5 minutes)

GitHub is a free website that stores your game's code and — this is the magic
part — **publishes it to the internet for free**.

1. Go to **[github.com](https://github.com)** and click **Sign up**.
2. Enter your email, create a password, and **choose a username**.
   > 🔒 **Choose the username carefully — it becomes part of your game's public
   > web address, which you'll share widely.** If your username is `sunshinefam`,
   > your game lives at `https://sunshinefam.github.io/your-game-name/`. **Don't
   > use a full name, a surname, a birth year, or anything identifying** — a
   > made-up word or hobby name is perfect (letters, numbers, hyphens only).
   > This is the grown-up's account, so pick it yourself rather than with the
   > kid.
3. Follow the prompts (there's a quick puzzle to prove you're human, and a
   verification code sent to your email — keep your email open).
4. If GitHub asks about plans, the **Free** plan is all you need. **No credit
   card, ever.**

✅ **You'll know it worked when:** you're logged in and see your GitHub home page.

---

## Part 2 — Get your own copy of the game (2 minutes)

You're going to "stamp out" your own copy of this template. Your copy is 100%
yours — nothing you do to it can affect anyone else's game.

1. Go to **[github.com/markjeromecruz/threejs-claude-starter](https://github.com/markjeromecruz/threejs-claude-starter)**.
2. Click the green **Use this template** button (top right) → **Create a new
   repository**. ("Repository," or "repo," is just GitHub's word for a project
   folder.)
3. Fill in the form:
   - **Repository name:** this becomes the last part of your game's web address.
     Let the kid pick! `dragon-world`, `puppy-park`, `crystal-kingdom`…
     (lowercase, hyphens instead of spaces, no personal info)
   - **Public** must be selected (it's the default). Free publishing only works
     for public projects — see the safety note below.
4. Click **Create repository**. After a few seconds you'll be looking at *your*
   copy of the game.

📌 **Bookmark this page now** — it's your repo, the home base where every change
happens. (Lost it later? Go to [github.com](https://github.com), sign in, and
your repos are listed on the left.)

> 🛡️ **A note for parents on "Public":** public means anyone *could* view your
> game's code — which is normal and how most open-source projects work. It's
> completely safe **as long as you keep personal information out of the game**:
> no last names, addresses, school names, phone numbers, or family photos.
> Character names and first names are fine. This is also a great early internet-
> safety conversation to have with your Game Designer. 🙂

✅ **You'll know it worked when:** the page shows `your-username/your-game-name`
at the top, with files like `index.html` and `src` listed.

---

## Part 3 — Publish your game to the internet (3 minutes)

This turns your copy into a real, live website using **GitHub Pages** — GitHub's
free hosting. You only do this once; afterwards, every change republishes
automatically.

1. On your repository page, click **Settings** (the tab with a ⚙️ gear, in the
   top row — if you don't see it, widen the browser window).
2. In the left sidebar, click **Pages** (under "Code and automation").
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Under **Branch**, pick **`main`**, keep the folder as **`/ (root)`**, and
   click **Save**.
5. Wait a couple of minutes, then **refresh the page**. A box appears at the
   top: **"Your site is live at `https://your-username.github.io/your-game-name/`"**.
6. Click that link. 🎉

✅ **You'll know it worked when:** you see a loading screen that fades into a
sunny 3D courtyard with a fountain, trees, and five floating crystals. Drag to
look around, scroll to zoom, use the arrow keys (or WASD) to glide.

> 🐢 **Not there yet?** The very first publish is the slowest — GitHub says it
> can take **up to ~10 minutes** (everyday changes later usually appear in about
> a minute). Wait, then refresh. If you still see a **404** page, double-check
> step 4 (branch `main`, folder `/ (root)`) and that your repository is
> **Public**. You can watch progress on the repo's **Actions** tab — a green ✓
> on "pages build and deployment" means it published.

📌 **Bookmark your game's link too**, and send it to someone you love. It updates
automatically every time you change the game from now on.

---

## Part 4 — Choose how you'll build with Claude

Both ways below need a **free Claude account**: go to **[claude.ai](https://claude.ai)**,
click **Sign up** (grown-up's account — Claude is 18+), and verify your email.
Then pick the path that fits your family:

| | **Path A: claude.ai + GitHub website** | **Path B: Claude Code** |
|---|---|---|
| Cost | Works on Claude's **free** plan | Needs a Claude **Pro/Max** plan |
| Install anything? | No — just browser tabs | Optional (web version exists too) |
| How it feels | You're the messenger: Claude writes the code, you paste it in | Claude does everything: edits, saves, publishes |
| Best for | Trying it out, casual building | Building a lot, the smoothest experience |

Both paths build the exact same game. Many families start with Path A and
upgrade later.

---

### Path A — claude.ai + copy-paste (free, nothing to install)

The loop is: **kid describes → Claude writes the whole file → you paste it into
GitHub → the game updates itself.**

**One-time setup:** open **[claude.ai](https://claude.ai)**, start a **new
chat**, and paste this **Kickoff Message** — after replacing `YOUR-USERNAME` and
`YOUR-GAME-NAME` (in **both** links) with your real ones:

```text
I'm a parent building a 3D browser game with my kid. We started from the
"threejs-claude-starter" template — a zero-build three.js + anime.js game.
We are NOT programmers, so please be our friendly game programmer.

Our game:
- Code file: https://raw.githubusercontent.com/YOUR-USERNAME/YOUR-GAME-NAME/main/src/main.js
- Live game: https://YOUR-USERNAME.github.io/YOUR-GAME-NAME/

How we'll work together:
1. My kid will describe ONE idea at a time, in their own words.
2. At the START of a session, read our current code from the link above so you
   have the latest. DURING a session, build on the newest COMPLETE file you
   sent me in THIS chat — the link can lag a few minutes behind our latest
   save, so your own last version is the source of truth mid-session. If you
   ever can't open the link, just ask and I'll paste the file in.
3. Reply with the COMPLETE updated file in ONE code block — never a partial
   snippet or "add this after line 20" — because I copy-paste the entire file
   into GitHub. Almost every change lives in src/main.js.
4. If a change truly needs a DIFFERENT file (for example the game's title,
   which lives in index.html), say so plainly, tell me exactly which file to
   open, and give me the COMPLETE new version of THAT file. If you need that
   file's current contents first, ask and I'll paste them.
5. After the code, explain what changed in 1-2 kid-friendly sentences.
6. Keep the game zero-build: only import from 'three', 'three/addons/...', and
   'animejs' (already included via an importmap). Never add CDN links, external
   URLs, or new libraries. Keep all file paths relative (./...). Keep every
   part of the game kid-appropriate.
7. If an idea is too big for one step, build the first small visible piece and
   tell us what could come next. If our file ever gets too long to send in one
   reply, suggest splitting it into a few smaller files and walk us through it.
8. If we say something broke, give us back the last COMPLETE working version of
   the file (or a fix) — always a complete file, never a fragment.

To start: please read our code file and tell us in a few sentences what the
game currently has — then ask my kid what they'd like to add first!
```

> 🔎 **First-time toggle:** for Claude to open your code link, the **web search /
> web tool** must be on in the chat (look for a tools/settings icon near the
> message box and enable it — it's available on the Free plan). If it's off,
> no problem: when Claude asks, paste the file in yourself (see the tip below on
> getting your code out of GitHub).

**Then, for every idea:**
1. 🧒 The kid describes an idea (their own words are perfect — see the
   [Prompt Idea Book](PROMPT-IDEAS.md) if they want inspiration).
2. 🤖 Claude replies with the complete new code block. Note **which file** it
   says to update (almost always `src/main.js`). Click the **copy** button at
   the top of the code block.
3. 💻 In your repo tab, open that file:
   - for **`src/main.js`**: click the **`src`** folder, then **`main.js`**;
   - for **`index.html`**: it's right on the repo's front page (not inside
     `src`).
   Then click the **✏️ pencil** (top right of the file view) to edit.
4. Select everything in the editor (**Ctrl+A** / **Cmd+A**), paste, then click
   the green **Commit changes...** button → **Commit changes** again.
   (A "commit" is just a save. The message box is a label — type what changed,
   like `added rainbow crystals`, or keep the suggestion. Every commit is kept
   forever, so you can always go back — see "Go back in time" below.)
5. ⏱️ Wait about a minute, then refresh your game link. If it looks unchanged,
   do a **hard refresh**:
   - **Chrome / Edge / Firefox:** Cmd+Shift+R (Mac) or Ctrl+Shift+R (Windows)
   - **Safari:** Cmd+Option+R (or hold **Shift** and click the reload button)

> 💡 **Path A tips**
> - **One file per paste — never mix them up.** Paste the code Claude gave for
>   `main.js` into `main.js`, and code for `index.html` into `index.html`.
>   Pasting one file's code into the other is the #1 cause of a black screen.
> - **If Claude's reply gets cut off** mid-code, say **"continue"** — but now
>   you have two code blocks. Don't try to glue them yourself: instead say
>   **"please resend the whole file as one code block"** and paste that single
>   block. (If a file ever gets too big for one reply even after that, ask
>   Claude to **"split the game into a few smaller files"** — it'll guide you.)
> - **Getting your code OUT of GitHub** (for when Claude asks you to paste it):
>   open the file in your repo and click the **Raw** button (or the copy-icon)
>   to see the plain text, then select-all and copy.
> - **Making a brand-new file** Claude gives you: on your repo page use
>   **Add file → Create new file**, type the exact name Claude says (e.g.
>   `src/sounds.js`), paste, and commit.
> - **The free plan has usage limits** that reset on a rolling window (a few
>   hours), not a strict daily cap — a focused 30–60 minute session is the sweet
>   spot anyway. If you hit the limit mid-session, you're not done for good; take
>   a break and come back in a few hours. End on a win! 🎉
> - Have Claude **Pro**? You can connect your GitHub repo to a Claude
>   **Project** so Claude has your code without links — just remember it takes a
>   **snapshot** and you must click **Sync** after you commit changes, or it'll
>   answer from an older version.

> ☀️ **Coming back tomorrow (Path A).** Two good options:
> - **Same chat:** scroll back to your claude.ai conversation and keep going —
>   Claude still remembers your game. (If you ever see *"this conversation has
>   reached its maximum length,"* the chat is full — start a new one as below.)
> - **New chat:** paste the **Kickoff Message** again first (that's what teaches
>   Claude the rules and where your code is), then continue. Starting fresh
>   *without* the kickoff is why Claude sometimes replies with snippets instead
>   of the whole file — the kickoff prevents that.

> ⏪ **Go back in time (Path A).** Broke something and Claude can't recover it
> (e.g. it's a new chat)? Your last good version is safe in GitHub:
> 1. In your repo, open the file (e.g. `src/main.js`) and click **History**.
> 2. Click a commit from *before* it broke.
> 3. Click the **⋯** (or "View file" / the file name) to see the **whole file at
>    that point** — **not** the red/green comparison view. (If you only see
>    +/− lines, you're looking at the diff; use "View file" to get the clean
>    version.)
> 4. Copy it, then paste it back into the file with the pencil, and commit.
>    You're restored. Nothing is ever truly lost. 💙

---

### Path B — Claude Code (the deluxe way)

[Claude Code](https://claude.com/claude-code) is Claude with hands: it reads
your whole project, makes the edits, saves the versions, and publishes — you
just talk. It automatically reads this repo's [`CLAUDE.md`](CLAUDE.md), which
teaches it the house rules (no build steps, free CC0 assets only, one idea at a
time, kid-friendly explanations).

**Easiest — Claude Code on the web (no install):**
1. Go to **[claude.ai/code](https://claude.ai/code)** and connect your GitHub
   account when asked.
2. Pick your game repository and describe what you want, e.g.
   *"Make the crystals rainbow-colored."*
3. Claude makes the change and proposes it. Approve/merge it when it's ready
   (Claude will tell you exactly what to click), wait a minute, refresh your
   game link.

**Most powerful — Claude Code on your computer:**
1. Install the [desktop app or CLI](https://claude.com/claude-code) and open it.
2. Ask Claude Code itself to set you up — it's good at this:
   *"Clone https://github.com/YOUR-USERNAME/YOUR-GAME-NAME and open it."*
3. Describe ideas. Claude edits, commits, and pushes; your live game updates
   ~1 minute after each push. Bonus: ask it to *"start a local server so we can
   preview instantly"* and you'll see changes right away without waiting for
   publishing. Don't have Python or any dev tools? You don't need to set them up
   yourself — Claude Code figures out what's needed and walks you through it. The
   very first time it installs something on a brand-new Mac or PC, you may see
   one system dialog to approve and be asked for your computer password; Claude
   tells you exactly what to click, and after that it's automatic. (This only
   affects the optional instant preview — editing, saving, and publishing your
   game always work.)

> 🔐 **One privacy note for local Path B:** commits you make from your own
> computer can attach your real name and email to the public repo. Before your
> first commit, either let Claude Code set a private GitHub **noreply** email
> for you (just ask: *"set my git email to my GitHub noreply address"*) or turn
> on **"Keep my email addresses private"** in GitHub → Settings → Emails. (Path
> A web edits don't have this issue.)

---

## Part 5 — Your first change (a guaranteed win)

Start with something **instantly visible** and impossible to get wrong. Great
first asks:

> *"Make the floating crystals rainbow-colored, and add five more of them."*

> *"Make it sunset — pink and orange sky."*

> *"Make the fountain area twice as big with more trees."*

Make the change, wait a minute, refresh the game link… and watch the Game
Designer's face. 🎉 Then send the link to a grandparent.

> ✍️ **Want to rename the game** from "3D World" to your own title? Just ask
> Claude — the title lives in `index.html`, not `main.js`. On **Path B** Claude
> edits it directly; on **Path A** Claude will hand you the complete
> `index.html` to paste (same steps as always — just open `index.html` on your
> repo's front page instead of `src/main.js`).

---

## How to talk to Claude — the family workflow

This is the actual workflow the original family used to grow this exact starter
into a whole town with quests, neighbors, and a pet dog:

- **One idea per message.** "Add a pond" then "put ducks on it" beats
  "add a pond with ducks and fish and a bridge and a boat."
- **Kids' words work.** "Make the crystals bounce like they're excited" is a
  *great* prompt. Describe what you want to **see**, not code.
- **Small steps, big dreams.** If the dream is "make Minecraft," the first step
  is "let me place a block where I click." Claude will help break big ideas down.
- **Every save is a save point.** Each change you commit is kept forever in your
  repository's history — you can *always* go back (see "Go back in time" above).
- **"Undo" is always safe to say.**
  - Path B: just say *"undo that last change."*
  - Path A (same chat): say *"that broke / we don't like it — give us the
    complete previous working version again."* If it's a new chat and Claude no
    longer has it, use **"Go back in time"** above to restore from GitHub — that
    always works.
- **Let the kid drive the ideas.** The grown-up types and pastes; the designer
  decides what the world needs next. Take turns if there are multiple designers
  — or make each kid their own copy of the template!

## When something goes wrong (it will — that's normal)

| What you see | What to do |
|---|---|
| Game didn't change after a paste | Wait a couple of minutes, then **hard refresh** (Chrome/Edge/Firefox: Cmd+Shift+R / Ctrl+Shift+R · Safari: Cmd+Option+R). Check your repo's **Actions** tab — a green ✓ on "pages build and deployment" means it published. |
| A change we made earlier disappeared | Claude probably built on an older copy of the file. Tell it: *"you built on an old version — here's our current code,"* and paste your latest `main.js` from GitHub (open the file → **Raw** → copy). Then re-ask the idea. |
| Black or empty screen | A code error. Open the browser **Console** and tell Claude what it says: **Chrome/Edge/Firefox** — press F12 (Mac: Cmd+Option+J) → **Console**. **Safari** — first enable Settings → Advanced → *Show features for web developers*, then Cmd+Option+C. Copy any **red** text and tell Claude: *"the game shows a black screen and this error: …"* Kids make great bug detectives. 🔍 |
| 404 page at your game link | Pages isn't set up or still building (first publish can take ~10 min) — redo Part 3 and check the repo is **Public**. |
| "It did something weird" | Describe exactly what you see to Claude — *"the dog is flying sideways"* is genuinely useful information. |
| Totally stuck / broken beyond repair | No such thing 🙂 Use **"Go back in time"** (above) to restore your last good version from GitHub. Worst case, make a fresh copy from the template (Part 2, 2 minutes) and paste in that good `main.js`. |

## FAQ

**Does this cost money?**
GitHub and GitHub Pages: free, forever, for public projects. claude.ai: has a
free plan (usage resets on a rolling few-hour window). Claude Pro (paid, about
$20/month) gives much higher limits and unlocks Claude Code — though even Pro has
usage caps over rolling and weekly windows, so very long sessions can still pause.

**Do we need to install anything?**
No. Path A is 100% browser tabs. Path B has a web version too.

**Can other people see our code?**
Yes — public repos are viewable by anyone (that's what makes hosting free).
Keep personal info out of the game (and see the Path B email note) and it's fine.

**Can we do this on a tablet or phone?**
The game *runs* on tablets — you can drag to look and pinch to zoom — but the
starter's movement is **keyboard-only** (arrow keys/WASD), so on a touch screen
you can't walk around yet. It's a one-prompt fix: ask Claude for *"an on-screen
joystick so I can move on a tablet or phone."* For *building*, use a computer —
some GitHub buttons hide on small screens.

**Can we build from a second computer** (the other parent's laptop, a library)?
Yes — Path A stores nothing on your machine, so any browser works after you sign
in to github.com and claude.ai. Heads up: GitHub emails a verification code when
you sign in on a new device, so the grown-up needs access to that email right
then.

**How do we find our game again tomorrow?**
Your two bookmarks: the **repo** (where you make changes) and the **game link**
(what you share). Lost them? Sign in at [github.com](https://github.com) — your
repos are listed on the left.

**Can two kids build together?**
Yes — take turns as the designer on one game, or create one repo per kid from
the template. Separate worlds, zero arguments. 😄

**What's next after the first few changes?**
Open the **[Prompt Idea Book](PROMPT-IDEAS.md)** — including the real, in-order
list of ideas that grew this starter into a full neighborhood game.

---

*Happy building! This template began as one family's weekend project — a whole
3D town grew out of the exact file you just published. Yours will grow into
something nobody's ever seen before.* 💎
