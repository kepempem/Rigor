A set is a collection of objects (the members of the set) satisfying a certain set of axioms. The statement $x \in y$ means that $x$ is a member of the set $y$.

## Formal Language

The formal language used here is composed of formulas and is called the formal language of ZF.
If a formula $\phi$ depends on some variable $u$, one may write $\phi\left(u\right)$.
Statements of the form $x \in y$ are formulas.
Given formulas $\phi$ and $\psi$ the following are also formulas:

* $\lnot \phi$
* $\phi \land \psi$
* $\phi \lor \psi$
* $\phi \Longrightarrow \psi$
* $\phi \iff \psi$
* $\forall v: \phi$
* $\exists v: \phi$


A variable $v$ used in some formula $\phi$ is called bound in $\phi$ if a string of the form $\forall v \left(\psi\right)$ or $\exists v \left(\psi\right)$ appears within $\phi$ (Where $\psi$ is a formula). If a variable is not bound in $\phi$, then it is called free in $\phi$. A formula with no free variables is called a sentence.


## Notation
A set with members $a,b,c, \cdots$ can be denoted $\left\\{a,b,c,\cdots\right\\}$. For example, a set whose only members are $x$ and $y$ can be denoted $\left\\{x,y\right\\}$.

### Abbreviations

| Abbreviation                           | Equivalent                                                   | Notes                                                  |
| -------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------ |
| $x \subseteq y$                        | $\forall z \left( z \in x \Longrightarrow z \in y \right)$   | If $x \subseteq y$ then $x$ is called a subset of $y$. |
| $\forall x \in X : \phi\left(x\right)$ | $\forall x \left( x \in X \Longrightarrow \phi\left(x\right) \right)$ |                                                        |
| $\exists x \in X : \phi\left(x\right)$ | $\exists x \left( x \in X \land \phi\left(x\right) \right)$  |                                                        |


## ZF Axioms

The Zermelo-Fraenkel axioms are listed below.

### Axiom Of Extensionality

The axiom of extensionality states that two sets are equal if and only if they have exactly the same members.


$$
\forall x \forall y \left( x = y \iff \forall z \left( z \in x \iff z \in y \right) \right)
$$


### Empty Set Axiom

The empty set axiom states that there is an empty set (denoted $\emptyset$).


$$
\exists \emptyset \forall x \left( \lnot \left(x \in \emptyset\right) \right)
$$


#### Uniqueness Of Empty Set
There is exactly one empty set.

In order to prove this, one may assume that both $\emptyset$ and $\Omega$ are empty sets. That is: $\forall x\left( \lnot \left(x \in \emptyset\right) \right)$ and $\forall x\left( \lnot \left(x \in \Omega\right) \right)$. Hence, the statement $\forall z \left( z \in \emptyset \iff z \in \Omega \right)$ is vacuously true and thus, by the axiom of extensionality, $\emptyset = \Omega$. $\blacksquare$

### Axiom Of Regularity
The axiom of regularity (Also known as the axiom of foundation) states that any non-empty set $x$ contains a member $y$ such that $x$ and $y$ have no shared members.


$$
\forall x \left( \left( \exists a\left(a \in x\right) \right) \Longrightarrow \exists y \left( y \in x \land \lnot \left( \exists z \left( z \in x \land z \in y \right) \right) \right)\right)
$$


### Axiom Schema Of Specification
The axiom of specification states that for any set $x$, there is a set $y$ such that the members of $y$ are exactly those members of $x$ that satisfy a formula.

Let $\phi\left(u,p\right)$ be a formula.
Then:


$$
\forall x \forall p \exists y \forall u \left( u \in y \iff \left[ u \in x \land \phi\left(u, p\right) \right] \right)
$$


#### Set Builder Notation
By using the axiom schema of specification, given a set $x$ and a formula $\phi\left(u,p\right)$, one may construct a set consisting of all the members of $x$ that satisfy $\phi$ and denote it $\left\\{ u \in x \; : \; \phi\left(u,p\right) \right\\}$.

That is:

$$
\forall v\left( v \in \left\\{ u \in x \; : \; \phi\left(u,p\right) \right\\} \iff \left( v \in x \land \phi\left(v,p\right) \right) \right)
$$


In addition, by letting $\phi\left( u \right)$ be a formula, the following holds:


$$
\forall x \left[ \left( \forall u \left( \phi\left(u,p\right) \Longrightarrow u \in x \right) \right) \Longrightarrow \left( \forall y \left( y \in \left\\{ u \in x : \phi\left(u,p\right) \right\\} \iff \phi\left( y,p \right) \right) \right) \right]
$$


In order to prove this, one may let $x$ be a set and $\phi\left(u,p\right)$ be a formula such that $\forall u \left( \phi\left(u,p\right) \Longrightarrow u \in x \right)$.

Firstly, one may assume that $y$ is a set such that $y \in \left\\{ u \in x : \phi\left(u,p\right) \right\\}$. Hence: $y \in x \land \phi\left(y, p\right)$ and thus: $\phi\left(y, p\right)$ holds.

One may then assume that $y$ is a set such that $\phi\left(y,p\right)$ holds. Hence: $y \in x$ which implies that $y \in x \land \phi\left(y,p\right)$. This is equivalent to $y \in \left\\{ u \in x : \phi\left(u,p\right) \right\\}$.


#### Nonexistence Of The Set Of All Sets
The following holds:


$$
 \not\exists \mathbb{U} \left( \forall x \left( x \in \mathbb{U} \right) \right)
$$


In order to prove this, one may assume that $\exists \mathbb{U} \left( \forall x \left( x \in \mathbb{U} \right) \right)$.
Hence, by the axiom schema of specification, one may define a set as follows: $S = \left\\{ x \in \mathbb{U} : x \not\in x \right\\}$. $S$ is a set and thus: $S \in \mathbb{U}$. Therefore: $S \in S \veebar S \not\in S$. If $S \in S$ then, by definition of $S$: $S \not\in S$, a contradiction. If $S \not\in S$ then, by definition of $S$: $S \in S$, also a contradiction. Since each of these leads to a contradiction, $\mathbb{U}$ must not be a set. $\blacksquare$

This is known as *Russell's paradox*.

### Axiom Of Pairing
The axiom of pairing states that for any two sets $x$ and $y$, there is a set $z$ such that the members of $z$ are $x$ and $y$ and only them. In other words, for any two sets $x$ and $y$, the set $\left\\{x,y\right\\}$ exists.


$$
\forall x \forall y \exists z \forall u \left( u \in z \iff \left( u = x \lor u = y \right) \right)
$$


#### Uniqueness Of Pair
Let $x$ and $y$ be sets and assume that $z$ is a set such that $\forall u \left( u \in z \iff \left( u = x \lor u = y \right) \right)$ and $z^\ast$ is a set such that $\forall u \left( u \in z^\ast \iff \left( u = x \lor u = y \right) \right)$.

Hence:


$$
\begin{split}
    \forall u ( u \in z \iff & u = x \lor u = y \\
    \iff & u \in z^\ast )
\end{split}
$$


And thus, by the axiom of extensionality: $z = z^\ast$.

#### Existence Of Singleton
For any set $x$, the set $\left\\{ x \right\\}$ that contains $x$ and only $x$ exists.

One may prove this by using the axiom of pairing and the axiom of extensionality.

Firstly, by the axiom of pairing, for any set $x$, the set $\left\\{x, x\right\\}$ exists. Hence:


$$
\begin{split}
    \forall x \forall u ( u \in \left\\{x, x\right\\} \iff & \left( u = x \lor u = x \right) \\
    \iff & u = x )
\end{split}
$$


Hence, the only member of $\left\\{x, x\right\\}$ is $x$. Which implies that the set for any $x$, the set $\left\\{ x \right\\}$ exists and $\left\\{ x,x \right\\} = \left\\{ x \right\\}$.

### Axiom of Union

The axiom of union states that for any set $x$,
there is a set $y$ which is the union of the members of $x$.


$$
 \forall x \exists y \forall u \left( u \in y \iff \left( \exists z \left(z \in x \land u \in z\right) \right) \right)
$$


#### Notation Of Union
The union of all members of a set $x$ is denoted $\displaystyle \bigcup \, x$.
That is:


$$
\forall x\forall u\left( u \in \bigcup \, x \iff \exists z \left( z \in x \land u \in z \right) \right)
$$


#### Union Of Sets
Given two sets $x$ and $y$, one may use the axiom of pairing and observe that the set $\left\\{x, y\right\\}$ exists and thus, by the axiom of union, the union of $x$ and $y$ exists. Hence, one may let:


$$
\forall x \forall y \left( x \cup y := \bigcup \left\\{ x,y \right\\} \right)
$$


Hence:


$$
\begin{split}
    \forall x \forall y \forall u ( u \in x \cup y \iff & \exists z \left( z \in \left\\{x,y\right\\} \land u \in z \right) \\
    \iff & \exists z \left( \left(z = x \lor z = y\right) \land u \in z \right) \\
    \iff & u \in x \lor u \in y )
\end{split}
$$


### Axiom Schema Of Replacement

Let $\phi\left(x,y,p\right)$ be a formula.
Then:


$$
\begin{split}
    & \left[ \forall x \forall y \forall z \left( \left( \phi\left(x,y,p\right) \land \phi\left(x,z,p\right) \right) \Longrightarrow y = z \right) \right]
    \\ & \Longrightarrow \forall X \exists Y \forall y \left(y \in Y \iff \exists x \left(x \in X \land \phi\left(x,y,p\right)\right)\right)
\end{split}
$$


That is, if $\phi$ defines a unique $x$-to-$y$ correspondence (a function) then given a set $X$, all $y$ that $\phi$-correspond to some $x$ in $X$ form a new set.

### Axiom Of Infinity
The axiom of infinity states the following:


$$
\exists x \left( \emptyset \in x \land \forall y \left( y \in x \Longrightarrow y \cup \left\\{ y \right\\} \in x \right) \right)
$$


### Power Set Axiom
The power set axiom states that for any set $x$, a set of all its subsets (also called its power set) exists.


$$
\forall x \exists P \forall y \left( y \in P \iff \forall z \left( z \in y \Longrightarrow z \in x \right) \right)
$$


#### Uniqueness Of Power Set
A power set of a set $x$ is unique. Let $x$ be a set and assume that $P$ is a set such that $\forall y \left( y \in P \iff y \subseteq x \right)$ and that $P^\ast$ is a set such that $\forall y \left( y \in P^\ast \iff y \subseteq x \right)$.

Then:

$$
\begin{split}
    \forall y ( y \in P \iff & y \subseteq x \\
    \iff & y \in P^\ast )
\end{split}
$$



Hence, by the axiom of extensionality: $P = P^\ast$ and thus, the power set of $x$ is unique. $\blacksquare$

One may use this axiom and for any set $x$, denote its power set $\mathcal{P}\left(x\right)$.
Hence, with this notation the axiom becomes:


$$
\forall x \exists \mathcal{P}\left(x\right) \forall y \left( y \in \mathcal{P}\left(x\right) \iff y \subseteq x \right)
$$



## Basic Properties

### x ∉ x
The following holds:


$$
\not\exists x \left(
        x \in x
    \right)
$$


In order to prove this, one may let $x$ be a set. Therefore, the set $\left\\{x\right\\}$ exists
and by the axiom of regularity: $\exists y \left( y \in \left\\{x\right\\} \land \not\exists z \left( z \in \left\\{x\right\\} \land z \in y \right) \right)$. Thus, by definition of a singleton: $y = x$ which implies: $\not\exists z \left( z = x \land z \in x \right)$. $\blacksquare$

### {x,y} = {z} ⇒ x = y = z
The following holds:


$$
 \forall x \forall y \forall z \left( \left\\{ x,y \right\\} = \left\\{ a \right\\} \Longrightarrow x = y = a \right)
$$


In order to prove this, one may let $x$, $y$, and $z$ be sets such that $\left\\{ x,y \right\\} = \left\\{ a \right\\}$.
Hence, by the axiom of extensionality:


$$
\begin{split}
    & \forall u ( u \in \left\\{ x, y \right\\} \iff u \in \left\\{ z \right\\} \\
    \Rightarrow & \forall u \left( \left(u = x \lor u = y\right) \iff u = z \right)
\end{split}
$$


Hence, since this is valid for all $u$, then the following holds:
* $\left[ u = x \Longrightarrow u = z \right] \Longrightarrow x = z$
* $\left[ u = y \Longrightarrow u = z \right] \Longrightarrow y = z$

And thus: $x = z = y$. $\blacksquare$

### x ⊆ y ⇒ ⋃ x ⊆ ⋃ y
The following holds:


$$
\forall x \forall y \left( x \subseteq y \Longrightarrow \bigcup x \subseteq \bigcup y \right)
$$


In order to prove this, one may let $x$ and $y$ be sets such that $x \subseteq y$.
Then:


$$
\forall z \left( z \in x \Longrightarrow z \in y \right)
$$


In addition:


$$
\forall z \left( z \in \bigcup x \iff \exists u \left( u \in x \land z \in u \right) \right)
$$


Hence:


$$
\begin{split}
    \forall z ( z \in \bigcup x \iff & \exists u \left( u \in x \land z \in u \right) \\
    \Longrightarrow & \exists u \left( u \in y \land z \in u \right) \\
    \iff & z \in \bigcup y )
\end{split}
$$


Therefore, the condition holds. $\blacksquare$

## Intersection Of Sets
The intersection of two sets $x$ and $y$ is defined as follows:


$$
\forall x \forall y \left( x \cap y := \left\\{ u \in x \cup y \; : \; u \in x \land u \in y \right\\} \right)
$$


In addition, the intersection of all members of a set $x$, denoted $\displaystyle \cap \, x$ and sometimes called the intersection of $x$ is defined as:


$$
\forall x \left( \cap \, x := \left\\{ u \in \cup \, x \, : \, \forall y \left( y \in x \Longrightarrow u \in y \right) \right\\} \right)
$$


Furthermore, the following holds:


$$
\forall x \forall y \forall z \left( z \in x \cap y \iff z \in x \land z \in y \right)
$$


In order to prove this, one may first assume that $x$, $y$, and $z$ are sets such that $z \in x \cap y$. Then, by definition of intersection: $z \in x \land z \in y$.

One may then assume that $x$, $y$, and $z$ are sets such that $z \in x \land z \in y$. Hence, by definition of union: $z \in x \cup y$ which implies that $z \in x \cap y$. Therefore, the condition holds. $\blacksquare$


### x ⋂ y = Ø
The following holds:


$$
\forall x \forall y \left( x \cap y = \emptyset \iff \lnot \left( \exists z \left( z \in x \land z \in y \right) \right) \right)
$$


In order to prove this, one may first let $x$ and $y$ be sets such that $x \cap y = \emptyset$. Assume that $\exists z \left( z \in x \land z \in y \right)$. Then $z \in x \cap y = \emptyset$ which is a contradiction.

One may then let $x$ and $y$ be sets such that $\lnot\left( \exists z \left( z \in x \land z \in y \right) \right)$. Hence: $\lnot\left( \exists z \left( z \in x \cap y \right) \right)$ which implies that $x \cap y = \emptyset$. $\blacksquare$


## Complement
Given two sets $x$ and $y$, the complement of $y$ in $x$, denoted $x \setminus y$ is defined as follows:


$$
\forall x \forall y \left( x \setminus y := \left\\{ u \in x \; : \; \lnot\left( u \in y \right) \right\\} \right)
$$


## Ordered Pairs

Let $x$ and $y$ be sets, then by the axiom of pairing, the set $\left\\{x, y\right\\}$
exists and the set $\left\\{x\right\\}$ exists. Hence, also by the axiom of pairing,
the set $\left\\{ \left\\{x\right\\}, \left\\{x, y\right\\} \right\\}$ exists.
One may then define an ordered pair $\langle x,y \rangle$ as follows:


$$
\forall x \forall y \left( \; \langle x,y \rangle := \left\\{ \left\\{x\right\\}, \left\\{x, y\right\\} \right\\} \; \right)
$$


In an ordered pair $\langle x, y \rangle$, $x$ is called the first coordinate and $y$ is called the second coordinate.

#### The Characteristic Property Of Ordered Pairs

The following holds:


$$
\forall x \forall y \forall a \forall b \left( \langle x, y \rangle = \langle a, b \rangle \iff x = a \land y = b \right)
$$


In order to prove this, one may first assume that $x$, $y$, $a$, and $b$ are sets such that $\langle x, y \rangle = \langle a, b \rangle$.


One of two cases must then be true:
* If $x = y$ then:
  
  $$
	\begin{split}
		\langle x, y \rangle &= \left\\{ \left\\{x\right\\}, \left\\{x,y\right\\} \right\\} \\
		&= \left\\{ \left\\{x\right\\}, \left\\{x,x\right\\} \right\\} \\
		&= \left\\{ \left\\{x\right\\}, \left\\{x\right\\} \right\\} \\
		&= \left\\{ \left\\{x\right\\} \right\\} \\
	\end{split}
  $$
  
  And thus:
  
  $$
	\begin{split}
		& \left\\{ \left\\{a\right\\}, \left\\{a,b\right\\} \right\\} = \left\\{ \left\\{x\right\\} \right\\} \\
		\Rightarrow & \left\\{a\right\\} = \left\\{a,b\right\\} = \left\\{x\right\\} \\
        \Rightarrow & \left[a = x\right] \land \left[a = b\right] \\
        \Rightarrow & \left[x = a\right] \land \left[x = b\right] \\
		\Rightarrow & \left[x = a\right] \land \left[y = b\right] \\
	\end{split}
  $$


* If $\lnot \left( x = y \right)$ then $\left\\{ \left\\{x\right\\}, \left\\{x,y\right\\} \right\\} = \left\\{ \left\\{a\right\\}, \left\\{a,b\right\\} \right\\}$. Assume that $\left\\{a,b\right\\} = \left\\{x\right\\}$, then $a = b = x$ which implies $\left\\{ \left\\{a\right\\}, \left\\{a,b\right\\} \right\\} = \left\\{ \left\\{x\right\\}, \left\\{x,x\right\\} \right\\} = \left\\{ \left\\{x\right\\} \right\\}$ and thus: $\left\\{ \left\\{x\right\\}, \left\\{x,y\right\\} \right\\} = \left\\{ \left\\{x\right\\} \right\\}$ which implies $x = y$, a contradiction to $\lnot \left( x = y \right)$. Assume that $\left\\{x,y\right\\} = \left\\{a\right\\}$, then $x = y = a$ which also contradicts $\lnot \left(x = y\right)$. Hence: $\left[ \left\\{x\right\\} = \left\\{a\right\\} \Rightarrow x = a \right] \land \left\\{x,y\right\\} = \left\\{a,b\right\\} = \left\\{x,b\right\\}$. If $b = x$ then $\left\\{x,y\right\\} = \left\\{x, b\right\\} = \left\\{x, x\right\\} = \left\\{x\right\\}$ which implies $x = y$, a contradiction. Hence: $b = y$, as desired.

Thus: $\forall x \forall y \forall a \forall b \left( \langle x, y \rangle = \langle a, b \rangle \Longrightarrow x = a \land y = b \right)$.

One may then assume that $x$, $y$, $a$, and $b$ are sets such that $x = a \land y = b$. Hence:

$$
\begin{split}
    \langle x, y \rangle &= \left\\{ \left\\{x\right\\}, \left\\{x,y\right\\} \right\\} \\
    &= \left\\{ \left\\{a\right\\}, \left\\{a,b\right\\} \right\\} \\
    &= \langle a, b \rangle
\end{split}
$$

And thus, the condition holds. $\blacksquare$

## Cartesian Products

One may observe the following:


$$
\begin{split}
    \forall X \forall Y \forall x \forall y ( x \in X \land y \in Y \Longrightarrow & \, \left\\{ x \right\\} \subseteq X \cup Y \land \left\\{x,y\right\\} \subseteq X \cup Y \\
    \Longrightarrow & \, \left\\{ x \right\\} \in \mathcal{P}\left(X \cup Y \right) \land \left\\{x,y\right\\} \in \mathcal{P}\left(X \cup Y \right) \\
    \Longrightarrow & \, \left\\{ \left\\{ x \right\\}, \left\\{x,y\right\\} \right\\} \subseteq \mathcal{P}\left(X \cup Y \right) \\
    \Longrightarrow & \, \left\\{ \left\\{ x \right\\}, \left\\{x,y\right\\} \right\\} \in \mathcal{P}\left( \mathcal{P}\left(X \cup Y \right) \right) \\
    \Longrightarrow & \, \langle x, y \rangle \in \mathcal{P}\left( \mathcal{P}\left(X \cup Y \right) \right) )
\end{split}
$$




Hence, given two sets $X$ and $Y$, one may use the axiom schema of specification and define the Cartesian Product of $X$ and $Y$, denoted $X \times Y$, as the set of all ordered pairs whose first coordinate is a member of $X$ and whose second coordinate is a member of $Y$.


$$
\forall X \forall Y \left( X \times Y := \left\\{ u \in \mathcal{P}\left( \mathcal{P}\left(X \cup Y \right) \right) \; : \; \exists x \exists y \left( x \in X \land y \in Y \land u = \langle x, y \rangle \right) \right\\} \right)
$$


In addition, the following holds:


$$
\forall X \forall Y \forall x \forall y \left( \langle x, y \rangle \in X \times Y \iff x \in X \land y \in Y \right)
$$


In order to prove this, one may first assume that $X$, $Y$, $x$ and $y$ are sets such that $\langle x, y \rangle \in X \times Y$. Hence, by definition of Cartesian Product:


$$
\exists a \exists b \left( a \in X \land b \in Y \land \langle x, y \rangle = \langle a, b \rangle \right)
$$



Thus: $x = a \land y = b$ which implies that $x \in X \land y \in Y$.

One may then assume that $X$, $Y$, $x$, and $y$ are sets such that $x \in X \land y \in Y$. Hence, as was proved above: $\langle x, y \rangle \in \mathcal{P}\left( \mathcal{P}\left(X \cup Y \right) \right)$. Let $u = \langle x, y \rangle$. Thus, because $\exists x \exists y \left( x \in X \land y \in Y \land u = \langle x, y \rangle \right)$ then $\langle x, y \rangle \in X \times Y$. Therefore, the condition holds. $\blacksquare$


### X × Y ≠ Ø
The following holds:


$$
\forall X \forall Y \left( X \neq \emptyset \land Y \neq \emptyset \Longrightarrow X \times Y \neq \emptyset \right)
$$


In order to prove this, one may let $X$ and $Y$ be sets such that $X \neq \emptyset \land Y \neq \emptyset$.
Hence: $\exists x \exists y \left( x \in X \land y \in Y \right)$ which implies that $\langle x,y \rangle \in X \times Y$. $\blacksquare$

## Partitions
Let $X$ and $P$ be sets such that the following holds:

* $P \subseteq \mathcal{P}\left(X\right)$
* $\emptyset \not\in P$
* $\displaystyle \bigcup P = X$
* $\forall A,B \in P \left( A \neq B \Longrightarrow A \cap B = \emptyset \right)$

Then $P$ is called a partition of $X$.