To check the validity of the given formulas using sequent calculus, we need to perform a series of logical manipulations on each formula to determine if it is valid. I'll provide the proofs for each formula:

### Formula 1:
\[ \forall x. \exists y. p(x, y) \Rightarrow \exists x. p(x, a) \]

**Proof:**
1. \[ \forall x. \exists y. p(x, y) \Rightarrow \exists y. p(a, y) \] (Instantiate \(\forall\) with \(a\))
2. \[ \exists y. p(a, y) \Rightarrow p(a, a) \] (Instantiate \(\exists\) with \(a\))
3. \[ p(a, a) \] (Modus Ponens)
4. \[ \exists x. p(x, a) \] (Introduce \(\exists\))
5. \[ \forall x. \exists y. p(x, y) \Rightarrow \exists x. p(x, a) \] (Introduce \(\forall\))

The formula is valid.

### Formula 2:
\[ \exists x. (p(x) \Rightarrow q(x)) \land \exists x. p(x) \Rightarrow \exists x. q(x) \]

**Proof:**
1. \[ (p(a) \Rightarrow q(a)) \land \exists x. p(x) \Rightarrow \exists x. q(x) \] (Instantiate \(\exists\) with \(a\))
2. \[ p(a) \Rightarrow q(a) \] (Simplify)
3. \[ \exists x. p(x) \] (Instantiate \(\exists\) with \(a\))
4. \[ p(a) \] (Existential Elimination)
5. \[ q(a) \] (Modus Ponens)
6. \[ \exists x. q(x) \] (Existential Introduction)
7. \[ \exists x. (p(x) \Rightarrow q(x)) \land \exists x. p(x) \Rightarrow \exists x. q(x) \] (Existential Introduction)

The formula is valid.

### Formula 3:
\[ \forall x. (p(x) \land q(x)) \Rightarrow (\forall x. p(x) \land \forall x. q(x)) \]

**Proof:**
1. \[ p(a) \land q(a) \Rightarrow p(a) \] (Simplify)
2. \[ p(a) \land q(a) \Rightarrow q(a) \] (Simplify)
3. \[ \forall x. (p(x) \land q(x)) \Rightarrow (\forall x. p(x) \land \forall x. q(x)) \] (Introduce \(\forall\))

The formula is valid.

### Formula 4:
\[ \forall x. (p(x) \Rightarrow q(x)) \Rightarrow (\forall x. p(x) \Rightarrow \forall x. q(x)) \]

**Proof:**
1. \[ p(a) \Rightarrow q(a) \Rightarrow p(a) \Rightarrow \forall x. q(x) \] (Simplify)
2. \[ \forall x. (p(x) \Rightarrow q(x)) \Rightarrow (\forall x. p(x) \Rightarrow \forall x. q(x)) \] (Introduce \(\forall\))

The formula is valid.

All four formulas are valid based on the provided sequent calculus proofs.