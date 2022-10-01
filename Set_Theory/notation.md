Let $A$ and $B$ be two statements, $x$ and $y$ be used to represent variables and $T\left(x\right)$ and $P\left(x\right)$ be statements that depend on $x$.



| Symbol            | Name           | Explanation                                                  |
| ----------------- | -------------- | ------------------------------------------------------------ |
| $\Longrightarrow$ | Implies        | The statement: $A \Longrightarrow B$ means:<br />If $A$ is true then $B$ is necessarily true but if $A$ is false then $B$ is not necessarily false. |
| $\lnot$           | Negation       | The statement $\lnot A$ is true only if $A$ is false.        |
| $\land$           | And            | The statement $A \land B$ is true only if both $A$ and $B$ are true. |
| $\iff$            | If and only if | The statement $A \iff B$ means that $A$ and $B$ are equivalent ( $A \Longrightarrow B \land B \Longrightarrow A$ ) |
| $\lor$            | Or             | The statement $A \lor B$ is true only if $A$ is true, or $B$ is true, or both. |
| $\forall$         | For All        | The statement $\forall x: P\left(x\right) \Longrightarrow T\left(x\right)$ means that for every $x$ such that $P\left(x\right)$ is true, the statement $T\left(x\right)$ is true. |
| $\exists$         | Exists         | The statement $\exists x: T\left(x\right)$ means that there exists at least one $x$ such that $T\left(x\right)$ is true. |
| $=$               | Equals         | The statement $x = y$ means that $x$ is equal to $y$.        |



## Abbreviations

| Symbol            | Name               | Definition                                                   |
| ----------------- | ------------------ | ------------------------------------------------------------ |
| $\exists!$        | Exists Exactly One | $\left[ \exists! x: P\left(x\right) \right] \iff \left[ \exists x: \forall y: P\left(y\right) \Rightarrow y = x\right]$ |
| $\not\exists$     | Not Exists         | $\not\exists x: P\left(x\right) \iff \lnot\left( \exists x: P\left(x\right) \right)$ |
| $\veebar, \oplus$ | Exclusive Or       | $A \veebar B \iff \left[ A \lor B \right] \land \lnot \left[ A \land B \right]$ |
| $\neq$            | Not equals         | $x \neq y \iff \lnot\left( x = y \right)$                    |