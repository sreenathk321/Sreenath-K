# Sreenath-K
Program 1 Problem-1: Create a small calculator which performs operations such as Addition, Subtraction, Multiplication and Division using class.   Calculator inputs :> ‘a’, ‘b’ and ‘type of operation’   Datatype :> ‘a’ = double, ‘b’ = double, ‘type of operation’ = string

import java.util.*;
public class Calculator{
  public static void main(String[] args){
    Scanner sc=new Scanner(System.in);
    System.out.print("Enter first number: ");
    double a=sc.nextDouble();
    System.out.print("Enter second number: ");
    double b=sc.nextDouble();
    sc.nextLine();
    String opp="";
    System.out.println(Addition);
    System.out.println(Subtraction);
    System.out.println(Multiplication);
    System.out.println(Division);
    String opp="";
    switch(opp){
    case "Addition":
          System.out.println(a+b);
          break;
    
    case "Subtraction":
          System.out.println(a-b);
          break;
    
    case "Multiplication":
          System.out.println(a*b);
          break;
    
    case "Division":
         if (b != 0) {
                    System.out.println("Result: " + (a / b));
                } else {
                    System.out.println("Error: Division by zero");
                }
                break;
    
    default: System.out.println("Error");
    }
    
  }
}


Problem-2: With a single integer as the input, generate the following until a = x [series of numbers as shown in below examples]
 
  Output: (examples)
    1) input a = 1, then output : 1
    2) input a = 2, then output : 1, 3Number
    3) input a = 3, then output : 1, 3, 5
    4) input a = 4, then output : 1, 3, 5, 7
    .
    .
    5) input a = x, then output : 1, 3, 5, 7, .......


import java.util.*;
public class Number{
  public static void main(String[] args){
    Scanner sc=new Scanner(System.in);
      int a=sc.nextInt();
      int num;
      for(int i=1;i<=a;i++){
        num=i*2-1;
        System.out.print(num);
        System.out.print(", ");
      }
}
}




Problem-3: With a single integer as the input, generate the following until a = x [series of numbers as shown in below examples]     Output: (examples)     1) input a = 1, then output : 1     2) input a = 2, then output : 1     3) input a = 3, then output : 1, 3, 5     4) input a = 4, then output : 1, 3, 5     5) input a = 5, then output : 1, 3, 5, 7, 9     6) input a = 6, then output : 1, 3, 5, 7, 9     .     .     7) input a = x, then output : 1, 3, 5, 7, .......

import java.util.Scanner;

public class Problem3Series {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int a = sc.nextInt();

       
        if (a % 2 == 0) {
            a = a - 1;
        }

        for (int i = 1; i <= a; i++) {
            int odd = 2 * i - 1;
            System.out.print(odd);
            if (i < a) {
                System.out.print(", ");
            }
        }

       
    }
}



Problem-4: Get the total count of number listed in the dictionary which is multiple of [1,2,3,4,5,6,7,8,9]   (examples)   input: [1,2,8,9,12,46,76,82,15,20,30]   Output:      {1: 11, 2: 8, 3: 4, 4: 4, 5: 3, 6: 2, 7: 0, 8: 1, 9: 1}

import java.util.*;

public class Problem4 {
    public static void main(String[] args) {
        int[] input = {1, 2, 8, 9, 12, 46, 76, 82, 15, 20, 30};
        Map<Integer, Integer> multiplesCount = new LinkedHashMap<>();

        for (int i = 1; i <= 9; i++) {
            multiplesCount.put(i, 0);
        }
        for (int i = 1; i <= 9; i++) {
            int count = 0;
            for (int num : input) {
                if (num % i == 0) {
                    count++;
                }
            }
            multiplesCount.put(i, count);
        }
        System.out.println(multiplesCount);
    }
}
