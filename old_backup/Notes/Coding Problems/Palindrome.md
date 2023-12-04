- Java

```java
public class Main {
	public static void main(String[] args) {
		System.out.println("Is Kayak a palindrome: " + isPalindrome("Kayak"));
	}

	public static boolean isPalindrome(String word) {
		if (word.length() == 0 || word.length() == 1) {
			return true;
		}

		word = word.toLowerCase();

		if (word.charAt(0) == word.charAt(word.length() - 1)) {
			return isPalindrome(word.substring(1, word.length() - 1));
		}

		return false;
	}
}
```