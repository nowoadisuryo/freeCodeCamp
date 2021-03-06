---
id: 5900f3761000cf542c50fe88
challengeType: 5
title: 'Problem 9: Special Pythagorean triplet'
forumTopicId: 302205
localeTitle: 'Задача 9: Специальный пифагорейский триплет'
---

## Description
<section id='description'>
Пифагорейский триплет представляет собой набор из трех натуральных чисел <var>a</var> &lt; <var>b</var> &lt; <var>c</var> , для которых, <div style="text-align: center;"> <var>a</var> <sup>2</sup> + <var>b</var> <sup>2</sup> = <var>c</var> <sup>2</sup> </div> Например, 3 <sup>2</sup> + 4 <sup>2</sup> = 9 + 16 = 25 = 5 <sup>2</sup> . Существует ровно один пифагорейский триплет, для которого <var>a</var> + <var>b</var> + <var>c</var> = 1000. Найдите произведение <var>abc</var> такое, что <var>a</var> + <var>b</var> + <var>c</var> = <code>n</code> .
</section>

## Instructions
<section id='instructions'>

</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: <code>specialPythagoreanTriplet(1000)</code> should return 31875000.
    testString: assert.strictEqual(specialPythagoreanTriplet(1000), 31875000);
  - text: <code>specialPythagoreanTriplet(24)</code> should return 480.
    testString: assert.strictEqual(specialPythagoreanTriplet(24), 480);
  - text: <code>specialPythagoreanTriplet(120)</code> should return 49920, 55080 or 60000
    testString: assert([49920, 55080, 60000].includes(specialPythagoreanTriplet(120)));

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='js-seed'>

```js
function specialPythagoreanTriplet(n) {
 let sumOfabc = n;
 // Good luck!
 return true;
}

specialPythagoreanTriplet(1000);

```

</div>

</section>

## Solution
<section id='solution'>

```js
const specialPythagoreanTriplet = (n)=>{
 let sumOfabc = n;
 let a,b,c;
 for(a = 1; a<=sumOfabc/3; a++){
 for(b = a+1; b<=sumOfabc/2; b++){
 c = Math.sqrt(a*a+b*b);
 if((a+b+c) == sumOfabc){
 return a*b*c;
 }
 }
 }
}
```

</section>
