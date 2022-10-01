Let $F$ be a set such that the following holds:

* $\forall p \left( p \in F \Longrightarrow \exists x \exists y \left( p = \langle x, y \rangle \right) \right)$
* $\forall x \forall y \forall y^\ast \left( \langle x, y \rangle \in F \land \langle x, y^\ast \rangle \in F \Longrightarrow y = y^\ast \right)$

Then $F$ is called a function. One may denote the fact that a set $F$ is a function by writing $\mathrm{Func}\left(F\right)$. That is:


$$
\forall F \left( \mathrm{Func}\left(F\right) \iff \left( \forall p \left( p \in F \Longrightarrow \exists x \exists y \left( p = \langle x, y \rangle \right) \right) \right) \land \left( \forall x \forall y \forall y^\ast \left( \langle x, y \rangle \in F \land \langle x, y^\ast \rangle \in F \Longrightarrow y = y^\ast \right) \right) \right)
$$


The following holds:


$$
\forall F \forall x \forall y \left( \langle x, y \rangle \in F \Rightarrow x \in \bigcup \left( \bigcup F \right) \land y \in \bigcup \left( \bigcup F \right) \right)
$$


In order to prove this, let $F$, $x$ and $y$ be sets such that $\langle x, y \rangle \in F$. Then:
$$
\begin{split}
    & \langle x, y \rangle = \left\{ \left\{x\right\}, \left\{x,y\right\} \right\} \in F \\
    \Longrightarrow & \left\{ x, y \right\} \in \bigcup F \\
    \Longrightarrow & x \in \bigcup \left( \bigcup F \right) \land y \in \bigcup \left( \bigcup F \right)
\end{split}
$$


## Domain

The domain of a function $F$, denoted $\mathrm{Dom}\left(F\right)$ is defined as follows:
$$
\forall F \left( \mathrm{Func}\left(F\right) \Longrightarrow \mathrm{Dom}\left(F\right) := \left\{ x \in \bigcup \left( \bigcup F \right) \; \vert \; \exists y \left( \langle x, y \rangle \in F \right) \right\} \right)
$$


## Range
The range of a function $F$, denoted $\mathrm{Range}\left(F\right)$ is defined as follows:
$$
\forall F \left( \mathrm{Func}\left(F\right) \Longrightarrow \mathrm{Range}\left( F \right) := \left\{ y \in \bigcup \left( \bigcup F \right) \; \vert \; \exists x \left( \langle x, y \rangle \in F \right) \right\} \right)
$$


## Restriction
Given a function $F$ and a set $X$ such that $X \subseteq \mathrm{Dom}\left(F\right)$,
the restriction of the function $F$ to $X$, denoted $F\vert_X$, is defined as follows:
$$
\forall F \forall X \left( \mathrm{Func}\left(F\right) \land X \subseteq \mathrm{Dom}\left(F\right) \Longrightarrow F\vert_X := \left\{ p \in F \; \vert \; \exists x \exists y \left( x \in X \land p = \langle x, y \rangle \right) \right\} \right)
$$


A restriction of a function $F$ to $X$ is a function such that $\mathrm{Dom}\left(F\vert_X\right) = X$.
In order to prove this, one may let $F$ be a set such that $\mathrm{Func}\left(F\right)$ and $X$ be a set
such that $X \subseteq \mathrm{Dom}\left(F\right)$. Hence:
$$
\mathrm{Dom}\left(F\vert_X\right) = \left\{ x \in \bigcup \left( \bigcup F\vert_X \right) \; \vert \; \exists y \left( \langle x, y \rangle \in F\vert_X \right) \right\}
$$


One may then prove that $\forall x \left( x \in X \iff x \in \mathrm{Dom}\left(F\vert_X\right) \right)$.

Assume that $x$ is a set such that $x \in X \subseteq \mathrm{Dom}\left(F\right)$. Then $x \in \mathrm{Dom}\left(F\right)$. Hence, by definition of the domain of a function: $\exists y \left( \langle x, y \rangle \in F \right)$. Therefore, because $x \in X \land \langle x, y \rangle \in F$ then $\langle x, y \rangle \in F\vert_X$. In addition, the following holds:

$$
\begin{split}
    & \langle x, y \rangle \in F\vert_X \\
    \Longrightarrow & \left\{ \left\{x\right\}, \left\{x,y\right\} \right\} \in F\vert_X \\
    \Longrightarrow & \left\{ x \right\} \in \bigcup F\vert_X \\
    \Longrightarrow & x \in \bigcup \left( \bigcup F\vert_X \right)
\end{split}
$$

Thus: $x \in \mathrm{Dom}\left(F\vert_X\right)$.

One may then assume that $x$ is a set such that $x \in \mathrm{Dom}\left(F\vert_X\right)$ then $\exists y \left( \langle x, y \rangle \in F\vert_X \right)$ and thus: $x \in X$. $\blacksquare$


## Notation
The following are a few notation conventions:
* $\forall F \forall X \forall Y \left( F: X \rightarrow Y \iff \mathrm{Func}\left(F\right) \land X = \mathrm{Dom}\left(F\right) \land \mathrm{Range}\left(F\right) \subseteq Y \right)$
* $\forall F \forall X \forall Y \left( F: X \rightarrow Y \Longrightarrow \forall x \forall y \left( F\left(x\right) = y \iff \langle x, y \rangle \in F \right) \right)$
* $\forall F \forall X \forall Y \left( F: X \rightarrow Y \Longrightarrow \forall A \left( A \subseteq X \Longrightarrow F\left[ A \right] = \left\{ y \in \mathrm{Range}\left(F\right) : \exists x \left( x \in A \land y = f\left(x\right) \right) \right\} \right) \right)$

The following holds:
$$
\forall F \left( \mathrm{Func}\left(F\right) \Longrightarrow \forall x \left( x \in \mathrm{Dom}\left(F\right) \Longrightarrow \exists ! y \left( F\left(x\right) = y \right) \right) \right)
$$


In order to prove this, one may let $F$ be a function and let $x$ be a set such that $x \in \mathrm{Dom}\left(F\right)$. By definition of the domain of a function: $\exists y \left( \langle x, y \rangle \in F \right)$. Hence: $F\left(x\right) = y$. Assume that $\exists y^\ast \left( y^\ast \neq y \land F\left(x\right) = y^\ast \right)$, then $\langle x, y^\ast \rangle \in F$ and thus, by definition of a function: $y = y^\ast$. $\blacksquare$

## F: X → Y ⇒ F ⊆ X × Y
The following holds:
$$
\forall F \forall X \forall Y \left( F: X \rightarrow Y \Longrightarrow F \subseteq X \times Y \right)
$$


In order to prove this, one may let $F$, $X$ and $Y$ be sets such that
$F: X \rightarrow Y$. Hence, the following holds:

* $\mathrm{Func}\left(F\right) \Longrightarrow \forall p \left( p \in F \Longrightarrow \exists x \exists y \left( p = \langle x, y \rangle \right) \right)$
* $X = \mathrm{Dom}\left(F\right)$
* $\mathrm{Range}\left(F\right) \subseteq Y$

Let $p \in F$ and $x$ and $y$ be sets such that $p = \langle x, y \rangle$. Hence: $x \in \bigcup \left( \bigcup F \right) \land y \in \bigcup \left( \bigcup F \right)$. Thus, by definition of domain and range: $x \in \mathrm{Dom}\left(F\right) \land y \in \mathrm{Range}\left(F\right)$. Because $X = \mathrm{Dom}\left(F\right)$ then $x \in X$ and because $y \in \mathrm{Range}\left(F\right) \subseteq Y$ then $y \in Y$. This implies that $p = \langle x, y \rangle \in X \times Y$.

Hence, because $\forall p \left( p \in F \Longrightarrow p \in X \times Y \right)$ then $F \subseteq X \times Y$. $\blacksquare$

## Injections
Let $F$ be a set such that $\mathrm{Func}\left(F\right)$. and $\forall \alpha \forall \beta \left( \alpha \in \mathrm{Dom}\left(F\right) \land \beta \in \mathrm{Dom}\left(F\right) \land F\left( \alpha \right) = F\left(\beta\right) \Longrightarrow \alpha = \beta \right)$. Then $F$ is called an injective function, or injection. One may denote this $\mathrm{Inj}\left(F\right)$.

$$
 \forall F \left( \mathrm{Inj}\left( F \right) \iff \mathrm{Func}\left(F\right) \land \forall \alpha \forall \beta \left( \alpha \in \mathrm{Dom}\left(F\right) \land \beta \in \mathrm{Dom}\left(F\right) \land F\left( \alpha \right) = F\left(\beta\right) \Longrightarrow \alpha = \beta \right) \right)
$$


## Surjections
If one lets $F$, $X$, and $Y$ be sets such that $F: X \rightarrow Y \land Y = \mathrm{Range}\left(F\right)$. Then $F$ is called a function from $X$ <i>onto</i> $Y$, sometimes called a surjection. One may denote this $F\left\{ X \rightarrow Y \right\}$.
That is:
$$
\forall F \forall X \forall Y \left( F\left\{ X \rightarrow Y \right\} \iff F : X \rightarrow Y \land Y = \mathrm{Range}\left(F\right) \right)
$$


The following holds:


$$
 \forall F \forall X \forall Y \left(
        F: X \rightarrow Y \Longrightarrow
        \left(
            F\left\{ X \rightarrow Y \right\} \iff
            \forall y \left( y \in Y \Longrightarrow
                \exists x \left(
                    x \in X \land F\left(x\right) = y
                \right)
            \right)
        \right)
    \right)
$$


In order to prove this, one may let $F$, $X$ and $Y$ be sets such that $F: X \rightarrow Y$.

Firstly, one may assume that $F\left\{ X \rightarrow Y \right\}$.
Hence: $\mathrm{Range}\left(F\right) = Y$. Let $y$ be a set such that $y \in Y$, then $y \in \mathrm{Range}\left(F\right)$ and thus: $\exists x \left( \langle x,y \rangle \in F \right)$. Therefore: $F\left(x\right) = y$.

One may then assume that $\forall y \left( y \in Y \Longrightarrow \exists x \left( x \in X \land F\left(x\right) = y \right) \right)$.
Firstly, one may observe that $\mathrm{Range}\left(F\right) \subseteq Y$.
In addition:


$$
\forall y \left( y \in \mathrm{Range}\left(F\right) \subseteq Y \iff \exists x \left( x \in X \land F\left(x\right) = y \Longrightarrow y \in \mathrm{Range}\left(F\right) \right) \right)
$$


Hence: $Y \subseteq \mathrm{Range}\left(F\right)$ and therefore: $\mathrm{Range}\left(F\right) = Y$ which implies that $F\left\{ X \rightarrow Y \right\}$. $\blacksquare$




## Bijections
If one lets $F$, $X$, and $Y$ be sets such that $F\left\{X \rightarrow Y\right\} \land \mathrm{Inj}\left(F\right)$.
Then $F$ is called a bijection from $X$ onto $Y$. One may denote this $F\left[ X \rightarrow Y \right]$.
That is:
$$
\forall F \forall X \forall Y \left( F\left[ X \rightarrow Y \right] \iff F\left\{ X \rightarrow Y \right\} \land \mathrm{Inj}\left(F\right) \right)
$$


## Compositions
Let the statement $\mathfrak{Com}\left(F, G\right)$ denote the following:
$$
\forall F \forall G \left( \mathfrak{Com}\left(F, G\right) \iff \left( \mathrm{Func}\left(F\right) \land \mathrm{Func}\left(G\right) \land \mathrm{Range}\left(G\right) \subseteq \mathrm{Dom}\left(F\right) \right) \right)
$$


Let $F$ and $G$ be functions such that $\mathfrak{Com}\left(F, G\right)$.
One may then define a function $F \circ G$, called the composition of $F$ and $G$ as follows:
$$
\begin{split}
    & \forall F \forall G ( \mathfrak{Com}\left(F, G\right) \Longrightarrow \\
    & F \circ G = \left\{ p \in \mathrm{Dom}\left(G\right) \times \mathrm{Range}\left(F\right) : \exists x \exists y \left( x \in \mathrm{Dom}\left(G\right) \land y = F\left(G\left(x\right)\right) \land p = \langle x,y \rangle \right) \right\} )
\end{split}
$$


In addition, the following holds:
$$
    \forall F \forall G \left(
        \mathfrak{Com}\left(F,G\right) \Longrightarrow
        \left(
            \forall x \forall y \left(
                x \in \mathrm{Dom}\left(G\right) \land
                y = F\left(G\left(x\right)\right)
                \Longrightarrow
                \langle x,y \rangle \in \mathrm{Dom}\left(G\right) \times \mathrm{Range}\left(F\right)
            \right)
        \right)
    \right)
$$


In order to prove this, one may assume that $F$ and $G$ are functions
such that $\mathfrak{Com}\left(F,G\right)$.
Hence:


$$
\begin{split}
    \forall x \forall y ( x \in \mathrm{Dom}\left(G\right) \land
    y = F\left(G\left(x\right)\right) \Longrightarrow & G\left(x\right) \in \mathrm{Range}\left(G\right) \subseteq \mathrm{Dom}\left(F\right) \\
    \Longrightarrow & y = F\left(G\left(x\right)\right) \in \mathrm{Range}\left(F\right) \\
    \Longrightarrow & \langle x,y \rangle \in \mathrm{Dom}\left(G\right) \times \mathrm{Range}\left(F\right) )
\end{split}
$$


This also implies that $F \circ G \subseteq \mathrm{Dom}\left(G\right) \times \mathrm{Range}\left(F\right)$.

### Composition Is A Function
The following holds:
$$
\forall F \forall G \left( \mathfrak{Com}\left(F, G\right) \Longrightarrow F \circ G : \mathrm{Dom}\left(G\right) \rightarrow \mathrm{Range}\left(F\right) \right)
$$


In order to prove this, one may let $F$ and $G$ be functions such that $\mathfrak{Com}\left(F, G\right)$. Hence: $F \circ G = \left\{ p \in \mathrm{Dom}\left(G\right) \times \mathrm{Range}\left(F\right) : \exists x \exists y \left( x \in \mathrm{Dom}\left(G\right) \land y = F\left(G\left(x\right)\right) \land p = \langle x,y \rangle \right) \right\}$.

Firstly, one may observe that $\forall p \left( p \in F \circ G \Longrightarrow \exists x \exists y \left( p = \langle x, y \rangle \right) \right)$.

In addition, one may observe the following:


$$
\begin{split}
    \forall x \forall y \forall y^\ast ( \langle x, y \rangle \in F \circ G \land \langle x, y^\ast \rangle \in F \circ G \Longrightarrow & F\left(G\left( x \right)\right) = y \land F\left(G\left( x \right)\right) = y^\ast \\
    \Longrightarrow & y = y^{\ast} )
\end{split}
$$


Hence: $\mathrm{Func}\left( F \circ G \right)$.



One may then observe the following:
$$
\begin{split}
    \forall x (
        x \in \mathrm{Dom}\left( G \right) \iff
        \exists y ( & \langle x,y \rangle \in G \\
            \iff & G\left(x\right) = y \\
            \Longrightarrow & F\left(G\left(x\right)\right) = F\left(y\right) \\
            \iff & \langle x, F\left(y\right) \rangle \in F \circ G \\
            \Longrightarrow & x \in \mathrm{Dom}\left( F \circ G \right)
        )
    )
\end{split}
$$


Thus: $\mathrm{Dom}\left( G \right) \subseteq \mathrm{Dom}\left( F \circ G \right)$.
In addition:
$$
\begin{split}
    \forall x ( & x \in \mathrm{Dom}\left( F \circ G \right) \\
    \Longrightarrow & \exists y ( \langle x, y \rangle \in F \circ G \subseteq \mathrm{Dom}\left(G\right) \times \mathrm{Range}\left(F\right) & \\
    \Longrightarrow & x \in \mathrm{Dom}\left(G\right) ) )
\end{split}
$$


Hence: $\mathrm{Dom}\left(F \circ G\right) = \mathrm{Dom}\left(G\right)$.

In addition:
$$
\begin{split}
    \forall y (
        y \in \mathrm{Range}\left( F \circ G \right) \Longrightarrow
        \exists x (
            & \langle x,y \rangle \in F \circ G \subseteq \mathrm{Dom}\left(G\right) \times \mathrm{Range}\left(F\right) \\
            \Longrightarrow & y \in \mathrm{Range}\left(F\right)
        )
    )
\end{split}
$$


Hence: $\mathrm{Range}\left(F \circ G\right) \subseteq \mathrm{Range}\left(F\right)$
and thus: $F \circ G : \mathrm{Dom}\left( G \right) \rightarrow \mathrm{Range}\left(F\right)$, as desired. $\blacksquare$

### Composition Of Bijections

The following holds:
$$
\forall F \forall G \forall X \forall Y \forall Z \left( G\left[X \rightarrow Y\right] \land F\left[Y \rightarrow Z\right] \Longrightarrow \mathfrak{Com}\left(F,G\right) \land F \circ G\left[X \rightarrow Z\right] \right)
$$


In order to prove this, one may let $F$, $G$, $X$, $Y$, and $Z$ be functions such that $G\left[X \rightarrow Y\right]$ and $F\left[Y \rightarrow Z\right]$. Hence: $\mathrm{Range}\left(G\right) = Y \subseteq Y = \mathrm{Dom}\left(F\right)$ which implies that $\mathfrak{Com}\left(F,G\right)$.


Therefore: $F \circ G: X \rightarrow Z$.
One may then observe the following:

$$
\begin{split}
    \forall \alpha \forall \beta (
        & \alpha \in X \land \beta \in X \land F \circ G \left(\alpha\right) = F \circ G \left(\beta\right) \\
        \Longrightarrow & F\left(G\left(\alpha\right)\right) = F\left(G\left(\alpha\right)\right) \\
        \Longrightarrow & G\left(\alpha\right) = G\left(\beta\right) \\
        \Longrightarrow & \alpha = \beta
    )
\end{split}
$$


Hence: $\mathrm{Inj}\left(F \circ G\right)$. In addition, let $z$ be a set such that $z \in Z$, then $\exists y \left( y \in Y \land F\left(y\right) = z \right)$. Furthermore, because $y \in Y$ then $\exists x \left( x \in X \land G\left(x\right) = y \right)$. Hence: $F \circ G \left( x \right) = F\left(G\left(x\right)\right) = F\left(y\right) = z$. Therefore: $F \circ G \left\{X \rightarrow Z\right\}$ which implies that $F \circ G \left[X \rightarrow Z\right]$. $\blacksquare$

## Permutations
Let $F$ and $X$ be sets such that $F\left[X \rightarrow X\right]$.
Then $F$ is called a permutation of $X$.

## Basic Functions

### First Coordinate
Let $X$ and $Y$ be sets. One may define a function $\pi_1: X \times Y \rightarrow X$ as follows:
$$
\pi_1 = \left\{ p \in \left(X \times Y\right) \times X : \exists x \exists y \left( x \in X \land y \in Y \land p = \langle \langle x, y \rangle, x \rangle \right) \right\}
$$


Hence:
$$
\forall x \forall y \left( x \in X \land y \in Y \Longrightarrow \pi_1\left( \langle x,y \rangle \right) = x \right)
$$


The function $\pi_1$ is called the first coordinate function and can be defined for any two sets $X$ and $Y$.