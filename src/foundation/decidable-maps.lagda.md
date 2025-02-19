# Decidable maps

```agda
{-# OPTIONS --without-K --exact-split #-}

module foundation.decidable-maps where

open import foundation.decidable-equality using (has-decidable-equality)
open import foundation.decidable-types using
  ( is-decidable; is-decidable-iff)
open import foundation.dependent-pair-types using (Σ; pair; pr1; pr2)
open import foundation.fibers-of-maps using (fib)
open import foundation.functions using (_∘_)
open import foundation.identity-types using (Id; ap; inv; _∙_)
open import foundation.retractions using (retr)
open import foundation.universe-levels using (Level; UU; _⊔_)
```

## Definition

A map is said to be decidable if its fibers are decidable types.

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : UU l2}
  where

  is-decidable-map : (A → B) → UU (l1 ⊔ l2)
  is-decidable-map f = (y : B) → is-decidable (fib f y)
```

```agda
is-decidable-map-retr :
  {l1 l2 : Level} {A : UU l1} {B : UU l2} → has-decidable-equality B →
  (i : A → B) → retr i → is-decidable-map i
is-decidable-map-retr d i (pair r R) b =
  is-decidable-iff
    ( λ (p : Id (i (r b)) b) → pair (r b) p)
    ( λ t → ap (i ∘ r) (inv (pr2 t)) ∙ (ap i (R (pr1 t)) ∙ pr2 t))
    ( d (i (r b)) b)
```
