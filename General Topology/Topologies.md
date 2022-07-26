# [[Topologies]]

## Definitions

Let $X$ be any set, and let $\mathcal T$ be a collection of some subsets of $X$, i.e., $\mathcal T \subseteq \mathcal P(X)$.

#### Definition 1 (Via Open Set Axioms)

$\mathcal T$ is a **topology** on $X$ if and only if it satisfies **Open Set Axioms**:

1. $X \in \mathcal T$;

2. $\mathcal T$ is closed under arbitrary union; i.e., for any $\mathcal A \subseteq \mathcal T$, $\bigcup \mathcal A \in \mathcal T$.

3. $\mathcal T$ is closed under finite intersection; i.e., for any finite $\mathcal F \subseteq \mathcal T$, $\bigcap \mathcal F \in \mathcal T$.

Some authors also count $\emptyset \in \mathcal T$ in Open Set Axioms, but, rigorously, it can be deduced by Open Set Axiom 2 or 3. As $\emptyset$ is the subset of any set, $\emptyset \in \mathcal T$. And as $\emptyset = \bigcup \mathcal \emptyset$, by Open Set Axiom 2, $\emptyset \in \mathcal T$.


#### Definition 2 (Via Bases of Sets)

$\mathcal T$ is a **topology** on $X$ if and only if there is a $\mathcal B$ being a [[Bases of Sets#Definition|basis]] of $X$, such that $\mathcal T$ is [[Bases of Sets#Generated Collection|generated]] by $\mathcal B$. Explicitly, that is,

$$
\mathcal T = \left\{ \bigcup\mathcal A : \mathcal A \subseteq \mathcal B \right\}.
$$

#### Topological Space

In the above situation, the ordered pair $(X, \mathcal T)$ is a **topological space**.

#### Open Sets

In the above situation, a subset $U \subseteq X$ is said to be **open** if and only if $U \in \mathcal T$.

In the term of metric space, if $(X, \rho)$ is a [[Metric Spaces|metric space]], then $U$ is open if and only if for any for any $x \in U$, there is a $\delta \in \mathbb R_{> 0}$, such that $B(x, \delta) \subseteq U$. Equivalently, that is, $U$ is a union of some [[Metric Spaces#Balls|open balls]].

#### Closed Sets

In the above situation, a subset $V \subseteq X$ is said to be **closed** if and only if there is an open $U \subseteq X$, such that $V$ is the complement of $U$ in $X$, i.e., $V = X \setminus U$.

In a [[Metric Spaces|metric space]] $(X, \rho)$, a subset $V \subseteq X$ is closed if and only if $V$ is an intersection of some [[Metric Spaces#Balls|closed balls]]. Equivalently, that is, for any $x$ in the complement of $V$ in $X$, there is a $\delta \in \mathbb R_{> 0}$, such that $B(x, \delta) \subseteq X \setminus V$.


## Proof of Equivalence of the Definitions of Topologies on Sets

**Definition 1 implies 2**

Assume $\mathcal T$ is a topology on $X$, then $\mathcal T$ is a [[Bases of Sets|basis]] of $X$. (See [[Bases of Sets#Topologies are Bases|this]].)

Let $\mathcal T'$ be [[Bases of Sets#Topologies Generated by Bases|generated]] by $\mathcal T$, i.e., $\mathcal T' = \left\{ \bigcup \mathcal A: \mathcal A \subseteq \mathcal B \right\}$.

Let $U \in \mathcal T'$. Then, there is and $\mathcal A \subseteq \mathcal T$, such that $U = \bigcup \mathcal A$. As $\mathcal T$ satisfies [[Topologies#Definition 1 Via Open Set Axioms|Open Axiom 2]], $U \in \mathcal T$. Thus, $\mathcal T' \subseteq \mathcal T$.

By the assumption, for any $V \in \mathcal T$, $\bigcup \{U\} \in \mathcal T'$. Thus, $\mathcal T \subseteq \mathcal T'$.

Therefore, $\mathcal T' = \mathcal T$, which implies that $\mathcal T$ is a [[Bases of Sets|basis]] generates $\mathcal T$ itself.

$\Box$

**Definition 2 implies 1**

Let $\mathcal B$ be a [[Bases of Sets|basis]] of $X$, and assume $\mathcal T$ is a collection [[Bases of Sets#Topologies Generated by Bases|generated]] by $\mathcal B$. Then, $\mathcal T$ is a topology on $X$. (See [[Bases of Sets#Topologies Generated by Bases|this]]).

$\blacksquare$

## Comparison of Topologies

Let $X$ be any set, and let $\mathcal T, \mathcal T'$ be topologies on $X$. $\mathcal T$ is said to be **finer** than $\mathcal T'$, or $\mathcal T'$ is said to be **coarser** than $\mathcal T$, if and only if $\mathcal T' \subseteq \mathcal T$.

## Examples of Topological Spaces

#### Discrete Topologies

Let $X$ be any set. The power set $\mathcal P(X)$ itself is a topology on $X$, called **discrete topology** on $X$. As any topology $\mathcal T$ on $X$ is a subset of $\mathcal P(X)$, the discrete topology $\mathcal P(X)$ is the finest topology on $X$.

#### Indiscrete Topologies

Let $X$ be any set. The coarsest topology on $X$ is $\{\emptyset, X\}$, called **indiscrete topology**, or **trivial topology**, on $X$.

#### Metric Spaces

It is a straight corollary, by [[Topologies#Definition 2 Via Bases of Sets|the alternative definition of topologes]], that "[[Metric Spaces|metric spaces]] are topological spaces". Rigorously, that is, for any [[Metric Spaces|metric space]] $(X, \rho)$, if $\mathcal O$ is the collection of all [[Metric Spaces#Balls|open balls]] in the space, then $\mathcal O$, as it is a [[Bases of Sets|basis]] of $X$ (see [[Metric Spaces#Basis Induced by Metric|this]]), it generates a topology $\mathcal T$ for $X$.