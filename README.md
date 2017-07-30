# Gibberish.js 
## Effective Gibberish Detection for Clientside Input Verification
A JavaScript tool to detect gibberish text.

Based on Rob Neuhaus's [Gibberish Detector](https://github.com/rrenaud/Gibberish-Detector), described in his repo.

Using a transition matrix generated from Neuhaus' program, gibberish.js classifies text using a two charachter Markov Chain on the client side.  

## Examples
```javascript
console.log(Gibberish.isGibberish('hey there buddy')) // => false
console.log(Gibberish.isGibberish('hey asfgdsdfhgsdgh buddy')) // => true
console.log(Gibberish.isGibberish('i really like markov chains')) // => false
console.log(Gibberish.isGibberish(';sdfkhgas')) // => true
```
To change the threshold for what is classified as gibberish and what is not, modify the matrix object.
```javascript
Gibberish.matrix['tresh'] = 0.04; // default
Gibberish.matrix['tresh'] = 0.02; // the threshold chosen by Neuhaus' method
Gibberish.matrix['tresh'] = 0.06; // fairly strict, more likely to misclassify valid strings 
