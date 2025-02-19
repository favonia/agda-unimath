# Equivalences between large precategories

```agda
{-# OPTIONS --without-K --exact-split #-}

module category-theory.equivalences-large-precategories where

open import Agda.Primitive using (Setω)
open import category-theory.functors-large-precategories using
  ( functor-Large-Precat; comp-functor-Large-Precat;
    id-functor-Large-Precat)
open import category-theory.natural-isomorphisms-large-precategories using
  ( natural-isomorphism-Large-Precat)
open import category-theory.large-precategories using
  ( Large-Precat)
open import foundation.universe-levels using (Level)
```

## Idea

The large precategories `C` and `D` are equivalent if there are functors `F : C → D` and `G : D → C` such that
- `comp G F` is naturally isomorphic to the identity functor on `C`,
- `comp F G` is naturally isomorphic to the identity functor on `D`.

## Definition

```agda
module _
  {αC αD : Level → Level} {βC βD : Level → Level → Level}
  (C : Large-Precat αC βC) (D : Large-Precat αD βD)
  where

  record equivalence-Large-Precat (γ-there γ-back : Level → Level) : Setω where
    constructor make-equivalence-Large-Precat
    field
      there-equivalence-Large-Precat : functor-Large-Precat C D γ-there
      back-equivalence-Large-Precat : functor-Large-Precat D C γ-back
      back-there-equivalence-Large-Precat :
        natural-isomorphism-Large-Precat
          (comp-functor-Large-Precat back-equivalence-Large-Precat there-equivalence-Large-Precat)
          (id-functor-Large-Precat)
      there-back-equivalence-Large-Precat :
        natural-isomorphism-Large-Precat
          (comp-functor-Large-Precat there-equivalence-Large-Precat back-equivalence-Large-Precat)
          (id-functor-Large-Precat)
```
