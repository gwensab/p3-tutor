# The loop is understood; two misconceptions remain, M4 and M6

On quiz 0001 (submission s2, from memory) Riley showed the loop structure: what makes an agent, that the model outputs a tool request, and that tool results go back as the next input.
Still open: M4, the model runs the tools itself, and M6, an agent left to run will eventually succeed without a stopping condition.
Riley also explained tool choice by the tool's name alone, not its full description.

**Evidence:** quiz 0001, s2: q1, q2 and q5 correct. q4 had the right count (4) with the reasoning "the model can only run one tool itself", showing M4. q3 chose "no change", showing M6. q6 answered "by the name", which is partial.

**Implications:** Before building on the loop, have Riley restate who does what at each step, the program or the model. Mention step limits again when cost comes up, since they also cap spending. Tool descriptions are worth teaching on their own, since Riley must write one for the makerspace tools.
