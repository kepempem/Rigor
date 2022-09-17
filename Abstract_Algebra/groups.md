## Definition
A set $G$ and a binary operation $\ast$ on $G$ form an Algebraic Structure called a group only if $G$ and $\ast$ meet the following conditions:
* $\ast$ is closed under $G$.
* $\ast$ is associative.
* $\ast$ has an identity element.
* Every element of $G$ has an inverse element.

If $G$ and $\ast$ form a group, one may write:
$\left(G, \ast\right)$ is a group.

$$
\begin{split}
	& \left(G, \ast\right) \text{ is a group } \iff \\
	& \forall a, b \in G: a \ast b \in G \land \\
	& \forall a,b,c \in G: a \ast \left(b \ast c\right) = \left(a \ast b\right) \ast c \land \\
	& \exists e \in G: \forall a \in G: a \ast e = e \ast a = a \land \\
	& \forall a \in G: \exists a^{-1} \in G: a \ast a^{-1} = a^{-1} \ast a = e
\end{split}
$$

The group definition does not require that $\ast$ be commutative, but if it is, then $\left(G, \ast\right)$ is called an abelian group.

## Properties

Let $\left(G, \ast\right)$ be a group and $e \in G$ be its identity element.

### The Identity Element

In any group there is only one identity element. One may prove this using proof by contradiction.
<br/>
Assume that $q \in G$ is also an identity element of $\left(G, \ast\right)$ that satisfies $q \neq e$.
Hence, because $e$ is an identity element: $e \ast q = e$. And because $q$ is an identity element: $e \ast q = q$.
Therefore, $e = q$, a contradiction to one's assumption that $e \neq q$.
Therefore, in any group $\left(G, \ast \right)$ there is only one identity element,
which can be called <b>The</b> identity element. $\blacksquare$

$$
\exists! \; e \in G: \forall a \in G: a \ast e = e \ast a = a
$$

### The Inverse Element Of An Element
For every element $a \in G$ there exists exactly one inverse element $a^{-1} \in G$.
One may prove this using proof by contradiction.
Let $a \in G$. By the definition of a group, $a$ has at least one inverse element.
Assume that $a$ has two inverse elements $a^{-1}_1$ and $a^{-1}_2$ that satisfy $a^{-1}_1 \neq a^{-1}_2$.
Then $a^{-1}_1 \ast a = e$ and thus, because $\ast$ is a function, it associates with any two equal elements the same element
which implies $\left(a^{-1}_1 \ast a\right) \ast a^{-1}_2 = e \ast a^{-1}_2$.
Hence, by the associativity of $\ast$ and the definition of the identity element:
$a^{-1}_1 \ast \left(a \ast a^{-1}_2\right) = a^{-1}_2$.
By one's assumption, $a \ast a^{-1}_2 = e$, therefore: $a^{-1}_1 \ast e = a^{-1}_2$.
And thus: $a^{-1}_1 = a^{-1}_2$.

Which is a contradiction to one's assumption that $a^{-1}_1 \neq a^{-1}_2$ and therefore, in any group $\left(G, \ast\right)$,
for every element $a \in G$ there exists exactly one inverse element. $\blacksquare$

$$
\forall a \in G: \exists! a^{-1} \in G: a \ast a^{-1} = a^{-1} \ast a = e
$$

As a consequence, if two elements $a, b \in G$ satisfy $a \ast b = e$, then $a^{-1} = b$ and $b^{-1} = a$

### The Inverse Element Of The Result Of An Operation

Let $a_1, a_2, a_3, \cdots, a_n \in G$, then the inverse element of $a_1 \ast a_2 \ast a_3 \ast \cdots \ast a_n$
is $a_{n}^{-1} \ast a_{n-1}^{-1} \ast a_{n-2}^{-1} \ast \cdots \ast a_{2}^{-1} \ast a_{1}^{-1}$.
This can be proved using induction on $n$:
1. For $n = 1$: $a_1 \ast a_{1}^{-1} = e$, and therefore, $\left(a^{-1}\right)^{-1} = a$.
2. The induction hypothesis is then, for a positive integer $k$: $\left(a_1 \ast \cdots \ast a_k \right)^{-1} = a_{k}^{-1} \ast \cdots \ast a_{1}^{-1}$. Therefore: $\left(a_1 \ast \cdots \ast a_k \right) \ast \left(a_{k}^{-1} \ast \cdots \ast a_{1}^{-1}\right) = e$.
3. Hence, For $n = k + 1$:
   
   $$
   \begin{split}
   			&\left(a_1 \ast \cdots \ast a_k \ast a_{k+1} \right) \ast \left(a_{k+1}^{-1} \ast a_{k}^{-1} \ast \cdots \ast a_{1}^{-1}\right) \\
   			&= \left(a_1 \ast \cdots \ast a_k \right) \ast \left(a_{k+1} \ast a_{k+1}^{-1} \right) \ast \left(a_{k}^{-1} \ast \cdots \ast a_{1}^{-1}\right) \\
   			&= \left(a_1 \ast \cdots \ast a_k \right) \ast e \ast \left(a_{k}^{-1} \ast \cdots \ast a_{1}^{-1}\right) \\
   			&= \left(a_1 \ast \cdots \ast a_k \right) \ast \left(a_{k}^{-1} \ast \cdots \ast a_{1}^{-1}\right) \\
   			&= e
   		\end{split}
   $$

Hence, for every positive integer $n$, the inverse element of the result of opearting on $n$ elements is given by:

$$
\forall n \in \mathbb{N}: \forall a_1,\cdots, a_n \in G: \left(a_1 \ast \cdots \ast a_n\right)^{-1} = a_{n}^{-1} \ast \cdots \ast a_{1}^{-1}
$$

### Cancellation

Every element of a group is cancellative. One may prove this property in the following way:

#### Proof Of Left-Cancellation
Let $a,b,c \in G$ such that $a \ast b = a \ast c$. Then, by the definition of a group, there exists an element $a^{-1}$ which
is the inverse element of $a$. Hence, $a^{-1} \ast \left(a \ast b\right) = a^{-1} \ast \left(a \ast c\right)$.
Hence, because $\ast$ is associative: $\left(a^{-1} \ast a \right) \ast b = \left(a^{-1} \ast a \right) \ast c$,
which implies: $e \ast b = e \ast c$, and because $e$ is the identity element: $b = c$. $\blacksquare$

$$
\forall a,b,c \in G: a \ast b = a \ast c \implies b = c
$$

#### Proof Of Right-Cancellation
Let $a,b,c \in G$ such that $b \ast a = c \ast a$. Then, by the definition of a group, there exists an element $a^{-1}$ which
is the inverse element of $a$. Hence, $\left(a \ast b\right) \ast a^{-1} = \left(a \ast c\right) \ast a^{-1}$.
Hence, because $\ast$ is associative: $b \ast \left(a \ast a^{-1} \right) = c \ast \left(a \ast a^{-1} \right)$,
which implies: $b \ast e = c \ast e$, and because $e$ is the identity element: $b = c$. $\blacksquare$

$$
\forall a,b,c \in G: b \ast a = c \ast a \implies b = c
$$


### Inverse Element Of An Inverse Element
Let $a \in G$. By the definition of inverse elements in a group: $a \ast a^{-1} = e$.
In addition: $a^{-1} \ast \left(a^{-1}\right)^{-1} = e$.
Therefore, both $a$ and $\left(a^{-1}\right)^{-1}$ are inverse elements of $a^{-1}$.
Hence, by the singularity of inverse elements in a group: $\left(a^{-1}\right)^{-1} = a$ $\blacksquare$

## Powers And Roots Of Group Elements
Let $\left(G, \ast\right)$ be a group.
Then:

$$
\begin{split}
	\forall a \in G: \; & a^1 = a \\
	& \forall n \in \mathbb{N}: a^{n+1} = a^{n} \ast a
\end{split}
$$

If $a \in G$ and $\exists x \in G, n \in \mathbb{N}: x^n = a$
then $x$ is called an $n$th root of $a$.

## Subgroups
Let $\left(G, \ast\right)$ be a group and $S \subseteq G$ such that:
* $S \neq \emptyset$
* $\forall a,b \in S: a \ast b \in S$
* $\forall a \in S: a^{-1} \in S$

Then $\left(S, \ast\right)$ is called a subgroup of $\left(G, \ast\right)$.

### Subgroups Are Groups
Let $\left(S, \ast\right)$ be a subgroup of $\left(G, \ast\right)$, then $\left(S, \ast\right)$ is a group.

In order to prove this one may let $e \in G$ be the identity element
of $\left(G, \ast\right)$ and observe that $\forall a,b \in S: a \ast b \in S$.
Hence, because $S \neq \emptyset$ then $\exists a \in S$.
Thus: $\exists a^{-1} \in S: a \ast a^{-1} = e$. This implies that $e \in S$.
Hence:

* $\forall a,b \in S: a \ast b \in S$
* $\forall a,b,c \in S: a,b,c \in G \Rightarrow a \ast \left(b \ast c\right) = \left(a \ast b\right) \ast c$
* $e \in S \land \forall a \in S: a \in G \Rightarrow a \ast e = e \ast a = a$
* $\forall a \in S: \exists a^{-1} \in S: a \ast a^{-1} = a^{-1} \ast a = e$


Therefore, $\left(S,\ast\right)$ is a group. $\blacksquare$

## Symmetric Groups
Let $X$ be a set and define $S_{\small X} = \left\{ \sigma: X \rightarrow X \; \vert \; \mathfrak{B}\left(\sigma\right) \right\}$ (The set of all permutations of $X$).

One may let $\sigma_1,\sigma_2 \in S_{\small X}$ and observe that because $\sigma_1: X \rightarrow X$ and $\sigma_2: X \rightarrow X$
are bijections, their composition is also a bijection $\left[ \sigma_1 \circ \sigma_2 \right]: X \rightarrow X$
and thus, it is a permutation of $X$ which implies that $\sigma_1 \circ \sigma_2 \in S_{\small X}$.

Let $\sigma_1, \sigma_2, \sigma_3 \in S_{\small X}$. Then:

$$
\begin{split}
	\forall x \in X: \left[ \sigma_1 \circ \left( \sigma_2 \circ \sigma_3 \right) \right]\left(x\right) &= \sigma_1\left( \left[\sigma_2 \circ \sigma_3\right]\left(x\right) \right) \\
	&= \sigma_1\left( \sigma_2 \left( \sigma_3 \left(x\right) \right) \right) \\
	&= \left[\sigma_1 \circ \sigma_2 \right]\left( \sigma_3\left(x\right) \right) \\
	&= \left[ \left(\sigma_1 \circ \sigma_2 \right) \circ \sigma_3 \right] \left(x\right)
\end{split}
$$

Hence: $\forall \sigma_1, \sigma_2, \sigma_3 \in S_{\small X}: \sigma_1 \circ \left( \sigma_2 \circ \sigma_3 \right) = \left(\sigma_1 \circ \sigma_2 \right) \circ \sigma_3$
which implies that $\circ$ is associative under $S_{\small X}$.

The identity function of $X$, $\mathrm{id}_X: X \rightarrow X$, is a bijection.
Hence: $\mathrm{id}_X \in S_{\small X}$. In addition:

$$
\begin{split}
	\forall \sigma \in S_{\small X}: \forall x \in X: \left[ \sigma \circ \mathrm{id}_X \right] \left(x\right) &= \sigma\left(\mathrm{id}_X \left(x\right)\right) \\
	&= \sigma\left(x\right) \\
	&= \mathrm{id}_X \left( \sigma\left(x\right) \right) \\
	&= \left[ \mathrm{id}_X \circ \sigma \right] \left( x \right)
\end{split}
$$

Therefore: $\forall \sigma \in S_{\small X}: \sigma \circ \mathrm{id}_X = \mathrm{id}_X \circ \sigma = \sigma$
which implies that $\mathrm{id}_X$ is an identity element of $\circ$.

Let $\sigma \in S_{\small X}$. Because $\sigma$ is bijective, it has a bijective inverse function $\sigma^{-1}: X \rightarrow X \in S_{\small X}$ and $\sigma \circ \sigma^{-1} = \sigma^{-1} \circ \sigma = \mathrm{id}_X$.
Hence: $\forall \sigma \in S_{\small X}: \exists \sigma^{-1} \in S_{\small X}: \sigma \circ \sigma^{-1} = \sigma^{-1} \circ \sigma = \mathrm{id}_X$.

To conclude: $\left( S_{\small X}, \circ \right)$ is a group and is called the Symmetric group of $X$.

## Group Isomorphism
Let $\left(G_1, \ast\right)$ and $\left(G_2, \cdot \right)$ be groups.
If there exists a bijective function $f: G_1 \rightarrow G_2$ such that the following holds:

$$
\forall x,y \in G_1: f\left(x \ast y\right) = f\left(x\right) \cdot f\left(y\right)
$$

Then $f$ is called an isomorphism from $G_1$ to $G_2$ and $G_1$ is said to be isomorphic to $G_2$.
One may then write $G_1 \cong G_2$.

### Cayley's Theorem
Let $\left(G, \ast\right)$ be a group. Then $G$ is isomorphic to a subgroup of its Symmetric group.

Let $\left(G, \ast\right)$ be a group with an identity element $e \in G$.
In order to prove this theorem, one may define the following:

$$
\begin{split}
	\forall a \in G: \; & \left[ \; \pi_a: G \rightarrow G \; \right] \\
	& \forall x \in G: \pi_a \left(x\right) = a \ast x \in G
\end{split}
$$

Let $a \in G$.

One may let $y_0 \in G$ and $x_0 = a^{-1} \ast y_0 \in G$.
Then:

$$
\begin{split}
	\pi_a\left(x_0\right) &= a \ast x_0 \\
	&= a \ast a^{-1} \ast y_0 \\
	&= y_0
\end{split}
$$

Hence: $\pi_a$ is surjective.

One may then let $x_1, x_2 \in G$ such that $x_1 \neq x_2$
and assume that $\pi_a\left(x_1\right) = \pi_a\left(x_2\right)$.
Then:

$$
\begin{split}
	a \ast x_1 & = a \ast x_2 \\
	\Rightarrow x_1 & = x_2
\end{split}
$$

This is a contradiction and thus, $\pi_a$ is injective.


Hence, $\pi_a: G \rightarrow G$ is a bijective function and thus, it's a permutation of $G$.

---

Let $G^{\ast} = \left\{ \pi_a \; \vert \; a \in G \right\}$.
One may observe that $G^{\ast} \subseteq S_{\small G}$.

Let $a,b \in G$. Then:

$$
\begin{split}
	\forall x \in G: \left[ \pi_a \circ \pi_b \right]\left(x\right) &= \pi_a\left(\pi_b\left(x\right)\right) \\
	&= a \ast \left( b \ast x \right) \\
	&= \left(a \ast b \right) \ast x \\
	&= \pi_{a \ast b} \left( x \right)
\end{split}
$$

This implies that $\forall a,b \in G: \pi_a \circ \pi_b = \pi_{a \ast b}$. Thus, because $a \ast b \in G$ then $\pi_{a \ast b} \in G^{\ast}$. Therefore: $\forall \pi_a,\pi_b \in G^{\ast}: \pi_a \circ \pi_b \in G^{\ast}$.

One may observe that $\forall a \in G: \pi_a \circ \pi_{a^{-1}} = \pi_{a \ast a^{-1}} = \pi_e$ and thus, because $\forall x \in G: \pi_e\left(x\right) = e \ast x = x$ then $\pi_e = \mathrm{id}_G$ which implies that $\forall \pi_a \in G^{\ast}: \left( \pi_{a} \right)^{-1} \in G^{\ast}$.

Thus, because $G^{\ast}$ is closed with respect to composition and inverses,
then $G^{\ast}$ is a subgroup of $S_G$.

One may then prove that $G$ is isomorphic to $G^{\ast}$. Let $f: G \rightarrow G^{\ast}$ such that $\forall a \in G: f\left(a\right) = \pi_a$.

Let $\pi_a \in G^{\ast}$. Then by definition of $G^{\ast}$: $\exists a \in G: f\left(a\right) = \pi_a$
and thus, $f$ is surjective.

Let $a,b \in G$ such that $a \neq b$ and assume that $f\left(a\right) = f\left(b\right)$.
Then $\pi_a = \pi_b$ which is equivalent to:

$$
\begin{split}
	\forall x \in G: & \pi_a\left(x\right) = \pi_b\left(x\right) \\
	\Rightarrow \; & a \ast x = b \ast x \\
	\Rightarrow  \; & a = b
\end{split}
$$

This is a contradiction and thus $f\left(a\right) \neq f\left(b\right)$.

Thus, because $f$ is surjective and injective, it's bijective.

One may then complete the proof by observing the following:

$$
\begin{split}
	\forall a,b \in G: f\left(a \ast b\right) &= \pi_{a \ast b} \\
	&= \pi_a \circ \pi_b \\
	&= f\left(a\right) \circ f\left(b\right)
\end{split}
$$

Hence, $f$ is an isomorphism from $G$ to $G^{\ast}$ and thus, $G$ is isomorphic to $G^{\ast}$. $\blacksquare$

### Isomorphism is an equivalence relation
Let $\left(G_1, \ast\right)$, $\left(G_2, \cdot \right)$, and $\left(G_3,\Delta\right)$ be groups. Then the following holds:
* $G_1 \cong G_1$
* $G_1 \cong G_2 \iff G_2 \cong G_1$
* $G_1 \cong G_2 \land G_2 \cong G_3 \Rightarrow G_1 \cong G_3$


#### Reflexivity
In order to prove that every group $\left(G, \ast\right)$ is isomorphic to itself, one may consider the identity function $\mathrm{id}_G$. This function is bijective and the following holds:

$$
\begin{split}
	\forall x,y \in G: \mathrm{id}_G\left(x \ast y\right) &= x \ast y \\
	&= \mathrm{id}_G\left(x\right) \ast \mathrm{id}_G\left(y\right)
\end{split}
$$

And thus: $G \cong G$. $\blacksquare$

#### Symmetricity
Let $\left(G_1, \ast\right)$ and $\left(G_2, \cdot \right)$ be groups and assume that $G_1 \cong G_2$. Hence, because $G_1$ is isomorphic to $G_2$ then there exists an isomorphism $f: G_1 \rightarrow G_2$. Hence, because $f$ is bijective, it has a bijective inverse function $f^{-1}: G_2 \rightarrow G_1$. Let $y_1, y_2 \in G_2$. Because $f$ is bijective then $\exists x_1, x_2 \in G_1: f\left(x_1\right) = y_1 \land f\left(x_2\right) = y_2$.
Thus: $f\left(x_1 \ast x_2\right) = f\left(x_1\right) \cdot f\left(x_2\right) = y_1 \cdot y_2$ which implies that $f^{-1}\left(y_1 \cdot y_2\right) = x_1 \ast x_2 = f^{-1}\left(y_1\right) \ast f^{-1}\left(y_2\right)$. Hence, $f^{-1}$ is an isomorphism from $G_2$ to $G_1$ which implies that $G_2 \cong G_1$. $\blacksquare$

#### Transitivity
Let $\left(G_1, \ast\right)$, $\left(G_2, \cdot \right)$, and $\left(G_3,\Delta\right)$ be groups
such that $G_1 \cong G_2 \land G_2 \cong G_3$.
Then there is an isomorphism $f_{1 \rightarrow 2}$ from $G_1$ to $G_2$
and an isomorphism $f_{2 \rightarrow 3}$ from $G_2$ to $G_3$.
One may let $f_{1 \rightarrow 3} = f_{2 \rightarrow 3} \circ f_{1 \rightarrow 2}$.

$f_{1 \rightarrow 3}$ is a function from $G_1$ to $G_3$ and because $f_{1 \rightarrow 2}$
and $f_{2 \rightarrow 3}$ are bijective then $f_{1 \rightarrow 3}$ is bijective.

One may then observe that:

$$
\begin{split}
	\forall x,y \in G_1: f_{1 \rightarrow 3} \left(x \ast y\right) &= f_{2 \rightarrow 3} \left( f_{1 \rightarrow 2} \left( x \ast y \right) \right) \\
	&= f_{2 \rightarrow 3} \left( f_{1 \rightarrow 2} \left(x\right) \cdot f_{1 \rightarrow 2} \left( y \right) \right) \\
	&= f_{2 \rightarrow 3} \left( f_{1 \rightarrow 2} \left( x \right) \right) \; \Delta \; f_{2 \rightarrow 3} \left( f_{1 \rightarrow 2} \left( y \right) \right) \\
	&= f_{1 \rightarrow 3} \left(x\right) \; \Delta \; f_{1 \rightarrow 3} \left(y\right)
\end{split}
$$

Hence, $f_{1 \rightarrow 3}$ is an isomorphism from $G_1$ to $G_3$ and thus,
$G_1$ is isomorphic to $G_3$. $\blacksquare$

### Properties Of Isomorphisms

#### Identity Element and Inverse elements
Let $\left(G_1, \ast\right)$ and $\left(G_2, \cdot\right)$ be to groups isomorphic to each other such that $e_1$ is the identity element of $G_1$ and $e_2$ is the identity element of $G_2$.
In addition, let $f: G_1 \rightarrow G_2$ be an isomorphism. Then:

* $f\left(e_1\right) = e_2$
* $\forall a \in G_1: f\left(a^{-1}\right) = f\left(a\right)^{-1}$ (Where $a^{-1}$ is the inverse element of $a$ in the group $\left(G_1,\ast\right)$ and $f\left(a\right)^{-1}$ is the inverse element of $f\left(a\right)$ in the group $\left(G_2,\cdot\right)$)

In order to prove this, one may first observe the following:

$$
\begin{split}
	\forall a \in G_1: & f\left(a \ast e_1\right) = f\left(a\right) \cdot f\left(e_1\right) \; \land \\
	& f\left(a \ast e_1\right) = f\left(a\right)
\end{split}
$$

Hence: $\forall a \in G_1: f\left(a\right) \cdot f\left(e_1\right) = f\left(a\right) \cdot e_2$
and thus: $f\left(e_1\right) = e_2$.

In addition, one may let $a \in G_1$ and observe that $f\left(a \ast a^{-1}\right) = f\left(e_1\right) = e_2$.
Hence: $f\left(a\right) \cdot f\left(a^{-1}\right) = e_2$. Thus, $f\left(a^{-1}\right)$ is the inverse element
of $f\left(a\right)$ in the group $\left(G_2,\cdot\right)$, as desired. $\blacksquare$

## Group Homomorphism

Let $\left(A, \ast_{\small A}\right)$ and $\left(B, \ast_{\small B}\right)$ be groups. A function $f: A \rightarrow B$ is called a group
homomorphism if $\forall x, y \in A: f\left(x \ast_{\small A} y\right) = f\left(x\right) \ast_{\small B} f\left(y\right)$.