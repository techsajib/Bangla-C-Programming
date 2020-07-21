# সি গাণিতিক অপারেটর

আমরা পূর্বের পর্বে জেনেছি সি প্রোগ্রামিং এ ব্যবহৃত অপারেটর ও অপারেন্ড নিয়ে। এই পর্বে আমরা সি প্রোগ্রামিং এ ব্যবহৃত Arithmetic Operator \(গাণিতিক অপারেটর\) নিয়ে বিস্তারিত আলোচনা করব।

#### **Arithmetic Operator \(গাণিতিক অপারেটর\)**

আমরা গাণিতিক সমস্যা সমাধান করার জন্য যেই সকল অপারেটর ব্যবহার করে থাকি, সেই সকল অপারেটরকে Arithmetic Operator বা গাণিতিক অপারেটর বলে। যেমন- যোগ, বিয়োগ, গুন, ভাগ ইত্যাদি। প্রোগ্রামিং সি তে গাণিতিক সমস্যা সমাধানের জন্য এই সকল অপারেটর ব্যবহার করা হয়। সি তে ৫টি গাণিতিক অপারেটর রয়েছে যার মাঝে ‘%’ অপারেটর ছাড়া বাকি সবগুলা হচ্ছে যোগ, বিয়োগ, গুন, ভাগ। ‘%’ কে যদিও গণিতে পারসেন্টেজ বা শতকরা চিহ্ন হিসেবে ধরা হয় কিন্তু সি তে এটিকে Reminder অথবা Modulo \(মডুলো\) বলে থাকে। আবার একে মডুলাস অপারেটর বা সংক্ষেপে \(Mode\) ও বলে থাকে। এই মডুলাস অপারেটর মূলত একটি সংখ্যাকে আরেকটি সংখ্যা দিয়ে ভাগ করে যে ভাগশেষ পাওয়া যায় তা রিটার্ন করে।

**Arithmetic Operator বা গাণিতিক অপারেটর এর একটি লিস্ট ও উদাহরণ নিচে দেওয়া হল-**

|  **অপারেটর** | **নাম** | **কাজ** | **উদাহরণ** | **বাস্তব উদাহরণ** |
| :--- | :--- | :--- | :--- | :--- |
| **+**  | যোগ অপারেটর | দুটি সংখ্যা বা স্ট্রিং যোগ করার জন্য | x + y | 10 + 5 = 15 |
| - | বিয়োগ অপারেটর | ১ম সংখ্যা থেকে ২য় সংখ্যা বিয়োগ করার জন্য | x - y | 10 - 5 = 10 |
| \* | গুণ অপারেটর | দুটি সংখ্যাকে গুণ করার জন্য | x \* y | 10 \* 5 = 50 |
| / | ভাগ অপারেটর | ১ম সংখ্যাকে ২য় সংখ্যা দিয়ে ভাগ করার জন্য | x / y | 10 / 5 = 2 |
| % | ভাগশেষ অপারেটর | ১ম সংখ্যাকে ২য় সংখ্যা দিয়ে ভাগ | x % y | 10 % 5 = 0 |

Arithmetic Operator বা গাণিতিক অপারেটর কিভাবে সি প্রোগ্রামিং এ ব্যবহার করতে হয় তা জানতে নিচের প্রোগ্রামটি লক্ষ্য করুন-

```c
#include <stdio.h>
 
int main()
{
    int a = 10, b = 5;  // মানসহ ভেরিয়েবল ডিক্লারেশন  
    int addition, subtraction, multiplication, division, modulus; // ভেরিয়েবল ডিক্লারেশন 
    
    addition = a+b;         // যোগ করার জন্য 
    subtraction = a-b;      // বিয়োগ করার জন্য 
    multiplication = a*b;   // গুন করার জন্য 
    division = a/b          // ভাগ করার জন্য 
    modulus = a%b;          // ভাগশেষ করার জন্য 
    
    printf("Addition: %d\n", addition);
    printf("Subtraction: %d\n", subtraction);
    printf("Multiplication: %d\n", multiplication);
    printf("Division: %d\n", division);
    printf("Modulus: %d\n", modulus);
    
    return 0;
}
```

**আউটপুটঃ** 

```c
Addition: 15
Subtraction: 5
Multiplication: 50
Division: 2
Modulus: 0
```

**ব্যাখ্যা**

প্রথমে মেইন ফাংশনের ভিতরে আমরা ইন্টিজার ডেটাটাইপ a ও b নামে দুইটা ভেরিয়েবল নিয়েছি এবং যথাক্রমে তাদের মান 10 ও 5 দিয়েছি। এরপর আবার ইন্টিজার ডেটাটাইপ ৫টি ভেরিয়েবল addition, subtraction, multiplication, division, modulus নিয়েছি। এরপর a ও b এর যোগফল addition ভেরিয়েবলের ভিতরে রেখেছি যথাক্রমে subtraction, multiplication, division ও modulus এর কাজ করেছি। এরপর প্রত্যেকটি ভেরিয়েবলের মানকে প্রিন্ট করেছি।

এখানে সরাসরি ভেল্যু বা মান এসাইন করে দেওয়া হয়েছে। এখন আমরা যদি চাই, কিবোর্ড থেকে ইনপুট নিতে তাহলে প্রোগ্রামটি কেমন করে করতে হবে, তা জানতে নিচের কোডটি দেখুন-

```c
#include <stdio.h>
 
int main()
{
    int a, b;  //  ভেরিয়েবল ডিক্লারেশন
    int addition, subtraction, multiplication, division, modulus;
 
    //  কিবোর্ড থেকে ইনপুট নেওয়ার জন্য
    printf("Enter first value: ");
    scanf("%d", &a);
    printf("Enter second value: ");
    scanf("%d", &b);
 
    addition = a+b;         // যোগ করার জন্য
    subtraction = a-b;      // বিয়োগ করার জন্য
    multiplication = a*b;   // গুন করার জন্য
    division = a/b;          // ভাগ করার জন্য
    modulus = a%b;          // ভাগশেষ করার জন্য
 
     // সবগুলো মান প্রিন্ট করার জন্য 
    printf("Addition: %d\n", addition);
    printf("Subtraction: %d\n", subtraction);
    printf("Multiplication: %d\n", multiplication);
    printf("Division: %d\n", division);
    printf("Modulus: %d\n", modulus);
 
    return 0;
}
```

**Tags:** _Arithmetic Operator \(গাণিতিক অপারেটর\), সি প্রোগ্রামিং_

