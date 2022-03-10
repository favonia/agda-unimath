# Univalent mathematics in Agda

Welcome to the website of the `agda-unimath` formalization project.

[![build](https://github.com/UniMath/agda-unimath/actions/workflows/ci.yaml/badge.svg?branch=master)](https://github.com/UniMath/agda-unimath/actions/workflows/ci.yaml)

<pre class="Agda"><a id="281" class="Symbol">{-#</a> <a id="285" class="Keyword">OPTIONS</a> <a id="293" class="Pragma">--without-K</a> <a id="305" class="Pragma">--exact-split</a> <a id="319" class="Symbol">#-}</a>
</pre>
## Categories

<pre class="Agda"><a id="351" class="Keyword">open</a> <a id="356" class="Keyword">import</a> <a id="363" href="categories.html" class="Module">categories</a>
<a id="374" class="Keyword">open</a> <a id="379" class="Keyword">import</a> <a id="386" href="categories.adjunctions.html" class="Module">categories.adjunctions</a>
<a id="409" class="Keyword">open</a> <a id="414" class="Keyword">import</a> <a id="421" href="categories.categories.html" class="Module">categories.categories</a>
<a id="443" class="Keyword">open</a> <a id="448" class="Keyword">import</a> <a id="455" href="categories.functors.html" class="Module">categories.functors</a>
<a id="475" class="Keyword">open</a> <a id="480" class="Keyword">import</a> <a id="487" href="categories.large-categories.html" class="Module">categories.large-categories</a>
<a id="515" class="Keyword">open</a> <a id="520" class="Keyword">import</a> <a id="527" href="categories.natural-transformations.html" class="Module">categories.natural-transformations</a>
</pre>
## Elementary number theory

<pre class="Agda"><a id="604" class="Keyword">open</a> <a id="609" class="Keyword">import</a> <a id="616" href="elementary-number-theory.html" class="Module">elementary-number-theory</a>
<a id="641" class="Keyword">open</a> <a id="646" class="Keyword">import</a> <a id="653" href="elementary-number-theory.absolute-value-integers.html" class="Module">elementary-number-theory.absolute-value-integers</a>
<a id="702" class="Keyword">open</a> <a id="707" class="Keyword">import</a> <a id="714" href="elementary-number-theory.addition-integers.html" class="Module">elementary-number-theory.addition-integers</a>
<a id="757" class="Keyword">open</a> <a id="762" class="Keyword">import</a> <a id="769" href="elementary-number-theory.addition-natural-numbers.html" class="Module">elementary-number-theory.addition-natural-numbers</a>
<a id="819" class="Keyword">open</a> <a id="824" class="Keyword">import</a> <a id="831" href="elementary-number-theory.binomial-coefficients.html" class="Module">elementary-number-theory.binomial-coefficients</a>
<a id="878" class="Keyword">open</a> <a id="883" class="Keyword">import</a> <a id="890" href="elementary-number-theory.classical-finite-types.html" class="Module">elementary-number-theory.classical-finite-types</a>
<a id="938" class="Keyword">open</a> <a id="943" class="Keyword">import</a> <a id="950" href="elementary-number-theory.collatz-bijection.html" class="Module">elementary-number-theory.collatz-bijection</a>
<a id="993" class="Keyword">open</a> <a id="998" class="Keyword">import</a> <a id="1005" href="elementary-number-theory.collatz-conjecture.html" class="Module">elementary-number-theory.collatz-conjecture</a>
<a id="1049" class="Keyword">open</a> <a id="1054" class="Keyword">import</a> <a id="1061" href="elementary-number-theory.congruence-integers.html" class="Module">elementary-number-theory.congruence-integers</a>
<a id="1106" class="Keyword">open</a> <a id="1111" class="Keyword">import</a> <a id="1118" href="elementary-number-theory.congruence-natural-numbers.html" class="Module">elementary-number-theory.congruence-natural-numbers</a>
<a id="1170" class="Keyword">open</a> <a id="1175" class="Keyword">import</a> <a id="1182" href="elementary-number-theory.decidable-dependent-function-types.html" class="Module">elementary-number-theory.decidable-dependent-function-types</a>
<a id="1242" class="Keyword">open</a> <a id="1247" class="Keyword">import</a> <a id="1254" href="elementary-number-theory.decidable-dependent-pair-types.html" class="Module">elementary-number-theory.decidable-dependent-pair-types</a>
<a id="1310" class="Keyword">open</a> <a id="1315" class="Keyword">import</a> <a id="1322" href="elementary-number-theory.difference-integers.html" class="Module">elementary-number-theory.difference-integers</a>
<a id="1367" class="Keyword">open</a> <a id="1372" class="Keyword">import</a> <a id="1379" href="elementary-number-theory.distance-integers.html" class="Module">elementary-number-theory.distance-integers</a>
<a id="1422" class="Keyword">open</a> <a id="1427" class="Keyword">import</a> <a id="1434" href="elementary-number-theory.distance-natural-numbers.html" class="Module">elementary-number-theory.distance-natural-numbers</a>
<a id="1484" class="Keyword">open</a> <a id="1489" class="Keyword">import</a> <a id="1496" href="elementary-number-theory.divisibility-integers.html" class="Module">elementary-number-theory.divisibility-integers</a>
<a id="1543" class="Keyword">open</a> <a id="1548" class="Keyword">import</a> <a id="1555" href="elementary-number-theory.divisibility-natural-numbers.html" class="Module">elementary-number-theory.divisibility-natural-numbers</a>
<a id="1609" class="Keyword">open</a> <a id="1614" class="Keyword">import</a> <a id="1621" href="elementary-number-theory.divisibility-standard-finite-types.html" class="Module">elementary-number-theory.divisibility-standard-finite-types</a>
<a id="1681" class="Keyword">open</a> <a id="1686" class="Keyword">import</a> <a id="1693" href="elementary-number-theory.equality-integers.html" class="Module">elementary-number-theory.equality-integers</a>
<a id="1736" class="Keyword">open</a> <a id="1741" class="Keyword">import</a> <a id="1748" href="elementary-number-theory.equality-natural-numbers.html" class="Module">elementary-number-theory.equality-natural-numbers</a>
<a id="1798" class="Keyword">open</a> <a id="1803" class="Keyword">import</a> <a id="1810" href="elementary-number-theory.euclidean-division-natural-numbers.html" class="Module">elementary-number-theory.euclidean-division-natural-numbers</a>
<a id="1870" class="Keyword">open</a> <a id="1875" class="Keyword">import</a> <a id="1882" href="elementary-number-theory.eulers-totient-function.html" class="Module">elementary-number-theory.eulers-totient-function</a>
<a id="1931" class="Keyword">open</a> <a id="1936" class="Keyword">import</a> <a id="1943" href="elementary-number-theory.exponentiation-natural-numbers.html" class="Module">elementary-number-theory.exponentiation-natural-numbers</a>
<a id="1999" class="Keyword">open</a> <a id="2004" class="Keyword">import</a> <a id="2011" href="elementary-number-theory.factorials.html" class="Module">elementary-number-theory.factorials</a>
<a id="2047" class="Keyword">open</a> <a id="2052" class="Keyword">import</a> <a id="2059" href="elementary-number-theory.falling-factorials.html" class="Module">elementary-number-theory.falling-factorials</a>
<a id="2103" class="Keyword">open</a> <a id="2108" class="Keyword">import</a> <a id="2115" href="elementary-number-theory.fibonacci-sequence.html" class="Module">elementary-number-theory.fibonacci-sequence</a>
<a id="2159" class="Keyword">open</a> <a id="2164" class="Keyword">import</a> <a id="2171" href="elementary-number-theory.finitary-natural-numbers.html" class="Module">elementary-number-theory.finitary-natural-numbers</a>
<a id="2221" class="Keyword">open</a> <a id="2226" class="Keyword">import</a> <a id="2233" href="elementary-number-theory.finitely-cyclic-maps.html" class="Module">elementary-number-theory.finitely-cyclic-maps</a>
<a id="2279" class="Keyword">open</a> <a id="2284" class="Keyword">import</a> <a id="2291" href="elementary-number-theory.fractions.html" class="Module">elementary-number-theory.fractions</a>
<a id="2326" class="Keyword">open</a> <a id="2331" class="Keyword">import</a> <a id="2338" href="elementary-number-theory.goldbach-conjecture.html" class="Module">elementary-number-theory.goldbach-conjecture</a>
<a id="2383" class="Keyword">open</a> <a id="2388" class="Keyword">import</a> <a id="2395" href="elementary-number-theory.greatest-common-divisor-integers.html" class="Module">elementary-number-theory.greatest-common-divisor-integers</a>
<a id="2453" class="Keyword">open</a> <a id="2458" class="Keyword">import</a> <a id="2465" href="elementary-number-theory.greatest-common-divisor-natural-numbers.html" class="Module">elementary-number-theory.greatest-common-divisor-natural-numbers</a>
<a id="2530" class="Keyword">open</a> <a id="2535" class="Keyword">import</a> <a id="2542" href="elementary-number-theory.inequality-integers.html" class="Module">elementary-number-theory.inequality-integers</a>
<a id="2587" class="Keyword">open</a> <a id="2592" class="Keyword">import</a> <a id="2599" href="elementary-number-theory.inequality-natural-numbers.html" class="Module">elementary-number-theory.inequality-natural-numbers</a>
<a id="2651" class="Keyword">open</a> <a id="2656" class="Keyword">import</a> <a id="2663" href="elementary-number-theory.inequality-standard-finite-types.html" class="Module">elementary-number-theory.inequality-standard-finite-types</a>
<a id="2721" class="Keyword">open</a> <a id="2726" class="Keyword">import</a> <a id="2733" href="elementary-number-theory.infinitude-of-primes.html" class="Module">elementary-number-theory.infinitude-of-primes</a>
<a id="2779" class="Keyword">open</a> <a id="2784" class="Keyword">import</a> <a id="2791" href="elementary-number-theory.integers.html" class="Module">elementary-number-theory.integers</a>
<a id="2825" class="Keyword">open</a> <a id="2830" class="Keyword">import</a> <a id="2837" href="elementary-number-theory.iterating-functions.html" class="Module">elementary-number-theory.iterating-functions</a>
<a id="2882" class="Keyword">open</a> <a id="2887" class="Keyword">import</a> <a id="2894" href="elementary-number-theory.lower-bounds-natural-numbers.html" class="Module">elementary-number-theory.lower-bounds-natural-numbers</a>
<a id="2948" class="Keyword">open</a> <a id="2953" class="Keyword">import</a> <a id="2960" href="elementary-number-theory.modular-arithmetic-standard-finite-types.html" class="Module">elementary-number-theory.modular-arithmetic-standard-finite-types</a>
<a id="3026" class="Keyword">open</a> <a id="3031" class="Keyword">import</a> <a id="3038" href="elementary-number-theory.modular-arithmetic.html" class="Module">elementary-number-theory.modular-arithmetic</a>
<a id="3082" class="Keyword">open</a> <a id="3087" class="Keyword">import</a> <a id="3094" href="elementary-number-theory.multiplication-integers.html" class="Module">elementary-number-theory.multiplication-integers</a>
<a id="3143" class="Keyword">open</a> <a id="3148" class="Keyword">import</a> <a id="3155" href="elementary-number-theory.multiplication-natural-numbers.html" class="Module">elementary-number-theory.multiplication-natural-numbers</a>
<a id="3211" class="Keyword">open</a> <a id="3216" class="Keyword">import</a> <a id="3223" href="elementary-number-theory.natural-numbers.html" class="Module">elementary-number-theory.natural-numbers</a>
<a id="3264" class="Keyword">open</a> <a id="3269" class="Keyword">import</a> <a id="3276" href="elementary-number-theory.ordinal-induction-natural-numbers.html" class="Module">elementary-number-theory.ordinal-induction-natural-numbers</a>
<a id="3335" class="Keyword">open</a> <a id="3340" class="Keyword">import</a> <a id="3347" href="elementary-number-theory.prime-numbers.html" class="Module">elementary-number-theory.prime-numbers</a>
<a id="3386" class="Keyword">open</a> <a id="3391" class="Keyword">import</a> <a id="3398" href="elementary-number-theory.products-of-natural-numbers.html" class="Module">elementary-number-theory.products-of-natural-numbers</a>
<a id="3451" class="Keyword">open</a> <a id="3456" class="Keyword">import</a> <a id="3463" href="elementary-number-theory.proper-divisors-natural-numbers.html" class="Module">elementary-number-theory.proper-divisors-natural-numbers</a>
<a id="3520" class="Keyword">open</a> <a id="3525" class="Keyword">import</a> <a id="3532" href="elementary-number-theory.rational-numbers.html" class="Module">elementary-number-theory.rational-numbers</a>
<a id="3574" class="Keyword">open</a> <a id="3579" class="Keyword">import</a> <a id="3586" href="elementary-number-theory.relatively-prime-integers.html" class="Module">elementary-number-theory.relatively-prime-integers</a>
<a id="3637" class="Keyword">open</a> <a id="3642" class="Keyword">import</a> <a id="3649" href="elementary-number-theory.relatively-prime-natural-numbers.html" class="Module">elementary-number-theory.relatively-prime-natural-numbers</a>
<a id="3707" class="Keyword">open</a> <a id="3712" class="Keyword">import</a> <a id="3719" href="elementary-number-theory.repeating-element-standard-finite-type.html" class="Module">elementary-number-theory.repeating-element-standard-finite-type</a>
<a id="3783" class="Keyword">open</a> <a id="3788" class="Keyword">import</a> <a id="3795" href="elementary-number-theory.retracts-of-natural-numbers.html" class="Module">elementary-number-theory.retracts-of-natural-numbers</a>
<a id="3848" class="Keyword">open</a> <a id="3853" class="Keyword">import</a> <a id="3860" href="elementary-number-theory.retracts-of-standard-finite-types.html" class="Module">elementary-number-theory.retracts-of-standard-finite-types</a>
<a id="3919" class="Keyword">open</a> <a id="3924" class="Keyword">import</a> <a id="3931" href="elementary-number-theory.skipping-element-standard-finite-type.html" class="Module">elementary-number-theory.skipping-element-standard-finite-type</a>
<a id="3994" class="Keyword">open</a> <a id="3999" class="Keyword">import</a> <a id="4006" href="elementary-number-theory.stirling-numbers-of-the-second-kind.html" class="Module">elementary-number-theory.stirling-numbers-of-the-second-kind</a>
<a id="4067" class="Keyword">open</a> <a id="4072" class="Keyword">import</a> <a id="4079" href="elementary-number-theory.strong-induction-natural-numbers.html" class="Module">elementary-number-theory.strong-induction-natural-numbers</a>
<a id="4137" class="Keyword">open</a> <a id="4142" class="Keyword">import</a> <a id="4149" href="elementary-number-theory.sums-of-natural-numbers.html" class="Module">elementary-number-theory.sums-of-natural-numbers</a>
<a id="4198" class="Keyword">open</a> <a id="4203" class="Keyword">import</a> <a id="4210" href="elementary-number-theory.triangular-numbers.html" class="Module">elementary-number-theory.triangular-numbers</a>
<a id="4254" class="Keyword">open</a> <a id="4259" class="Keyword">import</a> <a id="4266" href="elementary-number-theory.twin-prime-conjecture.html" class="Module">elementary-number-theory.twin-prime-conjecture</a>
<a id="4313" class="Keyword">open</a> <a id="4318" class="Keyword">import</a> <a id="4325" href="elementary-number-theory.universal-property-natural-numbers.html" class="Module">elementary-number-theory.universal-property-natural-numbers</a>
<a id="4385" class="Keyword">open</a> <a id="4390" class="Keyword">import</a> <a id="4397" href="elementary-number-theory.upper-bounds-natural-numbers.html" class="Module">elementary-number-theory.upper-bounds-natural-numbers</a>
<a id="4451" class="Keyword">open</a> <a id="4456" class="Keyword">import</a> <a id="4463" href="elementary-number-theory.well-ordering-principle-natural-numbers.html" class="Module">elementary-number-theory.well-ordering-principle-natural-numbers</a>
<a id="4528" class="Keyword">open</a> <a id="4533" class="Keyword">import</a> <a id="4540" href="elementary-number-theory.well-ordering-principle-standard-finite-types.html" class="Module">elementary-number-theory.well-ordering-principle-standard-finite-types</a>
</pre>
## Finite groups

<pre class="Agda"><a id="4642" class="Keyword">open</a> <a id="4647" class="Keyword">import</a> <a id="4654" href="finite-groups.abstract-quaternion-group.html" class="Module">finite-groups.abstract-quaternion-group</a>
<a id="4694" class="Keyword">open</a> <a id="4699" class="Keyword">import</a> <a id="4706" href="finite-groups.concrete-quaternion-group.html" class="Module">finite-groups.concrete-quaternion-group</a>
<a id="4746" class="Keyword">open</a> <a id="4751" class="Keyword">import</a> <a id="4758" href="finite-groups.finite-groups.html" class="Module">finite-groups.finite-groups</a>
<a id="4786" class="Keyword">open</a> <a id="4791" class="Keyword">import</a> <a id="4798" href="finite-groups.orbits-permutations.html" class="Module">finite-groups.orbits-permutations</a>
<a id="4832" class="Keyword">open</a> <a id="4837" class="Keyword">import</a> <a id="4844" href="finite-groups.transpositions.html" class="Module">finite-groups.transpositions</a>
</pre>
## Foundation

<pre class="Agda"><a id="4901" class="Keyword">open</a> <a id="4906" class="Keyword">import</a> <a id="4913" href="foundation.html" class="Module">foundation</a>
<a id="4924" class="Keyword">open</a> <a id="4929" class="Keyword">import</a> <a id="4936" href="foundation.0-maps.html" class="Module">foundation.0-maps</a>
<a id="4954" class="Keyword">open</a> <a id="4959" class="Keyword">import</a> <a id="4966" href="foundation.1-types.html" class="Module">foundation.1-types</a>
<a id="4985" class="Keyword">open</a> <a id="4990" class="Keyword">import</a> <a id="4997" href="foundation.2-types.html" class="Module">foundation.2-types</a>
<a id="5016" class="Keyword">open</a> <a id="5021" class="Keyword">import</a> <a id="5028" href="foundation.algebras-polynomial-endofunctors.html" class="Module">foundation.algebras-polynomial-endofunctors</a>
<a id="5072" class="Keyword">open</a> <a id="5077" class="Keyword">import</a> <a id="5084" href="foundation.automorphisms.html" class="Module">foundation.automorphisms</a>
<a id="5109" class="Keyword">open</a> <a id="5114" class="Keyword">import</a> <a id="5121" href="foundation.axiom-of-choice.html" class="Module">foundation.axiom-of-choice</a>
<a id="5148" class="Keyword">open</a> <a id="5153" class="Keyword">import</a> <a id="5160" href="foundation.binary-embeddings.html" class="Module">foundation.binary-embeddings</a>
<a id="5189" class="Keyword">open</a> <a id="5194" class="Keyword">import</a> <a id="5201" href="foundation.binary-equivalences.html" class="Module">foundation.binary-equivalences</a>
<a id="5232" class="Keyword">open</a> <a id="5237" class="Keyword">import</a> <a id="5244" href="foundation.binary-relations.html" class="Module">foundation.binary-relations</a>
<a id="5272" class="Keyword">open</a> <a id="5277" class="Keyword">import</a> <a id="5284" href="foundation.boolean-reflection.html" class="Module">foundation.boolean-reflection</a>
<a id="5314" class="Keyword">open</a> <a id="5319" class="Keyword">import</a> <a id="5326" href="foundation.booleans.html" class="Module">foundation.booleans</a>
<a id="5346" class="Keyword">open</a> <a id="5351" class="Keyword">import</a> <a id="5358" href="foundation.cantors-diagonal-argument.html" class="Module">foundation.cantors-diagonal-argument</a>
<a id="5395" class="Keyword">open</a> <a id="5400" class="Keyword">import</a> <a id="5407" href="foundation.cartesian-product-types.html" class="Module">foundation.cartesian-product-types</a>
<a id="5442" class="Keyword">open</a> <a id="5447" class="Keyword">import</a> <a id="5454" href="foundation.choice-of-representatives-equivalence-relation.html" class="Module">foundation.choice-of-representatives-equivalence-relation</a>
<a id="5512" class="Keyword">open</a> <a id="5517" class="Keyword">import</a> <a id="5524" href="foundation.coherently-invertible-maps.html" class="Module">foundation.coherently-invertible-maps</a>
<a id="5562" class="Keyword">open</a> <a id="5567" class="Keyword">import</a> <a id="5574" href="foundation.commuting-squares.html" class="Module">foundation.commuting-squares</a>
<a id="5603" class="Keyword">open</a> <a id="5608" class="Keyword">import</a> <a id="5615" href="foundation.complements.html" class="Module">foundation.complements</a>
<a id="5638" class="Keyword">open</a> <a id="5643" class="Keyword">import</a> <a id="5650" href="foundation.conjunction.html" class="Module">foundation.conjunction</a>
<a id="5673" class="Keyword">open</a> <a id="5678" class="Keyword">import</a> <a id="5685" href="foundation.connected-components-universes.html" class="Module">foundation.connected-components-universes</a>
<a id="5727" class="Keyword">open</a> <a id="5732" class="Keyword">import</a> <a id="5739" href="foundation.connected-components.html" class="Module">foundation.connected-components</a>
<a id="5771" class="Keyword">open</a> <a id="5776" class="Keyword">import</a> <a id="5783" href="foundation.connected-types.html" class="Module">foundation.connected-types</a>
<a id="5810" class="Keyword">open</a> <a id="5815" class="Keyword">import</a> <a id="5822" href="foundation.constant-maps.html" class="Module">foundation.constant-maps</a>
<a id="5847" class="Keyword">open</a> <a id="5852" class="Keyword">import</a> <a id="5859" href="foundation.contractible-maps.html" class="Module">foundation.contractible-maps</a>
<a id="5888" class="Keyword">open</a> <a id="5893" class="Keyword">import</a> <a id="5900" href="foundation.contractible-types.html" class="Module">foundation.contractible-types</a>
<a id="5930" class="Keyword">open</a> <a id="5935" class="Keyword">import</a> <a id="5942" href="foundation.coproduct-types.html" class="Module">foundation.coproduct-types</a>
<a id="5969" class="Keyword">open</a> <a id="5974" class="Keyword">import</a> <a id="5981" href="foundation.coslice.html" class="Module">foundation.coslice</a>
<a id="6000" class="Keyword">open</a> <a id="6005" class="Keyword">import</a> <a id="6012" href="foundation.decidable-dependent-function-types.html" class="Module">foundation.decidable-dependent-function-types</a>
<a id="6058" class="Keyword">open</a> <a id="6063" class="Keyword">import</a> <a id="6070" href="foundation.decidable-dependent-pair-types.html" class="Module">foundation.decidable-dependent-pair-types</a>
<a id="6112" class="Keyword">open</a> <a id="6117" class="Keyword">import</a> <a id="6124" href="foundation.decidable-embeddings.html" class="Module">foundation.decidable-embeddings</a>
<a id="6156" class="Keyword">open</a> <a id="6161" class="Keyword">import</a> <a id="6168" href="foundation.decidable-equality.html" class="Module">foundation.decidable-equality</a>
<a id="6198" class="Keyword">open</a> <a id="6203" class="Keyword">import</a> <a id="6210" href="foundation.decidable-maps.html" class="Module">foundation.decidable-maps</a>
<a id="6236" class="Keyword">open</a> <a id="6241" class="Keyword">import</a> <a id="6248" href="foundation.decidable-propositions.html" class="Module">foundation.decidable-propositions</a>
<a id="6282" class="Keyword">open</a> <a id="6287" class="Keyword">import</a> <a id="6294" href="foundation.decidable-subtypes.html" class="Module">foundation.decidable-subtypes</a>
<a id="6324" class="Keyword">open</a> <a id="6329" class="Keyword">import</a> <a id="6336" href="foundation.decidable-types.html" class="Module">foundation.decidable-types</a>
<a id="6363" class="Keyword">open</a> <a id="6368" class="Keyword">import</a> <a id="6375" href="foundation.dependent-pair-types.html" class="Module">foundation.dependent-pair-types</a>
<a id="6407" class="Keyword">open</a> <a id="6412" class="Keyword">import</a> <a id="6419" href="foundation.diagonal-maps-of-types.html" class="Module">foundation.diagonal-maps-of-types</a>
<a id="6453" class="Keyword">open</a> <a id="6458" class="Keyword">import</a> <a id="6465" href="foundation.disjunction.html" class="Module">foundation.disjunction</a>
<a id="6488" class="Keyword">open</a> <a id="6493" class="Keyword">import</a> <a id="6500" href="foundation.distributivity-of-dependent-functions-over-coproduct-types.html" class="Module">foundation.distributivity-of-dependent-functions-over-coproduct-types</a>
<a id="6570" class="Keyword">open</a> <a id="6575" class="Keyword">import</a> <a id="6582" href="foundation.distributivity-of-dependent-functions-over-dependent-pairs.html" class="Module">foundation.distributivity-of-dependent-functions-over-dependent-pairs</a>
<a id="6652" class="Keyword">open</a> <a id="6657" class="Keyword">import</a> <a id="6664" href="foundation.double-negation.html" class="Module">foundation.double-negation</a>
<a id="6691" class="Keyword">open</a> <a id="6696" class="Keyword">import</a> <a id="6703" href="foundation.effective-maps-equivalence-relations.html" class="Module">foundation.effective-maps-equivalence-relations</a>
<a id="6751" class="Keyword">open</a> <a id="6756" class="Keyword">import</a> <a id="6763" href="foundation.elementhood-relation-w-types.html" class="Module">foundation.elementhood-relation-w-types</a>
<a id="6803" class="Keyword">open</a> <a id="6808" class="Keyword">import</a> <a id="6815" href="foundation.embeddings.html" class="Module">foundation.embeddings</a>
<a id="6837" class="Keyword">open</a> <a id="6842" class="Keyword">import</a> <a id="6849" href="foundation.empty-types.html" class="Module">foundation.empty-types</a>
<a id="6872" class="Keyword">open</a> <a id="6877" class="Keyword">import</a> <a id="6884" href="foundation.epimorphisms-with-respect-to-sets.html" class="Module">foundation.epimorphisms-with-respect-to-sets</a>
<a id="6929" class="Keyword">open</a> <a id="6934" class="Keyword">import</a> <a id="6941" href="foundation.equality-cartesian-product-types.html" class="Module">foundation.equality-cartesian-product-types</a>
<a id="6985" class="Keyword">open</a> <a id="6990" class="Keyword">import</a> <a id="6997" href="foundation.equality-coproduct-types.html" class="Module">foundation.equality-coproduct-types</a>
<a id="7033" class="Keyword">open</a> <a id="7038" class="Keyword">import</a> <a id="7045" href="foundation.equality-dependent-function-types.html" class="Module">foundation.equality-dependent-function-types</a>
<a id="7090" class="Keyword">open</a> <a id="7095" class="Keyword">import</a> <a id="7102" href="foundation.equality-dependent-pair-types.html" class="Module">foundation.equality-dependent-pair-types</a>
<a id="7143" class="Keyword">open</a> <a id="7148" class="Keyword">import</a> <a id="7155" href="foundation.equality-fibers-of-maps.html" class="Module">foundation.equality-fibers-of-maps</a>
<a id="7190" class="Keyword">open</a> <a id="7195" class="Keyword">import</a> <a id="7202" href="foundation.equivalence-classes.html" class="Module">foundation.equivalence-classes</a>
<a id="7233" class="Keyword">open</a> <a id="7238" class="Keyword">import</a> <a id="7245" href="foundation.equivalence-induction.html" class="Module">foundation.equivalence-induction</a>
<a id="7278" class="Keyword">open</a> <a id="7283" class="Keyword">import</a> <a id="7290" href="foundation.equivalence-relations.html" class="Module">foundation.equivalence-relations</a>
<a id="7323" class="Keyword">open</a> <a id="7328" class="Keyword">import</a> <a id="7335" href="foundation.equivalences-maybe.html" class="Module">foundation.equivalences-maybe</a>
<a id="7365" class="Keyword">open</a> <a id="7370" class="Keyword">import</a> <a id="7377" href="foundation.equivalences.html" class="Module">foundation.equivalences</a>
<a id="7401" class="Keyword">open</a> <a id="7406" class="Keyword">import</a> <a id="7413" href="foundation.existential-quantification.html" class="Module">foundation.existential-quantification</a>
<a id="7451" class="Keyword">open</a> <a id="7456" class="Keyword">import</a> <a id="7463" href="foundation.extensional-w-types.html" class="Module">foundation.extensional-w-types</a>
<a id="7494" class="Keyword">open</a> <a id="7499" class="Keyword">import</a> <a id="7506" href="foundation.faithful-maps.html" class="Module">foundation.faithful-maps</a>
<a id="7531" class="Keyword">open</a> <a id="7536" class="Keyword">import</a> <a id="7543" href="foundation.fiber-inclusions.html" class="Module">foundation.fiber-inclusions</a>
<a id="7571" class="Keyword">open</a> <a id="7576" class="Keyword">import</a> <a id="7583" href="foundation.fibered-maps.html" class="Module">foundation.fibered-maps</a>
<a id="7607" class="Keyword">open</a> <a id="7612" class="Keyword">import</a> <a id="7619" href="foundation.fibers-of-maps.html" class="Module">foundation.fibers-of-maps</a>
<a id="7645" class="Keyword">open</a> <a id="7650" class="Keyword">import</a> <a id="7657" href="foundation.function-extensionality.html" class="Module">foundation.function-extensionality</a>
<a id="7692" class="Keyword">open</a> <a id="7697" class="Keyword">import</a> <a id="7704" href="foundation.functions.html" class="Module">foundation.functions</a>
<a id="7725" class="Keyword">open</a> <a id="7730" class="Keyword">import</a> <a id="7737" href="foundation.functoriality-cartesian-product-types.html" class="Module">foundation.functoriality-cartesian-product-types</a>
<a id="7786" class="Keyword">open</a> <a id="7791" class="Keyword">import</a> <a id="7798" href="foundation.functoriality-coproduct-types.html" class="Module">foundation.functoriality-coproduct-types</a>
<a id="7839" class="Keyword">open</a> <a id="7844" class="Keyword">import</a> <a id="7851" href="foundation.functoriality-dependent-function-types.html" class="Module">foundation.functoriality-dependent-function-types</a>
<a id="7901" class="Keyword">open</a> <a id="7906" class="Keyword">import</a> <a id="7913" href="foundation.functoriality-dependent-pair-types.html" class="Module">foundation.functoriality-dependent-pair-types</a>
<a id="7959" class="Keyword">open</a> <a id="7964" class="Keyword">import</a> <a id="7971" href="foundation.functoriality-function-types.html" class="Module">foundation.functoriality-function-types</a>
<a id="8011" class="Keyword">open</a> <a id="8016" class="Keyword">import</a> <a id="8023" href="foundation.functoriality-propositional-truncation.html" class="Module">foundation.functoriality-propositional-truncation</a>
<a id="8073" class="Keyword">open</a> <a id="8078" class="Keyword">import</a> <a id="8085" href="foundation.functoriality-set-quotients.html" class="Module">foundation.functoriality-set-quotients</a>
<a id="8124" class="Keyword">open</a> <a id="8129" class="Keyword">import</a> <a id="8136" href="foundation.functoriality-set-truncation.html" class="Module">foundation.functoriality-set-truncation</a>
<a id="8176" class="Keyword">open</a> <a id="8181" class="Keyword">import</a> <a id="8188" href="foundation.functoriality-w-types.html" class="Module">foundation.functoriality-w-types</a>
<a id="8221" class="Keyword">open</a> <a id="8226" class="Keyword">import</a> <a id="8233" href="foundation.fundamental-theorem-of-identity-types.html" class="Module">foundation.fundamental-theorem-of-identity-types</a>
<a id="8282" class="Keyword">open</a> <a id="8287" class="Keyword">import</a> <a id="8294" href="foundation.global-choice.html" class="Module">foundation.global-choice</a>
<a id="8319" class="Keyword">open</a> <a id="8324" class="Keyword">import</a> <a id="8331" href="foundation.homotopies.html" class="Module">foundation.homotopies</a>
<a id="8353" class="Keyword">open</a> <a id="8358" class="Keyword">import</a> <a id="8365" href="foundation.identity-systems.html" class="Module">foundation.identity-systems</a>
<a id="8393" class="Keyword">open</a> <a id="8398" class="Keyword">import</a> <a id="8405" href="foundation.identity-types.html" class="Module">foundation.identity-types</a>
<a id="8431" class="Keyword">open</a> <a id="8436" class="Keyword">import</a> <a id="8443" href="foundation.images.html" class="Module">foundation.images</a>
<a id="8461" class="Keyword">open</a> <a id="8466" class="Keyword">import</a> <a id="8473" href="foundation.impredicative-encodings.html" class="Module">foundation.impredicative-encodings</a>
<a id="8508" class="Keyword">open</a> <a id="8513" class="Keyword">import</a> <a id="8520" href="foundation.indexed-w-types.html" class="Module">foundation.indexed-w-types</a>
<a id="8547" class="Keyword">open</a> <a id="8552" class="Keyword">import</a> <a id="8559" href="foundation.induction-principle-propositional-truncation.html" class="Module">foundation.induction-principle-propositional-truncation</a>
<a id="8615" class="Keyword">open</a> <a id="8620" class="Keyword">import</a> <a id="8627" href="foundation.induction-w-types.html" class="Module">foundation.induction-w-types</a>
<a id="8656" class="Keyword">open</a> <a id="8661" class="Keyword">import</a> <a id="8668" href="foundation.inequality-w-types.html" class="Module">foundation.inequality-w-types</a>
<a id="8698" class="Keyword">open</a> <a id="8703" class="Keyword">import</a> <a id="8710" href="foundation.injective-maps.html" class="Module">foundation.injective-maps</a>
<a id="8736" class="Keyword">open</a> <a id="8741" class="Keyword">import</a> <a id="8748" href="foundation.interchange-law.html" class="Module">foundation.interchange-law</a>
<a id="8775" class="Keyword">open</a> <a id="8780" class="Keyword">import</a> <a id="8787" href="foundation.involutions.html" class="Module">foundation.involutions</a>
<a id="8810" class="Keyword">open</a> <a id="8815" class="Keyword">import</a> <a id="8822" href="foundation.isolated-points.html" class="Module">foundation.isolated-points</a>
<a id="8849" class="Keyword">open</a> <a id="8854" class="Keyword">import</a> <a id="8861" href="foundation.isomorphisms-of-sets.html" class="Module">foundation.isomorphisms-of-sets</a>
<a id="8893" class="Keyword">open</a> <a id="8898" class="Keyword">import</a> <a id="8905" href="foundation.law-of-excluded-middle.html" class="Module">foundation.law-of-excluded-middle</a>
<a id="8939" class="Keyword">open</a> <a id="8944" class="Keyword">import</a> <a id="8951" href="foundation.lawveres-fixed-point-theorem.html" class="Module">foundation.lawveres-fixed-point-theorem</a>
<a id="8991" class="Keyword">open</a> <a id="8996" class="Keyword">import</a> <a id="9003" href="foundation.locally-small-types.html" class="Module">foundation.locally-small-types</a>
<a id="9034" class="Keyword">open</a> <a id="9039" class="Keyword">import</a> <a id="9046" href="foundation.logical-equivalences.html" class="Module">foundation.logical-equivalences</a>
<a id="9078" class="Keyword">open</a> <a id="9083" class="Keyword">import</a> <a id="9090" href="foundation.maybe.html" class="Module">foundation.maybe</a>
<a id="9107" class="Keyword">open</a> <a id="9112" class="Keyword">import</a> <a id="9119" href="foundation.mere-equality.html" class="Module">foundation.mere-equality</a>
<a id="9144" class="Keyword">open</a> <a id="9149" class="Keyword">import</a> <a id="9156" href="foundation.mere-equivalences.html" class="Module">foundation.mere-equivalences</a>
<a id="9185" class="Keyword">open</a> <a id="9190" class="Keyword">import</a> <a id="9197" href="foundation.monomorphisms.html" class="Module">foundation.monomorphisms</a>
<a id="9222" class="Keyword">open</a> <a id="9227" class="Keyword">import</a> <a id="9234" href="foundation.multisets.html" class="Module">foundation.multisets</a>
<a id="9255" class="Keyword">open</a> <a id="9260" class="Keyword">import</a> <a id="9267" href="foundation.negation.html" class="Module">foundation.negation</a>
<a id="9287" class="Keyword">open</a> <a id="9292" class="Keyword">import</a> <a id="9299" href="foundation.non-contractible-types.html" class="Module">foundation.non-contractible-types</a>
<a id="9333" class="Keyword">open</a> <a id="9338" class="Keyword">import</a> <a id="9345" href="foundation.path-algebra.html" class="Module">foundation.path-algebra</a>
<a id="9369" class="Keyword">open</a> <a id="9374" class="Keyword">import</a> <a id="9381" href="foundation.path-split-maps.html" class="Module">foundation.path-split-maps</a>
<a id="9408" class="Keyword">open</a> <a id="9413" class="Keyword">import</a> <a id="9420" href="foundation.polynomial-endofunctors.html" class="Module">foundation.polynomial-endofunctors</a>
<a id="9455" class="Keyword">open</a> <a id="9460" class="Keyword">import</a> <a id="9467" href="foundation.propositional-extensionality.html" class="Module">foundation.propositional-extensionality</a>
<a id="9507" class="Keyword">open</a> <a id="9512" class="Keyword">import</a> <a id="9519" href="foundation.propositional-maps.html" class="Module">foundation.propositional-maps</a>
<a id="9549" class="Keyword">open</a> <a id="9554" class="Keyword">import</a> <a id="9561" href="foundation.propositional-truncations.html" class="Module">foundation.propositional-truncations</a>
<a id="9598" class="Keyword">open</a> <a id="9603" class="Keyword">import</a> <a id="9610" href="foundation.propositions.html" class="Module">foundation.propositions</a>
<a id="9634" class="Keyword">open</a> <a id="9639" class="Keyword">import</a> <a id="9646" href="foundation.pullbacks.html" class="Module">foundation.pullbacks</a>
<a id="9667" class="Keyword">open</a> <a id="9672" class="Keyword">import</a> <a id="9679" href="foundation.raising-universe-levels.html" class="Module">foundation.raising-universe-levels</a>
<a id="9714" class="Keyword">open</a> <a id="9719" class="Keyword">import</a> <a id="9726" href="foundation.ranks-of-elements-w-types.html" class="Module">foundation.ranks-of-elements-w-types</a>
<a id="9763" class="Keyword">open</a> <a id="9768" class="Keyword">import</a> <a id="9775" href="foundation.reflecting-maps-equivalence-relations.html" class="Module">foundation.reflecting-maps-equivalence-relations</a>
<a id="9824" class="Keyword">open</a> <a id="9829" class="Keyword">import</a> <a id="9836" href="foundation.replacement.html" class="Module">foundation.replacement</a>
<a id="9859" class="Keyword">open</a> <a id="9864" class="Keyword">import</a> <a id="9871" href="foundation.retractions.html" class="Module">foundation.retractions</a>
<a id="9894" class="Keyword">open</a> <a id="9899" class="Keyword">import</a> <a id="9906" href="foundation.russells-paradox.html" class="Module">foundation.russells-paradox</a>
<a id="9934" class="Keyword">open</a> <a id="9939" class="Keyword">import</a> <a id="9946" href="foundation.sections.html" class="Module">foundation.sections</a>
<a id="9966" class="Keyword">open</a> <a id="9971" class="Keyword">import</a> <a id="9978" href="foundation.set-presented-types.html" class="Module">foundation.set-presented-types</a>
<a id="10009" class="Keyword">open</a> <a id="10014" class="Keyword">import</a> <a id="10021" href="foundation.set-truncations.html" class="Module">foundation.set-truncations</a>
<a id="10048" class="Keyword">open</a> <a id="10053" class="Keyword">import</a> <a id="10060" href="foundation.sets.html" class="Module">foundation.sets</a>
<a id="10076" class="Keyword">open</a> <a id="10081" class="Keyword">import</a> <a id="10088" href="foundation.singleton-induction.html" class="Module">foundation.singleton-induction</a>
<a id="10119" class="Keyword">open</a> <a id="10124" class="Keyword">import</a> <a id="10131" href="foundation.slice.html" class="Module">foundation.slice</a>
<a id="10148" class="Keyword">open</a> <a id="10153" class="Keyword">import</a> <a id="10160" href="foundation.small-maps.html" class="Module">foundation.small-maps</a>
<a id="10182" class="Keyword">open</a> <a id="10187" class="Keyword">import</a> <a id="10194" href="foundation.small-multisets.html" class="Module">foundation.small-multisets</a>
<a id="10221" class="Keyword">open</a> <a id="10226" class="Keyword">import</a> <a id="10233" href="foundation.small-types.html" class="Module">foundation.small-types</a>
<a id="10256" class="Keyword">open</a> <a id="10261" class="Keyword">import</a> <a id="10268" href="foundation.small-universes.html" class="Module">foundation.small-universes</a>
<a id="10295" class="Keyword">open</a> <a id="10300" class="Keyword">import</a> <a id="10307" href="foundation.split-surjective-maps.html" class="Module">foundation.split-surjective-maps</a>
<a id="10340" class="Keyword">open</a> <a id="10345" class="Keyword">import</a> <a id="10352" href="foundation.structure-identity-principle.html" class="Module">foundation.structure-identity-principle</a>
<a id="10392" class="Keyword">open</a> <a id="10397" class="Keyword">import</a> <a id="10404" href="foundation.structure.html" class="Module">foundation.structure</a>
<a id="10425" class="Keyword">open</a> <a id="10430" class="Keyword">import</a> <a id="10437" href="foundation.subterminal-types.html" class="Module">foundation.subterminal-types</a>
<a id="10466" class="Keyword">open</a> <a id="10471" class="Keyword">import</a> <a id="10478" href="foundation.subtype-identity-principle.html" class="Module">foundation.subtype-identity-principle</a>
<a id="10516" class="Keyword">open</a> <a id="10521" class="Keyword">import</a> <a id="10528" href="foundation.subtypes.html" class="Module">foundation.subtypes</a>
<a id="10548" class="Keyword">open</a> <a id="10553" class="Keyword">import</a> <a id="10560" href="foundation.subuniverses.html" class="Module">foundation.subuniverses</a>
<a id="10584" class="Keyword">open</a> <a id="10589" class="Keyword">import</a> <a id="10596" href="foundation.surjective-maps.html" class="Module">foundation.surjective-maps</a>
<a id="10623" class="Keyword">open</a> <a id="10628" class="Keyword">import</a> <a id="10635" href="foundation.truncated-maps.html" class="Module">foundation.truncated-maps</a>
<a id="10661" class="Keyword">open</a> <a id="10666" class="Keyword">import</a> <a id="10673" href="foundation.truncated-types.html" class="Module">foundation.truncated-types</a>
<a id="10700" class="Keyword">open</a> <a id="10705" class="Keyword">import</a> <a id="10712" href="foundation.truncation-levels.html" class="Module">foundation.truncation-levels</a>
<a id="10741" class="Keyword">open</a> <a id="10746" class="Keyword">import</a> <a id="10753" href="foundation.truncations.html" class="Module">foundation.truncations</a>
<a id="10776" class="Keyword">open</a> <a id="10781" class="Keyword">import</a> <a id="10788" href="foundation.type-arithmetic-cartesian-product-types.html" class="Module">foundation.type-arithmetic-cartesian-product-types</a>
<a id="10839" class="Keyword">open</a> <a id="10844" class="Keyword">import</a> <a id="10851" href="foundation.type-arithmetic-coproduct-types.html" class="Module">foundation.type-arithmetic-coproduct-types</a>
<a id="10894" class="Keyword">open</a> <a id="10899" class="Keyword">import</a> <a id="10906" href="foundation.type-arithmetic-dependent-pair-types.html" class="Module">foundation.type-arithmetic-dependent-pair-types</a>
<a id="10954" class="Keyword">open</a> <a id="10959" class="Keyword">import</a> <a id="10966" href="foundation.type-arithmetic-empty-type.html" class="Module">foundation.type-arithmetic-empty-type</a>
<a id="11004" class="Keyword">open</a> <a id="11009" class="Keyword">import</a> <a id="11016" href="foundation.type-arithmetic-unit-type.html" class="Module">foundation.type-arithmetic-unit-type</a>
<a id="11053" class="Keyword">open</a> <a id="11058" class="Keyword">import</a> <a id="11065" href="foundation.uniqueness-image.html" class="Module">foundation.uniqueness-image</a>
<a id="11093" class="Keyword">open</a> <a id="11098" class="Keyword">import</a> <a id="11105" href="foundation.uniqueness-set-quotients.html" class="Module">foundation.uniqueness-set-quotients</a>
<a id="11141" class="Keyword">open</a> <a id="11146" class="Keyword">import</a> <a id="11153" href="foundation.uniqueness-set-truncations.html" class="Module">foundation.uniqueness-set-truncations</a>
<a id="11191" class="Keyword">open</a> <a id="11196" class="Keyword">import</a> <a id="11203" href="foundation.uniqueness-truncation.html" class="Module">foundation.uniqueness-truncation</a>
<a id="11236" class="Keyword">open</a> <a id="11241" class="Keyword">import</a> <a id="11248" href="foundation.unit-type.html" class="Module">foundation.unit-type</a>
<a id="11269" class="Keyword">open</a> <a id="11274" class="Keyword">import</a> <a id="11281" href="foundation.univalence-implies-function-extensionality.html" class="Module">foundation.univalence-implies-function-extensionality</a>
<a id="11335" class="Keyword">open</a> <a id="11340" class="Keyword">import</a> <a id="11347" href="foundation.univalence.html" class="Module">foundation.univalence</a>
<a id="11369" class="Keyword">open</a> <a id="11374" class="Keyword">import</a> <a id="11381" href="foundation.univalent-type-families.html" class="Module">foundation.univalent-type-families</a>
<a id="11416" class="Keyword">open</a> <a id="11421" class="Keyword">import</a> <a id="11428" href="foundation.universal-multiset.html" class="Module">foundation.universal-multiset</a>
<a id="11458" class="Keyword">open</a> <a id="11463" class="Keyword">import</a> <a id="11470" href="foundation.universal-property-booleans.html" class="Module">foundation.universal-property-booleans</a>
<a id="11509" class="Keyword">open</a> <a id="11514" class="Keyword">import</a> <a id="11521" href="foundation.universal-property-cartesian-product-types.html" class="Module">foundation.universal-property-cartesian-product-types</a>
<a id="11575" class="Keyword">open</a> <a id="11580" class="Keyword">import</a> <a id="11587" href="foundation.universal-property-coproduct-types.html" class="Module">foundation.universal-property-coproduct-types</a>
<a id="11633" class="Keyword">open</a> <a id="11638" class="Keyword">import</a> <a id="11645" href="foundation.universal-property-dependent-pair-types.html" class="Module">foundation.universal-property-dependent-pair-types</a>
<a id="11696" class="Keyword">open</a> <a id="11701" class="Keyword">import</a> <a id="11708" href="foundation.universal-property-empty-type.html" class="Module">foundation.universal-property-empty-type</a>
<a id="11749" class="Keyword">open</a> <a id="11754" class="Keyword">import</a> <a id="11761" href="foundation.universal-property-fiber-products.html" class="Module">foundation.universal-property-fiber-products</a>
<a id="11806" class="Keyword">open</a> <a id="11811" class="Keyword">import</a> <a id="11818" href="foundation.universal-property-identity-types.html" class="Module">foundation.universal-property-identity-types</a>
<a id="11863" class="Keyword">open</a> <a id="11868" class="Keyword">import</a> <a id="11875" href="foundation.universal-property-image.html" class="Module">foundation.universal-property-image</a>
<a id="11911" class="Keyword">open</a> <a id="11916" class="Keyword">import</a> <a id="11923" href="foundation.universal-property-maybe.html" class="Module">foundation.universal-property-maybe</a>
<a id="11959" class="Keyword">open</a> <a id="11964" class="Keyword">import</a> <a id="11971" href="foundation.universal-property-propositional-truncation-into-sets.html" class="Module">foundation.universal-property-propositional-truncation-into-sets</a>
<a id="12036" class="Keyword">open</a> <a id="12041" class="Keyword">import</a> <a id="12048" href="foundation.universal-property-propositional-truncation.html" class="Module">foundation.universal-property-propositional-truncation</a>
<a id="12103" class="Keyword">open</a> <a id="12108" class="Keyword">import</a> <a id="12115" href="foundation.universal-property-pullbacks.html" class="Module">foundation.universal-property-pullbacks</a>
<a id="12155" class="Keyword">open</a> <a id="12160" class="Keyword">import</a> <a id="12167" href="foundation.universal-property-set-quotients.html" class="Module">foundation.universal-property-set-quotients</a>
<a id="12211" class="Keyword">open</a> <a id="12216" class="Keyword">import</a> <a id="12223" href="foundation.universal-property-set-truncation.html" class="Module">foundation.universal-property-set-truncation</a>
<a id="12268" class="Keyword">open</a> <a id="12273" class="Keyword">import</a> <a id="12280" href="foundation.universal-property-truncation.html" class="Module">foundation.universal-property-truncation</a>
<a id="12321" class="Keyword">open</a> <a id="12326" class="Keyword">import</a> <a id="12333" href="foundation.universal-property-unit-type.html" class="Module">foundation.universal-property-unit-type</a>
<a id="12373" class="Keyword">open</a> <a id="12378" class="Keyword">import</a> <a id="12385" href="foundation.universe-levels.html" class="Module">foundation.universe-levels</a>
<a id="12412" class="Keyword">open</a> <a id="12417" class="Keyword">import</a> <a id="12424" href="foundation.unordered-pairs.html" class="Module">foundation.unordered-pairs</a>
<a id="12451" class="Keyword">open</a> <a id="12456" class="Keyword">import</a> <a id="12463" href="foundation.w-types.html" class="Module">foundation.w-types</a>
<a id="12482" class="Keyword">open</a> <a id="12487" class="Keyword">import</a> <a id="12494" href="foundation.weak-function-extensionality.html" class="Module">foundation.weak-function-extensionality</a>
<a id="12534" class="Keyword">open</a> <a id="12539" class="Keyword">import</a> <a id="12546" href="foundation.weakly-constant-maps.html" class="Module">foundation.weakly-constant-maps</a>
</pre>
## Foundation Core

<pre class="Agda"><a id="12611" class="Keyword">open</a> <a id="12616" class="Keyword">import</a> <a id="12623" href="foundation-core.0-maps.html" class="Module">foundation-core.0-maps</a>
<a id="12646" class="Keyword">open</a> <a id="12651" class="Keyword">import</a> <a id="12658" href="foundation-core.1-types.html" class="Module">foundation-core.1-types</a>
<a id="12682" class="Keyword">open</a> <a id="12687" class="Keyword">import</a> <a id="12694" href="foundation-core.cartesian-product-types.html" class="Module">foundation-core.cartesian-product-types</a>
<a id="12734" class="Keyword">open</a> <a id="12739" class="Keyword">import</a> <a id="12746" href="foundation-core.coherently-invertible-maps.html" class="Module">foundation-core.coherently-invertible-maps</a>
<a id="12789" class="Keyword">open</a> <a id="12794" class="Keyword">import</a> <a id="12801" href="foundation-core.commuting-squares.html" class="Module">foundation-core.commuting-squares</a>
<a id="12835" class="Keyword">open</a> <a id="12840" class="Keyword">import</a> <a id="12847" href="foundation-core.constant-maps.html" class="Module">foundation-core.constant-maps</a>
<a id="12877" class="Keyword">open</a> <a id="12882" class="Keyword">import</a> <a id="12889" href="foundation-core.contractible-maps.html" class="Module">foundation-core.contractible-maps</a>
<a id="12923" class="Keyword">open</a> <a id="12928" class="Keyword">import</a> <a id="12935" href="foundation-core.contractible-types.html" class="Module">foundation-core.contractible-types</a>
<a id="12970" class="Keyword">open</a> <a id="12975" class="Keyword">import</a> <a id="12982" href="foundation-core.dependent-pair-types.html" class="Module">foundation-core.dependent-pair-types</a>
<a id="13019" class="Keyword">open</a> <a id="13024" class="Keyword">import</a> <a id="13031" href="foundation-core.embeddings.html" class="Module">foundation-core.embeddings</a>
<a id="13058" class="Keyword">open</a> <a id="13063" class="Keyword">import</a> <a id="13070" href="foundation-core.empty-types.html" class="Module">foundation-core.empty-types</a>
<a id="13098" class="Keyword">open</a> <a id="13103" class="Keyword">import</a> <a id="13110" href="foundation-core.equality-cartesian-product-types.html" class="Module">foundation-core.equality-cartesian-product-types</a>
<a id="13159" class="Keyword">open</a> <a id="13164" class="Keyword">import</a> <a id="13171" href="foundation-core.equality-dependent-pair-types.html" class="Module">foundation-core.equality-dependent-pair-types</a>
<a id="13217" class="Keyword">open</a> <a id="13222" class="Keyword">import</a> <a id="13229" href="foundation-core.equality-fibers-of-maps.html" class="Module">foundation-core.equality-fibers-of-maps</a>
<a id="13269" class="Keyword">open</a> <a id="13274" class="Keyword">import</a> <a id="13281" href="foundation-core.equivalence-induction.html" class="Module">foundation-core.equivalence-induction</a>
<a id="13319" class="Keyword">open</a> <a id="13324" class="Keyword">import</a> <a id="13331" href="foundation-core.equivalences.html" class="Module">foundation-core.equivalences</a>
<a id="13360" class="Keyword">open</a> <a id="13365" class="Keyword">import</a> <a id="13372" href="foundation-core.faithful-maps.html" class="Module">foundation-core.faithful-maps</a>
<a id="13402" class="Keyword">open</a> <a id="13407" class="Keyword">import</a> <a id="13414" href="foundation-core.fibers-of-maps.html" class="Module">foundation-core.fibers-of-maps</a>
<a id="13445" class="Keyword">open</a> <a id="13450" class="Keyword">import</a> <a id="13457" href="foundation-core.functions.html" class="Module">foundation-core.functions</a>
<a id="13483" class="Keyword">open</a> <a id="13488" class="Keyword">import</a> <a id="13495" href="foundation-core.functoriality-dependent-pair-types.html" class="Module">foundation-core.functoriality-dependent-pair-types</a>
<a id="13546" class="Keyword">open</a> <a id="13551" class="Keyword">import</a> <a id="13558" href="foundation-core.fundamental-theorem-of-identity-types.html" class="Module">foundation-core.fundamental-theorem-of-identity-types</a>
<a id="13612" class="Keyword">open</a> <a id="13617" class="Keyword">import</a> <a id="13624" href="foundation-core.homotopies.html" class="Module">foundation-core.homotopies</a>
<a id="13651" class="Keyword">open</a> <a id="13656" class="Keyword">import</a> <a id="13663" href="foundation-core.identity-systems.html" class="Module">foundation-core.identity-systems</a>
<a id="13696" class="Keyword">open</a> <a id="13701" class="Keyword">import</a> <a id="13708" href="foundation-core.identity-types.html" class="Module">foundation-core.identity-types</a>
<a id="13739" class="Keyword">open</a> <a id="13744" class="Keyword">import</a> <a id="13751" href="foundation-core.logical-equivalences.html" class="Module">foundation-core.logical-equivalences</a>
<a id="13788" class="Keyword">open</a> <a id="13793" class="Keyword">import</a> <a id="13800" href="foundation-core.negation.html" class="Module">foundation-core.negation</a>
<a id="13825" class="Keyword">open</a> <a id="13830" class="Keyword">import</a> <a id="13837" href="foundation-core.path-split-maps.html" class="Module">foundation-core.path-split-maps</a>
<a id="13869" class="Keyword">open</a> <a id="13874" class="Keyword">import</a> <a id="13881" href="foundation-core.propositional-maps.html" class="Module">foundation-core.propositional-maps</a>
<a id="13916" class="Keyword">open</a> <a id="13921" class="Keyword">import</a> <a id="13928" href="foundation-core.propositions.html" class="Module">foundation-core.propositions</a>
<a id="13957" class="Keyword">open</a> <a id="13962" class="Keyword">import</a> <a id="13969" href="foundation-core.retractions.html" class="Module">foundation-core.retractions</a>
<a id="13997" class="Keyword">open</a> <a id="14002" class="Keyword">import</a> <a id="14009" href="foundation-core.sections.html" class="Module">foundation-core.sections</a>
<a id="14034" class="Keyword">open</a> <a id="14039" class="Keyword">import</a> <a id="14046" href="foundation-core.sets.html" class="Module">foundation-core.sets</a>
<a id="14067" class="Keyword">open</a> <a id="14072" class="Keyword">import</a> <a id="14079" href="foundation-core.singleton-induction.html" class="Module">foundation-core.singleton-induction</a>
<a id="14115" class="Keyword">open</a> <a id="14120" class="Keyword">import</a> <a id="14127" href="foundation-core.subtype-identity-principle.html" class="Module">foundation-core.subtype-identity-principle</a>
<a id="14170" class="Keyword">open</a> <a id="14175" class="Keyword">import</a> <a id="14182" href="foundation-core.subtypes.html" class="Module">foundation-core.subtypes</a>
<a id="14207" class="Keyword">open</a> <a id="14212" class="Keyword">import</a> <a id="14219" href="foundation-core.truncated-maps.html" class="Module">foundation-core.truncated-maps</a>
<a id="14250" class="Keyword">open</a> <a id="14255" class="Keyword">import</a> <a id="14262" href="foundation-core.truncated-types.html" class="Module">foundation-core.truncated-types</a>
<a id="14294" class="Keyword">open</a> <a id="14299" class="Keyword">import</a> <a id="14306" href="foundation-core.truncation-levels.html" class="Module">foundation-core.truncation-levels</a>
<a id="14340" class="Keyword">open</a> <a id="14345" class="Keyword">import</a> <a id="14352" href="foundation-core.type-arithmetic-cartesian-product-types.html" class="Module">foundation-core.type-arithmetic-cartesian-product-types</a>
<a id="14408" class="Keyword">open</a> <a id="14413" class="Keyword">import</a> <a id="14420" href="foundation-core.type-arithmetic-dependent-pair-types.html" class="Module">foundation-core.type-arithmetic-dependent-pair-types</a>
<a id="14473" class="Keyword">open</a> <a id="14478" class="Keyword">import</a> <a id="14485" href="foundation-core.univalence.html" class="Module">foundation-core.univalence</a>
<a id="14512" class="Keyword">open</a> <a id="14517" class="Keyword">import</a> <a id="14524" href="foundation-core.universe-levels.html" class="Module">foundation-core.universe-levels</a>
</pre>
## Graph theory

<pre class="Agda"><a id="14586" class="Keyword">open</a> <a id="14591" class="Keyword">import</a> <a id="14598" href="graph-theory.directed-graphs.html" class="Module">graph-theory.directed-graphs</a>
<a id="14627" class="Keyword">open</a> <a id="14632" class="Keyword">import</a> <a id="14639" href="graph-theory.finite-graphs.html" class="Module">graph-theory.finite-graphs</a>
<a id="14666" class="Keyword">open</a> <a id="14671" class="Keyword">import</a> <a id="14678" href="graph-theory.polygons.html" class="Module">graph-theory.polygons</a>
<a id="14700" class="Keyword">open</a> <a id="14705" class="Keyword">import</a> <a id="14712" href="graph-theory.reflexive-graphs.html" class="Module">graph-theory.reflexive-graphs</a>
<a id="14742" class="Keyword">open</a> <a id="14747" class="Keyword">import</a> <a id="14754" href="graph-theory.undirected-graphs.html" class="Module">graph-theory.undirected-graphs</a>
</pre>
## Groups 

<pre class="Agda"><a id="14810" class="Keyword">open</a> <a id="14815" class="Keyword">import</a> <a id="14822" href="groups.html" class="Module">groups</a>
<a id="14829" class="Keyword">open</a> <a id="14834" class="Keyword">import</a> <a id="14841" href="groups.abstract-abelian-groups.html" class="Module">groups.abstract-abelian-groups</a>
<a id="14872" class="Keyword">open</a> <a id="14877" class="Keyword">import</a> <a id="14884" href="groups.abstract-abelian-subgroups.html" class="Module">groups.abstract-abelian-subgroups</a>
<a id="14918" class="Keyword">open</a> <a id="14923" class="Keyword">import</a> <a id="14930" href="groups.abstract-group-actions.html" class="Module">groups.abstract-group-actions</a>
<a id="14960" class="Keyword">open</a> <a id="14965" class="Keyword">import</a> <a id="14972" href="groups.abstract-group-torsors.html" class="Module">groups.abstract-group-torsors</a>
<a id="15002" class="Keyword">open</a> <a id="15007" class="Keyword">import</a> <a id="15014" href="groups.abstract-groups.html" class="Module">groups.abstract-groups</a>
<a id="15037" class="Keyword">open</a> <a id="15042" class="Keyword">import</a> <a id="15049" href="groups.abstract-subgroups.html" class="Module">groups.abstract-subgroups</a>
<a id="15075" class="Keyword">open</a> <a id="15080" class="Keyword">import</a> <a id="15087" href="groups.concrete-group-actions.html" class="Module">groups.concrete-group-actions</a>
<a id="15117" class="Keyword">open</a> <a id="15122" class="Keyword">import</a> <a id="15129" href="groups.concrete-groups.html" class="Module">groups.concrete-groups</a>
<a id="15152" class="Keyword">open</a> <a id="15157" class="Keyword">import</a> <a id="15164" href="groups.concrete-subgroups.html" class="Module">groups.concrete-subgroups</a>
<a id="15190" class="Keyword">open</a> <a id="15195" class="Keyword">import</a> <a id="15202" href="groups.examples-higher-groups.html" class="Module">groups.examples-higher-groups</a>
<a id="15232" class="Keyword">open</a> <a id="15237" class="Keyword">import</a> <a id="15244" href="groups.furstenberg-groups.html" class="Module">groups.furstenberg-groups</a>
<a id="15270" class="Keyword">open</a> <a id="15275" class="Keyword">import</a> <a id="15282" href="groups.higher-groups.html" class="Module">groups.higher-groups</a>
<a id="15303" class="Keyword">open</a> <a id="15308" class="Keyword">import</a> <a id="15315" href="groups.sheargroups.html" class="Module">groups.sheargroups</a>
</pre>
## Linear algebra

<pre class="Agda"><a id="15366" class="Keyword">open</a> <a id="15371" class="Keyword">import</a> <a id="15378" href="linear-algebra.matrices.html" class="Module">linear-algebra.matrices</a>
<a id="15402" class="Keyword">open</a> <a id="15407" class="Keyword">import</a> <a id="15414" href="linear-algebra.vectors.html" class="Module">linear-algebra.vectors</a>
</pre>
## Order theory

<pre class="Agda"><a id="15467" class="Keyword">open</a> <a id="15472" class="Keyword">import</a> <a id="15479" href="order-theory.html" class="Module">order-theory</a>
<a id="15492" class="Keyword">open</a> <a id="15497" class="Keyword">import</a> <a id="15504" href="order-theory.finite-posets.html" class="Module">order-theory.finite-posets</a>
<a id="15531" class="Keyword">open</a> <a id="15536" class="Keyword">import</a> <a id="15543" href="order-theory.finite-preorders.html" class="Module">order-theory.finite-preorders</a>
<a id="15573" class="Keyword">open</a> <a id="15578" class="Keyword">import</a> <a id="15585" href="order-theory.finitely-graded-posets.html" class="Module">order-theory.finitely-graded-posets</a>
<a id="15621" class="Keyword">open</a> <a id="15626" class="Keyword">import</a> <a id="15633" href="order-theory.planar-binary-trees.html" class="Module">order-theory.planar-binary-trees</a>
<a id="15666" class="Keyword">open</a> <a id="15671" class="Keyword">import</a> <a id="15678" href="order-theory.posets.html" class="Module">order-theory.posets</a>
<a id="15698" class="Keyword">open</a> <a id="15703" class="Keyword">import</a> <a id="15710" href="order-theory.preorders.html" class="Module">order-theory.preorders</a>
</pre>
## Polytopes

<pre class="Agda"><a id="15760" class="Keyword">open</a> <a id="15765" class="Keyword">import</a> <a id="15772" href="polytopes.abstract-polytopes.html" class="Module">polytopes.abstract-polytopes</a>
</pre>
## Rings

<pre class="Agda"><a id="15824" class="Keyword">open</a> <a id="15829" class="Keyword">import</a> <a id="15836" href="rings.html" class="Module">rings</a>
<a id="15842" class="Keyword">open</a> <a id="15847" class="Keyword">import</a> <a id="15854" href="rings.eisenstein-integers.html" class="Module">rings.eisenstein-integers</a>
<a id="15880" class="Keyword">open</a> <a id="15885" class="Keyword">import</a> <a id="15892" href="rings.gaussian-integers.html" class="Module">rings.gaussian-integers</a>
<a id="15916" class="Keyword">open</a> <a id="15921" class="Keyword">import</a> <a id="15928" href="rings.ideals.html" class="Module">rings.ideals</a>
<a id="15941" class="Keyword">open</a> <a id="15946" class="Keyword">import</a> <a id="15953" href="rings.localizations-rings.html" class="Module">rings.localizations-rings</a>
<a id="15979" class="Keyword">open</a> <a id="15984" class="Keyword">import</a> <a id="15991" href="rings.rings-with-properties.html" class="Module">rings.rings-with-properties</a>
<a id="16019" class="Keyword">open</a> <a id="16024" class="Keyword">import</a> <a id="16031" href="rings.rings.html" class="Module">rings.rings</a>
</pre>
## Synthetic homotopy theory

<pre class="Agda"><a id="16086" class="Keyword">open</a> <a id="16091" class="Keyword">import</a> <a id="16098" href="synthetic-homotopy-theory.html" class="Module">synthetic-homotopy-theory</a>
<a id="16124" class="Keyword">open</a> <a id="16129" class="Keyword">import</a> <a id="16136" href="synthetic-homotopy-theory.23-pullbacks.html" class="Module">synthetic-homotopy-theory.23-pullbacks</a>
<a id="16175" class="Keyword">open</a> <a id="16180" class="Keyword">import</a> <a id="16187" href="synthetic-homotopy-theory.24-pushouts.html" class="Module">synthetic-homotopy-theory.24-pushouts</a>
<a id="16225" class="Keyword">open</a> <a id="16230" class="Keyword">import</a> <a id="16237" href="synthetic-homotopy-theory.25-cubical-diagrams.html" class="Module">synthetic-homotopy-theory.25-cubical-diagrams</a>
<a id="16283" class="Keyword">open</a> <a id="16288" class="Keyword">import</a> <a id="16295" href="synthetic-homotopy-theory.26-descent.html" class="Module">synthetic-homotopy-theory.26-descent</a>
<a id="16332" class="Keyword">open</a> <a id="16337" class="Keyword">import</a> <a id="16344" href="synthetic-homotopy-theory.26-id-pushout.html" class="Module">synthetic-homotopy-theory.26-id-pushout</a>
<a id="16384" class="Keyword">open</a> <a id="16389" class="Keyword">import</a> <a id="16396" href="synthetic-homotopy-theory.27-sequences.html" class="Module">synthetic-homotopy-theory.27-sequences</a>
<a id="16435" class="Keyword">open</a> <a id="16440" class="Keyword">import</a> <a id="16447" href="synthetic-homotopy-theory.circle.html" class="Module">synthetic-homotopy-theory.circle</a>
<a id="16480" class="Keyword">open</a> <a id="16485" class="Keyword">import</a> <a id="16492" href="synthetic-homotopy-theory.cyclic-types.html" class="Module">synthetic-homotopy-theory.cyclic-types</a>
<a id="16531" class="Keyword">open</a> <a id="16536" class="Keyword">import</a> <a id="16543" href="synthetic-homotopy-theory.double-loop-spaces.html" class="Module">synthetic-homotopy-theory.double-loop-spaces</a>
<a id="16588" class="Keyword">open</a> <a id="16593" class="Keyword">import</a> <a id="16600" href="synthetic-homotopy-theory.functoriality-loop-spaces.html" class="Module">synthetic-homotopy-theory.functoriality-loop-spaces</a>
<a id="16652" class="Keyword">open</a> <a id="16657" class="Keyword">import</a> <a id="16664" href="synthetic-homotopy-theory.infinite-cyclic-types.html" class="Module">synthetic-homotopy-theory.infinite-cyclic-types</a>
<a id="16712" class="Keyword">open</a> <a id="16717" class="Keyword">import</a> <a id="16724" href="synthetic-homotopy-theory.interval-type.html" class="Module">synthetic-homotopy-theory.interval-type</a>
<a id="16764" class="Keyword">open</a> <a id="16769" class="Keyword">import</a> <a id="16776" href="synthetic-homotopy-theory.iterated-loop-spaces.html" class="Module">synthetic-homotopy-theory.iterated-loop-spaces</a>
<a id="16823" class="Keyword">open</a> <a id="16828" class="Keyword">import</a> <a id="16835" href="synthetic-homotopy-theory.loop-spaces.html" class="Module">synthetic-homotopy-theory.loop-spaces</a>
<a id="16873" class="Keyword">open</a> <a id="16878" class="Keyword">import</a> <a id="16885" href="synthetic-homotopy-theory.pointed-dependent-functions.html" class="Module">synthetic-homotopy-theory.pointed-dependent-functions</a>
<a id="16939" class="Keyword">open</a> <a id="16944" class="Keyword">import</a> <a id="16951" href="synthetic-homotopy-theory.pointed-equivalences.html" class="Module">synthetic-homotopy-theory.pointed-equivalences</a>
<a id="16998" class="Keyword">open</a> <a id="17003" class="Keyword">import</a> <a id="17010" href="synthetic-homotopy-theory.pointed-families-of-types.html" class="Module">synthetic-homotopy-theory.pointed-families-of-types</a>
<a id="17062" class="Keyword">open</a> <a id="17067" class="Keyword">import</a> <a id="17074" href="synthetic-homotopy-theory.pointed-homotopies.html" class="Module">synthetic-homotopy-theory.pointed-homotopies</a>
<a id="17119" class="Keyword">open</a> <a id="17124" class="Keyword">import</a> <a id="17131" href="synthetic-homotopy-theory.pointed-maps.html" class="Module">synthetic-homotopy-theory.pointed-maps</a>
<a id="17170" class="Keyword">open</a> <a id="17175" class="Keyword">import</a> <a id="17182" href="synthetic-homotopy-theory.pointed-types.html" class="Module">synthetic-homotopy-theory.pointed-types</a>
<a id="17222" class="Keyword">open</a> <a id="17227" class="Keyword">import</a> <a id="17234" href="synthetic-homotopy-theory.spaces.html" class="Module">synthetic-homotopy-theory.spaces</a>
<a id="17267" class="Keyword">open</a> <a id="17272" class="Keyword">import</a> <a id="17279" href="synthetic-homotopy-theory.triple-loop-spaces.html" class="Module">synthetic-homotopy-theory.triple-loop-spaces</a>
<a id="17324" class="Keyword">open</a> <a id="17329" class="Keyword">import</a> <a id="17336" href="synthetic-homotopy-theory.universal-cover-circle.html" class="Module">synthetic-homotopy-theory.universal-cover-circle</a>
</pre>
## Tutorials

<pre class="Agda"><a id="17412" class="Keyword">open</a> <a id="17417" class="Keyword">import</a> <a id="17424" href="tutorials.basic-agda.html" class="Module">tutorials.basic-agda</a>
</pre>
## Univalent combinatorics

<pre class="Agda"><a id="17486" class="Keyword">open</a> <a id="17491" class="Keyword">import</a> <a id="17498" href="univalent-combinatorics.html" class="Module">univalent-combinatorics</a>
<a id="17522" class="Keyword">open</a> <a id="17527" class="Keyword">import</a> <a id="17534" href="univalent-combinatorics.2-element-types.html" class="Module">univalent-combinatorics.2-element-types</a>
<a id="17574" class="Keyword">open</a> <a id="17579" class="Keyword">import</a> <a id="17586" href="univalent-combinatorics.binomial-types.html" class="Module">univalent-combinatorics.binomial-types</a>
<a id="17625" class="Keyword">open</a> <a id="17630" class="Keyword">import</a> <a id="17637" href="univalent-combinatorics.cartesian-product-finite-types.html" class="Module">univalent-combinatorics.cartesian-product-finite-types</a>
<a id="17692" class="Keyword">open</a> <a id="17697" class="Keyword">import</a> <a id="17704" href="univalent-combinatorics.coproduct-finite-types.html" class="Module">univalent-combinatorics.coproduct-finite-types</a>
<a id="17751" class="Keyword">open</a> <a id="17756" class="Keyword">import</a> <a id="17763" href="univalent-combinatorics.counting-cartesian-product-types.html" class="Module">univalent-combinatorics.counting-cartesian-product-types</a>
<a id="17820" class="Keyword">open</a> <a id="17825" class="Keyword">import</a> <a id="17832" href="univalent-combinatorics.counting-coproduct-types.html" class="Module">univalent-combinatorics.counting-coproduct-types</a>
<a id="17881" class="Keyword">open</a> <a id="17886" class="Keyword">import</a> <a id="17893" href="univalent-combinatorics.counting-decidable-subtypes.html" class="Module">univalent-combinatorics.counting-decidable-subtypes</a>
<a id="17945" class="Keyword">open</a> <a id="17950" class="Keyword">import</a> <a id="17957" href="univalent-combinatorics.counting-dependent-function-types.html" class="Module">univalent-combinatorics.counting-dependent-function-types</a>
<a id="18015" class="Keyword">open</a> <a id="18020" class="Keyword">import</a> <a id="18027" href="univalent-combinatorics.counting-dependent-pair-types.html" class="Module">univalent-combinatorics.counting-dependent-pair-types</a>
<a id="18081" class="Keyword">open</a> <a id="18086" class="Keyword">import</a> <a id="18093" href="univalent-combinatorics.counting-fibers-of-maps.html" class="Module">univalent-combinatorics.counting-fibers-of-maps</a>
<a id="18141" class="Keyword">open</a> <a id="18146" class="Keyword">import</a> <a id="18153" href="univalent-combinatorics.counting-function-types.html" class="Module">univalent-combinatorics.counting-function-types</a>
<a id="18201" class="Keyword">open</a> <a id="18206" class="Keyword">import</a> <a id="18213" href="univalent-combinatorics.counting-maybe.html" class="Module">univalent-combinatorics.counting-maybe</a>
<a id="18252" class="Keyword">open</a> <a id="18257" class="Keyword">import</a> <a id="18264" href="univalent-combinatorics.counting.html" class="Module">univalent-combinatorics.counting</a>
<a id="18297" class="Keyword">open</a> <a id="18302" class="Keyword">import</a> <a id="18309" href="univalent-combinatorics.decidable-dependent-function-types.html" class="Module">univalent-combinatorics.decidable-dependent-function-types</a>
<a id="18368" class="Keyword">open</a> <a id="18373" class="Keyword">import</a> <a id="18380" href="univalent-combinatorics.decidable-dependent-pair-types.html" class="Module">univalent-combinatorics.decidable-dependent-pair-types</a>
<a id="18435" class="Keyword">open</a> <a id="18440" class="Keyword">import</a> <a id="18447" href="univalent-combinatorics.decidable-subtypes.html" class="Module">univalent-combinatorics.decidable-subtypes</a>
<a id="18490" class="Keyword">open</a> <a id="18495" class="Keyword">import</a> <a id="18502" href="univalent-combinatorics.dependent-product-finite-types.html" class="Module">univalent-combinatorics.dependent-product-finite-types</a>
<a id="18557" class="Keyword">open</a> <a id="18562" class="Keyword">import</a> <a id="18569" href="univalent-combinatorics.dependent-sum-finite-types.html" class="Module">univalent-combinatorics.dependent-sum-finite-types</a>
<a id="18620" class="Keyword">open</a> <a id="18625" class="Keyword">import</a> <a id="18632" href="univalent-combinatorics.distributivity-of-set-truncation-over-finite-products.html" class="Module">univalent-combinatorics.distributivity-of-set-truncation-over-finite-products</a>
<a id="18710" class="Keyword">open</a> <a id="18715" class="Keyword">import</a> <a id="18722" href="univalent-combinatorics.double-counting.html" class="Module">univalent-combinatorics.double-counting</a>
<a id="18762" class="Keyword">open</a> <a id="18767" class="Keyword">import</a> <a id="18774" href="univalent-combinatorics.embeddings-standard-finite-types.html" class="Module">univalent-combinatorics.embeddings-standard-finite-types</a>
<a id="18831" class="Keyword">open</a> <a id="18836" class="Keyword">import</a> <a id="18843" href="univalent-combinatorics.embeddings.html" class="Module">univalent-combinatorics.embeddings</a>
<a id="18878" class="Keyword">open</a> <a id="18883" class="Keyword">import</a> <a id="18890" href="univalent-combinatorics.equality-finite-types.html" class="Module">univalent-combinatorics.equality-finite-types</a>
<a id="18936" class="Keyword">open</a> <a id="18941" class="Keyword">import</a> <a id="18948" href="univalent-combinatorics.equality-standard-finite-types.html" class="Module">univalent-combinatorics.equality-standard-finite-types</a>
<a id="19003" class="Keyword">open</a> <a id="19008" class="Keyword">import</a> <a id="19015" href="univalent-combinatorics.equivalences-standard-finite-types.html" class="Module">univalent-combinatorics.equivalences-standard-finite-types</a>
<a id="19074" class="Keyword">open</a> <a id="19079" class="Keyword">import</a> <a id="19086" href="univalent-combinatorics.equivalences.html" class="Module">univalent-combinatorics.equivalences</a>
<a id="19123" class="Keyword">open</a> <a id="19128" class="Keyword">import</a> <a id="19135" href="univalent-combinatorics.fibers-of-maps-between-finite-types.html" class="Module">univalent-combinatorics.fibers-of-maps-between-finite-types</a>
<a id="19195" class="Keyword">open</a> <a id="19200" class="Keyword">import</a> <a id="19207" href="univalent-combinatorics.finite-choice.html" class="Module">univalent-combinatorics.finite-choice</a>
<a id="19245" class="Keyword">open</a> <a id="19250" class="Keyword">import</a> <a id="19257" href="univalent-combinatorics.finite-connected-components.html" class="Module">univalent-combinatorics.finite-connected-components</a>
<a id="19309" class="Keyword">open</a> <a id="19314" class="Keyword">import</a> <a id="19321" href="univalent-combinatorics.finite-function-types.html" class="Module">univalent-combinatorics.finite-function-types</a>
<a id="19367" class="Keyword">open</a> <a id="19372" class="Keyword">import</a> <a id="19379" href="univalent-combinatorics.finite-presentations.html" class="Module">univalent-combinatorics.finite-presentations</a>
<a id="19424" class="Keyword">open</a> <a id="19429" class="Keyword">import</a> <a id="19436" href="univalent-combinatorics.finite-types.html" class="Module">univalent-combinatorics.finite-types</a>
<a id="19473" class="Keyword">open</a> <a id="19478" class="Keyword">import</a> <a id="19485" href="univalent-combinatorics.finitely-presented-types.html" class="Module">univalent-combinatorics.finitely-presented-types</a>
<a id="19534" class="Keyword">open</a> <a id="19539" class="Keyword">import</a> <a id="19546" href="univalent-combinatorics.image-of-maps.html" class="Module">univalent-combinatorics.image-of-maps</a>
<a id="19584" class="Keyword">open</a> <a id="19589" class="Keyword">import</a> <a id="19596" href="univalent-combinatorics.inequality-types-with-counting.html" class="Module">univalent-combinatorics.inequality-types-with-counting</a>
<a id="19651" class="Keyword">open</a> <a id="19656" class="Keyword">import</a> <a id="19663" href="univalent-combinatorics.injective-maps.html" class="Module">univalent-combinatorics.injective-maps</a>
<a id="19702" class="Keyword">open</a> <a id="19707" class="Keyword">import</a> <a id="19714" href="univalent-combinatorics.lists.html" class="Module">univalent-combinatorics.lists</a>
<a id="19744" class="Keyword">open</a> <a id="19749" class="Keyword">import</a> <a id="19756" href="univalent-combinatorics.maybe.html" class="Module">univalent-combinatorics.maybe</a>
<a id="19786" class="Keyword">open</a> <a id="19791" class="Keyword">import</a> <a id="19798" href="univalent-combinatorics.pi-finite-types.html" class="Module">univalent-combinatorics.pi-finite-types</a>
<a id="19838" class="Keyword">open</a> <a id="19843" class="Keyword">import</a> <a id="19850" href="univalent-combinatorics.pigeonhole-principle.html" class="Module">univalent-combinatorics.pigeonhole-principle</a>
<a id="19895" class="Keyword">open</a> <a id="19900" class="Keyword">import</a> <a id="19907" href="univalent-combinatorics.presented-pi-finite-types.html" class="Module">univalent-combinatorics.presented-pi-finite-types</a>
<a id="19957" class="Keyword">open</a> <a id="19962" class="Keyword">import</a> <a id="19969" href="univalent-combinatorics.ramsey-theory.html" class="Module">univalent-combinatorics.ramsey-theory</a>
<a id="20007" class="Keyword">open</a> <a id="20012" class="Keyword">import</a> <a id="20019" href="univalent-combinatorics.retracts-of-finite-types.html" class="Module">univalent-combinatorics.retracts-of-finite-types</a>
<a id="20068" class="Keyword">open</a> <a id="20073" class="Keyword">import</a> <a id="20080" href="univalent-combinatorics.standard-finite-pruned-trees.html" class="Module">univalent-combinatorics.standard-finite-pruned-trees</a>
<a id="20133" class="Keyword">open</a> <a id="20138" class="Keyword">import</a> <a id="20145" href="univalent-combinatorics.standard-finite-trees.html" class="Module">univalent-combinatorics.standard-finite-trees</a>
<a id="20191" class="Keyword">open</a> <a id="20196" class="Keyword">import</a> <a id="20203" href="univalent-combinatorics.standard-finite-types.html" class="Module">univalent-combinatorics.standard-finite-types</a>
<a id="20249" class="Keyword">open</a> <a id="20254" class="Keyword">import</a> <a id="20261" href="univalent-combinatorics.sums-of-natural-numbers.html" class="Module">univalent-combinatorics.sums-of-natural-numbers</a>
<a id="20309" class="Keyword">open</a> <a id="20314" class="Keyword">import</a> <a id="20321" href="univalent-combinatorics.surjective-maps.html" class="Module">univalent-combinatorics.surjective-maps</a>
</pre>
## Univalent foundation

<pre class="Agda"><a id="20399" class="Keyword">open</a> <a id="20404" class="Keyword">import</a> <a id="20411" href="univalent-foundations.isolated-points.html" class="Module">univalent-foundations.isolated-points</a>
</pre>
### Wild algebra

<pre class="Agda"><a id="20480" class="Keyword">open</a> <a id="20485" class="Keyword">import</a> <a id="20492" href="wild-algebra.magmas.html" class="Module">wild-algebra.magmas</a>
<a id="20512" class="Keyword">open</a> <a id="20517" class="Keyword">import</a> <a id="20524" href="wild-algebra.universal-property-lists-wild-monoids.html" class="Module">wild-algebra.universal-property-lists-wild-monoids</a>
<a id="20575" class="Keyword">open</a> <a id="20580" class="Keyword">import</a> <a id="20587" href="wild-algebra.wild-groups.html" class="Module">wild-algebra.wild-groups</a>
<a id="20612" class="Keyword">open</a> <a id="20617" class="Keyword">import</a> <a id="20624" href="wild-algebra.wild-monoids.html" class="Module">wild-algebra.wild-monoids</a>
<a id="20650" class="Keyword">open</a> <a id="20655" class="Keyword">import</a> <a id="20662" href="wild-algebra.wild-unital-magmas.html" class="Module">wild-algebra.wild-unital-magmas</a>
</pre>
## Everything

See the list of all Agda modules [here](everything.html).

