# Univalent mathematics in Agda

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

<pre class="Agda"><a id="2967" class="Symbol">{-#</a> <a id="2971" class="Keyword">OPTIONS</a> <a id="2979" class="Pragma">--without-K</a> <a id="2991" class="Pragma">--exact-split</a> <a id="3005" class="Pragma">--guardedness</a> <a id="3019" class="Symbol">#-}</a>
</pre>
## Category theory

<pre class="Agda"><a id="3056" class="Keyword">open</a> <a id="3061" class="Keyword">import</a> <a id="3068" href="category-theory.html" class="Module">category-theory</a>
<a id="3084" class="Keyword">open</a> <a id="3089" class="Keyword">import</a> <a id="3096" href="category-theory.adjunctions-large-precategories.html" class="Module">category-theory.adjunctions-large-precategories</a>
<a id="3144" class="Keyword">open</a> <a id="3149" class="Keyword">import</a> <a id="3156" href="category-theory.anafunctors.html" class="Module">category-theory.anafunctors</a>
<a id="3184" class="Keyword">open</a> <a id="3189" class="Keyword">import</a> <a id="3196" href="category-theory.categories.html" class="Module">category-theory.categories</a>
<a id="3223" class="Keyword">open</a> <a id="3228" class="Keyword">import</a> <a id="3235" href="category-theory.equivalences-categories.html" class="Module">category-theory.equivalences-categories</a>
<a id="3275" class="Keyword">open</a> <a id="3280" class="Keyword">import</a> <a id="3287" href="category-theory.equivalences-large-precategories.html" class="Module">category-theory.equivalences-large-precategories</a>
<a id="3336" class="Keyword">open</a> <a id="3341" class="Keyword">import</a> <a id="3348" href="category-theory.equivalences-precategories.html" class="Module">category-theory.equivalences-precategories</a>
<a id="3391" class="Keyword">open</a> <a id="3396" class="Keyword">import</a> <a id="3403" href="category-theory.functors-categories.html" class="Module">category-theory.functors-categories</a>
<a id="3439" class="Keyword">open</a> <a id="3444" class="Keyword">import</a> <a id="3451" href="category-theory.functors-large-precategories.html" class="Module">category-theory.functors-large-precategories</a>
<a id="3496" class="Keyword">open</a> <a id="3501" class="Keyword">import</a> <a id="3508" href="category-theory.functors-precategories.html" class="Module">category-theory.functors-precategories</a>
<a id="3547" class="Keyword">open</a> <a id="3552" class="Keyword">import</a> <a id="3559" href="category-theory.homotopies-natural-transformations-large-precategories.html" class="Module">category-theory.homotopies-natural-transformations-large-precategories</a>
<a id="3630" class="Keyword">open</a> <a id="3635" class="Keyword">import</a> <a id="3642" href="category-theory.initial-objects-precategories.html" class="Module">category-theory.initial-objects-precategories</a>
<a id="3688" class="Keyword">open</a> <a id="3693" class="Keyword">import</a> <a id="3700" href="category-theory.isomorphisms-categories.html" class="Module">category-theory.isomorphisms-categories</a>
<a id="3740" class="Keyword">open</a> <a id="3745" class="Keyword">import</a> <a id="3752" href="category-theory.isomorphisms-large-precategories.html" class="Module">category-theory.isomorphisms-large-precategories</a>
<a id="3801" class="Keyword">open</a> <a id="3806" class="Keyword">import</a> <a id="3813" href="category-theory.isomorphisms-precategories.html" class="Module">category-theory.isomorphisms-precategories</a>
<a id="3856" class="Keyword">open</a> <a id="3861" class="Keyword">import</a> <a id="3868" href="category-theory.large-categories.html" class="Module">category-theory.large-categories</a>
<a id="3901" class="Keyword">open</a> <a id="3906" class="Keyword">import</a> <a id="3913" href="category-theory.large-precategories.html" class="Module">category-theory.large-precategories</a>
<a id="3949" class="Keyword">open</a> <a id="3954" class="Keyword">import</a> <a id="3961" href="category-theory.monomorphisms-large-precategories.html" class="Module">category-theory.monomorphisms-large-precategories</a>
<a id="4011" class="Keyword">open</a> <a id="4016" class="Keyword">import</a> <a id="4023" href="category-theory.natural-isomorphisms-categories.html" class="Module">category-theory.natural-isomorphisms-categories</a>
<a id="4071" class="Keyword">open</a> <a id="4076" class="Keyword">import</a> <a id="4083" href="category-theory.natural-isomorphisms-large-precategories.html" class="Module">category-theory.natural-isomorphisms-large-precategories</a>
<a id="4140" class="Keyword">open</a> <a id="4145" class="Keyword">import</a> <a id="4152" href="category-theory.natural-isomorphisms-precategories.html" class="Module">category-theory.natural-isomorphisms-precategories</a>
<a id="4203" class="Keyword">open</a> <a id="4208" class="Keyword">import</a> <a id="4215" href="category-theory.natural-transformations-categories.html" class="Module">category-theory.natural-transformations-categories</a>
<a id="4266" class="Keyword">open</a> <a id="4271" class="Keyword">import</a> <a id="4278" href="category-theory.natural-transformations-large-precategories.html" class="Module">category-theory.natural-transformations-large-precategories</a>
<a id="4338" class="Keyword">open</a> <a id="4343" class="Keyword">import</a> <a id="4350" href="category-theory.natural-transformations-precategories.html" class="Module">category-theory.natural-transformations-precategories</a>
<a id="4404" class="Keyword">open</a> <a id="4409" class="Keyword">import</a> <a id="4416" href="category-theory.precategories.html" class="Module">category-theory.precategories</a>
<a id="4446" class="Keyword">open</a> <a id="4451" class="Keyword">import</a> <a id="4458" href="category-theory.slice-precategories.html" class="Module">category-theory.slice-precategories</a>
<a id="4494" class="Keyword">open</a> <a id="4499" class="Keyword">import</a> <a id="4506" href="category-theory.terminal-objects-precategories.html" class="Module">category-theory.terminal-objects-precategories</a>
</pre>
## Elementary number theory

<pre class="Agda"><a id="4595" class="Keyword">open</a> <a id="4600" class="Keyword">import</a> <a id="4607" href="elementary-number-theory.html" class="Module">elementary-number-theory</a>
<a id="4632" class="Keyword">open</a> <a id="4637" class="Keyword">import</a> <a id="4644" href="elementary-number-theory.absolute-value-integers.html" class="Module">elementary-number-theory.absolute-value-integers</a>
<a id="4693" class="Keyword">open</a> <a id="4698" class="Keyword">import</a> <a id="4705" href="elementary-number-theory.addition-integers.html" class="Module">elementary-number-theory.addition-integers</a>
<a id="4748" class="Keyword">open</a> <a id="4753" class="Keyword">import</a> <a id="4760" href="elementary-number-theory.addition-natural-numbers.html" class="Module">elementary-number-theory.addition-natural-numbers</a>
<a id="4810" class="Keyword">open</a> <a id="4815" class="Keyword">import</a> <a id="4822" href="elementary-number-theory.arithmetic-functions.html" class="Module">elementary-number-theory.arithmetic-functions</a>
<a id="4868" class="Keyword">open</a> <a id="4873" class="Keyword">import</a> <a id="4880" href="elementary-number-theory.binomial-coefficients.html" class="Module">elementary-number-theory.binomial-coefficients</a>
<a id="4927" class="Keyword">open</a> <a id="4932" class="Keyword">import</a> <a id="4939" href="elementary-number-theory.bounded-sums-arithmetic-functions.html" class="Module">elementary-number-theory.bounded-sums-arithmetic-functions</a>
<a id="4998" class="Keyword">open</a> <a id="5003" class="Keyword">import</a> <a id="5010" href="elementary-number-theory.catalan-numbers.html" class="Module">elementary-number-theory.catalan-numbers</a>
<a id="5051" class="Keyword">open</a> <a id="5056" class="Keyword">import</a> <a id="5063" href="elementary-number-theory.collatz-bijection.html" class="Module">elementary-number-theory.collatz-bijection</a>
<a id="5106" class="Keyword">open</a> <a id="5111" class="Keyword">import</a> <a id="5118" href="elementary-number-theory.collatz-conjecture.html" class="Module">elementary-number-theory.collatz-conjecture</a>
<a id="5162" class="Keyword">open</a> <a id="5167" class="Keyword">import</a> <a id="5174" href="elementary-number-theory.congruence-integers.html" class="Module">elementary-number-theory.congruence-integers</a>
<a id="5219" class="Keyword">open</a> <a id="5224" class="Keyword">import</a> <a id="5231" href="elementary-number-theory.congruence-natural-numbers.html" class="Module">elementary-number-theory.congruence-natural-numbers</a>
<a id="5283" class="Keyword">open</a> <a id="5288" class="Keyword">import</a> <a id="5295" href="elementary-number-theory.decidable-dependent-function-types.html" class="Module">elementary-number-theory.decidable-dependent-function-types</a>
<a id="5355" class="Keyword">open</a> <a id="5360" class="Keyword">import</a> <a id="5367" href="elementary-number-theory.decidable-types.html" class="Module">elementary-number-theory.decidable-types</a>
<a id="5408" class="Keyword">open</a> <a id="5413" class="Keyword">import</a> <a id="5420" href="elementary-number-theory.difference-integers.html" class="Module">elementary-number-theory.difference-integers</a>
<a id="5465" class="Keyword">open</a> <a id="5470" class="Keyword">import</a> <a id="5477" href="elementary-number-theory.dirichlet-convolution.html" class="Module">elementary-number-theory.dirichlet-convolution</a>
<a id="5524" class="Keyword">open</a> <a id="5529" class="Keyword">import</a> <a id="5536" href="elementary-number-theory.distance-integers.html" class="Module">elementary-number-theory.distance-integers</a>
<a id="5579" class="Keyword">open</a> <a id="5584" class="Keyword">import</a> <a id="5591" href="elementary-number-theory.distance-natural-numbers.html" class="Module">elementary-number-theory.distance-natural-numbers</a>
<a id="5641" class="Keyword">open</a> <a id="5646" class="Keyword">import</a> <a id="5653" href="elementary-number-theory.divisibility-integers.html" class="Module">elementary-number-theory.divisibility-integers</a>
<a id="5700" class="Keyword">open</a> <a id="5705" class="Keyword">import</a> <a id="5712" href="elementary-number-theory.divisibility-modular-arithmetic.html" class="Module">elementary-number-theory.divisibility-modular-arithmetic</a>
<a id="5769" class="Keyword">open</a> <a id="5774" class="Keyword">import</a> <a id="5781" href="elementary-number-theory.divisibility-natural-numbers.html" class="Module">elementary-number-theory.divisibility-natural-numbers</a>
<a id="5835" class="Keyword">open</a> <a id="5840" class="Keyword">import</a> <a id="5847" href="elementary-number-theory.divisibility-standard-finite-types.html" class="Module">elementary-number-theory.divisibility-standard-finite-types</a>
<a id="5907" class="Keyword">open</a> <a id="5912" class="Keyword">import</a> <a id="5919" href="elementary-number-theory.equality-integers.html" class="Module">elementary-number-theory.equality-integers</a>
<a id="5962" class="Keyword">open</a> <a id="5967" class="Keyword">import</a> <a id="5974" href="elementary-number-theory.equality-natural-numbers.html" class="Module">elementary-number-theory.equality-natural-numbers</a>
<a id="6024" class="Keyword">open</a> <a id="6029" class="Keyword">import</a> <a id="6036" href="elementary-number-theory.euclidean-division-natural-numbers.html" class="Module">elementary-number-theory.euclidean-division-natural-numbers</a>
<a id="6096" class="Keyword">open</a> <a id="6101" class="Keyword">import</a> <a id="6108" href="elementary-number-theory.eulers-totient-function.html" class="Module">elementary-number-theory.eulers-totient-function</a>
<a id="6157" class="Keyword">open</a> <a id="6162" class="Keyword">import</a> <a id="6169" href="elementary-number-theory.exponentiation-natural-numbers.html" class="Module">elementary-number-theory.exponentiation-natural-numbers</a>
<a id="6225" class="Keyword">open</a> <a id="6230" class="Keyword">import</a> <a id="6237" href="elementary-number-theory.factorials.html" class="Module">elementary-number-theory.factorials</a>
<a id="6273" class="Keyword">open</a> <a id="6278" class="Keyword">import</a> <a id="6285" href="elementary-number-theory.falling-factorials.html" class="Module">elementary-number-theory.falling-factorials</a>
<a id="6329" class="Keyword">open</a> <a id="6334" class="Keyword">import</a> <a id="6341" href="elementary-number-theory.fibonacci-sequence.html" class="Module">elementary-number-theory.fibonacci-sequence</a>
<a id="6385" class="Keyword">open</a> <a id="6390" class="Keyword">import</a> <a id="6397" href="elementary-number-theory.finitary-natural-numbers.html" class="Module">elementary-number-theory.finitary-natural-numbers</a>
<a id="6447" class="Keyword">open</a> <a id="6452" class="Keyword">import</a> <a id="6459" href="elementary-number-theory.finitely-cyclic-maps.html" class="Module">elementary-number-theory.finitely-cyclic-maps</a>
<a id="6505" class="Keyword">open</a> <a id="6510" class="Keyword">import</a> <a id="6517" href="elementary-number-theory.fractions.html" class="Module">elementary-number-theory.fractions</a>
<a id="6552" class="Keyword">open</a> <a id="6557" class="Keyword">import</a> <a id="6564" href="elementary-number-theory.goldbach-conjecture.html" class="Module">elementary-number-theory.goldbach-conjecture</a>
<a id="6609" class="Keyword">open</a> <a id="6614" class="Keyword">import</a> <a id="6621" href="elementary-number-theory.greatest-common-divisor-integers.html" class="Module">elementary-number-theory.greatest-common-divisor-integers</a>
<a id="6679" class="Keyword">open</a> <a id="6684" class="Keyword">import</a> <a id="6691" href="elementary-number-theory.greatest-common-divisor-natural-numbers.html" class="Module">elementary-number-theory.greatest-common-divisor-natural-numbers</a>
<a id="6756" class="Keyword">open</a> <a id="6761" class="Keyword">import</a> <a id="6768" href="elementary-number-theory.group-of-integers.html" class="Module">elementary-number-theory.group-of-integers</a>
<a id="6811" class="Keyword">open</a> <a id="6816" class="Keyword">import</a> <a id="6823" href="elementary-number-theory.groups-of-modular-arithmetic.html" class="Module">elementary-number-theory.groups-of-modular-arithmetic</a>
<a id="6877" class="Keyword">open</a> <a id="6882" class="Keyword">import</a> <a id="6889" href="elementary-number-theory.inequality-integers.html" class="Module">elementary-number-theory.inequality-integers</a>
<a id="6934" class="Keyword">open</a> <a id="6939" class="Keyword">import</a> <a id="6946" href="elementary-number-theory.inequality-natural-numbers.html" class="Module">elementary-number-theory.inequality-natural-numbers</a>
<a id="6998" class="Keyword">open</a> <a id="7003" class="Keyword">import</a> <a id="7010" href="elementary-number-theory.inequality-standard-finite-types.html" class="Module">elementary-number-theory.inequality-standard-finite-types</a>
<a id="7068" class="Keyword">open</a> <a id="7073" class="Keyword">import</a> <a id="7080" href="elementary-number-theory.infinitude-of-primes.html" class="Module">elementary-number-theory.infinitude-of-primes</a>
<a id="7126" class="Keyword">open</a> <a id="7131" class="Keyword">import</a> <a id="7138" href="elementary-number-theory.integers.html" class="Module">elementary-number-theory.integers</a>
<a id="7172" class="Keyword">open</a> <a id="7177" class="Keyword">import</a> <a id="7184" href="elementary-number-theory.iterating-functions.html" class="Module">elementary-number-theory.iterating-functions</a>
<a id="7229" class="Keyword">open</a> <a id="7234" class="Keyword">import</a> <a id="7241" href="elementary-number-theory.lower-bounds-natural-numbers.html" class="Module">elementary-number-theory.lower-bounds-natural-numbers</a>
<a id="7295" class="Keyword">open</a> <a id="7300" class="Keyword">import</a> <a id="7307" href="elementary-number-theory.maximum-natural-numbers.html" class="Module">elementary-number-theory.maximum-natural-numbers</a>
<a id="7356" class="Keyword">open</a> <a id="7361" class="Keyword">import</a> <a id="7368" href="elementary-number-theory.mersenne-primes.html" class="Module">elementary-number-theory.mersenne-primes</a>
<a id="7409" class="Keyword">open</a> <a id="7414" class="Keyword">import</a> <a id="7421" href="elementary-number-theory.minimum-natural-numbers.html" class="Module">elementary-number-theory.minimum-natural-numbers</a>
<a id="7470" class="Keyword">open</a> <a id="7475" class="Keyword">import</a> <a id="7482" href="elementary-number-theory.modular-arithmetic-standard-finite-types.html" class="Module">elementary-number-theory.modular-arithmetic-standard-finite-types</a>
<a id="7548" class="Keyword">open</a> <a id="7553" class="Keyword">import</a> <a id="7560" href="elementary-number-theory.modular-arithmetic.html" class="Module">elementary-number-theory.modular-arithmetic</a>
<a id="7604" class="Keyword">open</a> <a id="7609" class="Keyword">import</a> <a id="7616" href="elementary-number-theory.multiplication-integers.html" class="Module">elementary-number-theory.multiplication-integers</a>
<a id="7665" class="Keyword">open</a> <a id="7670" class="Keyword">import</a> <a id="7677" href="elementary-number-theory.multiplication-natural-numbers.html" class="Module">elementary-number-theory.multiplication-natural-numbers</a>
<a id="7733" class="Keyword">open</a> <a id="7738" class="Keyword">import</a> <a id="7745" href="elementary-number-theory.natural-numbers.html" class="Module">elementary-number-theory.natural-numbers</a>
<a id="7786" class="Keyword">open</a> <a id="7791" class="Keyword">import</a> <a id="7798" href="elementary-number-theory.nonzero-natural-numbers.html" class="Module">elementary-number-theory.nonzero-natural-numbers</a>
<a id="7847" class="Keyword">open</a> <a id="7852" class="Keyword">import</a> <a id="7859" href="elementary-number-theory.ordinal-induction-natural-numbers.html" class="Module">elementary-number-theory.ordinal-induction-natural-numbers</a>
<a id="7918" class="Keyword">open</a> <a id="7923" class="Keyword">import</a> <a id="7930" href="elementary-number-theory.prime-numbers.html" class="Module">elementary-number-theory.prime-numbers</a>
<a id="7969" class="Keyword">open</a> <a id="7974" class="Keyword">import</a> <a id="7981" href="elementary-number-theory.products-of-natural-numbers.html" class="Module">elementary-number-theory.products-of-natural-numbers</a>
<a id="8034" class="Keyword">open</a> <a id="8039" class="Keyword">import</a> <a id="8046" href="elementary-number-theory.proper-divisors-natural-numbers.html" class="Module">elementary-number-theory.proper-divisors-natural-numbers</a>
<a id="8103" class="Keyword">open</a> <a id="8108" class="Keyword">import</a> <a id="8115" href="elementary-number-theory.rational-numbers.html" class="Module">elementary-number-theory.rational-numbers</a>
<a id="8157" class="Keyword">open</a> <a id="8162" class="Keyword">import</a> <a id="8169" href="elementary-number-theory.relatively-prime-integers.html" class="Module">elementary-number-theory.relatively-prime-integers</a>
<a id="8220" class="Keyword">open</a> <a id="8225" class="Keyword">import</a> <a id="8232" href="elementary-number-theory.relatively-prime-natural-numbers.html" class="Module">elementary-number-theory.relatively-prime-natural-numbers</a>
<a id="8290" class="Keyword">open</a> <a id="8295" class="Keyword">import</a> <a id="8302" href="elementary-number-theory.repeating-element-standard-finite-type.html" class="Module">elementary-number-theory.repeating-element-standard-finite-type</a>
<a id="8366" class="Keyword">open</a> <a id="8371" class="Keyword">import</a> <a id="8378" href="elementary-number-theory.retracts-of-natural-numbers.html" class="Module">elementary-number-theory.retracts-of-natural-numbers</a>
<a id="8431" class="Keyword">open</a> <a id="8436" class="Keyword">import</a> <a id="8443" href="elementary-number-theory.square-free-natural-numbers.html" class="Module">elementary-number-theory.square-free-natural-numbers</a>
<a id="8496" class="Keyword">open</a> <a id="8501" class="Keyword">import</a> <a id="8508" href="elementary-number-theory.stirling-numbers-of-the-second-kind.html" class="Module">elementary-number-theory.stirling-numbers-of-the-second-kind</a>
<a id="8569" class="Keyword">open</a> <a id="8574" class="Keyword">import</a> <a id="8581" href="elementary-number-theory.strong-induction-natural-numbers.html" class="Module">elementary-number-theory.strong-induction-natural-numbers</a>
<a id="8639" class="Keyword">open</a> <a id="8644" class="Keyword">import</a> <a id="8651" href="elementary-number-theory.sums-of-natural-numbers.html" class="Module">elementary-number-theory.sums-of-natural-numbers</a>
<a id="8700" class="Keyword">open</a> <a id="8705" class="Keyword">import</a> <a id="8712" href="elementary-number-theory.triangular-numbers.html" class="Module">elementary-number-theory.triangular-numbers</a>
<a id="8756" class="Keyword">open</a> <a id="8761" class="Keyword">import</a> <a id="8768" href="elementary-number-theory.telephone-numbers.html" class="Module">elementary-number-theory.telephone-numbers</a>
<a id="8811" class="Keyword">open</a> <a id="8816" class="Keyword">import</a> <a id="8823" href="elementary-number-theory.twin-prime-conjecture.html" class="Module">elementary-number-theory.twin-prime-conjecture</a>
<a id="8870" class="Keyword">open</a> <a id="8875" class="Keyword">import</a> <a id="8882" href="elementary-number-theory.unit-elements-standard-finite-types.html" class="Module">elementary-number-theory.unit-elements-standard-finite-types</a>
<a id="8943" class="Keyword">open</a> <a id="8948" class="Keyword">import</a> <a id="8955" href="elementary-number-theory.unit-similarity-standard-finite-types.html" class="Module">elementary-number-theory.unit-similarity-standard-finite-types</a>
<a id="9018" class="Keyword">open</a> <a id="9023" class="Keyword">import</a> <a id="9030" href="elementary-number-theory.universal-property-natural-numbers.html" class="Module">elementary-number-theory.universal-property-natural-numbers</a>
<a id="9090" class="Keyword">open</a> <a id="9095" class="Keyword">import</a> <a id="9102" href="elementary-number-theory.upper-bounds-natural-numbers.html" class="Module">elementary-number-theory.upper-bounds-natural-numbers</a>
<a id="9156" class="Keyword">open</a> <a id="9161" class="Keyword">import</a> <a id="9168" href="elementary-number-theory.well-ordering-principle-natural-numbers.html" class="Module">elementary-number-theory.well-ordering-principle-natural-numbers</a>
<a id="9233" class="Keyword">open</a> <a id="9238" class="Keyword">import</a> <a id="9245" href="elementary-number-theory.well-ordering-principle-standard-finite-types.html" class="Module">elementary-number-theory.well-ordering-principle-standard-finite-types</a>
</pre>
## Finite group theory

<pre class="Agda"><a id="9353" class="Keyword">open</a> <a id="9358" class="Keyword">import</a> <a id="9365" href="finite-group-theory.html" class="Module">finite-group-theory</a>
<a id="9385" class="Keyword">open</a> <a id="9390" class="Keyword">import</a> <a id="9397" href="finite-group-theory.abstract-quaternion-group.html" class="Module">finite-group-theory.abstract-quaternion-group</a>
<a id="9443" class="Keyword">open</a> <a id="9448" class="Keyword">import</a> <a id="9455" href="finite-group-theory.concrete-quaternion-group.html" class="Module">finite-group-theory.concrete-quaternion-group</a>
<a id="9501" class="Keyword">open</a> <a id="9506" class="Keyword">import</a> <a id="9513" href="finite-group-theory.finite-groups.html" class="Module">finite-group-theory.finite-groups</a>
<a id="9547" class="Keyword">open</a> <a id="9552" class="Keyword">import</a> <a id="9559" href="finite-group-theory.finite-monoids.html" class="Module">finite-group-theory.finite-monoids</a>
<a id="9594" class="Keyword">open</a> <a id="9599" class="Keyword">import</a> <a id="9606" href="finite-group-theory.finite-semigroups.html" class="Module">finite-group-theory.finite-semigroups</a>
<a id="9644" class="Keyword">open</a> <a id="9649" class="Keyword">import</a> <a id="9656" href="finite-group-theory.groups-of-order-2.html" class="Module">finite-group-theory.groups-of-order-2</a>
<a id="9694" class="Keyword">open</a> <a id="9699" class="Keyword">import</a> <a id="9706" href="finite-group-theory.orbits-permutations.html" class="Module">finite-group-theory.orbits-permutations</a>
<a id="9746" class="Keyword">open</a> <a id="9751" class="Keyword">import</a> <a id="9758" href="finite-group-theory.permutations.html" class="Module">finite-group-theory.permutations</a>
<a id="9791" class="Keyword">open</a> <a id="9796" class="Keyword">import</a> <a id="9803" href="finite-group-theory.sign-homomorphism.html" class="Module">finite-group-theory.sign-homomorphism</a>
<a id="9841" class="Keyword">open</a> <a id="9846" class="Keyword">import</a> <a id="9853" href="finite-group-theory.transpositions.html" class="Module">finite-group-theory.transpositions</a>
</pre>
## Foundation

<pre class="Agda"><a id="9916" class="Keyword">open</a> <a id="9921" class="Keyword">import</a> <a id="9928" href="foundation.html" class="Module">foundation</a>
<a id="9939" class="Keyword">open</a> <a id="9944" class="Keyword">import</a> <a id="9951" href="foundation.0-maps.html" class="Module">foundation.0-maps</a>
<a id="9969" class="Keyword">open</a> <a id="9974" class="Keyword">import</a> <a id="9981" href="foundation.1-types.html" class="Module">foundation.1-types</a>
<a id="10000" class="Keyword">open</a> <a id="10005" class="Keyword">import</a> <a id="10012" href="foundation.2-types.html" class="Module">foundation.2-types</a>
<a id="10031" class="Keyword">open</a> <a id="10036" class="Keyword">import</a> <a id="10043" href="foundation.algebras-polynomial-endofunctors.html" class="Module">foundation.algebras-polynomial-endofunctors</a>
<a id="10087" class="Keyword">open</a> <a id="10092" class="Keyword">import</a> <a id="10099" href="foundation.automorphisms.html" class="Module">foundation.automorphisms</a>
<a id="10124" class="Keyword">open</a> <a id="10129" class="Keyword">import</a> <a id="10136" href="foundation.axiom-of-choice.html" class="Module">foundation.axiom-of-choice</a>
<a id="10163" class="Keyword">open</a> <a id="10168" class="Keyword">import</a> <a id="10175" href="foundation.binary-embeddings.html" class="Module">foundation.binary-embeddings</a>
<a id="10204" class="Keyword">open</a> <a id="10209" class="Keyword">import</a> <a id="10216" href="foundation.binary-equivalences.html" class="Module">foundation.binary-equivalences</a>
<a id="10247" class="Keyword">open</a> <a id="10252" class="Keyword">import</a> <a id="10259" href="foundation.binary-relations.html" class="Module">foundation.binary-relations</a>
<a id="10287" class="Keyword">open</a> <a id="10292" class="Keyword">import</a> <a id="10299" href="foundation.boolean-reflection.html" class="Module">foundation.boolean-reflection</a>
<a id="10329" class="Keyword">open</a> <a id="10334" class="Keyword">import</a> <a id="10341" href="foundation.booleans.html" class="Module">foundation.booleans</a>
<a id="10361" class="Keyword">open</a> <a id="10366" class="Keyword">import</a> <a id="10373" href="foundation.cantors-diagonal-argument.html" class="Module">foundation.cantors-diagonal-argument</a>
<a id="10410" class="Keyword">open</a> <a id="10415" class="Keyword">import</a> <a id="10422" href="foundation.cartesian-product-types.html" class="Module">foundation.cartesian-product-types</a>
<a id="10457" class="Keyword">open</a> <a id="10462" class="Keyword">import</a> <a id="10469" href="foundation.choice-of-representatives-equivalence-relation.html" class="Module">foundation.choice-of-representatives-equivalence-relation</a>
<a id="10527" class="Keyword">open</a> <a id="10532" class="Keyword">import</a> <a id="10539" href="foundation.coherently-invertible-maps.html" class="Module">foundation.coherently-invertible-maps</a>
<a id="10577" class="Keyword">open</a> <a id="10582" class="Keyword">import</a> <a id="10589" href="foundation.commuting-squares.html" class="Module">foundation.commuting-squares</a>
<a id="10618" class="Keyword">open</a> <a id="10623" class="Keyword">import</a> <a id="10630" href="foundation.complements.html" class="Module">foundation.complements</a>
<a id="10653" class="Keyword">open</a> <a id="10658" class="Keyword">import</a> <a id="10665" href="foundation.conjunction.html" class="Module">foundation.conjunction</a>
<a id="10688" class="Keyword">open</a> <a id="10693" class="Keyword">import</a> <a id="10700" href="foundation.connected-components-universes.html" class="Module">foundation.connected-components-universes</a>
<a id="10742" class="Keyword">open</a> <a id="10747" class="Keyword">import</a> <a id="10754" href="foundation.connected-components.html" class="Module">foundation.connected-components</a>
<a id="10786" class="Keyword">open</a> <a id="10791" class="Keyword">import</a> <a id="10798" href="foundation.connected-types.html" class="Module">foundation.connected-types</a>
<a id="10825" class="Keyword">open</a> <a id="10830" class="Keyword">import</a> <a id="10837" href="foundation.constant-maps.html" class="Module">foundation.constant-maps</a>
<a id="10862" class="Keyword">open</a> <a id="10867" class="Keyword">import</a> <a id="10874" href="foundation.contractible-maps.html" class="Module">foundation.contractible-maps</a>
<a id="10903" class="Keyword">open</a> <a id="10908" class="Keyword">import</a> <a id="10915" href="foundation.contractible-types.html" class="Module">foundation.contractible-types</a>
<a id="10945" class="Keyword">open</a> <a id="10950" class="Keyword">import</a> <a id="10957" href="foundation.coproduct-types.html" class="Module">foundation.coproduct-types</a>
<a id="10984" class="Keyword">open</a> <a id="10989" class="Keyword">import</a> <a id="10996" href="foundation.coslice.html" class="Module">foundation.coslice</a>
<a id="11015" class="Keyword">open</a> <a id="11020" class="Keyword">import</a> <a id="11027" href="foundation.decidable-dependent-function-types.html" class="Module">foundation.decidable-dependent-function-types</a>
<a id="11073" class="Keyword">open</a> <a id="11078" class="Keyword">import</a> <a id="11085" href="foundation.decidable-dependent-pair-types.html" class="Module">foundation.decidable-dependent-pair-types</a>
<a id="11127" class="Keyword">open</a> <a id="11132" class="Keyword">import</a> <a id="11139" href="foundation.decidable-embeddings.html" class="Module">foundation.decidable-embeddings</a>
<a id="11171" class="Keyword">open</a> <a id="11176" class="Keyword">import</a> <a id="11183" href="foundation.decidable-equality.html" class="Module">foundation.decidable-equality</a>
<a id="11213" class="Keyword">open</a> <a id="11218" class="Keyword">import</a> <a id="11225" href="foundation.decidable-maps.html" class="Module">foundation.decidable-maps</a>
<a id="11251" class="Keyword">open</a> <a id="11256" class="Keyword">import</a> <a id="11263" href="foundation.decidable-propositions.html" class="Module">foundation.decidable-propositions</a>
<a id="11297" class="Keyword">open</a> <a id="11302" class="Keyword">import</a> <a id="11309" href="foundation.decidable-subtypes.html" class="Module">foundation.decidable-subtypes</a>
<a id="11339" class="Keyword">open</a> <a id="11344" class="Keyword">import</a> <a id="11351" href="foundation.decidable-types.html" class="Module">foundation.decidable-types</a>
<a id="11378" class="Keyword">open</a> <a id="11383" class="Keyword">import</a> <a id="11390" href="foundation.dependent-pair-types.html" class="Module">foundation.dependent-pair-types</a>
<a id="11422" class="Keyword">open</a> <a id="11427" class="Keyword">import</a> <a id="11434" href="foundation.diagonal-maps-of-types.html" class="Module">foundation.diagonal-maps-of-types</a>
<a id="11468" class="Keyword">open</a> <a id="11473" class="Keyword">import</a> <a id="11480" href="foundation.disjunction.html" class="Module">foundation.disjunction</a>
<a id="11503" class="Keyword">open</a> <a id="11508" class="Keyword">import</a> <a id="11515" href="foundation.distributivity-of-dependent-functions-over-coproduct-types.html" class="Module">foundation.distributivity-of-dependent-functions-over-coproduct-types</a>
<a id="11585" class="Keyword">open</a> <a id="11590" class="Keyword">import</a> <a id="11597" href="foundation.distributivity-of-dependent-functions-over-dependent-pairs.html" class="Module">foundation.distributivity-of-dependent-functions-over-dependent-pairs</a>
<a id="11667" class="Keyword">open</a> <a id="11672" class="Keyword">import</a> <a id="11679" href="foundation.double-negation.html" class="Module">foundation.double-negation</a>
<a id="11706" class="Keyword">open</a> <a id="11711" class="Keyword">import</a> <a id="11718" href="foundation.dubuc-penon-compact-types.html" class="Module">foundation.dubuc-penon-compact-types</a>
<a id="11755" class="Keyword">open</a> <a id="11760" class="Keyword">import</a> <a id="11767" href="foundation.effective-maps-equivalence-relations.html" class="Module">foundation.effective-maps-equivalence-relations</a>
<a id="11815" class="Keyword">open</a> <a id="11820" class="Keyword">import</a> <a id="11827" href="foundation.elementhood-relation-w-types.html" class="Module">foundation.elementhood-relation-w-types</a>
<a id="11867" class="Keyword">open</a> <a id="11872" class="Keyword">import</a> <a id="11879" href="foundation.embeddings.html" class="Module">foundation.embeddings</a>
<a id="11901" class="Keyword">open</a> <a id="11906" class="Keyword">import</a> <a id="11913" href="foundation.empty-types.html" class="Module">foundation.empty-types</a>
<a id="11936" class="Keyword">open</a> <a id="11941" class="Keyword">import</a> <a id="11948" href="foundation.epimorphisms-with-respect-to-sets.html" class="Module">foundation.epimorphisms-with-respect-to-sets</a>
<a id="11993" class="Keyword">open</a> <a id="11998" class="Keyword">import</a> <a id="12005" href="foundation.equality-cartesian-product-types.html" class="Module">foundation.equality-cartesian-product-types</a>
<a id="12049" class="Keyword">open</a> <a id="12054" class="Keyword">import</a> <a id="12061" href="foundation.equality-coproduct-types.html" class="Module">foundation.equality-coproduct-types</a>
<a id="12097" class="Keyword">open</a> <a id="12102" class="Keyword">import</a> <a id="12109" href="foundation.equality-dependent-function-types.html" class="Module">foundation.equality-dependent-function-types</a>
<a id="12154" class="Keyword">open</a> <a id="12159" class="Keyword">import</a> <a id="12166" href="foundation.equality-dependent-pair-types.html" class="Module">foundation.equality-dependent-pair-types</a>
<a id="12207" class="Keyword">open</a> <a id="12212" class="Keyword">import</a> <a id="12219" href="foundation.equality-fibers-of-maps.html" class="Module">foundation.equality-fibers-of-maps</a>
<a id="12254" class="Keyword">open</a> <a id="12259" class="Keyword">import</a> <a id="12266" href="foundation.equivalence-classes.html" class="Module">foundation.equivalence-classes</a>
<a id="12297" class="Keyword">open</a> <a id="12302" class="Keyword">import</a> <a id="12309" href="foundation.equivalence-induction.html" class="Module">foundation.equivalence-induction</a>
<a id="12342" class="Keyword">open</a> <a id="12347" class="Keyword">import</a> <a id="12354" href="foundation.equivalence-relations.html" class="Module">foundation.equivalence-relations</a>
<a id="12387" class="Keyword">open</a> <a id="12392" class="Keyword">import</a> <a id="12399" href="foundation.equivalences-maybe.html" class="Module">foundation.equivalences-maybe</a>
<a id="12429" class="Keyword">open</a> <a id="12434" class="Keyword">import</a> <a id="12441" href="foundation.equivalences.html" class="Module">foundation.equivalences</a>
<a id="12465" class="Keyword">open</a> <a id="12470" class="Keyword">import</a> <a id="12477" href="foundation.existential-quantification.html" class="Module">foundation.existential-quantification</a>
<a id="12515" class="Keyword">open</a> <a id="12520" class="Keyword">import</a> <a id="12527" href="foundation.extensional-w-types.html" class="Module">foundation.extensional-w-types</a>
<a id="12558" class="Keyword">open</a> <a id="12563" class="Keyword">import</a> <a id="12570" href="foundation.faithful-maps.html" class="Module">foundation.faithful-maps</a>
<a id="12595" class="Keyword">open</a> <a id="12600" class="Keyword">import</a> <a id="12607" href="foundation.fiber-inclusions.html" class="Module">foundation.fiber-inclusions</a>
<a id="12635" class="Keyword">open</a> <a id="12640" class="Keyword">import</a> <a id="12647" href="foundation.fibered-maps.html" class="Module">foundation.fibered-maps</a>
<a id="12671" class="Keyword">open</a> <a id="12676" class="Keyword">import</a> <a id="12683" href="foundation.fibers-of-maps.html" class="Module">foundation.fibers-of-maps</a>
<a id="12709" class="Keyword">open</a> <a id="12714" class="Keyword">import</a> <a id="12721" href="foundation.function-extensionality.html" class="Module">foundation.function-extensionality</a>
<a id="12756" class="Keyword">open</a> <a id="12761" class="Keyword">import</a> <a id="12768" href="foundation.functions.html" class="Module">foundation.functions</a>
<a id="12789" class="Keyword">open</a> <a id="12794" class="Keyword">import</a> <a id="12801" href="foundation.functoriality-cartesian-product-types.html" class="Module">foundation.functoriality-cartesian-product-types</a>
<a id="12850" class="Keyword">open</a> <a id="12855" class="Keyword">import</a> <a id="12862" href="foundation.functoriality-coproduct-types.html" class="Module">foundation.functoriality-coproduct-types</a>
<a id="12903" class="Keyword">open</a> <a id="12908" class="Keyword">import</a> <a id="12915" href="foundation.functoriality-dependent-function-types.html" class="Module">foundation.functoriality-dependent-function-types</a>
<a id="12965" class="Keyword">open</a> <a id="12970" class="Keyword">import</a> <a id="12977" href="foundation.functoriality-dependent-pair-types.html" class="Module">foundation.functoriality-dependent-pair-types</a>
<a id="13023" class="Keyword">open</a> <a id="13028" class="Keyword">import</a> <a id="13035" href="foundation.functoriality-function-types.html" class="Module">foundation.functoriality-function-types</a>
<a id="13075" class="Keyword">open</a> <a id="13080" class="Keyword">import</a> <a id="13087" href="foundation.functoriality-propositional-truncation.html" class="Module">foundation.functoriality-propositional-truncation</a>
<a id="13137" class="Keyword">open</a> <a id="13142" class="Keyword">import</a> <a id="13149" href="foundation.functoriality-set-quotients.html" class="Module">foundation.functoriality-set-quotients</a>
<a id="13188" class="Keyword">open</a> <a id="13193" class="Keyword">import</a> <a id="13200" href="foundation.functoriality-set-truncation.html" class="Module">foundation.functoriality-set-truncation</a>
<a id="13240" class="Keyword">open</a> <a id="13245" class="Keyword">import</a> <a id="13252" href="foundation.functoriality-w-types.html" class="Module">foundation.functoriality-w-types</a>
<a id="13285" class="Keyword">open</a> <a id="13290" class="Keyword">import</a> <a id="13297" href="foundation.fundamental-theorem-of-identity-types.html" class="Module">foundation.fundamental-theorem-of-identity-types</a>
<a id="13346" class="Keyword">open</a> <a id="13351" class="Keyword">import</a> <a id="13358" href="foundation.global-choice.html" class="Module">foundation.global-choice</a>
<a id="13383" class="Keyword">open</a> <a id="13388" class="Keyword">import</a> <a id="13395" href="foundation.hilberts-epsilon-operators.html" class="Module">foundation.hilberts-epsilon-operators</a>
<a id="13433" class="Keyword">open</a> <a id="13438" class="Keyword">import</a> <a id="13445" href="foundation.homotopies.html" class="Module">foundation.homotopies</a>
<a id="13467" class="Keyword">open</a> <a id="13472" class="Keyword">import</a> <a id="13479" href="foundation.identity-systems.html" class="Module">foundation.identity-systems</a>
<a id="13507" class="Keyword">open</a> <a id="13512" class="Keyword">import</a> <a id="13519" href="foundation.identity-types.html" class="Module">foundation.identity-types</a>
<a id="13545" class="Keyword">open</a> <a id="13550" class="Keyword">import</a> <a id="13557" href="foundation.images.html" class="Module">foundation.images</a>
<a id="13575" class="Keyword">open</a> <a id="13580" class="Keyword">import</a> <a id="13587" href="foundation.impredicative-encodings.html" class="Module">foundation.impredicative-encodings</a>
<a id="13622" class="Keyword">open</a> <a id="13627" class="Keyword">import</a> <a id="13634" href="foundation.indexed-w-types.html" class="Module">foundation.indexed-w-types</a>
<a id="13661" class="Keyword">open</a> <a id="13666" class="Keyword">import</a> <a id="13673" href="foundation.induction-principle-propositional-truncation.html" class="Module">foundation.induction-principle-propositional-truncation</a>
<a id="13729" class="Keyword">open</a> <a id="13734" class="Keyword">import</a> <a id="13741" href="foundation.induction-w-types.html" class="Module">foundation.induction-w-types</a>
<a id="13770" class="Keyword">open</a> <a id="13775" class="Keyword">import</a> <a id="13782" href="foundation.inequality-w-types.html" class="Module">foundation.inequality-w-types</a>
<a id="13812" class="Keyword">open</a> <a id="13817" class="Keyword">import</a> <a id="13824" href="foundation.injective-maps.html" class="Module">foundation.injective-maps</a>
<a id="13850" class="Keyword">open</a> <a id="13855" class="Keyword">import</a> <a id="13862" href="foundation.interchange-law.html" class="Module">foundation.interchange-law</a>
<a id="13889" class="Keyword">open</a> <a id="13894" class="Keyword">import</a> <a id="13901" href="foundation.involutions.html" class="Module">foundation.involutions</a>
<a id="13924" class="Keyword">open</a> <a id="13929" class="Keyword">import</a> <a id="13936" href="foundation.isolated-points.html" class="Module">foundation.isolated-points</a>
<a id="13963" class="Keyword">open</a> <a id="13968" class="Keyword">import</a> <a id="13975" href="foundation.isomorphisms-of-sets.html" class="Module">foundation.isomorphisms-of-sets</a>
<a id="14007" class="Keyword">open</a> <a id="14012" class="Keyword">import</a> <a id="14019" href="foundation.law-of-excluded-middle.html" class="Module">foundation.law-of-excluded-middle</a>
<a id="14053" class="Keyword">open</a> <a id="14058" class="Keyword">import</a> <a id="14065" href="foundation.lawveres-fixed-point-theorem.html" class="Module">foundation.lawveres-fixed-point-theorem</a>
<a id="14105" class="Keyword">open</a> <a id="14110" class="Keyword">import</a> <a id="14117" href="foundation.locally-small-types.html" class="Module">foundation.locally-small-types</a>
<a id="14148" class="Keyword">open</a> <a id="14153" class="Keyword">import</a> <a id="14160" href="foundation.logical-equivalences.html" class="Module">foundation.logical-equivalences</a>
<a id="14192" class="Keyword">open</a> <a id="14197" class="Keyword">import</a> <a id="14204" href="foundation.lower-types-w-types.html" class="Module">foundation.lower-types-w-types</a>
<a id="14235" class="Keyword">open</a> <a id="14240" class="Keyword">import</a> <a id="14247" href="foundation.maybe.html" class="Module">foundation.maybe</a>
<a id="14264" class="Keyword">open</a> <a id="14269" class="Keyword">import</a> <a id="14276" href="foundation.mere-equality.html" class="Module">foundation.mere-equality</a>
<a id="14301" class="Keyword">open</a> <a id="14306" class="Keyword">import</a> <a id="14313" href="foundation.mere-equivalences.html" class="Module">foundation.mere-equivalences</a>
<a id="14342" class="Keyword">open</a> <a id="14347" class="Keyword">import</a> <a id="14354" href="foundation.monomorphisms.html" class="Module">foundation.monomorphisms</a>
<a id="14379" class="Keyword">open</a> <a id="14384" class="Keyword">import</a> <a id="14391" href="foundation.multisets.html" class="Module">foundation.multisets</a>
<a id="14412" class="Keyword">open</a> <a id="14417" class="Keyword">import</a> <a id="14424" href="foundation.negation.html" class="Module">foundation.negation</a>
<a id="14444" class="Keyword">open</a> <a id="14449" class="Keyword">import</a> <a id="14456" href="foundation.non-contractible-types.html" class="Module">foundation.non-contractible-types</a>
<a id="14490" class="Keyword">open</a> <a id="14495" class="Keyword">import</a> <a id="14502" href="foundation.pairs-of-distinct-elements.html" class="Module">foundation.pairs-of-distinct-elements</a>
<a id="14540" class="Keyword">open</a> <a id="14545" class="Keyword">import</a> <a id="14552" href="foundation.path-algebra.html" class="Module">foundation.path-algebra</a>
<a id="14576" class="Keyword">open</a> <a id="14581" class="Keyword">import</a> <a id="14588" href="foundation.path-split-maps.html" class="Module">foundation.path-split-maps</a>
<a id="14615" class="Keyword">open</a> <a id="14620" class="Keyword">import</a> <a id="14627" href="foundation.polynomial-endofunctors.html" class="Module">foundation.polynomial-endofunctors</a>
<a id="14662" class="Keyword">open</a> <a id="14667" class="Keyword">import</a> <a id="14674" href="foundation.principle-of-omniscience.html" class="Module">foundation.principle-of-omniscience</a>
<a id="14710" class="Keyword">open</a> <a id="14715" class="Keyword">import</a> <a id="14722" href="foundation.propositional-extensionality.html" class="Module">foundation.propositional-extensionality</a>
<a id="14762" class="Keyword">open</a> <a id="14767" class="Keyword">import</a> <a id="14774" href="foundation.propositional-maps.html" class="Module">foundation.propositional-maps</a>
<a id="14804" class="Keyword">open</a> <a id="14809" class="Keyword">import</a> <a id="14816" href="foundation.propositional-truncations.html" class="Module">foundation.propositional-truncations</a>
<a id="14853" class="Keyword">open</a> <a id="14858" class="Keyword">import</a> <a id="14865" href="foundation.propositions.html" class="Module">foundation.propositions</a>
<a id="14889" class="Keyword">open</a> <a id="14894" class="Keyword">import</a> <a id="14901" href="foundation.pullbacks.html" class="Module">foundation.pullbacks</a>
<a id="14922" class="Keyword">open</a> <a id="14927" class="Keyword">import</a> <a id="14934" href="foundation.raising-universe-levels.html" class="Module">foundation.raising-universe-levels</a>
<a id="14969" class="Keyword">open</a> <a id="14974" class="Keyword">import</a> <a id="14981" href="foundation.ranks-of-elements-w-types.html" class="Module">foundation.ranks-of-elements-w-types</a>
<a id="15018" class="Keyword">open</a> <a id="15023" class="Keyword">import</a> <a id="15030" href="foundation.reflecting-maps-equivalence-relations.html" class="Module">foundation.reflecting-maps-equivalence-relations</a>
<a id="15079" class="Keyword">open</a> <a id="15084" class="Keyword">import</a> <a id="15091" href="foundation.replacement.html" class="Module">foundation.replacement</a>
<a id="15114" class="Keyword">open</a> <a id="15119" class="Keyword">import</a> <a id="15126" href="foundation.retractions.html" class="Module">foundation.retractions</a>
<a id="15149" class="Keyword">open</a> <a id="15154" class="Keyword">import</a> <a id="15161" href="foundation.russells-paradox.html" class="Module">foundation.russells-paradox</a>
<a id="15189" class="Keyword">open</a> <a id="15194" class="Keyword">import</a> <a id="15201" href="foundation.sections.html" class="Module">foundation.sections</a>
<a id="15221" class="Keyword">open</a> <a id="15226" class="Keyword">import</a> <a id="15233" href="foundation.set-presented-types.html" class="Module">foundation.set-presented-types</a>
<a id="15264" class="Keyword">open</a> <a id="15269" class="Keyword">import</a> <a id="15276" href="foundation.set-truncations.html" class="Module">foundation.set-truncations</a>
<a id="15303" class="Keyword">open</a> <a id="15308" class="Keyword">import</a> <a id="15315" href="foundation.sets.html" class="Module">foundation.sets</a>
<a id="15331" class="Keyword">open</a> <a id="15336" class="Keyword">import</a> <a id="15343" href="foundation.singleton-induction.html" class="Module">foundation.singleton-induction</a>
<a id="15374" class="Keyword">open</a> <a id="15379" class="Keyword">import</a> <a id="15386" href="foundation.slice.html" class="Module">foundation.slice</a>
<a id="15403" class="Keyword">open</a> <a id="15408" class="Keyword">import</a> <a id="15415" href="foundation.small-maps.html" class="Module">foundation.small-maps</a>
<a id="15437" class="Keyword">open</a> <a id="15442" class="Keyword">import</a> <a id="15449" href="foundation.small-multisets.html" class="Module">foundation.small-multisets</a>
<a id="15476" class="Keyword">open</a> <a id="15481" class="Keyword">import</a> <a id="15488" href="foundation.small-types.html" class="Module">foundation.small-types</a>
<a id="15511" class="Keyword">open</a> <a id="15516" class="Keyword">import</a> <a id="15523" href="foundation.small-universes.html" class="Module">foundation.small-universes</a>
<a id="15550" class="Keyword">open</a> <a id="15555" class="Keyword">import</a> <a id="15562" href="foundation.split-surjective-maps.html" class="Module">foundation.split-surjective-maps</a>
<a id="15595" class="Keyword">open</a> <a id="15600" class="Keyword">import</a> <a id="15607" href="foundation.structure-identity-principle.html" class="Module">foundation.structure-identity-principle</a>
<a id="15647" class="Keyword">open</a> <a id="15652" class="Keyword">import</a> <a id="15659" href="foundation.structure.html" class="Module">foundation.structure</a>
<a id="15680" class="Keyword">open</a> <a id="15685" class="Keyword">import</a> <a id="15692" href="foundation.subterminal-types.html" class="Module">foundation.subterminal-types</a>
<a id="15721" class="Keyword">open</a> <a id="15726" class="Keyword">import</a> <a id="15733" href="foundation.subtype-identity-principle.html" class="Module">foundation.subtype-identity-principle</a>
<a id="15771" class="Keyword">open</a> <a id="15776" class="Keyword">import</a> <a id="15783" href="foundation.subtypes.html" class="Module">foundation.subtypes</a>
<a id="15803" class="Keyword">open</a> <a id="15808" class="Keyword">import</a> <a id="15815" href="foundation.subuniverses.html" class="Module">foundation.subuniverses</a>
<a id="15839" class="Keyword">open</a> <a id="15844" class="Keyword">import</a> <a id="15851" href="foundation.surjective-maps.html" class="Module">foundation.surjective-maps</a>
<a id="15878" class="Keyword">open</a> <a id="15883" class="Keyword">import</a> <a id="15890" href="foundation.truncated-equality.html" class="Module">foundation.truncated-equality</a>
<a id="15920" class="Keyword">open</a> <a id="15925" class="Keyword">import</a> <a id="15932" href="foundation.truncated-maps.html" class="Module">foundation.truncated-maps</a>
<a id="15958" class="Keyword">open</a> <a id="15963" class="Keyword">import</a> <a id="15970" href="foundation.truncated-types.html" class="Module">foundation.truncated-types</a>
<a id="15997" class="Keyword">open</a> <a id="16002" class="Keyword">import</a> <a id="16009" href="foundation.truncation-levels.html" class="Module">foundation.truncation-levels</a>
<a id="16038" class="Keyword">open</a> <a id="16043" class="Keyword">import</a> <a id="16050" href="foundation.truncations.html" class="Module">foundation.truncations</a>
<a id="16073" class="Keyword">open</a> <a id="16078" class="Keyword">import</a> <a id="16085" href="foundation.type-arithmetic-cartesian-product-types.html" class="Module">foundation.type-arithmetic-cartesian-product-types</a>
<a id="16136" class="Keyword">open</a> <a id="16141" class="Keyword">import</a> <a id="16148" href="foundation.type-arithmetic-coproduct-types.html" class="Module">foundation.type-arithmetic-coproduct-types</a>
<a id="16191" class="Keyword">open</a> <a id="16196" class="Keyword">import</a> <a id="16203" href="foundation.type-arithmetic-dependent-pair-types.html" class="Module">foundation.type-arithmetic-dependent-pair-types</a>
<a id="16251" class="Keyword">open</a> <a id="16256" class="Keyword">import</a> <a id="16263" href="foundation.type-arithmetic-empty-type.html" class="Module">foundation.type-arithmetic-empty-type</a>
<a id="16301" class="Keyword">open</a> <a id="16306" class="Keyword">import</a> <a id="16313" href="foundation.type-arithmetic-unit-type.html" class="Module">foundation.type-arithmetic-unit-type</a>
<a id="16350" class="Keyword">open</a> <a id="16355" class="Keyword">import</a> <a id="16362" href="foundation.uniqueness-image.html" class="Module">foundation.uniqueness-image</a>
<a id="16390" class="Keyword">open</a> <a id="16395" class="Keyword">import</a> <a id="16402" href="foundation.uniqueness-set-quotients.html" class="Module">foundation.uniqueness-set-quotients</a>
<a id="16438" class="Keyword">open</a> <a id="16443" class="Keyword">import</a> <a id="16450" href="foundation.uniqueness-set-truncations.html" class="Module">foundation.uniqueness-set-truncations</a>
<a id="16488" class="Keyword">open</a> <a id="16493" class="Keyword">import</a> <a id="16500" href="foundation.uniqueness-truncation.html" class="Module">foundation.uniqueness-truncation</a>
<a id="16533" class="Keyword">open</a> <a id="16538" class="Keyword">import</a> <a id="16545" href="foundation.unit-type.html" class="Module">foundation.unit-type</a>
<a id="16566" class="Keyword">open</a> <a id="16571" class="Keyword">import</a> <a id="16578" href="foundation.univalence-implies-function-extensionality.html" class="Module">foundation.univalence-implies-function-extensionality</a>
<a id="16632" class="Keyword">open</a> <a id="16637" class="Keyword">import</a> <a id="16644" href="foundation.univalence.html" class="Module">foundation.univalence</a>
<a id="16666" class="Keyword">open</a> <a id="16671" class="Keyword">import</a> <a id="16678" href="foundation.univalent-type-families.html" class="Module">foundation.univalent-type-families</a>
<a id="16713" class="Keyword">open</a> <a id="16718" class="Keyword">import</a> <a id="16725" href="foundation.universal-multiset.html" class="Module">foundation.universal-multiset</a>
<a id="16755" class="Keyword">open</a> <a id="16760" class="Keyword">import</a> <a id="16767" href="foundation.universal-property-booleans.html" class="Module">foundation.universal-property-booleans</a>
<a id="16806" class="Keyword">open</a> <a id="16811" class="Keyword">import</a> <a id="16818" href="foundation.universal-property-cartesian-product-types.html" class="Module">foundation.universal-property-cartesian-product-types</a>
<a id="16872" class="Keyword">open</a> <a id="16877" class="Keyword">import</a> <a id="16884" href="foundation.universal-property-coproduct-types.html" class="Module">foundation.universal-property-coproduct-types</a>
<a id="16930" class="Keyword">open</a> <a id="16935" class="Keyword">import</a> <a id="16942" href="foundation.universal-property-dependent-pair-types.html" class="Module">foundation.universal-property-dependent-pair-types</a>
<a id="16993" class="Keyword">open</a> <a id="16998" class="Keyword">import</a> <a id="17005" href="foundation.universal-property-empty-type.html" class="Module">foundation.universal-property-empty-type</a>
<a id="17046" class="Keyword">open</a> <a id="17051" class="Keyword">import</a> <a id="17058" href="foundation.universal-property-fiber-products.html" class="Module">foundation.universal-property-fiber-products</a>
<a id="17103" class="Keyword">open</a> <a id="17108" class="Keyword">import</a> <a id="17115" href="foundation.universal-property-identity-types.html" class="Module">foundation.universal-property-identity-types</a>
<a id="17160" class="Keyword">open</a> <a id="17165" class="Keyword">import</a> <a id="17172" href="foundation.universal-property-image.html" class="Module">foundation.universal-property-image</a>
<a id="17208" class="Keyword">open</a> <a id="17213" class="Keyword">import</a> <a id="17220" href="foundation.universal-property-maybe.html" class="Module">foundation.universal-property-maybe</a>
<a id="17256" class="Keyword">open</a> <a id="17261" class="Keyword">import</a> <a id="17268" href="foundation.universal-property-propositional-truncation-into-sets.html" class="Module">foundation.universal-property-propositional-truncation-into-sets</a>
<a id="17333" class="Keyword">open</a> <a id="17338" class="Keyword">import</a> <a id="17345" href="foundation.universal-property-propositional-truncation.html" class="Module">foundation.universal-property-propositional-truncation</a>
<a id="17400" class="Keyword">open</a> <a id="17405" class="Keyword">import</a> <a id="17412" href="foundation.universal-property-pullbacks.html" class="Module">foundation.universal-property-pullbacks</a>
<a id="17452" class="Keyword">open</a> <a id="17457" class="Keyword">import</a> <a id="17464" href="foundation.universal-property-set-quotients.html" class="Module">foundation.universal-property-set-quotients</a>
<a id="17508" class="Keyword">open</a> <a id="17513" class="Keyword">import</a> <a id="17520" href="foundation.universal-property-set-truncation.html" class="Module">foundation.universal-property-set-truncation</a>
<a id="17565" class="Keyword">open</a> <a id="17570" class="Keyword">import</a> <a id="17577" href="foundation.universal-property-truncation.html" class="Module">foundation.universal-property-truncation</a>
<a id="17618" class="Keyword">open</a> <a id="17623" class="Keyword">import</a> <a id="17630" href="foundation.universal-property-unit-type.html" class="Module">foundation.universal-property-unit-type</a>
<a id="17670" class="Keyword">open</a> <a id="17675" class="Keyword">import</a> <a id="17682" href="foundation.universe-levels.html" class="Module">foundation.universe-levels</a>
<a id="17709" class="Keyword">open</a> <a id="17714" class="Keyword">import</a> <a id="17721" href="foundation.unordered-pairs.html" class="Module">foundation.unordered-pairs</a>
<a id="17748" class="Keyword">open</a> <a id="17753" class="Keyword">import</a> <a id="17760" href="foundation.w-types.html" class="Module">foundation.w-types</a>
<a id="17779" class="Keyword">open</a> <a id="17784" class="Keyword">import</a> <a id="17791" href="foundation.weak-function-extensionality.html" class="Module">foundation.weak-function-extensionality</a>
<a id="17831" class="Keyword">open</a> <a id="17836" class="Keyword">import</a> <a id="17843" href="foundation.weakly-constant-maps.html" class="Module">foundation.weakly-constant-maps</a>
</pre>
## Foundation Core

<pre class="Agda"><a id="17908" class="Keyword">open</a> <a id="17913" class="Keyword">import</a> <a id="17920" href="foundation-core.0-maps.html" class="Module">foundation-core.0-maps</a>
<a id="17943" class="Keyword">open</a> <a id="17948" class="Keyword">import</a> <a id="17955" href="foundation-core.1-types.html" class="Module">foundation-core.1-types</a>
<a id="17979" class="Keyword">open</a> <a id="17984" class="Keyword">import</a> <a id="17991" href="foundation-core.cartesian-product-types.html" class="Module">foundation-core.cartesian-product-types</a>
<a id="18031" class="Keyword">open</a> <a id="18036" class="Keyword">import</a> <a id="18043" href="foundation-core.coherently-invertible-maps.html" class="Module">foundation-core.coherently-invertible-maps</a>
<a id="18086" class="Keyword">open</a> <a id="18091" class="Keyword">import</a> <a id="18098" href="foundation-core.commuting-squares.html" class="Module">foundation-core.commuting-squares</a>
<a id="18132" class="Keyword">open</a> <a id="18137" class="Keyword">import</a> <a id="18144" href="foundation-core.constant-maps.html" class="Module">foundation-core.constant-maps</a>
<a id="18174" class="Keyword">open</a> <a id="18179" class="Keyword">import</a> <a id="18186" href="foundation-core.contractible-maps.html" class="Module">foundation-core.contractible-maps</a>
<a id="18220" class="Keyword">open</a> <a id="18225" class="Keyword">import</a> <a id="18232" href="foundation-core.contractible-types.html" class="Module">foundation-core.contractible-types</a>
<a id="18267" class="Keyword">open</a> <a id="18272" class="Keyword">import</a> <a id="18279" href="foundation-core.dependent-pair-types.html" class="Module">foundation-core.dependent-pair-types</a>
<a id="18316" class="Keyword">open</a> <a id="18321" class="Keyword">import</a> <a id="18328" href="foundation-core.embeddings.html" class="Module">foundation-core.embeddings</a>
<a id="18355" class="Keyword">open</a> <a id="18360" class="Keyword">import</a> <a id="18367" href="foundation-core.empty-types.html" class="Module">foundation-core.empty-types</a>
<a id="18395" class="Keyword">open</a> <a id="18400" class="Keyword">import</a> <a id="18407" href="foundation-core.equality-cartesian-product-types.html" class="Module">foundation-core.equality-cartesian-product-types</a>
<a id="18456" class="Keyword">open</a> <a id="18461" class="Keyword">import</a> <a id="18468" href="foundation-core.equality-dependent-pair-types.html" class="Module">foundation-core.equality-dependent-pair-types</a>
<a id="18514" class="Keyword">open</a> <a id="18519" class="Keyword">import</a> <a id="18526" href="foundation-core.equality-fibers-of-maps.html" class="Module">foundation-core.equality-fibers-of-maps</a>
<a id="18566" class="Keyword">open</a> <a id="18571" class="Keyword">import</a> <a id="18578" href="foundation-core.equivalence-induction.html" class="Module">foundation-core.equivalence-induction</a>
<a id="18616" class="Keyword">open</a> <a id="18621" class="Keyword">import</a> <a id="18628" href="foundation-core.equivalences.html" class="Module">foundation-core.equivalences</a>
<a id="18657" class="Keyword">open</a> <a id="18662" class="Keyword">import</a> <a id="18669" href="foundation-core.faithful-maps.html" class="Module">foundation-core.faithful-maps</a>
<a id="18699" class="Keyword">open</a> <a id="18704" class="Keyword">import</a> <a id="18711" href="foundation-core.fibers-of-maps.html" class="Module">foundation-core.fibers-of-maps</a>
<a id="18742" class="Keyword">open</a> <a id="18747" class="Keyword">import</a> <a id="18754" href="foundation-core.functions.html" class="Module">foundation-core.functions</a>
<a id="18780" class="Keyword">open</a> <a id="18785" class="Keyword">import</a> <a id="18792" href="foundation-core.functoriality-dependent-pair-types.html" class="Module">foundation-core.functoriality-dependent-pair-types</a>
<a id="18843" class="Keyword">open</a> <a id="18848" class="Keyword">import</a> <a id="18855" href="foundation-core.fundamental-theorem-of-identity-types.html" class="Module">foundation-core.fundamental-theorem-of-identity-types</a>
<a id="18909" class="Keyword">open</a> <a id="18914" class="Keyword">import</a> <a id="18921" href="foundation-core.homotopies.html" class="Module">foundation-core.homotopies</a>
<a id="18948" class="Keyword">open</a> <a id="18953" class="Keyword">import</a> <a id="18960" href="foundation-core.identity-systems.html" class="Module">foundation-core.identity-systems</a>
<a id="18993" class="Keyword">open</a> <a id="18998" class="Keyword">import</a> <a id="19005" href="foundation-core.identity-types.html" class="Module">foundation-core.identity-types</a>
<a id="19036" class="Keyword">open</a> <a id="19041" class="Keyword">import</a> <a id="19048" href="foundation-core.logical-equivalences.html" class="Module">foundation-core.logical-equivalences</a>
<a id="19085" class="Keyword">open</a> <a id="19090" class="Keyword">import</a> <a id="19097" href="foundation-core.negation.html" class="Module">foundation-core.negation</a>
<a id="19122" class="Keyword">open</a> <a id="19127" class="Keyword">import</a> <a id="19134" href="foundation-core.path-split-maps.html" class="Module">foundation-core.path-split-maps</a>
<a id="19166" class="Keyword">open</a> <a id="19171" class="Keyword">import</a> <a id="19178" href="foundation-core.propositional-maps.html" class="Module">foundation-core.propositional-maps</a>
<a id="19213" class="Keyword">open</a> <a id="19218" class="Keyword">import</a> <a id="19225" href="foundation-core.propositions.html" class="Module">foundation-core.propositions</a>
<a id="19254" class="Keyword">open</a> <a id="19259" class="Keyword">import</a> <a id="19266" href="foundation-core.retractions.html" class="Module">foundation-core.retractions</a>
<a id="19294" class="Keyword">open</a> <a id="19299" class="Keyword">import</a> <a id="19306" href="foundation-core.sections.html" class="Module">foundation-core.sections</a>
<a id="19331" class="Keyword">open</a> <a id="19336" class="Keyword">import</a> <a id="19343" href="foundation-core.sets.html" class="Module">foundation-core.sets</a>
<a id="19364" class="Keyword">open</a> <a id="19369" class="Keyword">import</a> <a id="19376" href="foundation-core.singleton-induction.html" class="Module">foundation-core.singleton-induction</a>
<a id="19412" class="Keyword">open</a> <a id="19417" class="Keyword">import</a> <a id="19424" href="foundation-core.subtype-identity-principle.html" class="Module">foundation-core.subtype-identity-principle</a>
<a id="19467" class="Keyword">open</a> <a id="19472" class="Keyword">import</a> <a id="19479" href="foundation-core.subtypes.html" class="Module">foundation-core.subtypes</a>
<a id="19504" class="Keyword">open</a> <a id="19509" class="Keyword">import</a> <a id="19516" href="foundation-core.truncated-maps.html" class="Module">foundation-core.truncated-maps</a>
<a id="19547" class="Keyword">open</a> <a id="19552" class="Keyword">import</a> <a id="19559" href="foundation-core.truncated-types.html" class="Module">foundation-core.truncated-types</a>
<a id="19591" class="Keyword">open</a> <a id="19596" class="Keyword">import</a> <a id="19603" href="foundation-core.truncation-levels.html" class="Module">foundation-core.truncation-levels</a>
<a id="19637" class="Keyword">open</a> <a id="19642" class="Keyword">import</a> <a id="19649" href="foundation-core.type-arithmetic-cartesian-product-types.html" class="Module">foundation-core.type-arithmetic-cartesian-product-types</a>
<a id="19705" class="Keyword">open</a> <a id="19710" class="Keyword">import</a> <a id="19717" href="foundation-core.type-arithmetic-dependent-pair-types.html" class="Module">foundation-core.type-arithmetic-dependent-pair-types</a>
<a id="19770" class="Keyword">open</a> <a id="19775" class="Keyword">import</a> <a id="19782" href="foundation-core.univalence.html" class="Module">foundation-core.univalence</a>
<a id="19809" class="Keyword">open</a> <a id="19814" class="Keyword">import</a> <a id="19821" href="foundation-core.universe-levels.html" class="Module">foundation-core.universe-levels</a>
</pre>
## Graph theory

<pre class="Agda"><a id="19883" class="Keyword">open</a> <a id="19888" class="Keyword">import</a> <a id="19895" href="graph-theory.html" class="Module">graph-theory</a>
<a id="19908" class="Keyword">open</a> <a id="19913" class="Keyword">import</a> <a id="19920" href="graph-theory.connected-undirected-graphs.html" class="Module">graph-theory.connected-undirected-graphs</a>
<a id="19961" class="Keyword">open</a> <a id="19966" class="Keyword">import</a> <a id="19973" href="graph-theory.directed-graphs.html" class="Module">graph-theory.directed-graphs</a>
<a id="20002" class="Keyword">open</a> <a id="20007" class="Keyword">import</a> <a id="20014" href="graph-theory.edge-coloured-undirected-graphs.html" class="Module">graph-theory.edge-coloured-undirected-graphs</a>
<a id="20059" class="Keyword">open</a> <a id="20064" class="Keyword">import</a> <a id="20071" href="graph-theory.equivalences-undirected-graphs.html" class="Module">graph-theory.equivalences-undirected-graphs</a>
<a id="20115" class="Keyword">open</a> <a id="20120" class="Keyword">import</a> <a id="20127" href="graph-theory.finite-graphs.html" class="Module">graph-theory.finite-graphs</a>
<a id="20154" class="Keyword">open</a> <a id="20159" class="Keyword">import</a> <a id="20166" href="graph-theory.incidence-undirected-graphs.html" class="Module">graph-theory.incidence-undirected-graphs</a>
<a id="20207" class="Keyword">open</a> <a id="20212" class="Keyword">import</a> <a id="20219" href="graph-theory.matchings.html" class="Module">graph-theory.matchings</a>
<a id="20242" class="Keyword">open</a> <a id="20247" class="Keyword">import</a> <a id="20254" href="graph-theory.mere-equivalences-undirected-graphs.html" class="Module">graph-theory.mere-equivalences-undirected-graphs</a>
<a id="20303" class="Keyword">open</a> <a id="20308" class="Keyword">import</a> <a id="20315" href="graph-theory.morphisms-directed-graphs.html" class="Module">graph-theory.morphisms-directed-graphs</a>
<a id="20354" class="Keyword">open</a> <a id="20359" class="Keyword">import</a> <a id="20366" href="graph-theory.morphisms-undirected-graphs.html" class="Module">graph-theory.morphisms-undirected-graphs</a>
<a id="20407" class="Keyword">open</a> <a id="20412" class="Keyword">import</a> <a id="20419" href="graph-theory.orientations-undirected-graphs.html" class="Module">graph-theory.orientations-undirected-graphs</a>
<a id="20463" class="Keyword">open</a> <a id="20468" class="Keyword">import</a> <a id="20475" href="graph-theory.paths-undirected-graphs.html" class="Module">graph-theory.paths-undirected-graphs</a>
<a id="20512" class="Keyword">open</a> <a id="20517" class="Keyword">import</a> <a id="20524" href="graph-theory.polygons.html" class="Module">graph-theory.polygons</a>
<a id="20546" class="Keyword">open</a> <a id="20551" class="Keyword">import</a> <a id="20558" href="graph-theory.reflexive-graphs.html" class="Module">graph-theory.reflexive-graphs</a>
<a id="20588" class="Keyword">open</a> <a id="20593" class="Keyword">import</a> <a id="20600" href="graph-theory.regular-undirected-graphs.html" class="Module">graph-theory.regular-undirected-graphs</a>
<a id="20639" class="Keyword">open</a> <a id="20644" class="Keyword">import</a> <a id="20651" href="graph-theory.simple-undirected-graphs.html" class="Module">graph-theory.simple-undirected-graphs</a>
<a id="20689" class="Keyword">open</a> <a id="20694" class="Keyword">import</a> <a id="20701" href="graph-theory.undirected-graphs.html" class="Module">graph-theory.undirected-graphs</a>
<a id="20732" class="Keyword">open</a> <a id="20737" class="Keyword">import</a> <a id="20744" href="graph-theory.voltage-graphs.html" class="Module">graph-theory.voltage-graphs</a>
</pre>
## Group theory

<pre class="Agda"><a id="20802" class="Keyword">open</a> <a id="20807" class="Keyword">import</a> <a id="20814" href="group-theory.html" class="Module">group-theory</a>
<a id="20827" class="Keyword">open</a> <a id="20832" class="Keyword">import</a> <a id="20839" href="group-theory.abelian-groups.html" class="Module">group-theory.abelian-groups</a>
<a id="20867" class="Keyword">open</a> <a id="20872" class="Keyword">import</a> <a id="20879" href="group-theory.abelian-subgroups.html" class="Module">group-theory.abelian-subgroups</a>
<a id="20910" class="Keyword">open</a> <a id="20915" class="Keyword">import</a> <a id="20922" href="group-theory.abstract-group-torsors.html" class="Module">group-theory.abstract-group-torsors</a>
<a id="20958" class="Keyword">open</a> <a id="20963" class="Keyword">import</a> <a id="20970" href="group-theory.addition-homomorphisms-abelian-groups.html" class="Module">group-theory.addition-homomorphisms-abelian-groups</a>
<a id="21021" class="Keyword">open</a> <a id="21026" class="Keyword">import</a> <a id="21033" href="group-theory.category-of-groups.html" class="Module">group-theory.category-of-groups</a>
<a id="21065" class="Keyword">open</a> <a id="21070" class="Keyword">import</a> <a id="21077" href="group-theory.category-of-semigroups.html" class="Module">group-theory.category-of-semigroups</a>
<a id="21113" class="Keyword">open</a> <a id="21118" class="Keyword">import</a> <a id="21125" href="group-theory.cayleys-theorem.html" class="Module">group-theory.cayleys-theorem</a>
<a id="21154" class="Keyword">open</a> <a id="21159" class="Keyword">import</a> <a id="21166" href="group-theory.concrete-group-actions.html" class="Module">group-theory.concrete-group-actions</a>
<a id="21202" class="Keyword">open</a> <a id="21207" class="Keyword">import</a> <a id="21214" href="group-theory.concrete-groups.html" class="Module">group-theory.concrete-groups</a>
<a id="21243" class="Keyword">open</a> <a id="21248" class="Keyword">import</a> <a id="21255" href="group-theory.concrete-subgroups.html" class="Module">group-theory.concrete-subgroups</a>
<a id="21287" class="Keyword">open</a> <a id="21292" class="Keyword">import</a> <a id="21299" href="group-theory.conjugation.html" class="Module">group-theory.conjugation</a>
<a id="21324" class="Keyword">open</a> <a id="21329" class="Keyword">import</a> <a id="21336" href="group-theory.embeddings-groups.html" class="Module">group-theory.embeddings-groups</a>
<a id="21367" class="Keyword">open</a> <a id="21372" class="Keyword">import</a> <a id="21379" href="group-theory.endomorphism-rings-abelian-groups.html" class="Module">group-theory.endomorphism-rings-abelian-groups</a>
<a id="21426" class="Keyword">open</a> <a id="21431" class="Keyword">import</a> <a id="21438" href="group-theory.equivalences-group-actions.html" class="Module">group-theory.equivalences-group-actions</a>
<a id="21478" class="Keyword">open</a> <a id="21483" class="Keyword">import</a> <a id="21490" href="group-theory.equivalences-semigroups.html" class="Module">group-theory.equivalences-semigroups</a>
<a id="21527" class="Keyword">open</a> <a id="21532" class="Keyword">import</a> <a id="21539" href="group-theory.examples-higher-groups.html" class="Module">group-theory.examples-higher-groups</a>
<a id="21575" class="Keyword">open</a> <a id="21580" class="Keyword">import</a> <a id="21587" href="group-theory.furstenberg-groups.html" class="Module">group-theory.furstenberg-groups</a>
<a id="21619" class="Keyword">open</a> <a id="21624" class="Keyword">import</a> <a id="21631" href="group-theory.group-actions.html" class="Module">group-theory.group-actions</a>
<a id="21658" class="Keyword">open</a> <a id="21663" class="Keyword">import</a> <a id="21670" href="group-theory.groups.html" class="Module">group-theory.groups</a>
<a id="21690" class="Keyword">open</a> <a id="21695" class="Keyword">import</a> <a id="21702" href="group-theory.higher-groups.html" class="Module">group-theory.higher-groups</a>
<a id="21729" class="Keyword">open</a> <a id="21734" class="Keyword">import</a> <a id="21741" href="group-theory.homomorphisms-abelian-groups.html" class="Module">group-theory.homomorphisms-abelian-groups</a>
<a id="21783" class="Keyword">open</a> <a id="21788" class="Keyword">import</a> <a id="21795" href="group-theory.homomorphisms-group-actions.html" class="Module">group-theory.homomorphisms-group-actions</a>
<a id="21836" class="Keyword">open</a> <a id="21841" class="Keyword">import</a> <a id="21848" href="group-theory.homomorphisms-groups.html" class="Module">group-theory.homomorphisms-groups</a>
<a id="21882" class="Keyword">open</a> <a id="21887" class="Keyword">import</a> <a id="21894" href="group-theory.homomorphisms-monoids.html" class="Module">group-theory.homomorphisms-monoids</a>
<a id="21929" class="Keyword">open</a> <a id="21934" class="Keyword">import</a> <a id="21941" href="group-theory.homomorphisms-semigroups.html" class="Module">group-theory.homomorphisms-semigroups</a>
<a id="21979" class="Keyword">open</a> <a id="21984" class="Keyword">import</a> <a id="21991" href="group-theory.inverse-semigroups.html" class="Module">group-theory.inverse-semigroups</a>
<a id="22023" class="Keyword">open</a> <a id="22028" class="Keyword">import</a> <a id="22035" href="group-theory.invertible-elements-monoids.html" class="Module">group-theory.invertible-elements-monoids</a>
<a id="22076" class="Keyword">open</a> <a id="22081" class="Keyword">import</a> <a id="22088" href="group-theory.isomorphisms-abelian-groups.html" class="Module">group-theory.isomorphisms-abelian-groups</a>
<a id="22129" class="Keyword">open</a> <a id="22134" class="Keyword">import</a> <a id="22141" href="group-theory.isomorphisms-group-actions.html" class="Module">group-theory.isomorphisms-group-actions</a>
<a id="22181" class="Keyword">open</a> <a id="22186" class="Keyword">import</a> <a id="22193" href="group-theory.isomorphisms-groups.html" class="Module">group-theory.isomorphisms-groups</a>
<a id="22226" class="Keyword">open</a> <a id="22231" class="Keyword">import</a> <a id="22238" href="group-theory.isomorphisms-semigroups.html" class="Module">group-theory.isomorphisms-semigroups</a>
<a id="22275" class="Keyword">open</a> <a id="22280" class="Keyword">import</a> <a id="22287" href="group-theory.mere-equivalences-group-actions.html" class="Module">group-theory.mere-equivalences-group-actions</a>
<a id="22332" class="Keyword">open</a> <a id="22337" class="Keyword">import</a> <a id="22344" href="group-theory.monoids.html" class="Module">group-theory.monoids</a>
<a id="22365" class="Keyword">open</a> <a id="22370" class="Keyword">import</a> <a id="22377" href="group-theory.orbits-group-actions.html" class="Module">group-theory.orbits-group-actions</a>
<a id="22411" class="Keyword">open</a> <a id="22416" class="Keyword">import</a> <a id="22423" href="group-theory.precategory-of-group-actions.html" class="Module">group-theory.precategory-of-group-actions</a>
<a id="22465" class="Keyword">open</a> <a id="22470" class="Keyword">import</a> <a id="22477" href="group-theory.precategory-of-groups.html" class="Module">group-theory.precategory-of-groups</a>
<a id="22512" class="Keyword">open</a> <a id="22517" class="Keyword">import</a> <a id="22524" href="group-theory.precategory-of-semigroups.html" class="Module">group-theory.precategory-of-semigroups</a>
<a id="22563" class="Keyword">open</a> <a id="22568" class="Keyword">import</a> <a id="22575" href="group-theory.principal-group-actions.html" class="Module">group-theory.principal-group-actions</a>
<a id="22612" class="Keyword">open</a> <a id="22617" class="Keyword">import</a> <a id="22624" href="group-theory.semigroups.html" class="Module">group-theory.semigroups</a>
<a id="22648" class="Keyword">open</a> <a id="22653" class="Keyword">import</a> <a id="22660" href="group-theory.sheargroups.html" class="Module">group-theory.sheargroups</a>
<a id="22685" class="Keyword">open</a> <a id="22690" class="Keyword">import</a> <a id="22697" href="group-theory.stabilizer-groups.html" class="Module">group-theory.stabilizer-groups</a>
<a id="22728" class="Keyword">open</a> <a id="22733" class="Keyword">import</a> <a id="22740" href="group-theory.subgroups.html" class="Module">group-theory.subgroups</a>
<a id="22763" class="Keyword">open</a> <a id="22768" class="Keyword">import</a> <a id="22775" href="group-theory.substitution-functor-group-actions.html" class="Module">group-theory.substitution-functor-group-actions</a>
<a id="22823" class="Keyword">open</a> <a id="22828" class="Keyword">import</a> <a id="22835" href="group-theory.symmetric-groups.html" class="Module">group-theory.symmetric-groups</a>
<a id="22865" class="Keyword">open</a> <a id="22870" class="Keyword">import</a> <a id="22877" href="group-theory.transitive-group-actions.html" class="Module">group-theory.transitive-group-actions</a>
</pre>
## Linear algebra

<pre class="Agda"><a id="22947" class="Keyword">open</a> <a id="22952" class="Keyword">import</a> <a id="22959" href="linear-algebra.html" class="Module">linear-algebra</a>
<a id="22974" class="Keyword">open</a> <a id="22979" class="Keyword">import</a> <a id="22986" href="linear-algebra.constant-matrices.html" class="Module">linear-algebra.constant-matrices</a>
<a id="23019" class="Keyword">open</a> <a id="23024" class="Keyword">import</a> <a id="23031" href="linear-algebra.constant-vectors.html" class="Module">linear-algebra.constant-vectors</a>
<a id="23063" class="Keyword">open</a> <a id="23068" class="Keyword">import</a> <a id="23075" href="linear-algebra.diagonal-matrices-on-rings.html" class="Module">linear-algebra.diagonal-matrices-on-rings</a>
<a id="23117" class="Keyword">open</a> <a id="23122" class="Keyword">import</a> <a id="23129" href="linear-algebra.functoriality-matrices.html" class="Module">linear-algebra.functoriality-matrices</a>
<a id="23167" class="Keyword">open</a> <a id="23172" class="Keyword">import</a> <a id="23179" href="linear-algebra.functoriality-vectors.html" class="Module">linear-algebra.functoriality-vectors</a>
<a id="23216" class="Keyword">open</a> <a id="23221" class="Keyword">import</a> <a id="23228" href="linear-algebra.matrices-on-rings.html" class="Module">linear-algebra.matrices-on-rings</a>
<a id="23261" class="Keyword">open</a> <a id="23266" class="Keyword">import</a> <a id="23273" href="linear-algebra.matrices.html" class="Module">linear-algebra.matrices</a>
<a id="23297" class="Keyword">open</a> <a id="23302" class="Keyword">import</a> <a id="23309" href="linear-algebra.multiplication-matrices.html" class="Module">linear-algebra.multiplication-matrices</a>
<a id="23348" class="Keyword">open</a> <a id="23353" class="Keyword">import</a> <a id="23360" href="linear-algebra.scalar-multiplication-matrices.html" class="Module">linear-algebra.scalar-multiplication-matrices</a>
<a id="23406" class="Keyword">open</a> <a id="23411" class="Keyword">import</a> <a id="23418" href="linear-algebra.scalar-multiplication-vectors.html" class="Module">linear-algebra.scalar-multiplication-vectors</a>
<a id="23463" class="Keyword">open</a> <a id="23468" class="Keyword">import</a> <a id="23475" href="linear-algebra.transposition-matrices.html" class="Module">linear-algebra.transposition-matrices</a>
<a id="23513" class="Keyword">open</a> <a id="23518" class="Keyword">import</a> <a id="23525" href="linear-algebra.vectors-on-rings.html" class="Module">linear-algebra.vectors-on-rings</a>
<a id="23557" class="Keyword">open</a> <a id="23562" class="Keyword">import</a> <a id="23569" href="linear-algebra.vectors.html" class="Module">linear-algebra.vectors</a>
</pre>
## Order theory

<pre class="Agda"><a id="23622" class="Keyword">open</a> <a id="23627" class="Keyword">import</a> <a id="23634" href="order-theory.html" class="Module">order-theory</a>
<a id="23647" class="Keyword">open</a> <a id="23652" class="Keyword">import</a> <a id="23659" href="order-theory.chains-posets.html" class="Module">order-theory.chains-posets</a>
<a id="23686" class="Keyword">open</a> <a id="23691" class="Keyword">import</a> <a id="23698" href="order-theory.chains-preorders.html" class="Module">order-theory.chains-preorders</a>
<a id="23728" class="Keyword">open</a> <a id="23733" class="Keyword">import</a> <a id="23740" href="order-theory.decidable-subposets.html" class="Module">order-theory.decidable-subposets</a>
<a id="23773" class="Keyword">open</a> <a id="23778" class="Keyword">import</a> <a id="23785" href="order-theory.decidable-subpreorders.html" class="Module">order-theory.decidable-subpreorders</a>
<a id="23821" class="Keyword">open</a> <a id="23826" class="Keyword">import</a> <a id="23833" href="order-theory.finite-posets.html" class="Module">order-theory.finite-posets</a>
<a id="23860" class="Keyword">open</a> <a id="23865" class="Keyword">import</a> <a id="23872" href="order-theory.finite-preorders.html" class="Module">order-theory.finite-preorders</a>
<a id="23902" class="Keyword">open</a> <a id="23907" class="Keyword">import</a> <a id="23914" href="order-theory.finitely-graded-posets.html" class="Module">order-theory.finitely-graded-posets</a>
<a id="23950" class="Keyword">open</a> <a id="23955" class="Keyword">import</a> <a id="23962" href="order-theory.greatest-lower-bounds-posets.html" class="Module">order-theory.greatest-lower-bounds-posets</a>
<a id="24004" class="Keyword">open</a> <a id="24009" class="Keyword">import</a> <a id="24016" href="order-theory.interval-subposets.html" class="Module">order-theory.interval-subposets</a>
<a id="24048" class="Keyword">open</a> <a id="24053" class="Keyword">import</a> <a id="24060" href="order-theory.largest-elements-posets.html" class="Module">order-theory.largest-elements-posets</a>
<a id="24097" class="Keyword">open</a> <a id="24102" class="Keyword">import</a> <a id="24109" href="order-theory.largest-elements-preorders.html" class="Module">order-theory.largest-elements-preorders</a>
<a id="24149" class="Keyword">open</a> <a id="24154" class="Keyword">import</a> <a id="24161" href="order-theory.least-elements-posets.html" class="Module">order-theory.least-elements-posets</a>
<a id="24196" class="Keyword">open</a> <a id="24201" class="Keyword">import</a> <a id="24208" href="order-theory.least-elements-preorders.html" class="Module">order-theory.least-elements-preorders</a>
<a id="24246" class="Keyword">open</a> <a id="24251" class="Keyword">import</a> <a id="24258" href="order-theory.locally-finite-posets.html" class="Module">order-theory.locally-finite-posets</a>
<a id="24293" class="Keyword">open</a> <a id="24298" class="Keyword">import</a> <a id="24305" href="order-theory.maximal-chains-posets.html" class="Module">order-theory.maximal-chains-posets</a>
<a id="24340" class="Keyword">open</a> <a id="24345" class="Keyword">import</a> <a id="24352" href="order-theory.maximal-chains-preorders.html" class="Module">order-theory.maximal-chains-preorders</a>
<a id="24390" class="Keyword">open</a> <a id="24395" class="Keyword">import</a> <a id="24402" href="order-theory.meet-semilattices.html" class="Module">order-theory.meet-semilattices</a>
<a id="24433" class="Keyword">open</a> <a id="24438" class="Keyword">import</a> <a id="24445" href="order-theory.planar-binary-trees.html" class="Module">order-theory.planar-binary-trees</a>
<a id="24478" class="Keyword">open</a> <a id="24483" class="Keyword">import</a> <a id="24490" href="order-theory.posets.html" class="Module">order-theory.posets</a>
<a id="24510" class="Keyword">open</a> <a id="24515" class="Keyword">import</a> <a id="24522" href="order-theory.preorders.html" class="Module">order-theory.preorders</a>
<a id="24545" class="Keyword">open</a> <a id="24550" class="Keyword">import</a> <a id="24557" href="order-theory.subposets.html" class="Module">order-theory.subposets</a>
<a id="24580" class="Keyword">open</a> <a id="24585" class="Keyword">import</a> <a id="24592" href="order-theory.subpreorders.html" class="Module">order-theory.subpreorders</a>
<a id="24618" class="Keyword">open</a> <a id="24623" class="Keyword">import</a> <a id="24630" href="order-theory.total-posets.html" class="Module">order-theory.total-posets</a>
<a id="24656" class="Keyword">open</a> <a id="24661" class="Keyword">import</a> <a id="24668" href="order-theory.total-preorders.html" class="Module">order-theory.total-preorders</a>
</pre>
## Polytopes

<pre class="Agda"><a id="24724" class="Keyword">open</a> <a id="24729" class="Keyword">import</a> <a id="24736" href="polytopes.html" class="Module">polytopes</a>
<a id="24746" class="Keyword">open</a> <a id="24751" class="Keyword">import</a> <a id="24758" href="polytopes.abstract-polytopes.html" class="Module">polytopes.abstract-polytopes</a>
</pre>
## Ring theory

<pre class="Agda"><a id="24816" class="Keyword">open</a> <a id="24821" class="Keyword">import</a> <a id="24828" href="ring-theory.html" class="Module">ring-theory</a>
<a id="24840" class="Keyword">open</a> <a id="24845" class="Keyword">import</a> <a id="24852" href="ring-theory.commutative-rings.html" class="Module">ring-theory.commutative-rings</a>
<a id="24882" class="Keyword">open</a> <a id="24887" class="Keyword">import</a> <a id="24894" href="ring-theory.discrete-fields.html" class="Module">ring-theory.discrete-fields</a>
<a id="24922" class="Keyword">open</a> <a id="24927" class="Keyword">import</a> <a id="24934" href="ring-theory.division-rings.html" class="Module">ring-theory.division-rings</a>
<a id="24961" class="Keyword">open</a> <a id="24966" class="Keyword">import</a> <a id="24973" href="ring-theory.eisenstein-integers.html" class="Module">ring-theory.eisenstein-integers</a>
<a id="25005" class="Keyword">open</a> <a id="25010" class="Keyword">import</a> <a id="25017" href="ring-theory.gaussian-integers.html" class="Module">ring-theory.gaussian-integers</a>
<a id="25047" class="Keyword">open</a> <a id="25052" class="Keyword">import</a> <a id="25059" href="ring-theory.homomorphisms-commutative-rings.html" class="Module">ring-theory.homomorphisms-commutative-rings</a>
<a id="25103" class="Keyword">open</a> <a id="25108" class="Keyword">import</a> <a id="25115" href="ring-theory.homomorphisms-rings.html" class="Module">ring-theory.homomorphisms-rings</a>
<a id="25147" class="Keyword">open</a> <a id="25152" class="Keyword">import</a> <a id="25159" href="ring-theory.ideals-generated-by-subsets-rings.html" class="Module">ring-theory.ideals-generated-by-subsets-rings</a>
<a id="25205" class="Keyword">open</a> <a id="25210" class="Keyword">import</a> <a id="25217" href="ring-theory.ideals-rings.html" class="Module">ring-theory.ideals-rings</a>
<a id="25242" class="Keyword">open</a> <a id="25247" class="Keyword">import</a> <a id="25254" href="ring-theory.invertible-elements-rings.html" class="Module">ring-theory.invertible-elements-rings</a>
<a id="25292" class="Keyword">open</a> <a id="25297" class="Keyword">import</a> <a id="25304" href="ring-theory.isomorphisms-commutative-rings.html" class="Module">ring-theory.isomorphisms-commutative-rings</a>
<a id="25347" class="Keyword">open</a> <a id="25352" class="Keyword">import</a> <a id="25359" href="ring-theory.isomorphisms-rings.html" class="Module">ring-theory.isomorphisms-rings</a>
<a id="25390" class="Keyword">open</a> <a id="25395" class="Keyword">import</a> <a id="25402" href="ring-theory.localizations-rings.html" class="Module">ring-theory.localizations-rings</a>
<a id="25434" class="Keyword">open</a> <a id="25439" class="Keyword">import</a> <a id="25446" href="ring-theory.nontrivial-rings.html" class="Module">ring-theory.nontrivial-rings</a>
<a id="25475" class="Keyword">open</a> <a id="25480" class="Keyword">import</a> <a id="25487" href="ring-theory.rings.html" class="Module">ring-theory.rings</a>
</pre>
## Synthetic homotopy theory

<pre class="Agda"><a id="25548" class="Keyword">open</a> <a id="25553" class="Keyword">import</a> <a id="25560" href="synthetic-homotopy-theory.html" class="Module">synthetic-homotopy-theory</a>
<a id="25586" class="Keyword">open</a> <a id="25591" class="Keyword">import</a> <a id="25598" href="synthetic-homotopy-theory.23-pullbacks.html" class="Module">synthetic-homotopy-theory.23-pullbacks</a>
<a id="25637" class="Keyword">open</a> <a id="25642" class="Keyword">import</a> <a id="25649" href="synthetic-homotopy-theory.24-pushouts.html" class="Module">synthetic-homotopy-theory.24-pushouts</a>
<a id="25687" class="Keyword">open</a> <a id="25692" class="Keyword">import</a> <a id="25699" href="synthetic-homotopy-theory.25-cubical-diagrams.html" class="Module">synthetic-homotopy-theory.25-cubical-diagrams</a>
<a id="25745" class="Keyword">open</a> <a id="25750" class="Keyword">import</a> <a id="25757" href="synthetic-homotopy-theory.26-descent.html" class="Module">synthetic-homotopy-theory.26-descent</a>
<a id="25794" class="Keyword">open</a> <a id="25799" class="Keyword">import</a> <a id="25806" href="synthetic-homotopy-theory.26-id-pushout.html" class="Module">synthetic-homotopy-theory.26-id-pushout</a>
<a id="25846" class="Keyword">open</a> <a id="25851" class="Keyword">import</a> <a id="25858" href="synthetic-homotopy-theory.27-sequences.html" class="Module">synthetic-homotopy-theory.27-sequences</a>
<a id="25897" class="Keyword">open</a> <a id="25902" class="Keyword">import</a> <a id="25909" href="synthetic-homotopy-theory.circle.html" class="Module">synthetic-homotopy-theory.circle</a>
<a id="25942" class="Keyword">open</a> <a id="25947" class="Keyword">import</a> <a id="25954" href="synthetic-homotopy-theory.commutative-operations.html" class="Module">synthetic-homotopy-theory.commutative-operations</a>
<a id="26003" class="Keyword">open</a> <a id="26008" class="Keyword">import</a> <a id="26015" href="synthetic-homotopy-theory.cyclic-types.html" class="Module">synthetic-homotopy-theory.cyclic-types</a>
<a id="26054" class="Keyword">open</a> <a id="26059" class="Keyword">import</a> <a id="26066" href="synthetic-homotopy-theory.double-loop-spaces.html" class="Module">synthetic-homotopy-theory.double-loop-spaces</a>
<a id="26111" class="Keyword">open</a> <a id="26116" class="Keyword">import</a> <a id="26123" href="synthetic-homotopy-theory.functoriality-loop-spaces.html" class="Module">synthetic-homotopy-theory.functoriality-loop-spaces</a>
<a id="26175" class="Keyword">open</a> <a id="26180" class="Keyword">import</a> <a id="26187" href="synthetic-homotopy-theory.groups-of-loops-in-1-types.html" class="Module">synthetic-homotopy-theory.groups-of-loops-in-1-types</a>
<a id="26240" class="Keyword">open</a> <a id="26245" class="Keyword">import</a> <a id="26252" href="synthetic-homotopy-theory.infinite-cyclic-types.html" class="Module">synthetic-homotopy-theory.infinite-cyclic-types</a>
<a id="26300" class="Keyword">open</a> <a id="26305" class="Keyword">import</a> <a id="26312" href="synthetic-homotopy-theory.interval-type.html" class="Module">synthetic-homotopy-theory.interval-type</a>
<a id="26352" class="Keyword">open</a> <a id="26357" class="Keyword">import</a> <a id="26364" href="synthetic-homotopy-theory.iterated-loop-spaces.html" class="Module">synthetic-homotopy-theory.iterated-loop-spaces</a>
<a id="26411" class="Keyword">open</a> <a id="26416" class="Keyword">import</a> <a id="26423" href="synthetic-homotopy-theory.loop-spaces.html" class="Module">synthetic-homotopy-theory.loop-spaces</a>
<a id="26461" class="Keyword">open</a> <a id="26466" class="Keyword">import</a> <a id="26473" href="synthetic-homotopy-theory.pointed-dependent-functions.html" class="Module">synthetic-homotopy-theory.pointed-dependent-functions</a>
<a id="26527" class="Keyword">open</a> <a id="26532" class="Keyword">import</a> <a id="26539" href="synthetic-homotopy-theory.pointed-equivalences.html" class="Module">synthetic-homotopy-theory.pointed-equivalences</a>
<a id="26586" class="Keyword">open</a> <a id="26591" class="Keyword">import</a> <a id="26598" href="synthetic-homotopy-theory.pointed-families-of-types.html" class="Module">synthetic-homotopy-theory.pointed-families-of-types</a>
<a id="26650" class="Keyword">open</a> <a id="26655" class="Keyword">import</a> <a id="26662" href="synthetic-homotopy-theory.pointed-homotopies.html" class="Module">synthetic-homotopy-theory.pointed-homotopies</a>
<a id="26707" class="Keyword">open</a> <a id="26712" class="Keyword">import</a> <a id="26719" href="synthetic-homotopy-theory.pointed-maps.html" class="Module">synthetic-homotopy-theory.pointed-maps</a>
<a id="26758" class="Keyword">open</a> <a id="26763" class="Keyword">import</a> <a id="26770" href="synthetic-homotopy-theory.pointed-types.html" class="Module">synthetic-homotopy-theory.pointed-types</a>
<a id="26810" class="Keyword">open</a> <a id="26815" class="Keyword">import</a> <a id="26822" href="synthetic-homotopy-theory.spaces.html" class="Module">synthetic-homotopy-theory.spaces</a>
<a id="26855" class="Keyword">open</a> <a id="26860" class="Keyword">import</a> <a id="26867" href="synthetic-homotopy-theory.triple-loop-spaces.html" class="Module">synthetic-homotopy-theory.triple-loop-spaces</a>
<a id="26912" class="Keyword">open</a> <a id="26917" class="Keyword">import</a> <a id="26924" href="synthetic-homotopy-theory.universal-cover-circle.html" class="Module">synthetic-homotopy-theory.universal-cover-circle</a>
</pre>
## Tutorials

<pre class="Agda"><a id="27000" class="Keyword">open</a> <a id="27005" class="Keyword">import</a> <a id="27012" href="tutorials.basic-agda.html" class="Module">tutorials.basic-agda</a>
</pre>
## Type theories

<pre class="Agda"><a id="27064" class="Keyword">open</a> <a id="27069" class="Keyword">import</a> <a id="27076" href="type-theories.html" class="Module">type-theories</a>
<a id="27090" class="Keyword">open</a> <a id="27095" class="Keyword">import</a> <a id="27102" href="type-theories.comprehension-type-theories.html" class="Module">type-theories.comprehension-type-theories</a>
<a id="27144" class="Keyword">open</a> <a id="27149" class="Keyword">import</a> <a id="27156" href="type-theories.dependent-type-theories.html" class="Module">type-theories.dependent-type-theories</a>
<a id="27194" class="Keyword">open</a> <a id="27199" class="Keyword">import</a> <a id="27206" href="type-theories.fibered-dependent-type-theories.html" class="Module">type-theories.fibered-dependent-type-theories</a>
<a id="27252" class="Keyword">open</a> <a id="27257" class="Keyword">import</a> <a id="27264" href="type-theories.sections-dependent-type-theories.html" class="Module">type-theories.sections-dependent-type-theories</a>
<a id="27311" class="Keyword">open</a> <a id="27316" class="Keyword">import</a> <a id="27323" href="type-theories.simple-type-theories.html" class="Module">type-theories.simple-type-theories</a>
<a id="27358" class="Keyword">open</a> <a id="27363" class="Keyword">import</a> <a id="27370" href="type-theories.unityped-type-theories.html" class="Module">type-theories.unityped-type-theories</a>
</pre>
## Univalent combinatorics

<pre class="Agda"><a id="27448" class="Keyword">open</a> <a id="27453" class="Keyword">import</a> <a id="27460" href="univalent-combinatorics.html" class="Module">univalent-combinatorics</a>
<a id="27484" class="Keyword">open</a> <a id="27489" class="Keyword">import</a> <a id="27496" href="univalent-combinatorics.2-element-decidable-subtypes.html" class="Module">univalent-combinatorics.2-element-decidable-subtypes</a>
<a id="27549" class="Keyword">open</a> <a id="27554" class="Keyword">import</a> <a id="27561" href="univalent-combinatorics.2-element-subtypes.html" class="Module">univalent-combinatorics.2-element-subtypes</a>
<a id="27604" class="Keyword">open</a> <a id="27609" class="Keyword">import</a> <a id="27616" href="univalent-combinatorics.2-element-types.html" class="Module">univalent-combinatorics.2-element-types</a>
<a id="27656" class="Keyword">open</a> <a id="27661" class="Keyword">import</a> <a id="27668" href="univalent-combinatorics.binomial-types.html" class="Module">univalent-combinatorics.binomial-types</a>
<a id="27707" class="Keyword">open</a> <a id="27712" class="Keyword">import</a> <a id="27719" href="univalent-combinatorics.cartesian-product-types.html" class="Module">univalent-combinatorics.cartesian-product-types</a>
<a id="27767" class="Keyword">open</a> <a id="27772" class="Keyword">import</a> <a id="27779" href="univalent-combinatorics.classical-finite-types.html" class="Module">univalent-combinatorics.classical-finite-types</a>
<a id="27826" class="Keyword">open</a> <a id="27831" class="Keyword">import</a> <a id="27838" href="univalent-combinatorics.complements-isolated-points.html" class="Module">univalent-combinatorics.complements-isolated-points</a>
<a id="27890" class="Keyword">open</a> <a id="27895" class="Keyword">import</a> <a id="27902" href="univalent-combinatorics.coproduct-types.html" class="Module">univalent-combinatorics.coproduct-types</a>
<a id="27942" class="Keyword">open</a> <a id="27947" class="Keyword">import</a> <a id="27954" href="univalent-combinatorics.counting-decidable-subtypes.html" class="Module">univalent-combinatorics.counting-decidable-subtypes</a>
<a id="28006" class="Keyword">open</a> <a id="28011" class="Keyword">import</a> <a id="28018" href="univalent-combinatorics.counting-dependent-pair-types.html" class="Module">univalent-combinatorics.counting-dependent-pair-types</a>
<a id="28072" class="Keyword">open</a> <a id="28077" class="Keyword">import</a> <a id="28084" href="univalent-combinatorics.counting-maybe.html" class="Module">univalent-combinatorics.counting-maybe</a>
<a id="28123" class="Keyword">open</a> <a id="28128" class="Keyword">import</a> <a id="28135" href="univalent-combinatorics.counting.html" class="Module">univalent-combinatorics.counting</a>
<a id="28168" class="Keyword">open</a> <a id="28173" class="Keyword">import</a> <a id="28180" href="univalent-combinatorics.cubes.html" class="Module">univalent-combinatorics.cubes</a>
<a id="28210" class="Keyword">open</a> <a id="28215" class="Keyword">import</a> <a id="28222" href="univalent-combinatorics.decidable-dependent-function-types.html" class="Module">univalent-combinatorics.decidable-dependent-function-types</a>
<a id="28281" class="Keyword">open</a> <a id="28286" class="Keyword">import</a> <a id="28293" href="univalent-combinatorics.decidable-dependent-pair-types.html" class="Module">univalent-combinatorics.decidable-dependent-pair-types</a>
<a id="28348" class="Keyword">open</a> <a id="28353" class="Keyword">import</a> <a id="28360" href="univalent-combinatorics.decidable-subtypes.html" class="Module">univalent-combinatorics.decidable-subtypes</a>
<a id="28403" class="Keyword">open</a> <a id="28408" class="Keyword">import</a> <a id="28415" href="univalent-combinatorics.dependent-function-types.html" class="Module">univalent-combinatorics.dependent-function-types</a>
<a id="28464" class="Keyword">open</a> <a id="28469" class="Keyword">import</a> <a id="28476" href="univalent-combinatorics.dedekind-finite-sets.html" class="Module">univalent-combinatorics.dedekind-finite-sets</a>
<a id="28521" class="Keyword">open</a> <a id="28526" class="Keyword">import</a> <a id="28533" href="univalent-combinatorics.dependent-sum-finite-types.html" class="Module">univalent-combinatorics.dependent-sum-finite-types</a>
<a id="28584" class="Keyword">open</a> <a id="28589" class="Keyword">import</a> <a id="28596" href="univalent-combinatorics.distributivity-of-set-truncation-over-finite-products.html" class="Module">univalent-combinatorics.distributivity-of-set-truncation-over-finite-products</a>
<a id="28674" class="Keyword">open</a> <a id="28679" class="Keyword">import</a> <a id="28686" href="univalent-combinatorics.double-counting.html" class="Module">univalent-combinatorics.double-counting</a>
<a id="28726" class="Keyword">open</a> <a id="28731" class="Keyword">import</a> <a id="28738" href="univalent-combinatorics.embeddings-standard-finite-types.html" class="Module">univalent-combinatorics.embeddings-standard-finite-types</a>
<a id="28795" class="Keyword">open</a> <a id="28800" class="Keyword">import</a> <a id="28807" href="univalent-combinatorics.embeddings.html" class="Module">univalent-combinatorics.embeddings</a>
<a id="28842" class="Keyword">open</a> <a id="28847" class="Keyword">import</a> <a id="28854" href="univalent-combinatorics.equality-finite-types.html" class="Module">univalent-combinatorics.equality-finite-types</a>
<a id="28900" class="Keyword">open</a> <a id="28905" class="Keyword">import</a> <a id="28912" href="univalent-combinatorics.equality-standard-finite-types.html" class="Module">univalent-combinatorics.equality-standard-finite-types</a>
<a id="28967" class="Keyword">open</a> <a id="28972" class="Keyword">import</a> <a id="28979" href="univalent-combinatorics.equivalences-cubes.html" class="Module">univalent-combinatorics.equivalences-cubes</a>
<a id="29022" class="Keyword">open</a> <a id="29027" class="Keyword">import</a> <a id="29034" href="univalent-combinatorics.equivalences-standard-finite-types.html" class="Module">univalent-combinatorics.equivalences-standard-finite-types</a>
<a id="29093" class="Keyword">open</a> <a id="29098" class="Keyword">import</a> <a id="29105" href="univalent-combinatorics.equivalences.html" class="Module">univalent-combinatorics.equivalences</a>
<a id="29142" class="Keyword">open</a> <a id="29147" class="Keyword">import</a> <a id="29154" href="univalent-combinatorics.fibers-of-maps.html" class="Module">univalent-combinatorics.fibers-of-maps</a>
<a id="29193" class="Keyword">open</a> <a id="29198" class="Keyword">import</a> <a id="29205" href="univalent-combinatorics.finite-choice.html" class="Module">univalent-combinatorics.finite-choice</a>
<a id="29243" class="Keyword">open</a> <a id="29248" class="Keyword">import</a> <a id="29255" href="univalent-combinatorics.finite-connected-components.html" class="Module">univalent-combinatorics.finite-connected-components</a>
<a id="29307" class="Keyword">open</a> <a id="29312" class="Keyword">import</a> <a id="29319" href="univalent-combinatorics.finite-presentations.html" class="Module">univalent-combinatorics.finite-presentations</a>
<a id="29364" class="Keyword">open</a> <a id="29369" class="Keyword">import</a> <a id="29376" href="univalent-combinatorics.finite-types.html" class="Module">univalent-combinatorics.finite-types</a>
<a id="29413" class="Keyword">open</a> <a id="29418" class="Keyword">import</a> <a id="29425" href="univalent-combinatorics.finitely-presented-types.html" class="Module">univalent-combinatorics.finitely-presented-types</a>
<a id="29474" class="Keyword">open</a> <a id="29479" class="Keyword">import</a> <a id="29486" href="univalent-combinatorics.function-types.html" class="Module">univalent-combinatorics.function-types</a>
<a id="29525" class="Keyword">open</a> <a id="29530" class="Keyword">import</a> <a id="29537" href="univalent-combinatorics.image-of-maps.html" class="Module">univalent-combinatorics.image-of-maps</a>
<a id="29575" class="Keyword">open</a> <a id="29580" class="Keyword">import</a> <a id="29587" href="univalent-combinatorics.inequality-types-with-counting.html" class="Module">univalent-combinatorics.inequality-types-with-counting</a>
<a id="29642" class="Keyword">open</a> <a id="29647" class="Keyword">import</a> <a id="29654" href="univalent-combinatorics.injective-maps.html" class="Module">univalent-combinatorics.injective-maps</a>
<a id="29693" class="Keyword">open</a> <a id="29698" class="Keyword">import</a> <a id="29705" href="univalent-combinatorics.kuratowsky-finite-sets.html" class="Module">univalent-combinatorics.kuratowsky-finite-sets</a>
<a id="29752" class="Keyword">open</a> <a id="29757" class="Keyword">import</a> <a id="29764" href="univalent-combinatorics.lists.html" class="Module">univalent-combinatorics.lists</a>
<a id="29794" class="Keyword">open</a> <a id="29799" class="Keyword">import</a> <a id="29806" href="univalent-combinatorics.maybe.html" class="Module">univalent-combinatorics.maybe</a>
<a id="29836" class="Keyword">open</a> <a id="29841" class="Keyword">import</a> <a id="29848" href="univalent-combinatorics.orientations-cubes.html" class="Module">univalent-combinatorics.orientations-cubes</a>
<a id="29891" class="Keyword">open</a> <a id="29896" class="Keyword">import</a> <a id="29903" href="univalent-combinatorics.petri-nets.html" class="Module">univalent-combinatorics.petri-nets</a>
<a id="29938" class="Keyword">open</a> <a id="29943" class="Keyword">import</a> <a id="29950" href="univalent-combinatorics.pi-finite-types.html" class="Module">univalent-combinatorics.pi-finite-types</a>
<a id="29990" class="Keyword">open</a> <a id="29995" class="Keyword">import</a> <a id="30002" href="univalent-combinatorics.pigeonhole-principle.html" class="Module">univalent-combinatorics.pigeonhole-principle</a>
<a id="30047" class="Keyword">open</a> <a id="30052" class="Keyword">import</a> <a id="30059" href="univalent-combinatorics.presented-pi-finite-types.html" class="Module">univalent-combinatorics.presented-pi-finite-types</a>
<a id="30109" class="Keyword">open</a> <a id="30114" class="Keyword">import</a> <a id="30121" href="univalent-combinatorics.ramsey-theory.html" class="Module">univalent-combinatorics.ramsey-theory</a>
<a id="30159" class="Keyword">open</a> <a id="30164" class="Keyword">import</a> <a id="30171" href="univalent-combinatorics.retracts-of-finite-types.html" class="Module">univalent-combinatorics.retracts-of-finite-types</a>
<a id="30220" class="Keyword">open</a> <a id="30225" class="Keyword">import</a> <a id="30232" href="univalent-combinatorics.skipping-element-standard-finite-types.html" class="Module">univalent-combinatorics.skipping-element-standard-finite-types</a>
<a id="30295" class="Keyword">open</a> <a id="30300" class="Keyword">import</a> <a id="30307" href="univalent-combinatorics.species.html" class="Module">univalent-combinatorics.species</a>
<a id="30339" class="Keyword">open</a> <a id="30344" class="Keyword">import</a> <a id="30351" href="univalent-combinatorics.standard-finite-pruned-trees.html" class="Module">univalent-combinatorics.standard-finite-pruned-trees</a>
<a id="30404" class="Keyword">open</a> <a id="30409" class="Keyword">import</a> <a id="30416" href="univalent-combinatorics.standard-finite-trees.html" class="Module">univalent-combinatorics.standard-finite-trees</a>
<a id="30462" class="Keyword">open</a> <a id="30467" class="Keyword">import</a> <a id="30474" href="univalent-combinatorics.standard-finite-types.html" class="Module">univalent-combinatorics.standard-finite-types</a>
<a id="30520" class="Keyword">open</a> <a id="30525" class="Keyword">import</a> <a id="30532" href="univalent-combinatorics.sums-of-natural-numbers.html" class="Module">univalent-combinatorics.sums-of-natural-numbers</a>
<a id="30580" class="Keyword">open</a> <a id="30585" class="Keyword">import</a> <a id="30592" href="univalent-combinatorics.surjective-maps.html" class="Module">univalent-combinatorics.surjective-maps</a>
</pre>
## Wild algebra

<pre class="Agda"><a id="30662" class="Keyword">open</a> <a id="30667" class="Keyword">import</a> <a id="30674" href="wild-algebra.html" class="Module">wild-algebra</a>
<a id="30687" class="Keyword">open</a> <a id="30692" class="Keyword">import</a> <a id="30699" href="wild-algebra.magmas.html" class="Module">wild-algebra.magmas</a>
<a id="30719" class="Keyword">open</a> <a id="30724" class="Keyword">import</a> <a id="30731" href="wild-algebra.morphisms-magmas.html" class="Module">wild-algebra.morphisms-magmas</a>
<a id="30761" class="Keyword">open</a> <a id="30766" class="Keyword">import</a> <a id="30773" href="wild-algebra.morphisms-wild-unital-magmas.html" class="Module">wild-algebra.morphisms-wild-unital-magmas</a>
<a id="30815" class="Keyword">open</a> <a id="30820" class="Keyword">import</a> <a id="30827" href="wild-algebra.universal-property-lists-wild-monoids.html" class="Module">wild-algebra.universal-property-lists-wild-monoids</a>
<a id="30878" class="Keyword">open</a> <a id="30883" class="Keyword">import</a> <a id="30890" href="wild-algebra.wild-groups.html" class="Module">wild-algebra.wild-groups</a>
<a id="30915" class="Keyword">open</a> <a id="30920" class="Keyword">import</a> <a id="30927" href="wild-algebra.wild-loops.html" class="Module">wild-algebra.wild-loops</a>
<a id="30951" class="Keyword">open</a> <a id="30956" class="Keyword">import</a> <a id="30963" href="wild-algebra.wild-monoids.html" class="Module">wild-algebra.wild-monoids</a>
<a id="30989" class="Keyword">open</a> <a id="30994" class="Keyword">import</a> <a id="31001" href="wild-algebra.wild-quasigroups.html" class="Module">wild-algebra.wild-quasigroups</a>
<a id="31031" class="Keyword">open</a> <a id="31036" class="Keyword">import</a> <a id="31043" href="wild-algebra.wild-semigroups.html" class="Module">wild-algebra.wild-semigroups</a>
<a id="31072" class="Keyword">open</a> <a id="31077" class="Keyword">import</a> <a id="31084" href="wild-algebra.wild-unital-magmas.html" class="Module">wild-algebra.wild-unital-magmas</a>
</pre>
## Everything

See the list of all Agda modules [here](everything.html).

