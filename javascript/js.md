## 2022.09.01

1. textContent, innerText, innerHTML

- textContent: is all text contained by an element and all its children that are for formatting purposes only, also contained all text in script and style
- innerText returns all text contained by an element and all its child elements, does not get the text in script and style
- innerHtml returns all text, including html tags, that is contained by an element

## 2022.09.05

1. String ends with?

Complete the solution so that it returns true if the first argument(string) passed in ends with the 2nd argument (also a string).

```js
solution("abc", "bc"); // returns true
solution("abc", "d"); // returns false
```

solution:

1).

```js
function solution(str, ending) {
  return str.indexOf(ending, str.length - ending.length) !== -1;
}
```

2).

```js
function solution(str, ending) {
  return str.substr(-ending.length) === ending;
}
```

3).

```js
function solution(str, ending) {
  return str.endsWith(ending);
}
```

4).

```js
function solution(str, ending) {
  return str.includes(ending, str.length - ending.length);
}
```

2. Reversed Strings

```js
function solution(str) {
  return str.split("").reverse().join("");
}
```

3. String repeat

```js
function repeatStr(n, s) {
  return s.repeat(n);
}
```

## 2022.09.06

1. choose a checked checkbox with a type radio

```js
form.addEventListener("submit", (event) => {
  event.preventDefault();
  let result;

  const numberOfA = Number(event.target.elements.numberA.value);
  const numberOfB = Number(event.target.elements.numberB.value);

  //   solution 1
  const operator = event.target.querySelector(
    "input[type= radio]:checked"
  ).value;
  console.log(operator);

  if (operator === "additon") {
    result = add(numberOfA, numberOfB);
  } else if (operator === "substraction") {
    result = subtract(numberOfA, numberOfB);
  } else if (operator === "multiplication") {
    result = multiply(numberOfA, numberOfB);
  } else if (operator === "division") {
    result = divide(numberOfA, numberOfB);
  }

  // solution 2
  if (event.target.querySelector("input[value= addition]").checked) {
    result = add(numberOfA, numberOfB);
  } else if (event.target.elements.operator[1].checked) {
    result = subtract(numberOfA, numberOfB);
  } else if (event.target.elements.operator[2].checked) {
    result = multiply(numberOfA, numberOfB);
  } else if (event.target.elements.operator[3].checked) {
    result = divide(numberOfA, numberOfB);
  }

  resultOutput.textContent = result;
});
```

## 2022.09.07

## 1. defer

```html
<script src="" defer></script>
```

first HTML--> script, when hier is a defer.
