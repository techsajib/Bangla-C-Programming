# nested if স্টেটমেন্ট

আমরা পূর্বের পর্বে জেনেছি সি প্রোগ্রামিং এর if- else Ladder statement নিয়ে। এই পর্বে আমরা সি প্রোগ্রামিং এর ডিসিশন মেকিং স্টেটমেন্টের nested if-else স্টেটমেন্ট নিয়ে বিস্তারিত আলোচনা করব।

আমরা আগে if- else ও if- else Ladder স্টেটমেন্ট নিয়ে কাজ করেছি, এখন আমরা nested if-else স্টেটমেন্ট নিয়ে কাজ করব। if- else ও nested if-else স্টেটমেন্ট এর মাঝে তেমন কোনো বিশেষ পার্থক্য নাই। nested if-else স্টেটমেন্ট এর ভেতরে এক বা একাধিক if-else স্টেটমেন্ট নিয়ে কাজ করা যায়। আমাদের কোডিং এর স্বার্থে প্রায়ই সময় if-else স্টেটমেন্টের ভিতরে একাধিক if-else স্টেটমেন্ট নিয়ে কাজ করতে হয়। এই সমস্যা সমাধানের জন্যই মূলত nested if-else স্টেটমেন্টের ধারণা আসে।

#### nested if-else স্টেটমেন্ট এর সিনট্যাক্স

```c
if(condition1) 
{

    if(condition2) 
    {
       statements
    }
    else 
    {
       statements
    }
}else 
{
    statements
}
```

নেস্টেড if-else এর ব্যবহার বুঝতে নিচের সি প্রোগ্রাম গুলো লক্ষ্য করুন-

```c
#include <stdio.h>

int main()
{
   int x, y;
   
   printf("Enter 2 number: ");
   scanf("%d %d", &x, &y);
   
   if(x == y)
   {
       if(y == x)
       {
           printf("Number is Similar!\n");
       }
   }else
    {
        printf("Number is not Similar!\n");
    }
   
   return 0;
}
```

#### আউটপুট 

```c
Enter 2 number: 55 55 
Number is Similar!
```

বড় নাম্বার বের করার জন্য নেস্টেড if-else এর ব্যবহার

```c
#include <stdio.h>

int main()
{
    int x, y;
    
    printf("Enter 2 number: ");
    scanf("%d %d", &x, &y);
    
    if(x != y)
    {
        printf("%d is not equal to %d!\n", x, y);
        
        if(x > y)
            printf("%d is Biggest!\n", x);
        else
            printf("%d is Biggest!\n", y);
    }else
    {
        printf("%d is equal to %d!\n", x, y);
    }
    

    return 0;
}
```

#### আউটপুট 

```c
Enter 2 number: 5 50 
5 is not equal to 50! 
50 is Biggest!
```

