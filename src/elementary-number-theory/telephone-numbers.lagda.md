# Telephone numbers

```agda
{-# OPTIONS --without-K --exact-split #-}

module elementary-number-theory.telephone-numbers where

open import elementary-number-theory.addition-natural-numbers using (add-ℕ)
open import elementary-number-theory.multiplication-natural-numbers using
  ( mul-ℕ)
open import elementary-number-theory.natural-numbers using (ℕ; zero-ℕ; succ-ℕ)
```

## Idea

The telephone numbers are a sequence of natural numbers that count the way `n` telephone lines can be connected to each other, where each line can be connected to at most one other line. They also occur in several other combinatorics problems.

## Definitions

```agda
telephone-number : ℕ → ℕ
telephone-number zero-ℕ = succ-ℕ zero-ℕ
telephone-number (succ-ℕ zero-ℕ) = succ-ℕ zero-ℕ
telephone-number (succ-ℕ (succ-ℕ n)) =
  add-ℕ (telephone-number (succ-ℕ n)) (mul-ℕ (succ-ℕ n) (telephone-number n))
```
