import java.util.Scanner;   
public class L1_002 {
     public static void main(String[] args){
         Scanner sc=new Scanner(System.in);  
         String input=sc.nextLine();   
         String[] ss=input.split(" ");   
         sc.close(); 
         int num=Integer.parseInt(ss[0]);   
         String code=ss[1];  
         int sum=0;  
         int sign =0;  
         if(num==1){  
             System.out.println(code);  
             System.out.println(0);  
             return;  
         }  
           
         for (int i = 1; i < num; i=i+2) {  
             sum+=i;  
            if(sum>num/2){  
                sign=i-2;   
                sum=(sign+1)/2 * (sign+1)-1;  
                break;  
            }  
        }   
         for (int i = sign; i > 0 ; i=i-2) {  
            for (int j = 0; j < (sign-i)/2; j++) {  
                System.out.print(" ");  
            }  
            for (int j = 0; j < i; j++) {  
                 System.out.print(code);  
            }  
            System.out.println();  
        }  
         for (int i = 3; i <= sign ; i=i+2) {  
                for (int j = 0; j < (sign-i)/2; j++) {  
                    System.out.print(" ");  
                }  
                for (int j = 0; j < i; j++) {  
                     System.out.print(code);  
                }  
                System.out.println();  
        }  
         System.out.println(num-sum);  
    }   
} 
