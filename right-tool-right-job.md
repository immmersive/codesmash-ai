# Use the Right Tool for the Right Job

Since our goal is to be able to solve any problem, we should create a guiding principle which will always steer us in the right direction. The statement, which by definition does that, is the following one.

> _**Use the right tool for the right job**_

If we analyze this statement closer, we will notice that it is advising us to use certain tools, or methods to get the job done, i.e. solve a problem. But it is telling us to use the appropriate tools, i.e. appropriate methods to do so. The appropriate methods in question here, are by definition, the ones which will indeed get the job done,t hat is, solve teh problem. It should now be noted that if we actually know what those methods are and what the appropriate problems are, then if we stick to this statement while we are solving problems, then we can by definition solve any problem. The only thing that is now left for us to find out, are the following

- The correct tools (methods)
- The correct jobs (problem)
- The correct goal

So, by finding out which tool (method) works well on which job (solves a problem), we can always be sure that when we use them together, we will actually solve the problem. The only thing left for us to add here, is the goal. The statement actually implies that if you use the right tool for the right job, by definition you will reach your goal, meaning, you will get an appropriate result. This is clearly implied, even though it is not stated explicitly.


# Formalization

So, let us now start with formalizing this statement into an axiom. We shall follow this axiom while we are coming up with new ideas.
 
- Let $T(x)$ represent "Tool $x$ is the right tool for the job."

- Let $J(y)$ represent "Job $y$ is the right job."

- Let $R(x,y)$ represent "Using tool $x$ for job $y$ gives the right result."
 
We can now proceed to transform this statement into a tautology. We shall start with making sure that using the right tool for the right job, always implies that you get the correct outcome. Thus, we shall use the following statement.

> _**Use the right tool for the right job, and you will always get the right result.**_

Which we formalize as

```math
(T(x) ∧ J(y)) → R(x,y)
```

Where: 

- $T(x) ∧ J(y)$ means "Tool $x$ is the right tool and Job $y$ is the right job."
  
- $R(x,y)$ means "Using tool $x$ for job $y$ results in the right outcome."


To make this a **tautology**, we can define $R(x,y)$ in terms of $T(x)$ and $J(y)$. Specifically, we define $R(x,y)$ such that it **must** be true whenever $T(x)∧J(y)$ is true. This way, the statement becomes true by definition.

```math
R(x,y)⟺(T(x)∧J(y))
```

We now formalize the entire statement as a logical tautology:

```math
(T(x)∧J(y))→((T(x)∧J(y))→R(x,y))
```

This is a tautology because:

- The **implication** $(T(x)∧J(y))→R(x,y)$ is true by definition (as $R(x,y)$ is defined to be true whenever $T(x)∧J(y)$ is true).

- The overall statement $(T(x)∧J(y))→((T(x)∧J(y))→R(x,y))$ is always true because it formalizes the idea that using the right tool for the right job leads to the right result.

# Application of the Definition

Let us now assume that $P$ is a specific problem that needs to be solved. Then $T = \{T_1, T_2, \ldots, T_n\}$ is the set of all available tools which can be used to solve $P$. Furthermore, we can define $R_P$ as the set of constraints which limit us in how we can use the tools at our disposal in order to solve $P$. Now, we can define the function $E(T_i, P)$ as a measure, which represents the effectiveness of tool $T_i$ when applied to problem $P$. This function assesses how well the tool $T_i$ addresses the problem $P$, meeting the desired outcomes specified in $R_P$. It can consider factors like precision, accuracy, efficiency, and overall impact on solving $P$.

The function $C(T_i)$ is a measure representing the cost when using tool $T_i$ to solve $P$. This function measures the resources required to use $T_i$, which could include monetary cost, time, labor, or other resources. Lower costs are preferable for the same level of effectiveness. Lastly the function $S(T_i, P)$ is a suitability measure which tells us how appropriate is the tool $T_i$ for solving $P$, considering both effectiveness and cost. This ratio ensures that the selected tool not only meets the problem's requirements effectively but also does so in a resource-efficient manner. The tool with the highest score $S$ is considered the most suitable, as it offers the best trade-off between effectiveness and cost.

We can now define the suitability of a tool $T_i$ for a problem $P$, given the specific requirements $R_P$as:
```math
S(T_i, P) = \frac{E(T_i, P)}{C(T_i)}
```

We can then define how to choose the best tool $T^*$ when using the above Suitability function:
```math
T^* = \arg\max_{T_i \in T} S(T_i, P)
```

This means choosing the tool $T_i$ from the set $T$ that maximizes the suitability score $S(T_i, P)$ and we have chosen the right tool for the right job.
 
# Example

We are now going to show a simple example, where our goal is to perform a simple home improvement task, like nailing planks, which is a common task in carpentry.

Let $P$ be the problem of performing basic home improvement tasks. Let $T = \{ Hammer, Saw, Screwdriver \}$ be the set of tools available. Then we can measure **Effectiveness $E(T_i, P)$** and **Cost $C(T_i)$** for each tool as follows:
  
We can then calculate the effectiveness of each tool by using the **Effectiveness $E(T_i, P)$** function as follows:

$E(Hammer, P)$ = 10 for nailing, 0 for cutting, 0 for screwing.
  
$E(Saw, P)$ = 0 for nailing, 10 for cutting, 0 for screwing.
  
$E(Screwdriver, P)$ = 0 for nailing, 0 for cutting, 10 for screwing.

Furthermore, the **Cost $C(T_i)$** function then gives the the following for each tool:

$C(Hammer)$ = 2 

$C(Saw)$ = 5 

$C(Screwdriver)$ = 3 

Now that we have both the effectiveness and the cost of each tool, we can proceed with determining which tool is the right one for the job, meaning we are going to calculate each tool's **Suitability $S(T_i, P)$** score. We are going to measure the suitability of each tool, for each of the tasks we need to perform, so for the task of hammering we have the following scores.

- $S(\text{Hammer}, \text{nailing}) = \frac{10}{2} = 5$

- $S(\text{Saw}, \text{nailing}) = \frac{0}{5} = 0$

- $S(\text{Screwdriver}, \text{nailing}) = \frac{0}{3} = 0$
 

In the case of cutting task, the suitability score is as follows:


- $S(\text{Hammer}, \text{cutting}) = \frac{0}{2} = 0$

- $S(\text{Saw}, \text{cutting}) = \frac{10}{5} = 2$

- $S(\text{Screwdriver}, \text{cutting}) = \frac{0}{3} = 0$

In the case of driving screws, the suitability score is as follows:

- $S(\text{Hammer}, \text{screwing}) = \frac{0}{2} = 0$

- $S(\text{Saw}, \text{screwing}) = \frac{0}{5} = 0$

- $S(\text{Screwdriver}, \text{screwing}) = \frac{10}{3} \approx 3.33$

We can now conclude that for each task, the following tools are the best.

- **Nailing** - The hammer has the highest suitability score of 5.
  
- **Cutting** - The saw has the highest suitability score of 2.
  
- **Screwing** - The screwdriver has the highest suitability score of approximately 3.33. 

These calculations show how to quantitatively decide which tool is the most suitable for each specific task based on the concept of "using the right tool for the right job." Each tool's suitability is evaluated based on its effectiveness for the task relative to its cost, leading to the most efficient choice.
