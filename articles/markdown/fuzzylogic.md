# Fuzzy Logics

## Two values logics

### Basic logical operators

| $X$ | $Y$ | $X \land Y$ | $X \lor Y$ | $\lnot X$ |
|:---:|:---:|:-----------:|:----------:|:---------:|
| 1   | 1   | 1           | 1          | 0         |
| 1   | 0   | 0           | 1          | 0         |
| 0   | 1   | 0           | 1          | 1         |
| 0   | 0   | 0           | 0          | 1         |

> These are gruped because it is possible to generate all the relevent logic operators in Fuzzy Logic course

| $X$ | $Y$ | $X \implies Y$ | $X \iff Y$ | $X \uparrow Y$ | $X \downarrow Y$ |
|:---:|:---:|:--------------:|:----------:|:--------------:|:----------------:|
| 1   | 1   | 1              | 1          | 0              | 1                |
| 1   | 0   | 0              | 0          | 1              | 0                |
| 0   | 1   | 1              | 0          | 1              | 0                |
| 0   | 0   | 1              | 1          | 1              | 0                |

> $\uparrow$: NAND, $\downarrow$:NOR, These notations need tobe clearified before the exam

### Excercises

This section illustrate the format of the answer in which our professor expects his students to follow. Also outline some potential  tasks may appear in the exam

#### $(\alpha \vee \beta)\wedge \neg \beta$

Soltution:

- Step 1: Fill columns $\alpha, \beta $ with values

| $(\alpha$ | $\vee$ | $\beta)$ | $\wedge$ | $\neg$ | $\beta$ |
|:---------:|:------:|:--------:|:--------:|:------:|:-------:|
| 1         |        | 1        |          |        | 1       |
| 1         |        | 0        |          |        | 0       |
| 0         |        | 1        |          |        | 1       |
| 0         |        | 0        |          |        | 0       |

- Step 2:  Fill calculate the values for $\vee ,\neg$ 

| $(\alpha$ | $\vee$ | $\beta)$ | $\wedge$ | $\neg$ | $\beta$ |
|:---------:|:------:|:--------:|:--------:|:------:|:-------:|
| 1         | 1      | 1        |          | 0      | 1       |
| 1         | 1      | 0        |          | 1      | 0       |
| 0         | 1      | 1        |          | 0      | 1       |
| 0         | 0      | 0        |          | 1      | 0       |

- Step 3: Use values from step 2 to calculate column $\wedge$ . This is the final solution

| $(\alpha$ | $\vee$ | $\beta)$ | $\wedge$ | $\neg$ | $\beta$ |
|:---------:|:------:|:--------:|:--------:|:------:|:-------:|
| 1         | 1      | 1        | 0        | 0      | 1       |
| 1         | 1      | 0        | 1        | 1      | 0       |
| 0         | 1      | 1        | 0        | 0      | 1       |
| 0         | 0      | 0        | 0        | 1      | 0       |

#### Convert a logical statement

Since any logical statements can be represented as 3 logical operations $\vee, \wedge, \neg$ . It is possible to have task look like these:

1. Using only $\vee, \wedge, \neg$ rewrite these: $\alpha \implies \beta$, $\alpha \iff \beta$

2. Using only $NAND$ rewrite these: $\alpha \implies \beta$, $\alpha \iff \beta$

3. Similarly we have, use $NOR$ to rewrite these: $\alpha \implies \beta$, $\alpha \iff \beta$

>  Of course the logical statement can be different in the exam!!!

#### Proving Tautology

To prove a logical statement is a Tautology. We search for values that can give us $0$ for the logical statement.

##### Backward proving

>  `I don't have a clear way to explain this yet`

## Set

### Basic Set Operators

| Conjuntion                                        | Disjunsion                                        |
|:------------------------------------------------- | ------------------------------------------------- |
| $A \cap B = B \cap A$                             | $A \cup B = B \cup A$                             |
| $A \cap (B \cap C) = (A \cap B ) \cap C$          | $A \cup (B \cup C) = (A \cup B ) \cup C$          |
| $A \cap A = A$                                    | $A \cup A = A$                                    |
| $A \cap (A \cup B) = A$                           | $A \cup (A \cap B) = A$                           |
| $A \cap (B \cup C) = (A \cap B ) \cup (A \cap C)$ | $A \cup (B \cap C) = (A \cup B ) \cap (A \cup C)$ |
| $A \cap A' = \phi$                                | $A \cup A' =U$                                    |

> These are basic operators. In class, we assumed these are true and proceeded to prove all the operators in the next session. This type of exercise can appear in the exam.

### Derivatives from the basic operators

1. $A \subset B :\iff A \cap B =A$

2. $A \subset B :\iff A \cup B =B$

3. $A \cap U = A,\ A \cup U = U$

4. $A \cap \phi = \phi, \ A\cup\phi = A$

5. $A \setminus B \coloneqq A \cap B'$

6. $A \coloneqq A''$

7. $A \div B \coloneqq (A \setminus B) \cup (B \setminus A)$

8. $A \cap B = \phi \ \ \& \ \ A \cup B \iff A = B'$ 

9. $(A \subset B \wedge B \subset A) \iff A = B$

10. $A \cap B = \phi \ \ \& \ \ A \cup B = U \iff A = B'$

> $\phi$ : is empty set
> 
> $U$: is universal set, it contains all sets

`Todo: What the hell is number 7`

### Exercises

Typical excercises for here will be proving given statemets are correct using all the rules we have in the last session.

#### E1: $Prove: A \cap B = \phi \ \& \ A \cap B = U \iff A = B'$

Let: $A = B' \implies A \cap B = \phi \ (1) ,\ A \cap B = U \ (2)$

$(1):$

$$
A \cap B = \phi \\ 
A \cap B, \{A \backslash B'\} \\ 
B' \cap B \\ 
\phi \\ 
\implies A \cap B = \phi
$$

$(2):$

$$
A \cup B = U \\
A \cup B, \{ A \backslash B'\} \\
B \cup B \\
U\\
\implies A \cup B = U
$$

from $(1)$ and $(2)$ $\implies A \cap B = \phi \ \& \ A \cap B = U \iff A = B'$

> $\{ A \backslash B'\}$ is read "replace $A$ for $B'$"

#### E2: $Prove: (A \cap B)' = A' \cup B'$

$let: (A \cap B)' = A' \cup B' \implies A' \cap A = \phi,\ A' \cup A = U \\
then:$

$$
(A \cap B)'' = A \cap B \\\
(A \cap B) \cap (A' \cup B') = \phi \ (1) \\\
(A \cap B) \cup (A' \cup B') = U \ (2)
$$

$(1):$

$$
(A \cap B) \cap (A' \cup B') = \phi\\
(A \cap B) \cap (A' \cup B')\\
((A \cap B) \cap A') \cup ((A \cap B) \cap B')\\
((A \cap A') \cap B) \cup (A \cap (B \cap B'))\\
(\phi \cap B) \cup (A \cap \phi)\\
\phi \cup \phi\\
\phi\\
\implies (A \cap B) \cap (A' \cup B') = \phi
$$

$(2):$

$$
(A \cap B) \cup (A' \cup B') = U\\
(A \cap B) \cup (A' \cup B')\\
(A \cup (A' \cup B')) \cap (B \cup (A' \cup B'))\\
((A \cup A') \cup B') \cap (A' \cup(B' \cup B'))\\
(U \cup B') \cap (A' \cup U)\\
U \cap U\\
U\\
\implies (A \cap B) \cup (A' \cup B')  = U
$$

from $(1)$ and $(2)$ $\implies (A \cap B)' = A' \cup B'$

#### E3: $Prove: A \subset B \iff B' \subset A'$

`Todo:`

## Three values logic

Let **Unknown**, **True**, and **False** be denoted as $U$, $T$, and $F$, respectively, and let $\upsilon$ be a function that converts $U$, $T$, and $F$ to numeric values.

Then we have $\upsilon (U) = 0.5, \upsilon (T) = 1, \upsilon (F) = 0$ 

1. $\upsilon(p \wedge q) = \min \{ \upsilon(p),\upsilon(q)\}$

2. $\upsilon(p \vee q) = \max\{\upsilon(p),\upsilon(q)\}$

3. $\upsilon(\neg q) = 1 - \upsilon(q)$

4. $\upsilon(p \implies q) = \max\{1-\upsilon(q), \upsilon(p)\}$

5. $\upsilon(p \iff q) = \min \{ \max\{1 - \upsilon(q), \upsilon(p)\}, \max\{1 - \upsilon(p), \upsilon(q)\} \}$

> Notice: Equation 4 and 5 can have different forms 
> 
> * Łukasiewicz: When $\upsilon(U \implies U) = T$ , This is contradicted with the formulars 4 and 5. We just have to remember it
> 
> * Kleene: Follow 4 and 5
> 
> * Łukasiewicz often denotes as $Ł, {\implies}_Ł, {\iff}_Ł$ . Same goes for Kleene $K, {\implies}_K, {\iff}_K$

## Fuzzy logics

We were introduced to 3 fuzzy operations, each of them has 3 versions: Zadeh, Mengenhauser (Mengen), and Łukasiewicz

### T-norm

Co-norm is a different way to say $AND$ or $\wedge$ in FL.

1. ${T-norm}_Z : \min\{\upsilon (p),\upsilon(q)\}$

2. ${T-norm}_Z : \upsilon (p). \upsilon (q)$

3. ${T-norm}_Ł : \max\{0,\upsilon (p) + \upsilon(q) - 1\}$

### Co-norm

T-norm is $OR$ , $\vee$ version of FL. It also has 3 different version.

1. ${Co-norm}_Z: \max\{\upsilon(p),\upsilon(q) \}$

2. ${Co-norm}_M: \upsilon(p) + \upsilon(q) - \upsilon(p). \upsilon(q)$

3. ${Co-norm}_Ł : 1 - \max \{0, 1 - (\upsilon(p) + \upsilon(q))\}$

### Implication

1. ${\implies}_Z: \max\{1 - \upsilon(p),\upsilon(q) \}$

2. ${\implies}_M: \upsilon(p). \upsilon(q) + (1- \upsilon(q))$

3. ${\implies}_Ł : \min \{1, 1 + (\upsilon(q) - \upsilon(p))\}$

> Notice: In the 3rd equation, the positions of p and q are swapped.

### Complementation

For some reasons this was not explicitly introduced to us in class. complementation has only one form for all Zadeh, Mengen and Łukasiewicz:

Let $\alpha$ be a fuzzy value then $\alpha$ complement is: $\alpha^c = 1 - \upsilon(\alpha)$

### Exercises

| $\alpha$       | $(-2,0)$ | $(-1,0.3)$ | $(1,0.5)$ | $(0,1)$   | $(4,0)$   | $(3,0.7)$ | $(6,0.2)$ |
|:--------------:|:--------:|:----------:|:---------:|:---------:|:---------:|:---------:|:---------:|
| $\beta$        | $(-2,1)$ | $(-1,1)$   | $(1,0.8)$ | $(0,0.5)$ | $(4,0.1)$ | $(3,1)$   | $(6,001)$ |
| ${T-norm}_Z$   |          |            |           |           |           |           |           |
| ${T-norm}_M$   |          |            |           |           |           |           |           |
| ${T-norm}_Ł$   |          |            |           |           |           |           |           |
| ${Co-norm}_Z$  |          |            |           |           |           |           |           |
| ${Co-norm}_M$  |          |            |           |           |           |           |           |
| ${Co-norm}_Ł$  |          |            |           |           |           |           |           |
| ${\implies}_Z$ |          |            |           |           |           |           |           |
| ${\implies}_M$ |          |            |           |           |           |           |           |
| ${\implies}_Ł$ |          |            |           |           |           |           |           |

## Fuzzy relations

For intersection ($\cap$) and union ($\cup$) we will reuse the notion of $Co-norm$ and $T-norm$ respectively. We also introduced to subset.

### Intersection

Let $R,S \subset U, M_{R}(x,y), M_{r}(x,y) \in [0,1]$

1. $R \cup_{Z} S = \min \{ M_{R}(x,y), M_{S}(x,y) \}$
2. $R \cup_{M} S =  M_{R}(x,y).M_{S}(x,y)$
3. $R \cup_{Ł} S = \max \{0,M_{R}(x,y) + M_{S}(x,y) - 1\}$

### Union

1. $R \cap_{Z} S = \max \{ M_{R}(x,y), M_{S}(x,y) \}$
2. $R \cap_{M} S = (M_{R}(x,y)+M_{S}(x,y)) - M_{R}(x,y).M_{S}(x,y)$
3. $R \cap_{Ł} S = \max \{0,1 - (M_{R}(x,y) + M_{S}(x,y))\}$

### Complementation

${M_{R}(x,y)}^c  = 1 - M_{R}(x,y)$

### Subset

$R \subset S  = M_{R}(x,y) \le M_{S}(x,y)$

### Exercises

#### E1:

1. something

| $R$ | $a$ | $b$ | $c$ | $d$ |
|:---:|:---:|:---:|:---:|:---:|
| $a$ |     |     |     |     |
| $b$ |     |     |     |     |
| $c$ |     |     |     |     |
| $d$ |     |     |     |     |

| $S$ | $a$ | $b$ | $c$ | $d$ |
|:---:|:---:|:---:|:---:|:---:|
| $a$ |     |     |     |     |
| $b$ |     |     |     |     |
| $c$ |     |     |     |     |
| $d$ |     |     |     |     |

| $R {\cup}_M S$ | $a$ | $b$ | $c$ | $d$ |
|:--------------:|:---:|:---:|:---:|:---:|
| $a$            |     |     |     |     |
| $b$            |     |     |     |     |
| $c$            |     |     |     |     |
| $d$            |     |     |     |     |

# Disclaimer

For the same logic operator in Fuzzy, Binary, or Trinary, we were presented different formulas for them. This version of the cheat sheet is easier for me to remember, therefore I have it like this.
