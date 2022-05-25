# Day-4-Class-vs.-Instance-HackerRank
https://www.hackerrank.com/challenges/30-class-vs-instance/problem patika.dev


<img width="1003" alt="Ekran Resmi 2022-05-25 17 07 26" src="https://user-images.githubusercontent.com/105243448/170282154-07778fda-d674-41f4-9bfa-82eb1aa5e448.png">






```

using System;
using System.Collections.Generic;
using System.IO;

class Person {
    public int age;     
    public Person(int initialAge) {
        // Add some more code to run some checks on initialAge
        
        if(initialAge>0){
            age = initialAge;
        }else{
            age = 0;
            Console.WriteLine("Age is not valid, setting age to 0.");
            
        }
        
     }
     
     public void amIOld() {
        if(age<13){
            Console.WriteLine("You are young.");
        }
        if(age<18 && age >= 13){
            Console.WriteLine("You are a teenager.");
        }
        
         if(age>= 18){
            Console.WriteLine("You are old.");
        }
        
        

     }

     public void yearPasses() {
        // Increment the age of the person in here
        age++;
     }

static void Main(String[] args) {
        int T=int.Parse(Console.In.ReadLine());
        for (int i = 0; i < T; i++) {
            int age=int.Parse(Console.In.ReadLine());
            Person p=new Person(age);
             p.amIOld();
                for (int j = 0; j < 3; j++) {
                  p.yearPasses();
                }
                p.amIOld();
                Console.WriteLine();
        }
    }
}
```
