# Reviews: c1-skills

Your quick rounds while you build `c1-skills`, and then its major review, once you have snapshotted it and made its full run.
In this step no round adds a subagent, because subagents arrive in `c2-review` and `c3-split`: a round changes or adds a skill, or makes another change the skills need, such as an allow rule (Kind `other`).
Your first round can start from the tutor as it ships, so the baseline is the output without your first change.
The major review covers all four jobs, and its previous step is `c0-baseline`, so compare with your baseline runs.
What it finds becomes the checklists of your reviewer subagents in `c2-review`, so be specific.
`reviews/README.md` says how to write each part.
A rating on every criterion and What the next step should fix make the major review complete; the lines under each rating, Live tries and Compared with the previous step are optional, and you may leave their markers as they are.
You write your thoughts, ratings and feedback; Claude Code writes only the What changed part of each round.
Keep every heading as it is, because `p3 check` reads them, and add a round by copying the last one with its marker lines.

## Quick rounds

### Round 1

**Run:** bench/runs/_live/20261124-052048-agent-architecture-m30-r1, an --only run of tutor-p01 and tutor-p02

**My thoughts:**

This version is a bit to verbose, i would perfer more straight to the point responses. and when the tutor cannot explicitly answer the question, I would rather it tell me where to look or help me walk through a different example that has the same concept. 

**What changed:**

- Kind: new skill
- Files: tutor/.claude/skills/tutor/SKILL.md, tutor/CLAUDE.md
- Why: Chat questions ran inside /teach; a tutor skill of its own keeps replies under 150 words and, when it cannot answer, says where to look or walks through a different example of the same concept, as these thoughts ask, and tutor/CLAUDE.md now sends questions to it.

### Round 2

**Run:** bench/runs/_live/20261124-233958-agent-architecture-m30-r1, an --only run of the quiz and the two tutor probes

**My thoughts:**

These examples are better and easier to understand. The length of reply is also better. I also like how there is a suggestion of how to apply the example to the actual question. The quiz is easy to break down and i like the use of  multiple choice questions.

**What changed:**

- Kind: new skill
- Files: tutor/.claude/skills/quiz/SKILL.md, tutor/CLAUDE.md
- Why: Quizzes were still written inside /teach; a quiz skill of its own makes the qualities these thoughts liked into rules, with at least two thirds multiple choice and stems that are easy to break down, and tutor/CLAUDE.md now sends quiz requests to it.

### Round 3

**Run:**   bench/runs/_live/20261128-013555-agent-architecture-m30-r1, an --only run of the quiz and grade-s1

**My thoughts:**

The grading is good, the summary of feedback is nice to know what to focus on reviewing. Explanations for correct answers are a bit to long, they can be shorter. Answers marked wrong and partial should have slightly longer explanations about why.

**What changed:**

- Kind: new skill
- Files: tutor/.claude/skills/grade/SKILL.md, tutor/CLAUDE.md, tutor/.claude/skills/quiz/SKILL.md
- Why: Grading still ran inside /teach with one length for all feedback; a grade skill of its own keeps correct answers to one or two sentences, explains wrong and partial answers at more length with the reason why, and keeps the review summary, as these thoughts ask.

### Round 4

**Run:**   bench/runs/_live/20261128-015248-agent-architecture-m30-r1, an --only run of teach and grade-s1

**My thoughts:**

I liked the diagrams used for explanation. The lengths and content were also good. I liked the quiz questions to check understanding during the lesson. These things should be kept for teach. teach should be responsible for doing whats described above.

**What changed:**

- Kind: modified skill
- Files: tutor/.claude/skills/teach/SKILL.md, tutor/.claude/skills/teach/references/LESSONS.md, tutor/.claude/skills/teach/references/lesson-template.html, tutor/.claude/skills/teach/references/QUIZZES.md (removed), tutor/.claude/skills/teach/references/GRADING.md (removed), tutor/.claude/skills/teach/references/TUTORING.md (removed)
- Why: These thoughts ask teach to be responsible for the diagrams, lengths, content and in-lesson quiz questions they liked, so teach now only writes lessons and requires explaining diagrams, check questions with feedback in each section, the requested length and content that fits the objective.


## Major review

**Run:**   bench/runs/c1-skills/20261128-035839-agent-architecture-m30-r1

**Live tries:**

TODO

### Lesson

#### Technical correctness and facts

Rating: 5

#### Pedagogy

Rating: 5

#### Alignment with the learning goal

Rating: 5

#### Overall quality

Rating: 5

### Quiz

#### Difficulty

Rating: 5

#### Coverage of the lesson's core

Rating: 4

The questions cover the points of the lesson well but could have a more widespread coverage of topics.

#### Wording and possible misreadings

Rating: 5

Wording made sense.

#### Writing quality

Rating: 5

#### Alignment with the learning goal

Rating: 5

### Feedback

#### Useful

Rating: 5

#### Explains enough

Rating: 4

Occasionally too verbose with explanations.

#### Personalized to how I like things explained

Rating: 5

### Tutor

#### Guardrails

Rating: 5

Adequately avoids giving away answers in a polite manner.

#### Personalization

Rating: 5

Uses good examples relevant to my own experience.

### Compared with the previous step

TODO (optional)

### What the next step should fix

Make sure feedback is not too wordy, responses should be thorough yet consise. Like the response to s1 q4 is long and hard to read. Instead of using the code syntax in the answer, simplify it while still getting the point across. There should be about one question on each of the sections in the lesson on the quiz to avoid trivial questions.
