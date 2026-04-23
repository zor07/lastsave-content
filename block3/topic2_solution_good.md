```java
package com.lastsave.block03.topic02;

public class QuestB3T2 {

    public String join(String[] words) {
        StringBuilder sb = new StringBuilder();
        for (String word : words) {
            sb.append(word);
        }
        return sb.toString();
    }

    public String joinWithSeparator(String[] words, String separator) {
        StringBuilder sb = new StringBuilder();
        for (int i = 0; i < words.length; i++) {
            sb.append(words[i]);
            if (i < words.length - 1) {
                sb.append(separator);
            }
        }
        return sb.toString();
    }

    public String repeat(String s, int n) {
        StringBuilder sb = new StringBuilder();
        for (int i = 0; i < n; i++) {
            sb.append(s);
        }
        return sb.toString();
    }

    public String reverse(String s) {
        return new StringBuilder(s).reverse().toString();
    }

    public String charCount(String s) {
        return new StringBuilder("Символов: ").append(s.length()).toString();
    }
}
```
