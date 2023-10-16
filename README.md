import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class ShuffleArray {
    public static void main(String[] args) {

        List<Integer> list = new ArrayList<>();
        list.add(1);
        list.add(2);
        list.add(3);
        list.add(4);
        list.add(5);
        list.add(6);
        list.add(7);

   
        Collections.shuffle(list);




import java.util.HashMap;
import java.util.Map;

public class Main {
    private static final Map<Character, Integer> romanNumerals = new HashMap<>();

    static {
        romanNumerals.put('I', 1);
        romanNumerals.put('V', 5);
        romanNumerals.put('X', 10);
        // Add more Roman numerals as needed
    }

    public static void main(String[] args) {
        String romanNumber = "IX";
        int result = romanToInteger(romanNumber);
        System.out.println("Roman Number " + romanNumber + " as Integer: " + result);
    }

    public static int romanToInteger(String s) {
        int result = 0;
        int prevValue = 0;

        for (int i = s.length() - 1; i >= 0; i--) {
            int charValue = romanNumerals.get(s.charAt(i));
            if (charValue < prevValue) {
                result -= charValue;
            } else {
                result += charValue;
            }
            prevValue = charValue;
        }
        return result;
    }
}



public class Main {
    public static void main(String[] args) {
        String input = "The quick brown fox jumps over the lazy dog";
        boolean isPangram = checkIfPangram(input.toLowerCase());
        System.out.println("Is the input a Pangram? " + isPangram);
    }

    public static boolean checkIfPangram(String input) {
        boolean[] alphabet = new boolean[26];
        for (char c : input.toCharArray()) {
            if (Character.isLetter(c)) {
                alphabet[c - 'a'] = true;
            }
        }

        for (boolean letterPresent : alphabet) {
            if (!letterPresent) {
                return false;
            }
        }
        return true;
    }
}


          

  
        System.out.println("Shuffled array: " + list);
    }
}
