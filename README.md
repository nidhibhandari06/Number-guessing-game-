# Number-guessing-game-
import java.util.Scanner;
public class Game
{
       //implementing function
       public static void
       GuessingNumberGame()                             //Creatin Guessing number game function
    {
        int number;
       
        Scanner sc =new Scanner(System.in);        //scanner class
       
          number = 1+(int)(100*Math.random());       //generate the number 

          System.out.println("Chose the number.");
          System.out.println("The number is in between 1 to 100.");
          System.out.println("With in 5 trials.");
        
          int k=5,i,guess;                                  //k is number of trails 

          for(i=1;i<=(k+1)-1;i++)
          {
            System.out.println("Guess The Number?? :-");

            guess=sc.nextInt();                            //calling the object
            
            if(number==guess)
            {
                System.out.println("Congratularions!! You guess the number");
                break;
            }
            if (guess>=101){
                System.out.println("The number is grater than 100??"+" "+ "Plese enter the number less than 101");
                
            }
            if(guess<=-0)
            {
                System.out.println("The number is 'Nigetive'!");
                System.out.println("Plese enter the 'Positive' number!");
            }

            else if(number > guess && i !=k)
            {
                 System.out.println("The number is greater than "+guess);
            }

            else if(number < guess && i !=k)
            {
                System.out.println("The number is less than "+guess);
            }

            if (i==k)
            {
                System.out.println( "Sorry! you can not guess the number??");
                 break;
            }
        }
    }
         public static void  main(String []args)       //Main function
         {
            GuessingNumberGame();                          //calling the Gussing number function 
        
         }
         
    }
