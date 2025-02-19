# W-types

```agda
{-# OPTIONS --without-K --exact-split --allow-unsolved-metas #-}

module foundation.w-types where

open import foundation.algebras-polynomial-endofunctors using
  ( algebra-polynomial-endofunctor-UU; type-algebra-polynomial-endofunctor;
    structure-algebra-polynomial-endofunctor;
    hom-algebra-polynomial-endofunctor; map-hom-algebra-polynomial-endofunctor;
    structure-hom-algebra-polynomial-endofunctor;
    htpy-hom-algebra-polynomial-endofunctor;
    eq-htpy-hom-algebra-polynomial-endofunctor)
open import foundation.contractible-types using (is-contr)
open import foundation.dependent-pair-types using (Σ; pair; pr1; pr2)
open import foundation.empty-types using (is-empty; ex-falso; empty-Prop)
open import foundation.equivalences using
  ( is-equiv; map-inv-is-equiv; _≃_; is-equiv-has-inverse)
open import foundation.function-extensionality using
  ( eq-htpy; eq-htpy-refl-htpy)
open import foundation.functions using (_∘_; id)
open import foundation.fundamental-theorem-of-identity-types using
  ( fundamental-theorem-id)
open import foundation.homotopies using (_~_; _·r_; ind-htpy; _∙h_; _·l_)
open import foundation.identity-types using
  ( Id; refl; tr; ap; _∙_; inv; right-unit; concat; left-inv; assoc)
open import foundation.polynomial-endofunctors using
  ( type-polynomial-endofunctor; map-polynomial-endofunctor;
    htpy-polynomial-endofunctor; coh-refl-htpy-polynomial-endofunctor)
open import foundation.propositional-truncations using
  ( type-trunc-Prop; apply-universal-property-trunc-Prop)
open import foundation.truncated-types using
  ( is-trunc; is-trunc-is-equiv; is-trunc-Σ; is-trunc-Π; is-trunc-is-equiv')
open import foundation.type-theoretic-principle-of-choice using
  ( map-distributive-Π-Σ)
open import foundation.universe-levels using (Level; UU; _⊔_)

open import foundation-core.truncation-levels using (𝕋; succ-𝕋)
```

## Idea

Consider a type `A` equipped with a type family `B` over `A`. The type `W` generated inductively by a constructor `B x → W` for each `x : A` is called the W-typpe `W A B` of `B`. The elements of `A` can be thought of as symbols for the constructors of `W A B`, and the functions `B x → W A B` are the constructors. The elements of `W A B` are well-founded trees.

## Definition

```agda
data 𝕎 {l1 l2 : Level} (A : UU l1) (B : A → UU l2) : UU (l1 ⊔ l2) where
  tree-𝕎 : (x : A) (α : B x → 𝕎 A B) → 𝕎 A B

module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where
  
  symbol-𝕎 : 𝕎 A B → A
  symbol-𝕎 (tree-𝕎 x α) = x
  
  component-𝕎 : (x : 𝕎 A B) → B (symbol-𝕎 x) → 𝕎 A B
  component-𝕎 (tree-𝕎 x α) = α

  η-𝕎 : (x : 𝕎 A B) → Id (tree-𝕎 (symbol-𝕎 x) (component-𝕎 x)) x
  η-𝕎 (tree-𝕎 x α) = refl
```

## Properties

### The elements of the form `tree-𝕎 x α` where `B x` is an empty type are called the constants of `W A B`

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  constant-𝕎 : (x : A) → is-empty (B x) → 𝕎 A B
  constant-𝕎 x h = tree-𝕎 x (ex-falso ∘ h)

  is-constant-𝕎 : 𝕎 A B → UU l2
  is-constant-𝕎 x = is-empty (B (symbol-𝕎 x))
```

### If each `B x` is inhabited, then the type `W A B` is empty

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where

  is-empty-𝕎 : ((x : A) → type-trunc-Prop (B x)) → is-empty (𝕎 A B)
  is-empty-𝕎 H (tree-𝕎 x α) =
    apply-universal-property-trunc-Prop
      ( H x)
      ( empty-Prop)
      ( λ y → is-empty-𝕎 H (α y))
```

### Equality of W-types

```agda
module _
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2}
  where
  
  Eq-𝕎 : 𝕎 A B → 𝕎 A B → UU (l1 ⊔ l2)
  Eq-𝕎 (tree-𝕎 x α) (tree-𝕎 y β) =
    Σ (Id x y) (λ p → (z : B x) → Eq-𝕎 (α z) (β (tr B p z))) 

  refl-Eq-𝕎 : (w : 𝕎 A B) → Eq-𝕎 w w
  refl-Eq-𝕎 (tree-𝕎 x α) = pair refl (λ z → refl-Eq-𝕎 (α z))

  center-total-Eq-𝕎 : (w : 𝕎 A B) → Σ (𝕎 A B) (Eq-𝕎 w)
  center-total-Eq-𝕎 w = pair w (refl-Eq-𝕎 w)

  aux-total-Eq-𝕎 :
    (x : A) (α : B x → 𝕎 A B) →
    Σ (B x → 𝕎 A B) (λ β → (y : B x) → Eq-𝕎 (α y) (β y)) →
    Σ (𝕎 A B) (Eq-𝕎 (tree-𝕎 x α))
  aux-total-Eq-𝕎 x α (pair β e) = pair (tree-𝕎 x β) (pair refl e)

  contraction-total-Eq-𝕎 :
    (w : 𝕎 A B) (t : Σ (𝕎 A B) (Eq-𝕎 w)) → Id (center-total-Eq-𝕎 w) t
  contraction-total-Eq-𝕎
    ( tree-𝕎 x α) (pair (tree-𝕎 .x β) (pair refl e)) =
    ap ( ( aux-total-Eq-𝕎 x α) ∘
         ( map-distributive-Π-Σ
           { A = B x}
           { B = λ y → 𝕎 A B}
           { C = λ y → Eq-𝕎 (α y)}))
       { x = λ y → pair (α y) (refl-Eq-𝕎 (α y))}
       { y = λ y → pair (β y) (e y)}
       ( eq-htpy (λ y → contraction-total-Eq-𝕎 (α y) (pair (β y) (e y))))

  is-contr-total-Eq-𝕎 : (w : 𝕎 A B) → is-contr (Σ (𝕎 A B) (Eq-𝕎 w))
  is-contr-total-Eq-𝕎 w =
    pair (center-total-Eq-𝕎 w) (contraction-total-Eq-𝕎 w)

  Eq-𝕎-eq : (v w : 𝕎 A B) → Id v w → Eq-𝕎 v w
  Eq-𝕎-eq v .v refl = refl-Eq-𝕎 v

  is-equiv-Eq-𝕎-eq : (v w : 𝕎 A B) → is-equiv (Eq-𝕎-eq v w)
  is-equiv-Eq-𝕎-eq v =
    fundamental-theorem-id v
      ( refl-Eq-𝕎 v)
      ( is-contr-total-Eq-𝕎 v)
      ( Eq-𝕎-eq v)

  eq-Eq-𝕎 : (v w : 𝕎 A B) → Eq-𝕎 v w → Id v w
  eq-Eq-𝕎 v w = map-inv-is-equiv (is-equiv-Eq-𝕎-eq v w)

  equiv-Eq-𝕎-eq : (v w : 𝕎 A B) → Id v w ≃ Eq-𝕎 v w
  equiv-Eq-𝕎-eq v w = pair (Eq-𝕎-eq v w) (is-equiv-Eq-𝕎-eq v w)
  
  is-trunc-𝕎 : (k : 𝕋) → is-trunc (succ-𝕋 k) A → is-trunc (succ-𝕋 k) (𝕎 A B)
  is-trunc-𝕎 k is-trunc-A (tree-𝕎 x α) (tree-𝕎 y β) =
    is-trunc-is-equiv k
      ( Eq-𝕎 (tree-𝕎 x α) (tree-𝕎 y β))
      ( Eq-𝕎-eq (tree-𝕎 x α) (tree-𝕎 y β))
      ( is-equiv-Eq-𝕎-eq (tree-𝕎 x α) (tree-𝕎 y β))
      ( is-trunc-Σ
        ( is-trunc-A x y)
        ( λ p → is-trunc-Π k
          ( λ z →
            is-trunc-is-equiv' k
            ( Id (α z) (β (tr B p z)))
            ( Eq-𝕎-eq (α z) (β (tr B p z)))
            ( is-equiv-Eq-𝕎-eq (α z) (β (tr B p z)))
            ( is-trunc-𝕎 k is-trunc-A (α z) (β (tr B p z))))))
```

### W-types are algebras for polynomial endofunctors

```agda
structure-𝕎-Alg :
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2} →
  type-polynomial-endofunctor A B (𝕎 A B) → 𝕎 A B
structure-𝕎-Alg (pair x α) = tree-𝕎 x α

𝕎-Alg :
  {l1 l2 : Level} (A : UU l1) (B : A → UU l2) →
  algebra-polynomial-endofunctor-UU (l1 ⊔ l2) A B
𝕎-Alg A B = pair (𝕎 A B) structure-𝕎-Alg

map-inv-structure-𝕎-Alg :
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2} →
  𝕎 A B → type-polynomial-endofunctor A B (𝕎 A B)
map-inv-structure-𝕎-Alg (tree-𝕎 x α) = pair x α

issec-map-inv-structure-𝕎-Alg :
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2} →
  (structure-𝕎-Alg {B = B} ∘ map-inv-structure-𝕎-Alg {B = B}) ~ id
issec-map-inv-structure-𝕎-Alg (tree-𝕎 x α) = refl

isretr-map-inv-structure-𝕎-Alg :
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2} →
  (map-inv-structure-𝕎-Alg {B = B} ∘ structure-𝕎-Alg {B = B}) ~ id
isretr-map-inv-structure-𝕎-Alg (pair x α) = refl

is-equiv-structure-𝕎-Alg :
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2} →
  is-equiv (structure-𝕎-Alg {B = B})
is-equiv-structure-𝕎-Alg =
  is-equiv-has-inverse
    map-inv-structure-𝕎-Alg
    issec-map-inv-structure-𝕎-Alg
    isretr-map-inv-structure-𝕎-Alg

equiv-structure-𝕎-Alg :
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2} →
  type-polynomial-endofunctor A B (𝕎 A B) ≃ 𝕎 A B
equiv-structure-𝕎-Alg =
  pair structure-𝕎-Alg is-equiv-structure-𝕎-Alg

is-equiv-map-inv-structure-𝕎-Alg :
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2} →
  is-equiv (map-inv-structure-𝕎-Alg {B = B})
is-equiv-map-inv-structure-𝕎-Alg =
  is-equiv-has-inverse
    structure-𝕎-Alg
    isretr-map-inv-structure-𝕎-Alg
    issec-map-inv-structure-𝕎-Alg

inv-equiv-structure-𝕎-Alg :
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2} →
  𝕎 A B ≃ type-polynomial-endofunctor A B (𝕎 A B)
inv-equiv-structure-𝕎-Alg =
  pair map-inv-structure-𝕎-Alg is-equiv-map-inv-structure-𝕎-Alg
```

### W-types are initial algebras for polynomial endofunctors

```agda
map-hom-𝕎-Alg :
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2}
  (X : algebra-polynomial-endofunctor-UU l3 A B) →
  𝕎 A B → type-algebra-polynomial-endofunctor X
map-hom-𝕎-Alg X (tree-𝕎 x α) =
  structure-algebra-polynomial-endofunctor X
    ( pair x (λ y → map-hom-𝕎-Alg X (α y)))

structure-hom-𝕎-Alg :
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2}
  (X : algebra-polynomial-endofunctor-UU l3 A B) →
  ( (map-hom-𝕎-Alg X) ∘ structure-𝕎-Alg) ~
  ( ( structure-algebra-polynomial-endofunctor X) ∘
    ( map-polynomial-endofunctor A B (map-hom-𝕎-Alg X)))
structure-hom-𝕎-Alg X (pair x α) = refl

hom-𝕎-Alg :
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2}
  (X : algebra-polynomial-endofunctor-UU l3 A B) →
  hom-algebra-polynomial-endofunctor (𝕎-Alg A B) X
hom-𝕎-Alg X = pair (map-hom-𝕎-Alg X) (structure-hom-𝕎-Alg X)

htpy-htpy-hom-𝕎-Alg :
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2}
  (X : algebra-polynomial-endofunctor-UU l3 A B) →
  (f : hom-algebra-polynomial-endofunctor (𝕎-Alg A B) X) →
  map-hom-𝕎-Alg X ~
  map-hom-algebra-polynomial-endofunctor (𝕎-Alg A B) X f
htpy-htpy-hom-𝕎-Alg {A = A} {B} X f (tree-𝕎 x α) =
  ( ap ( λ t → structure-algebra-polynomial-endofunctor X (pair x t))
       ( eq-htpy (λ z → htpy-htpy-hom-𝕎-Alg X f (α z)))) ∙
  ( inv
    ( structure-hom-algebra-polynomial-endofunctor (𝕎-Alg A B) X f
      ( pair x α)))
                 
compute-structure-htpy-hom-𝕎-Alg :
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2}
  (X : algebra-polynomial-endofunctor-UU l3 A B) (x : A) (α : B x → 𝕎 A B)
  {f : 𝕎 A B → type-algebra-polynomial-endofunctor X} →
  (H : map-hom-𝕎-Alg X ~ f) →
  Id ( ap ( structure-algebra-polynomial-endofunctor X)
          ( htpy-polynomial-endofunctor A B H (pair x α)))
     ( ap ( λ t → structure-algebra-polynomial-endofunctor X (pair x t))
          ( eq-htpy (H ·r α)))
compute-structure-htpy-hom-𝕎-Alg {A = A} {B} X x α = 
  ind-htpy
    ( map-hom-𝕎-Alg X)
    ( λ f H →
      Id ( ap ( structure-algebra-polynomial-endofunctor X)
              ( htpy-polynomial-endofunctor A B H (pair x α)))
         ( ap ( λ t → structure-algebra-polynomial-endofunctor X (pair x t))
              ( eq-htpy (H ·r α))))
    ( ap ( ap (pr2 X))
         ( coh-refl-htpy-polynomial-endofunctor A B
           ( map-hom-𝕎-Alg X)
           ( pair x α)) ∙
    ( inv
      ( ap ( ap (λ t → pr2 X (pair x t)))
           ( eq-htpy-refl-htpy (map-hom-𝕎-Alg X ∘ α)))))

structure-htpy-hom-𝕎-Alg :
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2}
  (X : algebra-polynomial-endofunctor-UU l3 A B) →
  (f : hom-algebra-polynomial-endofunctor (𝕎-Alg A B) X) →
  ( structure-hom-𝕎-Alg X ∙h
    ( ( structure-algebra-polynomial-endofunctor X) ·l
      ( htpy-polynomial-endofunctor A B (htpy-htpy-hom-𝕎-Alg X f)))) ~
  ( ( (htpy-htpy-hom-𝕎-Alg X f) ·r structure-𝕎-Alg {B = B}) ∙h
    ( structure-hom-algebra-polynomial-endofunctor (𝕎-Alg A B) X f))
structure-htpy-hom-𝕎-Alg {A = A} {B} X (pair f μ-f) (pair x α) =
  ( ( ( compute-structure-htpy-hom-𝕎-Alg X x α
        ( htpy-htpy-hom-𝕎-Alg X (pair f μ-f)))  ∙
      ( inv right-unit)) ∙
    ( ap ( concat
           ( ap
             ( λ t → pr2 X (pair x t))
             ( eq-htpy (htpy-htpy-hom-𝕎-Alg X (pair f μ-f) ·r α)))
         ( pr2 X (map-polynomial-endofunctor A B f (pair x α))))
         ( inv (left-inv ( μ-f (pair x α)))))) ∙
  ( inv
    ( assoc
      ( ap ( λ t → pr2 X (pair x t))
           ( eq-htpy (htpy-htpy-hom-𝕎-Alg X (pair f μ-f) ·r α)))
      ( inv (μ-f (pair x α)))
      ( μ-f (pair x α))))

htpy-hom-𝕎-Alg :
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2}
  (X : algebra-polynomial-endofunctor-UU l3 A B) →
  (f : hom-algebra-polynomial-endofunctor (𝕎-Alg A B) X) →
  htpy-hom-algebra-polynomial-endofunctor (𝕎-Alg A B) X (hom-𝕎-Alg X) f
htpy-hom-𝕎-Alg X f =
  pair (htpy-htpy-hom-𝕎-Alg X f) (structure-htpy-hom-𝕎-Alg X f)

is-initial-𝕎-Alg :
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2}
  (X : algebra-polynomial-endofunctor-UU l3 A B) →
  is-contr (hom-algebra-polynomial-endofunctor (𝕎-Alg A B) X)
is-initial-𝕎-Alg {A = A} {B} X =
  pair
    ( hom-𝕎-Alg X)
    ( λ f →
      eq-htpy-hom-algebra-polynomial-endofunctor (𝕎-Alg A B) X (hom-𝕎-Alg X) f
        ( htpy-hom-𝕎-Alg X f))
```
