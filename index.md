## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/riashrivastava/Stack/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

import java.util.Scanner;

class stacks{
	int s[] = new int[20];
	int top=-1, max;
	void input() {
		Scanner in = new Scanner(System.in);
		System.out.println("Enter the number of elements in Stack: ");
		max = in.nextInt();
	}
	
	void push(int x) 
	{
		if(top >= max-1) 
		{
			System.out.println("OverFlowing Condition");
		}
		else 
		{
			s[++top] = x;
		}
	}
	
	void pop() 
	{
		if(top == -1) 
		{
			System.out.println("UnderFlowing Condition");
		}
		else 
		{
			System.out.println("The Popped Element is : " + s[top--]);
		}
	}
	
	void display() {
		if(top == -1) 
		{
			System.out.println("Stack is Empty");
		}
		else 
		{
			System.out.println("Stack Contents are: ");
			for(int i=top;i>=0;i--) 
			{
				System.out.println(+s[i]);
			}
		}
	}
	}

public class Stack {
		public static void main(String[] args) {
		int n;
		Scanner in = new Scanner(System.in);
		stacks s = new stacks();
		s.input();
		do 
		{
			System.out.println("\nEnter 1.Push\t2.Pop\t3.Display\t4.Exit");
			System.out.println("\nEnter your choice: ");
			n = in.nextInt();
			
			switch(n) {
			case 1 : System.out.println("Enter the number to be pushed: ");
			         int p=in.nextInt();
			         s.push(p);
			         break;
			
			case 2 : s.pop();
			         break;
			         
			case 3 : s.display();
			         break;
			         
			case 4 : break;
			
			default : System.out.println("Enter a proper choice...");
			}
			
		}while(n!=4);
	}

}
