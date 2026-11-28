# Riley can say what a tool call is and where the result goes, but two ideas are still shaky

On the second attempt at quiz 0001, Riley correctly said the model outputs a tool request rather than running the tool (q2), and that the result goes back as the next input so the model can decide its next step (q5).
Still open: M4 (the model runs the tools itself) returned in the reasoning for q4, even with the right count; M6 (an agent left to run longer will get there, so it needs no stopping condition) in q3; and Riley named only the tool's name, not its description, in q6.
The next lessons should state plainly that the program runs the tools and that every loop needs a stopping condition, and should cover tool descriptions.

**Evidence:** quiz 0001, submission s2, items q2, q3, q4, q5 and q6. The first attempt (s1) had M4 on q2 and q4, which makes q2 an improvement.
