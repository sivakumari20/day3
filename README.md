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
***string manipulatin operations***
package First_one;

import java.util.Scanner;
import java.lang.String;
import java.util.ArrayList;

public class stringmanipulations {

	public static void main(String[] args) {
		
		// TODO Auto-generated method stub
		Scanner sc=new Scanner(System.in);
		System.out.println("enter the  string ");
		String str=sc.nextLine();
        String[] str1=str.split(" ");
        ArrayList<String> reversedwords =new ArrayList<>();
        String vowel="aeiouAEIOU";
        int count =0;
        int wordcount=0;
       
        for (String c:str1)
		{
			wordcount++;
			for(char ch :c.toCharArray())
			{
				if(vowel.contains(String.valueOf(ch)))
				{
			     count++;
			}
			}
			StringBuilder sb=new StringBuilder(c);
			String y=sb.reverse().toString();
			reversedwords.add(y);
			
		}
	for(String a :reversedwords)
	{
		System.out.print(a +" ");
	}
	System.out.println(" ");
	System.out.println(" no of vowels " + count);
	System.out.println(" no of words " + wordcount);

}
}
***bubblesort***
package First_one;

import java.util.Scanner;    //timecomplexity =0[n^2]

public class bubblesort {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc=new Scanner(System.in);
		System.out.println("enter the size of the array");
		int x=sc.nextInt();
		int[] arr=new int [x];
		System.out.println("enetr the ellements of the array");
		for(int i=0;i<x;i++)
		{
			int y=sc.nextInt();
			arr[i]=y;
		}
		for (int i=0;i<x-1;i++)
		{
			for(int j=0;j<x-i-1;j++)
			{
				if(arr[j+1]<arr[j])
				{
					int temp=arr[j];
					arr[j]=arr[j+1];
					arr[j+1]=temp;
				}
			}
			
		}
	for(int i=0;i<=x;i++)
	{
		System.out.print(arr[i]+ " ");
	}

}
}
***selection sort***
package First_one;

import java.util.Scanner;  outer loop =n,innerloop =n,time complexity =o[n^2]

public class selectionsort {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc=new Scanner(System.in);
		System.out.println("enter the size of the array");
		int x=sc.nextInt();
		int[] arr=new int [x];
		System.out.println("enetr the ellements of the array");
		for(int i=0;i<x;i++)
		{
			int y=sc.nextInt();
			arr[i]=y;
		}
		for(int i=0;i<x-1;i++)
		{
			int smallest=i;
			for (int j=i+1;j<x;j++)
			if(arr[smallest]>arr[j])
			{
				smallest =j;
			}
			int temp=arr[smallest];
			arr[smallest]=arr[i];
			arr[i]=temp;
		}
		for (int i=0;i<x;i++)
		{
			System.out.print(arr[i]+ " ");
		}
	}

}

***insertion sort***
package First_one;

import java.util.Scanner;

public class insertionsort {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		//sorted part,unsorted part 
		// initialize i=0 as sorted past
		//remaining unsorted
		Scanner sc=new Scanner(System.in);
		System.out.println("enter the size of the array");
		int x=sc.nextInt();
		int[] arr=new int [x];
		System.out.println("enetr the ellements of the array");
		for(int i=0;i<x;i++)
		{
			int y=sc.nextInt();
			arr[i]=y;
		}
		for(int i=1;i<x;i++)
		{
			int current =arr[i];
			int j=i-1;
			while(j>=0 && current <arr[j]) // checking the condition for traversal
			{
				arr[j+1]=arr[j]; // for shifting elements
				j--;
			}
			arr[j+1]=current; // for inserting elements
			
		}
		for (int i=0;i<x;i++)
		{
			System.out.print(arr[i]+ " ");
		}

	}
 ***sum of digits***
}
package First_one;

public class sumofdigits {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int x=65;
		int sum=0;
		while(x>0)
		{
			int y=x%10;
			sum=sum+y;
			x=x/10;
		}
        System.out.println(sum);
	}

}
***transpose of a matrix***
package First_one;

import java.util.Scanner;

public class matrixtranspose {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc =new Scanner(System.in);
		System.out.println("enter a number");
		int x=sc.nextInt();//no of rows of 1
		System.out.println("enter a number");
		int y=sc.nextInt();//no of colomns of 1
		
		int[][] matrix1=new int [x][y];
		int[][] matrix2=new int [x][y];
		System.out.println("enetr elements of first matrix");
		int i=0;int j=0;
		for (i=0;i<x;i++)
			{
				for ( j=0;j<y;j++)
				{
					 matrix1[i][j]=sc.nextInt();
				}
			}
		for (i=0;i<x;i++)
		{
			for ( j=0;j<y;j++)
			{
				 matrix2[i][j]=matrix1[j][i];
			}
		}
	for (i=0;i<x;i++)
	{
		for ( j=0;j<y;j++)
		{
System.out.print(matrix2[i][j]);

}
System.out.println();

}
	}
}


