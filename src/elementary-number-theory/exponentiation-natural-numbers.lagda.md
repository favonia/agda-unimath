# Exponentiation of natural numbers

```agda
{-# OPTIONS --without-K --exact-split #-}

module elementary-number-theory.exponentiation-natural-numbers where

open import elementary-number-theory.addition-natural-numbers using (add-ℕ)
open import elementary-number-theory.multiplication-natural-numbers using
  ( mul-ℕ; right-unit-law-mul-ℕ; mul-ℕ'; associative-mul-ℕ;
    interchange-law-mul-mul-ℕ)
open import elementary-number-theory.natural-numbers using (ℕ; zero-ℕ; succ-ℕ)

open import foundation.identity-types using (Id; refl; _∙_; inv; ap)
```

## Idea

The exponent `m^n` is the number obtained by multiplying `m` with itself `n` times.

## Definition

```agda
exp-ℕ : ℕ → (ℕ → ℕ)
exp-ℕ m 0 = 1
exp-ℕ m (succ-ℕ n) = mul-ℕ (exp-ℕ m n) m
```

## Properties

### Tarski's high school arithmetic laws for exponentiation

```agda
annihilation-law-exp-ℕ : (n : ℕ) → Id (exp-ℕ 1 n) 1
annihilation-law-exp-ℕ zero-ℕ = refl
annihilation-law-exp-ℕ (succ-ℕ n) = right-unit-law-mul-ℕ (exp-ℕ 1 n) ∙ annihilation-law-exp-ℕ n

left-distributive-exp-add-ℕ : (x y z : ℕ) → Id (exp-ℕ x (add-ℕ y z)) (mul-ℕ (exp-ℕ x y) (exp-ℕ x z))
left-distributive-exp-add-ℕ x y zero-ℕ = inv (right-unit-law-mul-ℕ (exp-ℕ x y))
left-distributive-exp-add-ℕ x y (succ-ℕ z) =
  ( ap (mul-ℕ' x) (left-distributive-exp-add-ℕ x y z) ) ∙
  ( associative-mul-ℕ (exp-ℕ x y) (exp-ℕ x z) x )

right-distributive-exp-mul-ℕ : (x y z : ℕ) → Id (exp-ℕ (mul-ℕ x y) z) (mul-ℕ (exp-ℕ x z) (exp-ℕ y z))
right-distributive-exp-mul-ℕ x y zero-ℕ = refl
right-distributive-exp-mul-ℕ x y (succ-ℕ z) =
  ( ap (mul-ℕ' (mul-ℕ x y)) (right-distributive-exp-mul-ℕ x y z) ) ∙
  ( interchange-law-mul-mul-ℕ (exp-ℕ x z) (exp-ℕ y z) x y )

exp-mul-ℕ : (x y z : ℕ) → Id (exp-ℕ x (mul-ℕ y z)) (exp-ℕ (exp-ℕ x y) z)
exp-mul-ℕ x zero-ℕ z = inv (annihilation-law-exp-ℕ z)
exp-mul-ℕ x (succ-ℕ y) z =
  ( left-distributive-exp-add-ℕ x (mul-ℕ y z) z) ∙
  ( ( ap (mul-ℕ' (exp-ℕ x z)) (exp-mul-ℕ x y z)) ∙
    ( inv (right-distributive-exp-mul-ℕ (exp-ℕ x y) x z)))
```
