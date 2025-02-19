# Equational reasoning

Tom de Jong, 27 May 2022.
Elisabeth Bonnevier, 31 May 2022.
```agda
{-# OPTIONS --without-K --exact-split #-}

module foundation.equational-reasoning where

open import foundation.identity-types using (Id ; refl ; _∙_; inv)
open import foundation.equivalences using (_≃_ ; _∘e_ ; id-equiv; inv-equiv)
open import foundation.universe-levels using (Level; UU)
open import order-theory.preorders using
  (Preorder ; element-Preorder ; leq-Preorder
  ; transitive-leq-Preorder ; refl-leq-Preorder)
```

## Idea

Often it's convenient to reason by chains of (in)equalities or equivalences,
i.e. to write a proof in the following form:

```md
X ≃⟨ equiv-1 ⟩
A ≃⟨ equiv-2 ⟩
B ≃⟨ equiv-3 ⟩
Y ∎
```

or
```md
x ≤⟨ ineq-1 ⟩
a ≤⟨ ineq-2 ⟩
b ≤⟨ ineq-3 ⟩
c ∎
```

where `equiv-x` and `ineq-x` are proofs of respectively the equivalences or
inequalities. The symbol ∎ marks the end of a chain.

Because we will want to have equational reasoning for both identifications and
equivalences and we can't use the same symbol twice, we use ∎ for
identifications and ■ for equivalences in the code below.

For inequalities we also need to pass the preorder as an argument.

We write Agda code that allows for such reasoning. The code for equational
reasoning for equalities and equivalences is based on Martín Escardó's Agda code
[1,2] and the Agda standard library [3].


## Definitions

### Equational reasoning for identifications

```agda
infix 1 _∎
infixr 0 step-= step-=˘

step-= : {l : Level} {X : UU l} (x : X) {y z : X}
       → Id y z → Id x y → Id x z
step-= _ q p = p ∙ q

step-=˘ : {l : Level} {X : UU l} (x : X) {y z : X}
        → Id y z → Id y x → Id x z
step-=˘ _ q p = inv p ∙ q

_∎ : {l : Level} {X : UU l} (x : X) → Id x x
x ∎ = refl

syntax step-= x q p = x =⟨ p ⟩ q
syntax step-=˘ x q p = x =˘⟨ p ⟩ q
```

### Equational reasoning for equivalences

```agda
infix 1 _■
infixr 0 step-≃ step-≃˘

step-≃ : {l1 l2 l3 : Level} (X : UU l1) {Y : UU l2 } {Z : UU l3}
       → Y ≃ Z → X ≃ Y → X ≃ Z
step-≃ _ g f = g ∘e f

step-≃˘ : {l1 l2 l3 : Level} (X : UU l1) {Y : UU l2 } {Z : UU l3}
        → Y ≃ Z → Y ≃ X → X ≃ Z
step-≃˘ _ g f = g ∘e inv-equiv f

_■ : {l : Level} (X : UU l) → X ≃ X
X ■ = id-equiv

syntax step-≃ X g f = X ≃⟨ f ⟩ g
syntax step-≃˘ X g f = X ≃˘⟨ f ⟩ g
```

### Equational reasoning for preorders

```agda
private
 transitivity : {l1 l2 : Level} (X : Preorder l1 l2)
                (x : element-Preorder X) {y z : element-Preorder X}
              → leq-Preorder X x y → leq-Preorder X y z → leq-Preorder X x z
 transitivity X x {y} {z} u v = transitive-leq-Preorder X x y z v u

syntax transitivity X x u v = x ≤⟨ X ⟩[ u ] v
infixr 0 transitivity

private
 reflexivity : {l1 l2 : Level} (X : Preorder l1 l2)
             → (x : element-Preorder X) → leq-Preorder X x x
 reflexivity = refl-leq-Preorder

syntax reflexivity X x = x ∎⟨ X ⟩
infix 1 reflexivity
```

For a preorder `X` we thus write the chains as follows

```md
x ≤⟨ X ⟩[ ineq-1 ]
y ≤⟨ X ⟩[ ineq-2 ]
z ∎⟨ X ⟩
```

## References

1. Martín Escardó. https://github.com/martinescardo/TypeTopology/blob/master/source/Id.lagda
2. Martín Escardó. https://github.com/martinescardo/TypeTopology/blob/master/source/UF-Equiv.lagda
3. The Agda standard library. https://github.com/agda/agda-stdlib/blob/master/src/Relation/Binary/PropositionalEquality/Core.agda
