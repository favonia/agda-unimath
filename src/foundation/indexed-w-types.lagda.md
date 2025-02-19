# Indexed W-types

```agda
{-# OPTIONS --without-K --exact-split #-}

module foundation.indexed-w-types where

open import foundation.universe-levels using (Level; UU; _⊔_)
```

```agda
data
  i𝕎
    {l1 l2 l3 : Level} (I : UU l1) (A : I → UU l2) (B : (i : I) → A i → UU l3)
    (f : (i : I) (x : A i) → B i x → I) (i : I) :
    UU (l2 ⊔ l3) where
  tree-i𝕎 : (x : A i) (α : (y : B i x) → i𝕎 I A B f (f i x y)) → i𝕎 I A B f i
```
