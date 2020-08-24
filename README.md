# Password-Entropy-Calculator

Built off of <a href="https://github.com/tests-always-included/password-strength" target="_blank">tests-always-included/password-strength</a> 
This Calculates the relative strength of a password using several techniques. Primarily this relies on letter trigraphs, which check each set of 3 characters in a given password. This also calculates the entropy bits based on Claude Shannon's technique on determining the number of bits required to represent a set of characters and multiplying it by the length of the password and there's a check to see if a password is contained in a list of common passwords and as a bonus there's also a "Search Space" or (Total Possible Combinations) Calculator, inspired by <a href="https://www.grc.com/haystack.htm" target="_blank">GRC's Interactive Brute Force Password “Search Space” Calculator.</a> You can toggle between the normal algorithm which is:  
```javascript
 Math.pow(number-of-characters, Password-length);
```
and a symbol character set size of 32.

GRC's algorithm which is:

```javascript
function GRC(Password-length) 
{ 
  if(Password-length < 1) 
  {
    return 0 ; 
  }
  if (Password-length == 1)
  {
    return Math.pow(number-of-characters, Password-length); 
  }
  return Math.pow(number-of-characters, Password-length - 1) + GRC(Password-length - 1); 
}
```
and a symbol character set size of 32.

  ![Password Entropy Calculator](https://raw.githubusercontent.com/AlecMcCutcheon/Password-Entropy-Calculator/master/Password%20Entropy%20Calculator%20.jpg)
Format: ![Alt Text](url)
