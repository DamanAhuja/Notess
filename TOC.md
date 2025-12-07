# ✅ **UNIT 1 – INTRODUCTION (7 Hours)**

**Alphabets, Strings, Languages, Operations on Languages, Concatenation, Union, Kleene Star**

This unit is the **foundation of the entire TOC subject**. Every future topic (FA, CFG, TM) is built on this.

---

## ✅ 1. Alphabet (Σ)

### 🔹 Definition:

An **alphabet** is a **finite, non-empty set of symbols**.

### 🔹 Examples:

| Alphabet        | Symbols            |
| --------------- | ------------------ |
| Σ = {0,1}       | Binary alphabet    |
| Σ = {a,b,c}     | Character alphabet |
| Σ = {x,y,z,1,2} | Mixed alphabet     |

✅ Alphabet is always **finite**
✅ Symbols are **atomic (cannot be broken further)**

---

## ✅ 2. String (w)

### 🔹 Definition:

A **string** is a **finite sequence of symbols** taken from an alphabet.

If Σ is an alphabet, then **any combination of symbols from Σ forms a string.**

### 🔹 Examples (Σ = {a, b}):

| String | Valid?               |
| ------ | -------------------- |
| ε      | ✅ Yes (empty string) |
| a      | ✅                    |
| ab     | ✅                    |
| bba    | ✅                    |
| abc    | ❌ (since c ∉ Σ)      |

---

### 🔹 Empty String (ε):

* A string with **zero symbols**
* Length of ε is **0**
* ε ≠ Ø (empty set)

---

### 🔹 Length of a String |w|

| String | Length |
| ------ | ------ |
| ε      | 0      |
| a      | 1      |
| ab     | 2      |
| aabb   | 4      |

---

### 🔹 Power of a String

| Expression | Meaning |
| ---------- | ------- |
| w⁰         | ε       |
| w¹         | w       |
| w²         | ww      |
| w³         | www     |

Example:
If w = ab
Then:

* w² = abab
* w³ = ababab

---

## ✅ 3. Language (L)

### 🔹 Definition:

A **language** is a **set of strings** formed using the symbols of a given alphabet.

Formally:

> If Σ is an alphabet, then any subset of Σ* is a language.

---

### 🔹 Σ* (Sigma Star)

Σ* is the **set of all possible strings** (including ε) that can be formed using Σ.

Example:
If Σ = {a, b}
Then:
Σ* = { ε, a, b, aa, ab, ba, bb, aaa, aab, ... }

✔ Infinite set
✔ Contains ε

---

### 🔹 Σ⁺ (Sigma Plus)

Σ⁺ = Σ* − {ε}
(All strings except empty string)

---

### 🔹 Examples of Languages:

| Language                                 | Description                     |
| ---------------------------------------- | ------------------------------- |
| L = {a, ab, abb}                         | Finite language                 |
| L = all strings over {0,1} ending with 1 | Infinite                        |
| L = Ø                                    | Empty language                  |
| L = {ε}                                  | Language with only empty string |

---

## ✅ 4. Types of Languages

| Type           | Meaning              |
| -------------- | -------------------- |
| Finite         | Limited strings      |
| Infinite       | Unlimited strings    |
| Empty (Ø)      | No strings           |
| Universal (Σ*) | All possible strings |

---

## ✅ 5. Basic Operations on Languages

Let L₁ and L₂ be two languages:

---

### ✅ (A) UNION (L₁ ∪ L₂)

All strings that are in **either L₁ or L₂**.

**Formula:**
L₁ ∪ L₂ = {w | w ∈ L₁ OR w ∈ L₂}

**Example:**
L₁ = {a, ab}
L₂ = {b, ba}

✅ L₁ ∪ L₂ = {a, ab, b, ba}

---

### ✅ (B) INTERSECTION (L₁ ∩ L₂)

Common strings in both languages.

L₁ = {a, b, ab}
L₂ = {b, ab, ba}

✅ L₁ ∩ L₂ = {b, ab}

---

### ✅ (C) DIFFERENCE (L₁ − L₂)

Strings in L₁ but **not** in L₂

✅ L₁ − L₂ = {a}

---

### ✅ (D) COMPLEMENT (L̅)

All strings in Σ* that are **not in L**

L = {a, ab}
Σ* = all strings over Σ

✅ L̅ = Σ* − L

---

## ✅ 6. Concatenation of Languages (L₁L₂)

### 🔹 Definition:

Concatenation means **joining every string of L₁ with every string of L₂**.

**Formula:**
L₁L₂ = {xy | x ∈ L₁ and y ∈ L₂}

---

### 🔹 Example:

L₁ = {a, b}
L₂ = {1, 2}

✅ L₁L₂ = {a1, a2, b1, b2}

---

### 🔹 Special Rules:

| Rule        | Result   |
| ----------- | -------- |
| Lε = εL = L | Identity |
| LØ = ØL = Ø | Zero     |

---

## ✅ 7. Kleene Star (L*)

### 🔹 Definition:

L* is the **set of all finite concatenations of strings from L**, including ε.

**Formula:**
L* = L⁰ ∪ L¹ ∪ L² ∪ L³ ∪ ...

---

### 🔹 Example:

If L = {a}

Then:
L* = {ε, a, aa, aaa, aaaa, ...}

---

### 🔹 Another Example:

If L = {ab}

L* = {ε, ab, abab, ababab, ...}

---

## ✅ 8. Kleene Plus (L⁺)

L⁺ = L* − {ε}

Means:

> One or more repetitions

If L = {x}

L⁺ = {x, xx, xxx, xxxx, ...}

---

## ✅ 9. Important Differences (EXAM CRITICAL)

| Feature | Σ        | Σ*          | L            |
| ------- | -------- | ----------- | ------------ |
| Meaning | Alphabet | All strings | Specific set |
| Finite? | ✅        | ❌ Infinite  | ✅ / ❌        |

---

## ✅ 10. Exam-Oriented Theoretical Questions

You should be able to answer:

✅ Define Alphabet
✅ Define String with example
✅ What is ε?
✅ Define Language
✅ Difference between Σ* and Σ⁺
✅ Define concatenation of two languages
✅ Explain Kleene Star with example
✅ What is empty language?
✅ Difference between Ø and {ε}

---

## ✅ 11. Numericals / Practice Examples

### Q1:

Σ = {0,1}
Write 5 strings of Σ* with length 3.

✅ Answer:
000, 001, 010, 011, 100

---

### Q2:

L = {a, b}
Find L² and L³

✅ L² = {aa, ab, ba, bb}
✅ L³ = {aaa, aab, aba, abb, baa, bab, bba, bbb}

---

### Q3:

L = {ab, ba}
Write L*

✅ {ε, ab, ba, abba, baab, ababab, ...}


# ✅ **UNIT 2 – FINITE AUTOMATA & REGULAR LANGUAGES (15 Hours)**

### **Topics Covered:**

1. Regular Expressions
2. Deterministic Finite Automata (DFA)
3. Non-Deterministic Finite Automata (NFA)
4. Relationship between NFA & DFA
5. Transition Graph (TG)
6. Properties of Regular Languages
7. Pumping Lemma for Regular Languages
8. Kleene’s Theorem
9. Relationship between Regular Languages & Finite Automata

---

# ✅ 1. REGULAR EXPRESSIONS (RE)

## 🔹 Definition:

A **Regular Expression** is a mathematical tool used to **describe regular languages** using symbols and operators.

---

## 🔹 Basic Rules of Regular Expressions

If **a ∈ Σ**, then:

| Expression | Meaning        |
| ---------- | -------------- |
| a          | Single symbol  |
| ε          | Empty string   |
| Ø          | Empty language |

---

## 🔹 Operators of Regular Expressions

| Operator      | Symbol | Meaning   |
| ------------- | ------ | --------- |
| Union         | + or ∪ | OR        |
| Concatenation | ·      | AND       |
| Kleene Star   | *      | 0 or more |

---

## 🔹 Precedence Order:

1. Star (*)
2. Concatenation
3. Union (+)

---

## ✅ Examples:

| Regular Expression | Language                |
| ------------------ | ----------------------- |
| a+b                | {a, b}                  |
| ab                 | {ab}                    |
| a*                 | {ε, a, aa, aaa, ...}    |
| (a+b)*             | All strings of a and b  |
| a*b                | {b, ab, aab, aaab, ...} |

---

## ✅ Some Important RE Patterns:

| Pattern   | Meaning                     |
| --------- | --------------------------- |
| (a+b)*    | All strings over {a,b}      |
| a(a+b)*   | All strings starting with a |
| (a+b)*b   | All strings ending with b   |
| (a+b)*abb | Strings ending with abb     |

---

# ✅ 2. DETERMINISTIC FINITE AUTOMATA (DFA)

## 🔹 Definition:

A **DFA** is a finite machine that **accepts or rejects strings** and has:

> Exactly **ONE transition** for every state and every input symbol.

---

## 🔹 Formal Definition of DFA:

A DFA is a 5-tuple:

**M = (Q, Σ, δ, q₀, F)**

| Symbol | Meaning                 |
| ------ | ----------------------- |
| Q      | Finite set of states    |
| Σ      | Input alphabet          |
| δ      | Transition function     |
| q₀     | Start state             |
| F      | Final (accepting) state |

---

## 🔹 Transition Function:

δ: Q × Σ → Q

Means:
For every state and every input symbol, **only ONE next state exists**.

---

## ✅ DFA Example:

Language: All strings over {0,1} ending with 1.

States:

* q₀ → start
* q₁ → final

Transitions:

| Current | Input | Next |
| ------- | ----- | ---- |
| q₀      | 0     | q₀   |
| q₀      | 1     | q₁   |
| q₁      | 0     | q₀   |
| q₁      | 1     | q₁   |

---

## ✅ Acceptance of String in DFA

A string is **accepted** if after processing all symbols, DFA reaches a **final state**.

---

# ✅ 3. NON-DETERMINISTIC FINITE AUTOMATA (NFA)

## 🔹 Definition:

An **NFA** allows:

* **Multiple transitions** for one input
* **ε-moves allowed** (move without input)

---

## 🔹 Formal Definition of NFA:

M = (Q, Σ, δ, q₀, F)

But:
δ: Q × Σ → 2^Q
(set of states)

---

## ✅ Key Difference: DFA vs NFA

| Feature              | DFA   | NFA   |
| -------------------- | ----- | ----- |
| Deterministic        | ✅ Yes | ❌ No  |
| ε-moves              | ❌ No  | ✅ Yes |
| Multiple transitions | ❌ No  | ✅ Yes |
| Power                | Same  | Same  |

✅ **DFA and NFA have equal computational power**

---

# ✅ 4. RELATIONSHIP BETWEEN NFA & DFA

### ✅ Important Result:

> **For every NFA, there exists an equivalent DFA.**

This is done using **Subset Construction Method**.

---

## ✅ Steps of NFA → DFA Conversion:

1. Start with ε-closure of start state
2. Create new DFA states as **sets of NFA states**
3. Repeat transitions using union rule
4. Any set containing a final state becomes a **final DFA state**

---

# ✅ 5. TRANSITION GRAPH (TG)

A **graphical representation** of finite automata:

* Nodes → States
* Edges → Transitions
* Initial State → Arrow
* Final State → Double circle

Used mainly for **visual understanding of FA**

---

# ✅ 6. REGULAR LANGUAGES

## 🔹 Definition:

A language is **Regular** if:

* It is accepted by a **Finite Automaton**
  OR
* It can be described using a **Regular Expression**

---

## ✅ Important Fact:

> Every language accepted by DFA/NFA is a **Regular Language**

---

# ✅ 7. PROPERTIES OF REGULAR LANGUAGES

Regular Languages are **closed under**:

| Operation     | Closed? |
| ------------- | ------- |
| Union         | ✅       |
| Intersection  | ✅       |
| Complement    | ✅       |
| Concatenation | ✅       |
| Kleene Star   | ✅       |
| Difference    | ✅       |
| Reversal      | ✅       |

---

# ✅ 8. PUMPING LEMMA FOR REGULAR LANGUAGES (VERY IMPORTANT)

## 🔹 Statement:

If **L is a regular language**, then there exists a number **p (pumping length)** such that:

Any string **w ∈ L**, with |w| ≥ p can be written as:

> **w = xyz**

Such that:

1. |xy| ≤ p
2. |y| > 0
3. For all i ≥ 0 → **xyⁱz ∈ L**

---

## ✅ Purpose of Pumping Lemma:

Used to **prove that a language is NOT regular**

---

## ✅ Steps to Apply Pumping Lemma:

1. Assume L is regular
2. Take pumping length p
3. Choose string w ∈ L with |w| ≥ p
4. Split as w = xyz
5. Pump y (remove or repeat)
6. If generated string ∉ L → **Contradiction → L is NOT regular**

---

## ✅ Example:

Prove L = {aⁿbⁿ | n ≥ 1} is NOT regular.

Take:
w = aᵖ bᵖ
Split xyz where y contains only a’s
Pump i = 0 → fewer a’s than b’s
So not in L ❌
Hence NOT regular ✅

---

# ✅ 9. KLEENE’S THEOREM (VERY IMPORTANT)

## 🔹 Statement:

> A language is **regular if and only if** it can be represented by a **finite automaton**.

That means:

* RE → FA ✅
* FA → RE ✅

---

## ✅ TWO PARTS:

| Direction | Proven By                |
| --------- | ------------------------ |
| RE → FA   | Thompson’s Construction  |
| FA → RE   | State Elimination Method |

---

# ✅ 10. RELATION BETWEEN REGULAR EXPRESSIONS & FINITE AUTOMATA

| Regular Expression | Equivalent Automaton |
| ------------------ | -------------------- |
| a                  | Single transition    |
| a+b                | Parallel paths       |
| ab                 | Series connection    |
| a*                 | Loop                 |

---

# ✅ 11. EXAM-ORIENTED QUESTIONS (VERY IMPORTANT)

✅ Define DFA & NFA
✅ Difference between DFA & NFA
✅ What is Regular Language?
✅ Define Pumping Lemma
✅ Purpose of Pumping Lemma
✅ State Kleene’s Theorem
✅ Closure properties of Regular Languages
✅ Convert RE → NFA
✅ Convert NFA → DFA
✅ Design DFA for given language

---

# ✅ 12. PRACTICE NUMERICAL QUESTIONS

### Q1:

Design DFA for:

> All strings over {0,1} that end with 01

---

### Q2:

Check if language using Pumping Lemma:
L = {aⁿbⁿ | n ≥ 1}

---

### Q3:

Find Regular Expression for:

> All strings starting with a and ending with b

---

# ✅ **UNIT 3 – CONTEXT FREE LANGUAGES (CFL)**

### **Topics Covered**

1. Context Free Grammar (CFG)
2. Deterministic & Non-Deterministic Pushdown Automata (PDA)
3. Relationship between CFG & PDA
4. Parse Trees
5. Leftmost & Rightmost Derivation
6. Ambiguity in Grammar
7. Pumping Lemma for CFL
8. Properties of CFL
9. Chomsky Normal Form (CNF)

---

# ✅ 1. CONTEXT FREE GRAMMAR (CFG)

## 🔹 Definition:

A **Context Free Grammar (CFG)** is a formal grammar that generates **Context Free Languages (CFL).**

A CFG is defined as a **4-tuple**:

> **G = (V, Σ, P, S)**

| Symbol | Meaning                          |
| ------ | -------------------------------- |
| V      | Set of non-terminals (variables) |
| Σ      | Set of terminals                 |
| P      | Set of production rules          |
| S      | Start symbol                     |

---

## 🔹 Production Rule Format:

> **A → α**

Where:

* A ∈ V (single non-terminal)
* α ∈ (V ∪ Σ)*

✅ Only **one non-terminal on LHS** → that is why it is called *Context Free*.

---

## 🔹 Example CFG:

Language: L = { aⁿbⁿ | n ≥ 1 }

Grammar:

```
S → aSb | ab
```

---

# ✅ 2. DERIVATIONS

## 🔹 (A) Leftmost Derivation (LMD)

Always replace the **leftmost non-terminal first**.

## 🔹 (B) Rightmost Derivation (RMD)

Always replace the **rightmost non-terminal first**.

---

### ✅ Example:

Grammar:

```
S → AB  
A → a  
B → b
```

Leftmost Derivation:

```
S ⇒ AB ⇒ aB ⇒ ab
```

Rightmost Derivation:

```
S ⇒ AB ⇒ Ab ⇒ ab
```

---

# ✅ 3. PARSE TREE

## 🔹 Definition:

A **parse tree** is a **hierarchical tree representation of derivation** of a string from a grammar.

### ✅ Properties:

* Root → Start symbol
* Internal nodes → Non-terminals
* Leaf nodes → Terminals
* Leaves read left to right give the string

---

# ✅ 4. AMBIGUOUS GRAMMAR

## 🔹 Definition:

A grammar is **ambiguous** if **one string has more than one parse tree OR more than one leftmost derivation.**

---

### ✅ Example of Ambiguous Grammar:

```
E → E + E | E * E | id
```

String:

```
id + id * id
```

Has **two different parse trees** → So ambiguous ✅

---

### ✅ Important Note:

> **Some CFLs are inherently ambiguous** (no unambiguous grammar exists).

---

# ✅ 5. PUSH DOWN AUTOMATA (PDA)

## 🔹 Definition:

A **Pushdown Automaton** is a finite automaton with an **extra stack memory**.

Used to accept **Context Free Languages**.

---

## 🔹 Formal Definition of PDA:

> **M = (Q, Σ, Γ, δ, q₀, Z₀, F)**

| Symbol | Meaning              |
| ------ | -------------------- |
| Q      | Set of states        |
| Σ      | Input alphabet       |
| Γ      | Stack alphabet       |
| δ      | Transition function  |
| q₀     | Start state          |
| Z₀     | Initial stack symbol |
| F      | Set of final states  |

---

## 🔹 PDA Transition Function:

> **δ: Q × (Σ ∪ ε) × Γ → 2^(Q×Γ*)**

---

# ✅ 6. TYPES OF PDA

| Type | Meaning               |
| ---- | --------------------- |
| DPDA | Deterministic PDA     |
| NPDA | Non-Deterministic PDA |

✅ **NPDA is more powerful than DPDA**
✅ Some CFLs cannot be accepted by DPDA

---

# ✅ 7. PDA ACCEPTANCE METHODS

| Method      | Meaning                      |
| ----------- | ---------------------------- |
| Final State | When PDA reaches final state |
| Empty Stack | When stack becomes empty     |

✅ Both methods are **equivalent in power**

---

# ✅ 8. RELATION BETWEEN CFG & PDA (VERY IMPORTANT)

### ✅ Theorem:

> A language is **Context Free if and only if** it is accepted by a **Pushdown Automaton**.

| Direction | Method                        |
| --------- | ----------------------------- |
| CFG → PDA | Standard construction         |
| PDA → CFG | Grammar construction from PDA |

---

# ✅ 9. PUMPING LEMMA FOR CONTEXT FREE LANGUAGES (VERY IMPORTANT)

## 🔹 Statement:

If **L is context free**, then there exists a number **p** such that any string
**w ∈ L with |w| ≥ p** can be written as:

> **w = uvxyz**

Such that:

1. |vxy| ≤ p
2. |vy| > 0
3. For all i ≥ 0 → **uvⁱx yⁱz ∈ L**

---

## ✅ Use:

Used to prove that a language is **NOT context free**.

---

### ✅ Example:

L = { aⁿbⁿcⁿ | n ≥ 1 }

Take:
w = aᵖ bᵖ cᵖ
After pumping → order breaks ❌
Hence **NOT CFL** ✅

---

# ✅ 10. CLOSURE PROPERTIES OF CFL

| Operation     | CFL Closed? |
| ------------- | ----------- |
| Union         | ✅           |
| Concatenation | ✅           |
| Kleene Star   | ✅           |
| Intersection  | ❌           |
| Complement    | ❌           |
| Difference    | ❌           |

---

# ✅ 11. CHOMSKY NORMAL FORM (CNF) – VERY IMPORTANT

## 🔹 Definition:

A CFG is in **Chomsky Normal Form** if all productions are of the form:

1. **A → BC**
2. **A → a**
3. **S → ε** (only if ε ∈ L)

Where:

* A, B, C are variables
* a is a terminal

---

## ✅ Steps to Convert CFG to CNF:

1. Remove **ε-productions**
2. Remove **unit productions**
3. Remove **useless symbols**
4. Convert RHS to proper binary format

---

# ✅ 12. EXAM-ORIENTED QUESTIONS (VERY IMPORTANT)

✅ Define CFG
✅ What is PDA?
✅ Difference between DFA & PDA
✅ Define Ambiguous Grammar
✅ What is Parse Tree?
✅ Define Pumping Lemma for CFL
✅ Properties of CFL
✅ Conversion of CFG to CNF
✅ CFG ↔ PDA Relation


# ✅ **UNIT 4 – TURING MACHINES & MODELS OF COMPUTATION**

### **Syllabus Coverage**

1. Turing Machine as a Model of Computation
2. Configuration of Turing Machine
3. Recursive Languages
4. Recursively Enumerable Languages
5. Church–Turing Thesis
6. Universal Turing Machine (UTM)
7. Decidability
8. Halting Problem

---

# ✅ 1. TURING MACHINE (TM)

## 🔹 Definition:

A **Turing Machine (TM)** is an **abstract mathematical model of computation** that can simulate **any algorithm**.

It is the **most powerful computational model** used to define what is *computable*.

---

## 🔹 Why Turing Machine is Important:

✅ Models real computers
✅ Basis of decidability theory
✅ Used to define **algorithmic limits**
✅ Foundation of **Computer Science**

---

## 🔹 Structure of a Turing Machine:

A Turing Machine consists of:

1. **Infinite Tape** (divided into cells)
2. **Read/Write Head**
3. **Finite Control (States)**

---

## 🔹 Formal Definition of TM:

A Turing Machine is a **7-tuple**:

> **M = (Q, Σ, Γ, δ, q₀, B, F)**

| Symbol | Meaning              |
| ------ | -------------------- |
| Q      | Finite set of states |
| Σ      | Input alphabet       |
| Γ      | Tape alphabet        |
| δ      | Transition function  |
| q₀     | Start state          |
| B      | Blank symbol         |
| F      | Set of final states  |

---

## 🔹 Transition Function of TM:

> **δ(q, a) = (p, b, D)**

Where:

* q = current state
* a = symbol read
* p = next state
* b = symbol written
* D = Head movement (L or R)

---

# ✅ 2. CONFIGURATION OF TURING MACHINE

## 🔹 Definition:

A **configuration** represents the **current status** of the TM during execution.

It includes:

* Current state
* Tape content
* Head position

---

### ✅ Notation:

If tape is: `001101` and head is on `1` in state `q`, then:

> **001 q 1 01**

---

### ✅ Initial Configuration:

Head at first symbol of input.

---

### ✅ Accepting Configuration:

If the TM reaches a **final state**, the input is **accepted**.

---

# ✅ 3. TYPES OF LANGUAGES BASED ON TM

---

## ✅ (A) RECURSIVE LANGUAGE

### 🔹 Definition:

A language **L is Recursive (Decidable)** if:

> There exists a Turing Machine which **accepts all strings of L and rejects all strings not in L**
> AND the TM **always halts**.

✅ TM stops for **every input**
✅ Membership problem is **decidable**

---

### ✅ Example:

* Palindrome checker
* Even number of 1s
* aⁿbⁿ language

---

## ✅ (B) RECURSIVELY ENUMERABLE (RE) LANGUAGE

### 🔹 Definition:

A language **L is Recursively Enumerable** if:

> There exists a Turing Machine which **accepts all strings in L**
> but **may not halt for strings not in L**.

✅ TM halts for **accepted strings only**
✅ TM may run **forever** on rejected strings

---

### ✅ Important Result:

> **Every Recursive Language is Recursively Enumerable**
> But
> **Not every RE Language is Recursive**

---

### ✅ Set Relationship:

```
Recursive ⊂ Recursively Enumerable ⊂ All Languages
```

---

# ✅ 4. DIFFERENCE BETWEEN RECURSIVE & RE LANGUAGES

| Feature                 | Recursive | Recursively Enumerable |
| ----------------------- | --------- | ---------------------- |
| TM Halts on every input | ✅ Yes     | ❌ No                   |
| Decidable               | ✅ Yes     | ❌ No                   |
| Always gives output     | ✅ Yes     | ❌ No                   |

---

# ✅ 5. CHURCH–TURING THESIS (VERY IMPORTANT)

## 🔹 Statement:

> **Any function that is computationally solvable by any real-world algorithm can be computed by a Turing Machine.**

---

## 🔹 Meaning:

* TM defines **exact meaning of algorithm**
* No machine can be **more powerful than a TM**

---

## ✅ Equivalent Computational Models:

All have **same power as TM**:

| Model               |
| ------------------- |
| Finite Automata     |
| Pushdown Automata   |
| Recursive Functions |
| Lambda Calculus     |
| Turing Machine      |

---

# ✅ 6. UNIVERSAL TURING MACHINE (UTM)

## 🔹 Definition:

A **Universal Turing Machine** is a TM that can **simulate any other Turing Machine** when given its description and input.

---

## 🔹 Working:

UTM takes:

* Description of another TM (⟨M⟩)
* Input string (w)

And simulates:

> **M(w)**

---

## ✅ Importance of UTM:

✅ Foundation of **modern computers**
✅ Concept of **stored program**
✅ One machine can perform **all computations**

---

# ✅ 7. DECIDABILITY

## 🔹 Definition:

A problem is **Decidable** if:

> A Turing Machine exists that **always halts** with a correct yes/no answer.

---

### ✅ Examples of Decidable Problems:

| Problem                   |
| ------------------------- |
| DFA acceptance            |
| CFG membership            |
| Regular language checking |

---

### ✅ Undecidable Problems:

| Problem         |
| --------------- |
| Halting problem |
| TM equivalence  |
| TM emptiness    |

---

# ✅ 8. HALTING PROBLEM (MOST IMPORTANT TOPIC)

## 🔹 Problem Statement:

> Given a Turing Machine **M** and input **w**, determine whether **M halts on w or runs forever**.

---

## ✅ Theorem:

> **Halting Problem is UNDECIDABLE.**

There exists **no Turing Machine** that can correctly solve this for all possible inputs.

---

## 🔹 Proof Idea (By Contradiction):

1. Assume Halting problem is decidable
2. Construct a machine that contradicts itself
3. Logical contradiction occurs
4. Hence, Halting problem is **undecidable**

---

## ✅ Consequences of Halting Problem:

✅ Some problems can **never be solved by any algorithm**
✅ There exist **limits to computation**

---

# ✅ 9. COMPARISON: DFA, PDA & TM

| Feature   | DFA     | PDA     | TM              |
| --------- | ------- | ------- | --------------- |
| Memory    | ❌ None  | ✅ Stack | ✅ Infinite Tape |
| Power     | Least   | Medium  | Maximum         |
| Languages | Regular | CFL     | Recursive & RE  |

---

# ✅ 10. EXAM-ORIENTED QUESTIONS (VERY IMPORTANT)

✅ Define Turing Machine
✅ Explain TM as a model of computation
✅ What is Configuration of TM?
✅ Define Recursive Language
✅ Define Recursively Enumerable Language
✅ Difference between Recursive & RE
✅ State Church–Turing Thesis
✅ Explain Universal Turing Machine
✅ What is Decidability?
✅ Explain Halting Problem with result

---
