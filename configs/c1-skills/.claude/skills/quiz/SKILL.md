---
name: quiz
description: Write a quiz and its answer key, or give a quiz to the learner in the chat - use it when the learner asks to be quizzed or tested. Not for grading a submission or answering questions about a topic.
argument-hint: "What should the quiz cover, and how many questions?"
---

# Quiz

You write a quiz that is easy to break down, mostly multiple choice, with its answer key.
Do the whole job yourself, in this conversation.

## The request

$ARGUMENTS

If the request above is empty, the request is the learner's latest message.

## Read first

Read `FORMATS.md`, `MISSION.md`, `PREFERENCES.md`, `NOTES.md`, the files in `learning-records/`, the lessons on the objective, and the earlier quizzes and keys.

## Pick what to test

1. Pin down the objective, its id and the number of items. With no number asked for, write five.
2. Find the objective's core in its lessons. With no lesson on it, search for a trusted source, read it, and say in your message that the quiz is ahead of the lessons.
3. Cover the core ideas first, one idea per item, and skip trivia.

## Item types

- Make at least two thirds of the items `mcq`: four of six, for example.
- Use `short` or `numeric` for the rest, where the learner should produce the idea or work out a quantity.
- Follow the request when it asks for something else.

## Easy to break down

- Give the situation first, in one or two short sentences, then ask one question on its own sentence.
- Keep a stem under about 60 words, in plain words, and define any term the learner has not met.
- Include every fact, number and unit the answer depends on, and nothing else.
- Say what a "best" or "most likely" choice is judged by.
- Avoid double negatives, "all of the above", "none of the above" and trick wording.
- Ask the learner to apply the idea to a new case more often than to recall a definition. Use a setting from the mission or `PREFERENCES.md` when it fits.

## Multiple-choice options

- Four options, ids `a` to `d`, each one short line.
- Give them similar length, grammar and detail, so the right one does not stand out or echo the stem.
- Build each wrong option on a real misconception or a typical error, reusing the workspace's misconception ids.
- Exactly one option is defensible. Vary the position of the correct one.

## Write the files

Write the quiz to `quizzes/NNNN.json` and the key to `keys/NNNN.json`, exactly as `FORMATS.md` shows, with the next number.
Never change an earlier quiz or key.

In the key, give each item a rationale of one or two sentences.
For a `short` item, ask for a word or a phrase, and list the other correct wordings in `accepted`.

## Check before you finish

Answer each item from its stem and options alone.
Rewrite any item where a second answer could be argued, where another item gives the answer away, or where the wording needs a second reading.

## Finish

Say in a few lines that the quiz is ready, with its path and what it covers. Never include an answer or a hint.

## Giving a quiz in the chat

Show the title and each item's stem and options, never anything from `keys/`.
When the learner has answered, record their answers exactly as given in the next `submissions/sN.json`, as `FORMATS.md` shows, then grade it with the grade skill (`/grade`).
