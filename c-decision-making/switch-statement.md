# switch-case স্টেটমেন্ট

আমরা পূর্বের পর্বে জেনেছি সি প্রোগ্রামিং এর nested if-else statement নিয়ে। এই পর্বে আমরা সি প্রোগ্রামিং এর switch case স্টেটমেন্ট নিয়ে বিস্তারিত আলোচনা করব।

আমাদের প্রায়ই সময় বিভিন্ন জটিল আর সময়সাধ্যমূলক প্রোগ্রামিং সমস্যা সমাধান করতে হয়। প্রোগ্রামে অনেকগুলো কন্ডিশন নিয়ে কাজ করার জন্য আমরা if-else অথবা if-else লেডার স্টেটমেন্ট নিয়ে কাজ করি কিন্তু শুধু if-else স্টেটমেন্ট ব্যবহার করে প্রোগ্রাম লেখা প্রোগ্রামারদের কাছে অনেক বিরক্তিকর বা সময়সাধ্য ব্যাপার। এই জন্য তাদের ভিন্ন পথ অবলম্বন করতে হয়, আর সেটা হচ্ছে switch case স্টেটমেন্ট।

switch case স্টেটমেন্টের সাহায্যে আপনি একটা নির্দিষ্ট ভ্যালুর উপর নির্ভর করে অনেকগুলা স্টেটমেন্ট নিয়ে কাজ করতে পারবেন আর এটাই হচ্ছে এই স্টেটমেন্টের সবচেয়ে বড় উপকারিতা।

#### switch case স্টেটমেন্টের সিনট্যাক্স

```c
switch (expression) 
{
    case value 1:
        statement;
        break;
        
    case value 2:
        statement;
        break;
        
    case value 3:
        statement;
        break;
    .
    .
    default:
        statement;
        break;
}
```

#### ব্যাখ্যা

এখানে switch স্টেটমেন্টের expression বা condition এর সাথে case value 1 এর স্টেটমেন্ট মিলে গেলে, এটি এক্সিকিউট হবে নতুবা break মানে এই স্টেটমেন্ট থেকে বের হয়ে আসবে। এরপর case value 2 এর স্টেটমেন্ট মিলে গেলে, এটি এক্সিকিউট হবে নতুবা break হয়ে আসবে, একইভাবে case value 3 চেক করবে। এইভাবে যতগুলা স্টেটমেন্ট থাকবে সবগুলা চেক করবে। যদি কোনো স্টেটমেন্টের সাথে কাঙ্ক্ষিত ফলাফল না মিলে তাহলে default ভেল্যু রিটার্ন করবে।

আরো সহজ কথায়, expression এর সাথে যে case value মিলে যাবে, সেই কোড ব্লকটি রিটার্ন হবে অন্যথায় default ভেল্যু রিটার্ন হবে।

#### **switch case স্টেটমেন্ট বুঝার জন্য নিচের সি প্রোগ্রামটি লক্ষ্য করুন-**

```c
#include <stdio.h>

int main()
{
    int number;
    
    printf("Enter a Number: ");
    scanf("%d", &number);
    
    switch(number)
    {
        case 0:
            printf("You Enter 0. \n");
            break;
            
        case 1:
            printf("You Enter 1. \n");
            break;
        
        case 2:
            printf("You Enter 2. \n");
            break;
        
        case 3:
            printf("You Enter 3. \n");
            break;
            
        case 4:
            printf("You Enter 4. \n");
            break;
            
        case 5:
            printf("You Enter 5. \n");
            break;
        
        default:
            printf("You Enter more than 5. \n");
            break;
    }

    return 0;
}
```

#### আউটপুট

```c
Enter a Number: 6
You Enter more than 5.
```

#### ব্যাখ্যা

এখানে প্রথমে আমরা ইন্টিজার টাইপ একটা ভেরিয়েবল কিবোর্ড থেকে ইনপুট নিলাম। এরপর switch এক্সপ্রেশনে ভেরিয়েবলটিকে কল করলাম। তারপর case 0 তে এক ধরণের স্টেটমেন্ট দিলাম এরমানে যদি কেউ কিবোর্ড থেকে 0 ইনপুট দেই তাহলে case 0 স্টেটমেন্ট এক্সিকিউট হবে। এইভাবে case 1, 2, 3, 4, 5 চলবে যদি এদের কারো সাথে switch এক্সপ্রেশন না মিলে তাহলে default স্টেটমেন্ট এক্সিকিউট হবে।

#### এখন আমরা যদি ৭ দিনের নাম switch case স্টেটমেন্ট ব্যবহার করে প্রিন্ট করতে চাই তাহলে-

```c
#include <stdio.h>

int main()
{
    int day;
    
    printf("Enter a Number (1-7): ");
    scanf("%d", &day);
    
    switch(day)
    {
        case 1:
            printf("Saturday! \n");
            break;
        
        case 2:
            printf("Sunday! \n");
            break;
        
        case 3:
            printf("Monday! \n");
            break;
            
        case 4:
            printf("Tuesday! \n");
            break;
            
        case 5:
            printf("Wednesday! \n");
            break;
            
        case 6:
            printf("Thursday! \n");
            break;
            
        case 7:
            printf("Friday! \n");
            break;
        
        default:
            printf("Invalid Input! Only input 1-7! \n");
            break;
    }

    return 0;
}
```

#### আউটপুট

```c
Enter a Number (1-7): 7 
Friday!
```

একইভাবে, আমরা যদি ১২ মাসের নাম প্রিন্ট করতে চাই তাহলে আমাদের কোডের ধরণ কেমন হবে ? এখন একটু কমপ্লেক্স কোড করার চেষ্টা করি, এইবার যে মাস হবে তার নামের প্রথম ছোট অথবা বড় হাতের অক্ষর কিবোর্ড থেকে ইনপুট দিলে, সেই নামের সবগুলা মাস প্রিন্ট হবে। যেমন- A ইনপুট দিলে April, August প্রিন্ট হবে। আসুন কোড গুলো লক্ষ্য করি-

```c
#include <stdio.h>

int main()
{
    char month;
    
    printf("Enter a first character of month: ");
    scanf("%c", &month);
    
    switch(month)
    {
        case 'j':
        case 'J':
            printf("January, June & July! \n");
            break;
        
        case 'f':
        case 'F':
            printf("February! \n");
            break;
        
        case 'm':
        case 'M':
            printf("March & May! \n");
            break;
            
        case 'a':
        case 'A':
            printf("April & August! \n");
            break;
            
        case 's':
        case 'S':
            printf("September! \n");
            break;
            
        case 'o':
        case 'O':
            printf("October! \n");
            break;
            
            
        case 'n':
        case 'N':
            printf("November! \n");
            break;
            
            
        case 'd':
        case 'D':
            printf("December! \n");
            break;
        
        default:
            printf("Invalid Input!\n");
            break;
    }

    return 0;
}
```

#### আউটপুট

```c
Enter a first character of month: j
January, June & July!

Enter a first character of month: w
Invalid Input! 
```

#### switch case স্টেটমেন্ট ব্যবহার করে গ্রেডিং মার্ক নির্ণয় করার কোড-

```c
#include<stdio.h>

int main()
{
    int score;
    char mark;
    
    printf("Enter your score number: ");
    scanf("%d", &score);

    if(score >= 0 && score <= 100)
    {
        //90-100=A, 80-89=B, 70-79=C, 60-69=D, 40-59=E, 0-39=F
        switch(score/10)
        {
        case 10:
        case 9: mark = 'A'; break;
        case 8: mark = 'B'; break;
        case 7: mark = 'C'; break;
        case 6: mark = 'D'; break;
        case 5:
        case 4: mark = 'E'; break;
        case 3:
        case 2:
        case 1:
        case 0: mark = 'F'; break;
        }

        printf("Your Grade is: %c\n", mark);
    }else
    {
        printf("Invalid Input!\n");
    }

    return 0;
}
```

#### আউটপুট

```c
Enter your score number: 90 
Your Grade is: A
```

#### সবশেষে, switch case স্টেটমেন্ট ব্যবহার করে একটি সাধারণ ক্যালকুলেটর বানানোর চেষ্টা করি-

```c
#include<stdio.h>

int main()
{
    float a, b;
    char op;
    
    printf("Enter 2 Number & an operator (+, -, *, /): ");
    scanf("%f %f %c", &a, &b, &op);    

    switch(op)
    {
        case '+':
            {
                printf("Addition: %.2f\n", a+b);
                break;
            }
            
        case '-':
            {
                printf("Subtraction: %.2f\n", a-b);
                break;
            }
            
        case '*':
            {
                printf("Multiplication: %.2f\n", a*b);
                break;
            }
            
        case '/':
            {
                printf("Division: %.2f\n", a/b);
                break;
            }
            
        default:
            {
                printf("Invalid Input!\n");
                break;
            }
    }
        

    return 0;
}
```

#### আউটপুট

```c
Enter 2 Number & an operator (+, -, *, /): 45 5 * 
Multiplication: 225.00
```

