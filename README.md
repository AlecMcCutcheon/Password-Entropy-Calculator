# Password Entropy & strength Calculator

Built off of <a href="https://github.com/tests-always-included/password-strength">tests-always-included/password-strength</a>. Included is version 1 of the calculator, please write me if you'd like to clean up the code and make it better. I want this to be fully community built. 

This Calculates the relative strength of a password using several techniques. Primarily this relies on letter trigraphs, which check each set of 3 characters in a given password. This also calculates the entropy bits based on Claude Shannon's technique on determining the number of bits required to represent a set of characters and multiplying it by the length of the password and there's a check to see if a password is contained in a list of common passwords and as a bonus there's also a "Search Space" or (Total Possible Combinations) Calculator, inspired by <a href="https://www.grc.com/haystack.htm">GRC's Interactive Brute Force Password “Search Space” Calculator.</a> 
You can toggle between the normal algorithm and GRC's algorithm and create custom scenarios. Took me forever to figure out how GRC was calculating their "Search Space Size" but happy to have figured it out. <a href="https://alecmccutcheon.github.io/Password-Entropy-Calculator/">Live Demo</a>

For these examples the password is: 12345

* The normal algorithm is:  
```javascript

Var charset = 10;
Var length = 5;

 Math.pow(charset, length);
```
and a symbol character set size of 32. Which = 100,000

* GRC's algorithm is:

The charset, length, and currentlength are all dynamic variables pulled from the current password. length and currentlength are pulled from the same place but only length is manipulated by the function and currentlength preserves the current input length so it can be used in the calculation.

```javascript

Var charset = 10;
Var length = 5;
Var currentlength = 5;

function GRC(length) 
{ 
  if(length < 1) 
  {
    return 0 ; 
  }
  if (length == 1)
  {
    return Math.pow(charset, currentlength); 
  }
  return Math.pow(charset, length - 1) + GRC(length - 1); 
}
```
and a symbol character set size of 33. Which = 111,110
