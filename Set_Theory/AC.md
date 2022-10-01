The axiom of choice, also known as the AC, states the following:
$$
\forall X \left( \emptyset \not\in X \Longrightarrow \exists F \left( F: X \rightarrow \bigcup X \land \forall Y \left( Y \in X \Longrightarrow F\left( Y \right) \in Y \right) \right) \right)
$$


## Equivalent Statements
Let $AC$ denote the axiom of choice.
In addition, let $AC_\emptyset$ denote the following statement:


$$
\forall X \left( \emptyset \not\in X \land \left( \forall A \forall B \left(A \in X \land B \in X \land A \neq B \Longrightarrow A \cap B = \emptyset \right) \right) \Longrightarrow \exists F \left( F: X \rightarrow \bigcup X \land \forall Y \left( Y \in X \Longrightarrow F\left( Y \right) \in Y \right) \right)  \right)
$$


And let $AC_\mathcal{P}$ denote the following statement:


$$
 \forall X \left( X \neq \emptyset \Longrightarrow \exists F \left( F: \mathcal{P}\left(X\right) \setminus \left\{ \emptyset \right\} \rightarrow X \land \forall Y \left( Y \in \mathcal{P}\left(X\right) \setminus \left\{\emptyset\right\} \Longrightarrow F\left(Y\right) \in Y \right) \right) \right)
$$


Then:


$$
AC \iff AC_\emptyset \iff AC_\mathcal{P}
$$


In order to prove that all three statements are equivalent,
one may prove that $AC \Longrightarrow AC_\emptyset \Longrightarrow AC_\mathcal{P} \Longrightarrow AC$.

* $AC \Longrightarrow AC_\emptyset$
    Assume $AC$ holds and let $X$ be a set such that $\emptyset \not\in X \land \left( \forall A \forall B \left(A \in X \land B \in X \land A \neq B \Longrightarrow A \cap B = \emptyset \right) \right)$.
    By $AC$, because $\emptyset \not\in X$, then $\exists F \left( F: X \rightarrow \bigcup X \land \forall Y \left( Y \in X \Longrightarrow F\left( Y \right) \in Y \right) \right)$.
    Hence, $AC_\emptyset$ holds and thus: $AC \Longrightarrow AC_\emptyset$.
    
* $AC_\emptyset \Longrightarrow AC_\mathcal{P}$

    Assume that $AC_\emptyset$ holds. Let $X$ be a set such that $X \neq \emptyset$ and define:
    
    $$
    \mathcal{S} = \left\{ Z \in \mathcal{P}\left( X \times \mathcal{P}\left( X \right) \right) : \exists A \left( A \in \mathcal{P}\left(X\right) \setminus \left\{ \emptyset \right\} \land Z = A \times \left\{ A \right\} \right) \right\}
    $$
    One may then let $\alpha$ and $\beta$ be sets such that $\alpha \in \mathcal{S} \land \beta \in \mathcal{S} \land \alpha \neq \beta$. Hence: $\exists A \left( A \in \mathcal{P}\left(X\right) \setminus \left\{ \emptyset \right\} \land \alpha = A \times \left\{ A \right\} \right) \land \exists B \left( B \in \mathcal{P}\left(X\right) \setminus \left\{ \emptyset \right\} \land \beta = B \times \left\{ B \right\} \right)$. Thus:
    
    $$
    z \in \alpha \iff \exists a \exists b \left( a \in A \land b = A \land z = \langle a,b \rangle \right)
    $$
    
    $$
    z \in \beta \iff \exists a \exists b \left( a \in B \land b = B \land z = \langle a,b \rangle \right)
    $$
    
    This implies the following:
    
    $$
    z \in \alpha \cap \beta \iff \exists a \exists b \left( z = \langle a,b \rangle \land a \in A \cap B \land b = A \land b = B \right)
    $$
    
    Assume that $\exists z \left( z \in \alpha \cap \beta \right)$. Then, as was shown above, $A = B$. This implies that $\alpha = A \times \left\{A\right\} = B \times \left\{B\right\} = \beta$, a contradiction. Hence: $\forall \alpha \forall \beta \left( \alpha \in \mathcal{S} \land \beta \in \mathcal{S} \land \alpha \neq \beta \Longrightarrow \alpha \cap \beta = \emptyset \right)$.
    
    In addition, because $\mathcal{S}$ consists of Cartesian Products of non-empty sets, then $\emptyset \not\in \mathcal{S}$. Thus, by $AC_\emptyset$: $\exists F \left( F: \mathcal{S} \rightarrow \bigcup \mathcal{S} \land \forall \alpha \left( \alpha \in \mathcal{S} \Longrightarrow F\left( \alpha \right) \in \alpha \right) \right)$. Hence:
    
    $$
    \begin{split}
    \forall \alpha ( \alpha \in \mathcal{S} \Longrightarrow & \exists A \left( A \in \mathcal{P}\left(X\right) \setminus \left\{ \emptyset \right\} \land \alpha = A \times \left\{ A \right\} \right) \\
    \Longrightarrow & F\left(\alpha\right) \in A \times \left\{ A \right\} \\
    \Longrightarrow & \exists a \left( a \in A \land F\left(\alpha\right) = \langle a, A \rangle \right) )
    \end{split}
    $$
    
    One may then define the first coordinate function $\displaystyle \pi_1: \left( \bigcup X \right) \times \left( \mathcal{P}\left( X \right) \setminus \left\{ \emptyset \right\} \right) \rightarrow \bigcup X$ and a function:
    
    $$
    G = \left\{ p \in \mathcal{P}\left(X\right) \times \mathcal{S} : \exists A \left( A \in \mathcal{P}\left(X\right) \setminus \left\{ \emptyset \right\} \land p = \langle A, A \times \left\{A\right\} \rangle \right) \right\}
    $$
    
    Hence, the required choice function can be denoted $\mathcal{F}$ where $\mathcal{F} = \pi_1 \circ \left( F \circ G \right)$:
    
    $$
    \begin{split}
    \forall Y ( Y \in \mathcal{P}\left( X \right) \setminus \left\{ \emptyset \right\} \Longrightarrow & G\left( Y \right) = Y \times \left\{Y\right\} \in \mathcal{S} \\
    \Longrightarrow & F\left( G\left( Y \right) \right) \in Y \times \left\{Y\right\} \\
    \Longrightarrow & \pi_1 \left( F\left( G\left( Y \right) \right) \right) \in Y )
    \end{split}
    $$
    
    And thus, the condition holds.
    
* $AC_\mathcal{P} \Longrightarrow AC$
    Assume that $AC_\mathcal{P}$ holds. Let $X$ be a set such that $\emptyset \not\in X$. If $X = \emptyset$ then the condition vacuously holds. Hence, assume that $X \neq \emptyset$. One may let $\mathfrak{U} = \bigcup X$. Hence:

    $$
    \forall Y \left( Y \in X \Longrightarrow \left[ \forall y \left( y \in Y \Longrightarrow y \in \mathfrak{U} \right) \right] \Longrightarrow Y \subseteq \mathfrak{U} \right)
    $$

    This implies that $\forall Y \left( Y \in X \Longrightarrow Y \in \mathcal{P}\left( \mathfrak{U} \right) \right)$ which is equivalent to $X \subseteq \mathcal{P}\left( \mathfrak{U} \right)$ and because $\emptyset \not\in X$, then $X \subseteq \mathcal{P}\left( \mathfrak{U} \right) \setminus \left\{ \emptyset \right\}$.

    Hence, because $X \neq \emptyset$ and $\emptyset \not\in X$ then $\mathfrak{U} \neq \emptyset$ and by $AC_\mathcal{P}$: $\exists F \left( F: \mathcal{P}\left(\mathfrak{U}\right) \setminus \left\{ \emptyset \right\} \rightarrow \mathfrak{U} \land \forall Y \left( Y \in \mathcal{P}\left(\mathfrak{U}\right) \setminus \left\{\emptyset\right\} \Longrightarrow F\left(Y\right) \in Y \right) \right)$. Thus: $F\vert_X: X \rightarrow \bigcup X$ and the following holds:

    $$
    \forall Y \left( Y \in X \Longrightarrow F\vert_X\left(Y\right) \in Y \right)
    $$

    Therefore, the condition holds.

Hence, because $AC \Longrightarrow AC_\emptyset \Longrightarrow AC_\mathcal{P} \Longrightarrow AC$ then $AC \iff AC_\emptyset \iff AC_\mathcal{P}$. $\blacksquare$