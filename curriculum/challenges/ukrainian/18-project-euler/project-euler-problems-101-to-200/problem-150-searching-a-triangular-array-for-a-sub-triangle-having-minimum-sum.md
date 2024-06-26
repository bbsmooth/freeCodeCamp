---
id: 5900f4031000cf542c50ff15
title: >-
  Завдання 150: пошук трикутника з найменшою сумою в трикутному масиві
challengeType: 1
forumTopicId: 301781
dashedName: problem-150-searching-a-triangular-array-for-a-sub-triangle-having-minimum-sum
---

# --description--

Нам потрібно знайти трикутник, сума чисел якого є найменшою серед інших трикутників у масиві з додатними та від’ємними числами.

У наведеному нижче прикладі можна легко довести, що виділений трикутник відповідає умові, оскільки його сума дорівнює −42.

<img alt="трикутний масив з виділеним трикутником із сумою -42" src="https://cdn.freecodecamp.org/curriculum/project-euler/searching-a-triangular-array-for-a-sub-triangle-having-minimum-sum.gif" style="background-color: white; padding: 10px; display: block; margin-right: auto; margin-left: auto; margin-bottom: 1.2rem;" />

Нам потрібно створити трикутний масив з однією тисячею рядків, тому ми генеруємо 500500 псевдовипадкових чисел $s_k$ у діапазоні $±2^{19}$, використовуючи генератор випадкових чисел (відомий як лінійний конгруентний метод):

$$\begin{align}   t := & \\ 0\\\\
  \text{при}\\ & k = 1\\ \text{до}\\ k = 500500:\\\\   & t := (615949 × t + 797807)\\ \text{modulo}\\ 2^{20}\\\\
  & s_k := t − 219\\\\ \end{align}$$

Отже, $s_1 = 273519$, $s_2 = −153582$, $s_3 = 450905$ і т. д.

Після цього утворюється наш трикутний масив з використанням псевдовипадкових чисел:

$$ s_1 \\\\
s_2\\;s_3 \\\\ s_4\\; s_5\\; s_6 \\\\
s_7\\; s_8\\; s_9\\; s_{10} \\\\ \ldots $$

Менші трикутники можуть починатися з будь-якого елемента масиву і сягати вниз настільки, наскільки потрібно (захоплюючи два елементи одразу під ним з наступного ряду, три елементи одразу під ним з наступного ряду і так далі).

«Сума меншого трикутника» визначається як сума всіх його елементів.

Знайдіть найменшу можливу суму меншого трикутника.

# --hints--

`smallestSubTriangleSum()` має повернути `-271248680`.

```js
assert.strictEqual(smallestSubTriangleSum(), -271248680);
```

# --seed--

## --seed-contents--

```js
function smallestSubTriangleSum() {

  return true;
}

smallestSubTriangleSum();
```

# --solutions--

```js
// solution required
```
