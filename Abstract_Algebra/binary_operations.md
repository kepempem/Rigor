Binary operations are operations of arity 2, which are simply multivariate
functions of two variables. A Binary Operation $\ast$ on a set $A$
is a function $\ast: A^2 \rightarrow A$. If $a, b \in A$ then the image
of $a$ and $b$ by $\ast$, $\ast\left(a, b\right)$ (A single image requires two elements of $A$ because
$\ast$ is a function of two variables) is denoted $a \ast b$ and $a$ and $b$ are then called the operands of the operation.

An important thing to note is that if $\ast$ is a binary operation defined on a set $A$, then $\ast: A^2 \rightarrow A$. Hence, if $b, c \in A$, then the equality $b = c$ implies that $\ast\left(a, b\right) = \ast\left(a,c\right)$. In other words, $a \ast b = a \ast c$ (due to the fact that a function associates to two equal objects of the domain, the same object in the codomain, and because $b=c$, then $\left(a, b\right) = \left(a, c\right)$). The same principle applies for $b \ast a = c \ast a$.


## Properties

### Closure

A Binary Operation $\ast$ is said to be closed under a set $A$ because each combination of two members of $A$ by $\ast$ produces another
element of $A$.
$$
	A \text{ is closed under } \ast \iff \forall a, b \in A: a \ast b \in A
$$

### Associativity

$$
\begin{split}
	&\text{The Binary Operation } \ast \text{ on the set } A \text{ is associative } \iff \\
	&\forall a,b,c \in A: a \ast \left(b \ast c\right) = \left(a \ast b\right) \ast c
\end{split}
$$

If a binary operation $\ast$ is associative, then the order in which one performs the operation $\ast$ on multiple elements does not change the result of the operation, in other words, placing parentheses in an expression with $\ast$ does not change the result of the operation.

### Commutativity

$$
\begin{split}
	&\text{The operation } \ast \text{ on the set } A \text{ is commutative } \iff \\
	& \forall a, b \in A: a \ast b = b \ast a
\end{split}
$$

### Distributivity

If $A$ is a set and $\ast$ and $\Delta$ are two binary operations on $A$ then the operation $\ast$ is said to be distributive over $\Delta$ if it is both left-distributive and right-distributive over $\Delta$.

#### Left Distributivity

$$
\begin{split}
	& \ast \text{ is left-distributive over } \Delta \iff \\
	&\forall a, b, c \in A: a \ast \left(b \Delta c\right) = \left(a \ast b\right) \Delta \left(a \ast c\right)
\end{split}
$$

#### Right Distributivity

$$
\begin{split}
	& \ast \text{ is right-distributive over } \Delta \iff \\
	&\forall a, b, c \in A: \left(b \Delta c\right) \ast a = \left(b \ast a\right) \Delta \left(c \ast a\right)
\end{split}
$$

### Cancellation

An element $a \in A$ is cancellative if it is both left-cancellative and right-cancellative.

#### Left Cancellation

An element $a \in A$ is left-cancellative only if, for all $b, c \in A$, the equality $a \ast b = a \ast c$ implies that $b = c$.

$$
\begin{split}
	&a \in A \text{ is left-cancellative } \iff \\
	&\forall b,c \in A: \Big{[} a \ast b = a \ast c \Longrightarrow b = c \Big{]}
\end{split}
$$

#### Right Cancellation

An element $a \in A$ is right-cancellative only if, for all $b, c \in A$, the equality $b \ast a = c \ast a$ implies that $b = c$.

$$
\begin{split}
	&a \in A \text{ is right-cancellative } \iff \\
	&\forall b,c \in A: \Big{[} b \ast a = c \ast a \Longrightarrow b = c \Big{]}
\end{split}
$$

## Identity Element

An element $e \in A$ is called an identity element of $\ast$ if
$e$ is both a left-identity and right-identity.
$$
\begin{split}
	&e \in A \text{ is an identity element of } \ast \iff \\
	&\forall a \in A: e \ast a = a \ast e = a
\end{split}
$$

### Left Identity
$$
e \in A \text{ is a left-identity } \iff \forall a \in A: e \ast a = a
$$

### Right Identity
$$
e \in A \text{ is a right-identity } \iff \forall a \in A: a \ast e = a
$$

## Inverse Element

If a binary operation $\ast$ on a set $A$ has an identity element, then an inverse element of $a \in A$ is a member of $A$, often denoted
$a^{-1}$ which is both a left and right inverse of $a$.
$$
\begin{split}
	& a^{-1} \in A \text{ is an inverse element of } a \in A \iff \\
	& e \in A \text{ is an identity element of } A \land a \ast a^{-1} = a^{-1} \ast a = e
\end{split}
$$

### Left Inverse
If $a, b \in A$, and $e \in A$ is an identity element of $A$ and $b \ast a = e$ then $b$ is called a left inverse of $a$.

### Right Inverse
If $a, b \in A$, and $e \in A$ is an identity element of $A$ and $a \ast b = e$ then $b$ is called a right inverse of $a$.

### Absorbing Element
An absorbing element of a set $A$ with respect to a binary operation $\ast$ is
an element such that the result combining any element of $A$ with this element
results in this element.
$$
z \in A \text{ is an absorbing element } \iff \forall a \in A: a \ast z = z \ast a = z
$$
