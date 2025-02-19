# Epimorphism in large precategories

```agda
{-# OPTIONS --without-K --exact-split #-}

module category-theory.epimorphisms-large-precategories where

open import category-theory.isomorphisms-large-precategories using
  ( iso-Large-Precat; hom-iso-Large-Precat; is-sec-hom-inv-iso-Large-Precat;
    hom-inv-iso-Large-Precat)
open import category-theory.large-precategories using
  ( Large-Precat; obj-Large-Precat; type-hom-Large-Precat;
    comp-hom-Large-Precat; right-unit-law-comp-hom-Large-Precat;
    associative-comp-hom-Large-Precat; is-set-type-hom-Large-Precat)

open import foundation.embeddings using (is-emb-Prop)
open import foundation.equivalences using (is-equiv-has-inverse)
open import foundation.identity-types using (Id; refl; _∙_; ap; inv)
open import foundation.propositions using
  ( UU-Prop; Π-Prop; type-Prop; is-prop; is-prop-type-Prop; eq-is-prop)
open import foundation.universe-levels using (UU; Level; _⊔_)
```

## Idea

A morphism `f : x → y` is a epimorphism if whenever we have two morphisms `g h : y → w` such that `g ∘ f = h ∘ f`, then in fact `g = h`. The way to state this in Homotopy Type Theory is to say that precomposition by `f` is an embedding.

## Definition

```agda
module _ {α : Level → Level} {β : Level → Level → Level}
  (C : Large-Precat α β) {l1 l2 : Level} (l3 : Level)
  (X : obj-Large-Precat C l1) (Y : obj-Large-Precat C l2)
  (f : type-hom-Large-Precat C X Y) where

  is-epi-Large-Precat-Prop : UU-Prop (α l3 ⊔ β l1 l3 ⊔ β l2 l3)
  is-epi-Large-Precat-Prop =
    Π-Prop
      ( obj-Large-Precat C l3)
      ( λ Z → is-emb-Prop (λ g → comp-hom-Large-Precat C {Z = Z} g f))

  is-epi-Large-Precat : UU (α l3 ⊔ β l1 l3 ⊔ β l2 l3)
  is-epi-Large-Precat = type-Prop is-epi-Large-Precat-Prop

  is-prop-is-epi-Large-Precat : is-prop is-epi-Large-Precat
  is-prop-is-epi-Large-Precat = is-prop-type-Prop is-epi-Large-Precat-Prop
```

## Properties

### Isomorphisms are epimorphisms

```agda
module _ {α : Level → Level} {β : Level → Level → Level}
  (C : Large-Precat α β) {l1 l2 : Level} (l3 : Level)
  (X : obj-Large-Precat C l1) (Y : obj-Large-Precat C l2)
  (f : iso-Large-Precat C X Y) where

  is-epi-iso-Large-Precat :
    is-epi-Large-Precat C l3 X Y (hom-iso-Large-Precat C X Y f)
  is-epi-iso-Large-Precat Z g h =
    is-equiv-has-inverse
      ( λ P →
        ( inv
          ( right-unit-law-comp-hom-Large-Precat C g)) ∙
          ( ( ap
            ( λ h' → comp-hom-Large-Precat C g h')
            ( inv (is-sec-hom-inv-iso-Large-Precat C X Y f))) ∙
            ( ( inv
              ( associative-comp-hom-Large-Precat C
                ( g)
                ( hom-iso-Large-Precat C X Y f)
                ( hom-inv-iso-Large-Precat C X Y f))) ∙
              ( ( ap
                ( λ h' → comp-hom-Large-Precat C h' (hom-inv-iso-Large-Precat C X Y f))
                ( P)) ∙
                ( ( associative-comp-hom-Large-Precat C
                  ( h)
                  ( hom-iso-Large-Precat C X Y f)
                  ( hom-inv-iso-Large-Precat C X Y f)) ∙
                  ( ( ap
                    ( comp-hom-Large-Precat C h)
                    ( is-sec-hom-inv-iso-Large-Precat C X Y f)) ∙
                    ( right-unit-law-comp-hom-Large-Precat C h)))))))
      ( λ p →
        eq-is-prop
          ( is-set-type-hom-Large-Precat C X Z
            ( comp-hom-Large-Precat C g (hom-iso-Large-Precat C X Y f))
            ( comp-hom-Large-Precat C h (hom-iso-Large-Precat C X Y f))))
      ( λ p → eq-is-prop (is-set-type-hom-Large-Precat C Y Z g h))
```
