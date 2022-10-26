# lab01
\\exercitiu din lucrarea 4  
import java.util.*;

class Main{

   public static void main(String[] args)  {

       //This creates a Scanner Object

       Scanner input=new Scanner(System.in);

       //This declares and initializes all integer variables

       int num, count =0, sum = 0, max = Integer.MIN_VALUE; int min = Integer.MAX_VALUE;

       //This declares and initializes the average variable

       float avg =0;

       //The following is repeated until the user enters 99

       do{

           //Prompts the user for a score

           System.out.print("Score: ");

           //Get input for score

           num =input.nextInt();

           //Inputs less than 0 or greater than 10 are invalid

           if (num < 0 || num >10){

               System.out.println("Invalid input");

           }

           //For valid inputs

           else{

               //This keeps count of valid inputs

               count++;

               //This adds valid inputs

               sum+=num;

               //This gets the maximum of valid inputs

               if(num > max){

                   max = num;

               }

               //This gets the minimum of valid inputs

               if(num < min){

                   min = num;

               }

           }

       }

       while(num != 99);

       //Calculate average

       avg= sum/count;

       //Print the highest score

       System.out.println("Highest: " +max);

       //Print the least score

       System.out.println("Lowest: "+min);

       //Print the average score

       System.out.println("Average: "+avg);

}

}

