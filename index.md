---
title: Home
layout: home
math: mathjax
nav_order: 1

---

<style>
    mjx-container {text-align: left !important;}
</style>

![](/imgs/logo-navbar.png)

### A formal specification

---

## §1. The Manifold

Let
$$\mathcal{M}$$
denote a continuous *Manifold* with
$$dim(\mathcal{M}) \ge 5$$
.

$$\mathcal{M}$$
is the embedding space of all possible realisations.

## §2. Submanifolds

Let
$$m_i \subset \mathcal{M}$$
denote a connected embedded *Sub-manifold* with 
$$\dim(m_i) < dim(\mathcal{M})$$
.

$$m_i$$
is a realisation with locally coherent spaces.

Realisations are generally pairwise disjoint:
$$m_i \cap m_j = \varnothing \quad \text{for } i \ne j$$

*Submanifolds* <ins>cannot</ins> be ordered.



## §3. Phases

A *Phase* in $$m_i$$ is the ordered pair
$$
\Phi_i^\alpha = (m_i,\Delta t_\alpha)
$$

Each
$$\Phi_i^\alpha$$
is a bounded spatiotemporal regime.


For distinct Phases
$$\Phi_i^\alpha$$
and
$$\Phi_i^\beta$$
their spatiotemporal intervals are (mostly) disjoint:
$$
\Delta t_\alpha \cap \Delta t_\beta = \varnothing
\quad \text{for } \alpha \ne \beta
$$

*Phases* <ins>may</ins> be ordered.

## §4. Observations

An *Observation* in
$$
\Phi_i^\alpha
$$
is a temporal sample of a *Phase*:
$$
O_i^{\alpha,k} = (\Phi_i^\alpha | [t_i^k,t_f^k])
$$

*Observations* <ins>must</ins> ordered.



{% comment %}


## §5. Strata

*Strata* are separate conditions for *Submanifolds* and *Phases*.

For any points 
$$p \in m_i \text{, } q \in m_j$$
with
$$i \ne j$$ and
$$r \in \Phi_k^\alpha \text{, } s \in \Phi_l^\alpha$$
with
$$k \ne l$$

$$
\operatorname{Sep}(p,q) > 0
$$

where $\operatorname{Sep}$ is induced by the Stratum field $S$ and ambient metric structure.

Equivalently, manifolds remain isolated when

$$
S(x) \gg 0
$$

in regions between them.

## §6. Anchors

Let

$$
A \subset \mathcal{M}
$$

be an Anchor.

A Phase $\Phi_i^\alpha$ is **incident to** $A$ if there exists some Observation time $t_k$ and some spatial region $U \subset m_i$ such that

$$
U \cap (A \cap m_i) \ne \varnothing
$$

during the interval $\Delta t_\alpha$.

---

## §10. Phase Support

The **support** of a Phase is the spacetime region

$$
\operatorname{Supp}(\Phi_i^\alpha) = m_i \times [t_0^\alpha,t_1^\alpha]
$$

or, if desired, a more localized subset

$$
\operatorname{Supp}(\Phi_i^\alpha) = U_i^\alpha \times [t_0^\alpha,t_1^\alpha]
$$

where

$$
U_i^\alpha \subseteq m_i
$$

is the spatial domain relevant to that Phase.

---

## §11. Phase Ordering

Phases in a given Submanifold inherit a total order from local time:

$$
\Phi_i^\alpha \prec \Phi_i^\beta
\quad \Longleftrightarrow \quad
t_1^\alpha < t_0^\beta
$$

---

## §12. Axiomatic Summary

1. A Submanifold is an embedded spacetime $m_i \subset \mathcal{M}$.
2. A Phase is a bounded temporal regime of a Submanifold:
   $$
   \Phi_i^\alpha = (m_i,[t_0^\alpha,t_1^\alpha])
   $$
3. Distinct Phases in the same Submanifold are temporally disjoint.
4. An Observation is a temporal sample of a Phase:
   $$
   O_i^{\alpha,k} = (m_i,t_k)
   $$
5. A Phase may be associated with one or more Anchors through spatial incidence.
6. Phases are ordered by local time within each Submanifold.







## §3. Structural Fields on $\mathcal{M}$

Define the following scalar fields on $\mathcal{M}$:

### 1. Stratum Field (Order)

$$
S:\mathcal{M}\rightarrow \mathbb{R}_{\ge 0}
$$

### 2. Chaos Field

$$
\chi:\mathcal{M}\rightarrow \mathbb{R}_{\ge 0}
$$

### 3. Petroleum Field (Resonant Field)

$$
P:\mathcal{M}\rightarrow \mathbb{R}_{\ge 0}
$$

Each manifold inherits restricted fields:

$$
S_i = S|_{m_i}, \quad
\chi_i = \chi|_{m_i}, \quad
P_i = P|_{m_i}
$$

---

## §4. Stratum Separation Condition

Define the **Separation Condition** for manifolds:

For any points $p \in m_i$, $q \in m_j$ with $i \ne j$,

$$
\operatorname{Sep}(p,q) > 0
$$

where $\operatorname{Sep}$ is induced by the Stratum field $S$ and ambient metric structure.

Equivalently, manifolds remain isolated when

$$
S(x) \gg 0
$$

in regions between them.

---

## §5. Thinness Functional

Define the **Thinness Function**

$$
\Theta : \mathcal{M} \rightarrow \mathbb{R}_{\ge 0}
$$

by

$$
\Theta(x) = \frac{\chi(x)\, P(x)}{1 + S(x)}
$$

---

## §6. Thin Regions

A point $x \in \mathcal{M}$ is **thin** if

$$
\Theta(x) > \kappa
$$

for fixed threshold $\kappa > 0$.

A connected region

$$
U \subset \mathcal{M}
$$

is a **Thin Region** if

$$
\inf_{x \in U} \Theta(x) > \kappa
$$

---

## §7. Ambient Proximity

Let $d_{\mathcal{M}}$ denote a metric (or generalized distance) on $\mathcal{M}$.

For points $p \in m_i$, $q \in m_j$, define proximity kernel

$$
K(p,q) = e^{-\lambda d_{\mathcal{M}}(p,q)}
$$

for constant $\lambda > 0$.

---

## §8. Cross-Manifold Coupling

The coupling intensity between $p \in m_i$ and $q \in m_j$ is

$$
C(p,q) = K(p,q)\,\Theta(p)\,\Theta(q)
$$

Cross-manifold interaction is possible when

$$
C(p,q) > \epsilon
$$

for some threshold $\epsilon > 0$.

---

## §9. Localized Identification (Portal Event)

Let $U \subset m_i$, $V \subset m_j$ be open subsets.

A **Portal Event** occurs if there exists a diffeomorphic identification

$$
\pi: U \rightarrow V
$$

such that

$$
\forall x \in U, \quad C(x,\pi(x)) > \epsilon
$$

and

$$
U \cup V \subset \{x \in \mathcal{M} \mid \Theta(x) > \kappa\}
$$

Portal events are transient and exist only while the above inequalities hold.

---

## §10. Petroleum Invariance

Petroleum is defined on $\mathcal{M}$ rather than intrinsically on each manifold.

For all $i,j$,

$$
P_i = P|_{m_i}, \quad
P_j = P|_{m_j}
$$

Petroleum continuity across manifolds is given by continuity of $P$ on $\mathcal{M}$.

---

## §11. Stability Regime

Manifold isolation is stable when

$$
S(x) \gg \chi(x)\,P(x)
$$

for all $x$ in regions between manifolds.

Bleed becomes possible when

$$
\chi(x)\,P(x) \gtrsim S(x)
$$

locally.

---

## §12. Axiomatic Summary

1. $\mathcal{M}$ is an ambient topological space.  
2. Worlds are embedded manifolds $m_i \subset \mathcal{M}$.  
3. Manifolds are disjoint under normal conditions.  
4. The Stratum field $S$ enforces separation.  
5. The Chaos field $\chi$ drives cross-manifold pressure.  
6. Petroleum field $P$ enables coupling.  
7. Thinness is determined by $\Theta = \frac{\chi P}{1+S}$.  
8. Cross-manifold interaction occurs only in thin regions with sufficient ambient proximity.

{% endcomment %}