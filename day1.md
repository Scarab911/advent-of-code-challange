```js
// //array isskaidymas po tris elementus
// let R = [];
// for (var i = 0, len = a.length; i < len; i += 3) R.push(a.slice(i, i + 3));

//pirmos dienos, pirmos uzduoties antra dalis
let pradinis = 477;

for (let i = 0; i < a.length; i++) {
  let suma = 0;
  let dalis = a.slice(i, 3 + i);
  console.log(dalis.length);

  if (dalis.length < 3) {
    console.log('ilgis po patikrinimo', dalis.length);
    return;
  }
  suma = dalis.reduce((sum, a) => sum + a, 0);
  console.log(suma);
  if (pradinis < suma) {
    count++;
    pradinis = suma;
  } else {
    pradinis = suma;
  }
  console.log(count);
}
```
