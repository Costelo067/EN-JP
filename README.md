import java.util.Scanner;

public class LatinToJapanese {

    public static void main(String[] args) {
        // Create a scanner object to take input
        Scanner scanner = new Scanner(System.in);

        // Display a prompt to the user
        System.out.println("Enter Latin letters to see corresponding Japanese characters:");
        String input = scanner.nextLine().toLowerCase(); // Take the input and convert it to lowercase

        // Translate Latin to Japanese
        String translated = translateToJapanese(input);

        // Display the translated text
        System.out.println("Japanese translation: " + translated);
        
        // Close the scanner
        scanner.close();
    }

    public static String translateToJapanese(String input) {
        // A simple mapping of Latin letters to Japanese Katakana characters
        StringBuilder output = new StringBuilder();

        for (int i = 0; i < input.length(); i++) {
            char c = input.charAt(i);
            
            // Check for Latin letters and map them to Japanese characters
            switch (c) {
                case 'a': output.append("ア"); break;
                case 'b': output.append("ビ"); break;
                case 'c': output.append("シ"); break;
                case 'd': output.append("デ"); break;
                case 'e': output.append("エ"); break;
                case 'f': output.append("フ"); break;
                case 'g': output.append("ギ"); break;
                case 'h': output.append("ヒ"); break;
                case 'i': output.append("イ"); break;
                case 'j': output.append("ジ"); break;
                case 'k': output.append("ケ"); break;
                case 'l': output.append("ル"); break;
                case 'm': output.append("ム"); break;
                case 'n': output.append("ン"); break;
                case 'o': output.append("オ"); break;
                case 'p': output.append("プ"); break;
                case 'q': output.append("ク"); break;
                case 'r': output.append("ラ"); break;
                case 's': output.append("ス"); break;
                case 't': output.append("テ"); break;
                case 'u': output.append("ウ"); break;
                case 'v': output.append("ヴ"); break;
                case 'w': output.append("ワ"); break;
                case 'x': output.append("クス"); break;
                case 'y': output.append("イ"); break;
                case 'z': output.append("ズ"); break;
                default:
                    // If the character is not a Latin letter, just append it as is
                    output.append(c);
            }
        }

        return output.toString();
    }
}
