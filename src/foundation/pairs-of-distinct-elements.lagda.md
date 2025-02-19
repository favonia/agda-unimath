---
title: Pairs of distinct elements
---

```agda
{-# OPTIONS --without-K --exact-split #-}

module foundation.pairs-of-distinct-elements where

open import foundation.cartesian-product-types using (_×_)
open import foundation.contractible-types using (is-contr; is-contr-total-path)
open import foundation.dependent-pair-types using (Σ; pair; pr1; pr2)
open import foundation.embeddings using
  ( _↪_; map-emb; equiv-ap-emb; is-emb; is-emb-map-emb; emb-Σ)
open import foundation.equivalences using
  ( _≃_; map-equiv; is-equiv-map-equiv; is-equiv; map-inv-is-equiv;
    map-inv-equiv; is-equiv-map-inv-equiv; issec-map-inv-equiv;
    isretr-map-inv-equiv; is-equiv-has-inverse; emb-equiv)
open import foundation.fundamental-theorem-of-identity-types using
  ( fundamental-theorem-id)
open import foundation.identity-types using (Id; refl)
open import foundation.injective-maps using (is-injective-is-equiv)
open import foundation.negation using (¬; is-prop-neg; equiv-neg)
open import foundation.structure-identity-principle using
  ( is-contr-total-Eq-structure)
open import foundation.subtype-identity-principle using
  ( is-contr-total-Eq-subtype)
open import foundation.universe-levels using (Level; UU)
```

## Idea

Pairs of distinct elements in a type `A` consist of two elements `x` and `y` of `A` equipped with an element of type `x ≠ y`.

## Definition

```agda
pair-of-distinct-elements : {l : Level} → UU l → UU l
pair-of-distinct-elements A =
  Σ A (λ x → Σ A (λ y → ¬ (Id x y)))

module _
  {l : Level} {A : UU l} (p : pair-of-distinct-elements A)
  where
  
  fst-pair-of-distinct-elements : A
  fst-pair-of-distinct-elements = pr1 p

  snd-pair-of-distinct-elements : A
  snd-pair-of-distinct-elements = pr1 (pr2 p)

  distinction-pair-of-distinct-elements :
    ¬ (Id fst-pair-of-distinct-elements snd-pair-of-distinct-elements)
  distinction-pair-of-distinct-elements = pr2 (pr2 p)
```

## Properties

### Characterization of the identity type of the type of pairs of distinct elements

```agda
module _
  {l : Level} {A : UU l}
  where
  
  Eq-pair-of-distinct-elements :
    (p q : pair-of-distinct-elements A) → UU l
  Eq-pair-of-distinct-elements p q =
    Id (fst-pair-of-distinct-elements p) (fst-pair-of-distinct-elements q) ×
    Id (snd-pair-of-distinct-elements p) (snd-pair-of-distinct-elements q)

  refl-Eq-pair-of-distinct-elements :
    (p : pair-of-distinct-elements A) → Eq-pair-of-distinct-elements p p
  pr1 (refl-Eq-pair-of-distinct-elements p) = refl
  pr2 (refl-Eq-pair-of-distinct-elements p) = refl

  Eq-eq-pair-of-distinct-elements :
    (p q : pair-of-distinct-elements A) →
    Id p q → Eq-pair-of-distinct-elements p q
  Eq-eq-pair-of-distinct-elements p .p refl =
    refl-Eq-pair-of-distinct-elements p

  is-contr-total-Eq-pair-of-distinct-elements :
    (p : pair-of-distinct-elements A) →
    is-contr (Σ (pair-of-distinct-elements A) (Eq-pair-of-distinct-elements p))
  is-contr-total-Eq-pair-of-distinct-elements p =
    is-contr-total-Eq-structure
      ( λ x ynp α → Id (snd-pair-of-distinct-elements p) (pr1 ynp))
      ( is-contr-total-path (fst-pair-of-distinct-elements p))
      ( pair (fst-pair-of-distinct-elements p) refl)
      ( is-contr-total-Eq-subtype
        ( is-contr-total-path (snd-pair-of-distinct-elements p))
        ( λ x → is-prop-neg)
        ( snd-pair-of-distinct-elements p)
        ( refl)
        ( distinction-pair-of-distinct-elements p))

  is-equiv-Eq-eq-pair-of-distinct-elements :
    (p q : pair-of-distinct-elements A) →
    is-equiv (Eq-eq-pair-of-distinct-elements p q)
  is-equiv-Eq-eq-pair-of-distinct-elements p =
    fundamental-theorem-id p
      ( refl-Eq-pair-of-distinct-elements p)
      ( is-contr-total-Eq-pair-of-distinct-elements p)
      ( Eq-eq-pair-of-distinct-elements p)

  eq-Eq-pair-of-distinct-elements :
    {p q : pair-of-distinct-elements A} →
    Id (fst-pair-of-distinct-elements p) (fst-pair-of-distinct-elements q) →
    Id (snd-pair-of-distinct-elements p) (snd-pair-of-distinct-elements q) →
    Id p q
  eq-Eq-pair-of-distinct-elements {p} {q} α β =
    map-inv-is-equiv (is-equiv-Eq-eq-pair-of-distinct-elements p q) (pair α β)
  
```

### Equivalences map pairs of distinct elements to pairs of distinct elements

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : UU l2} (e : A ≃ B)
  where

  map-equiv-pair-of-distinct-elements :
    pair-of-distinct-elements A → pair-of-distinct-elements B
  pr1 (map-equiv-pair-of-distinct-elements p) =
    map-equiv e (fst-pair-of-distinct-elements p)
  pr1 (pr2 (map-equiv-pair-of-distinct-elements p)) =
    map-equiv e (snd-pair-of-distinct-elements p)
  pr2 (pr2 (map-equiv-pair-of-distinct-elements p)) q =
    distinction-pair-of-distinct-elements p
      ( is-injective-is-equiv (is-equiv-map-equiv e) q)

  map-inv-equiv-pair-of-distinct-elements :
    pair-of-distinct-elements B → pair-of-distinct-elements A
  pr1 (map-inv-equiv-pair-of-distinct-elements q) =
    map-inv-equiv e (fst-pair-of-distinct-elements q)
  pr1 (pr2 (map-inv-equiv-pair-of-distinct-elements q)) =
    map-inv-equiv e (snd-pair-of-distinct-elements q)
  pr2 (pr2 (map-inv-equiv-pair-of-distinct-elements q)) p =
    distinction-pair-of-distinct-elements q
      ( is-injective-is-equiv (is-equiv-map-inv-equiv e) p)

  issec-map-inv-equiv-pair-of-distinct-elements :
    (q : pair-of-distinct-elements B) →
    Id ( map-equiv-pair-of-distinct-elements
         ( map-inv-equiv-pair-of-distinct-elements q))
       ( q)
  issec-map-inv-equiv-pair-of-distinct-elements q =
    eq-Eq-pair-of-distinct-elements
      ( issec-map-inv-equiv e (fst-pair-of-distinct-elements q))
      ( issec-map-inv-equiv e (snd-pair-of-distinct-elements q))

  isretr-map-inv-equiv-pair-of-distinct-elements :
    (p : pair-of-distinct-elements A) →
    Id ( map-inv-equiv-pair-of-distinct-elements
         ( map-equiv-pair-of-distinct-elements p))
       ( p)
  isretr-map-inv-equiv-pair-of-distinct-elements p =
    eq-Eq-pair-of-distinct-elements
      ( isretr-map-inv-equiv e (fst-pair-of-distinct-elements p))
      ( isretr-map-inv-equiv e (snd-pair-of-distinct-elements p))

  is-equiv-map-equiv-pair-of-distinct-elements :
    is-equiv map-equiv-pair-of-distinct-elements
  is-equiv-map-equiv-pair-of-distinct-elements =
    is-equiv-has-inverse
      map-inv-equiv-pair-of-distinct-elements
      issec-map-inv-equiv-pair-of-distinct-elements
      isretr-map-inv-equiv-pair-of-distinct-elements

  equiv-pair-of-distinct-elements :
    pair-of-distinct-elements A ≃ pair-of-distinct-elements B
  pr1 equiv-pair-of-distinct-elements = map-equiv-pair-of-distinct-elements
  pr2 equiv-pair-of-distinct-elements =
    is-equiv-map-equiv-pair-of-distinct-elements
```

### Embeddings map pairs of distinct elements to pairs of distinct elements

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : UU l2} (e : A ↪ B)
  where

  emb-pair-of-distinct-elements :
    pair-of-distinct-elements A ↪ pair-of-distinct-elements B
  emb-pair-of-distinct-elements =
    emb-Σ
      ( λ x → Σ B (λ y → ¬ (Id x y)))
      ( e)
      ( λ x →
        emb-Σ
          ( λ y → ¬ (Id (map-emb e x) y))
          ( e)
          ( λ y → emb-equiv (equiv-neg (equiv-ap-emb e))))

  map-emb-pair-of-distinct-elements :
    pair-of-distinct-elements A → pair-of-distinct-elements B
  map-emb-pair-of-distinct-elements =
    map-emb emb-pair-of-distinct-elements

  is-emb-map-emb-pair-of-distinct-elements :
    is-emb map-emb-pair-of-distinct-elements
  is-emb-map-emb-pair-of-distinct-elements =
    is-emb-map-emb emb-pair-of-distinct-elements
```
