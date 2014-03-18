Java-Program
============

package ata_work;

 class ThreadAddSubMul extends Thread{
	 
	 int a=10,b=20,c;
	 public void run(){
		 
		 this.add();
		 
		 
		 
	 }
	 public void add(){
		 
		 c= (a+b);
		 System.out.println("sum"+c);
		 
	 }
 }
 class Sub extends ThreadAddSubMul{
	
	 
	 
    public void run(){
		 
		 this.sub();
     }
    public void sub(){
		 
		 c= (a-b);
		 System.out.println("sum"+c);
		 
	 }
 }


public class AddSubMul {
	
	public static void main(String a[]){
		
		ThreadAddSubMul ob1=new ThreadAddSubMul();
		ob1.start();
		Sub ob2=new Sub();
		ob2.start();
		
	}

}
