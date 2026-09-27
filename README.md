# Superpowers workshop

<img src="qr-code.png" alt="QR code linking to github.com/presnick/superpowers-workshop" width="280">

Scan to open this page, or go to **github.com/presnick/superpowers-workshop**.

Superpowers is a free plugin for AI coding agents such as Claude Code and Codex. It changes how
the agent works: before it builds anything, it asks you questions, writes a short spec for you to
approve, and turns that into a step-by-step plan. While it builds, it tests and checks its own
work instead of just telling you it is finished.

In this workshop you install Superpowers, put this repository on your laptop, and try it on one
of two tasks. You need Claude Code or Codex already installed and signed in.

## Step 1: install Superpowers

Pick the one you use.

- **Claude Code:** type this into a session and press Enter, then quit and start a new session:

  ```
  /plugin install superpowers@claude-plugins-official
  ```

- **Codex app:** open Plugins (in the sidebar, or in the strip under the message box), find
  Superpowers and add it.
- **Codex CLI:** type `/plugins`, search for `superpowers`, and choose Install Plugin.

### Check that it worked

Start a **new** session and paste this:

```
Let's make a react todo list
```

If Superpowers is working, the agent does **not** start writing code. It says it is using a
brainstorming skill and asks you a question about what you want. That is the sign it worked.
You can stop there; you do not need to build the todo list.

If instead it starts creating files or writing code, stop it (press Esc), check that the plugin
shows as installed and enabled, then quit completely and start a new session. Plugins only load
when a session starts. If it still writes code straight away, ask a facilitator.

## Step 2: get the workshop onto your laptop

Start a new session and paste this prompt. The agent will ask you before it installs anything.

```
Please set up the files for a workshop on this computer. This is a setup job, not a
design task, so there is no need to brainstorm.

1. Ask me where to put the workshop folder. Suggest my Documents folder.
2. Check whether git is installed. If it is not, tell me and ask me before installing it.
3. Clone https://github.com/presnick/superpowers-workshop into the place I chose.
4. Check whether Node.js version 20 or later is installed, and whether Python 3 with the
   pandas library is installed. For each one that is missing or too old, tell me what it is
   for and ask me before installing it. Ask about each one separately.
5. When you are done, tell me the full path of the analytics folder and of the react-app
   folder inside the workshop, and tell me to open one of them in a new session. Do not
   start either task yourself.
```

You do not need a GitHub account for this. You will not push anything back; Superpowers saves
its work as commits on your laptop, which is all you need.

## Step 3: pick a task

Open the folder for your task in a **new** session. In the Claude or Codex desktop app, choose
that folder as the project. In a terminal, `cd` into the folder and start `claude` or `codex`
there. Then follow that folder's README.

- [**analytics/**](analytics/README.md): answer three questions about a dataset of movie
  ratings, and find out how Superpowers helps you trust the answers. Good if you work with data.
- [**react-app/**](react-app/README.md): design and build a small web quiz app, making the design
  decisions yourself. Good if you want to see it build software.

## A note on cost

Superpowers can use a lot of your plan's usage, because it does more checking than plain
prompting. When it asks how you want it to carry out the plan, choosing to do it **inline** (in
this session) rather than with **subagents** is the cheaper option, but slower.
