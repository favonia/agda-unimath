---
title: Univalent Combinatorics
---

Univalent combinatorics is the study of finite univalent mathematics. Finiteness in univalent mathematics is expressed by a mere equivalence to a standard finite object.

Many finite structures naturally organize themselves into groupoids, in which the isomorphic objects are identified by the univalence axiom. Univalence can therefore help with counting finite structures up to isomorphism. The main piece of machinery that helps in this task is the general notion of π-finiteness. A level `k` π-finite type is a type that has finitely many connected components, such that all its homotopy groups up to level `k` are finite. The π-finite types enjoy useful closure properties, such as closedness under Σ, cartesian products, coproducts, and closedness under Π under a mild condition.

```agda
{-# OPTIONS --without-K --exact-split #-}

module univalent-combinatorics where

open import univalent-combinatorics.2-element-decidable-subtypes public
open import univalent-combinatorics.2-element-subtypes public
open import univalent-combinatorics.2-element-types public
open import univalent-combinatorics.binomial-types public
open import univalent-combinatorics.cartesian-product-types public
open import univalent-combinatorics.classical-finite-types
open import univalent-combinatorics.complements-isolated-points public
open import univalent-combinatorics.composition-species public
open import univalent-combinatorics.coproduct-types public
open import univalent-combinatorics.counting-decidable-subtypes public
open import univalent-combinatorics.counting-dependent-pair-types public
open import univalent-combinatorics.counting-maybe public
open import univalent-combinatorics.counting public
open import univalent-combinatorics.cubes public
open import univalent-combinatorics.decidable-dependent-function-types public
open import univalent-combinatorics.decidable-dependent-pair-types public
open import univalent-combinatorics.decidable-propositions public
open import univalent-combinatorics.decidable-subtypes public
open import univalent-combinatorics.dependent-function-types public
open import univalent-combinatorics.dedekind-finite-sets public
open import univalent-combinatorics.dependent-sum-finite-types public
open import univalent-combinatorics.distributivity-of-set-truncation-over-finite-products public
open import univalent-combinatorics.double-counting public
open import univalent-combinatorics.embeddings public
open import univalent-combinatorics.embeddings-standard-finite-types public
open import univalent-combinatorics.equality-finite-types public
open import univalent-combinatorics.equality-standard-finite-types public
open import univalent-combinatorics.equivalences-cubes public
open import univalent-combinatorics.equivalences-standard-finite-types public
open import univalent-combinatorics.equivalences public
open import univalent-combinatorics.ferrers-diagrams public
open import univalent-combinatorics.fibers-of-maps public
open import univalent-combinatorics.finite-choice public
open import univalent-combinatorics.finite-connected-components public
open import univalent-combinatorics.finite-presentations public
open import univalent-combinatorics.finite-types public
open import univalent-combinatorics.finitely-presented-types public
open import univalent-combinatorics.function-types public
open import univalent-combinatorics.image-of-maps public
open import univalent-combinatorics.inequality-types-with-counting public
open import univalent-combinatorics.injective-maps public
open import univalent-combinatorics.isotopies-latin-squares public
open import univalent-combinatorics.kuratowsky-finite-sets public
open import univalent-combinatorics.latin-squares public
open import univalent-combinatorics.lists public
open import univalent-combinatorics.main-classes-of-latin-hypercubes public
open import univalent-combinatorics.main-classes-of-latin-squares public
open import univalent-combinatorics.maybe public
open import univalent-combinatorics.orientations-cubes public
open import univalent-combinatorics.petri-nets public
open import univalent-combinatorics.pi-finite-types public
open import univalent-combinatorics.pigeonhole-principle public
open import univalent-combinatorics.presented-pi-finite-types public
open import univalent-combinatorics.ramsey-theory public
open import univalent-combinatorics.retracts-of-finite-types public
open import univalent-combinatorics.skipping-element-standard-finite-types public
open import univalent-combinatorics.standard-finite-pruned-trees public
open import univalent-combinatorics.standard-finite-trees public
open import univalent-combinatorics.standard-finite-types public
open import univalent-combinatorics.sums-of-natural-numbers public
open import univalent-combinatorics.surjective-maps public
open import univalent-combinatorics.universal-property-standard-finite-types public
```
