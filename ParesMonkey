import java.util.ArrayList;
import java.util.Arrays;
import java.util.Scanner;
import java.util.Random;

public class ParesMonkey{ 
        static String[] suits = {"(♠)", "(♥)", "(♦)" ,"(♣)"};
        static String[] ranks = {"A","2","3","4","5","6","7","8","9","10","J","Q","K"};       
        static String[] deck = new String[52];  
        static int coinToss; 
       static String[] total;

       ParesMonkey(){
          
       }
     
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);  
        System.out.print("Cards         : ");
            for(int i=0; i<deck.length; i++)
            {
                deck[i] = ranks[i%13] + " of " + suits[i/13];    
                    System.out.print(deck[i] + " ");
                total = deck;
            }
                    System.out.println("\nRemaining Cards : " + total.length);
                    System.out.println("No Duplicate card found.");
            ArrayList <String> deckCard = new ArrayList<>(Arrays.asList(total));
                pickOne(deckCard);
                    System.out.print("Remaining Cards : " + deckCard.size() + " \nCards         : ");
                 for(int i=0; i<deckCard.size(); i++){
                    System.out.print(deckCard + " ");
                    }
                    System.out.println("\nLets start the game!!!!");
                System.out.println("\nDistributed Cards.....\t" + deckCard.size() + ", remaining cards...");
    // shuffle deck
    for (int i = 0; total.length < deckCard.size(); i++) {
        int r = i + (int) (Math.random() * (deckCard.size()-total.length));
        String temp = deck[r];
        deck[r] = deck[total.length];
        deck[total.length] = temp;
    }
    for (int i = 0; i < 2; i++) {
        System.out.println("** Player " + (i + 1) + " **");
        for (int j = 0; j < 25; j++) {
            System.out.println(deck[i + j * 2]);// this is the result of distribution dont delete.
        }

        
      scan.close();
    }
}
            //main class

    public static ArrayList<String> pickOne(ArrayList<String> deckCard) {
        Random r = new Random();
        int oneCard = r.nextInt(deckCard.size());
            System.out.println("Selected Card : " + deckCard.get(oneCard) + ", got picked. " + "\nPicked Card   : " + 
                                deckCard.remove(oneCard) + ", has been hidden.");
        return deckCard;// the removed card
    } 

}
