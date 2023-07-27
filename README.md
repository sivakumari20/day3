# day3
***primenumbersintherange***

package First_one;

import java.util.Scanner;

public class primenumberintherange {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc=new Scanner(System.in);
		System.out.println("enter the first number");
		int x=sc.nextInt();
		System.out.println("enter the last number");
		int y=sc.nextInt();
		
		int[] arr =new int[y];
		int j=0;
		for (int i=x;i<y;i++)
		{
			boolean isprime=true;
			for(j=2;j<=i/2;j++)
			{
			if (i%j==0)
			{
				isprime=false;
				break;
			}
		}
			if(isprime)
			{
				
			System.out.print(i +" ");
				
			}
		}

	}

}
