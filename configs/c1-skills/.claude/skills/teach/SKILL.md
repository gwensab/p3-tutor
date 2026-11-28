---
name: teach
description: Write the learner a lesson of the requested length as a self-contained HTML page with diagrams and check-your-understanding questions - use it when the learner asks for a lesson. Not for chat questions, quizzes or grading.
argument-hint: "What would you like a lesson on, and for how many minutes?"
---

# Teach

You write one lesson for this learner.
Do the whole job yourself, in this conversation.

## The request

$ARGUMENTS

If the request above is empty, the request is the learner's latest message.

A request that says what to teach gets done now, without stopping to ask first.
Put any question for the learner at the end of your final message.

## Read first

Read `FORMATS.md`, `MISSION.md`, `PREFERENCES.md`, `NOTES.md` and every file in `learning-records/`.
Then read `references/LESSONS.md` and `references/lesson-template.html`, the titles of earlier lessons, and whatever exists of `assets/`, `cheatsheets/`, `RESOURCES.md` and `GLOSSARY.md`.
The `references/` folder is `${CLAUDE_SKILL_DIR}/references/`.
Use Read, Glob and Grep to look around and Write to create files; no step needs the shell, so judge the length from your section plan.

## Every lesson has these

**Diagrams that explain.**
Draw two to four inline SVG figures, each where a picture shows a mechanism, process or comparison better than words.
Put each beside the text it explains, label its parts, and add a caption that says what to notice.

**Questions that check understanding during the lesson.**
End each main section with one or two questions on what it just taught, before the next section starts.
Ask the learner to apply the idea to a new case, and give immediate feedback: why the right answer is right and why each tempting wrong one is wrong.

**The requested length.**
Budget about 150 visible words per minute, split the budget across sections before writing, and write each section to its budget.

**Content that fits the objective.**
Cover each part of the objective, and stay on it.
Order the lesson from a concrete example to the general idea, one idea per section, at the learner's level.

## Steps

1. **Pin down the lesson:** the objective and its id, the length in minutes, where the learner starts, and what they will be able to do at the end. With no length asked for, use the one `PREFERENCES.md` implies, or 15 minutes.
2. **Find the knowledge:** search the web for trusted sources on exactly this objective, read the best two or three, and choose one as the primary source. Do not teach a fact from memory. Add the sources to `RESOURCES.md`, as `references/RESOURCES-FORMAT.md` describes.
3. **Plan:** list the sections with a word budget, a figure or none, and a check question for each.
4. **Write** the lesson to `lessons/NNNN-<slug>.html`, following `FORMATS.md`, `references/LESSONS.md` and the template.
5. **Check** it against "Every lesson has these" and the list at the end of `references/LESSONS.md`, and fix what fails.
6. **Keep the workspace current:** a cheat sheet in `cheatsheets/` when the lesson holds something worth looking up later, and `NOTES.md` for anything you learned about the learner. When they tell you what they already know, write a learning record (`references/LEARNING-RECORD-FORMAT.md`).

Do not write a quiz or a key; the quiz skill does that when the learner asks.
If `MISSION.md` is missing, teach the request first, then ask why they want to learn it and record the answer as `references/MISSION-FORMAT.md` describes.
`GLOSSARY.md`, once it exists, is the workspace's language (`references/GLOSSARY-FORMAT.md`).
Never edit `PREFERENCES.md`, `FORMATS.md` or anything under `.claude/`.

## Finish

Reply briefly: the lesson's path, what it covers, and that they can ask you about it or ask for a quiz.

---

Adapted from the `teach` skill in mattpocock/skills (MIT License, copyright (c) 2026 Matt Pocock); the full notice is in `THIRD-PARTY.md` at the root of the template repo.
