# Metrics

This insight connects the concept of structured creativity to Kolmogorov Complexity (KC) in a more nuanced way by considering the rarity of patterns in the search space. Patterns with low KC are rare and thus harder to discover or invent, even though they are simple to describe. This rarity makes them difficult to "stumble upon" in a large search space.

Let’s refine the metric to incorporate this idea:

## New Consideration: Rarity of Patterns in the Search Space

Low KC patterns are rare: In a large search space, patterns with low Kolmogorov Complexity (like "00000000") are rare, even though they are simple. This makes them harder to invent or discover.
High KC patterns are common: Patterns with higher KC, like random sequences, are more prevalent in the search space and easier to find by chance.

To account for this, we introduce a rarity factor R(Pi)R(Pi​) into the metric. This rarity factor reflects how likely or unlikely it is to find a pattern PiPi​ in the search space, based on its KC.


## Rarity Factor R(Pi)R(Pi​):

Patterns with low KC (e.g., 00000000) are rare, so R(Pi)R(Pi​) will be high.
Patterns with high KC (e.g., 01101001) are common, so R(Pi)R(Pi​) will be low.

## Incorporating Rarity into the Metric:

We update the metric to reflect the difficulty of discovering rare patterns:
D(O)=∑i=1nf(Pi)⋅(R(Pi)⋅K(Pi)⋅H(Pi)⋅T(Pi))+∑i=1n∑j=1nI(Pi,Pj)
D(O)=i=1∑n​f(Pi​)⋅(R(Pi​)⋅K(Pi​)⋅H(Pi​)⋅T(Pi​))+i=1∑n​j=1∑n​I(Pi​,Pj​)

Where:

- R(Pi)R(Pi​) is the rarity of pattern PiPi​ in the search space, which increases as KC decreases.
  
- K(Pi)K(Pi​) is the Kolmogorov complexity, which reflects the simplicity of the pattern.
  
- H(Pi)H(Pi​) is the Shannon information, representing the entropy or unpredictability of the pattern.
  
- T(Pi)T(Pi​) is the computational cost of constructing the pattern.
  
- f(Pi)f(Pi​) is the frequency or proportion of pattern PiPi​ in the object.
  
- I(Pi,Pj)I(Pi​,Pj​) represents interdependencies between patterns.

How Rarity Works:

Low KC, High Rarity: For a simple, structured pattern (like 00000000), even though its KC is low, its rarity in the search space is high because there are very few such patterns. This makes it harder to find or invent.
High KC, Low Rarity: For a more random pattern (like 01101001), the KC is higher, but the pattern is common in the search space. Therefore, it’s easier to find or invent, and its rarity factor R(Pi)R(Pi​) is low.

Adjusting the Balance:

The rarity factor modifies the metric to reflect that patterns with low KC, despite being simple, are hard to invent due to their scarcity in the search space. This accounts for the creative difficulty of finding simple but rare patterns.
Final Refined Metric:

```math
D(O)=∑i=1nf(Pi)⋅(R(Pi)⋅K(Pi)⋅H(Pi)⋅T(Pi))+∑i=1n∑j=1nI(Pi,Pj)
D(O)=i=1∑n​f(Pi​)⋅(R(Pi​)⋅K(Pi​)⋅H(Pi​)⋅T(Pi​))+i=1∑n​j=1∑n​I(Pi​,Pj​)
```

Low KC Patterns (e.g., a pencil): These have low KC but high rarity R(Pi)R(Pi​), making them harder to invent despite their simplicity.
High KC Patterns (e.g., a mess): These have high KC but low rarity R(Pi)R(Pi​), making them easier to discover in a random search, despite their complexity.

Practical Example:

Pencil (00000000):
K(Pencil)K(Pencil): Low KC (simple).
R(Pencil)R(Pencil): High (rare in the search space).
H(Pencil)H(Pencil): Low entropy (predictable).
T(Pencil)T(Pencil): Moderate computational cost.
The overall difficulty D(O)D(O) will be higher due to the high rarity R(Pencil)R(Pencil).

Mess (01101001):
K(Mess)K(Mess): High KC (complex).
R(Mess)R(Mess): Low (common in the search space).
H(Mess)H(Mess): High entropy (unpredictable).
T(Mess)T(Mess): Low computational cost.
The overall difficulty D(O)D(O) will be lower due to the low rarity R(Mess)R(Mess).

Summary:

The rarity factor now reflects the challenge of finding rare, low-KC patterns in a large search space, capturing the inventive difficulty of discovering something like a pencil (simple but rare).
This refinement balances the Kolmogorov Complexity, Shannon Information, Computational Complexity, and the new Rarity Factor to measure how hard it is to build something in a realistic 
