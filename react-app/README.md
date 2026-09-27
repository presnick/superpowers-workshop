# React app task: an acronym quiz

You will ask the agent to design and build a small web app that tests whether someone knows what
an acronym stands for. The app does not exist yet; this folder is where it will be built. You do
not need to write any code yourself. Your job is to make the design decisions.

Make sure this `react-app` folder is the one your session is working in.

## The starter prompt

Paste this into a new session:

```
Use Superpowers to design and build a React app in this folder. It tests whether someone knows
what YAGNI stands for (You Aren't Gonna Need It): the screen shows the letters; user types each
word. Start fresh after a reload.

Discuss with me what to do for the following design elements:
- **Scaffolding.** What does the user get before they type?
- **Feedback.** What do they learn, and when?
- **Help.** Is there any, and what form does it take?
- **Scoring.** Is there scoring, and what is it?
```

## What you will see

1. **Questions, one at a time.** This is the brainstorming stage. It may offer to show you
   mockups in a browser. Answer in your own words; it is fine to say "what would you suggest?"
2. **A spec to approve.** Approve it only when it records a decision on each of the four design
   elements: scaffolding, feedback, help and scoring. If one is missing, say so.
3. **An offer of a worktree.** This is a separate copy of the folder for the new work, so nothing
   else gets disturbed. Either answer is fine.
4. **A plan, and a choice of how to carry it out.** Inline (in this session) is the cheaper
   choice.
5. **The work itself**, with tests.

When it says it is done, run the app and try it. If it has not told you how, ask it: "How do I
run the app?" Does it do what the spec says?

## The stretch prompt

If you finish early, paste this into the same session:

```
Use Superpowers to add a server and a database to my acronym app. I need an editor mode to
add, change and delete acronyms, and a learner mode that shows one acronym at a time and
checks what I type. My scores have to still be there after a reload.

Server and DB local only. Any convenient DB is fine.
```
