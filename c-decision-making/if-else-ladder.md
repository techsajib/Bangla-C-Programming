# if- else Ladder স্টেটমেন্ট

আমরা পূর্বের পর্বে জেনেছি সি প্রোগ্রামিং এর **if-else statement** নিয়ে। এই পর্বে আমরা সি প্রোগ্রামিং এর ডিসিশন মেকিং স্টেটমেন্টের **if- else Ladder** statement নিয়ে বিস্তারিত আলোচনা করব।

আমরা জানি if-else স্টেটমেন্ট মূলত বিভিন্ন কন্ডিশনের উপর ভিত্তি করে কাজ করে থাকে। অর্থাৎ প্রোগ্রামের কন্ডিশন বা test expression যদি সত্য হয় তাহলে সে এক রকম আউটপুট দিবে আবার প্রোগ্রামের কন্ডিশন বা test expression যদি মিথ্যা হয় তাহলে আরেক রকম আউটপুট দিবে।

এই ধরণের সমস্যা সমাধানের জন্য অনেক সময় আমাদের দুই বা ততোধিক কন্ডিশন নিয়ে কাজ করতে হয় আর এই জন্য আমাদেরকে if...else Ladder স্টেটমেন্ট ব্যবহার করতে হয়। অনেকগুলা test expression কে চেক করতে এবং তাদের প্রত্যেকের স্টেটমেন্টকে আলাদাভাবে এক্সিকিউট করতে এই Ladder স্টেটমেন্ট ব্যবহৃত হয়।

#### if...else Ladder স্টেটমেন্ট এর সিনট্যাক্স

```c
if(condition1)
{
  statements
}else if(condition2)
{
  statements
}
.
.
else
{
 statements
}
```

আমাদের বাস্তব জীবনে অনেক সমস্যা সমাধানের জন্য এই লেডার স্টেটমেন্ট ব্যবহার করা হয়। যেমন ধরুন- আপনি কোনো ছাত্রের মার্কসিট বানাতে চান অথবা বেশ কয়েকটি সংখ্যার মাঝে বৃহৎ সংখ্যা অথবা ক্ষুদ্রতর সংখ্যা বের করতে চান অথবা আপনি লিপ ইয়ার নির্ণয় করতে চান তাহলে আপনাকে এই লেডার স্টেটমেন্ট ব্যবহার করতে হবে।

লেডার স্টেটমেন্ট বুঝার জন্য আমি নিচে কিছু সি প্রোগ্রামের উদাহরণ দিয়েছি-

এখন আমরা যদি তিনটি সংখ্যার মাঝে বৃহত্তর সংখ্যা বের করতে চাই, তাহলে আমাদের সি কোডের ধরণ এমন হবে-

```c
#include<stdio.h>

int main()
{
    int x, y, z, result;

        printf("Enter 3 Number: ");
        scanf("%d %d %d", &x, &y, &z);

        if(x>y && x>z)
        {
            result = x;
        }else if(y>x && y>z)
        {
            result = y;
        }else
        {
            result = z;
        }

        printf("Bigger Number: %d\n", result);

    return 0;
}
```

#### আউটপুট

```c
Enter 3 Number: 57 23 34
Bigger Number: 57
```

#### ব্যাখ্যা 

আমরা এই প্রোগ্রামে **x, y, z, result** নামে চারটি ইন্টিজার টাইপ ভেরিয়েবল নিয়েছি। x, y, z, ভেরিয়েবলকে কিবোর্ড থেকে ইনপুট নেওয়ার জন্য scanf ফাংশন ব্যবহার করেছি। এরপর মূলত আমাদের if- else Ladder statement নিয়ে কাজ করেছি। প্রথমে আমরা x কে y এর সাথে তুলনা করেছি, যদি x এর মান y এর মানের চেয়ে বড় হয় এবং x এর মান z এর মানের চেয়ে বড় হয় তাহলে সে ব্লক স্টেটমেন্টের ভেতরে রাখা result ভেরিয়েবলের মাঝে x এর মান স্টোর করবে।

দ্বিতীয় স্টেপে, অথবা যদি y এর মান x এর মানের চেয়ে বড় হয় এবং y এর মান z এর মানের চেয়ে বড় হয় তাহলে result ভেরিয়েবলের মাঝে y এর মান স্টোর করবে।

তৃতীয় ধাপে, যদি x ও y এর মান কন্ডিশনের সাথে না মিলে তাহলে সে result ভেরিয়েবলের মাঝে z এর মান স্টোর করবে। তারপর printf ফাংশন ইক্সিকিউট করবে।

if- else Ladder স্টেটমেন্ট ব্যবহার করে আমরা যদি লিপ ইয়ার নির্ণয় করতে চাই-

```c
#include<stdio.h>

int main()
{
    int year;

        printf("Enter Year: ");
        scanf("%d", &year);

        if(year%400 == 0)       /*if(year%4==0) && (year%400==0) || (year%100==0)*/
        {
            printf("Leap Year!\n");
        }else if(year%100 == 0)
        {
            printf("Not Leap Year!\n");
        }else if(year%4 == 0)
        {
            printf("Leap Year!\n");
        }else
        {
            printf("Not Leap Year!\n");
        }

    return 0;
}
```

#### আউটপুট

```c
Enter Year: 2020
Leap Year!
```

#### ব্যাখ্যা

আমরা জানি যে সকল বৎসরকে 4 ও 400 দিয়ে ভাগ করলে ভাগশেষ শূন্য হয়, সে সকল বৎসরকে লিপ ইয়ার বলে। এবং যে সকল ইয়ারকে 100 দিয়ে ভাগ করলে ভাগশেষ শূন্য হয় এবং এছাড়াও বাকি সব বৎসর লিপ ইয়ারের অন্তর্ভুক্ত না অর্থাৎ এইগুলা লিপ ইয়ার না।

তাই আমাদের প্রোগ্রামে প্রথমেই আমাদের ইনপুট দেওয়া বছর কে 400 দিয়ে ভাগ করে দেখছে এর রেজাল্ট 0 কি না, যদি শূন্য হয় তাহলে Leap Year! লেখাটি প্রিন্ট হবে। আবার আমাদের ইনপুটকে 100 দিয়ে ভাগ করে ভাগশেষ শূন্য হলে এটি Not Leap Year! লেখাটি প্রিন্ট করবে, একইভাবে আবার আমাদের ইনপুটকে 4 দিয়ে ভাগ করে ভাগশেষ শূন্য হলে Leap Year! লেখাটি প্রিন্ট করবে অন্যথায় আবার Not Leap Year! লেখাটি প্রিন্ট করবে।

এখন আমরা যদি গ্রেডিং মার্ক নির্ণয় করতে চাই তাহলে -

```c
#include<stdio.h>

int main()
{
    int mark;

    printf("Enter your mark: ");
    scanf("%d", &mark);

    if(mark < 0 || mark > 100)
    {
        printf("Wrong Input, please make it 0-100! \n");
    }else if(mark >= 80)
    {
        printf("You got A+!");
    }else if(mark >= 70)
    {
        printf("You got A!");
    }else if(mark >= 60)
    {
        printf("You got A-!");
    }else if(mark >= 50)
    {
        printf("You got B!");
    }else if(mark >= 40)
    {
        printf("You got C!");
    }else if(mark >= 33)
    {
        printf("You got D!");
    }else
    {
        printf("You're Failed!");
    }

    return 0;
}
```

#### আউটপুট

```c
Enter your mark: 80
You got A+!
```

এখন আমরা যদি ৫টি বিষয়ের মান নিয়ে তার টোটাল, পারসেন্টিজ ও এর গ্রেডিং হিসেব করে আউটপুট করতে চাই, তখন কোডের ধরণ কেমন হবে-

```c
#include<stdio.h>

int main()
{
    int bangla, english, math, science, social, total, percentage;

    printf("Bangla Mark: ");
    scanf("%d", &bangla);

    printf("\nEnglish Mark: ");
    scanf("%d", &english);

    printf("\nMath Mark: ");
    scanf("%d", &math);

    printf("\nScience Mark: ");
    scanf("%d", &science);

    printf("\nSocial Mark: ");
    scanf("%d", &social);

    total = bangla+english+math+science+social;
    percentage = total/5;

    printf("\nTotal Marks = %d/500", total);
    printf("\nTotal Percentage = %d%% \n", percentage);

    if(percentage <40)
    {
        printf("You have failed! \n");
    }else if((percentage >40) && (percentage <55))
    {
        printf("You got C! \n");
    }else if((percentage >55) && (percentage <65))
    {
        printf("You got B! \n");
    }else if ((percentage >65) && (percentage <80))
    {
        printf("You got A! \n");

    }else if((percentage >80) && (percentage <100))
    {
        printf("You got A+! \n");
    }else
    {
        printf("Invalid input! try again \n");
    }

    return 0;
}

```

#### আউটপুট 

```c
Bangla Mark: 78 
English Mark: 79 
Math Mark: 90
Science Mark: 89 
Social Mark: 85

Total Marks = 421/500 
Total Percentage = 84% 
You got A+!
```

