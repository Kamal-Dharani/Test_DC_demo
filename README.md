# Test_DC_demo
These are demo programs of palindrome, reverse string and OOP related program

// Palidrome
/**
 * Palindrome is performed.
 */
package palindrome;

import java.util.Scanner;

/**
 * @author Kamal Dharani
 * 
 */
public class Palindrome {

public static void main(String[] args){

    Scanner keyboard = new Scanner(System.in);
    System.out.println("Enter a string to check if it is a palindrome");
    String word = keyboard.nextLine();

    if(isPalindrome(word))
        System.out.println(word + " is a Palindrome");
    else
        System.out.println(word + " is not a Palindrome" );


}


public static boolean isPalindrome(String word){
    int length = word.length();
    // loop until i reaches the midpoint index
    for(int i = 0; i < length/2 ; i++){
        //compare first char with last, second with second last
        //and so on until it reaches the mid point
        if(word.charAt(i) != word.charAt(length-i-1))
            return false;
    }
    return true;
}
}

// Reverse
/**
 * Reversing the String is performed.
 */
package reverse;

/**
 *
 * This program is used for Reversing the String.
 */
import java.io.*;

public class reverseString {
    public static void main(String[] args) {
        String input="";
        System.out.println("Enter the input string");
        try
        {
            /**
             * BufferedReader is used here
             * @see BufferReader.
             */
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            input = br.readLine();
            char[] try1= input.toCharArray();
            for (int i=try1.length-1;i>=0;i--)
            System.out.print(try1[i]);
        }
        catch (IOException e) {
            e.printStackTrace();
        }
}}
