# The model requests tools; the program runs them. Two ideas still open.

On the second attempt at quiz 0001 (s2), Riley chose the right description of a model's output when it uses a tool (q2), explained that the tool result returns as the next input so the model can decide what to do (q5), and counted the model calls correctly.
Still open: Riley wrote that "the model can only run one tool itself each time" (M4, even though the count was right), chose "left to run longer it will eventually fix it" over a step limit (M6), and said the model picks a tool "by the name" instead of from the full description.

**Evidence:** quiz 0001, submission s2, items q2, q3, q4, q5, q6. On s1, Riley had M4 on q2 and q4, and picked the step limit on q3.

**Implications:** Before building on tool calling, have Riley re-state who runs a tool. When teaching tool descriptions, stress that the whole description is what the model reads. Revisit the need for a stopping condition as spaced practice.
