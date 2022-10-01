## Transitive Sets
One may define the following:

$$
\begin{split}
    \forall X (
        \mathrm{TR}\left( X \right) \iff & \forall x \in X : x \subseteq X \\
        \iff & \forall x \left( x \in X \Longrightarrow x \subseteq X \iff x \in \mathcal{P}\left(X\right) \right) \\
        \iff & X \subseteq \mathcal{P}\left(X\right)
    )
\end{split}
$$

If a set $X$ satisfies $\mathrm{TR}\left( X \right)$ then it is called a transitive set.

### Properties

#### TR(X ⋂ Y)
One may observe that the intersection of transitive sets is also transitive.
That is:

$$
\begin{split}
    \forall X \forall Y (
        \mathrm{TR}\left( X \right) \land \mathrm{TR}\left( Y \right) \Longrightarrow & \forall x \in X \cap Y: x \subseteq X \land x \subseteq Y \\
        \Longrightarrow & \forall x \in X \cap Y : x \subseteq X \cap Y \\
        \iff & \mathrm{TR}\left( X \cap Y \right)
    )
\end{split}
$$

#### TR(X ⋃ Y)
The union of transitive sets is transitive.
That is:

$$
\begin{split}
    \forall X \forall Y (
        \mathrm{TR}\left( X \right) \land \mathrm{TR}\left( Y \right) \Longrightarrow & \forall x \in X \cup Y : x \in X \lor x \in Y \Longrightarrow x \subseteq X \lor x \subseteq Y \Longrightarrow x \subseteq X \cup Y \\
        \iff & \mathrm{TR}\left(X \cup Y\right)
    )
\end{split}
$$

#### Union Of A Set Of Transitive Sets Is Transitive
The following holds:

$$
\forall X \left(
        \left( \forall x \in X: \mathrm{TR}\left(x\right) \right) \Longrightarrow
        \mathrm{TR}\left( \bigcup X \right)
    \right)
$$

In order to prove this, one may let $X$ be a set such that $\forall x \in X: \mathrm{TR}\left(x\right)$.

Let $\displaystyle x \in \bigcup X$, then $\exists y \in X: x \in y$.
Hence, because $y \in X$, then $\mathrm{TR}\left(y\right)$ which implies that $x \subseteq y \subseteq \bigcup X$.
Therefore: $x \subseteq \bigcup X$. $\blacksquare$

#### Intersection Of A Set Of Transitive Sets Is Transitive
The following holds:

$$
\forall X \left(
        \left( \forall x \in X: \mathrm{TR}\left(x\right) \right) \Longrightarrow
        \mathrm{TR}\left( \bigcap X \right)
    \right)
$$

In order to prove this, one may let $X$ be a set such that $\forall x \in X: \mathrm{TR}\left(x\right)$
and let $x \in \bigcap X$. Then $\forall y \in S : x \in y$ which implies that $\forall y \in S: x \subseteq y$
and therefore: $\forall z \in x: \left(\forall y \in X: z \in y\right)$.
One may then use the definition of intersection and observe the following: $\displaystyle \forall z \in x: z \in \bigcap X$ which is equivalent to $\displaystyle x \subseteq \bigcap X$. $\blacksquare$


## Definition Of Ordinals

For convenience, one may define the following notation:

$$
\forall \alpha \left( \in_{\alpha} = \left\\{ p \in \alpha \times \alpha : \exists x,y \in \alpha \left( x \in y \land p = \langle x,y \rangle \right) \right\\} \right)
$$

A set $\alpha$ is called a (Von Neumann) ordinal if and only if $\mathrm{ON}\left(\alpha\right)$
where $\mathrm{ON}$ is defined by:

$$
\forall \alpha (
        \mathrm{ON}\left(\alpha\right) \iff \mathrm{TR}\left(\alpha\right) \land
        \mathfrak{W}\left( \in_{\alpha} , \alpha \right)
    )
$$

For convenience, one may denote the fact that $\alpha, \beta, \cdots$ are ordinals by $\mathrm{ON}\left(\alpha,\beta,\cdots\right)$.
That is: $\mathrm{ON}\left(\alpha,\beta,\cdots\right) \iff \mathrm{ON}\left(\alpha\right) \land \mathrm{ON}\left(\beta\right) \land \cdots$.

In addition, one may define the following notation:

$$
\begin{split}
    \forall \alpha, \beta (
        \mathrm{ON}\left(\alpha, \beta\right) \Longrightarrow & \left( \alpha < \beta \iff \alpha \in \beta \right) \land \\
        & \left( \alpha \leq \beta \iff \alpha < \beta \lor \alpha = \beta \right)
    )
\end{split}
$$

$$
 \forall X \left(
        \mathrm{ON_C}\left(X\right) \iff \forall \alpha \in X: \mathrm{ON}\left(\alpha\right)
    \right)
$$

That is, $\mathrm{ON_C}\left(X\right)$ if and only if $X$ is a set of ordinals.


## TR Lemma
The following holds:

$$
\forall \alpha: \mathrm{ON}\left(\alpha\right) \Longrightarrow \mathrm{ON_C}\left(\alpha\right)
$$

In order to prove this, one may let $\alpha$ be an ordinal and let $\beta$ be a set such that $\beta \in \alpha$. Hence, by definition of ordinals: $\beta \subseteq \alpha$. Hence, because $\in_{\alpha}$ well-orders $\alpha$ and $\beta \subseteq \alpha$, then $\in_{\beta}$ well-orders $\beta$. That is: $\mathfrak{W}\left(\in_{\beta}, \beta\right)$.

In addition, one may let $\gamma$ and $\delta$ be sets such that $\delta \in \gamma \in \beta$.
Then:

$$
\begin{split}
    \beta \subseteq \alpha \Longrightarrow \; & \gamma \in \alpha \\
    \Longrightarrow \; & \gamma \subseteq \alpha \\
    \Longrightarrow \; & \delta \in \alpha
\end{split}
$$

Therefore: $\mathrm{TR}\left(\beta\right)$ and thus: $\mathrm{ON}\left( \beta \right)$. $\blacksquare$

## Intersection Lemma
The following holds:

$$
\forall \alpha \forall \beta \left( \mathrm{ON}\left(\alpha, \beta\right) \Longrightarrow \mathrm{ON}\left(\alpha \cap \beta\right) \right)
$$

In order to prove this, one may let $\alpha$ and $\beta$ be ordinals. Firstly, one may observe that $\mathrm{TR}\left( \alpha \cap \beta \right)$. In addition, because $\in_\alpha$ well-orders $\alpha$ and $\alpha \cap \beta \subseteq \alpha$ then $\in_{\alpha \, \cap \, \beta}$ well-orders $\alpha \cap \beta$. Thus: $\mathrm{ON}\left(\alpha \cap \beta\right)$. $\blacksquare$

## Subsets Lemma
The following holds:

$$
\forall \alpha \forall \beta \left(
        \mathrm{ON}\left(\alpha\right) \land \mathrm{ON}\left(\beta\right) \Longrightarrow \left(
            \alpha \subseteq \beta \iff \alpha \in \beta \lor \alpha = \beta
        \right)
    \right)
$$

In order to prove this, one may let $\alpha$ and $\beta$ be ordinals.
Firstly, one may observe that $\mathrm{TR}\left(\beta\right)$ and thus, if $\alpha \in \beta \lor \alpha = \beta$ then $\alpha \subseteq \beta$.
One may then assume that $\alpha \subseteq \beta$. If $\alpha = \beta$ then we are done. Therefore, assume that $\alpha \neq \beta$.

Let $X = \beta \setminus \alpha$, then $X \neq \emptyset$ (If $X = \emptyset$ then $\beta = \alpha$) and thus, because $X \subseteq \beta$ then by the well-orderedness of $\beta$: $\exists \gamma \in X : \forall x \in X: \gamma \neq x \Longrightarrow \gamma \in_{\beta} x \Longrightarrow \gamma \in x$.
In addition, because $\gamma \in X$ then $\gamma \in \beta$ which implies that $\gamma \subseteq \beta$.

Let $\delta \in \gamma$ and assume that $\delta \in X$, then $\delta \in \beta$ and thus: $\delta \in_{\beta} \gamma \land \gamma \in_{\beta} \delta$.

By definition of a well-order, this is possible only if $\gamma = \delta$, but then $\gamma \in \gamma$, a contradiction. Hence: $\forall \delta \in \gamma: \delta \not\in X$.

In addition, because $\gamma \subseteq \beta$ then $\forall \delta \in \gamma: \delta \in \beta \land \delta \not\in X$ which implies: $\forall \delta \in \gamma: \delta \in \alpha$ which is equivalent to $\gamma \subseteq \alpha$.

Let $\delta \in \alpha \setminus \gamma$, then $\delta \in \alpha \subseteq \beta$ and $\gamma \in \beta$. Therefore, because $\beta$ is well-ordered by $\in_{\beta}$, it's also totally ordered by it. Hence, because $\delta \not\in \gamma$ then $\delta = \gamma \lor \gamma \in \delta$.
One may then observe that $\gamma \not\in \alpha$ (because $\gamma \in X$) which implies that $\delta \neq \gamma$ (because $\delta \in \alpha$) and if $\gamma \in \delta$ then $\gamma \in \alpha$ (because $\delta \in \alpha \Longrightarrow \delta \subseteq \alpha$), a contradiction. Therefore: $\alpha \setminus \gamma = \emptyset$ which implies that $\alpha = \gamma$ (because $\gamma \subseteq \alpha$) and thus: $\alpha \in \beta$ (because $\gamma \in \beta$). $\blacksquare$

In addition, The following holds:

$$
\forall \alpha, \beta \left(
        \mathrm{ON}\left(\alpha, \beta\right) \Longrightarrow \left(
            \alpha \leq \beta \iff \alpha \subseteq \beta
        \right)
    \right)
$$


In order to prove this, one may let $\alpha$ and $\beta$ be ordinals. Assume that $\alpha \leq \beta$. If $\alpha < \beta$ then $\alpha \in \beta$ and thus, because $\mathrm{TR}\left(\beta\right)$ then $\alpha \subseteq \beta$. Otherwise, if $\alpha = \beta$ then $\alpha \subseteq \beta$.

One may then assume that $\alpha \subseteq \beta$, then by the subsets lemma: $\alpha \in \beta \lor \alpha = \beta \iff \alpha \leq \beta$. $\blacksquare$

## Asymmetry Lemma
The following holds:

$$
\forall \alpha, \beta \left(
        \mathrm{ON}\left(\alpha, \beta\right) \Longrightarrow
        \left(
            \alpha < \beta \Longrightarrow \alpha \neq \beta \land \lnot\left( \beta < \alpha \right)
        \right)
    \right)
$$


In order to prove this, one may first assume that there is an ordinal $\alpha$ such that $\alpha < \alpha$, then $\alpha \in \alpha$, a contradiction.

One may then let $\alpha$ and $\beta$ be ordinals and assume that $\alpha < \beta \land \beta < \alpha$. That is:
$\alpha \in \beta \land \beta \in \alpha$. Therefore, by definition of ordinals: $\alpha \subseteq \beta \land \beta \subseteq \alpha$. This implies that $\alpha = \beta$ and thus: $\alpha \in \alpha$, a contradiction. $\blacksquare$

## Well-Orderedness of the Ordinals
The following holds:
* $\forall \alpha \left( \mathrm{ON}\left(\alpha\right) \Longrightarrow \lnot\left(\alpha < \alpha\right) \right)$
* $\forall \alpha, \beta, \gamma \left( \mathrm{ON}\left(\alpha,\beta,\gamma\right) \Longrightarrow \left( \alpha < \beta \land \beta < \gamma \Longrightarrow \alpha < \gamma \right) \right)$
* $\forall \alpha, \beta \left( \mathrm{ON}\left(\alpha,\beta\right) \Longrightarrow \left( \left( \alpha < \beta \land \lnot\left(\alpha = \beta \lor \beta < \alpha\right) \right) \lor \left( \beta < \alpha \land \lnot\left(\alpha = \beta \lor \alpha < \beta\right) \right) \lor \left( \alpha = \beta \land \lnot\left(\alpha < \beta \lor \beta < \alpha\right) \right) \right) \right)$
* $\forall S \left( \left( S \neq \emptyset \land \mathrm{ON_C}\left(S\right) \right) \Longrightarrow \exists \beta \in S : \forall \alpha \in S: \beta \neq \alpha \Longrightarrow \beta < \alpha \right)$


Proof of this is presented below.

* Let $\alpha$ be an ordinal, then $\alpha \not\in \alpha$ which is equivalent to $\lnot\left( \alpha < \alpha \right)$.

* Let $\alpha$, $\beta$, and $\gamma$ be ordinals such that $\alpha < \beta \land \beta < \gamma$. Then $\alpha \in \beta \land \beta \in \gamma$. In addition, because $\mathrm{TR}\left(\gamma\right)$ then $\alpha \in \beta \subseteq \gamma$ which implies that $\alpha \in \gamma \iff \alpha < \gamma$. Therefore, the condition holds.

* Let $\alpha$ and $\beta$ be ordinals and $\delta = \alpha \cap \beta$. Hence, by the intersection lemma: $\mathrm{ON}\left(\delta\right)$. In addition: $\delta \subseteq \alpha \land \delta \subseteq \beta$. Therefore, by the subsets lemma: $\left( \delta \in \alpha \lor \delta = \alpha \right) \land \left( \delta \in \beta \lor \delta = \beta \right)$.
  One may then observe the following:
  
  $$
        \begin{split}
            \delta = \alpha \Longrightarrow & \alpha \cap \beta = \alpha \\
            \iff & \alpha \subseteq \beta \\
            \iff & \alpha \in \beta \lor \alpha = \beta \\
            \iff & \alpha < \beta \veebar \alpha = \beta
        \end{split}
  $$
  
  In addition:
  
  $$
        \begin{split}
            \delta = \beta \Longrightarrow & \alpha \cap \beta = \beta \\
            \iff & \beta \subseteq \alpha \\
            \iff & \beta \in \alpha \lor \beta = \alpha \\
            \iff & \beta < \alpha \veebar \beta = \alpha
        \end{split}
  $$
  
  Therefore, if $\delta = \alpha \lor \delta = \beta$ then the condition is met. Assume that $\lnot \left( \delta = \alpha \lor \delta = \beta \right) \iff \delta \neq \alpha \land \delta \neq \beta$, then $\delta \in \alpha \land \delta \in \beta$, meaning $\delta \in \alpha \cap \beta = \delta$, a contradiction. Therefore: $\delta = \alpha \lor \delta = \beta$, and thus, the condition holds.
  
* Let $S$ be a set such that $S \neq \emptyset \land \forall \alpha \in S: \mathrm{ON}\left(\alpha\right)$ and let $\alpha \in S$.
  If $\forall \beta \in S: \alpha \neq \beta \Longrightarrow \alpha < \beta$ then the condition holds. Otherwise ( $\exists \beta \in S: \alpha \neq \beta \land \beta < \alpha$ ) then one may observe that $\alpha \cap S = \left\\{\gamma \in S : \gamma \in \alpha\right\\} = \left\\{\gamma \in S : \gamma < \alpha\right\\} \neq \emptyset$. Hence, because $\alpha \cap S \subseteq \alpha$ then $\exists \delta \in \alpha \cap S: \forall \varepsilon \in \alpha \cap S: \delta \neq \varepsilon \Longrightarrow \delta < \varepsilon$. One may observe that because $\delta \in \alpha \cap S$ then $\delta < \alpha$. Therefore, one may let $\varepsilon \in S$ such that $\varepsilon \neq \delta$ and observe that $\varepsilon = \alpha \lor \varepsilon < \alpha \lor \alpha < \varepsilon$. If $\varepsilon = \alpha$ then $\delta < \varepsilon$. If $\varepsilon < \alpha$ then $\varepsilon < \alpha \land \varepsilon \in S$ which implies that $\varepsilon \in \alpha \cap S$ and thus: $\delta < \varepsilon$. If $\alpha < \varepsilon$ then $\delta < \alpha \land \alpha < \varepsilon \Longrightarrow \delta < \varepsilon$. Therefore, the condition holds. $\blacksquare$

This result implies that $\forall X \left( \mathrm{ON_C}\left(X\right) \Longrightarrow \mathfrak{W}\left(\in_X, X\right) \right)$.

## Transitive Set Of Ordinals is an Ordinal
The following holds:

$$
\forall \alpha \left( \mathrm{TR}\left(\alpha\right) \land \mathrm{ON_C}\left(\alpha\right) \Longrightarrow \mathrm{ON}\left(\alpha\right) \right)
$$


In order to prove this, one may let $\alpha$ be a transitive set of ordinals. Then $\alpha$ is transitive and $\mathfrak{W}\left( \in_{\alpha}, \alpha \right)$, which implies that $\mathrm{ON}\left(\alpha\right)$. $\blacksquare$

## Min, Max, inf, sup

In addition:

$$
\begin{split}
    \forall X \forall \alpha (
        \mathrm{ON_C}\left(X\right) \Longrightarrow (
            & \left( \min X = \alpha \iff \alpha \in X \land \forall \beta \in X: \alpha \leq \beta \right) \\
            & \left( \max X = \alpha \iff \alpha \in X \land \forall \beta \in X: \beta \leq \alpha \right) \\
            & \left( \inf X = \alpha \iff \mathrm{ON}\left(\alpha\right) \land \left( \forall \beta \in X: \alpha \leq \beta \right) \land \left(\not\exists \beta \left( \mathrm{ON}\left(\beta\right) \land \alpha < \beta \land \forall \gamma \in X: \beta \leq \gamma \right)\right) \right) \\
            & \left( \sup X = \alpha \iff \mathrm{ON}\left(\alpha\right) \land \left( \forall \beta \in X: \beta \leq \alpha \right) \land \left(\not\exists \beta \left( \mathrm{ON}\left(\beta\right) \land \beta < \alpha \land \forall \gamma \in X: \gamma \leq \beta \right)\right) \right)
        )
    )
\end{split}
$$

An ordinal $\alpha$ is called a lower bound of a set $X$ if $\forall x \in X: \alpha \leq x$.
An ordinal $\alpha$ is called an upper bound of a set $X$ if $\forall x \in X: x \leq \alpha$.
$\inf X$ is called the infimum of $X$ and is the greatest lower bound of $X$.
$\sup X$ is called the supremum of $X$ and is the least upper bound of $X$.

### Union
The following holds:

$$
\forall \alpha, \beta \left( \mathrm{ON}\left(\alpha,\beta\right) \Longrightarrow \mathrm{ON}\left( \alpha \cup \beta \right) \land \alpha \cup \beta = \max \left\\{ \alpha, \beta \right\\} \right)
$$

In order to prove this, one may let $\alpha$ and $\beta$ be ordinals.

Firstly, one may use the TR lemma and observe that $\mathrm{ON_C}\left(\alpha \cup \beta \right)$ and thus: $\mathfrak{W}\left( \in_{\alpha \cup \beta}, \alpha \cup \beta \right)$. In addition: $\mathrm{TR}\left(\alpha \cup \beta\right)$. Therefore: $\mathrm{ON}\left(\alpha \cup \beta\right)$.


One may then observe that $\alpha < \beta \lor \beta < \alpha \lor \alpha = \beta$. If $\alpha = \beta$ then $\max \left\\{ \alpha, \beta \right\\} = \alpha = \alpha \cup \beta$.

If $\alpha < \beta$ then $\alpha \in \beta$ which implies that $\alpha \subseteq \beta$. Hence: $\alpha \cup \beta = \beta$ and thus: $\max \left\\{ \alpha, \beta \right\\} = \beta = \alpha \cup \beta$.

If $\beta < \alpha$ then $\beta \in \alpha$ which implies that $\beta \subseteq \alpha$. Hence: $\alpha \cup \beta = \alpha$ and thus: $\max \left\\{ \alpha, \beta \right\\} = \alpha = \alpha \cup \beta$. $\blacksquare$


In addition, the following holds:

$$
\forall X \left( \mathrm{ON_C}\left(X\right) \land X \neq \emptyset \Longrightarrow \sup X = \bigcup X \right)
$$

In order to prove this, one may let $X$ be a set such that $\mathrm{ON_C}\left(X\right) \land X \neq \emptyset$.
Therefore, because $X$ is a nonempty set of ordinals, it's a set of transitive sets.
This implies that $\displaystyle \mathrm{TR}\left(\bigcup X\right)$.

In addition:

$$
\begin{split}
    \forall x \in \bigcup X: & \exists y \in X: x \in y \\
    \Longrightarrow & \mathrm{ON}\left(y\right) \land x \in y \\
    \Longrightarrow & \mathrm{ON}\left(x\right)
\end{split}
$$

Hence: $\displaystyle \mathrm{ON_C}\left(\bigcup X\right)$. Therefore, because $\displaystyle \bigcup X$ is a transitive set of ordinals,
then $\displaystyle \mathrm{ON}\left(\bigcup X\right)$.

In addition, one may observe the following:

$$
\forall y \in X: y \subseteq \bigcup X \Longrightarrow y \leq \bigcup X
$$

Hence, $\displaystyle \bigcup X$ is an upper bound of $X$.
Assume that $U$ is another upper bound of $X$ and let $\displaystyle x \in \bigcup X$.
One may observe that $\exists y \in X: x \in y$ and because $U$ is an upper bound of $X$:
$x \in y \land y \leq U$ which is equivalent to $x \in y \land y \subseteq U$ and thus: $x \in U$. Hence: $\displaystyle \forall x \in \bigcup X: x \in U$ which is equivalent to $\displaystyle \bigcup X \subseteq U$ and thus: $\displaystyle \bigcup X \leq U$. $\blacksquare$

### Intersection
The following holds:

$$
\forall \alpha, \beta \left( \mathrm{ON}\left(\alpha,\beta\right) \Longrightarrow \alpha \cap \beta = \min \left\\{ \alpha, \beta \right\\} \right)
$$

In order to prove this, one may let $\alpha$ and $\beta$ be ordinals. By the intersection lemma: $\mathrm{ON}\left(\alpha \cap \beta\right)$. In addition, by the well-orderedness of the ordinals: $\alpha < \beta \lor \beta < \alpha \lor \alpha = \beta$.
If $\alpha < \beta$ then $\alpha \subseteq \beta$ and thus: $\alpha \cap \beta = \alpha$ which implies that $\alpha \cap \beta = \alpha = \min \left\\{ \alpha,\beta \right\\}$.
If $\beta < \alpha$ then $\beta \subseteq \alpha$ and thus: $\alpha \cap \beta = \beta$ which implies that $\alpha \cap \beta = \beta = \min \left\\{ \alpha,\beta \right\\}$.
If $\alpha = \beta$ then $\alpha \cap \beta = \alpha$ which implies that $\alpha \cap \beta = \alpha = \min \left\\{ \alpha,\beta \right\\}$. $\blacksquare$

More generally, the following holds:

$$
\forall X \left(
        \mathrm{ON_C}\left(X\right) \land X \neq \emptyset \Longrightarrow \mathrm{ON}\left( \bigcap X \right) \land \bigcap X = \min X
    \right)
$$

In order to prove this, one may let $X$ be a set such that $\mathrm{ON_C}\left(X\right) \land X \neq \emptyset$.

Firstly, one may observe that $\displaystyle \mathrm{TR}\left(\bigcap X\right)$.
In addition:

$$
\begin{split}
    \forall x \in \bigcap X: & \forall y \in X: x \in y \\
    \Longrightarrow & \forall y \in X: x \subseteq y \\
    \Longrightarrow & \mathrm{ON}\left(x\right)
\end{split}
$$

Therefore, because $\displaystyle \bigcap X$ is a transitive set of ordinals, then $\displaystyle \mathrm{ON}\left(\bigcap X\right)$.

One may then observe that $\exists \alpha \in X: \forall \beta \in X: \alpha \neq \beta \Longrightarrow \alpha < \beta$.
Hence: $\forall \beta \in X: \alpha \leq \beta$ which implies that $\min X = \alpha$.

Firstly, one may observe that because $\alpha \in X$ then $\displaystyle \bigcap X \subseteq \alpha$.
In addition:

$$
\begin{split}
    & \forall \beta \in X: \alpha \subseteq \beta \\
    \Longrightarrow & \forall z \in \alpha : \forall \beta \in X: z \in \alpha \subseteq \beta \\
    \Longrightarrow & \forall z \in \alpha : z \in \bigcap X \\
    \Longrightarrow & \alpha \subseteq \bigcap X
\end{split}
$$

Therefore: $\displaystyle \alpha = \bigcap X$. $\blacksquare$

## Order-Isomorphic Ordinals
The following holds:

$$
\forall \alpha,\beta,F \left(
        \mathrm{ON}\left(\alpha,\beta\right) \land F\left[\alpha \rightarrow \beta\right] \land
        \left(
            \forall \gamma, \delta \in \alpha: \gamma < \delta \iff F\left(\gamma\right) < F\left(\delta\right)
        \right) \Longrightarrow
        \alpha = \beta
    \right)
$$


In order to prove this, one may let $\alpha$ and $\beta$ be ordinals and let $F$ be an order isomorphism. That is: $F\left[\alpha \rightarrow \beta\right] \land \left( \forall \gamma, \delta \in \alpha: \gamma < \delta \iff F\left(\gamma\right) < F\left(\delta\right) \right)$.

One may first prove that $\forall \gamma \in \alpha: F\left(\gamma\right) = \left\\{ \delta \in \beta : \exists \varepsilon \in \alpha \left( \varepsilon < \gamma \land F\left( \varepsilon \right) = \delta \right) \right\\}$.

Let $\gamma \in \alpha$. Firstly, let $\delta \in F\left(\gamma\right)$. Then $\exists \varepsilon \in \alpha \left( F\left(\varepsilon\right) = \delta \right)$ and therefore: $\delta \in F\left(\gamma\right) \iff F\left(\varepsilon\right) < F\left(\gamma\right) \iff \varepsilon < \gamma$. One may then let $\delta \in \beta$ such that $\exists \varepsilon \in \alpha \left( \varepsilon < \gamma \land F\left( \varepsilon \right) = \delta \right)$. Then $\varepsilon < \gamma \iff \delta < F\left(\gamma\right) \iff \delta \in F\left(\gamma\right)$. Hence: $F\left(\gamma\right) = \left\\{ \delta \in \beta : \exists \varepsilon \in \alpha \left( \varepsilon < \gamma \land F\left( \varepsilon \right) = \delta \right) \right\\}$.

Let $X = \left\\{ \varepsilon \in \alpha : F\left(\varepsilon\right) \neq \varepsilon \right\\}$ and assume that $X \neq \emptyset$. Then $\exists \gamma \in X: \forall \varepsilon \in X: \gamma \leq \varepsilon$. Therefore: $\forall \varepsilon \in \alpha: \varepsilon < \gamma \Longrightarrow \varepsilon \not\in X \Longrightarrow F\left(\varepsilon\right) = \varepsilon$. This implies that $F\left(\gamma\right) = \left\\{ \delta \in \beta : \exists \varepsilon \in \alpha \left( \varepsilon < \gamma \land F\left( \varepsilon \right) = \delta \right) \right\\}$ but since $\varepsilon < \gamma$ implies $F\left(\varepsilon\right) = \varepsilon$ the statement becomes $F\left(\gamma\right) = \left\\{ \delta \in \beta : \exists \varepsilon \in \alpha \left( \varepsilon < \gamma \land \varepsilon = \delta \right) \right\\}$. In addition:

$$
\begin{split}
    \forall \delta ( \delta \in \gamma \iff & \delta \in \gamma \land \delta \in \alpha \\
    \iff & \delta < \gamma \land \delta \in \alpha \\
    \iff & \delta \in F\left(\gamma\right) )
\end{split}
$$

And therefore: $F\left(\gamma\right) = \gamma$, a contradiction (because $\gamma \in X$).

Hence: $X = \emptyset$ and thus: $F = \mathrm{id}_\alpha$ which implies that $\alpha = \beta$. $\blacksquare$



## Definition Of Successor
Let $\alpha$ be an ordinal. Then the set $\alpha \cup \left\\{\alpha\right\\}$, denoted $S\left(\alpha\right)$, is called the successor ordinal of $\alpha$.

$$
\forall \alpha \left( S\left(\alpha\right) = \alpha \cup \left\\{ \alpha \right\\} \right)
$$

### Successor is an ordinal
The following holds:

$$
\forall \alpha \left(
        \mathrm{ON}\left(\alpha\right) \Longrightarrow \mathrm{ON}\left(S\left(\alpha\right)\right)
    \right)
$$

In order to prove this, one may let $\alpha$ be an ordinal. Firstly, because $\mathrm{ON_C}\left(\alpha\right) \land \mathrm{ON}\left(\alpha\right)$ then $\mathrm{ON_C}\left(S\left(\alpha\right)\right)$.

In addition, one may let $\beta \in S\left(\alpha\right)$ and observe that $\beta \in \alpha \lor \beta = \alpha$. If $\beta \in \alpha$ then $\beta \subseteq \alpha \subseteq S\left(\alpha\right)$. Otherwise, if $\beta = \alpha$ then $\beta = \alpha \subseteq S\left(\alpha\right)$. Therefore: $\mathrm{TR}\left(S\left(\alpha\right)\right)$.

Hence, because $S\left(\alpha\right)$ is a transitive set of ordinals, then it's an ordinal. $\blacksquare$

### Characteristic Property
The following holds:

$$
\forall \alpha, \beta \left(
        \mathrm{ON}\left(\alpha,\beta\right) \Longrightarrow
        \left(
            \beta < S\left(\alpha\right) \iff
            \beta \leq \alpha
        \right)
    \right)
$$

In order to prove this, one may let $\alpha$ and $\beta$ be ordinals.
Then:

$$
\begin{split}
    \beta < S\left(\alpha\right) \iff & \beta \in S\left(\alpha\right) \\
    \iff & \beta \in \alpha \lor \beta = \alpha \\
    \iff & \beta \leq \alpha
\end{split}
$$

Therefore, the condition holds. $\blacksquare$

### Successor Is Greater
The following holds:

$$
\forall \alpha \left(
        \mathrm{ON}\left(\alpha\right) \Longrightarrow \alpha < S\left(\alpha\right)
    \right)
$$

In order to prove this, one may let $\alpha$ be an ordinal. Then $\alpha \in S\left(\alpha\right)$ which is equivalent to $\alpha < S\left(\alpha\right)$. $\blacksquare$


## Types Of Ordinals
One may define the following:

$$
\forall \alpha \left(
        \mathrm{ON_S}\left( \alpha \right) \iff \mathrm{ON}\left(\alpha\right) \land \exists \beta \left( \mathrm{ON}\left(\beta\right) \land S\left(\beta\right) = \alpha \right)
    \right)
$$

$$
\forall \alpha \left(
        \mathrm{ON_L}\left( \alpha \right) \iff \mathrm{ON}\left(\alpha\right) \land \alpha \neq \emptyset \land \lnot\left( \mathrm{ON_S}\left(\alpha\right) \right)
    \right)
$$

$$
\forall \alpha \left(
            \mathrm{ON_F}\left( \alpha \right) \iff
            \mathrm{ON}\left(\alpha\right) \land
            \forall \beta \left(
                \mathrm{ON}\left(\beta\right) \land
                \beta \leq \alpha \Longrightarrow \beta = \emptyset \lor \mathrm{ON_S}\left(\beta\right)
            \right)
    \right)
$$


If $\mathrm{ON_S}\left( \alpha \right)$ then $\alpha$ is called a successor ordinal.
If $\mathrm{ON_L}\left( \alpha \right)$ then $\alpha$ is called a limit ordinal.
If $\mathrm{ON_F}\left( \alpha \right)$ then $\alpha$ is called a finite ordinal.

## Finite Ordinals

### Successor Of A Finite Ordinal
The following holds:

$$
\forall n \left(
        \mathrm{ON_F}\left( n \right) \Longrightarrow
        \mathrm{ON_F}\left(S\left(n\right)\right)
    \right)
$$


In order to prove this, one may let $n$ be a finite ordinal and $n^{+} = S\left(n\right)$.
Hence, by definition of finite ordinals: $\forall \beta \left( \mathrm{ON}\left(\beta\right) \land \beta \leq n \Longrightarrow \beta = \emptyset \lor \mathrm{ON_S}\left(\beta\right) \right)$. Therefore:

$$
\begin{split}
    \forall \beta (
        \mathrm{ON}\left(\beta\right) \land \beta \leq S\left(n\right) \Longrightarrow & \beta < S\left(n\right) \lor \beta = S\left(n\right) \\
        \iff & \beta \leq n \lor \beta = S\left(n\right) \\
        \Longrightarrow & \beta = \emptyset \lor \mathrm{ON_S}\left(\beta\right) \lor \beta = S\left(n\right)
    )
\end{split}
$$

Thus, because $\beta = S\left(n\right) \Longrightarrow \mathrm{ON_S}\left(\beta\right)$ then:

$$
\forall \beta \left(
        \mathrm{ON}\left(\beta\right) \land \beta \leq S\left(n\right) \Longrightarrow
        \beta = \emptyset \lor \mathrm{ON_S}\left(\beta\right)
    \right)
$$

This implies that $S\left(n\right)$ is a finite ordinal. $\blacksquare$

### A Finite Ordinal Is A Set Of Finite Ordinals
The following holds:

$$
\forall n \left(
        \mathrm{ON_F}\left(n\right) \Longrightarrow
        \forall k \in n : \mathrm{ON_F}\left(k\right)
    \right)
$$

In order to prove this, one may let $n$ be a finite ordinal and $k \in n$. Then:

$$
\begin{split}
    \forall \beta (
        \mathrm{ON}\left(\beta\right) \land \beta \leq k \Longrightarrow & \beta \subseteq k \in n \\
        \Longrightarrow & \beta \subseteq k \subseteq n \\
        \Longrightarrow & \beta \subseteq n \\
        \Longrightarrow & \beta \leq n \\
        \Longrightarrow & \beta = \emptyset \lor \mathrm{ON_S}\left(\beta\right)
    )
\end{split}
$$

This implies that $\mathrm{ON_F}\left(k\right)$. $\blacksquare$

### Principle of Ordinary Induction
The following holds:

$$
\forall X \left(
        \left(
            \emptyset \in X \land
            \left(
                \forall x \in X: S\left(x\right) \in X
            \right)
        \right)
        \Longrightarrow
        \forall n \left(
            \mathrm{ON_F}\left(n\right) \Longrightarrow n \in X
        \right)
    \right)
$$

In order to prove this, one may let $X$ be a set such that $\emptyset \in X \land \left(\forall x \in X: S\left(x\right) \in X \right)$.
Assume that $\exists n \left( \mathrm{ON_F}\left(n\right) \land n \not\in X \right)$ and let $Y = S\left(n\right) \setminus X$.
Firstly, one may observe that because $Y \subseteq S\left(n\right)$ then $\forall u \in Y: \mathrm{ON_F}\left(u\right)$.
In addition, because $n \in Y$ then $Y \neq \emptyset$ and thus, by the well ordering of the ordinals: $\exists k \in Y: \forall \beta \in Y: k \leq \beta$. Because $\emptyset \in X$ then $\emptyset \not\in Y$ and thus: $k \neq \emptyset$. Therefore: $\mathrm{ON_S}\left(k\right)$, which implies that $\exists i \left( \mathrm{ON}\left(i\right) \land S\left(i\right) = k \right)$.
Hence, because $i < k$ then $i \not\in Y$ and $i < k \leq n < S\left(n\right)$ and thus: $i \in S\left(n\right)$.
Therefore, because $i \not\in Y$ then $i \in X$ which implies that $k = S\left(i\right) \in X$ which is a contradiction. $\blacksquare$

### The Set Of All Finite Ordinals
One may use the axiom of infinity and observe the following:

$$
\exists \mathcal{I} \left( \emptyset \in \mathcal{I} \land \forall x \left( x \in \mathcal{I} \Longrightarrow S\left(x\right) \in \mathcal{I} \right) \right)
$$

Hence, by the principle of ordinary induction: $\forall n \left( \mathrm{ON_F}\left(n\right) \Longrightarrow n \in \mathcal{I} \right)$.
Therefore, one may use the axiom schema of specification and define the following set:

$$
\omega = \left\\{ n \in \mathcal{I} : \mathrm{ON_F}\left(n\right) \right\\}
$$

The set $\omega$ satisfies $\forall n \left( n \in \omega \iff \mathrm{ON_F}\left( n \right) \right)$.

### Proof By Induction
Let $\phi\left(n\right)$ be a formula such that the following holds: $\phi\left(\emptyset\right) \land \forall n \in \omega: \phi\left(n\right) \Longrightarrow \phi\left(S\left(n\right)\right)$. Then: $\forall n \in \omega: \phi\left(n\right)$.

In order to prove this, one may let $X = \left\\{ n \in \omega : \phi\left(n\right) \right\\}$ and observe that $\emptyset \in X \land \forall n \in X: S\left(n\right) \in X$. Therefore, by the principle of ordinary induction: $X = \omega$ which implies that $\forall n \in \omega: \phi\left(n\right)$. $\blacksquare$


### Initial Segment Lemma
The following holds:

$$
\forall X \left(
        \mathrm{ON_C}\left(X\right) \land
        \left( \forall \beta \in X: \forall \alpha \left(
            \mathrm{ON}\left(\alpha\right) \land \alpha < \beta \Longrightarrow
            \alpha \in X
        \right) \right) \Longrightarrow
        \mathrm{ON}\left(X\right)
    \right)
$$

In order to prove this, one may first observe that because $\mathrm{ON_C}\left(X\right)$ then $\mathfrak{W}\left(\in_X, X\right)$. In addition:

$$
\begin{split}
    \forall \beta \in X: & \forall \alpha \in \beta: \alpha \in X \\
    \Longrightarrow & \beta \subseteq X
\end{split}
$$

Therefore, $X$ is a transitive set which implies that $X$ is an ordinal. $\blacksquare$

### ω is the least limit ordinal
The following holds:

$$
\forall \alpha \left(
        \mathrm{ON_L}\left(\alpha\right) \Longrightarrow \omega \leq \alpha
    \right)
$$

In order to prove this, one may first observe that $\mathrm{ON_C}\left(\omega\right)$ and:

$$
 \forall n \in \omega: \forall k \left(
        \mathrm{ON}\left(k\right) \land k < n \Longrightarrow
        k \in \omega
    \right)
$$

Therefore, by the initial segment lemma: $\mathrm{ON}\left(\omega\right)$. In addition, because $\emptyset \in \omega$ then $\omega \neq \emptyset$.

Assume that $\mathrm{ON_S}\left(\omega\right)$, then $\exists k \left( \mathrm{ON}\left(k\right) \land S\left(k\right) = \omega \right)$ and $k < \omega$ which implies that $k \in \omega$ and thus, because $\mathrm{ON_F}\left(k\right)$, then $\mathrm{ON_F}\left(\omega\right)$ which implies that $\omega \in \omega$, a contradiction.


Therefore: $\mathrm{ON_L}\left(\omega\right)$.

One may then assume that $\exists \gamma \left( \mathrm{ON_L}\left(\gamma\right) \land \gamma < \omega \right)$. Then $\gamma \in \omega$ which implies that $\forall \beta \left( \mathrm{ON}\left(\beta\right) \land \beta \leq \gamma \Longrightarrow \beta = \emptyset \lor \mathrm{ON_S}\left(\beta\right) \right)$. Hence: $\gamma = \emptyset \lor \mathrm{ON_S}\left(\gamma\right)$ which is a contradiction. $\blacksquare$