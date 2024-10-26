# The Pragmatic Maxim

The **Pragmatic Maxim** originally suggested that the meaning of a concept or idea lies in its practical effects and consequences. According to Charles Sanders Peirce, one of the founders of Pragmatism, the meaning of a concept can be understood by considering what practical effects the object of the concept might have and how those effects could potentially influence our experiences. The statement was defined as follows.

> Consider what effects, that might conceivably have practical bearings, we conceive the object of our conception to have. Then, our conception of these effects is the whole of our conception of the object. 

We can see that, as we have said previously, the ideas that we have about any object in question, is only what we have experienced with respect to that object. Since we concluded that we never have full information at hand, and can never confirm absolute truth, then this definition clearly tells us that we are working with objects based on incomplete information. This is in line with our conclusion that we should make decision based on the best available knowledge, which is - the inference to the bext explanation. Note, making a decision on the best available knowledge is also in live with our main Axiom because we are using the best tool (knowledge) for the job (giving an explanation).

With respect to ideas in general, which is what we are ultimately dealing with, in our problem solving approach, we shall redefine the Pragmatic Maxim as follows.

> Ideas should be evaluated based on how useful they are with respect to the goal we are trying to achieve.

This definition tells us several things. Ideas are what we are evaluating while solving problems. Since everything starts from ideas, this is the most encompassing approach possible. When we are evaluating ideas, we should do it with respect to the goal we are tryign to achieve. This is in line with our main Axiom because it is telling us to use the best idea for the job at hand, which in general is the goal we are trying to achieve.

# Formal Definition

We can start by defining the variables in question.

- **$I_i$:** Represents the $i$-th idea or concept.
- **$G$:** Represents the goal or objective that you are trying to achieve.
- **$U(I_i, G)$:** Represents the utility function, which measures how useful idea $I_i$ is with respect to the goal $G$.
- **$S(I_i)$:** Represents the score or effectiveness of idea $I_i$ in solving the problem.

We can then define teh **Utility function** $U(I_i, G)$ as follows.

```math
U(I_i, G) = \frac{O(I_i, G)}{C(I_i)}
```

Where:

- **$O(I_i, G)$:** Represents the outcome or result produced by idea $I_i$ with respect to the goal $G$. This could be measured in terms of effectiveness, success rate, or some other metric related to the goal.

- **$C(I_i)$:** Represents the cost or resources required to implement idea $I_i$, such as time, energy, money, etc.
 
We then take into account the optimization condition. The goal is to find the idea $I^*$ that maximizes the utility function:

```math
I^* = \arg\max_{I_i} U(I_i, G)
```

This equation means that the optimal idea $I^*$ is the one that maximizes the utility with respect to the goal $G$. Furthermore, given our new theory of truth, we can represent the "truth" $T$ as the optimal solution $I^*$:

```math
T = I^*
```

Thus, the "truth" is defined as the idea $I^*$ that maximizes the utility function, i.e., the idea that is most useful and effective in achieving the goal $G$. If we consider this as a problem-solving framework, the process can be represented as follows.

```math
T = \arg\max_{I_i} \frac{O(I_i, G)}{C(I_i)}
```

Where the "truth" $T$ is the idea $I^*$ that provides the highest utility in achieving the goal $G$, taking into account both the outcome and the cost. This formalization captures the essence of your new pragmatic maxim by expressing the evaluation of ideas in terms of maximizing their practical utility relative to a specific goal. The optimal solution, which solves the problem most effectively, is equated with the "truth" in this framework.
 
