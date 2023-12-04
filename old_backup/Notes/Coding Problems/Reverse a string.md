- Java

```java
public class Main {
	public static void main(String[] args) {  
		System.out.println(reverseString("This is a sentence!"));
		// !ecnetnes a si sihT
	}  
	  
	public static String reverseString(String sentence) {  
		if (sentence.equals("")) {
			return "";
		}
	  
		return reverseString(sentence.substring(1)) + sentence.charAt(0);
	}
}
```