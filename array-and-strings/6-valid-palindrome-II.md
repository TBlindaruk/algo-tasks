### Valid Palindrome II

Given a non-empty string s, you may delete at most one character. Judge whether you can make it a palindrome.

#### Example 1:

```
Input: "aba"
Output: True
```

#### Example 2:

```
Input: "abca"
Output: True
Explanation: You could delete the character 'c'.
```

#### Note:

1. The string will only contain lowercase characters a-z. The maximum length of the string is 50000.


```JavaScript
/**
 * @param {string} s
 * @return {boolean}
 */
const validPalindrome = (s) => {
    for (let i = 0, stop = s.length / 2; i < stop; i++) {
        let j = s.length - i - 1
        if (s[i] !== s[j]) {
            return isPalindrome(cut(s, i)) || isPalindrome(cut(s, j))
        }
    }
    return true
};

const cut = (s, i) => s.substr(0, i) + s.substr(i + 1);

const isPalindrome = (s) => s === s.split('').reverse().join('');
```
