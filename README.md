# SiZeYuSuan2
package basic;
//lvzekun 2016/3/19
import java.util.Scanner;

public class BasicArithmetic {
	public static void main(String []args){
		//定制数量
		System.out.println("输入定制数量 ：n:");
		Scanner input=new Scanner(System.in);
		int n=input.nextInt();
		/*System.out.println("定制数量 ：n"+n);*/
		
		
		
		//判断是否乘除
			System.out.println("是否有乘除，有输入（1），无输入（0）");
			Scanner scan=new Scanner(System.in);
			int j=scan.nextInt();
			
		if(j==0)//无乘除
		{	
			System.out.println("是否有负数，有输入（1），无输入（0）");
			Scanner scanner=new Scanner(System.in);
			int j2=scanner.nextInt();
			
		for(int i=0;i<n;i++)
		{//随机分配运算符号
			System.out.println("题目");
			//随机生成数字a,b(0--100);
			int a=(int)(Math.random()*100);
			int b=(int)(Math.random()*100);
			
			
				 String  s[]={"+","-"};
					int c=(int)(Math.random()*2);
					String d=s[c];
					
				 //判断整数分数
				 int k=(int)(Math.random()*2)+1;
				 
				 if(k==1)//整数运算
				 {
					 if(j2==0)//说明没有负数
						 
					 System.out.println(a+d+b+"=");
					 
					 else//有复数运算
					 {   //分为整数运算，和负整数运算
						 int j22=(int)(Math.random()*2);
						 if(j22==1)
						 System.out.println(a+d+"("+"-"+b+")"+"=");
						 else
							 System.out.println(a+d+b+"=");
							 
				     }
				 }
				 else
				 {
					
					  int gcd=gcd(a,b);//求最大公约数
					 
						int num1=(int)(Math.random()*98)+1;
						 int num2=(int)(Math.random()*98)+1;
						 int gcd2=gcd(num1,num2);
					  System.out.println(a/gcd+"/"+b/gcd+d+num1/gcd2+"/"+num2/gcd2+"="); 
						
				 }
				 
		
		}
		}
		
		//有乘除运算
		if(j==1)
		{
		
            //判断是否有余数的除法运算j3
			System.out.println("是否有余数，有输入（1），无输入（0）");
			Scanner scanner=new Scanner(System.in);
			int j3=scanner.nextInt();
			
			//进行循环运算
			for(int i=0;i<n;i++)
			{	
				
				
			    //判断是否有括号(最多可以支持十个数参与计算)；
			
			      int j4=(int)(Math.random()*6+2);
			
				//分配运算符号
				String  s[]={"+","-","*","/"};
				int c=(int)(Math.random()*4);
				String d=s[c];
				
				//随机生成数字a,b(0--100);
				int a=(int)(Math.random()*100)+1;
				int b=(int)(Math.random()*100)+1;
				
				
			   //随机运算是除法时候判断是否有余数
				if(j3==0)//不存在余数的运算
				{
					
						int j42=(int)(Math.random()*2);
						if(j42==0)//不存在多项式运算
						System.out.println(2*a+d+a+"=");
						
						else
						{
							
							String  s2[]={"*","/"};
							int c2=(int)(Math.random()*2);
							String d2=s2[c2];
							
							if(j4==2)
							{
								System.out.println("("+b+d2+a+")"+d2+"("+2*a+d2+b+")"+"=");
							}
							if(j4==3)
							{
								
								System.out.println("("+b+d2+a+")"+d+"("+2*a+d2+b+")"+d+"("+b*2+d2+a+")"+"=");
							}
							if(j4==4){
								int w=gcd(a,b);
								System.out.println("("+b+d2+a+")"+d+"("+2*a+d2+b+")"+d+"("+b*2+d2+a+")"+d+
										"("+a/w+d2+b+")"+"=");
							}	
							if(j4==5)
							{
								int w=gcd(a,b);
								System.out.println("("+b+d2+a+")"+d+"("+2*a+d2+b+")"+d+"("+b*2+d2+a+")"+d+"("+
							a/w+d2+b+")"+d+"("+a+d2+b/w+")"+"=");
							}
						}
						
						
				    }
					else 
					{
						
						
							int j42=(int)(Math.random()*2);
							if(j42==0)//不存在多项式运算
							System.out.println(a+d+b+"=");
							else{

								String  s2[]={"*","/"};
								int c2=(int)(Math.random()*2);
								String d2=s2[c2];
								
								if(j4==2)
								{
									System.out.println("("+b+d2+a+")"+d2+"("+2*a+d2+b+")"+"+");
								}
								if(j4==3)
								{
									
									System.out.println("("+b+d2+a+")"+d+"("+2*a+d2+b+")"+d+"("+b*2+d2+a+")"+"=");
								}
								if(j4==4){
									int w=gcd(a,b);
									System.out.println("("+b+d2+a+")"+d+"("+2*a+d2+b+")"+d+"("+b*2+d2+a+")"+d+
											"("+a/w+d2+b+")"+"=");
								}	
								if(j4==5)
								{
									int w=gcd(a,b);
									System.out.println("("+b+d2+a+")"+d+"("+2*a+d2+b+")"+d+"("+b*2+d2+a+")"+d+"("+
								a/w+d2+b+")"+d+"("+a+d2+b/w+")"+"=");
								}
								
							
							
						}

							
						
					}
				}
		}
			
			
		}
			
		
		
	
	//求最大公约数构造函数
	public static int gcd(int x,int y){
		   if(y == 0)
		        return x;
	     else
		        return gcd(y,x%y);
	}

}
