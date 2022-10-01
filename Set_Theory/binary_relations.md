Let $X$ and $Y$ be sets. A set $R$ is called binary relation on $X$ and $Y$
if and only if $R \subseteq X \times Y$.

If $R$ is a binary relation on $X$ and $Y$ and $\langle x, y \rangle \in R$
then $x$ is said to be $R$-related to $y$, in which case, one may write
$x \; R \; y$. That is:

$$
x \; R \; y \iff \langle x, y \rangle \in R \iff x \text{ is } R \text{-related to } y
$$

Let $R \subseteq X \times Y$ be a binary relation on $X$ and $Y$.
If $X = Y$ then $R$ is called a homogeneous relation.

## Types Of Relations
Let $R \subseteq X \times Y$ be a binary relation on $X$ and $Y$.

### Coreflexive Relation

$$
	R \text{ is coreflexive } \iff \forall x \in X: \forall y \in Y: x \; R \; y \Longrightarrow x = y
$$

### Quasi-Reflexive Relation

$$
	R \text{ is quasi-reflexive } \iff \forall x \in X: \forall y \in Y: x \; R \; y \Longrightarrow x \; R \; x \; \land y \; R \; y
$$

### Symmetric Relation

$$
	R \text{ is symmetric } \iff \forall x \in X: \forall y \in Y: x \; R \; y \Longrightarrow y \; R \; x
$$

### Antisymmetric Relation

$$
	R \text{ is antisymmetric } \iff \forall x \in X: \forall y \in Y: x \; R \; y \; \land \; y \; R \; x \Longrightarrow x = y
$$

### Asymmetric Relation

$$
	R \text{ is asymmetric } \iff \forall x \in X: \forall y \in Y: x \; R \; y \Longrightarrow \neg\left(y \; R \; x\right)
$$

### Serial Relation

$$
	R \text{ is serial } \iff \forall x \in X : \exists y \in Y: x \; R \; y
$$

### Homogeneous Relations
Let $R \subseteq X \times X$ be a homogeneous binary relation on $X$.

#### Reflexive Relation

$$
	R \text{ is reflexive } \iff \forall x \in X : x \; R \; x
$$

#### Irreflexive Relation

$$
	R \text{ is irreflexive } \iff \not\exists x \in X : x \; R \; x
$$

#### Transitive Relation

$$
	R \text{ is transitive } \iff \forall x, y, z \in X : x \; R \; y \; \land \; y \; R \; z \Longrightarrow x \; R \; z
$$

#### Complete Relation
Also known as a Connex relation.

$$
	R \text{ is Complete } \iff \forall x, y \in X: x \; R \; y \; \lor \; y \; R \; x
$$

#### Trichotomous Relation

$$
\begin{split}
	& R \text{ is trichotomous } \iff \forall x,y \in X: ( \\
	& \left[x \; R \; y \; \land \; \lnot \left(y \; R \; x\right) \; \land \; \lnot \left(x=y\right)\right] \; \lor \\
	& \left[\lnot \left(x \; R \; y\right) \; \land \; y \; R \; x \; \land \; \lnot \left(x=y\right)\right] \; \lor \\
	& \left[\lnot \left(x \; R \; y\right) \; \land \; \lnot \left(y \; R \; x\right) \; \land \; x=y\right] )
\end{split}
$$

#### Right Euclidean Relation

$$
	R \text{ is right euclidean } \iff \forall x, y, z \in X: x \; R \; y \; \land x \; R \; z \; \Longrightarrow y \; R \; z
$$

#### Left Euclidean Relation

$$
	R \text{ is left euclidean } \iff \forall x, y, z \in X: y \; R \; x \; \land z \; R \; x \; \Longrightarrow y \; R \; z
$$

## Equivalence Relations
A Homogeneous binary relation $\sim$ on a set $X$ is called an equivalence relation
if and only if $\sim$ is reflexive, symmetric, and transitive.
One may denote the fact that a set $\sim$ is an equivalence realtion on
a set $X$ by $\mathrm{Eq}\left(\sim, X\right)$, That is:

$$
\begin{split}
	\forall X \forall \sim (
		& \mathrm{Eq}\left(\sim, X\right) \iff \\
		& \sim \, \subseteq X \times X \land \\
		& \left( \forall x \in X : x \sim x \right) \land \\
		& \left( \forall x, y \in X: x \sim y \Longrightarrow y \sim x \right) \land \\
		& \left( \forall x, y, z \in X : x \; R \; y \; \land \; y \; R \; z \Longrightarrow x \; R \; z \right)
	)
\end{split}
$$

### Equivalence Class
Let $S$ be a set and $\sim$ be an equivalence relation on $S$.
Then for every member $a \in S$, the equivalence class of $a$ with respect to $\sim$,
denoted $\left[a\right]_\sim$, is defined as:

$$
	\forall S \forall \sim \left( \mathrm{Eq}\left(\sim,S\right) \Longrightarrow \forall a \in S : \left[a\right]_\sim := \left\\{ x \in S : x \sim a \right\\} \right)
$$

In addition, one may observe the following:

$$
\begin{split}
	\forall S \forall \sim (
		\mathrm{Eq}\left(\sim,S\right) \Longrightarrow
		\forall a (
			a \in S \Longrightarrow & a \sim a \\
			\Longrightarrow & a \in \left[a\right]_\sim
		)
	)
\end{split}
$$

#### Equality Of Equivalence Classes
The following holds:

$$
	\forall S \forall \sim \left( \mathrm{Eq}\left(\sim,S\right) \Longrightarrow \forall a,b \in S: \left( \left[ a \right]_\sim = \left[ b \right]_\sim \iff a \sim b \right) \right)
$$

In order to prove this, one may let $S$, $\sim$, $a$, and $b$ be sets such that $\mathrm{Eq}\left(\sim,S\right) \land a \in S \land b \in S$.

Firstly, one may assume that $\left[a\right]_\sim = \left[b\right]_\sim$. Then $a \in \left[a\right]_\sim = \left[b\right]_\sim$ and thus, by definition: $a \sim b$.

One may then assume that $a \sim b$. Hence:

$$
\begin{split}
	\forall x (
		x \in \left[a\right]_\sim \iff & x \in S \land x \sim a \sim b \\
		\iff & x \in S \land x \sim b \\
		\iff & x \in \left[b\right]_\sim
	)
\end{split}
$$

Therefore: $\left[a\right]_\sim = \left[b\right]_\sim$, and thus, the condition holds. $\blacksquare$

#### Quotient Set
The quotient set of a set $X$ by an equivalence relation $R$, denoted $X/R$, is defined as follows:

$$
	\forall X \forall R \left( \mathrm{Eq}\left(R,X\right) \Longrightarrow X/R \, := \left\\{ C \in \mathcal{P}\left(X\right) : \exists a \left( a \in X \land C = \left[a\right]_R \right) \right\\} \right)
$$

##### Quotient Set Is A Partition

Let $X$ and $R$ be sets such that $\mathrm{Eq}\left(R,X\right)$.
Then $X/R$ is a partition of $X$.

In order to prove this, one may first assume that $X = \emptyset$,
then the claim is vacuously true. Hence, assume that $X \neq \emptyset$.

Firstly, one may observe that $X/R \subseteq \mathcal{P}\left(X\right)$.

In addition, assume that $\emptyset \in X/R$.
Then, by definition: $\exists a \left( a \in X \land \emptyset = \left[a\right]_R \right)$.
But then $a \in \left[a\right]_R$ which implies that $\left[a\right]_R \neq \emptyset$, a contradiction.
Thus: $\emptyset \not\in X/R$.


Let $a \in X$. Then $a \in \left[a\right]_R \in X/R$.
Hence: $\displaystyle \forall a \left( a \in X \Longrightarrow \exists C \left( C \in X/R \land a \in C \right) \Longrightarrow a \in \bigcup \left( X/R \right) \right)$.
Which implies that $\displaystyle X \subseteq \bigcup \left( X/R \right)$.


In addition, let $\displaystyle a \in \bigcup \left( X/R \right)$.
Then $\exists C \left( C \in X/R \land a \in C \right)$.
Hence: $a \in C \in X/R \subseteq \mathcal{P}\left(X\right)$.
This implies that $C \subseteq X$ and thus: $a \in X$.
Therefore: $\displaystyle \bigcup \left( X/R \right) \subseteq X$.


Hence: $\displaystyle \bigcup \left( X/R \right) = X$.



Assume that $\exists A,B \in X/R \left(A \neq B \land A \cap B \neq \emptyset \right)$.
Then $\exists a \exists b \left( a \in X \land b \in X \land A = \left[a\right]_R \land B = \left[b\right]_R \right)$ and $\exists x \left( x \in \left[a\right]_R \land x \in \left[b\right]_R \right) \Longrightarrow x \sim a \land x \sim b$. Hence, by symmetricity: $a \sim x \land x \sim b$ and thus, by transitivity: $a \sim b$. This implies that $A = B$, a contradiction.

## Orders

### Partial Order

#### Non-Strict
A non-strict partial order (or weak partial order) $\leq$ on a set $X$ is a homogeneous, reflexive, antisymmetric and transitive binary relation on $X$. The ordered pair $\langle X, \leq \rangle$ is then called a partially non-strictly-ordered set. One may denote the fact that $\leq$ is a non-strict partial order on $X$ by $\mathrm{PO_{ns}}\left(\leq, X\right)$. That is:

$$
\begin{split}
	\forall X \forall \leq (
		& \mathrm{PO_{ns}}\left(\leq, X\right) \iff \\
		& \leq \subseteq X \times X \land \forall x,y,z \in X ( \\
		& \left( x \leq x \right) \land \\
		& \left( x \leq y \; \land \; y \leq x \Longrightarrow x = y \right) \land \\
		& \left( x \leq y \land y \leq z \Longrightarrow x \leq z \right) )
	)
\end{split}
$$

#### Strict
A strict partial order $<$ on a set $X$ is a homogeneous, irreflexive, and transitive binary relation
on $X$. The ordered pair $\langle X, < \rangle$ is then called a partially strictly-ordered set.
One may denote the fact that $<$ is a strict partial order on $X$ by $\mathrm{PO_{s}}\left(\leq, X\right)$.
That is:

$$
\begin{split}
	\forall X \forall < (
		& \mathrm{PO_s}\left(<, X\right) \iff \\
		& < \subseteq X \times X \land \forall x,y,z \in X ( \\
		& \lnot\left( x < x \right) \land \\
		& \left( x < y \land y < z \Longrightarrow x < z \right) )
	)
\end{split}
$$

##### Asymmetry
The following holds:

$$
	\forall X \forall < \left( \mathrm{PO_s}\left(<,X\right) \Longrightarrow \forall x,y \in X: \left( x < y \Longrightarrow \lnot\left( y < x \right) \right) \right)
$$

That is, a strict partial order is asymmetrical.

In order to prove this, one may let $X$ and $<$ be sets such that $\mathrm{PO_s}\left(<,X\right)$ and $x$ and $y$ be sets such that $x < y$. Assume that $y < x$, then $x < y \land y < x$ and thus, by transitivity: $x < x$. This contradicts the irreflexivity of strict partial orders. $\blacksquare$

##### Strict Weak Order
A strict weak order is a strict partial order $<$ on $X$ such that:<br/>

$$
	\forall x, y, z \in X: \left( \left[\lnot\left(x < y\right) \land \lnot\left(y < x\right)\right] \land \left[ \lnot\left(y < z\right) \land \lnot\left(z < y\right) \right] \Longrightarrow \left[ \lnot\left(x < z\right) \land \lnot\left(z < x\right) \right]\right)
$$

#### Equivalence Of NS and S Partial Orders
The following holds:

$$
	\forall X \left(
		\left( \exists \leq \left( \mathrm{PO_{ns}}\left(\leq, X\right) \right) \right) \iff
		\left( \exists < \left( \mathrm{PO_s}\left(<, X\right) \right) \right)
	\right)
$$

In order to prove this, one may let $X$ be a set.


Firstly, one may assume that $\exists \leq \left( \mathrm{PO_{ns}}\left(\leq, X\right) \right)$ and let $< \; = \left\\{ p \in \; \leq \; : \; \exists x,y \in X \left( x \neq y \land x \leq y \land p = \langle x,y \rangle \right) \right\\}$. One may then observe that $\forall x \in X: \lnot\left( x < x \right)$. In addition, let $x$, $y$, and $z$ be sets such that $x,y,z \in X$ and $x < y \land y < z$. Hence: $x \neq y \land y \neq z$.

Assume that $x = z$, then $x \leq y \land y \leq x$ and thus, by definition of non-strict partial orders: $x = y$, a contradiction. Thus: $x \neq z$. In addition, by transitivity and definition of $<$:

$$
\begin{split}
	x \leq y \land y \leq z \land x \neq y \land y \neq z \Longrightarrow & x \leq z \land x \neq z \\
	\Longrightarrow & x < z
\end{split}
$$

Hence: $\mathrm{PO_{s}}\left(<, X\right)$.


One may then assume that $\exists < \left( \mathrm{PO_s}\left(<, X\right) \right)$ and let $\leq \; = \left\\{ p \in X \times X : \exists x,y \in X \left( \left( x < y \lor x = y \right) \land p = \langle x,y \rangle \right) \right\\}$. Hence: $\forall x \in X: x \leq x$. In addition, let $x$ and $y$ be sets such that $x \leq y \land y \leq x$. Assume that $x \neq y$, then $x < y \land y < x$ which contradicts the asymmetry of strict partial orders. Hence: $\forall x,y \in X: x \leq y \land y \leq x \Rightarrow x = y$. One may then let $x$, $y$ and $z$ be sets such that $x \leq y \land y \leq z$. If $x = y$ or $y = z$ then $x \leq z$. Otherwise, if $x \neq y \land y \neq z$ then: $x < y \land y < z$ and thus: $x < z$ which implies $x \leq z$. Hence: $\mathrm{PO_{ns}}\left(\leq, X\right)$. $\blacksquare$


Therefore, if $R$ is a partial order (non-strict or strict) on $X$,
one may call the ordered pair $\langle X, R \rangle$ a partially ordered set
and define the following:

$$
	\forall X \forall R \left( \mathrm{PO}\left(R, X\right) \iff \mathrm{PO_{ns}}\left(R, X\right) \lor \mathrm{PO_{s}}\left(R, X\right) \right)
$$

#### Order Isomorphism
Let $\langle X, R_X \rangle$ and $\langle Y, R_Y \rangle$ be partially ordered sets. Then a function $F$ that satisfies $F\left[X \rightarrow Y\right] \land \forall x,y \in X: x \; R_X \; y \iff F\left(x\right) \; R_Y \; F\left(y\right)$. Then $F$ is called an order isomorphism and one may write $\langle X, R_X \rangle \cong \langle Y, R_Y \rangle$.

### Total Order

#### Non-Strict
A non-strict total order $\leq$ is a homogeneous, antisymmetric, transitive and connex binary relation
on $X$. The ordered pair $\langle X, \leq \rangle$ is then called a totally non-strictly-ordered set.
One may denote the fact that $\leq$ is a non-strict total order on $X$ by $\mathrm{TO_{ns}}\left(\leq, X\right)$.
That is:

$$
\begin{split}
	\forall X \forall \leq (
		& \mathrm{TO_{ns}}\left(\leq, X\right) \iff \\
			& \leq \subseteq X \times X \land \forall x,y,z \in X ( \\
			& \left( x \leq y \; \land \; y \leq x \Longrightarrow x = y \right) \land \\
			& \left( x \leq y \land y \leq z \Longrightarrow x \leq z \right) \land \\
			& \left( x \leq y \lor y \leq x \right)
		)
	)
\end{split}
$$

##### Reflexivity
The following holds:

$$
	\forall X \forall \leq \left( \mathrm{TO_{ns}}\left(\leq, X\right) \Longrightarrow \forall x \in X: x \leq x \right)
$$

In order to prove this, one may observe the following:

$$
\begin{split}
	\forall X \forall \leq ( \mathrm{TO_{ns}}\left(\leq, X\right) \Longrightarrow & \forall x \in X: x \leq x \lor x \leq x \\
	\Longrightarrow & x \leq x )
\end{split}
$$

And thus, the condition holds. $\blacksquare$


#### Strict
Let $\mathrm{TO_{s}}\left(<, X\right)$ denote the following:

$$
	\forall X \forall < \left( \mathrm{TO_{s}}\left(<, X\right) \iff \exists \leq \left( \mathrm{TO_{ns}}\left(\leq, X\right) \land \left( \forall x,y \in X: x < y \iff \left( x \leq y \land x \neq y \right) \right) \right) \right)
$$

If $X$ and $<$ are sets such that $\mathrm{TO_{s}}\left(<, X\right)$, then $<$ is called a strict total order on $X$ and the ordered pair $\langle X, < \rangle$ is called a totally strictly-ordered set.

##### Irreflexivity
The following holds:

$$
	\forall X \forall < \left( \mathrm{TO_s}\left(<,X\right) \Longrightarrow \forall x \in X: \lnot\left( x < x \right) \right)
$$

In order to prove this, one may assume that $X$ and $<$ are sets such that $\mathrm{TO_s}\left(<,X\right)$ and let $x \in X$. Therefore, because $x = x$ then $\lnot\left(x < x\right)$. $\blacksquare$


##### Transitivity
The following holds:

$$
	\forall X \forall < \left( \mathrm{TO_s}\left(<,X\right) \Longrightarrow \forall x,y,z \in X: x < y \land y < z \Longrightarrow x < z \right)
$$

In order to prove this, one may assume that $X$ and $<$ are sets such that $\mathrm{TO_s}\left(<,X\right)$ and let $x$, $y$, and $z$ be sets such $x,y,z \in X \land x < y \land y < z$.
Hence: $x \leq y \land y \leq z \land x \neq y \land y \neq z$.
If $x = z$ then $y \leq x$ and thus, by the antisymmetry of $\leq$: $x = y$,
a contradicts. Hence: $x \neq z \land x \leq y \land y \leq z$.
Hence, by transitivity of $\leq$: $x \neq z \land x \leq z \iff x < z$. $\blacksquare$

##### Trichotomy
The following holds:

$$
\begin{split}
	\forall X \forall < (
		\mathrm{TO_s}\left(<,X\right) \Longrightarrow
		\forall x,y \in X: (
			& \left( x < y \land \lnot\left( y < x \lor x = y \right) \right) \lor \\
			& \left( y < x \land \lnot\left( x < y \lor x = y \right) \right) \lor \\
			& \left( x = y \land \lnot\left( x < y \lor y < x \right) \right)
		) 
	)
\end{split}
$$

In order to prove this, one may let $X$ and $<$ be sets such that $\mathrm{TO_s}\left(<,X\right)$ and let $x$ and $y$ be sets such that $x,y \in X$.
If $x = y$ then, by definition of a strict total order: $\lnot \left( x < y \lor y < x \right)$ and thus, the condition holds.
Otherwise, if $x \neq y$ then $\left( x \leq y \lor y \leq x \right) \land x \neq y$.
Assume that $x \leq y \land y \leq x$, then by antisymmetry of non-strict total orders: $x = y$,
a contradiction. Hence: $\left( x \leq y \veebar y \leq x \right) \land x \neq y$
and thus, the condition holds. $\blacksquare$

##### Incomparability
The following holds:

$$
	\forall X \forall < \left(
		\mathrm{TO_s}\left(<, X\right) \Longrightarrow \left(
			\forall x,y \in X : \lnot\left( x < y \right) \land \lnot\left( y < x \right) \iff
			x = y
		\right)
	\right)
$$

In order to prove this, one may let $X$ and $<$ be sets such that $\mathrm{TO_s}\left(<, X\right)$.

Firstly, assume that $x$ and $y$ are sets such that $x,y \in X \land \lnot\left( x < y \right) \land \lnot\left( y < x \right)$.
In addition: $x \leq y \lor y \leq x$.
Hence: $x \leq y \Longrightarrow \lnot\left(x \neq y\right) \iff x = y$ and $y \leq x \Longrightarrow \lnot\left(y \neq x\right) \iff y = x$.
Therefore, either way: $x = y$ and thus, the condition holds.

One may then assume that $x$ and $y$ are sets such that $x,y \in X \land x = y$.
Then, by definition of a strict total order: $\lnot\left( x < y \right) \land \lnot\left( y < x \right)$.
Thus, the condition holds. $\blacksquare$

##### SWO
A strict total order is a strict weak order, that is:

$$
\begin{split}
	\forall X \forall < (
		\mathrm{TO_s}\left(<, X\right) \Longrightarrow
		\forall x, y, z \in X: (
			& ( \left[\lnot\left(x < y\right) \land \lnot\left(y < x\right)\right] \land \\
			& \left[ \lnot\left(y < z\right) \land \lnot\left(z < y\right) \right] ) \Longrightarrow \\
			& \left[ \lnot\left(x < z\right) \land \lnot\left(z < x\right) \right]
		)
	)
\end{split}
$$

In order to prove this, one may let $X$ and $<$ be sets such that $\mathrm{TO_s}\left(<, X\right)$
and $x$, $y$, and $z$ be sets such that $x, y, z \in X \land \left[\lnot\left(x < y\right) \land \lnot\left(y < x\right)\right] \land \left[ \lnot\left(y < z\right) \land \lnot\left(z < y\right) \right]$.
Hence: $x = y \land y = z \Longrightarrow x = z$ which implies that $\lnot\left( x < z \right) \land \lnot\left( z < x \right)$. $\blacksquare$

##### Equivalent Definition
The following holds:

$$
\begin{split}
	\forall X \forall < (
		\mathrm{TO_s}\left(<, X\right) \iff & \left( \forall x \in X: \lnot\left( x < x \right) \right) \land \\
		& \left( \forall x,y,z \in X: x < y \land y < z \Longrightarrow x < z \right) \land \\
		& \left(
			\forall x,y \in X:
			\left( x < y \land \lnot \left( x = y \lor y < x \right) \right) \lor
			\left( y < x \land \lnot \left( x = y \lor x < y \right) \right) \lor
			\left( x = y \land \lnot \left( x < y \lor y < x \right) \right)
		\right)
	)
\end{split}
$$

In order to prove this, one may first assume that $X$ and $<$ are sets such that
$\mathrm{TO_s}\left(<, X\right)$, then the condition holds, as was proved above.

One may then assume that $X$ and $<$ are sets such that $<$ is irreflexive, transitive
and trichotomous and let $\leq \, = \, < \, \cup \left\\{ p \in X \times X : \exists x \in X: p = \langle x, x \rangle \right\\}$.
Firstly, one may observe that $\forall x,y \in X: x < y \iff x \leq y \land x \neq y$.

In addition, one may let $x,y \in X$ and assume that $x \leq y \land y \leq x$.
Then, by the trichotomy of $<$: $x = y$, which implies that $<$ is antisymmetric.

Furthermore, let $x,y,z \in X$ and assume that $x \leq y \land y \leq z$.
If $x = y \lor y = z$ then $x \leq z$.
Otherwise ( $x \neq y \land y \neq z$ ), one may observe that $x < y \land y < z$
which implies that $x < z$ and thus: $x \leq y$.

One may then let $x,y \in X$ and observe that, by trichotomy of $<$: $x < y \lor y < x \lor x = y$
which implies that $x \leq y \lor y \leq x$.

Hence: $\mathrm{TO_{ns}}\left(\leq, X\right)$, and thus, the condition holds. $\blacksquare$

#### Equivalence of NS and S total orders
The following holds:

$$
	\forall X \left(
		\left( \exists \leq \left( \mathrm{TO_{ns}}\left(\leq, X\right) \right) \right) \iff
		\left( \exists < \left( \mathrm{TO_s}\left(<, X\right) \right) \right)
	\right)
$$

In order to prove this, one may let $X$ be a set.

Firstly, one may assume that $\exists \leq \left( \mathrm{TO_{ns}}\left(\leq, X\right) \right)$
and let $< \; = \left\\{ p \in \; \leq \; : \exists x,y \in X \left( x \leq y \land x \neq y \land p = \langle x,y \rangle \right) \right\\}$.
Therefore, since $\forall x,y \in X: x \leq y \iff \langle x,y \rangle \in \; \leq$ then $\forall x,y \in X: x < y \iff x \leq y \land x \neq y$
and thus: $\mathrm{TO_s}\left(<, X\right)$.

One may then assume that $\exists < \left( \mathrm{TO_s}\left(<, X\right) \right)$.
Hence, by definition of a strict total order: $\exists \leq \left( \mathrm{TO_{ns}}\left(\leq,X\right) \right)$.
Hence, the condition holds. $\blacksquare$


Therefore, if $R$ is a total order (non-strict or strict) on $X$,
one may call the ordered pair $\langle X, R \rangle$ a totally ordered set
and define the following:

$$
	\forall X \forall R \left( \mathrm{TO}\left(R, X\right) \iff \mathrm{TO_{ns}}\left(R, X\right) \lor \mathrm{TO_{s}}\left(R, X\right) \right)
$$


### Well Order
Let $\langle X, R \rangle$ be a totally ordered set.
Then $\langle X, R \rangle$ is called a well-ordered set and $R$ is said to well-order $X$ if and only if the following holds
(one may denote the fact that $R$ well-orders $X$ by $\mathfrak{W}\left(R, X\right)$ ):

$$
\begin{split}
	\forall X \forall R (
		\mathfrak{W}\left(R, X\right) \iff & \mathrm{TO}\left(R,X\right) \land \\
		& \forall S \in \mathcal{P}\left(X\right) \setminus \left\\{\emptyset\right\\} \, \exists m \in S \left( \forall x \in S \left( x \neq m \Longrightarrow m \, R \, x \right) \right)
	)
\end{split}
$$

#### Initial Segment
One may define the following:

$$
	\forall X \forall R \forall a \left(
		\mathfrak{W}\left(R, X\right) \land a \in X \Longrightarrow
		\mathrm{Seg}_{X,R} \left(a\right) := \left\\{ x \in X : x \; R \; a \land x \neq a \right\\}
	\right)
$$

The set $\mathrm{Seg}_{X,R}\left(a\right)$ is called the initial segment of $X$ determined by $a$.

#### Subsets
The following holds:

$$
	\forall X \forall R \forall Y \left(
		\mathfrak{W}\left(R, X\right) \land Y \subseteq X \Longrightarrow
		\mathfrak{W}\left(R \cap \left(Y \times Y\right), Y\right)
	\right)
$$

In order to prove this, one mya let $X$, $R$, and $Y$ be sets such that
$\mathfrak{W}\left(R, X\right) \land Y \subseteq X$ and let $\mathcal{Q} = R \cap \left(Y \times Y\right)$. Therefore:

$$
	\forall a \forall b \left( a \, \mathcal{Q} \, b \iff a \in Y \land b \in Y \land a \, R \, b \right)
$$

Hence, because $\mathrm{TO}\left(R, X\right)$ then $\mathcal{Q}$ is transitive and homogeneous ( $\mathcal{Q} \subseteq Y \times Y$ ).

If $\mathrm{TO_{ns}}\left(R, X\right)$ then $\mathcal{Q}$ is antisymmetric
and $\forall a,b \in Y \subseteq X : a \, R \, b \lor b \, R \, a \Longrightarrow a \, \mathcal{Q} \, b \lor b \, \mathcal{Q} \, a$
which implies that $\mathcal{Q}$ is connex and thus: $\mathrm{TO_{ns}}\left(\mathcal{Q}, Y\right)$.

If $\mathrm{TO_s}\left(R, X\right)$ then $\exists R^\ast \left( \mathrm{TO_{ns}}\left(R^\ast, X\right) \land \left( \forall x,y \in X: x \, R \, y \iff \left( x R^\ast y \land x \neq y \right) \right) \right)$ and thus, one may let $\mathcal{Q}^\ast = R^{\ast} \cap \left(Y \times Y\right)$ and therefore, as was proved above: $\mathrm{TO_{ns}}\left(\mathcal{Q}^\ast, Y \right)$.
One may then prove that $\forall x, y \in Y: x \, \mathcal{Q} \, y \iff x \, \mathcal{Q}^\ast \, y \land x \neq y$.


Firstly, assume that $x,y \in Y$ such that $x \, \mathcal{Q} \, y$, then $x \, R \, y$ and thus: $x R^\ast y \land x \neq y$. Hence, because $x,y \in Y$ then $x \, \mathcal{Q}^\ast \, y \land x \neq y$.

One may then assume that $x,y \in Y$ such that $x \, \mathcal{Q}^\ast \, y \land x \neq y$, then $x \, R^\ast \, y \land x \neq y$ which is equivalent to $x \, R \, y$ and thus, because $x,y \in Y$: $x \, \mathcal{Q} \, y$. Therefore: $\mathrm{TO_s}\left(\mathcal{Q}, Y\right)$.

Either way: $\mathrm{TO}\left(\mathcal{Q}, Y\right)$. One may then let $S \in \mathcal{P}\left(Y\right) \setminus \left\\{\emptyset\right\\}$.
Therefore, because $\mathcal{P}\left(Y\right) \setminus \left\\{\emptyset\right\\} \subseteq \mathcal{P}\left(X\right) \setminus \left\\{\emptyset\right\\}$
then $S \in \mathcal{P}\left(X\right) \setminus \left\\{\emptyset\right\\}$ which implies that

$$
	\exists m \in S \left( \forall x \in S \left( x \neq m \Longrightarrow m \, R \, x \Longrightarrow m \, \mathcal{Q} \, x \right) \right)
$$

The statement $m \, R \, x \Longrightarrow m \, \mathcal{Q} \, x$ is true because $m,x \in S \subseteq Y$.
Therefore, the condition holds: $\mathfrak{W}\left(\mathcal{Q}, Y\right)$. $\blacksquare$