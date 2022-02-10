---
title: "Week2 Coding"
date: 2022-02-11T00:39:45+07:00
draft: false
tags: ['exam']
categories: ['data structure','algorithm']
---
[![img](/blog/pdf.png)](/blog/pdf/week2_algorithmic_warmup.pdf)
## Fibonacci Number
```java
import java.util.Scanner;

public class w2_lab01 {
    public static long fibofasterway(int m){
        if(m<2)
            return m;
        long[] f = new long[m+1];
        f[0]=0;
        f[1]=1;
        for(int i=2;i<=m;i++){
            f[i] = f[i-1]+f[i-2];
        }
        return f[m];
    }
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();
        scan.close();
        if(n>=0&&n<=45)
        System.out.println(fibofasterway(n));
        
    }
}
```

## Last Digit of a Large Fibonacci Number
```java
import java.util.Scanner;
public class w2_lab02 {
    public static long fibolastway(int m){
        if(m<2)
            return m;
        long[] f = new long[m+1];
        f[0]=0;
        f[1]=1;
        for(int i=2;i<=m;i++){
            f[i] = (f[i-1]+f[i-2])%10;
        }
        return f[m];
    }
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();
        scan.close();
        if(n>=0&&n<=Math.pow(10,7))
        System.out.println(fibolastway(n));
    }
}
```

## Greatest Common Divisor
```java
import java.util.Scanner;
public class w2_lab03 {
    public static int gcd(int a,int b){
        if(b==0)
            return a;
        int Aprime = a%b;
        return gcd(b,Aprime);
   }
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int a = scan.nextInt();
        int b = scan.nextInt();
        scan.close();
        if((a>=1&&a<=(2*Math.pow(10,9)))&&(b>=1&&b<=(2*Math.pow(10,9)))){
            System.out.println(gcd(a,b));
        }
    }
}
```

## Least Common Multiple
```java
import java.util.Scanner;
public class w2_lab04 {
    public static long gcd(int a,int b){
        if(b==0)
            return a;
        int Aprime = a%b;
        return gcd(b,Aprime);
   }
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int a = scan.nextInt();
        int b = scan.nextInt();
        scan.close();
        if((a>=1&&a<=(2*Math.pow(10,9)))&&(b>=1&&b<=(2*Math.pow(10,9)))){
            long output = ((long)a*b)/gcd(a,b);
            System.out.println(output);
        }
    }
}
```

##  Fibonacci Number Again
```java
import java.util.Scanner;
public class w2_lab05 {
    public static long pisano(long m){
    long prevIndex = 0;
    long currIndex = 1;
    long result = 0;
    for(int i = 0; i < m * m; i++){
        long temp = 0;
        temp = currIndex;
        currIndex = (prevIndex + currIndex) % m;
        prevIndex = temp;
        if (prevIndex == 0 && currIndex == 1)
            result= i + 1;
    }
    return result;
}
public static long fibocrazyway(long n,long m){
    long pisanoPeriod = pisano(m);
    n = n%pisanoPeriod;
    long prevIndex = 0;
    long currIndex = 1;
    if(n==0)
        return 0;
    else if(n==1)
        return 1;
    for(int i=0;i<n-1;i++){
        long temp = 0;
        temp = currIndex;
        currIndex = (prevIndex + currIndex) % m;
        prevIndex = temp;
    }
    return currIndex%m;
}
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        long n = scan.nextLong();
        long m = scan.nextLong();
        scan.close();
        if((n>=1&&n<=Math.pow(10,14))&&(m>=2&&m<=Math.pow(10,3)))
        System.out.println(fibocrazyway(n,m));
    }
}
```

### Last Digit of the Sum of Fibonacci Numbers
```java
import java.util.Scanner;

public class w2_lab06 {
    public static long pisano(long m){
        long prevIndex = 0;
        long currIndex = 1;
        long result = 0;
        for(int i = 0; i < m * m; i++){
            long temp = 0;
            temp = currIndex;
            currIndex = (prevIndex + currIndex) % m;
            prevIndex = temp;
            if (prevIndex == 0 && currIndex == 1)
                result= i + 1;
        }
        return result;
    }
    public static long fibolastsumway(long n){
        long pisanoPeriod = pisano(10);
        n = n%pisanoPeriod;
        long prevIndex = 0;
        long currIndex = 1;
        long sum=0;
        if(n==0)
            return 0;
        else if(n==1)
            return 1;
        for(int i=0;i<n-1;i++){
            long temp = 0;
            temp = currIndex;
            currIndex = (prevIndex + currIndex) % 10;
            prevIndex = temp;
            sum = sum+currIndex;
        }
        return (sum+1)%10;
    }
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        long n = scan.nextLong();
        scan.close();
        if(n==0)
        System.out.println(n);
        if((n>=1&&n<=Math.pow(10,14)))
        System.out.println(fibolastsumway(n));
        
    }
}

```

### Last Digit of the Sum of Fibonacci Numbers Again
` `

### Last Digit of the Sum of Squares of Fibonacci Numbers
```java
import java.util.Scanner;

public class w2_lab08 {
    public static long pisano(long m){
        long prevIndex = 0;
        long currIndex = 1;
        long result = 0;
        for(int i = 0; i < m * m; i++){
            long temp = 0;
            temp = currIndex;
            currIndex = (prevIndex + currIndex) % m;
            prevIndex = temp;
            if (prevIndex == 0 && currIndex == 1)
                result= i + 1;
        }
        return result;
    }
    public static long fibolastsumway(long n){
        long pisanoPeriod = pisano(10);
        n = n%pisanoPeriod;
        long prevIndex = 0;
        long currIndex = 1;
        long sum=0;
        if(n==0)
            return 0;
        else if(n==1)
            return 1;
        for(int i=0;i<n-1;i++){
            long temp = 0;
            temp = currIndex;
            currIndex = (prevIndex + currIndex) % 10;
            prevIndex = temp;
            sum = (sum+(int)Math.pow(currIndex,2))%10;
        }
        return (sum+1)%10;
    }
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        long n = scan.nextLong();
        scan.close();
        if(n==0)
        System.out.println(n);
        if((n>=1&&n<=Math.pow(10,14)))
        System.out.println(fibolastsumway(n));
        
    }
}
```

