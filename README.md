# Gibberish.js - Effective Gibberish Detection for Clientside Input Verification
A JavaScript tool to detect gibberish text.

Based on Rob Neuhaus's [Gibberish Detector](https://github.com/rrenaud/Gibberish-Detector), described in his repo.

This uses a transition matrix generated by Neuhaus' program, processed on the client side. Using  

# Examples
```javascript
console.log(Gibberish.isGibberish('hey there buddy')) // => true
console.log(Gibberish.isGibberish('hey asfgdsdfhgsdgh buddy')) // => false
console.log(Gibberish.isGibberish('i really like markov chains')) // => true
console.log(Gibberish.isGibberish(';sdfkhgas')) // => false
```
