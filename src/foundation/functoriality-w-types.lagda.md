# Functoriality of W-types

```agda
{-# OPTIONS --without-K --exact-split #-}

module foundation.functoriality-w-types where

open import foundation.cartesian-product-types using (_×_)
open import foundation.contractible-maps using
  ( is-equiv-is-contr-map; is-contr-map-is-equiv)
open import foundation.dependent-pair-types using (Σ; pair; pr1; pr2)
open import foundation.embeddings using (is-emb; _↪_; map-emb; is-emb-map-emb)
open import foundation.equivalences using
  ( _≃_; map-inv-equiv; inv-equiv; _∘e_; id-equiv; map-equiv;
    issec-map-inv-equiv; is-equiv; is-equiv-map-equiv)
open import foundation.fibers-of-maps using (fib)
open import foundation.functions using (_∘_)
open import foundation.functoriality-dependent-function-types using (equiv-Π)
open import foundation.functoriality-dependent-pair-types using
  ( equiv-tot; equiv-Σ)
open import foundation.identity-types using
  ( Id; equiv-tr; tr; equiv-concat'; ap; inv; equiv-concat)
open import foundation.propositional-maps using
  ( is-emb-is-prop-map; is-prop-map-is-emb)
open import foundation.truncated-maps using (is-trunc-map)
open import foundation.truncated-types using
  ( is-trunc-equiv; is-trunc-Σ; is-trunc-Π)
open import foundation.truncation-levels using (𝕋; neg-two-𝕋; neg-one-𝕋)
open import foundation.type-arithmetic-dependent-pair-types using
  ( assoc-Σ; equiv-left-swap-Σ)
open import foundation.type-theoretic-principle-of-choice using
  ( inv-distributive-Π-Σ)
open import foundation.universe-levels using (Level; UU; _⊔_)
open import foundation.w-types using
  ( 𝕎; tree-𝕎; equiv-Eq-𝕎-eq; structure-𝕎-Alg; inv-equiv-structure-𝕎-Alg;
    issec-map-inv-structure-𝕎-Alg)
```

## Idea

The W-type constructor acts functorially on `A` and `B`. It is covariant in `A`, and contravariant in `B`.

## Definition

```agda
map-𝕎' :
  {l1 l2 l3 l4 : Level} {A : UU l1} {B : A → UU l2} {C : UU l3} (D : C → UU l4)
  (f : A → C) (g : (x : A) → D (f x) → B x) →
  𝕎 A B → 𝕎 C D
map-𝕎' D f g (tree-𝕎 a α) = tree-𝕎 (f a) (λ d → map-𝕎' D f g (α (g a d)))

map-𝕎 :
  {l1 l2 l3 l4 : Level} {A : UU l1} {B : A → UU l2} {C : UU l3} (D : C → UU l4)
  (f : A → C) (e : (x : A) → B x ≃ D (f x)) →
  𝕎 A B → 𝕎 C D
map-𝕎 D f e = map-𝕎' D f (λ x → map-inv-equiv (e x))
```

## Properties

### We compute the fibers of `map-𝕎`

```agda
fib-map-𝕎 :
  {l1 l2 l3 l4 : Level} {A : UU l1} {B : A → UU l2} {C : UU l3} (D : C → UU l4)
  (f : A → C) (e : (x : A) → B x ≃ D (f x)) →
  𝕎 C D → UU (l1 ⊔ l2 ⊔ l3 ⊔ l4)
fib-map-𝕎 D f e (tree-𝕎 c γ) =
  (fib f c) × ((d : D c) → fib (map-𝕎 D f e) (γ d))

abstract
  equiv-fib-map-𝕎 :
    {l1 l2 l3 l4 : Level} {A : UU l1} {B : A → UU l2} {C : UU l3}
    (D : C → UU l4) (f : A → C) (e : (x : A) → B x ≃ D (f x)) →
    (y : 𝕎 C D) → fib (map-𝕎 D f e) y ≃ fib-map-𝕎 D f e y
  equiv-fib-map-𝕎 {A = A} {B} {C} D f e (tree-𝕎 c γ) =
    ( ( ( inv-equiv
          ( assoc-Σ A
            ( λ a → Id (f a) c)
            ( λ t → (d : D c) → fib (map-𝕎 D f e) (γ d)))) ∘e
        ( equiv-tot
          ( λ a →
            ( ( equiv-tot
                ( λ p →
                  ( ( equiv-Π
                      ( λ (d : D c) → fib (map-𝕎 D f e) (γ d))
                      ( (equiv-tr D p) ∘e (e a))
                      ( λ b → id-equiv)) ∘e
                    ( inv-distributive-Π-Σ)) ∘e 
                  ( equiv-tot
                    ( λ α →
                      equiv-Π
                        ( λ (b : B a) →
                          Id ( map-𝕎 D f e (α b))
                             ( γ (tr D p (map-equiv (e a) b))))
                        ( inv-equiv (e a))
                        ( λ d →
                          ( equiv-concat'
                            ( map-𝕎 D f e
                              ( α (map-inv-equiv (e a) d)))
                            ( ap ( γ ∘ (tr D p))
                                 ( inv (issec-map-inv-equiv (e a) d)))) ∘e
                          ( inv-equiv
                            ( equiv-Eq-𝕎-eq
                              ( map-𝕎 D f e
                                ( α (map-inv-equiv (e a) d)))
                              ( γ (tr D p d))))))))) ∘e
              ( equiv-left-swap-Σ)) ∘e
            ( equiv-tot
              ( λ α →
                equiv-Eq-𝕎-eq
                  ( tree-𝕎
                    ( f a)
                    ( ( map-𝕎 D f e) ∘
                      ( α ∘ map-inv-equiv (e a)))) (tree-𝕎 c γ)))))) ∘e
      ( assoc-Σ A
        ( λ a → B a → 𝕎 A B)
        ( λ t →
          Id (map-𝕎 D f e (structure-𝕎-Alg t)) (tree-𝕎 c γ)))) ∘e
    ( equiv-Σ
      ( λ t → Id (map-𝕎 D f e (structure-𝕎-Alg t)) (tree-𝕎 c γ))
      ( inv-equiv-structure-𝕎-Alg)
      ( λ x →
        equiv-concat
          ( ap (map-𝕎 D f e) (issec-map-inv-structure-𝕎-Alg x))
          ( tree-𝕎 c γ)))
```

### For any family of equivalences `e` over `f`, if `f` is truncated then `map-𝕎 f e` is truncated

```agda
is-trunc-map-map-𝕎 :
  {l1 l2 l3 l4 : Level} (k : 𝕋)
  {A : UU l1} {B : A → UU l2} {C : UU l3} (D : C → UU l4)
  (f : A → C) (e : (x : A) → B x ≃ D (f x)) →
  is-trunc-map k f → is-trunc-map k (map-𝕎 D f e)
is-trunc-map-map-𝕎 k D f e H (tree-𝕎 c γ) =
  is-trunc-equiv k
    ( fib-map-𝕎 D f e (tree-𝕎 c γ))
    ( equiv-fib-map-𝕎 D f e (tree-𝕎 c γ))
    ( is-trunc-Σ
      ( H c)
      ( λ t → is-trunc-Π k (λ d → is-trunc-map-map-𝕎 k D f e H (γ d))))
```

### For any family of equivalences `e` over `f`, if `f` is an equivalence then `map-𝕎 f e` is an equivalence

```agda
is-equiv-map-𝕎 :
  {l1 l2 l3 l4 : Level} {A : UU l1} {B : A → UU l2} {C : UU l3} (D : C → UU l4)
  (f : A → C) (e : (x : A) → B x ≃ D (f x)) →
  is-equiv f → is-equiv (map-𝕎 D f e)
is-equiv-map-𝕎 D f e H =
  is-equiv-is-contr-map
    ( is-trunc-map-map-𝕎 neg-two-𝕋 D f e (is-contr-map-is-equiv H))

equiv-𝕎 :
  {l1 l2 l3 l4 : Level} {A : UU l1} {B : A → UU l2} {C : UU l3} (D : C → UU l4)
  (f : A ≃ C) (e : (x : A) → B x ≃ D (map-equiv f x)) →
  𝕎 A B ≃ 𝕎 C D
equiv-𝕎 D f e =
  pair
    ( map-𝕎 D (map-equiv f) e)
    ( is-equiv-map-𝕎 D (map-equiv f) e (is-equiv-map-equiv f))
```

### For any family of equivalences `e` over `f`, if `f` is an embedding, then `map-𝕎 f e` is an embedding

```agda
is-emb-map-𝕎 :
  {l1 l2 l3 l4 : Level} {A : UU l1} {B : A → UU l2} {C : UU l3} (D : C → UU l4)
  (f : A → C) (e : (x : A) → B x ≃ D (f x)) →
  is-emb f → is-emb (map-𝕎 D f e)
is-emb-map-𝕎 D f e H =
  is-emb-is-prop-map
    (is-trunc-map-map-𝕎 neg-one-𝕋 D f e (is-prop-map-is-emb H))

emb-𝕎 :
  {l1 l2 l3 l4 : Level} {A : UU l1} {B : A → UU l2} {C : UU l3} (D : C → UU l4)
  (f : A ↪ C) (e : (x : A) → B x ≃ D (map-emb f x)) → 𝕎 A B ↪ 𝕎 C D
emb-𝕎 D f e =
  pair
    ( map-𝕎 D (map-emb f) e)
    ( is-emb-map-𝕎 D (map-emb f) e (is-emb-map-emb f))
```
