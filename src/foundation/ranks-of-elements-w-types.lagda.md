# Ranks of elements in W-types

```agda
{-# OPTIONS --without-K --exact-split #-}

module foundation.ranks-of-elements-w-types where

open import foundation.cartesian-product-types using (_×_)
open import foundation.dependent-pair-types using (Σ; pair; pr1; pr2)
open import foundation.elementhood-relation-w-types using (_∈-𝕎_)
open import foundation.empty-types using
  ( empty; empty-Prop; is-empty; ex-falso)
open import foundation.existential-quantification using
  ( exists-Prop; exists; intro-exists; ∃; intro-∃)
open import foundation.identity-types using (tr; inv; refl)
open import foundation.inequality-w-types using
  ( _le-𝕎_; le-∈-𝕎; propagate-le-𝕎)
open import foundation.negation using (¬)
open import foundation.propositional-truncations using
  ( unit-trunc-Prop; apply-universal-property-trunc-Prop)
open import foundation.propositions using
  ( UU-Prop; Π-Prop; type-Prop; prod-Prop)
open import foundation.universe-levels using (Level; UU; _⊔_)
open import foundation.w-types using (𝕎; tree-𝕎; constant-𝕎; is-constant-𝕎)
```

## Idea

Consider two elements `x` and `y` of a W-type `𝕎 A B`. We say that the rank of `x` is at most the rank of `y` if for every element `x' ∈ x` and for every element `y' ∈ y` the rank of `x'` is at most the rank of `y'`.

## Definition

### Rank comparison

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  _≼-𝕎-Prop_ : 𝕎 A B → 𝕎 A B → UU-Prop (l1 ⊔ l2)
  (tree-𝕎 x α) ≼-𝕎-Prop (tree-𝕎 y β) =
    Π-Prop (B x) (λ b → exists-Prop (λ c → (α b) ≼-𝕎-Prop (β c)))

  _≼-𝕎_ : 𝕎 A B → 𝕎 A B → UU (l1 ⊔ l2)
  x ≼-𝕎 y = type-Prop (x ≼-𝕎-Prop y)

  _≈-𝕎-Prop_ : (x y : 𝕎 A B) → UU-Prop (l1 ⊔ l2)
  x ≈-𝕎-Prop y = prod-Prop (x ≼-𝕎-Prop y) (y ≼-𝕎-Prop x)

  _≈-𝕎_ : (x y : 𝕎 A B) → UU (l1 ⊔ l2)
  x ≈-𝕎 y = type-Prop (x ≈-𝕎-Prop y)

{-
  ≈-has-same-lower-set-≺-𝕎 :
    {x y : 𝕎 A B} → has-same-lower-set-≺-𝕎 x y → x ≈-𝕎 y
  ≈-has-same-lower-set-≺-𝕎 {x} {y} H = {!!}
-}
```

### Strict rank comparison

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  _≺-𝕎-Prop_ : 𝕎 A B → 𝕎 A B → UU-Prop (l1 ⊔ l2)
  x ≺-𝕎-Prop y =
    exists-Prop (λ (t : Σ (𝕎 A B) (λ w → w ∈-𝕎 y)) → x ≼-𝕎-Prop (pr1 t))

  _≺-𝕎_ : 𝕎 A B → 𝕎 A B → UU (l1 ⊔ l2)
  x ≺-𝕎 y = type-Prop (x ≺-𝕎-Prop y)

  in-lower-set-≺-𝕎-Prop : (x y : 𝕎 A B) → UU-Prop (l1 ⊔ l2)
  in-lower-set-≺-𝕎-Prop x y = y ≺-𝕎-Prop x

  in-lower-set-≺-𝕎 : (x y : 𝕎 A B) → UU (l1 ⊔ l2)
  in-lower-set-≺-𝕎 x y = y ≺-𝕎 x

  has-same-lower-set-≺-𝕎 : (x y : 𝕎 A B) → UU (l1 ⊔ l2)
  has-same-lower-set-≺-𝕎 x y = (z : 𝕎 A B) → (z ≺-𝕎 x) × (z ≺-𝕎 y)
```

### Strong rank comparison

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  _strong-≼-𝕎-Prop_ : 𝕎 A B → 𝕎 A B → UU-Prop (l1 ⊔ l2)
  x strong-≼-𝕎-Prop y =
    Π-Prop
      ( 𝕎 A B)
      ( λ u →
        Π-Prop
          ( u ∈-𝕎 x)
          ( λ H →
            exists-Prop
              ( λ (v : 𝕎 A B) →
                exists-Prop (λ (K : v ∈-𝕎 y) → u ≼-𝕎-Prop v))))

  _strong-≼-𝕎_ : 𝕎 A B → 𝕎 A B → UU (l1 ⊔ l2)
  x strong-≼-𝕎 y = type-Prop (x strong-≼-𝕎-Prop y)
```

## Properties

### Reflexivity of rank comparison

```
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  refl-≼-𝕎 : (x : 𝕎 A B) → x ≼-𝕎 x
  refl-≼-𝕎 (tree-𝕎 x α) b = unit-trunc-Prop (pair b (refl-≼-𝕎 (α b)))
```

### Transitivity of rank comparison

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  transitive-≼-𝕎 : {x y z : 𝕎 A B} → (x ≼-𝕎 y) → (y ≼-𝕎 z) → (x ≼-𝕎 z)
  transitive-≼-𝕎 {tree-𝕎 x α} {tree-𝕎 y β} {tree-𝕎 z γ} H K a =
    apply-universal-property-trunc-Prop
      ( H a)
      ( exists-Prop (λ c → (α a) ≼-𝕎-Prop (γ c)))
      ( λ t →
        apply-universal-property-trunc-Prop
          ( K (pr1 t))
          ( exists-Prop (λ c → (α a) ≼-𝕎-Prop (γ c)))
          ( λ s →
            unit-trunc-Prop
              ( pair
                ( pr1 s)
                ( transitive-≼-𝕎
                  { α a}
                  { β (pr1 t)}
                  { γ (pr1 s)}
                  ( pr2 t)
                  ( pr2 s)))))
```

### Rank comparison is equivalent to strong rank comparison

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  strong-≼-≼-𝕎 : {x y : 𝕎 A B} → (x ≼-𝕎 y) → (x strong-≼-𝕎 y)
  strong-≼-≼-𝕎 {tree-𝕎 x α} {tree-𝕎 y β} H .(α b) (pair b refl) =
    apply-universal-property-trunc-Prop (H b)
      ( exists-Prop ((λ v → exists-Prop (λ hv → (α b) ≼-𝕎-Prop v))))
      ( f)
      where
      f : Σ (B y) (λ c → pr1 (α b ≼-𝕎-Prop β c)) →
          exists (λ v → exists-Prop (λ hv → α b ≼-𝕎-Prop v))
      f (pair c K) =
        intro-exists
          ( λ v → exists-Prop (λ hv → α b ≼-𝕎-Prop v))
          ( β c)
          ( intro-exists
            ( λ hβc → α b ≼-𝕎-Prop β c)
            ( pair c refl)
            ( K))

  ≼-strong-≼-𝕎 : {x y : 𝕎 A B} → (x strong-≼-𝕎 y) → (x ≼-𝕎 y)
  ≼-strong-≼-𝕎 {tree-𝕎 x α} {tree-𝕎 y β} H b =
    apply-universal-property-trunc-Prop
      ( H (α b) (pair b refl))
      ( exists-Prop (λ c → α b ≼-𝕎-Prop β c))
      ( f)
    where
    f : Σ ( 𝕎 A B) (λ v → exists (λ K → α b ≼-𝕎-Prop v)) →
        exists (λ c → α b ≼-𝕎-Prop β c)
    f (pair v K) =
        apply-universal-property-trunc-Prop K
          ( exists-Prop (λ c → α b ≼-𝕎-Prop β c))
          ( g)
      where
      g : (v ∈-𝕎 tree-𝕎 y β) × (α b ≼-𝕎 v) → ∃ (λ c → α b ≼-𝕎 β c)
      g (pair (pair c p) M) = intro-∃ c (tr (λ t → α b ≼-𝕎 t) (inv p) M)
```

### If `x ∈ y` then the rank of `x` is at most the rank of `y`

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  ≼-∈-𝕎 : {x y : 𝕎 A B} → (x ∈-𝕎 y) → (x ≼-𝕎 y)
  ≼-∈-𝕎 {tree-𝕎 x α} {tree-𝕎 y β} (pair v p) u =
    intro-exists
      ( λ z → α u ≼-𝕎-Prop β z)
      ( v)
      ( tr ( λ t → α u ≼-𝕎 t)
           ( inv p)
           ( ≼-∈-𝕎 {α u} {tree-𝕎 x α} (pair u refl)))
```

### If `x ∈ y` then the rank of `x` is strictly lower than the rank of `y`

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  ≼-le-𝕎 : {x y : 𝕎 A B} → (x le-𝕎 y) → (x ≼-𝕎 y)
  ≼-le-𝕎 {x} {y} (le-∈-𝕎 H) = ≼-∈-𝕎 H
  ≼-le-𝕎 {x} {y} (propagate-le-𝕎 {y = y'} K H) =
    transitive-≼-𝕎 {x = x} {y = y'} {y} (≼-le-𝕎 H) (≼-∈-𝕎 K)
```

### If `x ∈ y` then the rank of `y` is not lower than the rank of `x`

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  not-≼-∈-𝕎 : {x y : 𝕎 A B} → (x ∈-𝕎 y) → ¬ (y ≼-𝕎 x)
  not-≼-∈-𝕎 {tree-𝕎 x α} {tree-𝕎 y β} (pair b p) K =
    apply-universal-property-trunc-Prop (K b) (empty-Prop) f
    where
    f : Σ (B x) (λ c → β b ≼-𝕎 α c) → empty
    f (pair c L) =
      not-≼-∈-𝕎 {α c} {β b} (tr (λ t → α c ∈-𝕎 t) (inv p) (pair c refl)) L
```

### If `x ∈ y` then the rank of `y` is not strictly below the rank of `x`

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  not-≼-le-𝕎 : {x y : 𝕎 A B} → (x le-𝕎 y) → ¬ (y ≼-𝕎 x)
  not-≼-le-𝕎 {x} {y} (le-∈-𝕎 H) = not-≼-∈-𝕎 {x = x} {y} H
  not-≼-le-𝕎 {x} {y} (propagate-le-𝕎 {y = y'} H K) L =
    not-≼-∈-𝕎 {x = y'} {y} H (transitive-≼-𝕎 {x = y} {x} {y'} L (≼-le-𝕎 K))
```

### Constants are elements of least rank

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  is-least-≼-constant-𝕎 :
    {x : A} (h : is-empty (B x)) (w : 𝕎 A B) → constant-𝕎 x h ≼-𝕎 w
  is-least-≼-constant-𝕎 h (tree-𝕎 y β) x = ex-falso (h x)

  is-least-≼-is-constant-𝕎 :
    {x : 𝕎 A B} → is-constant-𝕎 x → (y : 𝕎 A B) → x ≼-𝕎 y
  is-least-≼-is-constant-𝕎 {tree-𝕎 x α} H (tree-𝕎 y β) z =
    ex-falso (H z)

  is-constant-is-least-≼-𝕎 :
    {x : 𝕎 A B} → ((y : 𝕎 A B) → x ≼-𝕎 y) → is-constant-𝕎 x
  is-constant-is-least-≼-𝕎 {tree-𝕎 x α} H b =
    not-≼-∈-𝕎 {x = α b} {tree-𝕎 x α} (pair b refl) (H (α b))
```

### If the rank of `x` is strictly below the rank of `y`, then the rank of `x` is at most the rank of `y`

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  ≼-≺-𝕎 : {x y : 𝕎 A B} → (x ≺-𝕎 y) → (x ≼-𝕎 y)
  ≼-≺-𝕎 {x} {y} H =
    apply-universal-property-trunc-Prop H (x ≼-𝕎-Prop y) f
    where
    f : Σ (Σ (𝕎 A B) (λ w → w ∈-𝕎 y)) (λ t → x ≼-𝕎 pr1 t) → (x ≼-𝕎 y)
    f (pair (pair w K) L) = transitive-≼-𝕎 {x = x} {w} {y} L (≼-∈-𝕎 K)
```

### Strict rank comparison is transitive

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  transitive-≺-𝕎 : {x y z : 𝕎 A B} → (x ≺-𝕎 y) → (y ≺-𝕎 z) → (x ≺-𝕎 z)
  transitive-≺-𝕎 {x} {y} {z} H K =
    apply-universal-property-trunc-Prop H (x ≺-𝕎-Prop z) f
    where
    f : Σ (Σ (𝕎 A B) (λ w → w ∈-𝕎 y)) (λ t → x ≼-𝕎 pr1 t) → x ≺-𝕎 z
    f (pair (pair w L) M) =
      apply-universal-property-trunc-Prop K (x ≺-𝕎-Prop z) g
      where
      g : Σ (Σ (𝕎 A B) (λ w → w ∈-𝕎 z)) (λ t → y ≼-𝕎 pr1 t) → x ≺-𝕎 z
      g (pair (pair v P) Q) =
        intro-exists
          ( λ (t : Σ (𝕎 A B) (λ s → s ∈-𝕎 z)) → x ≼-𝕎-Prop (pr1 t))
          ( pair v P)
          ( transitive-≼-𝕎 {x = x} {w} {v} M
            ( transitive-≼-𝕎 {x = w} {y} {v} (≼-∈-𝕎 L) Q))
```

### Strict rank comparison is irreflexive

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  irreflexive-≺-𝕎 : {x : 𝕎 A B} → ¬ (x ≺-𝕎 x)
  irreflexive-≺-𝕎 {tree-𝕎 x α} H =
    apply-universal-property-trunc-Prop H empty-Prop f
    where
    f : ¬ ( Σ ( Σ (𝕎 A B) (λ w → w ∈-𝕎 tree-𝕎 x α))
              ( λ t → tree-𝕎 x α ≼-𝕎 pr1 t))
    f (pair (pair w K) L) = not-≼-∈-𝕎 {x = w} {tree-𝕎 x α} K L
```
