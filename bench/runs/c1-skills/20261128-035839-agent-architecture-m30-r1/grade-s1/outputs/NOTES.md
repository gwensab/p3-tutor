# Notes

## What Riley knows
- Python from classes: functions, lists and dicts, reading JSON, and calling a web API in one class project.
- Has used a chatbot for homework help and report drafts, and has noticed that it can state an outdated fact with confidence.
- A language model takes text in and writes text out, one token at a time, from patterns learned in training (learning record 0001).
- The agent loop at a high level: the model asks for an action, the action is carried out, the result comes back, and this repeats until it is done (learning record 0002).

## What Riley does not know yet
- Has never called a language model from code or written a tool definition.
- Has heard the words "token" and "context window" but cannot say what they limit or why they affect cost.
- Has not met memory, retrieval, workflows versus agents, or multi-agent systems.
- Has no machine-learning background beyond one statistics course.

## Working notes
- Quiz 0001 (the agent loop and tool calling) was taken twice: `submissions/s1.json` on the day of the agent-loop session, and `submissions/s2.json` four days later, from memory, as spaced practice.
  `s1` is graded (`grades/0001-s1.json`); `s2` has not been graded yet.
- On `s1`: q1 and q3 correct (the loop, step limits). M4 (model runs tools itself) showed in q2 and q4. M3 (memory across sessions is automatic) showed in an added claim in q6. q5 said what happens to a tool result but not why.
- To work on: label each step of a request "model" or "program" and count model calls; cover who saves information between sessions in the context and memory material.
- Next in the mission is context and memory, because the makerspace assistant has to answer from long machine manuals and remember each student's training status between visits.
