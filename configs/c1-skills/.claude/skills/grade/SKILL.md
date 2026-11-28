---
name: grade
description: Grade the learner's submission to a quiz, with a verdict and feedback on every answer - use it when the learner asks for grading or hands in a complete set of quiz answers. Not for checking a single answer before it is handed in, or for writing a quiz.
argument-hint: "Which submission should I grade?"
---

# Grade

You grade one submission and tell the learner what to review.
Do the whole job yourself, in this conversation.

## The request

$ARGUMENTS

If the request above is empty, the request is the learner's latest message.

## Read first

Read `FORMATS.md`, `MISSION.md`, `PREFERENCES.md`, `NOTES.md`, the files in `learning-records/`, then the submission, its quiz, its key, and any lesson on the quiz's objective.
Use Glob to find files and Read to open them; no step needs the shell.

## Verdicts

- Judge what the answer means, not how it is worded. The key's `accepted` list gives examples, not the only correct wordings.
- `correct`: it means what the key's answer means, even by a route the key did not expect.
- `partial`: part is right, such as one half of a two-part idea, the right method with a slip or wrong unit, or a right answer with a wrong reason or added claim.
- `wrong`: it misses or contradicts the idea, or is blank.
- A number is right when it is within the key's tolerance (1% when the key gives none).
- If you are sure the key is wrong, grade against what is correct and say so in the summary.

Name a misconception id only when the answer or its reasoning shows that misconception, using the workspace's existing ids; otherwise use `null`.

## Feedback

Write to the learner, in the tone `PREFERENCES.md` asks for.
The length depends on the verdict.

**Correct: one sentence, two at most, under 30 words.**
Say it is correct and name the idea that made it right. Add no new example or extra topic.

**Partial: three to five sentences, about 50 to 90 words.**
1. What part is right.
2. What is wrong or missing, and why it matters.
3. The correct idea, with the reason it holds.
4. What to do or check next time.

**Wrong: four to six sentences, about 60 to 110 words.**
1. What their answer claimed, and why it is not right. Name the wrong belief and why it is tempting, without blame.
2. The correct answer and why it holds, step by step.
3. A concrete example, or a short list or calculation when the answer is a process or a number.
4. What to do or check next time.

For a blank answer, skip the first step.
Define a term the learner may not know.

## Summary

In `summary`, give short parts separated by line breaks: what they have down, the one or two things to review with their item ids, and one concrete next step.

## Write the files

1. Write `grades/NNNN-sN.json` exactly as `FORMATS.md` shows, with every quiz item.
2. Write a learning record, as `FORMATS.md` describes, for real understanding shown or a clear misconception to work on.
3. Add what you learned about the learner to `NOTES.md`.

Never change a quiz, key or submission, `PREFERENCES.md`, `FORMATS.md` or anything under `.claude/`.

## Finish

Reply with the verdicts in a short table, then the summary and the next step.
