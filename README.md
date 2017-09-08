# PrimeFactors

Write a Java program that is reading from the keyboard a value between 100 and 700 and is printing on the screen the prime factors  of the number.

Your program should use a cycle for validating the input (if the value typed from the keyboard is less than 100 or bigger than 700 to print an error and ask the user to input another value).

Also the program should print the divisors in the order from smallest to biggest. 

import java.util.Scanner;
public class Primefactors
{
 
    public static void main (String[] args)
    {
        int i;
	Scanner in = new Scanner(System.in);
	
	while(true)
	{
		System.out.println("Enter a Value:  ");
        	i = in.nextInt();
		if(i<100 || i>700)
		{
			System.out.println(" Error: Please enter the correct value!");
			
		}	
 		else
			break;
	}
	
	System.out.printf("\n");

	for( int j=2; j<i; j++)
	{
		if(i%j == 0)
		{
			int x;
			System.out.printf(i + "=");
			System.out.printf(j + "");
			x = i/j;
			while(true)
			{
				for(int a=2; a<=x; a++)
				{	
					if(x%a == 0)	
					{
						System.out.printf( "*" + a);
						x = x/a;	
						break;	
					}
				}
				if(x==1)
				{
					System.out.println();
					break;
				}
			}
			break;
		}	
	}
    }
}
