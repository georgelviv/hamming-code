# hamming-code
Hamming-code allows you to encode and decode binary strings with [hamming linear error correcting codes algorithm](https://en.wikipedia.org/wiki/Hamming_code). It has not any dependencies. Works only with binary strings. For example `'101010'`. 

It is UMD module. It means it capable of working in AMD, CommonJS-like, nodejs, browrser environments. For more information go to [UMD](https://github.com/umdjs/umd).

```sh
npm install hamming-code
```

Example

```js
var hammingCode = require("./index.js");

console.log("Encode 1111: ", hammingCode.encode("1111"));
console.log("Decode 0011111: ", hammingCode.decode(hammingCode.encode("1111")));
console.log("Check 0011111: ", hammingCode.check(hammingCode.encode("1111")));
console.log("Check 0001111: ", hammingCode.check("0001111"));
console.log("Decode 0001111: ", hammingCode.decode("0001111"));
console.log("Pure Decode (without correcting) 0001111: ", hammingCode.pureDecode("0001111"));
```