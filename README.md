---
title: Univalent mathematics in Agda
---

Welcome to the website of the `agda-unimath` formalization project.

[![CI](https://github.com/UniMath/agda-unimath/actions/workflows/ci.yaml/badge.svg)](https://github.com/UniMath/agda-unimath/actions/workflows/ci.yaml) [![pages-build-deployment](https://github.com/UniMath/agda-unimath/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/UniMath/agda-unimath/actions/workflows/pages/pages-build-deployment)

The `agda-unimath` library is a new formalisation project for univalent mathematics in Agda. Our goal is to formalize an extensive curriculum of mathematics from the univalent point of view. Furthermore, we think libraries of formalized mathematics have the potential to be useful, and informative resources for mathematicians. Our library is designed to work towards this goal, and we welcome contributions to the library about any topic in mathematics.

The library is built in Agda 2.6.2. It can be compiled by running `make check` from the main folder of the repository.

## Joining the project

Great, you want to contribute something! The best way to start is to find us in our chat channels on the [agda-unimath discord](https://discord.gg/Zp2e8hYsuX). We have a vibing community there, and you're more than welcome to join us just to hang out.

Once you've decided what you want to contribute, the best way to proceed is to make your own fork of the library. Within your fork, make a separate branch in which you will be making your contributions. Now you're ready to start your project! When you've completed your formalization you can proceed by making a pull request. Then we will review your contributions, and merge it when it is ready for the `agda-unimath` library.

## Statement of inclusion

There are many reasons to contribute something to a library of formalized mathematics. Some do it just for fun, some do it for their research, some do it to learn something. Whatever your reason is, we welcome your contributions! To keep the experience of contributing something to our library enjoyable for everyone, we strive for an inclusive community of contributors. You can expect from us that we are kind and respectful in discussions, that we will be mindful of your pronouns and use [inclusive language](https://www.apa.org/about/apa/equity-diversity-inclusion/language-guidelines), and that we value your input regardless of your level of experience or status in the community. We're commited to providing a safe and welcoming environment to people of any gender identity, sexual orientation, race, colour, age, ability, ethnicity, background, or fluency in English -- here on github, in online communication channels, and in person. Homotopy type theory is difficult enough without all the barriers that many of us have to face, so we hope to bring some of those down a bit.

:rainbow: Happy contributing!

Elisabeth Bonnevier
Jonathan Prieto-Cubides
Egbert Rijke

<pre class="Agda"><a id="2976" class="Symbol">{-#</a> <a id="2980" class="Keyword">OPTIONS</a> <a id="2988" class="Pragma">--without-K</a> <a id="3000" class="Pragma">--exact-split</a> <a id="3014" class="Pragma">--guardedness</a> <a id="3028" class="Symbol">#-}</a>
</pre>
See the list of all Agda modules [here](everything.html).

## Category theory

<pre class="Agda"><a id="3124" class="Keyword">open</a> <a id="3129" class="Keyword">import</a> <a id="3136" href="category-theory.html" class="Module">category-theory</a>
<a id="3152" class="Keyword">open</a> <a id="3157" class="Keyword">import</a> <a id="3164" href="category-theory.adjunctions-large-precategories.html" class="Module">category-theory.adjunctions-large-precategories</a>
<a id="3212" class="Keyword">open</a> <a id="3217" class="Keyword">import</a> <a id="3224" href="category-theory.anafunctors.html" class="Module">category-theory.anafunctors</a>
<a id="3252" class="Keyword">open</a> <a id="3257" class="Keyword">import</a> <a id="3264" href="category-theory.categories.html" class="Module">category-theory.categories</a>
<a id="3291" class="Keyword">open</a> <a id="3296" class="Keyword">import</a> <a id="3303" href="category-theory.epimorphisms-large-precategories.html" class="Module">category-theory.epimorphisms-large-precategories</a>
<a id="3352" class="Keyword">open</a> <a id="3357" class="Keyword">import</a> <a id="3364" href="category-theory.equivalences-categories.html" class="Module">category-theory.equivalences-categories</a>
<a id="3404" class="Keyword">open</a> <a id="3409" class="Keyword">import</a> <a id="3416" href="category-theory.equivalences-large-precategories.html" class="Module">category-theory.equivalences-large-precategories</a>
<a id="3465" class="Keyword">open</a> <a id="3470" class="Keyword">import</a> <a id="3477" href="category-theory.equivalences-precategories.html" class="Module">category-theory.equivalences-precategories</a>
<a id="3520" class="Keyword">open</a> <a id="3525" class="Keyword">import</a> <a id="3532" href="category-theory.functors-categories.html" class="Module">category-theory.functors-categories</a>
<a id="3568" class="Keyword">open</a> <a id="3573" class="Keyword">import</a> <a id="3580" href="category-theory.functors-large-precategories.html" class="Module">category-theory.functors-large-precategories</a>
<a id="3625" class="Keyword">open</a> <a id="3630" class="Keyword">import</a> <a id="3637" href="category-theory.functors-precategories.html" class="Module">category-theory.functors-precategories</a>
<a id="3676" class="Keyword">open</a> <a id="3681" class="Keyword">import</a> <a id="3688" href="category-theory.homotopies-natural-transformations-large-precategories.html" class="Module">category-theory.homotopies-natural-transformations-large-precategories</a>
<a id="3759" class="Keyword">open</a> <a id="3764" class="Keyword">import</a> <a id="3771" href="category-theory.initial-objects-precategories.html" class="Module">category-theory.initial-objects-precategories</a>
<a id="3817" class="Keyword">open</a> <a id="3822" class="Keyword">import</a> <a id="3829" href="category-theory.isomorphisms-categories.html" class="Module">category-theory.isomorphisms-categories</a>
<a id="3869" class="Keyword">open</a> <a id="3874" class="Keyword">import</a> <a id="3881" href="category-theory.isomorphisms-large-precategories.html" class="Module">category-theory.isomorphisms-large-precategories</a>
<a id="3930" class="Keyword">open</a> <a id="3935" class="Keyword">import</a> <a id="3942" href="category-theory.isomorphisms-precategories.html" class="Module">category-theory.isomorphisms-precategories</a>
<a id="3985" class="Keyword">open</a> <a id="3990" class="Keyword">import</a> <a id="3997" href="category-theory.large-categories.html" class="Module">category-theory.large-categories</a>
<a id="4030" class="Keyword">open</a> <a id="4035" class="Keyword">import</a> <a id="4042" href="category-theory.large-precategories.html" class="Module">category-theory.large-precategories</a>
<a id="4078" class="Keyword">open</a> <a id="4083" class="Keyword">import</a> <a id="4090" href="category-theory.monomorphisms-large-precategories.html" class="Module">category-theory.monomorphisms-large-precategories</a>
<a id="4140" class="Keyword">open</a> <a id="4145" class="Keyword">import</a> <a id="4152" href="category-theory.natural-isomorphisms-categories.html" class="Module">category-theory.natural-isomorphisms-categories</a>
<a id="4200" class="Keyword">open</a> <a id="4205" class="Keyword">import</a> <a id="4212" href="category-theory.natural-isomorphisms-large-precategories.html" class="Module">category-theory.natural-isomorphisms-large-precategories</a>
<a id="4269" class="Keyword">open</a> <a id="4274" class="Keyword">import</a> <a id="4281" href="category-theory.natural-isomorphisms-precategories.html" class="Module">category-theory.natural-isomorphisms-precategories</a>
<a id="4332" class="Keyword">open</a> <a id="4337" class="Keyword">import</a> <a id="4344" href="category-theory.natural-transformations-categories.html" class="Module">category-theory.natural-transformations-categories</a>
<a id="4395" class="Keyword">open</a> <a id="4400" class="Keyword">import</a> <a id="4407" href="category-theory.natural-transformations-large-precategories.html" class="Module">category-theory.natural-transformations-large-precategories</a>
<a id="4467" class="Keyword">open</a> <a id="4472" class="Keyword">import</a> <a id="4479" href="category-theory.natural-transformations-precategories.html" class="Module">category-theory.natural-transformations-precategories</a>
<a id="4533" class="Keyword">open</a> <a id="4538" class="Keyword">import</a> <a id="4545" href="category-theory.precategories.html" class="Module">category-theory.precategories</a>
<a id="4575" class="Keyword">open</a> <a id="4580" class="Keyword">import</a> <a id="4587" href="category-theory.slice-precategories.html" class="Module">category-theory.slice-precategories</a>
<a id="4623" class="Keyword">open</a> <a id="4628" class="Keyword">import</a> <a id="4635" href="category-theory.terminal-objects-precategories.html" class="Module">category-theory.terminal-objects-precategories</a>
</pre>
## Commutative algebra

<pre class="Agda"><a id="4719" class="Keyword">open</a> <a id="4724" class="Keyword">import</a> <a id="4731" href="commutative-algebra.html" class="Module">commutative-algebra</a>
<a id="4751" class="Keyword">open</a> <a id="4756" class="Keyword">import</a> <a id="4763" href="commutative-algebra.commutative-rings.html" class="Module">commutative-algebra.commutative-rings</a>
<a id="4801" class="Keyword">open</a> <a id="4806" class="Keyword">import</a> <a id="4813" href="commutative-algebra.discrete-fields.html" class="Module">commutative-algebra.discrete-fields</a>
<a id="4849" class="Keyword">open</a> <a id="4854" class="Keyword">import</a> <a id="4861" href="commutative-algebra.eisenstein-integers.html" class="Module">commutative-algebra.eisenstein-integers</a>
<a id="4901" class="Keyword">open</a> <a id="4906" class="Keyword">import</a> <a id="4913" href="commutative-algebra.gaussian-integers.html" class="Module">commutative-algebra.gaussian-integers</a>
<a id="4951" class="Keyword">open</a> <a id="4956" class="Keyword">import</a> <a id="4963" href="commutative-algebra.homomorphisms-commutative-rings.html" class="Module">commutative-algebra.homomorphisms-commutative-rings</a>
<a id="5015" class="Keyword">open</a> <a id="5020" class="Keyword">import</a> <a id="5027" href="commutative-algebra.ideals-commutative-rings.html" class="Module">commutative-algebra.ideals-commutative-rings</a>
<a id="5072" class="Keyword">open</a> <a id="5077" class="Keyword">import</a> <a id="5084" href="commutative-algebra.integral-domains.html" class="Module">commutative-algebra.integral-domains</a>
<a id="5121" class="Keyword">open</a> <a id="5126" class="Keyword">import</a> <a id="5133" href="commutative-algebra.isomorphisms-commutative-rings.html" class="Module">commutative-algebra.isomorphisms-commutative-rings</a>
<a id="5184" class="Keyword">open</a> <a id="5189" class="Keyword">import</a> <a id="5196" href="commutative-algebra.prime-ideals-commutative-rings.html" class="Module">commutative-algebra.prime-ideals-commutative-rings</a>
<a id="5247" class="Keyword">open</a> <a id="5252" class="Keyword">import</a> <a id="5259" href="commutative-algebra.zarisky-topology.html" class="Module">commutative-algebra.zarisky-topology</a>
</pre>
## Elementary number theory

<pre class="Agda"><a id="5338" class="Keyword">open</a> <a id="5343" class="Keyword">import</a> <a id="5350" href="elementary-number-theory.html" class="Module">elementary-number-theory</a>
<a id="5375" class="Keyword">open</a> <a id="5380" class="Keyword">import</a> <a id="5387" href="elementary-number-theory.absolute-value-integers.html" class="Module">elementary-number-theory.absolute-value-integers</a>
<a id="5436" class="Keyword">open</a> <a id="5441" class="Keyword">import</a> <a id="5448" href="elementary-number-theory.addition-integers.html" class="Module">elementary-number-theory.addition-integers</a>
<a id="5491" class="Keyword">open</a> <a id="5496" class="Keyword">import</a> <a id="5503" href="elementary-number-theory.addition-natural-numbers.html" class="Module">elementary-number-theory.addition-natural-numbers</a>
<a id="5553" class="Keyword">open</a> <a id="5558" class="Keyword">import</a> <a id="5565" href="elementary-number-theory.arithmetic-functions.html" class="Module">elementary-number-theory.arithmetic-functions</a>
<a id="5611" class="Keyword">open</a> <a id="5616" class="Keyword">import</a> <a id="5623" href="elementary-number-theory.binomial-coefficients.html" class="Module">elementary-number-theory.binomial-coefficients</a>
<a id="5670" class="Keyword">open</a> <a id="5675" class="Keyword">import</a> <a id="5682" href="elementary-number-theory.bounded-sums-arithmetic-functions.html" class="Module">elementary-number-theory.bounded-sums-arithmetic-functions</a>
<a id="5741" class="Keyword">open</a> <a id="5746" class="Keyword">import</a> <a id="5753" href="elementary-number-theory.catalan-numbers.html" class="Module">elementary-number-theory.catalan-numbers</a>
<a id="5794" class="Keyword">open</a> <a id="5799" class="Keyword">import</a> <a id="5806" href="elementary-number-theory.collatz-bijection.html" class="Module">elementary-number-theory.collatz-bijection</a>
<a id="5849" class="Keyword">open</a> <a id="5854" class="Keyword">import</a> <a id="5861" href="elementary-number-theory.collatz-conjecture.html" class="Module">elementary-number-theory.collatz-conjecture</a>
<a id="5905" class="Keyword">open</a> <a id="5910" class="Keyword">import</a> <a id="5917" href="elementary-number-theory.congruence-integers.html" class="Module">elementary-number-theory.congruence-integers</a>
<a id="5962" class="Keyword">open</a> <a id="5967" class="Keyword">import</a> <a id="5974" href="elementary-number-theory.congruence-natural-numbers.html" class="Module">elementary-number-theory.congruence-natural-numbers</a>
<a id="6026" class="Keyword">open</a> <a id="6031" class="Keyword">import</a> <a id="6038" href="elementary-number-theory.decidable-dependent-function-types.html" class="Module">elementary-number-theory.decidable-dependent-function-types</a>
<a id="6098" class="Keyword">open</a> <a id="6103" class="Keyword">import</a> <a id="6110" href="elementary-number-theory.decidable-types.html" class="Module">elementary-number-theory.decidable-types</a>
<a id="6151" class="Keyword">open</a> <a id="6156" class="Keyword">import</a> <a id="6163" href="elementary-number-theory.difference-integers.html" class="Module">elementary-number-theory.difference-integers</a>
<a id="6208" class="Keyword">open</a> <a id="6213" class="Keyword">import</a> <a id="6220" href="elementary-number-theory.dirichlet-convolution.html" class="Module">elementary-number-theory.dirichlet-convolution</a>
<a id="6267" class="Keyword">open</a> <a id="6272" class="Keyword">import</a> <a id="6279" href="elementary-number-theory.distance-integers.html" class="Module">elementary-number-theory.distance-integers</a>
<a id="6322" class="Keyword">open</a> <a id="6327" class="Keyword">import</a> <a id="6334" href="elementary-number-theory.distance-natural-numbers.html" class="Module">elementary-number-theory.distance-natural-numbers</a>
<a id="6384" class="Keyword">open</a> <a id="6389" class="Keyword">import</a> <a id="6396" href="elementary-number-theory.divisibility-integers.html" class="Module">elementary-number-theory.divisibility-integers</a>
<a id="6443" class="Keyword">open</a> <a id="6448" class="Keyword">import</a> <a id="6455" href="elementary-number-theory.divisibility-modular-arithmetic.html" class="Module">elementary-number-theory.divisibility-modular-arithmetic</a>
<a id="6512" class="Keyword">open</a> <a id="6517" class="Keyword">import</a> <a id="6524" href="elementary-number-theory.divisibility-natural-numbers.html" class="Module">elementary-number-theory.divisibility-natural-numbers</a>
<a id="6578" class="Keyword">open</a> <a id="6583" class="Keyword">import</a> <a id="6590" href="elementary-number-theory.divisibility-standard-finite-types.html" class="Module">elementary-number-theory.divisibility-standard-finite-types</a>
<a id="6650" class="Keyword">open</a> <a id="6655" class="Keyword">import</a> <a id="6662" href="elementary-number-theory.equality-integers.html" class="Module">elementary-number-theory.equality-integers</a>
<a id="6705" class="Keyword">open</a> <a id="6710" class="Keyword">import</a> <a id="6717" href="elementary-number-theory.equality-natural-numbers.html" class="Module">elementary-number-theory.equality-natural-numbers</a>
<a id="6767" class="Keyword">open</a> <a id="6772" class="Keyword">import</a> <a id="6779" href="elementary-number-theory.euclidean-division-natural-numbers.html" class="Module">elementary-number-theory.euclidean-division-natural-numbers</a>
<a id="6839" class="Keyword">open</a> <a id="6844" class="Keyword">import</a> <a id="6851" href="elementary-number-theory.eulers-totient-function.html" class="Module">elementary-number-theory.eulers-totient-function</a>
<a id="6900" class="Keyword">open</a> <a id="6905" class="Keyword">import</a> <a id="6912" href="elementary-number-theory.exponentiation-natural-numbers.html" class="Module">elementary-number-theory.exponentiation-natural-numbers</a>
<a id="6968" class="Keyword">open</a> <a id="6973" class="Keyword">import</a> <a id="6980" href="elementary-number-theory.factorials.html" class="Module">elementary-number-theory.factorials</a>
<a id="7016" class="Keyword">open</a> <a id="7021" class="Keyword">import</a> <a id="7028" href="elementary-number-theory.falling-factorials.html" class="Module">elementary-number-theory.falling-factorials</a>
<a id="7072" class="Keyword">open</a> <a id="7077" class="Keyword">import</a> <a id="7084" href="elementary-number-theory.fibonacci-sequence.html" class="Module">elementary-number-theory.fibonacci-sequence</a>
<a id="7128" class="Keyword">open</a> <a id="7133" class="Keyword">import</a> <a id="7140" href="elementary-number-theory.finitary-natural-numbers.html" class="Module">elementary-number-theory.finitary-natural-numbers</a>
<a id="7190" class="Keyword">open</a> <a id="7195" class="Keyword">import</a> <a id="7202" href="elementary-number-theory.finitely-cyclic-maps.html" class="Module">elementary-number-theory.finitely-cyclic-maps</a>
<a id="7248" class="Keyword">open</a> <a id="7253" class="Keyword">import</a> <a id="7260" href="elementary-number-theory.fractions.html" class="Module">elementary-number-theory.fractions</a>
<a id="7295" class="Keyword">open</a> <a id="7300" class="Keyword">import</a> <a id="7307" href="elementary-number-theory.goldbach-conjecture.html" class="Module">elementary-number-theory.goldbach-conjecture</a>
<a id="7352" class="Keyword">open</a> <a id="7357" class="Keyword">import</a> <a id="7364" href="elementary-number-theory.greatest-common-divisor-integers.html" class="Module">elementary-number-theory.greatest-common-divisor-integers</a>
<a id="7422" class="Keyword">open</a> <a id="7427" class="Keyword">import</a> <a id="7434" href="elementary-number-theory.greatest-common-divisor-natural-numbers.html" class="Module">elementary-number-theory.greatest-common-divisor-natural-numbers</a>
<a id="7499" class="Keyword">open</a> <a id="7504" class="Keyword">import</a> <a id="7511" href="elementary-number-theory.group-of-integers.html" class="Module">elementary-number-theory.group-of-integers</a>
<a id="7554" class="Keyword">open</a> <a id="7559" class="Keyword">import</a> <a id="7566" href="elementary-number-theory.groups-of-modular-arithmetic.html" class="Module">elementary-number-theory.groups-of-modular-arithmetic</a>
<a id="7620" class="Keyword">open</a> <a id="7625" class="Keyword">import</a> <a id="7632" href="elementary-number-theory.inequality-integers.html" class="Module">elementary-number-theory.inequality-integers</a>
<a id="7677" class="Keyword">open</a> <a id="7682" class="Keyword">import</a> <a id="7689" href="elementary-number-theory.inequality-natural-numbers.html" class="Module">elementary-number-theory.inequality-natural-numbers</a>
<a id="7741" class="Keyword">open</a> <a id="7746" class="Keyword">import</a> <a id="7753" href="elementary-number-theory.inequality-standard-finite-types.html" class="Module">elementary-number-theory.inequality-standard-finite-types</a>
<a id="7811" class="Keyword">open</a> <a id="7816" class="Keyword">import</a> <a id="7823" href="elementary-number-theory.infinitude-of-primes.html" class="Module">elementary-number-theory.infinitude-of-primes</a>
<a id="7869" class="Keyword">open</a> <a id="7874" class="Keyword">import</a> <a id="7881" href="elementary-number-theory.integer-partitions.html" class="Module">elementary-number-theory.integer-partitions</a>
<a id="7925" class="Keyword">open</a> <a id="7930" class="Keyword">import</a> <a id="7937" href="elementary-number-theory.integers.html" class="Module">elementary-number-theory.integers</a>
<a id="7971" class="Keyword">open</a> <a id="7976" class="Keyword">import</a> <a id="7983" href="elementary-number-theory.lower-bounds-natural-numbers.html" class="Module">elementary-number-theory.lower-bounds-natural-numbers</a>
<a id="8037" class="Keyword">open</a> <a id="8042" class="Keyword">import</a> <a id="8049" href="elementary-number-theory.maximum-natural-numbers.html" class="Module">elementary-number-theory.maximum-natural-numbers</a>
<a id="8098" class="Keyword">open</a> <a id="8103" class="Keyword">import</a> <a id="8110" href="elementary-number-theory.mersenne-primes.html" class="Module">elementary-number-theory.mersenne-primes</a>
<a id="8151" class="Keyword">open</a> <a id="8156" class="Keyword">import</a> <a id="8163" href="elementary-number-theory.minimum-natural-numbers.html" class="Module">elementary-number-theory.minimum-natural-numbers</a>
<a id="8212" class="Keyword">open</a> <a id="8217" class="Keyword">import</a> <a id="8224" href="elementary-number-theory.modular-arithmetic-standard-finite-types.html" class="Module">elementary-number-theory.modular-arithmetic-standard-finite-types</a>
<a id="8290" class="Keyword">open</a> <a id="8295" class="Keyword">import</a> <a id="8302" href="elementary-number-theory.modular-arithmetic.html" class="Module">elementary-number-theory.modular-arithmetic</a>
<a id="8346" class="Keyword">open</a> <a id="8351" class="Keyword">import</a> <a id="8358" href="elementary-number-theory.multiplication-integers.html" class="Module">elementary-number-theory.multiplication-integers</a>
<a id="8407" class="Keyword">open</a> <a id="8412" class="Keyword">import</a> <a id="8419" href="elementary-number-theory.multiplication-natural-numbers.html" class="Module">elementary-number-theory.multiplication-natural-numbers</a>
<a id="8475" class="Keyword">open</a> <a id="8480" class="Keyword">import</a> <a id="8487" href="elementary-number-theory.natural-numbers.html" class="Module">elementary-number-theory.natural-numbers</a>
<a id="8528" class="Keyword">open</a> <a id="8533" class="Keyword">import</a> <a id="8540" href="elementary-number-theory.nonzero-natural-numbers.html" class="Module">elementary-number-theory.nonzero-natural-numbers</a>
<a id="8589" class="Keyword">open</a> <a id="8594" class="Keyword">import</a> <a id="8601" href="elementary-number-theory.ordinal-induction-natural-numbers.html" class="Module">elementary-number-theory.ordinal-induction-natural-numbers</a>
<a id="8660" class="Keyword">open</a> <a id="8665" class="Keyword">import</a> <a id="8672" href="elementary-number-theory.prime-numbers.html" class="Module">elementary-number-theory.prime-numbers</a>
<a id="8711" class="Keyword">open</a> <a id="8716" class="Keyword">import</a> <a id="8723" href="elementary-number-theory.products-of-natural-numbers.html" class="Module">elementary-number-theory.products-of-natural-numbers</a>
<a id="8776" class="Keyword">open</a> <a id="8781" class="Keyword">import</a> <a id="8788" href="elementary-number-theory.proper-divisors-natural-numbers.html" class="Module">elementary-number-theory.proper-divisors-natural-numbers</a>
<a id="8845" class="Keyword">open</a> <a id="8850" class="Keyword">import</a> <a id="8857" href="elementary-number-theory.rational-numbers.html" class="Module">elementary-number-theory.rational-numbers</a>
<a id="8899" class="Keyword">open</a> <a id="8904" class="Keyword">import</a> <a id="8911" href="elementary-number-theory.relatively-prime-integers.html" class="Module">elementary-number-theory.relatively-prime-integers</a>
<a id="8962" class="Keyword">open</a> <a id="8967" class="Keyword">import</a> <a id="8974" href="elementary-number-theory.relatively-prime-natural-numbers.html" class="Module">elementary-number-theory.relatively-prime-natural-numbers</a>
<a id="9032" class="Keyword">open</a> <a id="9037" class="Keyword">import</a> <a id="9044" href="elementary-number-theory.repeating-element-standard-finite-type.html" class="Module">elementary-number-theory.repeating-element-standard-finite-type</a>
<a id="9108" class="Keyword">open</a> <a id="9113" class="Keyword">import</a> <a id="9120" href="elementary-number-theory.retracts-of-natural-numbers.html" class="Module">elementary-number-theory.retracts-of-natural-numbers</a>
<a id="9173" class="Keyword">open</a> <a id="9178" class="Keyword">import</a> <a id="9185" href="elementary-number-theory.square-free-natural-numbers.html" class="Module">elementary-number-theory.square-free-natural-numbers</a>
<a id="9238" class="Keyword">open</a> <a id="9243" class="Keyword">import</a> <a id="9250" href="elementary-number-theory.stirling-numbers-of-the-second-kind.html" class="Module">elementary-number-theory.stirling-numbers-of-the-second-kind</a>
<a id="9311" class="Keyword">open</a> <a id="9316" class="Keyword">import</a> <a id="9323" href="elementary-number-theory.strong-induction-natural-numbers.html" class="Module">elementary-number-theory.strong-induction-natural-numbers</a>
<a id="9381" class="Keyword">open</a> <a id="9386" class="Keyword">import</a> <a id="9393" href="elementary-number-theory.sums-of-natural-numbers.html" class="Module">elementary-number-theory.sums-of-natural-numbers</a>
<a id="9442" class="Keyword">open</a> <a id="9447" class="Keyword">import</a> <a id="9454" href="elementary-number-theory.telephone-numbers.html" class="Module">elementary-number-theory.telephone-numbers</a>
<a id="9497" class="Keyword">open</a> <a id="9502" class="Keyword">import</a> <a id="9509" href="elementary-number-theory.triangular-numbers.html" class="Module">elementary-number-theory.triangular-numbers</a>
<a id="9553" class="Keyword">open</a> <a id="9558" class="Keyword">import</a> <a id="9565" href="elementary-number-theory.twin-prime-conjecture.html" class="Module">elementary-number-theory.twin-prime-conjecture</a>
<a id="9612" class="Keyword">open</a> <a id="9617" class="Keyword">import</a> <a id="9624" href="elementary-number-theory.unit-elements-standard-finite-types.html" class="Module">elementary-number-theory.unit-elements-standard-finite-types</a>
<a id="9685" class="Keyword">open</a> <a id="9690" class="Keyword">import</a> <a id="9697" href="elementary-number-theory.unit-similarity-standard-finite-types.html" class="Module">elementary-number-theory.unit-similarity-standard-finite-types</a>
<a id="9760" class="Keyword">open</a> <a id="9765" class="Keyword">import</a> <a id="9772" href="elementary-number-theory.universal-property-natural-numbers.html" class="Module">elementary-number-theory.universal-property-natural-numbers</a>
<a id="9832" class="Keyword">open</a> <a id="9837" class="Keyword">import</a> <a id="9844" href="elementary-number-theory.upper-bounds-natural-numbers.html" class="Module">elementary-number-theory.upper-bounds-natural-numbers</a>
<a id="9898" class="Keyword">open</a> <a id="9903" class="Keyword">import</a> <a id="9910" href="elementary-number-theory.well-ordering-principle-natural-numbers.html" class="Module">elementary-number-theory.well-ordering-principle-natural-numbers</a>
<a id="9975" class="Keyword">open</a> <a id="9980" class="Keyword">import</a> <a id="9987" href="elementary-number-theory.well-ordering-principle-standard-finite-types.html" class="Module">elementary-number-theory.well-ordering-principle-standard-finite-types</a>
</pre>
## Finite group theory

<pre class="Agda"><a id="10095" class="Keyword">open</a> <a id="10100" class="Keyword">import</a> <a id="10107" href="finite-group-theory.html" class="Module">finite-group-theory</a>
<a id="10127" class="Keyword">open</a> <a id="10132" class="Keyword">import</a> <a id="10139" href="finite-group-theory.abstract-quaternion-group.html" class="Module">finite-group-theory.abstract-quaternion-group</a>
<a id="10185" class="Keyword">open</a> <a id="10190" class="Keyword">import</a> <a id="10197" href="finite-group-theory.concrete-quaternion-group.html" class="Module">finite-group-theory.concrete-quaternion-group</a>
<a id="10243" class="Keyword">open</a> <a id="10248" class="Keyword">import</a> <a id="10255" href="finite-group-theory.finite-groups.html" class="Module">finite-group-theory.finite-groups</a>
<a id="10289" class="Keyword">open</a> <a id="10294" class="Keyword">import</a> <a id="10301" href="finite-group-theory.finite-monoids.html" class="Module">finite-group-theory.finite-monoids</a>
<a id="10336" class="Keyword">open</a> <a id="10341" class="Keyword">import</a> <a id="10348" href="finite-group-theory.finite-semigroups.html" class="Module">finite-group-theory.finite-semigroups</a>
<a id="10386" class="Keyword">open</a> <a id="10391" class="Keyword">import</a> <a id="10398" href="finite-group-theory.groups-of-order-2.html" class="Module">finite-group-theory.groups-of-order-2</a>
<a id="10436" class="Keyword">open</a> <a id="10441" class="Keyword">import</a> <a id="10448" href="finite-group-theory.orbits-permutations.html" class="Module">finite-group-theory.orbits-permutations</a>
<a id="10488" class="Keyword">open</a> <a id="10493" class="Keyword">import</a> <a id="10500" href="finite-group-theory.permutations.html" class="Module">finite-group-theory.permutations</a>
<a id="10533" class="Keyword">open</a> <a id="10538" class="Keyword">import</a> <a id="10545" href="finite-group-theory.sign-homomorphism.html" class="Module">finite-group-theory.sign-homomorphism</a>
<a id="10583" class="Keyword">open</a> <a id="10588" class="Keyword">import</a> <a id="10595" href="finite-group-theory.transpositions.html" class="Module">finite-group-theory.transpositions</a>
</pre>
## Foundation

<pre class="Agda"><a id="10658" class="Keyword">open</a> <a id="10663" class="Keyword">import</a> <a id="10670" href="foundation.html" class="Module">foundation</a>
<a id="10681" class="Keyword">open</a> <a id="10686" class="Keyword">import</a> <a id="10693" href="foundation.0-maps.html" class="Module">foundation.0-maps</a>
<a id="10711" class="Keyword">open</a> <a id="10716" class="Keyword">import</a> <a id="10723" href="foundation.1-types.html" class="Module">foundation.1-types</a>
<a id="10742" class="Keyword">open</a> <a id="10747" class="Keyword">import</a> <a id="10754" href="foundation.2-types.html" class="Module">foundation.2-types</a>
<a id="10773" class="Keyword">open</a> <a id="10778" class="Keyword">import</a> <a id="10785" href="foundation.algebras-polynomial-endofunctors.html" class="Module">foundation.algebras-polynomial-endofunctors</a>
<a id="10829" class="Keyword">open</a> <a id="10834" class="Keyword">import</a> <a id="10841" href="foundation.automorphisms.html" class="Module">foundation.automorphisms</a>
<a id="10866" class="Keyword">open</a> <a id="10871" class="Keyword">import</a> <a id="10878" href="foundation.axiom-of-choice.html" class="Module">foundation.axiom-of-choice</a>
<a id="10905" class="Keyword">open</a> <a id="10910" class="Keyword">import</a> <a id="10917" href="foundation.bands.html" class="Module">foundation.bands</a>
<a id="10934" class="Keyword">open</a> <a id="10939" class="Keyword">import</a> <a id="10946" href="foundation.binary-embeddings.html" class="Module">foundation.binary-embeddings</a>
<a id="10975" class="Keyword">open</a> <a id="10980" class="Keyword">import</a> <a id="10987" href="foundation.binary-equivalences-unordered-pairs-of-types.html" class="Module">foundation.binary-equivalences-unordered-pairs-of-types</a>
<a id="11043" class="Keyword">open</a> <a id="11048" class="Keyword">import</a> <a id="11055" href="foundation.binary-equivalences.html" class="Module">foundation.binary-equivalences</a>
<a id="11086" class="Keyword">open</a> <a id="11091" class="Keyword">import</a> <a id="11098" href="foundation.binary-operations-unordered-pairs-of-types.html" class="Module">foundation.binary-operations-unordered-pairs-of-types</a>
<a id="11152" class="Keyword">open</a> <a id="11157" class="Keyword">import</a> <a id="11164" href="foundation.binary-relations.html" class="Module">foundation.binary-relations</a>
<a id="11192" class="Keyword">open</a> <a id="11197" class="Keyword">import</a> <a id="11204" href="foundation.boolean-reflection.html" class="Module">foundation.boolean-reflection</a>
<a id="11234" class="Keyword">open</a> <a id="11239" class="Keyword">import</a> <a id="11246" href="foundation.booleans.html" class="Module">foundation.booleans</a>
<a id="11266" class="Keyword">open</a> <a id="11271" class="Keyword">import</a> <a id="11278" href="foundation.cantor-schroder-bernstein-escardo.html" class="Module">foundation.cantor-schroder-bernstein-escardo</a>
<a id="11323" class="Keyword">open</a> <a id="11328" class="Keyword">import</a> <a id="11335" href="foundation.cantors-diagonal-argument.html" class="Module">foundation.cantors-diagonal-argument</a>
<a id="11372" class="Keyword">open</a> <a id="11377" class="Keyword">import</a> <a id="11384" href="foundation.cartesian-product-types.html" class="Module">foundation.cartesian-product-types</a>
<a id="11419" class="Keyword">open</a> <a id="11424" class="Keyword">import</a> <a id="11431" href="foundation.choice-of-representatives-equivalence-relation.html" class="Module">foundation.choice-of-representatives-equivalence-relation</a>
<a id="11489" class="Keyword">open</a> <a id="11494" class="Keyword">import</a> <a id="11501" href="foundation.coherently-invertible-maps.html" class="Module">foundation.coherently-invertible-maps</a>
<a id="11539" class="Keyword">open</a> <a id="11544" class="Keyword">import</a> <a id="11551" href="foundation.commutative-operations.html" class="Module">foundation.commutative-operations</a>
<a id="11585" class="Keyword">open</a> <a id="11590" class="Keyword">import</a> <a id="11597" href="foundation.commuting-squares.html" class="Module">foundation.commuting-squares</a>
<a id="11626" class="Keyword">open</a> <a id="11631" class="Keyword">import</a> <a id="11638" href="foundation.complements.html" class="Module">foundation.complements</a>
<a id="11661" class="Keyword">open</a> <a id="11666" class="Keyword">import</a> <a id="11673" href="foundation.cones-pullbacks.html" class="Module">foundation.cones-pullbacks</a>
<a id="11700" class="Keyword">open</a> <a id="11705" class="Keyword">import</a> <a id="11712" href="foundation.conjunction.html" class="Module">foundation.conjunction</a>
<a id="11735" class="Keyword">open</a> <a id="11740" class="Keyword">import</a> <a id="11747" href="foundation.connected-components-universes.html" class="Module">foundation.connected-components-universes</a>
<a id="11789" class="Keyword">open</a> <a id="11794" class="Keyword">import</a> <a id="11801" href="foundation.connected-components.html" class="Module">foundation.connected-components</a>
<a id="11833" class="Keyword">open</a> <a id="11838" class="Keyword">import</a> <a id="11845" href="foundation.connected-types.html" class="Module">foundation.connected-types</a>
<a id="11872" class="Keyword">open</a> <a id="11877" class="Keyword">import</a> <a id="11884" href="foundation.constant-maps.html" class="Module">foundation.constant-maps</a>
<a id="11909" class="Keyword">open</a> <a id="11914" class="Keyword">import</a> <a id="11921" href="foundation.contractible-maps.html" class="Module">foundation.contractible-maps</a>
<a id="11950" class="Keyword">open</a> <a id="11955" class="Keyword">import</a> <a id="11962" href="foundation.contractible-types.html" class="Module">foundation.contractible-types</a>
<a id="11992" class="Keyword">open</a> <a id="11997" class="Keyword">import</a> <a id="12004" href="foundation.coproduct-types.html" class="Module">foundation.coproduct-types</a>
<a id="12031" class="Keyword">open</a> <a id="12036" class="Keyword">import</a> <a id="12043" href="foundation.coslice.html" class="Module">foundation.coslice</a>
<a id="12062" class="Keyword">open</a> <a id="12067" class="Keyword">import</a> <a id="12074" href="foundation.decidable-dependent-function-types.html" class="Module">foundation.decidable-dependent-function-types</a>
<a id="12120" class="Keyword">open</a> <a id="12125" class="Keyword">import</a> <a id="12132" href="foundation.decidable-dependent-pair-types.html" class="Module">foundation.decidable-dependent-pair-types</a>
<a id="12174" class="Keyword">open</a> <a id="12179" class="Keyword">import</a> <a id="12186" href="foundation.decidable-embeddings.html" class="Module">foundation.decidable-embeddings</a>
<a id="12218" class="Keyword">open</a> <a id="12223" class="Keyword">import</a> <a id="12230" href="foundation.decidable-equality.html" class="Module">foundation.decidable-equality</a>
<a id="12260" class="Keyword">open</a> <a id="12265" class="Keyword">import</a> <a id="12272" href="foundation.decidable-maps.html" class="Module">foundation.decidable-maps</a>
<a id="12298" class="Keyword">open</a> <a id="12303" class="Keyword">import</a> <a id="12310" href="foundation.decidable-propositions.html" class="Module">foundation.decidable-propositions</a>
<a id="12344" class="Keyword">open</a> <a id="12349" class="Keyword">import</a> <a id="12356" href="foundation.decidable-subtypes.html" class="Module">foundation.decidable-subtypes</a>
<a id="12386" class="Keyword">open</a> <a id="12391" class="Keyword">import</a> <a id="12398" href="foundation.decidable-types.html" class="Module">foundation.decidable-types</a>
<a id="12425" class="Keyword">open</a> <a id="12430" class="Keyword">import</a> <a id="12437" href="foundation.dependent-pair-types.html" class="Module">foundation.dependent-pair-types</a>
<a id="12469" class="Keyword">open</a> <a id="12474" class="Keyword">import</a> <a id="12481" href="foundation.diagonal-maps-of-types.html" class="Module">foundation.diagonal-maps-of-types</a>
<a id="12515" class="Keyword">open</a> <a id="12520" class="Keyword">import</a> <a id="12527" href="foundation.disjunction.html" class="Module">foundation.disjunction</a>
<a id="12550" class="Keyword">open</a> <a id="12555" class="Keyword">import</a> <a id="12562" href="foundation.distributivity-of-dependent-functions-over-coproduct-types.html" class="Module">foundation.distributivity-of-dependent-functions-over-coproduct-types</a>
<a id="12632" class="Keyword">open</a> <a id="12637" class="Keyword">import</a> <a id="12644" href="foundation.distributivity-of-dependent-functions-over-dependent-pairs.html" class="Module">foundation.distributivity-of-dependent-functions-over-dependent-pairs</a>
<a id="12714" class="Keyword">open</a> <a id="12719" class="Keyword">import</a> <a id="12726" href="foundation.double-negation.html" class="Module">foundation.double-negation</a>
<a id="12753" class="Keyword">open</a> <a id="12758" class="Keyword">import</a> <a id="12765" href="foundation.double-powersets.html" class="Module">foundation.double-powersets</a>
<a id="12793" class="Keyword">open</a> <a id="12798" class="Keyword">import</a> <a id="12805" href="foundation.dubuc-penon-compact-types.html" class="Module">foundation.dubuc-penon-compact-types</a>
<a id="12842" class="Keyword">open</a> <a id="12847" class="Keyword">import</a> <a id="12854" href="foundation.effective-maps-equivalence-relations.html" class="Module">foundation.effective-maps-equivalence-relations</a>
<a id="12902" class="Keyword">open</a> <a id="12907" class="Keyword">import</a> <a id="12914" href="foundation.elementhood-relation-w-types.html" class="Module">foundation.elementhood-relation-w-types</a>
<a id="12954" class="Keyword">open</a> <a id="12959" class="Keyword">import</a> <a id="12966" href="foundation.embeddings.html" class="Module">foundation.embeddings</a>
<a id="12988" class="Keyword">open</a> <a id="12993" class="Keyword">import</a> <a id="13000" href="foundation.empty-types.html" class="Module">foundation.empty-types</a>
<a id="13023" class="Keyword">open</a> <a id="13028" class="Keyword">import</a> <a id="13035" href="foundation.endomorphisms.html" class="Module">foundation.endomorphisms</a>
<a id="13060" class="Keyword">open</a> <a id="13065" class="Keyword">import</a> <a id="13072" href="foundation.epimorphisms-with-respect-to-sets.html" class="Module">foundation.epimorphisms-with-respect-to-sets</a>
<a id="13117" class="Keyword">open</a> <a id="13122" class="Keyword">import</a> <a id="13129" href="foundation.equality-cartesian-product-types.html" class="Module">foundation.equality-cartesian-product-types</a>
<a id="13173" class="Keyword">open</a> <a id="13178" class="Keyword">import</a> <a id="13185" href="foundation.equality-coproduct-types.html" class="Module">foundation.equality-coproduct-types</a>
<a id="13221" class="Keyword">open</a> <a id="13226" class="Keyword">import</a> <a id="13233" href="foundation.equality-dependent-function-types.html" class="Module">foundation.equality-dependent-function-types</a>
<a id="13278" class="Keyword">open</a> <a id="13283" class="Keyword">import</a> <a id="13290" href="foundation.equality-dependent-pair-types.html" class="Module">foundation.equality-dependent-pair-types</a>
<a id="13331" class="Keyword">open</a> <a id="13336" class="Keyword">import</a> <a id="13343" href="foundation.equality-fibers-of-maps.html" class="Module">foundation.equality-fibers-of-maps</a>
<a id="13378" class="Keyword">open</a> <a id="13383" class="Keyword">import</a> <a id="13390" href="foundation.equational-reasoning.html" class="Module">foundation.equational-reasoning</a>
<a id="13422" class="Keyword">open</a> <a id="13427" class="Keyword">import</a> <a id="13434" href="foundation.equivalence-classes.html" class="Module">foundation.equivalence-classes</a>
<a id="13465" class="Keyword">open</a> <a id="13470" class="Keyword">import</a> <a id="13477" href="foundation.equivalence-induction.html" class="Module">foundation.equivalence-induction</a>
<a id="13510" class="Keyword">open</a> <a id="13515" class="Keyword">import</a> <a id="13522" href="foundation.equivalence-relations.html" class="Module">foundation.equivalence-relations</a>
<a id="13555" class="Keyword">open</a> <a id="13560" class="Keyword">import</a> <a id="13567" href="foundation.equivalences-maybe.html" class="Module">foundation.equivalences-maybe</a>
<a id="13597" class="Keyword">open</a> <a id="13602" class="Keyword">import</a> <a id="13609" href="foundation.equivalences.html" class="Module">foundation.equivalences</a>
<a id="13633" class="Keyword">open</a> <a id="13638" class="Keyword">import</a> <a id="13645" href="foundation.existential-quantification.html" class="Module">foundation.existential-quantification</a>
<a id="13683" class="Keyword">open</a> <a id="13688" class="Keyword">import</a> <a id="13695" href="foundation.extensional-w-types.html" class="Module">foundation.extensional-w-types</a>
<a id="13726" class="Keyword">open</a> <a id="13731" class="Keyword">import</a> <a id="13738" href="foundation.faithful-maps.html" class="Module">foundation.faithful-maps</a>
<a id="13763" class="Keyword">open</a> <a id="13768" class="Keyword">import</a> <a id="13775" href="foundation.fiber-inclusions.html" class="Module">foundation.fiber-inclusions</a>
<a id="13803" class="Keyword">open</a> <a id="13808" class="Keyword">import</a> <a id="13815" href="foundation.fibered-maps.html" class="Module">foundation.fibered-maps</a>
<a id="13839" class="Keyword">open</a> <a id="13844" class="Keyword">import</a> <a id="13851" href="foundation.fibers-of-maps.html" class="Module">foundation.fibers-of-maps</a>
<a id="13877" class="Keyword">open</a> <a id="13882" class="Keyword">import</a> <a id="13889" href="foundation.function-extensionality.html" class="Module">foundation.function-extensionality</a>
<a id="13924" class="Keyword">open</a> <a id="13929" class="Keyword">import</a> <a id="13936" href="foundation.functions.html" class="Module">foundation.functions</a>
<a id="13957" class="Keyword">open</a> <a id="13962" class="Keyword">import</a> <a id="13969" href="foundation.functoriality-cartesian-product-types.html" class="Module">foundation.functoriality-cartesian-product-types</a>
<a id="14018" class="Keyword">open</a> <a id="14023" class="Keyword">import</a> <a id="14030" href="foundation.functoriality-coproduct-types.html" class="Module">foundation.functoriality-coproduct-types</a>
<a id="14071" class="Keyword">open</a> <a id="14076" class="Keyword">import</a> <a id="14083" href="foundation.functoriality-dependent-function-types.html" class="Module">foundation.functoriality-dependent-function-types</a>
<a id="14133" class="Keyword">open</a> <a id="14138" class="Keyword">import</a> <a id="14145" href="foundation.functoriality-dependent-pair-types.html" class="Module">foundation.functoriality-dependent-pair-types</a>
<a id="14191" class="Keyword">open</a> <a id="14196" class="Keyword">import</a> <a id="14203" href="foundation.functoriality-function-types.html" class="Module">foundation.functoriality-function-types</a>
<a id="14243" class="Keyword">open</a> <a id="14248" class="Keyword">import</a> <a id="14255" href="foundation.functoriality-propositional-truncation.html" class="Module">foundation.functoriality-propositional-truncation</a>
<a id="14305" class="Keyword">open</a> <a id="14310" class="Keyword">import</a> <a id="14317" href="foundation.functoriality-set-quotients.html" class="Module">foundation.functoriality-set-quotients</a>
<a id="14356" class="Keyword">open</a> <a id="14361" class="Keyword">import</a> <a id="14368" href="foundation.functoriality-set-truncation.html" class="Module">foundation.functoriality-set-truncation</a>
<a id="14408" class="Keyword">open</a> <a id="14413" class="Keyword">import</a> <a id="14420" href="foundation.functoriality-w-types.html" class="Module">foundation.functoriality-w-types</a>
<a id="14453" class="Keyword">open</a> <a id="14458" class="Keyword">import</a> <a id="14465" href="foundation.fundamental-theorem-of-identity-types.html" class="Module">foundation.fundamental-theorem-of-identity-types</a>
<a id="14514" class="Keyword">open</a> <a id="14519" class="Keyword">import</a> <a id="14526" href="foundation.global-choice.html" class="Module">foundation.global-choice</a>
<a id="14551" class="Keyword">open</a> <a id="14556" class="Keyword">import</a> <a id="14563" href="foundation.hilberts-epsilon-operators.html" class="Module">foundation.hilberts-epsilon-operators</a>
<a id="14601" class="Keyword">open</a> <a id="14606" class="Keyword">import</a> <a id="14613" href="foundation.homotopies.html" class="Module">foundation.homotopies</a>
<a id="14635" class="Keyword">open</a> <a id="14640" class="Keyword">import</a> <a id="14647" href="foundation.identity-systems.html" class="Module">foundation.identity-systems</a>
<a id="14675" class="Keyword">open</a> <a id="14680" class="Keyword">import</a> <a id="14687" href="foundation.identity-types.html" class="Module">foundation.identity-types</a>
<a id="14713" class="Keyword">open</a> <a id="14718" class="Keyword">import</a> <a id="14725" href="foundation.images.html" class="Module">foundation.images</a>
<a id="14743" class="Keyword">open</a> <a id="14748" class="Keyword">import</a> <a id="14755" href="foundation.impredicative-encodings.html" class="Module">foundation.impredicative-encodings</a>
<a id="14790" class="Keyword">open</a> <a id="14795" class="Keyword">import</a> <a id="14802" href="foundation.indexed-w-types.html" class="Module">foundation.indexed-w-types</a>
<a id="14829" class="Keyword">open</a> <a id="14834" class="Keyword">import</a> <a id="14841" href="foundation.induction-principle-propositional-truncation.html" class="Module">foundation.induction-principle-propositional-truncation</a>
<a id="14897" class="Keyword">open</a> <a id="14902" class="Keyword">import</a> <a id="14909" href="foundation.induction-w-types.html" class="Module">foundation.induction-w-types</a>
<a id="14938" class="Keyword">open</a> <a id="14943" class="Keyword">import</a> <a id="14950" href="foundation.inequality-w-types.html" class="Module">foundation.inequality-w-types</a>
<a id="14980" class="Keyword">open</a> <a id="14985" class="Keyword">import</a> <a id="14992" href="foundation.inhabited-types.html" class="Module">foundation.inhabited-types</a>
<a id="15019" class="Keyword">open</a> <a id="15024" class="Keyword">import</a> <a id="15031" href="foundation.injective-maps.html" class="Module">foundation.injective-maps</a>
<a id="15057" class="Keyword">open</a> <a id="15062" class="Keyword">import</a> <a id="15069" href="foundation.interchange-law.html" class="Module">foundation.interchange-law</a>
<a id="15096" class="Keyword">open</a> <a id="15101" class="Keyword">import</a> <a id="15108" href="foundation.intersection.html" class="Module">foundation.intersection</a>
<a id="15132" class="Keyword">open</a> <a id="15137" class="Keyword">import</a> <a id="15144" href="foundation.involutions.html" class="Module">foundation.involutions</a>
<a id="15167" class="Keyword">open</a> <a id="15172" class="Keyword">import</a> <a id="15179" href="foundation.isolated-points.html" class="Module">foundation.isolated-points</a>
<a id="15206" class="Keyword">open</a> <a id="15211" class="Keyword">import</a> <a id="15218" href="foundation.isomorphisms-of-sets.html" class="Module">foundation.isomorphisms-of-sets</a>
<a id="15250" class="Keyword">open</a> <a id="15255" class="Keyword">import</a> <a id="15262" href="foundation.iterating-automorphisms.html" class="Module">foundation.iterating-automorphisms</a>
<a id="15297" class="Keyword">open</a> <a id="15302" class="Keyword">import</a> <a id="15309" href="foundation.iterating-functions.html" class="Module">foundation.iterating-functions</a>
<a id="15340" class="Keyword">open</a> <a id="15345" class="Keyword">import</a> <a id="15352" href="foundation.iterating-involutions.html" class="Module">foundation.iterating-involutions</a>
<a id="15385" class="Keyword">open</a> <a id="15390" class="Keyword">import</a> <a id="15397" href="foundation.law-of-excluded-middle.html" class="Module">foundation.law-of-excluded-middle</a>
<a id="15431" class="Keyword">open</a> <a id="15436" class="Keyword">import</a> <a id="15443" href="foundation.lawveres-fixed-point-theorem.html" class="Module">foundation.lawveres-fixed-point-theorem</a>
<a id="15483" class="Keyword">open</a> <a id="15488" class="Keyword">import</a> <a id="15495" href="foundation.locally-small-types.html" class="Module">foundation.locally-small-types</a>
<a id="15526" class="Keyword">open</a> <a id="15531" class="Keyword">import</a> <a id="15538" href="foundation.logical-equivalences.html" class="Module">foundation.logical-equivalences</a>
<a id="15570" class="Keyword">open</a> <a id="15575" class="Keyword">import</a> <a id="15582" href="foundation.lower-types-w-types.html" class="Module">foundation.lower-types-w-types</a>
<a id="15613" class="Keyword">open</a> <a id="15618" class="Keyword">import</a> <a id="15625" href="foundation.maybe.html" class="Module">foundation.maybe</a>
<a id="15642" class="Keyword">open</a> <a id="15647" class="Keyword">import</a> <a id="15654" href="foundation.mere-equality.html" class="Module">foundation.mere-equality</a>
<a id="15679" class="Keyword">open</a> <a id="15684" class="Keyword">import</a> <a id="15691" href="foundation.mere-equivalences.html" class="Module">foundation.mere-equivalences</a>
<a id="15720" class="Keyword">open</a> <a id="15725" class="Keyword">import</a> <a id="15732" href="foundation.monomorphisms.html" class="Module">foundation.monomorphisms</a>
<a id="15757" class="Keyword">open</a> <a id="15762" class="Keyword">import</a> <a id="15769" href="foundation.multisets.html" class="Module">foundation.multisets</a>
<a id="15790" class="Keyword">open</a> <a id="15795" class="Keyword">import</a> <a id="15802" href="foundation.multisubsets.html" class="Module">foundation.multisubsets</a>
<a id="15826" class="Keyword">open</a> <a id="15831" class="Keyword">import</a> <a id="15838" href="foundation.negation.html" class="Module">foundation.negation</a>
<a id="15858" class="Keyword">open</a> <a id="15863" class="Keyword">import</a> <a id="15870" href="foundation.non-contractible-types.html" class="Module">foundation.non-contractible-types</a>
<a id="15904" class="Keyword">open</a> <a id="15909" class="Keyword">import</a> <a id="15916" href="foundation.pairs-of-distinct-elements.html" class="Module">foundation.pairs-of-distinct-elements</a>
<a id="15954" class="Keyword">open</a> <a id="15959" class="Keyword">import</a> <a id="15966" href="foundation.path-algebra.html" class="Module">foundation.path-algebra</a>
<a id="15990" class="Keyword">open</a> <a id="15995" class="Keyword">import</a> <a id="16002" href="foundation.path-split-maps.html" class="Module">foundation.path-split-maps</a>
<a id="16029" class="Keyword">open</a> <a id="16034" class="Keyword">import</a> <a id="16041" href="foundation.polynomial-endofunctors.html" class="Module">foundation.polynomial-endofunctors</a>
<a id="16076" class="Keyword">open</a> <a id="16081" class="Keyword">import</a> <a id="16088" href="foundation.powersets.html" class="Module">foundation.powersets</a>
<a id="16109" class="Keyword">open</a> <a id="16114" class="Keyword">import</a> <a id="16121" href="foundation.principle-of-omniscience.html" class="Module">foundation.principle-of-omniscience</a>
<a id="16157" class="Keyword">open</a> <a id="16162" class="Keyword">import</a> <a id="16169" href="foundation.products-unordered-pairs-of-types.html" class="Module">foundation.products-unordered-pairs-of-types</a>
<a id="16214" class="Keyword">open</a> <a id="16219" class="Keyword">import</a> <a id="16226" href="foundation.products-unordered-tuples-of-types.html" class="Module">foundation.products-unordered-tuples-of-types</a>
<a id="16272" class="Keyword">open</a> <a id="16277" class="Keyword">import</a> <a id="16284" href="foundation.propositional-extensionality.html" class="Module">foundation.propositional-extensionality</a>
<a id="16324" class="Keyword">open</a> <a id="16329" class="Keyword">import</a> <a id="16336" href="foundation.propositional-maps.html" class="Module">foundation.propositional-maps</a>
<a id="16366" class="Keyword">open</a> <a id="16371" class="Keyword">import</a> <a id="16378" href="foundation.propositional-truncations.html" class="Module">foundation.propositional-truncations</a>
<a id="16415" class="Keyword">open</a> <a id="16420" class="Keyword">import</a> <a id="16427" href="foundation.propositions.html" class="Module">foundation.propositions</a>
<a id="16451" class="Keyword">open</a> <a id="16456" class="Keyword">import</a> <a id="16463" href="foundation.pullbacks.html" class="Module">foundation.pullbacks</a>
<a id="16484" class="Keyword">open</a> <a id="16489" class="Keyword">import</a> <a id="16496" href="foundation.raising-universe-levels.html" class="Module">foundation.raising-universe-levels</a>
<a id="16531" class="Keyword">open</a> <a id="16536" class="Keyword">import</a> <a id="16543" href="foundation.ranks-of-elements-w-types.html" class="Module">foundation.ranks-of-elements-w-types</a>
<a id="16580" class="Keyword">open</a> <a id="16585" class="Keyword">import</a> <a id="16592" href="foundation.reflecting-maps-equivalence-relations.html" class="Module">foundation.reflecting-maps-equivalence-relations</a>
<a id="16641" class="Keyword">open</a> <a id="16646" class="Keyword">import</a> <a id="16653" href="foundation.repetitions-sequences.html" class="Module">foundation.repetitions-sequences</a>
<a id="16686" class="Keyword">open</a> <a id="16691" class="Keyword">import</a> <a id="16698" href="foundation.repetitions.html" class="Module">foundation.repetitions</a>
<a id="16721" class="Keyword">open</a> <a id="16726" class="Keyword">import</a> <a id="16733" href="foundation.replacement.html" class="Module">foundation.replacement</a>
<a id="16756" class="Keyword">open</a> <a id="16761" class="Keyword">import</a> <a id="16768" href="foundation.retractions.html" class="Module">foundation.retractions</a>
<a id="16791" class="Keyword">open</a> <a id="16796" class="Keyword">import</a> <a id="16803" href="foundation.russells-paradox.html" class="Module">foundation.russells-paradox</a>
<a id="16831" class="Keyword">open</a> <a id="16836" class="Keyword">import</a> <a id="16843" href="foundation.sections.html" class="Module">foundation.sections</a>
<a id="16863" class="Keyword">open</a> <a id="16868" class="Keyword">import</a> <a id="16875" href="foundation.sequences.html" class="Module">foundation.sequences</a>
<a id="16896" class="Keyword">open</a> <a id="16901" class="Keyword">import</a> <a id="16908" href="foundation.set-presented-types.html" class="Module">foundation.set-presented-types</a>
<a id="16939" class="Keyword">open</a> <a id="16944" class="Keyword">import</a> <a id="16951" href="foundation.set-truncations.html" class="Module">foundation.set-truncations</a>
<a id="16978" class="Keyword">open</a> <a id="16983" class="Keyword">import</a> <a id="16990" href="foundation.sets.html" class="Module">foundation.sets</a>
<a id="17006" class="Keyword">open</a> <a id="17011" class="Keyword">import</a> <a id="17018" href="foundation.singleton-induction.html" class="Module">foundation.singleton-induction</a>
<a id="17049" class="Keyword">open</a> <a id="17054" class="Keyword">import</a> <a id="17061" href="foundation.slice.html" class="Module">foundation.slice</a>
<a id="17078" class="Keyword">open</a> <a id="17083" class="Keyword">import</a> <a id="17090" href="foundation.small-maps.html" class="Module">foundation.small-maps</a>
<a id="17112" class="Keyword">open</a> <a id="17117" class="Keyword">import</a> <a id="17124" href="foundation.small-multisets.html" class="Module">foundation.small-multisets</a>
<a id="17151" class="Keyword">open</a> <a id="17156" class="Keyword">import</a> <a id="17163" href="foundation.small-types.html" class="Module">foundation.small-types</a>
<a id="17186" class="Keyword">open</a> <a id="17191" class="Keyword">import</a> <a id="17198" href="foundation.small-universes.html" class="Module">foundation.small-universes</a>
<a id="17225" class="Keyword">open</a> <a id="17230" class="Keyword">import</a> <a id="17237" href="foundation.split-surjective-maps.html" class="Module">foundation.split-surjective-maps</a>
<a id="17270" class="Keyword">open</a> <a id="17275" class="Keyword">import</a> <a id="17282" href="foundation.structure-identity-principle.html" class="Module">foundation.structure-identity-principle</a>
<a id="17322" class="Keyword">open</a> <a id="17327" class="Keyword">import</a> <a id="17334" href="foundation.structure.html" class="Module">foundation.structure</a>
<a id="17355" class="Keyword">open</a> <a id="17360" class="Keyword">import</a> <a id="17367" href="foundation.subterminal-types.html" class="Module">foundation.subterminal-types</a>
<a id="17396" class="Keyword">open</a> <a id="17401" class="Keyword">import</a> <a id="17408" href="foundation.subtype-identity-principle.html" class="Module">foundation.subtype-identity-principle</a>
<a id="17446" class="Keyword">open</a> <a id="17451" class="Keyword">import</a> <a id="17458" href="foundation.subtypes.html" class="Module">foundation.subtypes</a>
<a id="17478" class="Keyword">open</a> <a id="17483" class="Keyword">import</a> <a id="17490" href="foundation.subuniverses.html" class="Module">foundation.subuniverses</a>
<a id="17514" class="Keyword">open</a> <a id="17519" class="Keyword">import</a> <a id="17526" href="foundation.surjective-maps.html" class="Module">foundation.surjective-maps</a>
<a id="17553" class="Keyword">open</a> <a id="17558" class="Keyword">import</a> <a id="17565" href="foundation.symmetric-difference.html" class="Module">foundation.symmetric-difference</a>
<a id="17597" class="Keyword">open</a> <a id="17602" class="Keyword">import</a> <a id="17609" href="foundation.truncated-equality.html" class="Module">foundation.truncated-equality</a>
<a id="17639" class="Keyword">open</a> <a id="17644" class="Keyword">import</a> <a id="17651" href="foundation.truncated-maps.html" class="Module">foundation.truncated-maps</a>
<a id="17677" class="Keyword">open</a> <a id="17682" class="Keyword">import</a> <a id="17689" href="foundation.truncated-types.html" class="Module">foundation.truncated-types</a>
<a id="17716" class="Keyword">open</a> <a id="17721" class="Keyword">import</a> <a id="17728" href="foundation.truncation-levels.html" class="Module">foundation.truncation-levels</a>
<a id="17757" class="Keyword">open</a> <a id="17762" class="Keyword">import</a> <a id="17769" href="foundation.truncations.html" class="Module">foundation.truncations</a>
<a id="17792" class="Keyword">open</a> <a id="17797" class="Keyword">import</a> <a id="17804" href="foundation.type-arithmetic-cartesian-product-types.html" class="Module">foundation.type-arithmetic-cartesian-product-types</a>
<a id="17855" class="Keyword">open</a> <a id="17860" class="Keyword">import</a> <a id="17867" href="foundation.type-arithmetic-coproduct-types.html" class="Module">foundation.type-arithmetic-coproduct-types</a>
<a id="17910" class="Keyword">open</a> <a id="17915" class="Keyword">import</a> <a id="17922" href="foundation.type-arithmetic-dependent-pair-types.html" class="Module">foundation.type-arithmetic-dependent-pair-types</a>
<a id="17970" class="Keyword">open</a> <a id="17975" class="Keyword">import</a> <a id="17982" href="foundation.type-arithmetic-empty-type.html" class="Module">foundation.type-arithmetic-empty-type</a>
<a id="18020" class="Keyword">open</a> <a id="18025" class="Keyword">import</a> <a id="18032" href="foundation.type-arithmetic-unit-type.html" class="Module">foundation.type-arithmetic-unit-type</a>
<a id="18069" class="Keyword">open</a> <a id="18074" class="Keyword">import</a> <a id="18081" href="foundation.union.html" class="Module">foundation.union</a>
<a id="18098" class="Keyword">open</a> <a id="18103" class="Keyword">import</a> <a id="18110" href="foundation.uniqueness-image.html" class="Module">foundation.uniqueness-image</a>
<a id="18138" class="Keyword">open</a> <a id="18143" class="Keyword">import</a> <a id="18150" href="foundation.uniqueness-set-quotients.html" class="Module">foundation.uniqueness-set-quotients</a>
<a id="18186" class="Keyword">open</a> <a id="18191" class="Keyword">import</a> <a id="18198" href="foundation.uniqueness-set-truncations.html" class="Module">foundation.uniqueness-set-truncations</a>
<a id="18236" class="Keyword">open</a> <a id="18241" class="Keyword">import</a> <a id="18248" href="foundation.uniqueness-truncation.html" class="Module">foundation.uniqueness-truncation</a>
<a id="18281" class="Keyword">open</a> <a id="18286" class="Keyword">import</a> <a id="18293" href="foundation.unit-type.html" class="Module">foundation.unit-type</a>
<a id="18314" class="Keyword">open</a> <a id="18319" class="Keyword">import</a> <a id="18326" href="foundation.univalence-implies-function-extensionality.html" class="Module">foundation.univalence-implies-function-extensionality</a>
<a id="18380" class="Keyword">open</a> <a id="18385" class="Keyword">import</a> <a id="18392" href="foundation.univalence.html" class="Module">foundation.univalence</a>
<a id="18414" class="Keyword">open</a> <a id="18419" class="Keyword">import</a> <a id="18426" href="foundation.univalent-type-families.html" class="Module">foundation.univalent-type-families</a>
<a id="18461" class="Keyword">open</a> <a id="18466" class="Keyword">import</a> <a id="18473" href="foundation.universal-multiset.html" class="Module">foundation.universal-multiset</a>
<a id="18503" class="Keyword">open</a> <a id="18508" class="Keyword">import</a> <a id="18515" href="foundation.universal-property-booleans.html" class="Module">foundation.universal-property-booleans</a>
<a id="18554" class="Keyword">open</a> <a id="18559" class="Keyword">import</a> <a id="18566" href="foundation.universal-property-cartesian-product-types.html" class="Module">foundation.universal-property-cartesian-product-types</a>
<a id="18620" class="Keyword">open</a> <a id="18625" class="Keyword">import</a> <a id="18632" href="foundation.universal-property-coproduct-types.html" class="Module">foundation.universal-property-coproduct-types</a>
<a id="18678" class="Keyword">open</a> <a id="18683" class="Keyword">import</a> <a id="18690" href="foundation.universal-property-dependent-pair-types.html" class="Module">foundation.universal-property-dependent-pair-types</a>
<a id="18741" class="Keyword">open</a> <a id="18746" class="Keyword">import</a> <a id="18753" href="foundation.universal-property-empty-type.html" class="Module">foundation.universal-property-empty-type</a>
<a id="18794" class="Keyword">open</a> <a id="18799" class="Keyword">import</a> <a id="18806" href="foundation.universal-property-fiber-products.html" class="Module">foundation.universal-property-fiber-products</a>
<a id="18851" class="Keyword">open</a> <a id="18856" class="Keyword">import</a> <a id="18863" href="foundation.universal-property-identity-types.html" class="Module">foundation.universal-property-identity-types</a>
<a id="18908" class="Keyword">open</a> <a id="18913" class="Keyword">import</a> <a id="18920" href="foundation.universal-property-image.html" class="Module">foundation.universal-property-image</a>
<a id="18956" class="Keyword">open</a> <a id="18961" class="Keyword">import</a> <a id="18968" href="foundation.universal-property-maybe.html" class="Module">foundation.universal-property-maybe</a>
<a id="19004" class="Keyword">open</a> <a id="19009" class="Keyword">import</a> <a id="19016" href="foundation.universal-property-propositional-truncation-into-sets.html" class="Module">foundation.universal-property-propositional-truncation-into-sets</a>
<a id="19081" class="Keyword">open</a> <a id="19086" class="Keyword">import</a> <a id="19093" href="foundation.universal-property-propositional-truncation.html" class="Module">foundation.universal-property-propositional-truncation</a>
<a id="19148" class="Keyword">open</a> <a id="19153" class="Keyword">import</a> <a id="19160" href="foundation.universal-property-pullbacks.html" class="Module">foundation.universal-property-pullbacks</a>
<a id="19200" class="Keyword">open</a> <a id="19205" class="Keyword">import</a> <a id="19212" href="foundation.universal-property-set-quotients.html" class="Module">foundation.universal-property-set-quotients</a>
<a id="19256" class="Keyword">open</a> <a id="19261" class="Keyword">import</a> <a id="19268" href="foundation.universal-property-set-truncation.html" class="Module">foundation.universal-property-set-truncation</a>
<a id="19313" class="Keyword">open</a> <a id="19318" class="Keyword">import</a> <a id="19325" href="foundation.universal-property-truncation.html" class="Module">foundation.universal-property-truncation</a>
<a id="19366" class="Keyword">open</a> <a id="19371" class="Keyword">import</a> <a id="19378" href="foundation.universal-property-unit-type.html" class="Module">foundation.universal-property-unit-type</a>
<a id="19418" class="Keyword">open</a> <a id="19423" class="Keyword">import</a> <a id="19430" href="foundation.universe-levels.html" class="Module">foundation.universe-levels</a>
<a id="19457" class="Keyword">open</a> <a id="19462" class="Keyword">import</a> <a id="19469" href="foundation.unordered-pairs-of-types.html" class="Module">foundation.unordered-pairs-of-types</a>
<a id="19505" class="Keyword">open</a> <a id="19510" class="Keyword">import</a> <a id="19517" href="foundation.unordered-pairs.html" class="Module">foundation.unordered-pairs</a>
<a id="19544" class="Keyword">open</a> <a id="19549" class="Keyword">import</a> <a id="19556" href="foundation.unordered-tuples-of-types.html" class="Module">foundation.unordered-tuples-of-types</a>
<a id="19593" class="Keyword">open</a> <a id="19598" class="Keyword">import</a> <a id="19605" href="foundation.unordered-tuples.html" class="Module">foundation.unordered-tuples</a>
<a id="19633" class="Keyword">open</a> <a id="19638" class="Keyword">import</a> <a id="19645" href="foundation.w-types.html" class="Module">foundation.w-types</a>
<a id="19664" class="Keyword">open</a> <a id="19669" class="Keyword">import</a> <a id="19676" href="foundation.weak-function-extensionality.html" class="Module">foundation.weak-function-extensionality</a>
<a id="19716" class="Keyword">open</a> <a id="19721" class="Keyword">import</a> <a id="19728" href="foundation.weakly-constant-maps.html" class="Module">foundation.weakly-constant-maps</a>
<a id="19760" class="Keyword">open</a> <a id="19765" class="Keyword">import</a> <a id="19772" href="foundation.xor.html" class="Module">foundation.xor</a>
</pre>
## Foundation Core

<pre class="Agda"><a id="19820" class="Keyword">open</a> <a id="19825" class="Keyword">import</a> <a id="19832" href="foundation-core.0-maps.html" class="Module">foundation-core.0-maps</a>
<a id="19855" class="Keyword">open</a> <a id="19860" class="Keyword">import</a> <a id="19867" href="foundation-core.1-types.html" class="Module">foundation-core.1-types</a>
<a id="19891" class="Keyword">open</a> <a id="19896" class="Keyword">import</a> <a id="19903" href="foundation-core.cartesian-product-types.html" class="Module">foundation-core.cartesian-product-types</a>
<a id="19943" class="Keyword">open</a> <a id="19948" class="Keyword">import</a> <a id="19955" href="foundation-core.coherently-invertible-maps.html" class="Module">foundation-core.coherently-invertible-maps</a>
<a id="19998" class="Keyword">open</a> <a id="20003" class="Keyword">import</a> <a id="20010" href="foundation-core.commuting-squares.html" class="Module">foundation-core.commuting-squares</a>
<a id="20044" class="Keyword">open</a> <a id="20049" class="Keyword">import</a> <a id="20056" href="foundation-core.cones-pullbacks.html" class="Module">foundation-core.cones-pullbacks</a>
<a id="20088" class="Keyword">open</a> <a id="20093" class="Keyword">import</a> <a id="20100" href="foundation-core.constant-maps.html" class="Module">foundation-core.constant-maps</a>
<a id="20130" class="Keyword">open</a> <a id="20135" class="Keyword">import</a> <a id="20142" href="foundation-core.contractible-maps.html" class="Module">foundation-core.contractible-maps</a>
<a id="20176" class="Keyword">open</a> <a id="20181" class="Keyword">import</a> <a id="20188" href="foundation-core.contractible-types.html" class="Module">foundation-core.contractible-types</a>
<a id="20223" class="Keyword">open</a> <a id="20228" class="Keyword">import</a> <a id="20235" href="foundation-core.dependent-pair-types.html" class="Module">foundation-core.dependent-pair-types</a>
<a id="20272" class="Keyword">open</a> <a id="20277" class="Keyword">import</a> <a id="20284" href="foundation-core.embeddings.html" class="Module">foundation-core.embeddings</a>
<a id="20311" class="Keyword">open</a> <a id="20316" class="Keyword">import</a> <a id="20323" href="foundation-core.empty-types.html" class="Module">foundation-core.empty-types</a>
<a id="20351" class="Keyword">open</a> <a id="20356" class="Keyword">import</a> <a id="20363" href="foundation-core.equality-cartesian-product-types.html" class="Module">foundation-core.equality-cartesian-product-types</a>
<a id="20412" class="Keyword">open</a> <a id="20417" class="Keyword">import</a> <a id="20424" href="foundation-core.equality-dependent-pair-types.html" class="Module">foundation-core.equality-dependent-pair-types</a>
<a id="20470" class="Keyword">open</a> <a id="20475" class="Keyword">import</a> <a id="20482" href="foundation-core.equality-fibers-of-maps.html" class="Module">foundation-core.equality-fibers-of-maps</a>
<a id="20522" class="Keyword">open</a> <a id="20527" class="Keyword">import</a> <a id="20534" href="foundation-core.equivalence-induction.html" class="Module">foundation-core.equivalence-induction</a>
<a id="20572" class="Keyword">open</a> <a id="20577" class="Keyword">import</a> <a id="20584" href="foundation-core.equivalences.html" class="Module">foundation-core.equivalences</a>
<a id="20613" class="Keyword">open</a> <a id="20618" class="Keyword">import</a> <a id="20625" href="foundation-core.faithful-maps.html" class="Module">foundation-core.faithful-maps</a>
<a id="20655" class="Keyword">open</a> <a id="20660" class="Keyword">import</a> <a id="20667" href="foundation-core.fibers-of-maps.html" class="Module">foundation-core.fibers-of-maps</a>
<a id="20698" class="Keyword">open</a> <a id="20703" class="Keyword">import</a> <a id="20710" href="foundation-core.function-extensionality.html" class="Module">foundation-core.function-extensionality</a>
<a id="20750" class="Keyword">open</a> <a id="20755" class="Keyword">import</a> <a id="20762" href="foundation-core.functions.html" class="Module">foundation-core.functions</a>
<a id="20788" class="Keyword">open</a> <a id="20793" class="Keyword">import</a> <a id="20800" href="foundation-core.functoriality-dependent-function-types.html" class="Module">foundation-core.functoriality-dependent-function-types</a>
<a id="20855" class="Keyword">open</a> <a id="20860" class="Keyword">import</a> <a id="20867" href="foundation-core.functoriality-dependent-pair-types.html" class="Module">foundation-core.functoriality-dependent-pair-types</a>
<a id="20918" class="Keyword">open</a> <a id="20923" class="Keyword">import</a> <a id="20930" href="foundation-core.functoriality-function-types.html" class="Module">foundation-core.functoriality-function-types</a>
<a id="20975" class="Keyword">open</a> <a id="20980" class="Keyword">import</a> <a id="20987" href="foundation-core.fundamental-theorem-of-identity-types.html" class="Module">foundation-core.fundamental-theorem-of-identity-types</a>
<a id="21041" class="Keyword">open</a> <a id="21046" class="Keyword">import</a> <a id="21053" href="foundation-core.homotopies.html" class="Module">foundation-core.homotopies</a>
<a id="21080" class="Keyword">open</a> <a id="21085" class="Keyword">import</a> <a id="21092" href="foundation-core.identity-systems.html" class="Module">foundation-core.identity-systems</a>
<a id="21125" class="Keyword">open</a> <a id="21130" class="Keyword">import</a> <a id="21137" href="foundation-core.identity-types.html" class="Module">foundation-core.identity-types</a>
<a id="21168" class="Keyword">open</a> <a id="21173" class="Keyword">import</a> <a id="21180" href="foundation-core.logical-equivalences.html" class="Module">foundation-core.logical-equivalences</a>
<a id="21217" class="Keyword">open</a> <a id="21222" class="Keyword">import</a> <a id="21229" href="foundation-core.negation.html" class="Module">foundation-core.negation</a>
<a id="21254" class="Keyword">open</a> <a id="21259" class="Keyword">import</a> <a id="21266" href="foundation-core.path-split-maps.html" class="Module">foundation-core.path-split-maps</a>
<a id="21298" class="Keyword">open</a> <a id="21303" class="Keyword">import</a> <a id="21310" href="foundation-core.propositional-maps.html" class="Module">foundation-core.propositional-maps</a>
<a id="21345" class="Keyword">open</a> <a id="21350" class="Keyword">import</a> <a id="21357" href="foundation-core.propositions.html" class="Module">foundation-core.propositions</a>
<a id="21386" class="Keyword">open</a> <a id="21391" class="Keyword">import</a> <a id="21398" href="foundation-core.pullbacks.html" class="Module">foundation-core.pullbacks</a>
<a id="21424" class="Keyword">open</a> <a id="21429" class="Keyword">import</a> <a id="21436" href="foundation-core.retractions.html" class="Module">foundation-core.retractions</a>
<a id="21464" class="Keyword">open</a> <a id="21469" class="Keyword">import</a> <a id="21476" href="foundation-core.sections.html" class="Module">foundation-core.sections</a>
<a id="21501" class="Keyword">open</a> <a id="21506" class="Keyword">import</a> <a id="21513" href="foundation-core.sets.html" class="Module">foundation-core.sets</a>
<a id="21534" class="Keyword">open</a> <a id="21539" class="Keyword">import</a> <a id="21546" href="foundation-core.singleton-induction.html" class="Module">foundation-core.singleton-induction</a>
<a id="21582" class="Keyword">open</a> <a id="21587" class="Keyword">import</a> <a id="21594" href="foundation-core.subtype-identity-principle.html" class="Module">foundation-core.subtype-identity-principle</a>
<a id="21637" class="Keyword">open</a> <a id="21642" class="Keyword">import</a> <a id="21649" href="foundation-core.subtypes.html" class="Module">foundation-core.subtypes</a>
<a id="21674" class="Keyword">open</a> <a id="21679" class="Keyword">import</a> <a id="21686" href="foundation-core.truncated-maps.html" class="Module">foundation-core.truncated-maps</a>
<a id="21717" class="Keyword">open</a> <a id="21722" class="Keyword">import</a> <a id="21729" href="foundation-core.truncated-types.html" class="Module">foundation-core.truncated-types</a>
<a id="21761" class="Keyword">open</a> <a id="21766" class="Keyword">import</a> <a id="21773" href="foundation-core.truncation-levels.html" class="Module">foundation-core.truncation-levels</a>
<a id="21807" class="Keyword">open</a> <a id="21812" class="Keyword">import</a> <a id="21819" href="foundation-core.type-arithmetic-cartesian-product-types.html" class="Module">foundation-core.type-arithmetic-cartesian-product-types</a>
<a id="21875" class="Keyword">open</a> <a id="21880" class="Keyword">import</a> <a id="21887" href="foundation-core.type-arithmetic-dependent-pair-types.html" class="Module">foundation-core.type-arithmetic-dependent-pair-types</a>
<a id="21940" class="Keyword">open</a> <a id="21945" class="Keyword">import</a> <a id="21952" href="foundation-core.univalence.html" class="Module">foundation-core.univalence</a>
<a id="21979" class="Keyword">open</a> <a id="21984" class="Keyword">import</a> <a id="21991" href="foundation-core.universal-property-pullbacks.html" class="Module">foundation-core.universal-property-pullbacks</a>
<a id="22036" class="Keyword">open</a> <a id="22041" class="Keyword">import</a> <a id="22048" href="foundation-core.universe-levels.html" class="Module">foundation-core.universe-levels</a>
</pre>
## Graph theory

<pre class="Agda"><a id="22110" class="Keyword">open</a> <a id="22115" class="Keyword">import</a> <a id="22122" href="graph-theory.html" class="Module">graph-theory</a>
<a id="22135" class="Keyword">open</a> <a id="22140" class="Keyword">import</a> <a id="22147" href="graph-theory.connected-undirected-graphs.html" class="Module">graph-theory.connected-undirected-graphs</a>
<a id="22188" class="Keyword">open</a> <a id="22193" class="Keyword">import</a> <a id="22200" href="graph-theory.directed-graphs.html" class="Module">graph-theory.directed-graphs</a>
<a id="22229" class="Keyword">open</a> <a id="22234" class="Keyword">import</a> <a id="22241" href="graph-theory.edge-coloured-undirected-graphs.html" class="Module">graph-theory.edge-coloured-undirected-graphs</a>
<a id="22286" class="Keyword">open</a> <a id="22291" class="Keyword">import</a> <a id="22298" href="graph-theory.equivalences-undirected-graphs.html" class="Module">graph-theory.equivalences-undirected-graphs</a>
<a id="22342" class="Keyword">open</a> <a id="22347" class="Keyword">import</a> <a id="22354" href="graph-theory.finite-graphs.html" class="Module">graph-theory.finite-graphs</a>
<a id="22381" class="Keyword">open</a> <a id="22386" class="Keyword">import</a> <a id="22393" href="graph-theory.incidence-undirected-graphs.html" class="Module">graph-theory.incidence-undirected-graphs</a>
<a id="22434" class="Keyword">open</a> <a id="22439" class="Keyword">import</a> <a id="22446" href="graph-theory.matchings.html" class="Module">graph-theory.matchings</a>
<a id="22469" class="Keyword">open</a> <a id="22474" class="Keyword">import</a> <a id="22481" href="graph-theory.mere-equivalences-undirected-graphs.html" class="Module">graph-theory.mere-equivalences-undirected-graphs</a>
<a id="22530" class="Keyword">open</a> <a id="22535" class="Keyword">import</a> <a id="22542" href="graph-theory.morphisms-directed-graphs.html" class="Module">graph-theory.morphisms-directed-graphs</a>
<a id="22581" class="Keyword">open</a> <a id="22586" class="Keyword">import</a> <a id="22593" href="graph-theory.morphisms-undirected-graphs.html" class="Module">graph-theory.morphisms-undirected-graphs</a>
<a id="22634" class="Keyword">open</a> <a id="22639" class="Keyword">import</a> <a id="22646" href="graph-theory.orientations-undirected-graphs.html" class="Module">graph-theory.orientations-undirected-graphs</a>
<a id="22690" class="Keyword">open</a> <a id="22695" class="Keyword">import</a> <a id="22702" href="graph-theory.paths-undirected-graphs.html" class="Module">graph-theory.paths-undirected-graphs</a>
<a id="22739" class="Keyword">open</a> <a id="22744" class="Keyword">import</a> <a id="22751" href="graph-theory.polygons.html" class="Module">graph-theory.polygons</a>
<a id="22773" class="Keyword">open</a> <a id="22778" class="Keyword">import</a> <a id="22785" href="graph-theory.reflexive-graphs.html" class="Module">graph-theory.reflexive-graphs</a>
<a id="22815" class="Keyword">open</a> <a id="22820" class="Keyword">import</a> <a id="22827" href="graph-theory.regular-undirected-graphs.html" class="Module">graph-theory.regular-undirected-graphs</a>
<a id="22866" class="Keyword">open</a> <a id="22871" class="Keyword">import</a> <a id="22878" href="graph-theory.simple-undirected-graphs.html" class="Module">graph-theory.simple-undirected-graphs</a>
<a id="22916" class="Keyword">open</a> <a id="22921" class="Keyword">import</a> <a id="22928" href="graph-theory.undirected-graphs.html" class="Module">graph-theory.undirected-graphs</a>
<a id="22959" class="Keyword">open</a> <a id="22964" class="Keyword">import</a> <a id="22971" href="graph-theory.vertex-covers.html" class="Module">graph-theory.vertex-covers</a>
<a id="22998" class="Keyword">open</a> <a id="23003" class="Keyword">import</a> <a id="23010" href="graph-theory.voltage-graphs.html" class="Module">graph-theory.voltage-graphs</a>
</pre>
## Group theory

<pre class="Agda"><a id="23068" class="Keyword">open</a> <a id="23073" class="Keyword">import</a> <a id="23080" href="group-theory.html" class="Module">group-theory</a>
<a id="23093" class="Keyword">open</a> <a id="23098" class="Keyword">import</a> <a id="23105" href="group-theory.abelian-groups.html" class="Module">group-theory.abelian-groups</a>
<a id="23133" class="Keyword">open</a> <a id="23138" class="Keyword">import</a> <a id="23145" href="group-theory.abelian-subgroups.html" class="Module">group-theory.abelian-subgroups</a>
<a id="23176" class="Keyword">open</a> <a id="23181" class="Keyword">import</a> <a id="23188" href="group-theory.abstract-group-torsors.html" class="Module">group-theory.abstract-group-torsors</a>
<a id="23224" class="Keyword">open</a> <a id="23229" class="Keyword">import</a> <a id="23236" href="group-theory.addition-homomorphisms-abelian-groups.html" class="Module">group-theory.addition-homomorphisms-abelian-groups</a>
<a id="23287" class="Keyword">open</a> <a id="23292" class="Keyword">import</a> <a id="23299" href="group-theory.automorphism-groups.html" class="Module">group-theory.automorphism-groups</a>
<a id="23332" class="Keyword">open</a> <a id="23337" class="Keyword">import</a> <a id="23344" href="group-theory.cartesian-products-abelian-groups.html" class="Module">group-theory.cartesian-products-abelian-groups</a>
<a id="23391" class="Keyword">open</a> <a id="23396" class="Keyword">import</a> <a id="23403" href="group-theory.cartesian-products-groups.html" class="Module">group-theory.cartesian-products-groups</a>
<a id="23442" class="Keyword">open</a> <a id="23447" class="Keyword">import</a> <a id="23454" href="group-theory.cartesian-products-monoids.html" class="Module">group-theory.cartesian-products-monoids</a>
<a id="23494" class="Keyword">open</a> <a id="23499" class="Keyword">import</a> <a id="23506" href="group-theory.cartesian-products-semigroups.html" class="Module">group-theory.cartesian-products-semigroups</a>
<a id="23549" class="Keyword">open</a> <a id="23554" class="Keyword">import</a> <a id="23561" href="group-theory.category-of-groups.html" class="Module">group-theory.category-of-groups</a>
<a id="23593" class="Keyword">open</a> <a id="23598" class="Keyword">import</a> <a id="23605" href="group-theory.category-of-semigroups.html" class="Module">group-theory.category-of-semigroups</a>
<a id="23641" class="Keyword">open</a> <a id="23646" class="Keyword">import</a> <a id="23653" href="group-theory.cayleys-theorem.html" class="Module">group-theory.cayleys-theorem</a>
<a id="23682" class="Keyword">open</a> <a id="23687" class="Keyword">import</a> <a id="23694" href="group-theory.commutative-monoids.html" class="Module">group-theory.commutative-monoids</a>
<a id="23727" class="Keyword">open</a> <a id="23732" class="Keyword">import</a> <a id="23739" href="group-theory.concrete-group-actions.html" class="Module">group-theory.concrete-group-actions</a>
<a id="23775" class="Keyword">open</a> <a id="23780" class="Keyword">import</a> <a id="23787" href="group-theory.concrete-groups.html" class="Module">group-theory.concrete-groups</a>
<a id="23816" class="Keyword">open</a> <a id="23821" class="Keyword">import</a> <a id="23828" href="group-theory.concrete-subgroups.html" class="Module">group-theory.concrete-subgroups</a>
<a id="23860" class="Keyword">open</a> <a id="23865" class="Keyword">import</a> <a id="23872" href="group-theory.conjugation.html" class="Module">group-theory.conjugation</a>
<a id="23897" class="Keyword">open</a> <a id="23902" class="Keyword">import</a> <a id="23909" href="group-theory.embeddings-groups.html" class="Module">group-theory.embeddings-groups</a>
<a id="23940" class="Keyword">open</a> <a id="23945" class="Keyword">import</a> <a id="23952" href="group-theory.endomorphism-rings-abelian-groups.html" class="Module">group-theory.endomorphism-rings-abelian-groups</a>
<a id="23999" class="Keyword">open</a> <a id="24004" class="Keyword">import</a> <a id="24011" href="group-theory.epimorphisms-groups.html" class="Module">group-theory.epimorphisms-groups</a>
<a id="24044" class="Keyword">open</a> <a id="24049" class="Keyword">import</a> <a id="24056" href="group-theory.equivalences-group-actions.html" class="Module">group-theory.equivalences-group-actions</a>
<a id="24096" class="Keyword">open</a> <a id="24101" class="Keyword">import</a> <a id="24108" href="group-theory.equivalences-semigroups.html" class="Module">group-theory.equivalences-semigroups</a>
<a id="24145" class="Keyword">open</a> <a id="24150" class="Keyword">import</a> <a id="24157" href="group-theory.examples-higher-groups.html" class="Module">group-theory.examples-higher-groups</a>
<a id="24193" class="Keyword">open</a> <a id="24198" class="Keyword">import</a> <a id="24205" href="group-theory.furstenberg-groups.html" class="Module">group-theory.furstenberg-groups</a>
<a id="24237" class="Keyword">open</a> <a id="24242" class="Keyword">import</a> <a id="24249" href="group-theory.group-actions.html" class="Module">group-theory.group-actions</a>
<a id="24276" class="Keyword">open</a> <a id="24281" class="Keyword">import</a> <a id="24288" href="group-theory.groups.html" class="Module">group-theory.groups</a>
<a id="24308" class="Keyword">open</a> <a id="24313" class="Keyword">import</a> <a id="24320" href="group-theory.higher-groups.html" class="Module">group-theory.higher-groups</a>
<a id="24347" class="Keyword">open</a> <a id="24352" class="Keyword">import</a> <a id="24359" href="group-theory.homomorphisms-abelian-groups.html" class="Module">group-theory.homomorphisms-abelian-groups</a>
<a id="24401" class="Keyword">open</a> <a id="24406" class="Keyword">import</a> <a id="24413" href="group-theory.homomorphisms-generated-subgroups.html" class="Module">group-theory.homomorphisms-generated-subgroups</a>
<a id="24460" class="Keyword">open</a> <a id="24465" class="Keyword">import</a> <a id="24472" href="group-theory.homomorphisms-group-actions.html" class="Module">group-theory.homomorphisms-group-actions</a>
<a id="24513" class="Keyword">open</a> <a id="24518" class="Keyword">import</a> <a id="24525" href="group-theory.homomorphisms-groups.html" class="Module">group-theory.homomorphisms-groups</a>
<a id="24559" class="Keyword">open</a> <a id="24564" class="Keyword">import</a> <a id="24571" href="group-theory.homomorphisms-monoids.html" class="Module">group-theory.homomorphisms-monoids</a>
<a id="24606" class="Keyword">open</a> <a id="24611" class="Keyword">import</a> <a id="24618" href="group-theory.homomorphisms-semigroups.html" class="Module">group-theory.homomorphisms-semigroups</a>
<a id="24656" class="Keyword">open</a> <a id="24661" class="Keyword">import</a> <a id="24668" href="group-theory.inverse-semigroups.html" class="Module">group-theory.inverse-semigroups</a>
<a id="24700" class="Keyword">open</a> <a id="24705" class="Keyword">import</a> <a id="24712" href="group-theory.invertible-elements-monoids.html" class="Module">group-theory.invertible-elements-monoids</a>
<a id="24753" class="Keyword">open</a> <a id="24758" class="Keyword">import</a> <a id="24765" href="group-theory.isomorphisms-abelian-groups.html" class="Module">group-theory.isomorphisms-abelian-groups</a>
<a id="24806" class="Keyword">open</a> <a id="24811" class="Keyword">import</a> <a id="24818" href="group-theory.isomorphisms-group-actions.html" class="Module">group-theory.isomorphisms-group-actions</a>
<a id="24858" class="Keyword">open</a> <a id="24863" class="Keyword">import</a> <a id="24870" href="group-theory.isomorphisms-groups.html" class="Module">group-theory.isomorphisms-groups</a>
<a id="24903" class="Keyword">open</a> <a id="24908" class="Keyword">import</a> <a id="24915" href="group-theory.isomorphisms-semigroups.html" class="Module">group-theory.isomorphisms-semigroups</a>
<a id="24952" class="Keyword">open</a> <a id="24957" class="Keyword">import</a> <a id="24964" href="group-theory.mere-equivalences-group-actions.html" class="Module">group-theory.mere-equivalences-group-actions</a>
<a id="25009" class="Keyword">open</a> <a id="25014" class="Keyword">import</a> <a id="25021" href="group-theory.monoid-actions.html" class="Module">group-theory.monoid-actions</a>
<a id="25049" class="Keyword">open</a> <a id="25054" class="Keyword">import</a> <a id="25061" href="group-theory.monoids.html" class="Module">group-theory.monoids</a>
<a id="25082" class="Keyword">open</a> <a id="25087" class="Keyword">import</a> <a id="25094" href="group-theory.monomorphisms-groups.html" class="Module">group-theory.monomorphisms-groups</a>
<a id="25128" class="Keyword">open</a> <a id="25133" class="Keyword">import</a> <a id="25140" href="group-theory.orbits-group-actions.html" class="Module">group-theory.orbits-group-actions</a>
<a id="25174" class="Keyword">open</a> <a id="25179" class="Keyword">import</a> <a id="25186" href="group-theory.orbits-monoid-actions.html" class="Module">group-theory.orbits-monoid-actions</a>
<a id="25221" class="Keyword">open</a> <a id="25226" class="Keyword">import</a> <a id="25233" href="group-theory.precategory-of-group-actions.html" class="Module">group-theory.precategory-of-group-actions</a>
<a id="25275" class="Keyword">open</a> <a id="25280" class="Keyword">import</a> <a id="25287" href="group-theory.precategory-of-groups.html" class="Module">group-theory.precategory-of-groups</a>
<a id="25322" class="Keyword">open</a> <a id="25327" class="Keyword">import</a> <a id="25334" href="group-theory.precategory-of-semigroups.html" class="Module">group-theory.precategory-of-semigroups</a>
<a id="25373" class="Keyword">open</a> <a id="25378" class="Keyword">import</a> <a id="25385" href="group-theory.principal-group-actions.html" class="Module">group-theory.principal-group-actions</a>
<a id="25422" class="Keyword">open</a> <a id="25427" class="Keyword">import</a> <a id="25434" href="group-theory.semigroups.html" class="Module">group-theory.semigroups</a>
<a id="25458" class="Keyword">open</a> <a id="25463" class="Keyword">import</a> <a id="25470" href="group-theory.sheargroups.html" class="Module">group-theory.sheargroups</a>
<a id="25495" class="Keyword">open</a> <a id="25500" class="Keyword">import</a> <a id="25507" href="group-theory.stabilizer-groups.html" class="Module">group-theory.stabilizer-groups</a>
<a id="25538" class="Keyword">open</a> <a id="25543" class="Keyword">import</a> <a id="25550" href="group-theory.subgroups-generated-by-subsets-groups.html" class="Module">group-theory.subgroups-generated-by-subsets-groups</a>
<a id="25601" class="Keyword">open</a> <a id="25606" class="Keyword">import</a> <a id="25613" href="group-theory.subgroups.html" class="Module">group-theory.subgroups</a>
<a id="25636" class="Keyword">open</a> <a id="25641" class="Keyword">import</a> <a id="25648" href="group-theory.substitution-functor-group-actions.html" class="Module">group-theory.substitution-functor-group-actions</a>
<a id="25696" class="Keyword">open</a> <a id="25701" class="Keyword">import</a> <a id="25708" href="group-theory.symmetric-groups.html" class="Module">group-theory.symmetric-groups</a>
<a id="25738" class="Keyword">open</a> <a id="25743" class="Keyword">import</a> <a id="25750" href="group-theory.transitive-group-actions.html" class="Module">group-theory.transitive-group-actions</a>
</pre>
## Linear algebra

<pre class="Agda"><a id="25820" class="Keyword">open</a> <a id="25825" class="Keyword">import</a> <a id="25832" href="linear-algebra.html" class="Module">linear-algebra</a>
<a id="25847" class="Keyword">open</a> <a id="25852" class="Keyword">import</a> <a id="25859" href="linear-algebra.constant-matrices.html" class="Module">linear-algebra.constant-matrices</a>
<a id="25892" class="Keyword">open</a> <a id="25897" class="Keyword">import</a> <a id="25904" href="linear-algebra.constant-vectors.html" class="Module">linear-algebra.constant-vectors</a>
<a id="25936" class="Keyword">open</a> <a id="25941" class="Keyword">import</a> <a id="25948" href="linear-algebra.diagonal-matrices-on-rings.html" class="Module">linear-algebra.diagonal-matrices-on-rings</a>
<a id="25990" class="Keyword">open</a> <a id="25995" class="Keyword">import</a> <a id="26002" href="linear-algebra.functoriality-matrices.html" class="Module">linear-algebra.functoriality-matrices</a>
<a id="26040" class="Keyword">open</a> <a id="26045" class="Keyword">import</a> <a id="26052" href="linear-algebra.functoriality-vectors.html" class="Module">linear-algebra.functoriality-vectors</a>
<a id="26089" class="Keyword">open</a> <a id="26094" class="Keyword">import</a> <a id="26101" href="linear-algebra.matrices-on-rings.html" class="Module">linear-algebra.matrices-on-rings</a>
<a id="26134" class="Keyword">open</a> <a id="26139" class="Keyword">import</a> <a id="26146" href="linear-algebra.matrices.html" class="Module">linear-algebra.matrices</a>
<a id="26170" class="Keyword">open</a> <a id="26175" class="Keyword">import</a> <a id="26182" href="linear-algebra.multiplication-matrices.html" class="Module">linear-algebra.multiplication-matrices</a>
<a id="26221" class="Keyword">open</a> <a id="26226" class="Keyword">import</a> <a id="26233" href="linear-algebra.scalar-multiplication-matrices.html" class="Module">linear-algebra.scalar-multiplication-matrices</a>
<a id="26279" class="Keyword">open</a> <a id="26284" class="Keyword">import</a> <a id="26291" href="linear-algebra.scalar-multiplication-vectors.html" class="Module">linear-algebra.scalar-multiplication-vectors</a>
<a id="26336" class="Keyword">open</a> <a id="26341" class="Keyword">import</a> <a id="26348" href="linear-algebra.transposition-matrices.html" class="Module">linear-algebra.transposition-matrices</a>
<a id="26386" class="Keyword">open</a> <a id="26391" class="Keyword">import</a> <a id="26398" href="linear-algebra.vectors-on-rings.html" class="Module">linear-algebra.vectors-on-rings</a>
<a id="26430" class="Keyword">open</a> <a id="26435" class="Keyword">import</a> <a id="26442" href="linear-algebra.vectors.html" class="Module">linear-algebra.vectors</a>
</pre>
## Order theory

<pre class="Agda"><a id="26495" class="Keyword">open</a> <a id="26500" class="Keyword">import</a> <a id="26507" href="order-theory.html" class="Module">order-theory</a>
<a id="26520" class="Keyword">open</a> <a id="26525" class="Keyword">import</a> <a id="26532" href="order-theory.chains-posets.html" class="Module">order-theory.chains-posets</a>
<a id="26559" class="Keyword">open</a> <a id="26564" class="Keyword">import</a> <a id="26571" href="order-theory.chains-preorders.html" class="Module">order-theory.chains-preorders</a>
<a id="26601" class="Keyword">open</a> <a id="26606" class="Keyword">import</a> <a id="26613" href="order-theory.decidable-subposets.html" class="Module">order-theory.decidable-subposets</a>
<a id="26646" class="Keyword">open</a> <a id="26651" class="Keyword">import</a> <a id="26658" href="order-theory.decidable-subpreorders.html" class="Module">order-theory.decidable-subpreorders</a>
<a id="26694" class="Keyword">open</a> <a id="26699" class="Keyword">import</a> <a id="26706" href="order-theory.finite-posets.html" class="Module">order-theory.finite-posets</a>
<a id="26733" class="Keyword">open</a> <a id="26738" class="Keyword">import</a> <a id="26745" href="order-theory.finite-preorders.html" class="Module">order-theory.finite-preorders</a>
<a id="26775" class="Keyword">open</a> <a id="26780" class="Keyword">import</a> <a id="26787" href="order-theory.finitely-graded-posets.html" class="Module">order-theory.finitely-graded-posets</a>
<a id="26823" class="Keyword">open</a> <a id="26828" class="Keyword">import</a> <a id="26835" href="order-theory.greatest-lower-bounds-posets.html" class="Module">order-theory.greatest-lower-bounds-posets</a>
<a id="26877" class="Keyword">open</a> <a id="26882" class="Keyword">import</a> <a id="26889" href="order-theory.interval-subposets.html" class="Module">order-theory.interval-subposets</a>
<a id="26921" class="Keyword">open</a> <a id="26926" class="Keyword">import</a> <a id="26933" href="order-theory.join-semilattices.html" class="Module">order-theory.join-semilattices</a>
<a id="26964" class="Keyword">open</a> <a id="26969" class="Keyword">import</a> <a id="26976" href="order-theory.large-posets.html" class="Module">order-theory.large-posets</a>
<a id="27002" class="Keyword">open</a> <a id="27007" class="Keyword">import</a> <a id="27014" href="order-theory.large-preorders.html" class="Module">order-theory.large-preorders</a>
<a id="27043" class="Keyword">open</a> <a id="27048" class="Keyword">import</a> <a id="27055" href="order-theory.largest-elements-posets.html" class="Module">order-theory.largest-elements-posets</a>
<a id="27092" class="Keyword">open</a> <a id="27097" class="Keyword">import</a> <a id="27104" href="order-theory.largest-elements-preorders.html" class="Module">order-theory.largest-elements-preorders</a>
<a id="27144" class="Keyword">open</a> <a id="27149" class="Keyword">import</a> <a id="27156" href="order-theory.lattices.html" class="Module">order-theory.lattices</a>
<a id="27178" class="Keyword">open</a> <a id="27183" class="Keyword">import</a> <a id="27190" href="order-theory.least-elements-posets.html" class="Module">order-theory.least-elements-posets</a>
<a id="27225" class="Keyword">open</a> <a id="27230" class="Keyword">import</a> <a id="27237" href="order-theory.least-elements-preorders.html" class="Module">order-theory.least-elements-preorders</a>
<a id="27275" class="Keyword">open</a> <a id="27280" class="Keyword">import</a> <a id="27287" href="order-theory.least-upper-bounds-posets.html" class="Module">order-theory.least-upper-bounds-posets</a>
<a id="27326" class="Keyword">open</a> <a id="27331" class="Keyword">import</a> <a id="27338" href="order-theory.locally-finite-posets.html" class="Module">order-theory.locally-finite-posets</a>
<a id="27373" class="Keyword">open</a> <a id="27378" class="Keyword">import</a> <a id="27385" href="order-theory.maximal-chains-posets.html" class="Module">order-theory.maximal-chains-posets</a>
<a id="27420" class="Keyword">open</a> <a id="27425" class="Keyword">import</a> <a id="27432" href="order-theory.maximal-chains-preorders.html" class="Module">order-theory.maximal-chains-preorders</a>
<a id="27470" class="Keyword">open</a> <a id="27475" class="Keyword">import</a> <a id="27482" href="order-theory.meet-semilattices.html" class="Module">order-theory.meet-semilattices</a>
<a id="27513" class="Keyword">open</a> <a id="27518" class="Keyword">import</a> <a id="27525" href="order-theory.order-preserving-maps-posets.html" class="Module">order-theory.order-preserving-maps-posets</a>
<a id="27567" class="Keyword">open</a> <a id="27572" class="Keyword">import</a> <a id="27579" href="order-theory.order-preserving-maps-preorders.html" class="Module">order-theory.order-preserving-maps-preorders</a>
<a id="27624" class="Keyword">open</a> <a id="27629" class="Keyword">import</a> <a id="27636" href="order-theory.planar-binary-trees.html" class="Module">order-theory.planar-binary-trees</a>
<a id="27669" class="Keyword">open</a> <a id="27674" class="Keyword">import</a> <a id="27681" href="order-theory.posets.html" class="Module">order-theory.posets</a>
<a id="27701" class="Keyword">open</a> <a id="27706" class="Keyword">import</a> <a id="27713" href="order-theory.preorders.html" class="Module">order-theory.preorders</a>
<a id="27736" class="Keyword">open</a> <a id="27741" class="Keyword">import</a> <a id="27748" href="order-theory.subposets.html" class="Module">order-theory.subposets</a>
<a id="27771" class="Keyword">open</a> <a id="27776" class="Keyword">import</a> <a id="27783" href="order-theory.subpreorders.html" class="Module">order-theory.subpreorders</a>
<a id="27809" class="Keyword">open</a> <a id="27814" class="Keyword">import</a> <a id="27821" href="order-theory.total-posets.html" class="Module">order-theory.total-posets</a>
<a id="27847" class="Keyword">open</a> <a id="27852" class="Keyword">import</a> <a id="27859" href="order-theory.total-preorders.html" class="Module">order-theory.total-preorders</a>
</pre>
## Polytopes

<pre class="Agda"><a id="27915" class="Keyword">open</a> <a id="27920" class="Keyword">import</a> <a id="27927" href="polytopes.html" class="Module">polytopes</a>
<a id="27937" class="Keyword">open</a> <a id="27942" class="Keyword">import</a> <a id="27949" href="polytopes.abstract-polytopes.html" class="Module">polytopes.abstract-polytopes</a>
</pre>
## Ring theory

<pre class="Agda"><a id="28007" class="Keyword">open</a> <a id="28012" class="Keyword">import</a> <a id="28019" href="ring-theory.html" class="Module">ring-theory</a>
<a id="28031" class="Keyword">open</a> <a id="28036" class="Keyword">import</a> <a id="28043" href="ring-theory.dependent-products-rings.html" class="Module">ring-theory.dependent-products-rings</a>
<a id="28080" class="Keyword">open</a> <a id="28085" class="Keyword">import</a> <a id="28092" href="ring-theory.division-rings.html" class="Module">ring-theory.division-rings</a>
<a id="28119" class="Keyword">open</a> <a id="28124" class="Keyword">import</a> <a id="28131" href="ring-theory.homomorphisms-rings.html" class="Module">ring-theory.homomorphisms-rings</a>
<a id="28163" class="Keyword">open</a> <a id="28168" class="Keyword">import</a> <a id="28175" href="ring-theory.ideals-generated-by-subsets-rings.html" class="Module">ring-theory.ideals-generated-by-subsets-rings</a>
<a id="28221" class="Keyword">open</a> <a id="28226" class="Keyword">import</a> <a id="28233" href="ring-theory.ideals-rings.html" class="Module">ring-theory.ideals-rings</a>
<a id="28258" class="Keyword">open</a> <a id="28263" class="Keyword">import</a> <a id="28270" href="ring-theory.invariant-basis-property-rings.html" class="Module">ring-theory.invariant-basis-property-rings</a>
<a id="28313" class="Keyword">open</a> <a id="28318" class="Keyword">import</a> <a id="28325" href="ring-theory.invertible-elements-rings.html" class="Module">ring-theory.invertible-elements-rings</a>
<a id="28363" class="Keyword">open</a> <a id="28368" class="Keyword">import</a> <a id="28375" href="ring-theory.isomorphisms-rings.html" class="Module">ring-theory.isomorphisms-rings</a>
<a id="28406" class="Keyword">open</a> <a id="28411" class="Keyword">import</a> <a id="28418" href="ring-theory.localizations-rings.html" class="Module">ring-theory.localizations-rings</a>
<a id="28450" class="Keyword">open</a> <a id="28455" class="Keyword">import</a> <a id="28462" href="ring-theory.modules-rings.html" class="Module">ring-theory.modules-rings</a>
<a id="28488" class="Keyword">open</a> <a id="28493" class="Keyword">import</a> <a id="28500" href="ring-theory.nil-ideals-rings.html" class="Module">ring-theory.nil-ideals-rings</a>
<a id="28529" class="Keyword">open</a> <a id="28534" class="Keyword">import</a> <a id="28541" href="ring-theory.nilpotent-elements-rings.html" class="Module">ring-theory.nilpotent-elements-rings</a>
<a id="28578" class="Keyword">open</a> <a id="28583" class="Keyword">import</a> <a id="28590" href="ring-theory.nontrivial-rings.html" class="Module">ring-theory.nontrivial-rings</a>
<a id="28619" class="Keyword">open</a> <a id="28624" class="Keyword">import</a> <a id="28631" href="ring-theory.opposite-rings.html" class="Module">ring-theory.opposite-rings</a>
<a id="28658" class="Keyword">open</a> <a id="28663" class="Keyword">import</a> <a id="28670" href="ring-theory.powers-of-elements-rings.html" class="Module">ring-theory.powers-of-elements-rings</a>
<a id="28707" class="Keyword">open</a> <a id="28712" class="Keyword">import</a> <a id="28719" href="ring-theory.products-rings.html" class="Module">ring-theory.products-rings</a>
<a id="28746" class="Keyword">open</a> <a id="28751" class="Keyword">import</a> <a id="28758" href="ring-theory.radical-ideals-rings.html" class="Module">ring-theory.radical-ideals-rings</a>
<a id="28791" class="Keyword">open</a> <a id="28796" class="Keyword">import</a> <a id="28803" href="ring-theory.rings.html" class="Module">ring-theory.rings</a>
<a id="28821" class="Keyword">open</a> <a id="28826" class="Keyword">import</a> <a id="28833" href="ring-theory.subsets-rings.html" class="Module">ring-theory.subsets-rings</a>
</pre>
## Set theory

<pre class="Agda"><a id="28887" class="Keyword">open</a> <a id="28892" class="Keyword">import</a> <a id="28899" href="set-theory.html" class="Module">set-theory</a>
<a id="28910" class="Keyword">open</a> <a id="28915" class="Keyword">import</a> <a id="28922" href="set-theory.countable-sets.html" class="Module">set-theory.countable-sets</a>
<a id="28948" class="Keyword">open</a> <a id="28953" class="Keyword">import</a> <a id="28960" href="set-theory.uncountable-sets.html" class="Module">set-theory.uncountable-sets</a>
</pre>
## Structured types

<pre class="Agda"><a id="29022" class="Keyword">open</a> <a id="29027" class="Keyword">import</a> <a id="29034" href="structured-types.html" class="Module">structured-types</a>
<a id="29051" class="Keyword">open</a> <a id="29056" class="Keyword">import</a> <a id="29063" href="structured-types.contractible-pointed-types.html" class="Module">structured-types.contractible-pointed-types</a>
<a id="29107" class="Keyword">open</a> <a id="29112" class="Keyword">import</a> <a id="29119" href="structured-types.equivalences-types-equipped-with-endomorphisms.html" class="Module">structured-types.equivalences-types-equipped-with-endomorphisms</a>
<a id="29183" class="Keyword">open</a> <a id="29188" class="Keyword">import</a> <a id="29195" href="structured-types.finite-multiplication-magmas.html" class="Module">structured-types.finite-multiplication-magmas</a>
<a id="29241" class="Keyword">open</a> <a id="29246" class="Keyword">import</a> <a id="29253" href="structured-types.magmas.html" class="Module">structured-types.magmas</a>
<a id="29277" class="Keyword">open</a> <a id="29282" class="Keyword">import</a> <a id="29289" href="structured-types.mere-equivalences-types-equipped-with-endomorphisms.html" class="Module">structured-types.mere-equivalences-types-equipped-with-endomorphisms</a>
<a id="29358" class="Keyword">open</a> <a id="29363" class="Keyword">import</a> <a id="29370" href="structured-types.morphisms-magmas.html" class="Module">structured-types.morphisms-magmas</a>
<a id="29404" class="Keyword">open</a> <a id="29409" class="Keyword">import</a> <a id="29416" href="structured-types.morphisms-types-equipped-with-endomorphisms.html" class="Module">structured-types.morphisms-types-equipped-with-endomorphisms</a>
<a id="29477" class="Keyword">open</a> <a id="29482" class="Keyword">import</a> <a id="29489" href="structured-types.morphisms-wild-unital-magmas.html" class="Module">structured-types.morphisms-wild-unital-magmas</a>
<a id="29535" class="Keyword">open</a> <a id="29540" class="Keyword">import</a> <a id="29547" href="structured-types.pointed-dependent-functions.html" class="Module">structured-types.pointed-dependent-functions</a>
<a id="29592" class="Keyword">open</a> <a id="29597" class="Keyword">import</a> <a id="29604" href="structured-types.pointed-equivalences.html" class="Module">structured-types.pointed-equivalences</a>
<a id="29642" class="Keyword">open</a> <a id="29647" class="Keyword">import</a> <a id="29654" href="structured-types.pointed-families-of-types.html" class="Module">structured-types.pointed-families-of-types</a>
<a id="29697" class="Keyword">open</a> <a id="29702" class="Keyword">import</a> <a id="29709" href="structured-types.pointed-homotopies.html" class="Module">structured-types.pointed-homotopies</a>
<a id="29745" class="Keyword">open</a> <a id="29750" class="Keyword">import</a> <a id="29757" href="structured-types.pointed-maps.html" class="Module">structured-types.pointed-maps</a>
<a id="29787" class="Keyword">open</a> <a id="29792" class="Keyword">import</a> <a id="29799" href="structured-types.pointed-types.html" class="Module">structured-types.pointed-types</a>
<a id="29830" class="Keyword">open</a> <a id="29835" class="Keyword">import</a> <a id="29842" href="structured-types.types-equipped-with-endomorphisms.html" class="Module">structured-types.types-equipped-with-endomorphisms</a>
<a id="29893" class="Keyword">open</a> <a id="29898" class="Keyword">import</a> <a id="29905" href="structured-types.universal-property-lists-wild-monoids.html" class="Module">structured-types.universal-property-lists-wild-monoids</a>
<a id="29960" class="Keyword">open</a> <a id="29965" class="Keyword">import</a> <a id="29972" href="structured-types.wild-groups.html" class="Module">structured-types.wild-groups</a>
<a id="30001" class="Keyword">open</a> <a id="30006" class="Keyword">import</a> <a id="30013" href="structured-types.wild-loops.html" class="Module">structured-types.wild-loops</a>
<a id="30041" class="Keyword">open</a> <a id="30046" class="Keyword">import</a> <a id="30053" href="structured-types.wild-monoids.html" class="Module">structured-types.wild-monoids</a>
<a id="30083" class="Keyword">open</a> <a id="30088" class="Keyword">import</a> <a id="30095" href="structured-types.wild-quasigroups.html" class="Module">structured-types.wild-quasigroups</a>
<a id="30129" class="Keyword">open</a> <a id="30134" class="Keyword">import</a> <a id="30141" href="structured-types.wild-semigroups.html" class="Module">structured-types.wild-semigroups</a>
<a id="30174" class="Keyword">open</a> <a id="30179" class="Keyword">import</a> <a id="30186" href="structured-types.wild-unital-magmas.html" class="Module">structured-types.wild-unital-magmas</a>
</pre>
## Synthetic homotopy theory

<pre class="Agda"><a id="30265" class="Keyword">open</a> <a id="30270" class="Keyword">import</a> <a id="30277" href="synthetic-homotopy-theory.html" class="Module">synthetic-homotopy-theory</a>
<a id="30303" class="Keyword">open</a> <a id="30308" class="Keyword">import</a> <a id="30315" href="synthetic-homotopy-theory.23-pullbacks.html" class="Module">synthetic-homotopy-theory.23-pullbacks</a>
<a id="30354" class="Keyword">open</a> <a id="30359" class="Keyword">import</a> <a id="30366" href="synthetic-homotopy-theory.24-pushouts.html" class="Module">synthetic-homotopy-theory.24-pushouts</a>
<a id="30404" class="Keyword">open</a> <a id="30409" class="Keyword">import</a> <a id="30416" href="synthetic-homotopy-theory.25-cubical-diagrams.html" class="Module">synthetic-homotopy-theory.25-cubical-diagrams</a>
<a id="30462" class="Keyword">open</a> <a id="30467" class="Keyword">import</a> <a id="30474" href="synthetic-homotopy-theory.26-descent.html" class="Module">synthetic-homotopy-theory.26-descent</a>
<a id="30511" class="Keyword">open</a> <a id="30516" class="Keyword">import</a> <a id="30523" href="synthetic-homotopy-theory.26-id-pushout.html" class="Module">synthetic-homotopy-theory.26-id-pushout</a>
<a id="30563" class="Keyword">open</a> <a id="30568" class="Keyword">import</a> <a id="30575" href="synthetic-homotopy-theory.27-sequences.html" class="Module">synthetic-homotopy-theory.27-sequences</a>
<a id="30614" class="Keyword">open</a> <a id="30619" class="Keyword">import</a> <a id="30626" href="synthetic-homotopy-theory.circle.html" class="Module">synthetic-homotopy-theory.circle</a>
<a id="30659" class="Keyword">open</a> <a id="30664" class="Keyword">import</a> <a id="30671" href="synthetic-homotopy-theory.cofibers.html" class="Module">synthetic-homotopy-theory.cofibers</a>
<a id="30706" class="Keyword">open</a> <a id="30711" class="Keyword">import</a> <a id="30718" href="synthetic-homotopy-theory.cyclic-types.html" class="Module">synthetic-homotopy-theory.cyclic-types</a>
<a id="30757" class="Keyword">open</a> <a id="30762" class="Keyword">import</a> <a id="30769" href="synthetic-homotopy-theory.double-loop-spaces.html" class="Module">synthetic-homotopy-theory.double-loop-spaces</a>
<a id="30814" class="Keyword">open</a> <a id="30819" class="Keyword">import</a> <a id="30826" href="synthetic-homotopy-theory.functoriality-loop-spaces.html" class="Module">synthetic-homotopy-theory.functoriality-loop-spaces</a>
<a id="30878" class="Keyword">open</a> <a id="30883" class="Keyword">import</a> <a id="30890" href="synthetic-homotopy-theory.groups-of-loops-in-1-types.html" class="Module">synthetic-homotopy-theory.groups-of-loops-in-1-types</a>
<a id="30943" class="Keyword">open</a> <a id="30948" class="Keyword">import</a> <a id="30955" href="synthetic-homotopy-theory.infinite-cyclic-types.html" class="Module">synthetic-homotopy-theory.infinite-cyclic-types</a>
<a id="31003" class="Keyword">open</a> <a id="31008" class="Keyword">import</a> <a id="31015" href="synthetic-homotopy-theory.interval-type.html" class="Module">synthetic-homotopy-theory.interval-type</a>
<a id="31055" class="Keyword">open</a> <a id="31060" class="Keyword">import</a> <a id="31067" href="synthetic-homotopy-theory.iterated-loop-spaces.html" class="Module">synthetic-homotopy-theory.iterated-loop-spaces</a>
<a id="31114" class="Keyword">open</a> <a id="31119" class="Keyword">import</a> <a id="31126" href="synthetic-homotopy-theory.joins-of-types.html" class="Module">synthetic-homotopy-theory.joins-of-types</a>
<a id="31167" class="Keyword">open</a> <a id="31172" class="Keyword">import</a> <a id="31179" href="synthetic-homotopy-theory.loop-spaces.html" class="Module">synthetic-homotopy-theory.loop-spaces</a>
<a id="31217" class="Keyword">open</a> <a id="31222" class="Keyword">import</a> <a id="31229" href="synthetic-homotopy-theory.triple-loop-spaces.html" class="Module">synthetic-homotopy-theory.triple-loop-spaces</a>
<a id="31274" class="Keyword">open</a> <a id="31279" class="Keyword">import</a> <a id="31286" href="synthetic-homotopy-theory.universal-cover-circle.html" class="Module">synthetic-homotopy-theory.universal-cover-circle</a>
<a id="31335" class="Keyword">open</a> <a id="31340" class="Keyword">import</a> <a id="31347" href="synthetic-homotopy-theory.wedges-of-pointed-types.html" class="Module">synthetic-homotopy-theory.wedges-of-pointed-types</a>
</pre>
## Tutorials

<pre class="Agda"><a id="31424" class="Keyword">open</a> <a id="31429" class="Keyword">import</a> <a id="31436" href="tutorials.basic-agda.html" class="Module">tutorials.basic-agda</a>
</pre>
## Type theories

<pre class="Agda"><a id="31488" class="Keyword">open</a> <a id="31493" class="Keyword">import</a> <a id="31500" href="type-theories.html" class="Module">type-theories</a>
<a id="31514" class="Keyword">open</a> <a id="31519" class="Keyword">import</a> <a id="31526" href="type-theories.comprehension-type-theories.html" class="Module">type-theories.comprehension-type-theories</a>
<a id="31568" class="Keyword">open</a> <a id="31573" class="Keyword">import</a> <a id="31580" href="type-theories.dependent-type-theories.html" class="Module">type-theories.dependent-type-theories</a>
<a id="31618" class="Keyword">open</a> <a id="31623" class="Keyword">import</a> <a id="31630" href="type-theories.fibered-dependent-type-theories.html" class="Module">type-theories.fibered-dependent-type-theories</a>
<a id="31676" class="Keyword">open</a> <a id="31681" class="Keyword">import</a> <a id="31688" href="type-theories.sections-dependent-type-theories.html" class="Module">type-theories.sections-dependent-type-theories</a>
<a id="31735" class="Keyword">open</a> <a id="31740" class="Keyword">import</a> <a id="31747" href="type-theories.simple-type-theories.html" class="Module">type-theories.simple-type-theories</a>
<a id="31782" class="Keyword">open</a> <a id="31787" class="Keyword">import</a> <a id="31794" href="type-theories.unityped-type-theories.html" class="Module">type-theories.unityped-type-theories</a>
</pre>
## Univalent combinatorics

<pre class="Agda"><a id="31872" class="Keyword">open</a> <a id="31877" class="Keyword">import</a> <a id="31884" href="univalent-combinatorics.html" class="Module">univalent-combinatorics</a>
<a id="31908" class="Keyword">open</a> <a id="31913" class="Keyword">import</a> <a id="31920" href="univalent-combinatorics.2-element-decidable-subtypes.html" class="Module">univalent-combinatorics.2-element-decidable-subtypes</a>
<a id="31973" class="Keyword">open</a> <a id="31978" class="Keyword">import</a> <a id="31985" href="univalent-combinatorics.2-element-subtypes.html" class="Module">univalent-combinatorics.2-element-subtypes</a>
<a id="32028" class="Keyword">open</a> <a id="32033" class="Keyword">import</a> <a id="32040" href="univalent-combinatorics.2-element-types.html" class="Module">univalent-combinatorics.2-element-types</a>
<a id="32080" class="Keyword">open</a> <a id="32085" class="Keyword">import</a> <a id="32092" href="univalent-combinatorics.binomial-types.html" class="Module">univalent-combinatorics.binomial-types</a>
<a id="32131" class="Keyword">open</a> <a id="32136" class="Keyword">import</a> <a id="32143" href="univalent-combinatorics.cartesian-product-types.html" class="Module">univalent-combinatorics.cartesian-product-types</a>
<a id="32191" class="Keyword">open</a> <a id="32196" class="Keyword">import</a> <a id="32203" href="univalent-combinatorics.classical-finite-types.html" class="Module">univalent-combinatorics.classical-finite-types</a>
<a id="32250" class="Keyword">open</a> <a id="32255" class="Keyword">import</a> <a id="32262" href="univalent-combinatorics.complements-isolated-points.html" class="Module">univalent-combinatorics.complements-isolated-points</a>
<a id="32314" class="Keyword">open</a> <a id="32319" class="Keyword">import</a> <a id="32326" href="univalent-combinatorics.composition-species.html" class="Module">univalent-combinatorics.composition-species</a>
<a id="32370" class="Keyword">open</a> <a id="32375" class="Keyword">import</a> <a id="32382" href="univalent-combinatorics.coproduct-types.html" class="Module">univalent-combinatorics.coproduct-types</a>
<a id="32422" class="Keyword">open</a> <a id="32427" class="Keyword">import</a> <a id="32434" href="univalent-combinatorics.counting-decidable-subtypes.html" class="Module">univalent-combinatorics.counting-decidable-subtypes</a>
<a id="32486" class="Keyword">open</a> <a id="32491" class="Keyword">import</a> <a id="32498" href="univalent-combinatorics.counting-dependent-pair-types.html" class="Module">univalent-combinatorics.counting-dependent-pair-types</a>
<a id="32552" class="Keyword">open</a> <a id="32557" class="Keyword">import</a> <a id="32564" href="univalent-combinatorics.counting-fibers-of-maps.html" class="Module">univalent-combinatorics.counting-fibers-of-maps</a>
<a id="32612" class="Keyword">open</a> <a id="32617" class="Keyword">import</a> <a id="32624" href="univalent-combinatorics.counting-maybe.html" class="Module">univalent-combinatorics.counting-maybe</a>
<a id="32663" class="Keyword">open</a> <a id="32668" class="Keyword">import</a> <a id="32675" href="univalent-combinatorics.counting.html" class="Module">univalent-combinatorics.counting</a>
<a id="32708" class="Keyword">open</a> <a id="32713" class="Keyword">import</a> <a id="32720" href="univalent-combinatorics.cubes.html" class="Module">univalent-combinatorics.cubes</a>
<a id="32750" class="Keyword">open</a> <a id="32755" class="Keyword">import</a> <a id="32762" href="univalent-combinatorics.decidable-dependent-function-types.html" class="Module">univalent-combinatorics.decidable-dependent-function-types</a>
<a id="32821" class="Keyword">open</a> <a id="32826" class="Keyword">import</a> <a id="32833" href="univalent-combinatorics.decidable-dependent-pair-types.html" class="Module">univalent-combinatorics.decidable-dependent-pair-types</a>
<a id="32888" class="Keyword">open</a> <a id="32893" class="Keyword">import</a> <a id="32900" href="univalent-combinatorics.decidable-propositions.html" class="Module">univalent-combinatorics.decidable-propositions</a>
<a id="32947" class="Keyword">open</a> <a id="32952" class="Keyword">import</a> <a id="32959" href="univalent-combinatorics.decidable-subtypes.html" class="Module">univalent-combinatorics.decidable-subtypes</a>
<a id="33002" class="Keyword">open</a> <a id="33007" class="Keyword">import</a> <a id="33014" href="univalent-combinatorics.dedekind-finite-sets.html" class="Module">univalent-combinatorics.dedekind-finite-sets</a>
<a id="33059" class="Keyword">open</a> <a id="33064" class="Keyword">import</a> <a id="33071" href="univalent-combinatorics.dependent-function-types.html" class="Module">univalent-combinatorics.dependent-function-types</a>
<a id="33120" class="Keyword">open</a> <a id="33125" class="Keyword">import</a> <a id="33132" href="univalent-combinatorics.dependent-sum-finite-types.html" class="Module">univalent-combinatorics.dependent-sum-finite-types</a>
<a id="33183" class="Keyword">open</a> <a id="33188" class="Keyword">import</a> <a id="33195" href="univalent-combinatorics.distributivity-of-set-truncation-over-finite-products.html" class="Module">univalent-combinatorics.distributivity-of-set-truncation-over-finite-products</a>
<a id="33273" class="Keyword">open</a> <a id="33278" class="Keyword">import</a> <a id="33285" href="univalent-combinatorics.double-counting.html" class="Module">univalent-combinatorics.double-counting</a>
<a id="33325" class="Keyword">open</a> <a id="33330" class="Keyword">import</a> <a id="33337" href="univalent-combinatorics.embeddings-standard-finite-types.html" class="Module">univalent-combinatorics.embeddings-standard-finite-types</a>
<a id="33394" class="Keyword">open</a> <a id="33399" class="Keyword">import</a> <a id="33406" href="univalent-combinatorics.embeddings.html" class="Module">univalent-combinatorics.embeddings</a>
<a id="33441" class="Keyword">open</a> <a id="33446" class="Keyword">import</a> <a id="33453" href="univalent-combinatorics.equality-finite-types.html" class="Module">univalent-combinatorics.equality-finite-types</a>
<a id="33499" class="Keyword">open</a> <a id="33504" class="Keyword">import</a> <a id="33511" href="univalent-combinatorics.equality-standard-finite-types.html" class="Module">univalent-combinatorics.equality-standard-finite-types</a>
<a id="33566" class="Keyword">open</a> <a id="33571" class="Keyword">import</a> <a id="33578" href="univalent-combinatorics.equivalences-cubes.html" class="Module">univalent-combinatorics.equivalences-cubes</a>
<a id="33621" class="Keyword">open</a> <a id="33626" class="Keyword">import</a> <a id="33633" href="univalent-combinatorics.equivalences-standard-finite-types.html" class="Module">univalent-combinatorics.equivalences-standard-finite-types</a>
<a id="33692" class="Keyword">open</a> <a id="33697" class="Keyword">import</a> <a id="33704" href="univalent-combinatorics.equivalences.html" class="Module">univalent-combinatorics.equivalences</a>
<a id="33741" class="Keyword">open</a> <a id="33746" class="Keyword">import</a> <a id="33753" href="univalent-combinatorics.ferrers-diagrams.html" class="Module">univalent-combinatorics.ferrers-diagrams</a>
<a id="33794" class="Keyword">open</a> <a id="33799" class="Keyword">import</a> <a id="33806" href="univalent-combinatorics.fibers-of-maps.html" class="Module">univalent-combinatorics.fibers-of-maps</a>
<a id="33845" class="Keyword">open</a> <a id="33850" class="Keyword">import</a> <a id="33857" href="univalent-combinatorics.finite-choice.html" class="Module">univalent-combinatorics.finite-choice</a>
<a id="33895" class="Keyword">open</a> <a id="33900" class="Keyword">import</a> <a id="33907" href="univalent-combinatorics.finite-connected-components.html" class="Module">univalent-combinatorics.finite-connected-components</a>
<a id="33959" class="Keyword">open</a> <a id="33964" class="Keyword">import</a> <a id="33971" href="univalent-combinatorics.finite-presentations.html" class="Module">univalent-combinatorics.finite-presentations</a>
<a id="34016" class="Keyword">open</a> <a id="34021" class="Keyword">import</a> <a id="34028" href="univalent-combinatorics.finite-types.html" class="Module">univalent-combinatorics.finite-types</a>
<a id="34065" class="Keyword">open</a> <a id="34070" class="Keyword">import</a> <a id="34077" href="univalent-combinatorics.finitely-presented-types.html" class="Module">univalent-combinatorics.finitely-presented-types</a>
<a id="34126" class="Keyword">open</a> <a id="34131" class="Keyword">import</a> <a id="34138" href="univalent-combinatorics.function-types.html" class="Module">univalent-combinatorics.function-types</a>
<a id="34177" class="Keyword">open</a> <a id="34182" class="Keyword">import</a> <a id="34189" href="univalent-combinatorics.image-of-maps.html" class="Module">univalent-combinatorics.image-of-maps</a>
<a id="34227" class="Keyword">open</a> <a id="34232" class="Keyword">import</a> <a id="34239" href="univalent-combinatorics.inequality-types-with-counting.html" class="Module">univalent-combinatorics.inequality-types-with-counting</a>
<a id="34294" class="Keyword">open</a> <a id="34299" class="Keyword">import</a> <a id="34306" href="univalent-combinatorics.injective-maps.html" class="Module">univalent-combinatorics.injective-maps</a>
<a id="34345" class="Keyword">open</a> <a id="34350" class="Keyword">import</a> <a id="34357" href="univalent-combinatorics.isotopies-latin-squares.html" class="Module">univalent-combinatorics.isotopies-latin-squares</a>
<a id="34405" class="Keyword">open</a> <a id="34410" class="Keyword">import</a> <a id="34417" href="univalent-combinatorics.kuratowsky-finite-sets.html" class="Module">univalent-combinatorics.kuratowsky-finite-sets</a>
<a id="34464" class="Keyword">open</a> <a id="34469" class="Keyword">import</a> <a id="34476" href="univalent-combinatorics.latin-squares.html" class="Module">univalent-combinatorics.latin-squares</a>
<a id="34514" class="Keyword">open</a> <a id="34519" class="Keyword">import</a> <a id="34526" href="univalent-combinatorics.lists.html" class="Module">univalent-combinatorics.lists</a>
<a id="34556" class="Keyword">open</a> <a id="34561" class="Keyword">import</a> <a id="34568" href="univalent-combinatorics.main-classes-of-latin-hypercubes.html" class="Module">univalent-combinatorics.main-classes-of-latin-hypercubes</a>
<a id="34625" class="Keyword">open</a> <a id="34630" class="Keyword">import</a> <a id="34637" href="univalent-combinatorics.main-classes-of-latin-squares.html" class="Module">univalent-combinatorics.main-classes-of-latin-squares</a>
<a id="34691" class="Keyword">open</a> <a id="34696" class="Keyword">import</a> <a id="34703" href="univalent-combinatorics.maybe.html" class="Module">univalent-combinatorics.maybe</a>
<a id="34733" class="Keyword">open</a> <a id="34738" class="Keyword">import</a> <a id="34745" href="univalent-combinatorics.orientations-complete-undirected-graph.html" class="Module">univalent-combinatorics.orientations-complete-undirected-graph</a>
<a id="34808" class="Keyword">open</a> <a id="34813" class="Keyword">import</a> <a id="34820" href="univalent-combinatorics.orientations-cubes.html" class="Module">univalent-combinatorics.orientations-cubes</a>
<a id="34863" class="Keyword">open</a> <a id="34868" class="Keyword">import</a> <a id="34875" href="univalent-combinatorics.petri-nets.html" class="Module">univalent-combinatorics.petri-nets</a>
<a id="34910" class="Keyword">open</a> <a id="34915" class="Keyword">import</a> <a id="34922" href="univalent-combinatorics.pi-finite-types.html" class="Module">univalent-combinatorics.pi-finite-types</a>
<a id="34962" class="Keyword">open</a> <a id="34967" class="Keyword">import</a> <a id="34974" href="univalent-combinatorics.pigeonhole-principle.html" class="Module">univalent-combinatorics.pigeonhole-principle</a>
<a id="35019" class="Keyword">open</a> <a id="35024" class="Keyword">import</a> <a id="35031" href="univalent-combinatorics.presented-pi-finite-types.html" class="Module">univalent-combinatorics.presented-pi-finite-types</a>
<a id="35081" class="Keyword">open</a> <a id="35086" class="Keyword">import</a> <a id="35093" href="univalent-combinatorics.ramsey-theory.html" class="Module">univalent-combinatorics.ramsey-theory</a>
<a id="35131" class="Keyword">open</a> <a id="35136" class="Keyword">import</a> <a id="35143" href="univalent-combinatorics.retracts-of-finite-types.html" class="Module">univalent-combinatorics.retracts-of-finite-types</a>
<a id="35192" class="Keyword">open</a> <a id="35197" class="Keyword">import</a> <a id="35204" href="univalent-combinatorics.sequences-finite-types.html" class="Module">univalent-combinatorics.sequences-finite-types</a>
<a id="35251" class="Keyword">open</a> <a id="35256" class="Keyword">import</a> <a id="35263" href="univalent-combinatorics.skipping-element-standard-finite-types.html" class="Module">univalent-combinatorics.skipping-element-standard-finite-types</a>
<a id="35326" class="Keyword">open</a> <a id="35331" class="Keyword">import</a> <a id="35338" href="univalent-combinatorics.species.html" class="Module">univalent-combinatorics.species</a>
<a id="35370" class="Keyword">open</a> <a id="35375" class="Keyword">import</a> <a id="35382" href="univalent-combinatorics.standard-finite-pruned-trees.html" class="Module">univalent-combinatorics.standard-finite-pruned-trees</a>
<a id="35435" class="Keyword">open</a> <a id="35440" class="Keyword">import</a> <a id="35447" href="univalent-combinatorics.standard-finite-trees.html" class="Module">univalent-combinatorics.standard-finite-trees</a>
<a id="35493" class="Keyword">open</a> <a id="35498" class="Keyword">import</a> <a id="35505" href="univalent-combinatorics.standard-finite-types.html" class="Module">univalent-combinatorics.standard-finite-types</a>
<a id="35551" class="Keyword">open</a> <a id="35556" class="Keyword">import</a> <a id="35563" href="univalent-combinatorics.sums-of-natural-numbers.html" class="Module">univalent-combinatorics.sums-of-natural-numbers</a>
<a id="35611" class="Keyword">open</a> <a id="35616" class="Keyword">import</a> <a id="35623" href="univalent-combinatorics.surjective-maps.html" class="Module">univalent-combinatorics.surjective-maps</a>
<a id="35663" class="Keyword">open</a> <a id="35668" class="Keyword">import</a> <a id="35675" href="univalent-combinatorics.symmetric-difference.html" class="Module">univalent-combinatorics.symmetric-difference</a>
<a id="35720" class="Keyword">open</a> <a id="35725" class="Keyword">import</a> <a id="35732" href="univalent-combinatorics.universal-property-standard-finite-types.html" class="Module">univalent-combinatorics.universal-property-standard-finite-types</a>
</pre>