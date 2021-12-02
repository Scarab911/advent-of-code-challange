```js
//antros dienos pirma uzduotis, logika su objects
let fSum = 0;
let dSum = 0;
let upSum = 0;
let aim = 0;
let depht = 0;
//forward
const forward = movement.map((obj) => (obj.forward ? obj.forward : 0));
fSum = forward.reduce((sum, a) => sum + a, 0);
//down
const down = movement.map((obj) => (obj.down ? obj.down : 0));
dSum = down.reduce((sum, a) => sum + a, 0);
//up
const up = movement.map((obj) => (obj.up ? obj.up : 0));
upSum = up.reduce((sum, a) => sum + a, 0);

console.log('forward total:', fSum);
console.log('down total:', dSum);
console.log('up total:', upSum);
//part two
movement.forEach((obj) => {
  if (obj.forward) {
    fSum += obj.forward;
    depht += obj.forward * aim;
  }
  if (obj.down) {
    aim += obj.down;
  }
  if (obj.up) {
    aim -= obj.up;
  }
});

console.log(depht * fSum);
```
