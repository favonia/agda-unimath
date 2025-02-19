# Embeddings

```agda
{-# OPTIONS --without-K --exact-split #-}

module foundation-core.embeddings where

open import foundation-core.dependent-pair-types using (Σ; pair; pr1; pr2)
open import foundation-core.equivalences using
  ( is-equiv; _≃_; is-equiv-htpy; is-equiv-id)
open import foundation-core.functions using (id)
open import foundation-core.identity-types using
  ( Id; refl; ap; inv; _∙_; ap-id)
open import foundation-core.universe-levels using (Level; UU; _⊔_)
```

## Idea

An embedding from one type into another is a map that induces equivalences on identity types. In other words, the identitifications `Id (f x) (f y)` for an embedding `f : A → B` are in one-to-one correspondence with the identitifications `Id x y`. Embeddings are better behaved homotopically than injective maps, because the condition of being an equivalence is a property under function extensionality.

## Definition

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : UU l2}
  where

  is-emb : (A → B) → UU (l1 ⊔ l2)
  is-emb f = (x y : A) → is-equiv (ap f {x} {y})

_↪_ :
  {l1 l2 : Level} → UU l1 → UU l2 → UU (l1 ⊔ l2)
A ↪ B = Σ (A → B) is-emb

module _
  {l1 l2 : Level} {A : UU l1} {B : UU l2}
  where

  map-emb : A ↪ B → A → B
  map-emb f = pr1 f

  is-emb-map-emb : (f : A ↪ B) → is-emb (map-emb f)
  is-emb-map-emb f = pr2 f

  equiv-ap-emb : (e : A ↪ B) {x y : A} → Id x y ≃ Id (map-emb e x) (map-emb e y)
  pr1 (equiv-ap-emb e {x} {y}) = ap (map-emb e)
  pr2 (equiv-ap-emb e {x} {y}) = is-emb-map-emb e x y
```

## Examples


### The identity map is an embedding

```agda
module _
  {l : Level} {A : UU l}
  where

  is-emb-id : is-emb (id {A = A})
  is-emb-id x y = is-equiv-htpy id ap-id is-equiv-id

  id-emb : A ↪ A
  pr1 id-emb = id
  pr2 id-emb = is-emb-id
```

### To prove that a map is an embedding, a point in the domain may be assumed

```agda
module _
  {l : Level} {A : UU l} {l2 : Level} {B : UU l2} {f : A → B}
  where
  
  abstract
    is-emb-is-emb : (A → is-emb f) → is-emb f
    is-emb-is-emb H x y = H x x y
```
