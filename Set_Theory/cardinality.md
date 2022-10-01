## In Terms Of Functions

### Equal Cardinality
$$
\mathrm{card}\left(A\right) = \mathrm{card}\left(B\right) \iff \exists f: A \rightarrow B, \text{ f is a bijection}
$$



Meaning, the cardinalities of $A$ and $B$ are equal if and only if there is a bijective function from $A$ to $B$. This is a result of the fact that a bijective function $f: A \rightarrow B$ is a one-to-one correspondence between $A$ and $B$.

### Less Than Or Equal To Cardinality
$$
\mathrm{card}\left(A\right) \leq \mathrm{card}\left(B\right) \iff \exists f: A \rightarrow B, \text{ f is an injection}
$$



Meaning, the cardinality of $A$ is equal to or less than the cardinality of $B$ if and only if there is an injective function from $A$ to $B$. This is a result of the fact that, by the definition of an injective function, for every element $a \in A$ there is no more than one element $b \in B$ such that $f\left(a\right) = b$. There could exist elements
$b \in B$ such that there exists no $a \in A$ that satisfies $f\left(a\right) = b$ and so, there is a one-to-one correspondence between $A$ and a subset of $B$ but not necessarily all of $B$.

### Strictly Less Than Cardinality
$$
\begin{split}
	& \mathrm{card}\left(A\right) < \mathrm{card}\left(B\right) \iff \\
	& \exists f: A \rightarrow B, f \text{ is an injection } \land \\
	& \not\exists g: A \to B, g \text{ is a bijection}
\end{split}
$$



Meaning, the cardinality of $A$ is strictly less than the cardinality of $B$ if and only if there is an injective function from $A$ to $B$ but there is no bijective function from $A$ to $B$. This is a result of the fact that, because there is an injective function from $A$ to $B$, then $\mathrm{card}\left(A\right) \leq \mathrm{card}\left(B\right)$ but because there is no bijective function from $A$ to $B$, then $\mathrm{card}\left(A\right) \neq \mathrm{card}\left(B\right)$ and hence: $\mathrm{card}\left(A\right) < \mathrm{card}\left(B\right)$.

## Cantor's Theorem

Cantor's Theorem states that if $A$ is any set then:
$$
\mathrm{card}\left(A\right) < \mathrm{card}\left(\mathcal{P}\left(A\right)\right)
$$


If one shows that there exists an injective function but there exists no bijective function from $A$ to $\mathcal{P}\left(A\right)$, then, as a consequence: $\mathrm{card}\left(A\right) < \mathrm{card}\left(\mathcal{P}\left(A\right)\right)$.

One may assume that there exists a surjective function $f: A \rightarrow \mathcal{P}\left(A\right)$
and prove the claim using proof by contradiction.

One may observe the existence of the set:
$$
B = \Big{\{} x \in A \; \Big{\vert} \; x \not\in f\left(x\right) \Big{\}}
$$


Clearly, $B \subseteq A$, therefore: $B \in \mathcal{P}\left(A\right)$. Hence, If $f$ is surjective then $\exists \xi \in A: f\left(\xi\right) = B$. One may then notice that either $\xi \in B$ or $\xi \notin B$.
* If $\xi \in B$ then, because $f\left(\xi\right) = B$: $\xi \in f\left(\xi\right)$ which implies, by the construction of $B$: $\xi \not\in B$ which is a contradiction to the assumption that $\xi \in B$.
* If $\xi \not\in B$ then, because $f\left(\xi\right) = B$: $\xi \not\in f\left(\xi\right)$ which implies, by the construction of $B$: $\xi \in B$ which is a contradiction to the assumption that $\xi \not\in B$.

Both of these options lead to a contradiction, therefore, $f$ is not surjective.
Therefore, because there's no surjective function from $A$ to $\mathcal{P}\left(A\right)$, there's no bijective function from $A$ to $\mathcal{P}\left(A\right)$.

One may then find an injective function $f: A \rightarrow \mathcal{P}\left(A\right)$ such as:
$$
\forall x \in A: f\left(x\right) = \{ x \} \in \mathcal{P}\left(A\right)
$$


This function is injective because $\forall x,y \in A: \{ x \} = \{ y \} \Rightarrow x = y$.

Therefore, because there is an injective function but no bijective function from $A$ to $\mathcal{P}\left(A\right)$:
$$
\mathrm{card}\left(A\right) < \mathrm{card}\left(\mathcal{P}\left(A\right)\right)
$$


## Infinite Sets
An infinite set is a set that doesn't have a finite number of members.

A set $A$ is only infinite if there is an injective function
from $A$ to $A$ that is not surjective. In terms of sets, $A$ is
only infinite if there is a proper subset of $A$ with the
same cardinality as $A$.
$$
\begin{split}
	& A \text{ is an infinite set } \iff \\
	& \exists f: A \to A \\
	& \not\exists x_1, x_2 \in A: x_1 \neq x_2 \land f\left(x_1\right) = f\left(x_2\right) \land \\
	& \exists y \in A \not\exists x \in A: f\left(x\right) = y \iff \\
	& \exists B: B \subset A \land \mathrm{card}\left(A\right) = \mathrm{card}\left(B\right)
\end{split}
$$


## Cantor Schroeder Bernstein Theorem
Let $A, B$ be sets, if there are injections $f: A \rightarrow B$ and $g: B \rightarrow A$ then there is a bijection $\varphi: A \rightarrow B$. In terms of cardinality: $\mathrm{card}\left(A\right) \leq \mathrm{card}\left(B\right) \land \mathrm{card}\left(B\right) \leq \mathrm{card}\left(A\right) \Longrightarrow \mathrm{card}\left(A\right) = \mathrm{card}\left(B\right)$.

In order to prove this, one may let $F: \mathcal{P}\left(A\right) \rightarrow \mathcal{P}\left(A\right)$
such that $\forall X \in \mathcal{P}\left(A\right), F\left(X\right) = A \setminus g\left[ B \setminus f\left[X\right] \right]$.

Firstly, one may prove that $\forall X, Y \in \mathcal{P}\left(A\right), X \subseteq Y \Rightarrow F\left(X\right) \subseteq F\left(Y\right)$.
Assuming $X, Y \in \mathcal{P}\left(A\right) \land X \subseteq Y$:
Because $f$ is a function, $f\left[X\right] \subseteq f\left[Y\right]$. Hence: $B \setminus f\left[Y\right] \subseteq B \setminus f\left[X\right]$.
Thus, because $g$ is a function: $g\left[B \setminus f\left[Y\right]\right] \subseteq g\left[B \setminus f\left[X\right]\right]$ and hence $A \setminus g\left[B \setminus f\left[X\right]\right] \subseteq A \setminus g\left[B \setminus f\left[Y\right]\right]$. Therefore: $F\left(X\right) = A \setminus g\left[B \setminus f\left[X\right]\right] \subseteq A \setminus g\left[B \setminus f\left[Y\right]\right] = F\left(Y\right)$. Hence: $F\left(X\right) \subseteq F\left(Y\right)$.



Because $\forall X, Y \in \mathcal{P}\left(A\right), X \subseteq Y \Rightarrow F\left(X\right) \subseteq F\left(Y\right)$, by [the fixed point lemma](Set_Theory/functions.md#Fixed-Point-Lemma), there is an $S \in \mathcal{P}\left(A\right)$ such that $F\left(S\right) = S$. Hence, $S = A \setminus g\left[ B \setminus f\left[S\right] \right]$ and thus, because $g\left[ B \setminus f\left[S\right] \right] \subseteq A$ then $A \setminus S = g\left[ B \setminus f\left[S\right] \right]$. Hence, because $g$ is injective, the function $\Omega: B \setminus f\left[S\right] \rightarrow A \setminus S$ such that $\forall b \in B \setminus f\left[S\right], \Omega\left(b\right) = g\left(b\right)$
is bijective, and thus, it has a bijective inverse function $\Omega^{-1}: A \setminus S \rightarrow B \setminus f\left[S\right]$.

One may let $\varphi: A \rightarrow B$:


$$
	\varphi \left(a\right) = {
		\begin{cases}
			f\left(a\right) & a \in S \\
			\Omega^{-1}\left(a\right) & a \in A \setminus S
		\end{cases}
	}
$$


One may observe that $\varphi\left[S\right] = f\left[S\right]$ and $\varphi\left[A \setminus S\right] = \Omega^{-1}\left[A \setminus S\right] = B \setminus f\left[S\right]$ and hence: $\varphi\left[A\right] = f\left[S\right] \cup \left(B \setminus f\left[S\right]\right)$. Thus, because $f\left[S\right] \subseteq B$ then: $\varphi\left[A\right] = B$ and hence $\varphi$ is surjective.

In addition, $\varphi$ is injective, due to $f$ and $\Omega^{-1}$ being injective (And $S \cap \left(B \setminus S\right) = \emptyset$). Thus, $\varphi: A \rightarrow B$ is a bijection. $\blacksquare$