# Analytics task: movie ratings

You will ask the agent to answer three questions about MovieLens, a public dataset of about
100,000 movie ratings. The questions are in [TASKS.md](TASKS.md) and the data is in
[movielens/](movielens/). You do not need to write any code yourself. Your job is to make the
decisions the questions leave open, and to decide whether you believe the answers.

Make sure this `analytics` folder is the one your session is working in.

## The starter prompt

Paste this into a new session:

```
Use Superpowers to answer the three tasks in TASKS.md using the data in movielens/. I need to be
confident the answers are right, not just to have answers.
```

## What you will see

1. **Questions, one at a time.** This is the brainstorming stage. Answer in your own words. It is
   fine to say "I don't know, what would you suggest?"
2. **A spec to approve.** It writes up what it understood and asks you to review it. Read it. If
   something is wrong or missing, say so and it will revise.
3. **A plan, and a choice of how to carry it out.** Inline (in this session) is the cheaper
   choice.
4. **The work itself**, with tests, and then the answers.

## What to watch for

The task statements leave real decisions open. A good brainstorm should raise them:

- how to break ties;
- whether a movie with exactly 50 ratings counts;
- how to count a movie that belongs to several genres;
- what to do with movies whose genre is `(no genres listed)`;
- how to check the answers without just trusting the code that produced them.

If it does not ask about one of these, ask it yourself. Then look at the spec: are your decisions
written down there?

## The stretch prompt

If you finish early, start a **new** session in this same folder and paste this. A second version
written without seeing the first is a strong check: if the two disagree, one of them is wrong.

```
Use Superpowers to write a second, independent version of Task 2 from TASKS.md, in a different
programming language from the existing version. Do not look at the existing code. Then write a
check that runs both versions on the data in movielens/ and says whether they give the same
answer, and what differs if they do not.
```
