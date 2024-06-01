# Fuzzy Logics

## Two values logics

### Basic logical operators

| $X$ | $Y$ | $X \land Y$ | $X \lor Y$ | $\lnot X$ |
| --- | --- | ----------- | ---------- | --------- |
| 1   | 1   | 1           | 1          | 0         |
| 1   | 0   | 0           | 1          | 0         |
| 0   | 1   | 0           | 1          | 1         |
| 0   | 0   | 0           | 0          | 1         |

> These are gruped because it is possible to generate all the relevent logic operators in Fuzzy Logic course

| $X$ | $Y$ | $X \implies Y$ | $X \iff Y$ | $X\ NOR\ Y$ | $X\ AND\ Y$ |
| --- | --- | -------------- | ---------- | ----------- | ----------- |
| 1   | 1   | 1              | 1          | 0           | 1           |
| 1   | 0   | 0              | 0          | 1           | 0           |
| 0   | 1   | 1              | 0          | 1           | 0           |
| 0   | 0   | 1              | 1          | 1           | 0           |

> One thing still unclear for me is the notations for $NOR$ and $AND$ . In the class we have  $\uparrow$ and $|$ but I have no idea which on for which. Wikipedia conflicts with what I have in my notebook

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

### Derivertives from the basic operators

1. $A \sub B :\iff A \cap B =A$

2. $A \sub B :\iff A \cup B =B$

3. $A \cap U = A,\ A \cup U = U$

4. $A \cap \phi = \phi, \ A\cup\phi = A$

5. $A \setminus B \coloneqq A \cap B' $

6. $A \coloneqq A''$

7. $A \div B \coloneqq (A \setminus B) \cup (B \setminus A)$

8. $A \cap B = \phi \ \ \& \ \ A \cup B \iff A = B'$ 

9. $(A \sub B \wedge B \sub A) \iff A = B$

10. $A \cap B = \phi \ \ \& \ \ A \cup B = U \iff A = B'$

> $\phi$ : is empty set
> 
> $U$: is universal set, it contains all sets

## `Todo: What the hell is number 7`

## Three values logic

Let **Unknown**, **True**, and **False** be denoted as $U$, $T$, and $F$, respectively, and let $\upsilon$ be a function that converts $U$, $T$, and $F$ to numeric values.

Then we have $\upsilon (U) = 0.5, \upsilon (T) = 1, \upsilon (F) = 0$ 

1. $\upsilon(p \wedge q) = \min \{ \upsilon(p),\upsilon(q)\}$

2. $\upsilon(p \vee q) = \max\{\upsilon(p),\upsilon(q)\}$

3. $\upsilon(\neg q) = 1 - \upsilon(q)$

4. $\upsilon(p \implies q) = \max\{1-\upsilon(q), \upsilon(p)\}$

5. $\upsilon(p \iff q) = \min \{ \max\{1 - \upsilon(q), \upsilon(p)\}, \max\{1 - \upsilon(p), \upsilon(q)\} \}$

> Notice: Equation 4 and 5 have forms 
> 
> * Łukasiewicz: When $\upsilon(U \implies U) = T$ , This is contradicted with the formulars 4 and 5. We just have to remember it
> 
> * Kleene: Follow 4 and 5
> 
> * Łukasiewicz often denotes as $Ł, {\implies}_Ł, {\iff}_Ł$ . Same goes for Kleene $K, {\implies}_K, {\iff}_K$



## Fuzzy logics

We were introduced to 3 fuzzy operations, each of them has 3 versions: Zadeh, Mengenhauser (Mengen), and Łukasiewicz

### T-norm

Co-norm is a different way to say $OR$ or $\vee$ in FL.

1. ${T-norm}_Z : \min\{\upsilon (p),\upsilon(q)\}$

2. ${T-norm}_Z : \upsilon (p). \upsilon (q)$

3. ${T-norm}_Ł : \max\{0,\upsilon (p) + \upsilon(q) - 1\}$



### Co-norm

T-norm is $AND$ , $\wedge$ version of FL. It also has 3 different version.

1. ${Co-norm}_Z: \max\{\upsilon(p),\upsilon(q) \}$

2. ${Co-norm}_M: \upsilon(p) + \upsilon(q) - \upsilon(p). \upsilon(q)$

3. ${Co-norm}_Ł : 1 - \max \{0, 1 - (\upsilon(p) + \upsilon(q))\}$

### Implication

1. ${\implies}_Z: \max\{1 - \upsilon(p),\upsilon(q) \}$

2. ${\implies}_M: \upsilon(p). \upsilon(q) + (1- \upsilon(q))$

3. ${\implies}_Ł : \min \{1, 1 + (\upsilon(q) - \upsilon(p))\}$

> Notice: In the 3rd equation, the positions of p and q are swapped.

# My bias

For the same logic operator in Fuzzy, Binary, or Trinary, we were presented different formulas for them. This version of the cheat sheet is easier for me to remember, therefore I have it like this.
