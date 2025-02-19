# Upper bounds for type families over the natural numbers

```agda
{-# OPTIONS --without-K --exact-split #-}

module elementary-number-theory.upper-bounds-natural-numbers where

open import elementary-number-theory.inequality-natural-numbers using
  ( leq-ℕ; le-ℕ; leq-le-ℕ)
open import elementary-number-theory.natural-numbers using (ℕ; zero-ℕ; succ-ℕ)

open import foundation.universe-levels using (Level; UU)
```

## Idea

A type family over the natural numbers has an upper bound `n`, if there is a function from `P x` to the type `x ≤ n` for all `x : ℕ`. Similar for strict upper bounds.

## Definition

### Upper bounds

```agda
is-upper-bound-ℕ :
  {l : Level} (P : ℕ → UU l) (n : ℕ) → UU l
is-upper-bound-ℕ P n =
  (m : ℕ) → P m → leq-ℕ m n
```

### Strict upper bounds

```agda
is-strict-upper-bound-ℕ :
  {l : Level} (P : ℕ → UU l) (n : ℕ) → UU l
is-strict-upper-bound-ℕ P n =
  (m : ℕ) → P m → le-ℕ m n
```

## Properties

### A strict upper bound is an upper bound

```agda
is-upper-bound-is-strict-upper-bound-ℕ :
  {l : Level} (P : ℕ → UU l) (n : ℕ) →
  is-strict-upper-bound-ℕ P n → is-upper-bound-ℕ P n
is-upper-bound-is-strict-upper-bound-ℕ P n H x p =
  leq-le-ℕ {x} {n} (H x p)
```
