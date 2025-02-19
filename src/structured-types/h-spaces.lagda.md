---
title: H-spaces
---

```agda
{-# OPTIONS --without-K --exact-split #-}

module structured-types.h-spaces where

open import foundation.cartesian-product-types
open import foundation.dependent-pair-types
open import foundation.functions
open import foundation.homotopies
open import foundation.identity-types
open import foundation.universe-levels

open import structured-types.pointed-types
```

## Idea

An H-space is a pointed type `A` equipped with a binary operation `μ` and homotopies `(λ x → μ pt x) ~ id` and `λ x → μ x pt ~ id`. If `A` is a connected H-space, then `λ x → μ a x` and `λ x → μ x a` are equivalences for each `a : A`.

## Definitions

```agda
h-space-structure :
  {l : Level} (A : Pointed-Type l) → UU l
h-space-structure A =
  Σ ( (x y : type-Pointed-Type A) → type-Pointed-Type A)
    ( λ μ →
      ( μ (pt-Pointed-Type A) ~ id) ×
      ( (λ x → μ x (pt-Pointed-Type A)) ~ id))

H-Space : (l : Level) → UU (lsuc l)
H-Space l = Σ (Pointed-Type l) h-space-structure

module _
  {l : Level} (A : H-Space l)
  where

  pointed-type-H-Space : Pointed-Type l
  pointed-type-H-Space = pr1 A

  type-H-Space : UU l
  type-H-Space = type-Pointed-Type pointed-type-H-Space

  pt-H-Space : type-H-Space
  pt-H-Space = pt-Pointed-Type pointed-type-H-Space

  mul-H-Space : type-H-Space → type-H-Space → type-H-Space
  mul-H-Space = pr1 (pr2 A)

  left-unit-law-mul-H-Space :
    (x : type-H-Space) → Id (mul-H-Space pt-H-Space x) x
  left-unit-law-mul-H-Space = pr1 (pr2 (pr2 A))

  right-unit-law-mul-H-Space :
    (x : type-H-Space) → Id (mul-H-Space x pt-H-Space) x
  right-unit-law-mul-H-Space = pr2 (pr2 (pr2 A))
```

## Properties
