# Superpowers workshop repository: design

## Purpose

A public repository to point participants at during a 90-minute workshop session. They install
Superpowers into their own Claude Code or Codex, get this repository onto their laptop, and use
Superpowers on one of two tasks. The point is to show what Superpowers adds over plain
prompting: it asks before it builds, it writes a spec and a plan you approve, and it checks its
own work.

Success: most people in the room have Superpowers installed and have been through at least the
brainstorm and spec stages on one task within about an hour of hands-on time.

## Audience

Mixed and semi-technical. Some write code, some do not. We cannot assume git, Node or Python are
installed, so the prompts have the agent check for them and install what is missing, after
asking. The READMEs say in plain words what the participant is about to see and what they are
being asked to decide.

## Layout

```
README.md
LICENSE                       MIT, for everything except movielens/
analytics/
  README.md
  TASKS.md
  movielens/                  MovieLens small dataset, with its own README.txt and LICENSE.txt
react-app/
  README.md
docs/superpowers/specs/       this file
```

## Top-level README

1. **What Superpowers is**, in three sentences.
2. **Step 1: install.** Superpowers installs as a plugin, through an action only the person can
   take, so this is steps rather than a prompt:
   - Claude Code: type `/plugin install superpowers@claude-plugins-official`, then start a new
     session.
   - Codex app: Plugins in the sidebar or in strip under the message box, find Superpowers under Coding, click `+`.
   - Codex CLI: `/plugins`, search `superpowers`, Install Plugin.

   Then a **check prompt** to paste into a new session, "Let's make a react todo list". A working
   install asks questions instead of writing code. Say what to do if it starts writing code.
3. **Step 2: get the workshop.** A prompt to paste. It asks the agent to:
   - ask where to put it, suggesting the Documents folder;
   - clone `https://github.com/presnick/superpowers-workshop`;
   - check for git, Node 20 or later, and Python 3 with pandas, and offer to install whatever is
     missing, asking before each install;
   - end by saying which folder to open for each task.

   No fork. Nobody needs to push, and Superpowers' local commits are enough.
4. **Step 3: pick a task**, a link to each folder and one line on each.
5. **A note on cost.** Superpowers can use a lot of a plan's usage. When it asks how to carry out
   the plan, choosing inline execution rather than subagents is the cheaper option.

## analytics/

`TASKS.md` gives PS1's three task statements verbatim:

- Task 1: the top 10 movies by average rating, among movies with at least 50 ratings.
- Task 2: the top 3 users by number of distinct genres rated, among users with 25 or fewer
  ratings.
- Task 3: the top 5 pairs by the naive overlap count, why that result may be uninteresting, and
  an alternative overlap measure compared against it.

`README.md` has:

- **The starter prompt:** "Use Superpowers to answer the three tasks in TASKS.md using the data in
  movielens/. I need to be confident the answers are right, not just to have answers."
- **What to watch for.** Brainstorming should raise decisions the task statements leave open:
  - how to break ties;
  - whether exactly 50 ratings counts;
  - how to count a movie that belongs to several genres;
  - what to do with `(no genres listed)`;
  - how to check the answers without trusting the code that produced them.

  If it does not ask, ask it.
- **The stretch prompt:** have a fresh session write an independent second version of Task 2 in
  another language, and a check that the two agree.

Left out from PS1:

- the `results.json` format;
- the report template;
- the second implementation as a requirement;
- `TEST-DATASETS.md`;
- the grading;
- the course's study questions.

## react-app/

`README.md` has:

- **The starter prompt:** the session 7 lab prompt. It changes only "in my assignments repository"
  to "in this folder":

  > Use Superpowers to design and build a React app in this folder. It tests whether someone knows
  > what YAGNI stands for (You Aren't Gonna Need It): the screen shows the letters; user types each
  > word. Start fresh after a reload.
  >
  > Discuss with me what to do for the following design elements:
  > - **Scaffolding.** What does the user get before they type?
  > - **Feedback.** What do they learn, and when?
  > - **Help.** Is there any, and what form does it take?
  > - **Scoring.** Is there scoring, and what is it?

- **What to watch for:**
  - Approve the spec only when it records a decision on each of the four elements.
  - It will offer a worktree, a plan, and a choice of how to carry out the plan.
  - When it says it is done, run the app and try it.
- **The stretch prompt:** the session 8 lab prompt, verbatim:

  > Use Superpowers to add a server and a database to my acronym app. I need an editor mode to
  > add, change and delete acronyms, and a learner mode that shows one acronym at a time and
  > checks what I type. My scores have to still be there after a reload.
  >
  > Server and DB local only. Any convenient DB is fine.

## What stays out

- Nothing from the private course repository.
- No references to Canvas, the course's AI gateway or the course's bootstrap: no pinned
  Superpowers clone, no `check-superpowers.mjs`, no `~/.codex/AGENTS.md`.
- Everything here is already public in the course's `assignments` repository or its published
  slides, adapted.

## Checking it

Before anything goes to GitHub:

- Paul reads the three READMEs.
- Links resolve.
- No em or en dashes.
- The MovieLens files match the public PS1 copy.

After pushing, one dry run of both prompts in a fresh session:

- the check prompt triggers brainstorming;
- the get-the-workshop prompt clones and reports correctly.
