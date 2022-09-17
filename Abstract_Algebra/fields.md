## Definition
A set $F$ and two binary operations $+$ (Called Addition) and $\cdot$ (Called Multiplication) on $F$ form an Algebraic Structure called a Field only if $F$, $+$, and $\cdot$ meet the following conditions:
* $+$ and $\cdot$ are closed under $F$.
* $+$ and $\cdot$ are associative.
* $+$ and $\cdot$ are commutative.
* $+$ has an identity element denoted $0$ (Not necessarily the number 0, this is simply notation) and $\cdot$ has a <b><u>different</u></b> identity element denoted $1$ (Not necessarily the number 1).
* Every element $a \in F$ has an inverse element of $+$, denoted $-a$ (Additive Inverse).
* Every element $a \in F \setminus \{0\}$ has an inverse element of $\cdot$, denoted $\frac{1}{a}$ (Multiplicative Inverse).
* $\cdot$ is distributive over $+$.

If $F$, $+$, and $\cdot$ form a Field, one may write:
$\left(F, +, \cdot\right)$ is a Field.

$$
\begin{split}
	&\left(F, +, \cdot\right) \text{ is a Field } \iff \\
	&\forall a,b \in F: a + b \in F \land a \cdot b \in F \land \\
	&\forall a,b,c \in F: a + \left(b + c\right) = \left(a + b\right) + c \land \\
	&\forall a,b,c \in F: a \cdot \left(b \cdot c\right) = \left(a \cdot b\right) \cdot c \land \\
	&\forall a,b \in F: a + b = b + a \land a \cdot b = b \cdot a \land \\
	&\exists 0 \in F: \forall a \in F: a + 0 = 0 + a = a \land \\
	&\exists 1 \in F: 1 \neq 0 \land \forall a \in F: a \cdot 1 = 1 \cdot a = a \land \\
	&\forall a \in F: \exists \left(-a\right) \in F: a + \left(-a\right) = \left(-a\right) + a = 0 \land \\
	&\forall a \in F \setminus \{0\}: \exists \frac{1}{a} \in F: a \cdot \frac{1}{a} = \frac{1}{a} \cdot a = 1 \land \\
	&\forall a,b,c \in F: a \cdot \left(b + c\right) = \left(a \cdot b\right) + \left(a \cdot c\right)
\end{split}
$$

$a \cdot b$ is called the product of $a$ and $b$.

## Properties
Let $\left(F, +, \cdot\right)$ be a Field.

### Addition Forms a Group

One may notice that due to the following:
1. $+$ is closed under $F$.
2. $+$ is associative.
3. $+$ has an identity element.
4. Every element of $F$ has an inverse element of $+$.
5. $+$ is commutative.

Then $\left(F, +\right)$ is an abelian group.
<br/>
As a consequence: $\forall a \in F: -\left(-a\right) = a$.

### 0 Is An Absorbing Element Under Multiplication
Let $a \in F$:

$$
\begin{split}
	0 \cdot a &= \left(0 \cdot a\right) + 0 \\
	&= \left(0 \cdot a\right) + a + \left(-a\right) \\
	&= \left(0 \cdot a\right) + \left(1 \cdot a\right) + \left(-a\right) \\
	&= \left[\left(0 + 1\right) \cdot a\right] + \left(-a\right) \\
	&= \left(1 \cdot a\right) + \left(-a\right) \\
	&= a + \left(-a\right) \\
	&= 0
\end{split}
$$

### Zero Product Property

The zero product property of a field is:

$$
\label{eqn:zero_product_property}
\forall a, b \in F: a \cdot b = 0 \implies a = 0 \lor b = 0
$$

In order to prove this, one may prove the following:

$$
\label{eqn:product_not_zero}
\forall a, b \in F \land a,b \neq 0 \implies a \cdot b \neq 0
$$

This can be proved using proof by contradiction, assume that $\exists a,b \in F \land a,b \neq 0 \land a \cdot b = 0$.
Then:

$$
\begin{split}
	& a \cdot b = 0 \\
	& \Rightarrow \left(a \cdot b\right) \cdot \frac{1}{b} = 0 \cdot \frac{1}{b} \\
	& \Rightarrow a \cdot \left(b \cdot \frac{1}{b} \right) = 0 \\
	& \Rightarrow a \cdot 1 = 0 \\
	& \Rightarrow a = 0
\end{split}
$$

Which is a contradiction to one's assumption that $a \neq 0$.<br/>
Hence, $\eqref{eqn:product_not_zero}$ is true.<br/>
Therefore, By $\eqref{eqn:product_not_zero}$, if $a, b \in F$ and $a \cdot b = 0$ then either $a = 0$ or $b = 0$.
In other words: $\eqref{eqn:zero_product_property}$ is proved. $\blacksquare$

### Multiplication Without 0 Forms a Group

One may notice that:
1. Due to the zero product property, $\cdot$ is closed under $F \setminus \{0\}$
2. Because $\cdot$ is associative under $F$, it's also associative under $F \setminus \{0\}$
3. $\cdot$ has an identity element $1 \neq 0$, because of this, $1 \in F \setminus \{0\}$ and therefore, this is also an identity element under $F \setminus \{0\}$.
4. By the definition of a field, every element $a \in F \setminus \{0\}$ has a multiplicative inverse denoted $\frac{1}{a}$. This inverse element can't be equal to $0$ because $a \cdot \frac{1}{a} = 1$ and $0$ is an absorbing element.
5. $\cdot$ is commutative.

Hence, $\left(F \setminus \{0\}, \cdot\right)$ is an abelian group.
<br/>
As a consequence, by inverse element of an inverse element in a group: $\forall a \in F \setminus \{0\}: \frac{1}{\left(\frac{1}{a}\right)} = a$.

### The Identity and Inverse Elements

Because $\left(F, +\right)$ is a group, $0$ is the only identity element of $+$.
Moreover, $\left(-a\right)$ is the only
additive inverse of $a \in F$.
<br/>
Because $\left(F \setminus \{0\},\cdot \right)$ is a group, $1$ is the only identity element of $\cdot$.
Moreover, $\frac{1}{a}$ is the only
additive inverse of $a \in F \setminus \{0\}$.

### The Additive Inverse

One may observe that, by the definition of additive inverses: $1 + \left(-1\right) = 0$
Hence: $a \cdot \left[1 + \left(-1\right)\right] = a \cdot 0$.
Therefore: $\left(a \cdot 1\right) + \left(a \cdot \left(-1\right)\right) = 0$.
Which implies: $a + \left(a \cdot \left(-1\right)\right) = 0$.
One may then observe that $a + \left(-a\right) = 0$
and hence, By the singularity of the additive inverse element of $a$:

$$
\label{eqn:general_additive_inverse}
-a = \left(-1\right) \cdot a
$$

### 0 Has No Multiplicative Inverse

The definition of a field does not require that $0$ will have a multiplicative inverse. One may prove that it doesn't have one.
This can be proved using proof by contradiction, the statement $\exists \frac{1}{0} \in F: 0 \cdot \frac{1}{0} = 1$ contradicts the fact that $0$ is an absorbing element and hence, is false.

### Addition and Multiplication of Additive Inverses
Let $a, b \in F$.<br/>
Adding the additive inverses of $a$ and $b$ will result in:

$$
\begin{split}
	\left(-a\right) + \left(-b\right) &= \left[\left(-1\right) \cdot a\right] + \left[\left(-1\right) \cdot b\right] \\
	&= \left(-1\right) \cdot \left(a + b\right) \\
	&= - \left(a+b\right)
\end{split}
$$

In order to find the product of the additive inverses of $a$ and $b$, one may first compute the product of $-1$ with itself.

One may observe that: $1 + \left(-1\right) = 0$.
And thus, by $\eqref{eqn:general_additive_inverse}$: $\left[\left(-1\right) \cdot \left(-1\right)\right] + \left(-1\right) = 0$.
Hence, both $1$ and $\left(-1\right) \cdot \left(-1\right)$ are additive inverses of $-1$, and therefore, by the singularity of additive inverses: $\left(-1\right) \cdot \left(-1\right) = 1$.

Hence:

$$
\begin{split}
	\left(-a\right) \cdot \left(-b\right) &= \left(-1\right) \cdot a \cdot \left(-1\right) \cdot b \\
	&= \left(-1\right) \cdot \left(-1\right) \cdot a \cdot b \\
	&= 1 \cdot a \cdot b \\
	&= a \cdot b
\end{split}
$$

Furthermore:

$$
\begin{split}
	a \cdot \left(-b\right) &= a \cdot \left(-1\right) \cdot b \\
	&= \left(-1\right) \cdot a \cdot b \\
	&= -\left(a \cdot b\right)
\end{split}
$$

### Addition and Multiplication of Multiplicative Inverses
Let $a, b \in F \setminus \{0\}$.<br/>
Because $\left(F \setminus \{0\}, \cdot\right)$ is a group:

$$
\begin{split}
	\frac{1}{a \cdot b} &= \frac{1}{b} \cdot \frac{1}{a}
\end{split}
$$

Which is the product of the multiplicative inverses of $a$ and $b$.

Hence, adding the multiplicative inverses of $a$ and $b$ will result in:

$$
\begin{split}
	\frac{1}{a} + \frac{1}{b} &= \left(1 \cdot \frac{1}{a}\right) + \left(1 \cdot \frac{1}{b}\right) \\
	&= \left(b \cdot \frac{1}{b} \cdot \frac{1}{a}\right) + \left(a \cdot \frac{1}{a} \cdot \frac{1}{b}\right) \\
	&= \left(b \cdot \frac{1}{a \cdot b}\right) + \left(a \cdot \frac{1}{a \cdot b}\right) \\
	&= \left(b + a\right) \cdot \frac{1}{a \cdot b}
\end{split}
$$

## Ordered Field
A field $\left(F, +, \cdot\right)$ equipped with a strict total order $<$ on $F$ such that, $\forall a,b,c \in F$:
* $a < b \Rightarrow a + c < b + c$
* $0 < a \land 0 < b \Rightarrow 0 < a \cdot b$

Is called an Ordered Field.