# Password-Entropy-Calculator

Calculates the relative strength of a password. This is accomplished by using several techniques. Primarily this relies on letter trigraphs, which check each set of 3 characters in a given password. This also calculates the entropy bits based on Claude Shannon's technique on determining the number of bits required to represent a set of characters and multiplying it by the length of the password. There is also a check to see if a password is contained in a list of common passwords.

As a bonus there's also a "Search Space" or (Total Possible Combinations) Calculator, inspired by <a href="https://www.grc.com/haystack.htm" target="_blank">GRC's Interactive Brute Force Password “Search Space” Calculator.
