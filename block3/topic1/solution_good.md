```java
package com.lastsave.block03.topic01;

public class QuestB3T1 {

    public int getLength(String s) {
        return s.length();
    }

    public char getFirstChar(String s) {
        if (s.isEmpty()) return '\0';
        return s.charAt(0);
    }

    public char getLastChar(String s) {
        if (s.isEmpty()) return '\0';
        return s.charAt(s.length() - 1);
    }

    public String toUpper(String s) {
        return s.toUpperCase();
    }

    public boolean containsSubstring(String s, String sub) {
        return s.contains(sub);
    }

    public String getSubstring(String s, int from, int to) {
        return s.substring(from, to);
    }

    public String trimSpaces(String s) {
        return s.trim();
    }

    public boolean equalsIgnoreCase(String a, String b) {
        return a.equalsIgnoreCase(b);
    }

    public boolean hasPrefix(String s, String prefix) {
        return s.startsWith(prefix);
    }

    public int parseNumber(String s) {
        return Integer.parseInt(s);
    }
}
```
