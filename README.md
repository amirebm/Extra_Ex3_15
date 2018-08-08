# Extra_Ex3_15

/*
Revise Listing 3.8, Lottery.java, to generate a lottery of a threedigit
number. The program prompts the user to enter a three-digit number and
determines whether the user wins according to the following rules:
1. If the user input matches the lottery number in the exact order, the award is
$10,000.
2. If all digits in the user input match all digits in the lottery number, the award is
$3,000.
3. If one digit in the user input matches a digit in the lottery number, the award is
$1,000. */



package com.personal.Extra3_15;

import java.util.Scanner;

public class Extra3_15 {

	public static void main(String[] args) {
		
				int lottery=(int)(Math.random()*899 ) +100 ;
				int result;
		
		char[] lot = (""+ lottery).toCharArray();
		 Scanner sc = new Scanner(System.in);
		 System.out.println
	      ("Enter a 3 digit number and take your chance to win ");
		 System.out.println(lottery);
		
			int getNum= sc.nextInt();
			char[] chance = (""+ getNum).toCharArray();
			
			
			result=lotteryMethod(lot, chance);
			System.out.println(result);
			if(result==3)
				System.out.print
			      ("You Win 10000$");
			else if (result==2)
				System.out.print
			      ("You Win 3000$");
			else if(result==1)
				System.out.print
			      ("You Win 1000$");
			else 
				System.out.print
			      ("You do not win");
				
	}
	
	 static int lotteryMethod(char[] x,char[] y) {
		 
		 int prize1=0,prize2=0;

		  for (int i = 0; i < x.length; i++) {
			 
			  if (x[i]==y[i])
				  prize1++;
					  
        	 for (int j = 0; j < y.length; j++) {
				if(x[i]==y[j]) {
				 prize2++;
				 break;
	       		}
        	 }}
        	 if (prize1==3)
        	     return 3;	 
        	 
        	 
        	 if (prize2== 1) 
        		return 1;
        	 
        	 
		  if(prize2==3)
			  return 2;
		  
		  return 0;
		  
         
		
	 }
}


