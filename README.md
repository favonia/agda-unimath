# Univalent mathematics in Agda

Welcome to the website of the `agda-unimath` formalization project.

[![build](https://github.com/UniMath/agda-unimath/actions/workflows/ci.yaml/badge.svg?branch=master)](https://github.com/UniMath/agda-unimath/actions/workflows/ci.yaml)

<pre class="Agda"><a id="281" class="Symbol">{-#</a> <a id="285" class="Keyword">OPTIONS</a> <a id="293" class="Pragma">--without-K</a> <a id="305" class="Pragma">--exact-split</a> <a id="319" class="Symbol">#-}</a>
</pre>
## Category theory

<pre class="Agda"><a id="356" class="Keyword">open</a> <a id="361" class="Keyword">import</a> <a id="368" href="category-theory.html" class="Module">category-theory</a>
<a id="384" class="Keyword">open</a> <a id="389" class="Keyword">import</a> <a id="396" href="category-theory.adjunctions-large-precategories.html" class="Module">category-theory.adjunctions-large-precategories</a>
<a id="444" class="Keyword">open</a> <a id="449" class="Keyword">import</a> <a id="456" href="category-theory.anafunctors.html" class="Module">category-theory.anafunctors</a>
<a id="484" class="Keyword">open</a> <a id="489" class="Keyword">import</a> <a id="496" href="category-theory.categories.html" class="Module">category-theory.categories</a>
<a id="523" class="Keyword">open</a> <a id="528" class="Keyword">import</a> <a id="535" href="category-theory.equivalences-categories.html" class="Module">category-theory.equivalences-categories</a>
<a id="575" class="Keyword">open</a> <a id="580" class="Keyword">import</a> <a id="587" href="category-theory.equivalences-large-precategories.html" class="Module">category-theory.equivalences-large-precategories</a>
<a id="636" class="Keyword">open</a> <a id="641" class="Keyword">import</a> <a id="648" href="category-theory.equivalences-precategories.html" class="Module">category-theory.equivalences-precategories</a>
<a id="691" class="Keyword">open</a> <a id="696" class="Keyword">import</a> <a id="703" href="category-theory.functors-categories.html" class="Module">category-theory.functors-categories</a>
<a id="739" class="Keyword">open</a> <a id="744" class="Keyword">import</a> <a id="751" href="category-theory.functors-large-precategories.html" class="Module">category-theory.functors-large-precategories</a>
<a id="796" class="Keyword">open</a> <a id="801" class="Keyword">import</a> <a id="808" href="category-theory.functors-precategories.html" class="Module">category-theory.functors-precategories</a>
<a id="847" class="Keyword">open</a> <a id="852" class="Keyword">import</a> <a id="859" href="category-theory.homotopies-natural-transformations-large-precategories.html" class="Module">category-theory.homotopies-natural-transformations-large-precategories</a>
<a id="930" class="Keyword">open</a> <a id="935" class="Keyword">import</a> <a id="942" href="category-theory.initial-objects-precategories.html" class="Module">category-theory.initial-objects-precategories</a>
<a id="988" class="Keyword">open</a> <a id="993" class="Keyword">import</a> <a id="1000" href="category-theory.isomorphisms-categories.html" class="Module">category-theory.isomorphisms-categories</a>
<a id="1040" class="Keyword">open</a> <a id="1045" class="Keyword">import</a> <a id="1052" href="category-theory.isomorphisms-large-precategories.html" class="Module">category-theory.isomorphisms-large-precategories</a>
<a id="1101" class="Keyword">open</a> <a id="1106" class="Keyword">import</a> <a id="1113" href="category-theory.isomorphisms-precategories.html" class="Module">category-theory.isomorphisms-precategories</a>
<a id="1156" class="Keyword">open</a> <a id="1161" class="Keyword">import</a> <a id="1168" href="category-theory.large-categories.html" class="Module">category-theory.large-categories</a>
<a id="1201" class="Keyword">open</a> <a id="1206" class="Keyword">import</a> <a id="1213" href="category-theory.large-precategories.html" class="Module">category-theory.large-precategories</a>
<a id="1249" class="Keyword">open</a> <a id="1254" class="Keyword">import</a> <a id="1261" href="category-theory.monomorphisms-large-precategories.html" class="Module">category-theory.monomorphisms-large-precategories</a>
<a id="1311" class="Keyword">open</a> <a id="1316" class="Keyword">import</a> <a id="1323" href="category-theory.natural-isomorphisms-categories.html" class="Module">category-theory.natural-isomorphisms-categories</a>
<a id="1371" class="Keyword">open</a> <a id="1376" class="Keyword">import</a> <a id="1383" href="category-theory.natural-isomorphisms-large-precategories.html" class="Module">category-theory.natural-isomorphisms-large-precategories</a>
<a id="1440" class="Keyword">open</a> <a id="1445" class="Keyword">import</a> <a id="1452" href="category-theory.natural-isomorphisms-precategories.html" class="Module">category-theory.natural-isomorphisms-precategories</a>
<a id="1503" class="Keyword">open</a> <a id="1508" class="Keyword">import</a> <a id="1515" href="category-theory.natural-transformations-categories.html" class="Module">category-theory.natural-transformations-categories</a>
<a id="1566" class="Keyword">open</a> <a id="1571" class="Keyword">import</a> <a id="1578" href="category-theory.natural-transformations-large-precategories.html" class="Module">category-theory.natural-transformations-large-precategories</a>
<a id="1638" class="Keyword">open</a> <a id="1643" class="Keyword">import</a> <a id="1650" href="category-theory.natural-transformations-precategories.html" class="Module">category-theory.natural-transformations-precategories</a>
<a id="1704" class="Keyword">open</a> <a id="1709" class="Keyword">import</a> <a id="1716" href="category-theory.precategories.html" class="Module">category-theory.precategories</a>
<a id="1746" class="Keyword">open</a> <a id="1751" class="Keyword">import</a> <a id="1758" href="category-theory.slice-precategories.html" class="Module">category-theory.slice-precategories</a>
<a id="1794" class="Keyword">open</a> <a id="1799" class="Keyword">import</a> <a id="1806" href="category-theory.terminal-objects-precategories.html" class="Module">category-theory.terminal-objects-precategories</a>
</pre>
## Elementary number theory

<pre class="Agda"><a id="1895" class="Keyword">open</a> <a id="1900" class="Keyword">import</a> <a id="1907" href="elementary-number-theory.html" class="Module">elementary-number-theory</a>
<a id="1932" class="Keyword">open</a> <a id="1937" class="Keyword">import</a> <a id="1944" href="elementary-number-theory.absolute-value-integers.html" class="Module">elementary-number-theory.absolute-value-integers</a>
<a id="1993" class="Keyword">open</a> <a id="1998" class="Keyword">import</a> <a id="2005" href="elementary-number-theory.addition-integers.html" class="Module">elementary-number-theory.addition-integers</a>
<a id="2048" class="Keyword">open</a> <a id="2053" class="Keyword">import</a> <a id="2060" href="elementary-number-theory.addition-natural-numbers.html" class="Module">elementary-number-theory.addition-natural-numbers</a>
<a id="2110" class="Keyword">open</a> <a id="2115" class="Keyword">import</a> <a id="2122" href="elementary-number-theory.arithmetic-functions.html" class="Module">elementary-number-theory.arithmetic-functions</a>
<a id="2168" class="Keyword">open</a> <a id="2173" class="Keyword">import</a> <a id="2180" href="elementary-number-theory.binomial-coefficients.html" class="Module">elementary-number-theory.binomial-coefficients</a>
<a id="2227" class="Keyword">open</a> <a id="2232" class="Keyword">import</a> <a id="2239" href="elementary-number-theory.bounded-sums-arithmetic-functions.html" class="Module">elementary-number-theory.bounded-sums-arithmetic-functions</a>
<a id="2298" class="Keyword">open</a> <a id="2303" class="Keyword">import</a> <a id="2310" href="elementary-number-theory.catalan-numbers.html" class="Module">elementary-number-theory.catalan-numbers</a>
<a id="2351" class="Keyword">open</a> <a id="2356" class="Keyword">import</a> <a id="2363" href="elementary-number-theory.collatz-bijection.html" class="Module">elementary-number-theory.collatz-bijection</a>
<a id="2406" class="Keyword">open</a> <a id="2411" class="Keyword">import</a> <a id="2418" href="elementary-number-theory.collatz-conjecture.html" class="Module">elementary-number-theory.collatz-conjecture</a>
<a id="2462" class="Keyword">open</a> <a id="2467" class="Keyword">import</a> <a id="2474" href="elementary-number-theory.congruence-integers.html" class="Module">elementary-number-theory.congruence-integers</a>
<a id="2519" class="Keyword">open</a> <a id="2524" class="Keyword">import</a> <a id="2531" href="elementary-number-theory.congruence-natural-numbers.html" class="Module">elementary-number-theory.congruence-natural-numbers</a>
<a id="2583" class="Keyword">open</a> <a id="2588" class="Keyword">import</a> <a id="2595" href="elementary-number-theory.decidable-dependent-function-types.html" class="Module">elementary-number-theory.decidable-dependent-function-types</a>
<a id="2655" class="Keyword">open</a> <a id="2660" class="Keyword">import</a> <a id="2667" href="elementary-number-theory.decidable-types.html" class="Module">elementary-number-theory.decidable-types</a>
<a id="2708" class="Keyword">open</a> <a id="2713" class="Keyword">import</a> <a id="2720" href="elementary-number-theory.difference-integers.html" class="Module">elementary-number-theory.difference-integers</a>
<a id="2765" class="Keyword">open</a> <a id="2770" class="Keyword">import</a> <a id="2777" href="elementary-number-theory.dirichlet-convolution.html" class="Module">elementary-number-theory.dirichlet-convolution</a>
<a id="2824" class="Keyword">open</a> <a id="2829" class="Keyword">import</a> <a id="2836" href="elementary-number-theory.distance-integers.html" class="Module">elementary-number-theory.distance-integers</a>
<a id="2879" class="Keyword">open</a> <a id="2884" class="Keyword">import</a> <a id="2891" href="elementary-number-theory.distance-natural-numbers.html" class="Module">elementary-number-theory.distance-natural-numbers</a>
<a id="2941" class="Keyword">open</a> <a id="2946" class="Keyword">import</a> <a id="2953" href="elementary-number-theory.divisibility-integers.html" class="Module">elementary-number-theory.divisibility-integers</a>
<a id="3000" class="Keyword">open</a> <a id="3005" class="Keyword">import</a> <a id="3012" href="elementary-number-theory.divisibility-modular-arithmetic.html" class="Module">elementary-number-theory.divisibility-modular-arithmetic</a>
<a id="3069" class="Keyword">open</a> <a id="3074" class="Keyword">import</a> <a id="3081" href="elementary-number-theory.divisibility-natural-numbers.html" class="Module">elementary-number-theory.divisibility-natural-numbers</a>
<a id="3135" class="Keyword">open</a> <a id="3140" class="Keyword">import</a> <a id="3147" href="elementary-number-theory.divisibility-standard-finite-types.html" class="Module">elementary-number-theory.divisibility-standard-finite-types</a>
<a id="3207" class="Keyword">open</a> <a id="3212" class="Keyword">import</a> <a id="3219" href="elementary-number-theory.equality-integers.html" class="Module">elementary-number-theory.equality-integers</a>
<a id="3262" class="Keyword">open</a> <a id="3267" class="Keyword">import</a> <a id="3274" href="elementary-number-theory.equality-natural-numbers.html" class="Module">elementary-number-theory.equality-natural-numbers</a>
<a id="3324" class="Keyword">open</a> <a id="3329" class="Keyword">import</a> <a id="3336" href="elementary-number-theory.euclidean-division-natural-numbers.html" class="Module">elementary-number-theory.euclidean-division-natural-numbers</a>
<a id="3396" class="Keyword">open</a> <a id="3401" class="Keyword">import</a> <a id="3408" href="elementary-number-theory.eulers-totient-function.html" class="Module">elementary-number-theory.eulers-totient-function</a>
<a id="3457" class="Keyword">open</a> <a id="3462" class="Keyword">import</a> <a id="3469" href="elementary-number-theory.exponentiation-natural-numbers.html" class="Module">elementary-number-theory.exponentiation-natural-numbers</a>
<a id="3525" class="Keyword">open</a> <a id="3530" class="Keyword">import</a> <a id="3537" href="elementary-number-theory.factorials.html" class="Module">elementary-number-theory.factorials</a>
<a id="3573" class="Keyword">open</a> <a id="3578" class="Keyword">import</a> <a id="3585" href="elementary-number-theory.falling-factorials.html" class="Module">elementary-number-theory.falling-factorials</a>
<a id="3629" class="Keyword">open</a> <a id="3634" class="Keyword">import</a> <a id="3641" href="elementary-number-theory.fibonacci-sequence.html" class="Module">elementary-number-theory.fibonacci-sequence</a>
<a id="3685" class="Keyword">open</a> <a id="3690" class="Keyword">import</a> <a id="3697" href="elementary-number-theory.finitary-natural-numbers.html" class="Module">elementary-number-theory.finitary-natural-numbers</a>
<a id="3747" class="Keyword">open</a> <a id="3752" class="Keyword">import</a> <a id="3759" href="elementary-number-theory.finitely-cyclic-maps.html" class="Module">elementary-number-theory.finitely-cyclic-maps</a>
<a id="3805" class="Keyword">open</a> <a id="3810" class="Keyword">import</a> <a id="3817" href="elementary-number-theory.fractions.html" class="Module">elementary-number-theory.fractions</a>
<a id="3852" class="Keyword">open</a> <a id="3857" class="Keyword">import</a> <a id="3864" href="elementary-number-theory.goldbach-conjecture.html" class="Module">elementary-number-theory.goldbach-conjecture</a>
<a id="3909" class="Keyword">open</a> <a id="3914" class="Keyword">import</a> <a id="3921" href="elementary-number-theory.greatest-common-divisor-integers.html" class="Module">elementary-number-theory.greatest-common-divisor-integers</a>
<a id="3979" class="Keyword">open</a> <a id="3984" class="Keyword">import</a> <a id="3991" href="elementary-number-theory.greatest-common-divisor-natural-numbers.html" class="Module">elementary-number-theory.greatest-common-divisor-natural-numbers</a>
<a id="4056" class="Keyword">open</a> <a id="4061" class="Keyword">import</a> <a id="4068" href="elementary-number-theory.group-of-integers.html" class="Module">elementary-number-theory.group-of-integers</a>
<a id="4111" class="Keyword">open</a> <a id="4116" class="Keyword">import</a> <a id="4123" href="elementary-number-theory.groups-of-modular-arithmetic.html" class="Module">elementary-number-theory.groups-of-modular-arithmetic</a>
<a id="4177" class="Keyword">open</a> <a id="4182" class="Keyword">import</a> <a id="4189" href="elementary-number-theory.inequality-integers.html" class="Module">elementary-number-theory.inequality-integers</a>
<a id="4234" class="Keyword">open</a> <a id="4239" class="Keyword">import</a> <a id="4246" href="elementary-number-theory.inequality-natural-numbers.html" class="Module">elementary-number-theory.inequality-natural-numbers</a>
<a id="4298" class="Keyword">open</a> <a id="4303" class="Keyword">import</a> <a id="4310" href="elementary-number-theory.inequality-standard-finite-types.html" class="Module">elementary-number-theory.inequality-standard-finite-types</a>
<a id="4368" class="Keyword">open</a> <a id="4373" class="Keyword">import</a> <a id="4380" href="elementary-number-theory.infinitude-of-primes.html" class="Module">elementary-number-theory.infinitude-of-primes</a>
<a id="4426" class="Keyword">open</a> <a id="4431" class="Keyword">import</a> <a id="4438" href="elementary-number-theory.integers.html" class="Module">elementary-number-theory.integers</a>
<a id="4472" class="Keyword">open</a> <a id="4477" class="Keyword">import</a> <a id="4484" href="elementary-number-theory.iterating-functions.html" class="Module">elementary-number-theory.iterating-functions</a>
<a id="4529" class="Keyword">open</a> <a id="4534" class="Keyword">import</a> <a id="4541" href="elementary-number-theory.lower-bounds-natural-numbers.html" class="Module">elementary-number-theory.lower-bounds-natural-numbers</a>
<a id="4595" class="Keyword">open</a> <a id="4600" class="Keyword">import</a> <a id="4607" href="elementary-number-theory.maximum-natural-numbers.html" class="Module">elementary-number-theory.maximum-natural-numbers</a>
<a id="4656" class="Keyword">open</a> <a id="4661" class="Keyword">import</a> <a id="4668" href="elementary-number-theory.mersenne-primes.html" class="Module">elementary-number-theory.mersenne-primes</a>
<a id="4709" class="Keyword">open</a> <a id="4714" class="Keyword">import</a> <a id="4721" href="elementary-number-theory.minimum-natural-numbers.html" class="Module">elementary-number-theory.minimum-natural-numbers</a>
<a id="4770" class="Keyword">open</a> <a id="4775" class="Keyword">import</a> <a id="4782" href="elementary-number-theory.modular-arithmetic-standard-finite-types.html" class="Module">elementary-number-theory.modular-arithmetic-standard-finite-types</a>
<a id="4848" class="Keyword">open</a> <a id="4853" class="Keyword">import</a> <a id="4860" href="elementary-number-theory.modular-arithmetic.html" class="Module">elementary-number-theory.modular-arithmetic</a>
<a id="4904" class="Keyword">open</a> <a id="4909" class="Keyword">import</a> <a id="4916" href="elementary-number-theory.multiplication-integers.html" class="Module">elementary-number-theory.multiplication-integers</a>
<a id="4965" class="Keyword">open</a> <a id="4970" class="Keyword">import</a> <a id="4977" href="elementary-number-theory.multiplication-natural-numbers.html" class="Module">elementary-number-theory.multiplication-natural-numbers</a>
<a id="5033" class="Keyword">open</a> <a id="5038" class="Keyword">import</a> <a id="5045" href="elementary-number-theory.natural-numbers.html" class="Module">elementary-number-theory.natural-numbers</a>
<a id="5086" class="Keyword">open</a> <a id="5091" class="Keyword">import</a> <a id="5098" href="elementary-number-theory.nonzero-natural-numbers.html" class="Module">elementary-number-theory.nonzero-natural-numbers</a>
<a id="5147" class="Keyword">open</a> <a id="5152" class="Keyword">import</a> <a id="5159" href="elementary-number-theory.ordinal-induction-natural-numbers.html" class="Module">elementary-number-theory.ordinal-induction-natural-numbers</a>
<a id="5218" class="Keyword">open</a> <a id="5223" class="Keyword">import</a> <a id="5230" href="elementary-number-theory.prime-numbers.html" class="Module">elementary-number-theory.prime-numbers</a>
<a id="5269" class="Keyword">open</a> <a id="5274" class="Keyword">import</a> <a id="5281" href="elementary-number-theory.products-of-natural-numbers.html" class="Module">elementary-number-theory.products-of-natural-numbers</a>
<a id="5334" class="Keyword">open</a> <a id="5339" class="Keyword">import</a> <a id="5346" href="elementary-number-theory.proper-divisors-natural-numbers.html" class="Module">elementary-number-theory.proper-divisors-natural-numbers</a>
<a id="5403" class="Keyword">open</a> <a id="5408" class="Keyword">import</a> <a id="5415" href="elementary-number-theory.rational-numbers.html" class="Module">elementary-number-theory.rational-numbers</a>
<a id="5457" class="Keyword">open</a> <a id="5462" class="Keyword">import</a> <a id="5469" href="elementary-number-theory.relatively-prime-integers.html" class="Module">elementary-number-theory.relatively-prime-integers</a>
<a id="5520" class="Keyword">open</a> <a id="5525" class="Keyword">import</a> <a id="5532" href="elementary-number-theory.relatively-prime-natural-numbers.html" class="Module">elementary-number-theory.relatively-prime-natural-numbers</a>
<a id="5590" class="Keyword">open</a> <a id="5595" class="Keyword">import</a> <a id="5602" href="elementary-number-theory.repeating-element-standard-finite-type.html" class="Module">elementary-number-theory.repeating-element-standard-finite-type</a>
<a id="5666" class="Keyword">open</a> <a id="5671" class="Keyword">import</a> <a id="5678" href="elementary-number-theory.retracts-of-natural-numbers.html" class="Module">elementary-number-theory.retracts-of-natural-numbers</a>
<a id="5731" class="Keyword">open</a> <a id="5736" class="Keyword">import</a> <a id="5743" href="elementary-number-theory.square-free-natural-numbers.html" class="Module">elementary-number-theory.square-free-natural-numbers</a>
<a id="5796" class="Keyword">open</a> <a id="5801" class="Keyword">import</a> <a id="5808" href="elementary-number-theory.stirling-numbers-of-the-second-kind.html" class="Module">elementary-number-theory.stirling-numbers-of-the-second-kind</a>
<a id="5869" class="Keyword">open</a> <a id="5874" class="Keyword">import</a> <a id="5881" href="elementary-number-theory.strong-induction-natural-numbers.html" class="Module">elementary-number-theory.strong-induction-natural-numbers</a>
<a id="5939" class="Keyword">open</a> <a id="5944" class="Keyword">import</a> <a id="5951" href="elementary-number-theory.sums-of-natural-numbers.html" class="Module">elementary-number-theory.sums-of-natural-numbers</a>
<a id="6000" class="Keyword">open</a> <a id="6005" class="Keyword">import</a> <a id="6012" href="elementary-number-theory.triangular-numbers.html" class="Module">elementary-number-theory.triangular-numbers</a>
<a id="6056" class="Keyword">open</a> <a id="6061" class="Keyword">import</a> <a id="6068" href="elementary-number-theory.telephone-numbers.html" class="Module">elementary-number-theory.telephone-numbers</a>
<a id="6111" class="Keyword">open</a> <a id="6116" class="Keyword">import</a> <a id="6123" href="elementary-number-theory.twin-prime-conjecture.html" class="Module">elementary-number-theory.twin-prime-conjecture</a>
<a id="6170" class="Keyword">open</a> <a id="6175" class="Keyword">import</a> <a id="6182" href="elementary-number-theory.unit-elements-standard-finite-types.html" class="Module">elementary-number-theory.unit-elements-standard-finite-types</a>
<a id="6243" class="Keyword">open</a> <a id="6248" class="Keyword">import</a> <a id="6255" href="elementary-number-theory.unit-similarity-standard-finite-types.html" class="Module">elementary-number-theory.unit-similarity-standard-finite-types</a>
<a id="6318" class="Keyword">open</a> <a id="6323" class="Keyword">import</a> <a id="6330" href="elementary-number-theory.universal-property-natural-numbers.html" class="Module">elementary-number-theory.universal-property-natural-numbers</a>
<a id="6390" class="Keyword">open</a> <a id="6395" class="Keyword">import</a> <a id="6402" href="elementary-number-theory.upper-bounds-natural-numbers.html" class="Module">elementary-number-theory.upper-bounds-natural-numbers</a>
<a id="6456" class="Keyword">open</a> <a id="6461" class="Keyword">import</a> <a id="6468" href="elementary-number-theory.well-ordering-principle-natural-numbers.html" class="Module">elementary-number-theory.well-ordering-principle-natural-numbers</a>
<a id="6533" class="Keyword">open</a> <a id="6538" class="Keyword">import</a> <a id="6545" href="elementary-number-theory.well-ordering-principle-standard-finite-types.html" class="Module">elementary-number-theory.well-ordering-principle-standard-finite-types</a>
</pre>
## Finite group theory

<pre class="Agda"><a id="6653" class="Keyword">open</a> <a id="6658" class="Keyword">import</a> <a id="6665" href="finite-group-theory.html" class="Module">finite-group-theory</a>
<a id="6685" class="Keyword">open</a> <a id="6690" class="Keyword">import</a> <a id="6697" href="finite-group-theory.abstract-quaternion-group.html" class="Module">finite-group-theory.abstract-quaternion-group</a>
<a id="6743" class="Keyword">open</a> <a id="6748" class="Keyword">import</a> <a id="6755" href="finite-group-theory.concrete-quaternion-group.html" class="Module">finite-group-theory.concrete-quaternion-group</a>
<a id="6801" class="Keyword">open</a> <a id="6806" class="Keyword">import</a> <a id="6813" href="finite-group-theory.finite-groups.html" class="Module">finite-group-theory.finite-groups</a>
<a id="6847" class="Keyword">open</a> <a id="6852" class="Keyword">import</a> <a id="6859" href="finite-group-theory.finite-monoids.html" class="Module">finite-group-theory.finite-monoids</a>
<a id="6894" class="Keyword">open</a> <a id="6899" class="Keyword">import</a> <a id="6906" href="finite-group-theory.finite-semigroups.html" class="Module">finite-group-theory.finite-semigroups</a>
<a id="6944" class="Keyword">open</a> <a id="6949" class="Keyword">import</a> <a id="6956" href="finite-group-theory.groups-of-order-2.html" class="Module">finite-group-theory.groups-of-order-2</a>
<a id="6994" class="Keyword">open</a> <a id="6999" class="Keyword">import</a> <a id="7006" href="finite-group-theory.orbits-permutations.html" class="Module">finite-group-theory.orbits-permutations</a>
<a id="7046" class="Keyword">open</a> <a id="7051" class="Keyword">import</a> <a id="7058" href="finite-group-theory.permutations.html" class="Module">finite-group-theory.permutations</a>
<a id="7091" class="Keyword">open</a> <a id="7096" class="Keyword">import</a> <a id="7103" href="finite-group-theory.sign-homomorphism.html" class="Module">finite-group-theory.sign-homomorphism</a>
<a id="7141" class="Keyword">open</a> <a id="7146" class="Keyword">import</a> <a id="7153" href="finite-group-theory.transpositions.html" class="Module">finite-group-theory.transpositions</a>
</pre>
## Foundation

<pre class="Agda"><a id="7216" class="Keyword">open</a> <a id="7221" class="Keyword">import</a> <a id="7228" href="foundation.html" class="Module">foundation</a>
<a id="7239" class="Keyword">open</a> <a id="7244" class="Keyword">import</a> <a id="7251" href="foundation.0-maps.html" class="Module">foundation.0-maps</a>
<a id="7269" class="Keyword">open</a> <a id="7274" class="Keyword">import</a> <a id="7281" href="foundation.1-types.html" class="Module">foundation.1-types</a>
<a id="7300" class="Keyword">open</a> <a id="7305" class="Keyword">import</a> <a id="7312" href="foundation.2-types.html" class="Module">foundation.2-types</a>
<a id="7331" class="Keyword">open</a> <a id="7336" class="Keyword">import</a> <a id="7343" href="foundation.algebras-polynomial-endofunctors.html" class="Module">foundation.algebras-polynomial-endofunctors</a>
<a id="7387" class="Keyword">open</a> <a id="7392" class="Keyword">import</a> <a id="7399" href="foundation.automorphisms.html" class="Module">foundation.automorphisms</a>
<a id="7424" class="Keyword">open</a> <a id="7429" class="Keyword">import</a> <a id="7436" href="foundation.axiom-of-choice.html" class="Module">foundation.axiom-of-choice</a>
<a id="7463" class="Keyword">open</a> <a id="7468" class="Keyword">import</a> <a id="7475" href="foundation.binary-embeddings.html" class="Module">foundation.binary-embeddings</a>
<a id="7504" class="Keyword">open</a> <a id="7509" class="Keyword">import</a> <a id="7516" href="foundation.binary-equivalences.html" class="Module">foundation.binary-equivalences</a>
<a id="7547" class="Keyword">open</a> <a id="7552" class="Keyword">import</a> <a id="7559" href="foundation.binary-relations.html" class="Module">foundation.binary-relations</a>
<a id="7587" class="Keyword">open</a> <a id="7592" class="Keyword">import</a> <a id="7599" href="foundation.boolean-reflection.html" class="Module">foundation.boolean-reflection</a>
<a id="7629" class="Keyword">open</a> <a id="7634" class="Keyword">import</a> <a id="7641" href="foundation.booleans.html" class="Module">foundation.booleans</a>
<a id="7661" class="Keyword">open</a> <a id="7666" class="Keyword">import</a> <a id="7673" href="foundation.cantors-diagonal-argument.html" class="Module">foundation.cantors-diagonal-argument</a>
<a id="7710" class="Keyword">open</a> <a id="7715" class="Keyword">import</a> <a id="7722" href="foundation.cartesian-product-types.html" class="Module">foundation.cartesian-product-types</a>
<a id="7757" class="Keyword">open</a> <a id="7762" class="Keyword">import</a> <a id="7769" href="foundation.choice-of-representatives-equivalence-relation.html" class="Module">foundation.choice-of-representatives-equivalence-relation</a>
<a id="7827" class="Keyword">open</a> <a id="7832" class="Keyword">import</a> <a id="7839" href="foundation.coherently-invertible-maps.html" class="Module">foundation.coherently-invertible-maps</a>
<a id="7877" class="Keyword">open</a> <a id="7882" class="Keyword">import</a> <a id="7889" href="foundation.commuting-squares.html" class="Module">foundation.commuting-squares</a>
<a id="7918" class="Keyword">open</a> <a id="7923" class="Keyword">import</a> <a id="7930" href="foundation.complements.html" class="Module">foundation.complements</a>
<a id="7953" class="Keyword">open</a> <a id="7958" class="Keyword">import</a> <a id="7965" href="foundation.conjunction.html" class="Module">foundation.conjunction</a>
<a id="7988" class="Keyword">open</a> <a id="7993" class="Keyword">import</a> <a id="8000" href="foundation.connected-components-universes.html" class="Module">foundation.connected-components-universes</a>
<a id="8042" class="Keyword">open</a> <a id="8047" class="Keyword">import</a> <a id="8054" href="foundation.connected-components.html" class="Module">foundation.connected-components</a>
<a id="8086" class="Keyword">open</a> <a id="8091" class="Keyword">import</a> <a id="8098" href="foundation.connected-types.html" class="Module">foundation.connected-types</a>
<a id="8125" class="Keyword">open</a> <a id="8130" class="Keyword">import</a> <a id="8137" href="foundation.constant-maps.html" class="Module">foundation.constant-maps</a>
<a id="8162" class="Keyword">open</a> <a id="8167" class="Keyword">import</a> <a id="8174" href="foundation.contractible-maps.html" class="Module">foundation.contractible-maps</a>
<a id="8203" class="Keyword">open</a> <a id="8208" class="Keyword">import</a> <a id="8215" href="foundation.contractible-types.html" class="Module">foundation.contractible-types</a>
<a id="8245" class="Keyword">open</a> <a id="8250" class="Keyword">import</a> <a id="8257" href="foundation.coproduct-types.html" class="Module">foundation.coproduct-types</a>
<a id="8284" class="Keyword">open</a> <a id="8289" class="Keyword">import</a> <a id="8296" href="foundation.coslice.html" class="Module">foundation.coslice</a>
<a id="8315" class="Keyword">open</a> <a id="8320" class="Keyword">import</a> <a id="8327" href="foundation.decidable-dependent-function-types.html" class="Module">foundation.decidable-dependent-function-types</a>
<a id="8373" class="Keyword">open</a> <a id="8378" class="Keyword">import</a> <a id="8385" href="foundation.decidable-dependent-pair-types.html" class="Module">foundation.decidable-dependent-pair-types</a>
<a id="8427" class="Keyword">open</a> <a id="8432" class="Keyword">import</a> <a id="8439" href="foundation.decidable-embeddings.html" class="Module">foundation.decidable-embeddings</a>
<a id="8471" class="Keyword">open</a> <a id="8476" class="Keyword">import</a> <a id="8483" href="foundation.decidable-equality.html" class="Module">foundation.decidable-equality</a>
<a id="8513" class="Keyword">open</a> <a id="8518" class="Keyword">import</a> <a id="8525" href="foundation.decidable-maps.html" class="Module">foundation.decidable-maps</a>
<a id="8551" class="Keyword">open</a> <a id="8556" class="Keyword">import</a> <a id="8563" href="foundation.decidable-propositions.html" class="Module">foundation.decidable-propositions</a>
<a id="8597" class="Keyword">open</a> <a id="8602" class="Keyword">import</a> <a id="8609" href="foundation.decidable-subtypes.html" class="Module">foundation.decidable-subtypes</a>
<a id="8639" class="Keyword">open</a> <a id="8644" class="Keyword">import</a> <a id="8651" href="foundation.decidable-types.html" class="Module">foundation.decidable-types</a>
<a id="8678" class="Keyword">open</a> <a id="8683" class="Keyword">import</a> <a id="8690" href="foundation.dependent-pair-types.html" class="Module">foundation.dependent-pair-types</a>
<a id="8722" class="Keyword">open</a> <a id="8727" class="Keyword">import</a> <a id="8734" href="foundation.diagonal-maps-of-types.html" class="Module">foundation.diagonal-maps-of-types</a>
<a id="8768" class="Keyword">open</a> <a id="8773" class="Keyword">import</a> <a id="8780" href="foundation.disjunction.html" class="Module">foundation.disjunction</a>
<a id="8803" class="Keyword">open</a> <a id="8808" class="Keyword">import</a> <a id="8815" href="foundation.distributivity-of-dependent-functions-over-coproduct-types.html" class="Module">foundation.distributivity-of-dependent-functions-over-coproduct-types</a>
<a id="8885" class="Keyword">open</a> <a id="8890" class="Keyword">import</a> <a id="8897" href="foundation.distributivity-of-dependent-functions-over-dependent-pairs.html" class="Module">foundation.distributivity-of-dependent-functions-over-dependent-pairs</a>
<a id="8967" class="Keyword">open</a> <a id="8972" class="Keyword">import</a> <a id="8979" href="foundation.double-negation.html" class="Module">foundation.double-negation</a>
<a id="9006" class="Keyword">open</a> <a id="9011" class="Keyword">import</a> <a id="9018" href="foundation.dubuc-penon-compact-types.html" class="Module">foundation.dubuc-penon-compact-types</a>
<a id="9055" class="Keyword">open</a> <a id="9060" class="Keyword">import</a> <a id="9067" href="foundation.effective-maps-equivalence-relations.html" class="Module">foundation.effective-maps-equivalence-relations</a>
<a id="9115" class="Keyword">open</a> <a id="9120" class="Keyword">import</a> <a id="9127" href="foundation.elementhood-relation-w-types.html" class="Module">foundation.elementhood-relation-w-types</a>
<a id="9167" class="Keyword">open</a> <a id="9172" class="Keyword">import</a> <a id="9179" href="foundation.embeddings.html" class="Module">foundation.embeddings</a>
<a id="9201" class="Keyword">open</a> <a id="9206" class="Keyword">import</a> <a id="9213" href="foundation.empty-types.html" class="Module">foundation.empty-types</a>
<a id="9236" class="Keyword">open</a> <a id="9241" class="Keyword">import</a> <a id="9248" href="foundation.epimorphisms-with-respect-to-sets.html" class="Module">foundation.epimorphisms-with-respect-to-sets</a>
<a id="9293" class="Keyword">open</a> <a id="9298" class="Keyword">import</a> <a id="9305" href="foundation.equality-cartesian-product-types.html" class="Module">foundation.equality-cartesian-product-types</a>
<a id="9349" class="Keyword">open</a> <a id="9354" class="Keyword">import</a> <a id="9361" href="foundation.equality-coproduct-types.html" class="Module">foundation.equality-coproduct-types</a>
<a id="9397" class="Keyword">open</a> <a id="9402" class="Keyword">import</a> <a id="9409" href="foundation.equality-dependent-function-types.html" class="Module">foundation.equality-dependent-function-types</a>
<a id="9454" class="Keyword">open</a> <a id="9459" class="Keyword">import</a> <a id="9466" href="foundation.equality-dependent-pair-types.html" class="Module">foundation.equality-dependent-pair-types</a>
<a id="9507" class="Keyword">open</a> <a id="9512" class="Keyword">import</a> <a id="9519" href="foundation.equality-fibers-of-maps.html" class="Module">foundation.equality-fibers-of-maps</a>
<a id="9554" class="Keyword">open</a> <a id="9559" class="Keyword">import</a> <a id="9566" href="foundation.equivalence-classes.html" class="Module">foundation.equivalence-classes</a>
<a id="9597" class="Keyword">open</a> <a id="9602" class="Keyword">import</a> <a id="9609" href="foundation.equivalence-induction.html" class="Module">foundation.equivalence-induction</a>
<a id="9642" class="Keyword">open</a> <a id="9647" class="Keyword">import</a> <a id="9654" href="foundation.equivalence-relations.html" class="Module">foundation.equivalence-relations</a>
<a id="9687" class="Keyword">open</a> <a id="9692" class="Keyword">import</a> <a id="9699" href="foundation.equivalences-maybe.html" class="Module">foundation.equivalences-maybe</a>
<a id="9729" class="Keyword">open</a> <a id="9734" class="Keyword">import</a> <a id="9741" href="foundation.equivalences.html" class="Module">foundation.equivalences</a>
<a id="9765" class="Keyword">open</a> <a id="9770" class="Keyword">import</a> <a id="9777" href="foundation.existential-quantification.html" class="Module">foundation.existential-quantification</a>
<a id="9815" class="Keyword">open</a> <a id="9820" class="Keyword">import</a> <a id="9827" href="foundation.extensional-w-types.html" class="Module">foundation.extensional-w-types</a>
<a id="9858" class="Keyword">open</a> <a id="9863" class="Keyword">import</a> <a id="9870" href="foundation.faithful-maps.html" class="Module">foundation.faithful-maps</a>
<a id="9895" class="Keyword">open</a> <a id="9900" class="Keyword">import</a> <a id="9907" href="foundation.fiber-inclusions.html" class="Module">foundation.fiber-inclusions</a>
<a id="9935" class="Keyword">open</a> <a id="9940" class="Keyword">import</a> <a id="9947" href="foundation.fibered-maps.html" class="Module">foundation.fibered-maps</a>
<a id="9971" class="Keyword">open</a> <a id="9976" class="Keyword">import</a> <a id="9983" href="foundation.fibers-of-maps.html" class="Module">foundation.fibers-of-maps</a>
<a id="10009" class="Keyword">open</a> <a id="10014" class="Keyword">import</a> <a id="10021" href="foundation.function-extensionality.html" class="Module">foundation.function-extensionality</a>
<a id="10056" class="Keyword">open</a> <a id="10061" class="Keyword">import</a> <a id="10068" href="foundation.functions.html" class="Module">foundation.functions</a>
<a id="10089" class="Keyword">open</a> <a id="10094" class="Keyword">import</a> <a id="10101" href="foundation.functoriality-cartesian-product-types.html" class="Module">foundation.functoriality-cartesian-product-types</a>
<a id="10150" class="Keyword">open</a> <a id="10155" class="Keyword">import</a> <a id="10162" href="foundation.functoriality-coproduct-types.html" class="Module">foundation.functoriality-coproduct-types</a>
<a id="10203" class="Keyword">open</a> <a id="10208" class="Keyword">import</a> <a id="10215" href="foundation.functoriality-dependent-function-types.html" class="Module">foundation.functoriality-dependent-function-types</a>
<a id="10265" class="Keyword">open</a> <a id="10270" class="Keyword">import</a> <a id="10277" href="foundation.functoriality-dependent-pair-types.html" class="Module">foundation.functoriality-dependent-pair-types</a>
<a id="10323" class="Keyword">open</a> <a id="10328" class="Keyword">import</a> <a id="10335" href="foundation.functoriality-function-types.html" class="Module">foundation.functoriality-function-types</a>
<a id="10375" class="Keyword">open</a> <a id="10380" class="Keyword">import</a> <a id="10387" href="foundation.functoriality-propositional-truncation.html" class="Module">foundation.functoriality-propositional-truncation</a>
<a id="10437" class="Keyword">open</a> <a id="10442" class="Keyword">import</a> <a id="10449" href="foundation.functoriality-set-quotients.html" class="Module">foundation.functoriality-set-quotients</a>
<a id="10488" class="Keyword">open</a> <a id="10493" class="Keyword">import</a> <a id="10500" href="foundation.functoriality-set-truncation.html" class="Module">foundation.functoriality-set-truncation</a>
<a id="10540" class="Keyword">open</a> <a id="10545" class="Keyword">import</a> <a id="10552" href="foundation.functoriality-w-types.html" class="Module">foundation.functoriality-w-types</a>
<a id="10585" class="Keyword">open</a> <a id="10590" class="Keyword">import</a> <a id="10597" href="foundation.fundamental-theorem-of-identity-types.html" class="Module">foundation.fundamental-theorem-of-identity-types</a>
<a id="10646" class="Keyword">open</a> <a id="10651" class="Keyword">import</a> <a id="10658" href="foundation.global-choice.html" class="Module">foundation.global-choice</a>
<a id="10683" class="Keyword">open</a> <a id="10688" class="Keyword">import</a> <a id="10695" href="foundation.hilberts-epsilon-operators.html" class="Module">foundation.hilberts-epsilon-operators</a>
<a id="10733" class="Keyword">open</a> <a id="10738" class="Keyword">import</a> <a id="10745" href="foundation.homotopies.html" class="Module">foundation.homotopies</a>
<a id="10767" class="Keyword">open</a> <a id="10772" class="Keyword">import</a> <a id="10779" href="foundation.identity-systems.html" class="Module">foundation.identity-systems</a>
<a id="10807" class="Keyword">open</a> <a id="10812" class="Keyword">import</a> <a id="10819" href="foundation.identity-types.html" class="Module">foundation.identity-types</a>
<a id="10845" class="Keyword">open</a> <a id="10850" class="Keyword">import</a> <a id="10857" href="foundation.images.html" class="Module">foundation.images</a>
<a id="10875" class="Keyword">open</a> <a id="10880" class="Keyword">import</a> <a id="10887" href="foundation.impredicative-encodings.html" class="Module">foundation.impredicative-encodings</a>
<a id="10922" class="Keyword">open</a> <a id="10927" class="Keyword">import</a> <a id="10934" href="foundation.indexed-w-types.html" class="Module">foundation.indexed-w-types</a>
<a id="10961" class="Keyword">open</a> <a id="10966" class="Keyword">import</a> <a id="10973" href="foundation.induction-principle-propositional-truncation.html" class="Module">foundation.induction-principle-propositional-truncation</a>
<a id="11029" class="Keyword">open</a> <a id="11034" class="Keyword">import</a> <a id="11041" href="foundation.induction-w-types.html" class="Module">foundation.induction-w-types</a>
<a id="11070" class="Keyword">open</a> <a id="11075" class="Keyword">import</a> <a id="11082" href="foundation.inequality-w-types.html" class="Module">foundation.inequality-w-types</a>
<a id="11112" class="Keyword">open</a> <a id="11117" class="Keyword">import</a> <a id="11124" href="foundation.injective-maps.html" class="Module">foundation.injective-maps</a>
<a id="11150" class="Keyword">open</a> <a id="11155" class="Keyword">import</a> <a id="11162" href="foundation.interchange-law.html" class="Module">foundation.interchange-law</a>
<a id="11189" class="Keyword">open</a> <a id="11194" class="Keyword">import</a> <a id="11201" href="foundation.involutions.html" class="Module">foundation.involutions</a>
<a id="11224" class="Keyword">open</a> <a id="11229" class="Keyword">import</a> <a id="11236" href="foundation.isolated-points.html" class="Module">foundation.isolated-points</a>
<a id="11263" class="Keyword">open</a> <a id="11268" class="Keyword">import</a> <a id="11275" href="foundation.isomorphisms-of-sets.html" class="Module">foundation.isomorphisms-of-sets</a>
<a id="11307" class="Keyword">open</a> <a id="11312" class="Keyword">import</a> <a id="11319" href="foundation.law-of-excluded-middle.html" class="Module">foundation.law-of-excluded-middle</a>
<a id="11353" class="Keyword">open</a> <a id="11358" class="Keyword">import</a> <a id="11365" href="foundation.lawveres-fixed-point-theorem.html" class="Module">foundation.lawveres-fixed-point-theorem</a>
<a id="11405" class="Keyword">open</a> <a id="11410" class="Keyword">import</a> <a id="11417" href="foundation.locally-small-types.html" class="Module">foundation.locally-small-types</a>
<a id="11448" class="Keyword">open</a> <a id="11453" class="Keyword">import</a> <a id="11460" href="foundation.logical-equivalences.html" class="Module">foundation.logical-equivalences</a>
<a id="11492" class="Keyword">open</a> <a id="11497" class="Keyword">import</a> <a id="11504" href="foundation.lower-types-w-types.html" class="Module">foundation.lower-types-w-types</a>
<a id="11535" class="Keyword">open</a> <a id="11540" class="Keyword">import</a> <a id="11547" href="foundation.maybe.html" class="Module">foundation.maybe</a>
<a id="11564" class="Keyword">open</a> <a id="11569" class="Keyword">import</a> <a id="11576" href="foundation.mere-equality.html" class="Module">foundation.mere-equality</a>
<a id="11601" class="Keyword">open</a> <a id="11606" class="Keyword">import</a> <a id="11613" href="foundation.mere-equivalences.html" class="Module">foundation.mere-equivalences</a>
<a id="11642" class="Keyword">open</a> <a id="11647" class="Keyword">import</a> <a id="11654" href="foundation.monomorphisms.html" class="Module">foundation.monomorphisms</a>
<a id="11679" class="Keyword">open</a> <a id="11684" class="Keyword">import</a> <a id="11691" href="foundation.multisets.html" class="Module">foundation.multisets</a>
<a id="11712" class="Keyword">open</a> <a id="11717" class="Keyword">import</a> <a id="11724" href="foundation.negation.html" class="Module">foundation.negation</a>
<a id="11744" class="Keyword">open</a> <a id="11749" class="Keyword">import</a> <a id="11756" href="foundation.non-contractible-types.html" class="Module">foundation.non-contractible-types</a>
<a id="11790" class="Keyword">open</a> <a id="11795" class="Keyword">import</a> <a id="11802" href="foundation.path-algebra.html" class="Module">foundation.path-algebra</a>
<a id="11826" class="Keyword">open</a> <a id="11831" class="Keyword">import</a> <a id="11838" href="foundation.path-split-maps.html" class="Module">foundation.path-split-maps</a>
<a id="11865" class="Keyword">open</a> <a id="11870" class="Keyword">import</a> <a id="11877" href="foundation.polynomial-endofunctors.html" class="Module">foundation.polynomial-endofunctors</a>
<a id="11912" class="Keyword">open</a> <a id="11917" class="Keyword">import</a> <a id="11924" href="foundation.principle-of-omniscience.html" class="Module">foundation.principle-of-omniscience</a>
<a id="11960" class="Keyword">open</a> <a id="11965" class="Keyword">import</a> <a id="11972" href="foundation.propositional-extensionality.html" class="Module">foundation.propositional-extensionality</a>
<a id="12012" class="Keyword">open</a> <a id="12017" class="Keyword">import</a> <a id="12024" href="foundation.propositional-maps.html" class="Module">foundation.propositional-maps</a>
<a id="12054" class="Keyword">open</a> <a id="12059" class="Keyword">import</a> <a id="12066" href="foundation.propositional-truncations.html" class="Module">foundation.propositional-truncations</a>
<a id="12103" class="Keyword">open</a> <a id="12108" class="Keyword">import</a> <a id="12115" href="foundation.propositions.html" class="Module">foundation.propositions</a>
<a id="12139" class="Keyword">open</a> <a id="12144" class="Keyword">import</a> <a id="12151" href="foundation.pullbacks.html" class="Module">foundation.pullbacks</a>
<a id="12172" class="Keyword">open</a> <a id="12177" class="Keyword">import</a> <a id="12184" href="foundation.raising-universe-levels.html" class="Module">foundation.raising-universe-levels</a>
<a id="12219" class="Keyword">open</a> <a id="12224" class="Keyword">import</a> <a id="12231" href="foundation.ranks-of-elements-w-types.html" class="Module">foundation.ranks-of-elements-w-types</a>
<a id="12268" class="Keyword">open</a> <a id="12273" class="Keyword">import</a> <a id="12280" href="foundation.reflecting-maps-equivalence-relations.html" class="Module">foundation.reflecting-maps-equivalence-relations</a>
<a id="12329" class="Keyword">open</a> <a id="12334" class="Keyword">import</a> <a id="12341" href="foundation.replacement.html" class="Module">foundation.replacement</a>
<a id="12364" class="Keyword">open</a> <a id="12369" class="Keyword">import</a> <a id="12376" href="foundation.retractions.html" class="Module">foundation.retractions</a>
<a id="12399" class="Keyword">open</a> <a id="12404" class="Keyword">import</a> <a id="12411" href="foundation.russells-paradox.html" class="Module">foundation.russells-paradox</a>
<a id="12439" class="Keyword">open</a> <a id="12444" class="Keyword">import</a> <a id="12451" href="foundation.sections.html" class="Module">foundation.sections</a>
<a id="12471" class="Keyword">open</a> <a id="12476" class="Keyword">import</a> <a id="12483" href="foundation.set-presented-types.html" class="Module">foundation.set-presented-types</a>
<a id="12514" class="Keyword">open</a> <a id="12519" class="Keyword">import</a> <a id="12526" href="foundation.set-truncations.html" class="Module">foundation.set-truncations</a>
<a id="12553" class="Keyword">open</a> <a id="12558" class="Keyword">import</a> <a id="12565" href="foundation.sets.html" class="Module">foundation.sets</a>
<a id="12581" class="Keyword">open</a> <a id="12586" class="Keyword">import</a> <a id="12593" href="foundation.singleton-induction.html" class="Module">foundation.singleton-induction</a>
<a id="12624" class="Keyword">open</a> <a id="12629" class="Keyword">import</a> <a id="12636" href="foundation.slice.html" class="Module">foundation.slice</a>
<a id="12653" class="Keyword">open</a> <a id="12658" class="Keyword">import</a> <a id="12665" href="foundation.small-maps.html" class="Module">foundation.small-maps</a>
<a id="12687" class="Keyword">open</a> <a id="12692" class="Keyword">import</a> <a id="12699" href="foundation.small-multisets.html" class="Module">foundation.small-multisets</a>
<a id="12726" class="Keyword">open</a> <a id="12731" class="Keyword">import</a> <a id="12738" href="foundation.small-types.html" class="Module">foundation.small-types</a>
<a id="12761" class="Keyword">open</a> <a id="12766" class="Keyword">import</a> <a id="12773" href="foundation.small-universes.html" class="Module">foundation.small-universes</a>
<a id="12800" class="Keyword">open</a> <a id="12805" class="Keyword">import</a> <a id="12812" href="foundation.split-surjective-maps.html" class="Module">foundation.split-surjective-maps</a>
<a id="12845" class="Keyword">open</a> <a id="12850" class="Keyword">import</a> <a id="12857" href="foundation.structure-identity-principle.html" class="Module">foundation.structure-identity-principle</a>
<a id="12897" class="Keyword">open</a> <a id="12902" class="Keyword">import</a> <a id="12909" href="foundation.structure.html" class="Module">foundation.structure</a>
<a id="12930" class="Keyword">open</a> <a id="12935" class="Keyword">import</a> <a id="12942" href="foundation.subterminal-types.html" class="Module">foundation.subterminal-types</a>
<a id="12971" class="Keyword">open</a> <a id="12976" class="Keyword">import</a> <a id="12983" href="foundation.subtype-identity-principle.html" class="Module">foundation.subtype-identity-principle</a>
<a id="13021" class="Keyword">open</a> <a id="13026" class="Keyword">import</a> <a id="13033" href="foundation.subtypes.html" class="Module">foundation.subtypes</a>
<a id="13053" class="Keyword">open</a> <a id="13058" class="Keyword">import</a> <a id="13065" href="foundation.subuniverses.html" class="Module">foundation.subuniverses</a>
<a id="13089" class="Keyword">open</a> <a id="13094" class="Keyword">import</a> <a id="13101" href="foundation.surjective-maps.html" class="Module">foundation.surjective-maps</a>
<a id="13128" class="Keyword">open</a> <a id="13133" class="Keyword">import</a> <a id="13140" href="foundation.truncated-equality.html" class="Module">foundation.truncated-equality</a>
<a id="13170" class="Keyword">open</a> <a id="13175" class="Keyword">import</a> <a id="13182" href="foundation.truncated-maps.html" class="Module">foundation.truncated-maps</a>
<a id="13208" class="Keyword">open</a> <a id="13213" class="Keyword">import</a> <a id="13220" href="foundation.truncated-types.html" class="Module">foundation.truncated-types</a>
<a id="13247" class="Keyword">open</a> <a id="13252" class="Keyword">import</a> <a id="13259" href="foundation.truncation-levels.html" class="Module">foundation.truncation-levels</a>
<a id="13288" class="Keyword">open</a> <a id="13293" class="Keyword">import</a> <a id="13300" href="foundation.truncations.html" class="Module">foundation.truncations</a>
<a id="13323" class="Keyword">open</a> <a id="13328" class="Keyword">import</a> <a id="13335" href="foundation.type-arithmetic-cartesian-product-types.html" class="Module">foundation.type-arithmetic-cartesian-product-types</a>
<a id="13386" class="Keyword">open</a> <a id="13391" class="Keyword">import</a> <a id="13398" href="foundation.type-arithmetic-coproduct-types.html" class="Module">foundation.type-arithmetic-coproduct-types</a>
<a id="13441" class="Keyword">open</a> <a id="13446" class="Keyword">import</a> <a id="13453" href="foundation.type-arithmetic-dependent-pair-types.html" class="Module">foundation.type-arithmetic-dependent-pair-types</a>
<a id="13501" class="Keyword">open</a> <a id="13506" class="Keyword">import</a> <a id="13513" href="foundation.type-arithmetic-empty-type.html" class="Module">foundation.type-arithmetic-empty-type</a>
<a id="13551" class="Keyword">open</a> <a id="13556" class="Keyword">import</a> <a id="13563" href="foundation.type-arithmetic-unit-type.html" class="Module">foundation.type-arithmetic-unit-type</a>
<a id="13600" class="Keyword">open</a> <a id="13605" class="Keyword">import</a> <a id="13612" href="foundation.uniqueness-image.html" class="Module">foundation.uniqueness-image</a>
<a id="13640" class="Keyword">open</a> <a id="13645" class="Keyword">import</a> <a id="13652" href="foundation.uniqueness-set-quotients.html" class="Module">foundation.uniqueness-set-quotients</a>
<a id="13688" class="Keyword">open</a> <a id="13693" class="Keyword">import</a> <a id="13700" href="foundation.uniqueness-set-truncations.html" class="Module">foundation.uniqueness-set-truncations</a>
<a id="13738" class="Keyword">open</a> <a id="13743" class="Keyword">import</a> <a id="13750" href="foundation.uniqueness-truncation.html" class="Module">foundation.uniqueness-truncation</a>
<a id="13783" class="Keyword">open</a> <a id="13788" class="Keyword">import</a> <a id="13795" href="foundation.unit-type.html" class="Module">foundation.unit-type</a>
<a id="13816" class="Keyword">open</a> <a id="13821" class="Keyword">import</a> <a id="13828" href="foundation.univalence-implies-function-extensionality.html" class="Module">foundation.univalence-implies-function-extensionality</a>
<a id="13882" class="Keyword">open</a> <a id="13887" class="Keyword">import</a> <a id="13894" href="foundation.univalence.html" class="Module">foundation.univalence</a>
<a id="13916" class="Keyword">open</a> <a id="13921" class="Keyword">import</a> <a id="13928" href="foundation.univalent-type-families.html" class="Module">foundation.univalent-type-families</a>
<a id="13963" class="Keyword">open</a> <a id="13968" class="Keyword">import</a> <a id="13975" href="foundation.universal-multiset.html" class="Module">foundation.universal-multiset</a>
<a id="14005" class="Keyword">open</a> <a id="14010" class="Keyword">import</a> <a id="14017" href="foundation.universal-property-booleans.html" class="Module">foundation.universal-property-booleans</a>
<a id="14056" class="Keyword">open</a> <a id="14061" class="Keyword">import</a> <a id="14068" href="foundation.universal-property-cartesian-product-types.html" class="Module">foundation.universal-property-cartesian-product-types</a>
<a id="14122" class="Keyword">open</a> <a id="14127" class="Keyword">import</a> <a id="14134" href="foundation.universal-property-coproduct-types.html" class="Module">foundation.universal-property-coproduct-types</a>
<a id="14180" class="Keyword">open</a> <a id="14185" class="Keyword">import</a> <a id="14192" href="foundation.universal-property-dependent-pair-types.html" class="Module">foundation.universal-property-dependent-pair-types</a>
<a id="14243" class="Keyword">open</a> <a id="14248" class="Keyword">import</a> <a id="14255" href="foundation.universal-property-empty-type.html" class="Module">foundation.universal-property-empty-type</a>
<a id="14296" class="Keyword">open</a> <a id="14301" class="Keyword">import</a> <a id="14308" href="foundation.universal-property-fiber-products.html" class="Module">foundation.universal-property-fiber-products</a>
<a id="14353" class="Keyword">open</a> <a id="14358" class="Keyword">import</a> <a id="14365" href="foundation.universal-property-identity-types.html" class="Module">foundation.universal-property-identity-types</a>
<a id="14410" class="Keyword">open</a> <a id="14415" class="Keyword">import</a> <a id="14422" href="foundation.universal-property-image.html" class="Module">foundation.universal-property-image</a>
<a id="14458" class="Keyword">open</a> <a id="14463" class="Keyword">import</a> <a id="14470" href="foundation.universal-property-maybe.html" class="Module">foundation.universal-property-maybe</a>
<a id="14506" class="Keyword">open</a> <a id="14511" class="Keyword">import</a> <a id="14518" href="foundation.universal-property-propositional-truncation-into-sets.html" class="Module">foundation.universal-property-propositional-truncation-into-sets</a>
<a id="14583" class="Keyword">open</a> <a id="14588" class="Keyword">import</a> <a id="14595" href="foundation.universal-property-propositional-truncation.html" class="Module">foundation.universal-property-propositional-truncation</a>
<a id="14650" class="Keyword">open</a> <a id="14655" class="Keyword">import</a> <a id="14662" href="foundation.universal-property-pullbacks.html" class="Module">foundation.universal-property-pullbacks</a>
<a id="14702" class="Keyword">open</a> <a id="14707" class="Keyword">import</a> <a id="14714" href="foundation.universal-property-set-quotients.html" class="Module">foundation.universal-property-set-quotients</a>
<a id="14758" class="Keyword">open</a> <a id="14763" class="Keyword">import</a> <a id="14770" href="foundation.universal-property-set-truncation.html" class="Module">foundation.universal-property-set-truncation</a>
<a id="14815" class="Keyword">open</a> <a id="14820" class="Keyword">import</a> <a id="14827" href="foundation.universal-property-truncation.html" class="Module">foundation.universal-property-truncation</a>
<a id="14868" class="Keyword">open</a> <a id="14873" class="Keyword">import</a> <a id="14880" href="foundation.universal-property-unit-type.html" class="Module">foundation.universal-property-unit-type</a>
<a id="14920" class="Keyword">open</a> <a id="14925" class="Keyword">import</a> <a id="14932" href="foundation.universe-levels.html" class="Module">foundation.universe-levels</a>
<a id="14959" class="Keyword">open</a> <a id="14964" class="Keyword">import</a> <a id="14971" href="foundation.unordered-pairs.html" class="Module">foundation.unordered-pairs</a>
<a id="14998" class="Keyword">open</a> <a id="15003" class="Keyword">import</a> <a id="15010" href="foundation.w-types.html" class="Module">foundation.w-types</a>
<a id="15029" class="Keyword">open</a> <a id="15034" class="Keyword">import</a> <a id="15041" href="foundation.weak-function-extensionality.html" class="Module">foundation.weak-function-extensionality</a>
<a id="15081" class="Keyword">open</a> <a id="15086" class="Keyword">import</a> <a id="15093" href="foundation.weakly-constant-maps.html" class="Module">foundation.weakly-constant-maps</a>
</pre>
## Foundation Core

<pre class="Agda"><a id="15158" class="Keyword">open</a> <a id="15163" class="Keyword">import</a> <a id="15170" href="foundation-core.0-maps.html" class="Module">foundation-core.0-maps</a>
<a id="15193" class="Keyword">open</a> <a id="15198" class="Keyword">import</a> <a id="15205" href="foundation-core.1-types.html" class="Module">foundation-core.1-types</a>
<a id="15229" class="Keyword">open</a> <a id="15234" class="Keyword">import</a> <a id="15241" href="foundation-core.cartesian-product-types.html" class="Module">foundation-core.cartesian-product-types</a>
<a id="15281" class="Keyword">open</a> <a id="15286" class="Keyword">import</a> <a id="15293" href="foundation-core.coherently-invertible-maps.html" class="Module">foundation-core.coherently-invertible-maps</a>
<a id="15336" class="Keyword">open</a> <a id="15341" class="Keyword">import</a> <a id="15348" href="foundation-core.commuting-squares.html" class="Module">foundation-core.commuting-squares</a>
<a id="15382" class="Keyword">open</a> <a id="15387" class="Keyword">import</a> <a id="15394" href="foundation-core.constant-maps.html" class="Module">foundation-core.constant-maps</a>
<a id="15424" class="Keyword">open</a> <a id="15429" class="Keyword">import</a> <a id="15436" href="foundation-core.contractible-maps.html" class="Module">foundation-core.contractible-maps</a>
<a id="15470" class="Keyword">open</a> <a id="15475" class="Keyword">import</a> <a id="15482" href="foundation-core.contractible-types.html" class="Module">foundation-core.contractible-types</a>
<a id="15517" class="Keyword">open</a> <a id="15522" class="Keyword">import</a> <a id="15529" href="foundation-core.dependent-pair-types.html" class="Module">foundation-core.dependent-pair-types</a>
<a id="15566" class="Keyword">open</a> <a id="15571" class="Keyword">import</a> <a id="15578" href="foundation-core.embeddings.html" class="Module">foundation-core.embeddings</a>
<a id="15605" class="Keyword">open</a> <a id="15610" class="Keyword">import</a> <a id="15617" href="foundation-core.empty-types.html" class="Module">foundation-core.empty-types</a>
<a id="15645" class="Keyword">open</a> <a id="15650" class="Keyword">import</a> <a id="15657" href="foundation-core.equality-cartesian-product-types.html" class="Module">foundation-core.equality-cartesian-product-types</a>
<a id="15706" class="Keyword">open</a> <a id="15711" class="Keyword">import</a> <a id="15718" href="foundation-core.equality-dependent-pair-types.html" class="Module">foundation-core.equality-dependent-pair-types</a>
<a id="15764" class="Keyword">open</a> <a id="15769" class="Keyword">import</a> <a id="15776" href="foundation-core.equality-fibers-of-maps.html" class="Module">foundation-core.equality-fibers-of-maps</a>
<a id="15816" class="Keyword">open</a> <a id="15821" class="Keyword">import</a> <a id="15828" href="foundation-core.equivalence-induction.html" class="Module">foundation-core.equivalence-induction</a>
<a id="15866" class="Keyword">open</a> <a id="15871" class="Keyword">import</a> <a id="15878" href="foundation-core.equivalences.html" class="Module">foundation-core.equivalences</a>
<a id="15907" class="Keyword">open</a> <a id="15912" class="Keyword">import</a> <a id="15919" href="foundation-core.faithful-maps.html" class="Module">foundation-core.faithful-maps</a>
<a id="15949" class="Keyword">open</a> <a id="15954" class="Keyword">import</a> <a id="15961" href="foundation-core.fibers-of-maps.html" class="Module">foundation-core.fibers-of-maps</a>
<a id="15992" class="Keyword">open</a> <a id="15997" class="Keyword">import</a> <a id="16004" href="foundation-core.functions.html" class="Module">foundation-core.functions</a>
<a id="16030" class="Keyword">open</a> <a id="16035" class="Keyword">import</a> <a id="16042" href="foundation-core.functoriality-dependent-pair-types.html" class="Module">foundation-core.functoriality-dependent-pair-types</a>
<a id="16093" class="Keyword">open</a> <a id="16098" class="Keyword">import</a> <a id="16105" href="foundation-core.fundamental-theorem-of-identity-types.html" class="Module">foundation-core.fundamental-theorem-of-identity-types</a>
<a id="16159" class="Keyword">open</a> <a id="16164" class="Keyword">import</a> <a id="16171" href="foundation-core.homotopies.html" class="Module">foundation-core.homotopies</a>
<a id="16198" class="Keyword">open</a> <a id="16203" class="Keyword">import</a> <a id="16210" href="foundation-core.identity-systems.html" class="Module">foundation-core.identity-systems</a>
<a id="16243" class="Keyword">open</a> <a id="16248" class="Keyword">import</a> <a id="16255" href="foundation-core.identity-types.html" class="Module">foundation-core.identity-types</a>
<a id="16286" class="Keyword">open</a> <a id="16291" class="Keyword">import</a> <a id="16298" href="foundation-core.logical-equivalences.html" class="Module">foundation-core.logical-equivalences</a>
<a id="16335" class="Keyword">open</a> <a id="16340" class="Keyword">import</a> <a id="16347" href="foundation-core.negation.html" class="Module">foundation-core.negation</a>
<a id="16372" class="Keyword">open</a> <a id="16377" class="Keyword">import</a> <a id="16384" href="foundation-core.path-split-maps.html" class="Module">foundation-core.path-split-maps</a>
<a id="16416" class="Keyword">open</a> <a id="16421" class="Keyword">import</a> <a id="16428" href="foundation-core.propositional-maps.html" class="Module">foundation-core.propositional-maps</a>
<a id="16463" class="Keyword">open</a> <a id="16468" class="Keyword">import</a> <a id="16475" href="foundation-core.propositions.html" class="Module">foundation-core.propositions</a>
<a id="16504" class="Keyword">open</a> <a id="16509" class="Keyword">import</a> <a id="16516" href="foundation-core.retractions.html" class="Module">foundation-core.retractions</a>
<a id="16544" class="Keyword">open</a> <a id="16549" class="Keyword">import</a> <a id="16556" href="foundation-core.sections.html" class="Module">foundation-core.sections</a>
<a id="16581" class="Keyword">open</a> <a id="16586" class="Keyword">import</a> <a id="16593" href="foundation-core.sets.html" class="Module">foundation-core.sets</a>
<a id="16614" class="Keyword">open</a> <a id="16619" class="Keyword">import</a> <a id="16626" href="foundation-core.singleton-induction.html" class="Module">foundation-core.singleton-induction</a>
<a id="16662" class="Keyword">open</a> <a id="16667" class="Keyword">import</a> <a id="16674" href="foundation-core.subtype-identity-principle.html" class="Module">foundation-core.subtype-identity-principle</a>
<a id="16717" class="Keyword">open</a> <a id="16722" class="Keyword">import</a> <a id="16729" href="foundation-core.subtypes.html" class="Module">foundation-core.subtypes</a>
<a id="16754" class="Keyword">open</a> <a id="16759" class="Keyword">import</a> <a id="16766" href="foundation-core.truncated-maps.html" class="Module">foundation-core.truncated-maps</a>
<a id="16797" class="Keyword">open</a> <a id="16802" class="Keyword">import</a> <a id="16809" href="foundation-core.truncated-types.html" class="Module">foundation-core.truncated-types</a>
<a id="16841" class="Keyword">open</a> <a id="16846" class="Keyword">import</a> <a id="16853" href="foundation-core.truncation-levels.html" class="Module">foundation-core.truncation-levels</a>
<a id="16887" class="Keyword">open</a> <a id="16892" class="Keyword">import</a> <a id="16899" href="foundation-core.type-arithmetic-cartesian-product-types.html" class="Module">foundation-core.type-arithmetic-cartesian-product-types</a>
<a id="16955" class="Keyword">open</a> <a id="16960" class="Keyword">import</a> <a id="16967" href="foundation-core.type-arithmetic-dependent-pair-types.html" class="Module">foundation-core.type-arithmetic-dependent-pair-types</a>
<a id="17020" class="Keyword">open</a> <a id="17025" class="Keyword">import</a> <a id="17032" href="foundation-core.univalence.html" class="Module">foundation-core.univalence</a>
<a id="17059" class="Keyword">open</a> <a id="17064" class="Keyword">import</a> <a id="17071" href="foundation-core.universe-levels.html" class="Module">foundation-core.universe-levels</a>
</pre>
## Graph theory

<pre class="Agda"><a id="17133" class="Keyword">open</a> <a id="17138" class="Keyword">import</a> <a id="17145" href="graph-theory.html" class="Module">graph-theory</a>
<a id="17158" class="Keyword">open</a> <a id="17163" class="Keyword">import</a> <a id="17170" href="graph-theory.connected-undirected-graphs.html" class="Module">graph-theory.connected-undirected-graphs</a>
<a id="17211" class="Keyword">open</a> <a id="17216" class="Keyword">import</a> <a id="17223" href="graph-theory.directed-graphs.html" class="Module">graph-theory.directed-graphs</a>
<a id="17252" class="Keyword">open</a> <a id="17257" class="Keyword">import</a> <a id="17264" href="graph-theory.edge-coloured-undirected-graphs.html" class="Module">graph-theory.edge-coloured-undirected-graphs</a>
<a id="17309" class="Keyword">open</a> <a id="17314" class="Keyword">import</a> <a id="17321" href="graph-theory.equivalences-undirected-graphs.html" class="Module">graph-theory.equivalences-undirected-graphs</a>
<a id="17365" class="Keyword">open</a> <a id="17370" class="Keyword">import</a> <a id="17377" href="graph-theory.finite-graphs.html" class="Module">graph-theory.finite-graphs</a>
<a id="17404" class="Keyword">open</a> <a id="17409" class="Keyword">import</a> <a id="17416" href="graph-theory.incidence-undirected-graphs.html" class="Module">graph-theory.incidence-undirected-graphs</a>
<a id="17457" class="Keyword">open</a> <a id="17462" class="Keyword">import</a> <a id="17469" href="graph-theory.matchings.html" class="Module">graph-theory.matchings</a>
<a id="17492" class="Keyword">open</a> <a id="17497" class="Keyword">import</a> <a id="17504" href="graph-theory.mere-equivalences-undirected-graphs.html" class="Module">graph-theory.mere-equivalences-undirected-graphs</a>
<a id="17553" class="Keyword">open</a> <a id="17558" class="Keyword">import</a> <a id="17565" href="graph-theory.morphisms-directed-graphs.html" class="Module">graph-theory.morphisms-directed-graphs</a>
<a id="17604" class="Keyword">open</a> <a id="17609" class="Keyword">import</a> <a id="17616" href="graph-theory.morphisms-undirected-graphs.html" class="Module">graph-theory.morphisms-undirected-graphs</a>
<a id="17657" class="Keyword">open</a> <a id="17662" class="Keyword">import</a> <a id="17669" href="graph-theory.orientations-undirected-graphs.html" class="Module">graph-theory.orientations-undirected-graphs</a>
<a id="17713" class="Keyword">open</a> <a id="17718" class="Keyword">import</a> <a id="17725" href="graph-theory.paths-undirected-graphs.html" class="Module">graph-theory.paths-undirected-graphs</a>
<a id="17762" class="Keyword">open</a> <a id="17767" class="Keyword">import</a> <a id="17774" href="graph-theory.polygons.html" class="Module">graph-theory.polygons</a>
<a id="17796" class="Keyword">open</a> <a id="17801" class="Keyword">import</a> <a id="17808" href="graph-theory.reflexive-graphs.html" class="Module">graph-theory.reflexive-graphs</a>
<a id="17838" class="Keyword">open</a> <a id="17843" class="Keyword">import</a> <a id="17850" href="graph-theory.regular-undirected-graphs.html" class="Module">graph-theory.regular-undirected-graphs</a>
<a id="17889" class="Keyword">open</a> <a id="17894" class="Keyword">import</a> <a id="17901" href="graph-theory.simple-undirected-graphs.html" class="Module">graph-theory.simple-undirected-graphs</a>
<a id="17939" class="Keyword">open</a> <a id="17944" class="Keyword">import</a> <a id="17951" href="graph-theory.undirected-graphs.html" class="Module">graph-theory.undirected-graphs</a>
<a id="17982" class="Keyword">open</a> <a id="17987" class="Keyword">import</a> <a id="17994" href="graph-theory.voltage-graphs.html" class="Module">graph-theory.voltage-graphs</a>
</pre>
## Group theory

<pre class="Agda"><a id="18052" class="Keyword">open</a> <a id="18057" class="Keyword">import</a> <a id="18064" href="group-theory.html" class="Module">group-theory</a>
<a id="18077" class="Keyword">open</a> <a id="18082" class="Keyword">import</a> <a id="18089" href="group-theory.abelian-groups.html" class="Module">group-theory.abelian-groups</a>
<a id="18117" class="Keyword">open</a> <a id="18122" class="Keyword">import</a> <a id="18129" href="group-theory.abelian-subgroups.html" class="Module">group-theory.abelian-subgroups</a>
<a id="18160" class="Keyword">open</a> <a id="18165" class="Keyword">import</a> <a id="18172" href="group-theory.abstract-group-torsors.html" class="Module">group-theory.abstract-group-torsors</a>
<a id="18208" class="Keyword">open</a> <a id="18213" class="Keyword">import</a> <a id="18220" href="group-theory.addition-homomorphisms-abelian-groups.html" class="Module">group-theory.addition-homomorphisms-abelian-groups</a>
<a id="18271" class="Keyword">open</a> <a id="18276" class="Keyword">import</a> <a id="18283" href="group-theory.category-of-groups.html" class="Module">group-theory.category-of-groups</a>
<a id="18315" class="Keyword">open</a> <a id="18320" class="Keyword">import</a> <a id="18327" href="group-theory.category-of-semigroups.html" class="Module">group-theory.category-of-semigroups</a>
<a id="18363" class="Keyword">open</a> <a id="18368" class="Keyword">import</a> <a id="18375" href="group-theory.cayleys-theorem.html" class="Module">group-theory.cayleys-theorem</a>
<a id="18404" class="Keyword">open</a> <a id="18409" class="Keyword">import</a> <a id="18416" href="group-theory.concrete-group-actions.html" class="Module">group-theory.concrete-group-actions</a>
<a id="18452" class="Keyword">open</a> <a id="18457" class="Keyword">import</a> <a id="18464" href="group-theory.concrete-groups.html" class="Module">group-theory.concrete-groups</a>
<a id="18493" class="Keyword">open</a> <a id="18498" class="Keyword">import</a> <a id="18505" href="group-theory.concrete-subgroups.html" class="Module">group-theory.concrete-subgroups</a>
<a id="18537" class="Keyword">open</a> <a id="18542" class="Keyword">import</a> <a id="18549" href="group-theory.conjugation.html" class="Module">group-theory.conjugation</a>
<a id="18574" class="Keyword">open</a> <a id="18579" class="Keyword">import</a> <a id="18586" href="group-theory.embeddings-groups.html" class="Module">group-theory.embeddings-groups</a>
<a id="18617" class="Keyword">open</a> <a id="18622" class="Keyword">import</a> <a id="18629" href="group-theory.endomorphism-rings-abelian-groups.html" class="Module">group-theory.endomorphism-rings-abelian-groups</a>
<a id="18676" class="Keyword">open</a> <a id="18681" class="Keyword">import</a> <a id="18688" href="group-theory.equivalences-group-actions.html" class="Module">group-theory.equivalences-group-actions</a>
<a id="18728" class="Keyword">open</a> <a id="18733" class="Keyword">import</a> <a id="18740" href="group-theory.equivalences-semigroups.html" class="Module">group-theory.equivalences-semigroups</a>
<a id="18777" class="Keyword">open</a> <a id="18782" class="Keyword">import</a> <a id="18789" href="group-theory.examples-higher-groups.html" class="Module">group-theory.examples-higher-groups</a>
<a id="18825" class="Keyword">open</a> <a id="18830" class="Keyword">import</a> <a id="18837" href="group-theory.furstenberg-groups.html" class="Module">group-theory.furstenberg-groups</a>
<a id="18869" class="Keyword">open</a> <a id="18874" class="Keyword">import</a> <a id="18881" href="group-theory.group-actions.html" class="Module">group-theory.group-actions</a>
<a id="18908" class="Keyword">open</a> <a id="18913" class="Keyword">import</a> <a id="18920" href="group-theory.groups.html" class="Module">group-theory.groups</a>
<a id="18940" class="Keyword">open</a> <a id="18945" class="Keyword">import</a> <a id="18952" href="group-theory.higher-groups.html" class="Module">group-theory.higher-groups</a>
<a id="18979" class="Keyword">open</a> <a id="18984" class="Keyword">import</a> <a id="18991" href="group-theory.homomorphisms-abelian-groups.html" class="Module">group-theory.homomorphisms-abelian-groups</a>
<a id="19033" class="Keyword">open</a> <a id="19038" class="Keyword">import</a> <a id="19045" href="group-theory.homomorphisms-group-actions.html" class="Module">group-theory.homomorphisms-group-actions</a>
<a id="19086" class="Keyword">open</a> <a id="19091" class="Keyword">import</a> <a id="19098" href="group-theory.homomorphisms-groups.html" class="Module">group-theory.homomorphisms-groups</a>
<a id="19132" class="Keyword">open</a> <a id="19137" class="Keyword">import</a> <a id="19144" href="group-theory.homomorphisms-monoids.html" class="Module">group-theory.homomorphisms-monoids</a>
<a id="19179" class="Keyword">open</a> <a id="19184" class="Keyword">import</a> <a id="19191" href="group-theory.homomorphisms-semigroups.html" class="Module">group-theory.homomorphisms-semigroups</a>
<a id="19229" class="Keyword">open</a> <a id="19234" class="Keyword">import</a> <a id="19241" href="group-theory.inverse-semigroups.html" class="Module">group-theory.inverse-semigroups</a>
<a id="19273" class="Keyword">open</a> <a id="19278" class="Keyword">import</a> <a id="19285" href="group-theory.invertible-elements-monoids.html" class="Module">group-theory.invertible-elements-monoids</a>
<a id="19326" class="Keyword">open</a> <a id="19331" class="Keyword">import</a> <a id="19338" href="group-theory.isomorphisms-abelian-groups.html" class="Module">group-theory.isomorphisms-abelian-groups</a>
<a id="19379" class="Keyword">open</a> <a id="19384" class="Keyword">import</a> <a id="19391" href="group-theory.isomorphisms-group-actions.html" class="Module">group-theory.isomorphisms-group-actions</a>
<a id="19431" class="Keyword">open</a> <a id="19436" class="Keyword">import</a> <a id="19443" href="group-theory.isomorphisms-groups.html" class="Module">group-theory.isomorphisms-groups</a>
<a id="19476" class="Keyword">open</a> <a id="19481" class="Keyword">import</a> <a id="19488" href="group-theory.isomorphisms-semigroups.html" class="Module">group-theory.isomorphisms-semigroups</a>
<a id="19525" class="Keyword">open</a> <a id="19530" class="Keyword">import</a> <a id="19537" href="group-theory.mere-equivalences-group-actions.html" class="Module">group-theory.mere-equivalences-group-actions</a>
<a id="19582" class="Keyword">open</a> <a id="19587" class="Keyword">import</a> <a id="19594" href="group-theory.monoids.html" class="Module">group-theory.monoids</a>
<a id="19615" class="Keyword">open</a> <a id="19620" class="Keyword">import</a> <a id="19627" href="group-theory.orbits-group-actions.html" class="Module">group-theory.orbits-group-actions</a>
<a id="19661" class="Keyword">open</a> <a id="19666" class="Keyword">import</a> <a id="19673" href="group-theory.precategory-of-group-actions.html" class="Module">group-theory.precategory-of-group-actions</a>
<a id="19715" class="Keyword">open</a> <a id="19720" class="Keyword">import</a> <a id="19727" href="group-theory.precategory-of-groups.html" class="Module">group-theory.precategory-of-groups</a>
<a id="19762" class="Keyword">open</a> <a id="19767" class="Keyword">import</a> <a id="19774" href="group-theory.precategory-of-semigroups.html" class="Module">group-theory.precategory-of-semigroups</a>
<a id="19813" class="Keyword">open</a> <a id="19818" class="Keyword">import</a> <a id="19825" href="group-theory.principal-group-actions.html" class="Module">group-theory.principal-group-actions</a>
<a id="19862" class="Keyword">open</a> <a id="19867" class="Keyword">import</a> <a id="19874" href="group-theory.semigroups.html" class="Module">group-theory.semigroups</a>
<a id="19898" class="Keyword">open</a> <a id="19903" class="Keyword">import</a> <a id="19910" href="group-theory.sheargroups.html" class="Module">group-theory.sheargroups</a>
<a id="19935" class="Keyword">open</a> <a id="19940" class="Keyword">import</a> <a id="19947" href="group-theory.stabilizer-groups.html" class="Module">group-theory.stabilizer-groups</a>
<a id="19978" class="Keyword">open</a> <a id="19983" class="Keyword">import</a> <a id="19990" href="group-theory.subgroups.html" class="Module">group-theory.subgroups</a>
<a id="20013" class="Keyword">open</a> <a id="20018" class="Keyword">import</a> <a id="20025" href="group-theory.substitution-functor-group-actions.html" class="Module">group-theory.substitution-functor-group-actions</a>
<a id="20073" class="Keyword">open</a> <a id="20078" class="Keyword">import</a> <a id="20085" href="group-theory.symmetric-groups.html" class="Module">group-theory.symmetric-groups</a>
<a id="20115" class="Keyword">open</a> <a id="20120" class="Keyword">import</a> <a id="20127" href="group-theory.transitive-group-actions.html" class="Module">group-theory.transitive-group-actions</a>
</pre>
## Linear algebra

<pre class="Agda"><a id="20197" class="Keyword">open</a> <a id="20202" class="Keyword">import</a> <a id="20209" href="linear-algebra.html" class="Module">linear-algebra</a>
<a id="20224" class="Keyword">open</a> <a id="20229" class="Keyword">import</a> <a id="20236" href="linear-algebra.constant-matrices.html" class="Module">linear-algebra.constant-matrices</a>
<a id="20269" class="Keyword">open</a> <a id="20274" class="Keyword">import</a> <a id="20281" href="linear-algebra.constant-vectors.html" class="Module">linear-algebra.constant-vectors</a>
<a id="20313" class="Keyword">open</a> <a id="20318" class="Keyword">import</a> <a id="20325" href="linear-algebra.diagonal-matrices-on-rings.html" class="Module">linear-algebra.diagonal-matrices-on-rings</a>
<a id="20367" class="Keyword">open</a> <a id="20372" class="Keyword">import</a> <a id="20379" href="linear-algebra.functoriality-matrices.html" class="Module">linear-algebra.functoriality-matrices</a>
<a id="20417" class="Keyword">open</a> <a id="20422" class="Keyword">import</a> <a id="20429" href="linear-algebra.functoriality-vectors.html" class="Module">linear-algebra.functoriality-vectors</a>
<a id="20466" class="Keyword">open</a> <a id="20471" class="Keyword">import</a> <a id="20478" href="linear-algebra.matrices-on-rings.html" class="Module">linear-algebra.matrices-on-rings</a>
<a id="20511" class="Keyword">open</a> <a id="20516" class="Keyword">import</a> <a id="20523" href="linear-algebra.matrices.html" class="Module">linear-algebra.matrices</a>
<a id="20547" class="Keyword">open</a> <a id="20552" class="Keyword">import</a> <a id="20559" href="linear-algebra.multiplication-matrices.html" class="Module">linear-algebra.multiplication-matrices</a>
<a id="20598" class="Keyword">open</a> <a id="20603" class="Keyword">import</a> <a id="20610" href="linear-algebra.scalar-multiplication-matrices.html" class="Module">linear-algebra.scalar-multiplication-matrices</a>
<a id="20656" class="Keyword">open</a> <a id="20661" class="Keyword">import</a> <a id="20668" href="linear-algebra.scalar-multiplication-vectors.html" class="Module">linear-algebra.scalar-multiplication-vectors</a>
<a id="20713" class="Keyword">open</a> <a id="20718" class="Keyword">import</a> <a id="20725" href="linear-algebra.transposition-matrices.html" class="Module">linear-algebra.transposition-matrices</a>
<a id="20763" class="Keyword">open</a> <a id="20768" class="Keyword">import</a> <a id="20775" href="linear-algebra.vectors-on-rings.html" class="Module">linear-algebra.vectors-on-rings</a>
<a id="20807" class="Keyword">open</a> <a id="20812" class="Keyword">import</a> <a id="20819" href="linear-algebra.vectors.html" class="Module">linear-algebra.vectors</a>
</pre>
## Order theory

<pre class="Agda"><a id="20872" class="Keyword">open</a> <a id="20877" class="Keyword">import</a> <a id="20884" href="order-theory.html" class="Module">order-theory</a>
<a id="20897" class="Keyword">open</a> <a id="20902" class="Keyword">import</a> <a id="20909" href="order-theory.chains-posets.html" class="Module">order-theory.chains-posets</a>
<a id="20936" class="Keyword">open</a> <a id="20941" class="Keyword">import</a> <a id="20948" href="order-theory.chains-preorders.html" class="Module">order-theory.chains-preorders</a>
<a id="20978" class="Keyword">open</a> <a id="20983" class="Keyword">import</a> <a id="20990" href="order-theory.decidable-subposets.html" class="Module">order-theory.decidable-subposets</a>
<a id="21023" class="Keyword">open</a> <a id="21028" class="Keyword">import</a> <a id="21035" href="order-theory.decidable-subpreorders.html" class="Module">order-theory.decidable-subpreorders</a>
<a id="21071" class="Keyword">open</a> <a id="21076" class="Keyword">import</a> <a id="21083" href="order-theory.finite-posets.html" class="Module">order-theory.finite-posets</a>
<a id="21110" class="Keyword">open</a> <a id="21115" class="Keyword">import</a> <a id="21122" href="order-theory.finite-preorders.html" class="Module">order-theory.finite-preorders</a>
<a id="21152" class="Keyword">open</a> <a id="21157" class="Keyword">import</a> <a id="21164" href="order-theory.finitely-graded-posets.html" class="Module">order-theory.finitely-graded-posets</a>
<a id="21200" class="Keyword">open</a> <a id="21205" class="Keyword">import</a> <a id="21212" href="order-theory.greatest-lower-bounds-posets.html" class="Module">order-theory.greatest-lower-bounds-posets</a>
<a id="21254" class="Keyword">open</a> <a id="21259" class="Keyword">import</a> <a id="21266" href="order-theory.interval-subposets.html" class="Module">order-theory.interval-subposets</a>
<a id="21298" class="Keyword">open</a> <a id="21303" class="Keyword">import</a> <a id="21310" href="order-theory.largest-elements-posets.html" class="Module">order-theory.largest-elements-posets</a>
<a id="21347" class="Keyword">open</a> <a id="21352" class="Keyword">import</a> <a id="21359" href="order-theory.largest-elements-preorders.html" class="Module">order-theory.largest-elements-preorders</a>
<a id="21399" class="Keyword">open</a> <a id="21404" class="Keyword">import</a> <a id="21411" href="order-theory.least-elements-posets.html" class="Module">order-theory.least-elements-posets</a>
<a id="21446" class="Keyword">open</a> <a id="21451" class="Keyword">import</a> <a id="21458" href="order-theory.least-elements-preorders.html" class="Module">order-theory.least-elements-preorders</a>
<a id="21496" class="Keyword">open</a> <a id="21501" class="Keyword">import</a> <a id="21508" href="order-theory.locally-finite-posets.html" class="Module">order-theory.locally-finite-posets</a>
<a id="21543" class="Keyword">open</a> <a id="21548" class="Keyword">import</a> <a id="21555" href="order-theory.maximal-chains-posets.html" class="Module">order-theory.maximal-chains-posets</a>
<a id="21590" class="Keyword">open</a> <a id="21595" class="Keyword">import</a> <a id="21602" href="order-theory.maximal-chains-preorders.html" class="Module">order-theory.maximal-chains-preorders</a>
<a id="21640" class="Keyword">open</a> <a id="21645" class="Keyword">import</a> <a id="21652" href="order-theory.meet-semilattices.html" class="Module">order-theory.meet-semilattices</a>
<a id="21683" class="Keyword">open</a> <a id="21688" class="Keyword">import</a> <a id="21695" href="order-theory.planar-binary-trees.html" class="Module">order-theory.planar-binary-trees</a>
<a id="21728" class="Keyword">open</a> <a id="21733" class="Keyword">import</a> <a id="21740" href="order-theory.posets.html" class="Module">order-theory.posets</a>
<a id="21760" class="Keyword">open</a> <a id="21765" class="Keyword">import</a> <a id="21772" href="order-theory.preorders.html" class="Module">order-theory.preorders</a>
<a id="21795" class="Keyword">open</a> <a id="21800" class="Keyword">import</a> <a id="21807" href="order-theory.subposets.html" class="Module">order-theory.subposets</a>
<a id="21830" class="Keyword">open</a> <a id="21835" class="Keyword">import</a> <a id="21842" href="order-theory.subpreorders.html" class="Module">order-theory.subpreorders</a>
<a id="21868" class="Keyword">open</a> <a id="21873" class="Keyword">import</a> <a id="21880" href="order-theory.total-posets.html" class="Module">order-theory.total-posets</a>
<a id="21906" class="Keyword">open</a> <a id="21911" class="Keyword">import</a> <a id="21918" href="order-theory.total-preorders.html" class="Module">order-theory.total-preorders</a>
</pre>
## Polytopes

<pre class="Agda"><a id="21974" class="Keyword">open</a> <a id="21979" class="Keyword">import</a> <a id="21986" href="polytopes.html" class="Module">polytopes</a>
<a id="21996" class="Keyword">open</a> <a id="22001" class="Keyword">import</a> <a id="22008" href="polytopes.abstract-polytopes.html" class="Module">polytopes.abstract-polytopes</a>
</pre>
## Ring theory

<pre class="Agda"><a id="22066" class="Keyword">open</a> <a id="22071" class="Keyword">import</a> <a id="22078" href="ring-theory.html" class="Module">ring-theory</a>
<a id="22090" class="Keyword">open</a> <a id="22095" class="Keyword">import</a> <a id="22102" href="ring-theory.commutative-rings.html" class="Module">ring-theory.commutative-rings</a>
<a id="22132" class="Keyword">open</a> <a id="22137" class="Keyword">import</a> <a id="22144" href="ring-theory.discrete-fields.html" class="Module">ring-theory.discrete-fields</a>
<a id="22172" class="Keyword">open</a> <a id="22177" class="Keyword">import</a> <a id="22184" href="ring-theory.division-rings.html" class="Module">ring-theory.division-rings</a>
<a id="22211" class="Keyword">open</a> <a id="22216" class="Keyword">import</a> <a id="22223" href="ring-theory.eisenstein-integers.html" class="Module">ring-theory.eisenstein-integers</a>
<a id="22255" class="Keyword">open</a> <a id="22260" class="Keyword">import</a> <a id="22267" href="ring-theory.gaussian-integers.html" class="Module">ring-theory.gaussian-integers</a>
<a id="22297" class="Keyword">open</a> <a id="22302" class="Keyword">import</a> <a id="22309" href="ring-theory.homomorphisms-commutative-rings.html" class="Module">ring-theory.homomorphisms-commutative-rings</a>
<a id="22353" class="Keyword">open</a> <a id="22358" class="Keyword">import</a> <a id="22365" href="ring-theory.homomorphisms-rings.html" class="Module">ring-theory.homomorphisms-rings</a>
<a id="22397" class="Keyword">open</a> <a id="22402" class="Keyword">import</a> <a id="22409" href="ring-theory.ideals-generated-by-subsets-rings.html" class="Module">ring-theory.ideals-generated-by-subsets-rings</a>
<a id="22455" class="Keyword">open</a> <a id="22460" class="Keyword">import</a> <a id="22467" href="ring-theory.ideals-rings.html" class="Module">ring-theory.ideals-rings</a>
<a id="22492" class="Keyword">open</a> <a id="22497" class="Keyword">import</a> <a id="22504" href="ring-theory.invertible-elements-rings.html" class="Module">ring-theory.invertible-elements-rings</a>
<a id="22542" class="Keyword">open</a> <a id="22547" class="Keyword">import</a> <a id="22554" href="ring-theory.isomorphisms-commutative-rings.html" class="Module">ring-theory.isomorphisms-commutative-rings</a>
<a id="22597" class="Keyword">open</a> <a id="22602" class="Keyword">import</a> <a id="22609" href="ring-theory.isomorphisms-rings.html" class="Module">ring-theory.isomorphisms-rings</a>
<a id="22640" class="Keyword">open</a> <a id="22645" class="Keyword">import</a> <a id="22652" href="ring-theory.localizations-rings.html" class="Module">ring-theory.localizations-rings</a>
<a id="22684" class="Keyword">open</a> <a id="22689" class="Keyword">import</a> <a id="22696" href="ring-theory.nontrivial-rings.html" class="Module">ring-theory.nontrivial-rings</a>
<a id="22725" class="Keyword">open</a> <a id="22730" class="Keyword">import</a> <a id="22737" href="ring-theory.rings.html" class="Module">ring-theory.rings</a>
</pre>
## Synthetic homotopy theory

<pre class="Agda"><a id="22798" class="Keyword">open</a> <a id="22803" class="Keyword">import</a> <a id="22810" href="synthetic-homotopy-theory.html" class="Module">synthetic-homotopy-theory</a>
<a id="22836" class="Keyword">open</a> <a id="22841" class="Keyword">import</a> <a id="22848" href="synthetic-homotopy-theory.23-pullbacks.html" class="Module">synthetic-homotopy-theory.23-pullbacks</a>
<a id="22887" class="Keyword">open</a> <a id="22892" class="Keyword">import</a> <a id="22899" href="synthetic-homotopy-theory.24-pushouts.html" class="Module">synthetic-homotopy-theory.24-pushouts</a>
<a id="22937" class="Keyword">open</a> <a id="22942" class="Keyword">import</a> <a id="22949" href="synthetic-homotopy-theory.25-cubical-diagrams.html" class="Module">synthetic-homotopy-theory.25-cubical-diagrams</a>
<a id="22995" class="Keyword">open</a> <a id="23000" class="Keyword">import</a> <a id="23007" href="synthetic-homotopy-theory.26-descent.html" class="Module">synthetic-homotopy-theory.26-descent</a>
<a id="23044" class="Keyword">open</a> <a id="23049" class="Keyword">import</a> <a id="23056" href="synthetic-homotopy-theory.26-id-pushout.html" class="Module">synthetic-homotopy-theory.26-id-pushout</a>
<a id="23096" class="Keyword">open</a> <a id="23101" class="Keyword">import</a> <a id="23108" href="synthetic-homotopy-theory.27-sequences.html" class="Module">synthetic-homotopy-theory.27-sequences</a>
<a id="23147" class="Keyword">open</a> <a id="23152" class="Keyword">import</a> <a id="23159" href="synthetic-homotopy-theory.circle.html" class="Module">synthetic-homotopy-theory.circle</a>
<a id="23192" class="Keyword">open</a> <a id="23197" class="Keyword">import</a> <a id="23204" href="synthetic-homotopy-theory.commutative-operations.html" class="Module">synthetic-homotopy-theory.commutative-operations</a>
<a id="23253" class="Keyword">open</a> <a id="23258" class="Keyword">import</a> <a id="23265" href="synthetic-homotopy-theory.cyclic-types.html" class="Module">synthetic-homotopy-theory.cyclic-types</a>
<a id="23304" class="Keyword">open</a> <a id="23309" class="Keyword">import</a> <a id="23316" href="synthetic-homotopy-theory.double-loop-spaces.html" class="Module">synthetic-homotopy-theory.double-loop-spaces</a>
<a id="23361" class="Keyword">open</a> <a id="23366" class="Keyword">import</a> <a id="23373" href="synthetic-homotopy-theory.functoriality-loop-spaces.html" class="Module">synthetic-homotopy-theory.functoriality-loop-spaces</a>
<a id="23425" class="Keyword">open</a> <a id="23430" class="Keyword">import</a> <a id="23437" href="synthetic-homotopy-theory.groups-of-loops-in-1-types.html" class="Module">synthetic-homotopy-theory.groups-of-loops-in-1-types</a>
<a id="23490" class="Keyword">open</a> <a id="23495" class="Keyword">import</a> <a id="23502" href="synthetic-homotopy-theory.infinite-cyclic-types.html" class="Module">synthetic-homotopy-theory.infinite-cyclic-types</a>
<a id="23550" class="Keyword">open</a> <a id="23555" class="Keyword">import</a> <a id="23562" href="synthetic-homotopy-theory.interval-type.html" class="Module">synthetic-homotopy-theory.interval-type</a>
<a id="23602" class="Keyword">open</a> <a id="23607" class="Keyword">import</a> <a id="23614" href="synthetic-homotopy-theory.iterated-loop-spaces.html" class="Module">synthetic-homotopy-theory.iterated-loop-spaces</a>
<a id="23661" class="Keyword">open</a> <a id="23666" class="Keyword">import</a> <a id="23673" href="synthetic-homotopy-theory.loop-spaces.html" class="Module">synthetic-homotopy-theory.loop-spaces</a>
<a id="23711" class="Keyword">open</a> <a id="23716" class="Keyword">import</a> <a id="23723" href="synthetic-homotopy-theory.pointed-dependent-functions.html" class="Module">synthetic-homotopy-theory.pointed-dependent-functions</a>
<a id="23777" class="Keyword">open</a> <a id="23782" class="Keyword">import</a> <a id="23789" href="synthetic-homotopy-theory.pointed-equivalences.html" class="Module">synthetic-homotopy-theory.pointed-equivalences</a>
<a id="23836" class="Keyword">open</a> <a id="23841" class="Keyword">import</a> <a id="23848" href="synthetic-homotopy-theory.pointed-families-of-types.html" class="Module">synthetic-homotopy-theory.pointed-families-of-types</a>
<a id="23900" class="Keyword">open</a> <a id="23905" class="Keyword">import</a> <a id="23912" href="synthetic-homotopy-theory.pointed-homotopies.html" class="Module">synthetic-homotopy-theory.pointed-homotopies</a>
<a id="23957" class="Keyword">open</a> <a id="23962" class="Keyword">import</a> <a id="23969" href="synthetic-homotopy-theory.pointed-maps.html" class="Module">synthetic-homotopy-theory.pointed-maps</a>
<a id="24008" class="Keyword">open</a> <a id="24013" class="Keyword">import</a> <a id="24020" href="synthetic-homotopy-theory.pointed-types.html" class="Module">synthetic-homotopy-theory.pointed-types</a>
<a id="24060" class="Keyword">open</a> <a id="24065" class="Keyword">import</a> <a id="24072" href="synthetic-homotopy-theory.spaces.html" class="Module">synthetic-homotopy-theory.spaces</a>
<a id="24105" class="Keyword">open</a> <a id="24110" class="Keyword">import</a> <a id="24117" href="synthetic-homotopy-theory.triple-loop-spaces.html" class="Module">synthetic-homotopy-theory.triple-loop-spaces</a>
<a id="24162" class="Keyword">open</a> <a id="24167" class="Keyword">import</a> <a id="24174" href="synthetic-homotopy-theory.universal-cover-circle.html" class="Module">synthetic-homotopy-theory.universal-cover-circle</a>
</pre>
## Tutorials

<pre class="Agda"><a id="24250" class="Keyword">open</a> <a id="24255" class="Keyword">import</a> <a id="24262" href="tutorials.basic-agda.html" class="Module">tutorials.basic-agda</a>
</pre>
## Univalent combinatorics

<pre class="Agda"><a id="24324" class="Keyword">open</a> <a id="24329" class="Keyword">import</a> <a id="24336" href="univalent-combinatorics.html" class="Module">univalent-combinatorics</a>
<a id="24360" class="Keyword">open</a> <a id="24365" class="Keyword">import</a> <a id="24372" href="univalent-combinatorics.2-element-decidable-subtypes.html" class="Module">univalent-combinatorics.2-element-decidable-subtypes</a>
<a id="24425" class="Keyword">open</a> <a id="24430" class="Keyword">import</a> <a id="24437" href="univalent-combinatorics.2-element-subtypes.html" class="Module">univalent-combinatorics.2-element-subtypes</a>
<a id="24480" class="Keyword">open</a> <a id="24485" class="Keyword">import</a> <a id="24492" href="univalent-combinatorics.2-element-types.html" class="Module">univalent-combinatorics.2-element-types</a>
<a id="24532" class="Keyword">open</a> <a id="24537" class="Keyword">import</a> <a id="24544" href="univalent-combinatorics.binomial-types.html" class="Module">univalent-combinatorics.binomial-types</a>
<a id="24583" class="Keyword">open</a> <a id="24588" class="Keyword">import</a> <a id="24595" href="univalent-combinatorics.cartesian-product-types.html" class="Module">univalent-combinatorics.cartesian-product-types</a>
<a id="24643" class="Keyword">open</a> <a id="24648" class="Keyword">import</a> <a id="24655" href="univalent-combinatorics.classical-finite-types.html" class="Module">univalent-combinatorics.classical-finite-types</a>
<a id="24702" class="Keyword">open</a> <a id="24707" class="Keyword">import</a> <a id="24714" href="univalent-combinatorics.complements-isolated-points.html" class="Module">univalent-combinatorics.complements-isolated-points</a>
<a id="24766" class="Keyword">open</a> <a id="24771" class="Keyword">import</a> <a id="24778" href="univalent-combinatorics.coproduct-types.html" class="Module">univalent-combinatorics.coproduct-types</a>
<a id="24818" class="Keyword">open</a> <a id="24823" class="Keyword">import</a> <a id="24830" href="univalent-combinatorics.counting-decidable-subtypes.html" class="Module">univalent-combinatorics.counting-decidable-subtypes</a>
<a id="24882" class="Keyword">open</a> <a id="24887" class="Keyword">import</a> <a id="24894" href="univalent-combinatorics.counting-dependent-pair-types.html" class="Module">univalent-combinatorics.counting-dependent-pair-types</a>
<a id="24948" class="Keyword">open</a> <a id="24953" class="Keyword">import</a> <a id="24960" href="univalent-combinatorics.counting-maybe.html" class="Module">univalent-combinatorics.counting-maybe</a>
<a id="24999" class="Keyword">open</a> <a id="25004" class="Keyword">import</a> <a id="25011" href="univalent-combinatorics.counting.html" class="Module">univalent-combinatorics.counting</a>
<a id="25044" class="Keyword">open</a> <a id="25049" class="Keyword">import</a> <a id="25056" href="univalent-combinatorics.cubes.html" class="Module">univalent-combinatorics.cubes</a>
<a id="25086" class="Keyword">open</a> <a id="25091" class="Keyword">import</a> <a id="25098" href="univalent-combinatorics.decidable-dependent-function-types.html" class="Module">univalent-combinatorics.decidable-dependent-function-types</a>
<a id="25157" class="Keyword">open</a> <a id="25162" class="Keyword">import</a> <a id="25169" href="univalent-combinatorics.decidable-dependent-pair-types.html" class="Module">univalent-combinatorics.decidable-dependent-pair-types</a>
<a id="25224" class="Keyword">open</a> <a id="25229" class="Keyword">import</a> <a id="25236" href="univalent-combinatorics.decidable-subtypes.html" class="Module">univalent-combinatorics.decidable-subtypes</a>
<a id="25279" class="Keyword">open</a> <a id="25284" class="Keyword">import</a> <a id="25291" href="univalent-combinatorics.dependent-function-types.html" class="Module">univalent-combinatorics.dependent-function-types</a>
<a id="25340" class="Keyword">open</a> <a id="25345" class="Keyword">import</a> <a id="25352" href="univalent-combinatorics.dedekind-finite-sets.html" class="Module">univalent-combinatorics.dedekind-finite-sets</a>
<a id="25397" class="Keyword">open</a> <a id="25402" class="Keyword">import</a> <a id="25409" href="univalent-combinatorics.dependent-sum-finite-types.html" class="Module">univalent-combinatorics.dependent-sum-finite-types</a>
<a id="25460" class="Keyword">open</a> <a id="25465" class="Keyword">import</a> <a id="25472" href="univalent-combinatorics.distributivity-of-set-truncation-over-finite-products.html" class="Module">univalent-combinatorics.distributivity-of-set-truncation-over-finite-products</a>
<a id="25550" class="Keyword">open</a> <a id="25555" class="Keyword">import</a> <a id="25562" href="univalent-combinatorics.double-counting.html" class="Module">univalent-combinatorics.double-counting</a>
<a id="25602" class="Keyword">open</a> <a id="25607" class="Keyword">import</a> <a id="25614" href="univalent-combinatorics.embeddings-standard-finite-types.html" class="Module">univalent-combinatorics.embeddings-standard-finite-types</a>
<a id="25671" class="Keyword">open</a> <a id="25676" class="Keyword">import</a> <a id="25683" href="univalent-combinatorics.embeddings.html" class="Module">univalent-combinatorics.embeddings</a>
<a id="25718" class="Keyword">open</a> <a id="25723" class="Keyword">import</a> <a id="25730" href="univalent-combinatorics.equality-finite-types.html" class="Module">univalent-combinatorics.equality-finite-types</a>
<a id="25776" class="Keyword">open</a> <a id="25781" class="Keyword">import</a> <a id="25788" href="univalent-combinatorics.equality-standard-finite-types.html" class="Module">univalent-combinatorics.equality-standard-finite-types</a>
<a id="25843" class="Keyword">open</a> <a id="25848" class="Keyword">import</a> <a id="25855" href="univalent-combinatorics.equivalences-cubes.html" class="Module">univalent-combinatorics.equivalences-cubes</a>
<a id="25898" class="Keyword">open</a> <a id="25903" class="Keyword">import</a> <a id="25910" href="univalent-combinatorics.equivalences-standard-finite-types.html" class="Module">univalent-combinatorics.equivalences-standard-finite-types</a>
<a id="25969" class="Keyword">open</a> <a id="25974" class="Keyword">import</a> <a id="25981" href="univalent-combinatorics.equivalences.html" class="Module">univalent-combinatorics.equivalences</a>
<a id="26018" class="Keyword">open</a> <a id="26023" class="Keyword">import</a> <a id="26030" href="univalent-combinatorics.fibers-of-maps.html" class="Module">univalent-combinatorics.fibers-of-maps</a>
<a id="26069" class="Keyword">open</a> <a id="26074" class="Keyword">import</a> <a id="26081" href="univalent-combinatorics.finite-choice.html" class="Module">univalent-combinatorics.finite-choice</a>
<a id="26119" class="Keyword">open</a> <a id="26124" class="Keyword">import</a> <a id="26131" href="univalent-combinatorics.finite-connected-components.html" class="Module">univalent-combinatorics.finite-connected-components</a>
<a id="26183" class="Keyword">open</a> <a id="26188" class="Keyword">import</a> <a id="26195" href="univalent-combinatorics.finite-presentations.html" class="Module">univalent-combinatorics.finite-presentations</a>
<a id="26240" class="Keyword">open</a> <a id="26245" class="Keyword">import</a> <a id="26252" href="univalent-combinatorics.finite-types.html" class="Module">univalent-combinatorics.finite-types</a>
<a id="26289" class="Keyword">open</a> <a id="26294" class="Keyword">import</a> <a id="26301" href="univalent-combinatorics.finitely-presented-types.html" class="Module">univalent-combinatorics.finitely-presented-types</a>
<a id="26350" class="Keyword">open</a> <a id="26355" class="Keyword">import</a> <a id="26362" href="univalent-combinatorics.function-types.html" class="Module">univalent-combinatorics.function-types</a>
<a id="26401" class="Keyword">open</a> <a id="26406" class="Keyword">import</a> <a id="26413" href="univalent-combinatorics.image-of-maps.html" class="Module">univalent-combinatorics.image-of-maps</a>
<a id="26451" class="Keyword">open</a> <a id="26456" class="Keyword">import</a> <a id="26463" href="univalent-combinatorics.inequality-types-with-counting.html" class="Module">univalent-combinatorics.inequality-types-with-counting</a>
<a id="26518" class="Keyword">open</a> <a id="26523" class="Keyword">import</a> <a id="26530" href="univalent-combinatorics.injective-maps.html" class="Module">univalent-combinatorics.injective-maps</a>
<a id="26569" class="Keyword">open</a> <a id="26574" class="Keyword">import</a> <a id="26581" href="univalent-combinatorics.kuratowsky-finite-sets.html" class="Module">univalent-combinatorics.kuratowsky-finite-sets</a>
<a id="26628" class="Keyword">open</a> <a id="26633" class="Keyword">import</a> <a id="26640" href="univalent-combinatorics.lists.html" class="Module">univalent-combinatorics.lists</a>
<a id="26670" class="Keyword">open</a> <a id="26675" class="Keyword">import</a> <a id="26682" href="univalent-combinatorics.maybe.html" class="Module">univalent-combinatorics.maybe</a>
<a id="26712" class="Keyword">open</a> <a id="26717" class="Keyword">import</a> <a id="26724" href="univalent-combinatorics.orientations-cubes.html" class="Module">univalent-combinatorics.orientations-cubes</a>
<a id="26767" class="Keyword">open</a> <a id="26772" class="Keyword">import</a> <a id="26779" href="univalent-combinatorics.petri-nets.html" class="Module">univalent-combinatorics.petri-nets</a>
<a id="26814" class="Keyword">open</a> <a id="26819" class="Keyword">import</a> <a id="26826" href="univalent-combinatorics.pi-finite-types.html" class="Module">univalent-combinatorics.pi-finite-types</a>
<a id="26866" class="Keyword">open</a> <a id="26871" class="Keyword">import</a> <a id="26878" href="univalent-combinatorics.pigeonhole-principle.html" class="Module">univalent-combinatorics.pigeonhole-principle</a>
<a id="26923" class="Keyword">open</a> <a id="26928" class="Keyword">import</a> <a id="26935" href="univalent-combinatorics.presented-pi-finite-types.html" class="Module">univalent-combinatorics.presented-pi-finite-types</a>
<a id="26985" class="Keyword">open</a> <a id="26990" class="Keyword">import</a> <a id="26997" href="univalent-combinatorics.ramsey-theory.html" class="Module">univalent-combinatorics.ramsey-theory</a>
<a id="27035" class="Keyword">open</a> <a id="27040" class="Keyword">import</a> <a id="27047" href="univalent-combinatorics.retracts-of-finite-types.html" class="Module">univalent-combinatorics.retracts-of-finite-types</a>
<a id="27096" class="Keyword">open</a> <a id="27101" class="Keyword">import</a> <a id="27108" href="univalent-combinatorics.skipping-element-standard-finite-types.html" class="Module">univalent-combinatorics.skipping-element-standard-finite-types</a>
<a id="27171" class="Keyword">open</a> <a id="27176" class="Keyword">import</a> <a id="27183" href="univalent-combinatorics.species.html" class="Module">univalent-combinatorics.species</a>
<a id="27215" class="Keyword">open</a> <a id="27220" class="Keyword">import</a> <a id="27227" href="univalent-combinatorics.standard-finite-pruned-trees.html" class="Module">univalent-combinatorics.standard-finite-pruned-trees</a>
<a id="27280" class="Keyword">open</a> <a id="27285" class="Keyword">import</a> <a id="27292" href="univalent-combinatorics.standard-finite-trees.html" class="Module">univalent-combinatorics.standard-finite-trees</a>
<a id="27338" class="Keyword">open</a> <a id="27343" class="Keyword">import</a> <a id="27350" href="univalent-combinatorics.standard-finite-types.html" class="Module">univalent-combinatorics.standard-finite-types</a>
<a id="27396" class="Keyword">open</a> <a id="27401" class="Keyword">import</a> <a id="27408" href="univalent-combinatorics.sums-of-natural-numbers.html" class="Module">univalent-combinatorics.sums-of-natural-numbers</a>
<a id="27456" class="Keyword">open</a> <a id="27461" class="Keyword">import</a> <a id="27468" href="univalent-combinatorics.surjective-maps.html" class="Module">univalent-combinatorics.surjective-maps</a>
</pre>
## Wild algebra

<pre class="Agda"><a id="27538" class="Keyword">open</a> <a id="27543" class="Keyword">import</a> <a id="27550" href="wild-algebra.html" class="Module">wild-algebra</a>
<a id="27563" class="Keyword">open</a> <a id="27568" class="Keyword">import</a> <a id="27575" href="wild-algebra.magmas.html" class="Module">wild-algebra.magmas</a>
<a id="27595" class="Keyword">open</a> <a id="27600" class="Keyword">import</a> <a id="27607" href="wild-algebra.morphisms-magmas.html" class="Module">wild-algebra.morphisms-magmas</a>
<a id="27637" class="Keyword">open</a> <a id="27642" class="Keyword">import</a> <a id="27649" href="wild-algebra.morphisms-wild-unital-magmas.html" class="Module">wild-algebra.morphisms-wild-unital-magmas</a>
<a id="27691" class="Keyword">open</a> <a id="27696" class="Keyword">import</a> <a id="27703" href="wild-algebra.universal-property-lists-wild-monoids.html" class="Module">wild-algebra.universal-property-lists-wild-monoids</a>
<a id="27754" class="Keyword">open</a> <a id="27759" class="Keyword">import</a> <a id="27766" href="wild-algebra.wild-groups.html" class="Module">wild-algebra.wild-groups</a>
<a id="27791" class="Keyword">open</a> <a id="27796" class="Keyword">import</a> <a id="27803" href="wild-algebra.wild-loops.html" class="Module">wild-algebra.wild-loops</a>
<a id="27827" class="Keyword">open</a> <a id="27832" class="Keyword">import</a> <a id="27839" href="wild-algebra.wild-monoids.html" class="Module">wild-algebra.wild-monoids</a>
<a id="27865" class="Keyword">open</a> <a id="27870" class="Keyword">import</a> <a id="27877" href="wild-algebra.wild-quasigroups.html" class="Module">wild-algebra.wild-quasigroups</a>
<a id="27907" class="Keyword">open</a> <a id="27912" class="Keyword">import</a> <a id="27919" href="wild-algebra.wild-semigroups.html" class="Module">wild-algebra.wild-semigroups</a>
<a id="27948" class="Keyword">open</a> <a id="27953" class="Keyword">import</a> <a id="27960" href="wild-algebra.wild-unital-magmas.html" class="Module">wild-algebra.wild-unital-magmas</a>
</pre>
## Everything

See the list of all Agda modules [here](everything.html).

