# Ex.No:3(C) ABSTRACTION

## QUESTION:
In a secret intelligence facility, encrypted messages are stored as arrays of characters. Each type of agent has a different way to decode these messages. Define an abstract class Decoder with a method decodeMessage(String[] fragments).
There are two types of agents:

AlphaAgent: Extracts a meaningful string by rearranging the fragments based on even indices first, then odd indices, and then reversing the final result.

BetaAgent: Picks all fragments that start and end with the same letter, joins them with -, and removes all vowels from the resulting string.

## AIM:
To implement an abstract Decoder class with AlphaAgent and BetaAgent subclasses that decrypt messages using different decoding strategies.

## ALGORITHM :
1.Create abstract Decoder class with abstract decodeMessage() method
2.Implement AlphaAgent that rearranges fragments (even indices → odd indices) and reverses result
3.Implement BetaAgent that filters fragments (same start/end letter), joins with "-", and removes vowels
4.Test both agents with sample encrypted messages




## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Vigneshwaran S
RegisterNumber: 212224060301
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class Decoder {
    public abstract String decodeMessage(String[] fragments);
}

class AlphaAgent extends Decoder {
    @Override
    public String decodeMessage(String[] fragments) {
        List<String> evenIndexed = new ArrayList<>();
        List<String> oddIndexed = new ArrayList<>();
        
        for (int i = 0; i < fragments.length; i++) {
            if (i % 2 == 0) {
                evenIndexed.add(fragments[i]);
            } else {
                oddIndexed.add(fragments[i]);
            }
        }
        
        List<String> combined = new ArrayList<>();
        combined.addAll(evenIndexed);
        combined.addAll(oddIndexed);
        
        Collections.reverse(combined);
        
        return String.join("", combined);
    }
}

class BetaAgent extends Decoder {
    @Override
    public String decodeMessage(String[] fragments) {
        List<String> selectedFragments = new ArrayList<>();
        
        for (String fragment : fragments) {
            if (fragment.length() > 0 && 
                Character.toLowerCase(fragment.charAt(0)) == 
                Character.toLowerCase(fragment.charAt(fragment.length() - 1))) {
                selectedFragments.add(fragment);
            }
        }
        
        String joined = String.join("-", selectedFragments);
        
        // Remove vowels (case insensitive)
        return joined.replaceAll("[aeiouAEIOU]", "");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Read number of fragments
        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline
        
        // Read fragments
        String[] fragments = new String[n];
        for (int i = 0; i < n; i++) {
            fragments[i] = scanner.nextLine();
        }
        
        // Read agent type
        int agentType = scanner.nextInt();
        
        Decoder decoder;
        if (agentType == 1) {
            decoder = new AlphaAgent();
        } else {
            decoder = new BetaAgent();
        }
        
        String result = decoder.decodeMessage(fragments);
        System.out.println(result);
        
        scanner.close();
    }
}
```






## OUTPUT:
<img width="599" height="424" alt="image" src="https://github.com/user-attachments/assets/b1ef72ea-f100-47fb-8761-da803402a910" />


## RESULT:
Both AlphaAgent and BetaAgent were successfully implemented. AlphaAgent correctly rearranged and reversed fragments, while BetaAgent properly filtered same-start-end fragments, joined them with hyphens, and removed all vowels, demonstrating polymorphic decoding behavior.




