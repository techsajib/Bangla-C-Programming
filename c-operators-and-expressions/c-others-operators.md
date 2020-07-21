# সি অন্যান্য অপারেটর

আমরা পূর্বের পর্বে জেনেছি সি প্রোগ্রামিং এ ব্যবহৃত Logical Operator \(লজিক্যাল অপারেটর\) নিয়ে। এই পর্বে আমরা সি প্রোগ্রামিং এর অন্যান্য অপারেটর নিয়ে বিস্তারিত আলোচনা করব।

### **Conditional Operator \(কন্ডিশনাল অপারেটর\)**

সময় ও কোডিং এর স্বার্থে অনেক সময় প্রোগ্রামাররা তাদের প্রোগ্রামকে যথাসম্ভব ছোট, সহজ ও সাবলীল রাখার চেষ্টা করে। এই ক্ষেত্রে কোডারদের বিশেষ কিছু নিয়মের মধ্য দিয়ে যেতে হয়। সি প্রোগ্রামিং এ কন্ডিশনযুক্ত বা শর্তযুক্ত বিভিন্ন কাজ করার জন্যই মূলত কন্ডিশনাল অপারেটর ব্যবহার করা হয়। এই অপারেটর দিয়ে একটা condition থেকে দুটি মান নির্ধারণ করার একটা সহজ পদ্ধতি রয়েছে। কন্ডিশনাল অপারেটর তিনটি অপারেন্ড নিয়ে কাজ করে বলে একে টারনারী \(ternary\) অপারেটরও বলা হয়।

**কন্ডিশনাল অপারেটরের সিনট্যাক্স**

```c
Expression1? Expression2: Expression3
```

**ব্যবহার**

```c
max = (n1 > n2) ? n1 : n2;
```

এখানে **max** নামক ভেরিয়েবলের ভিতরে আমরা কন্ডিশনাল এক্সপ্রেশনটি স্টোর করেছি। আর প্রথম স্টেপ **\(n1 &gt; n2\)** এ যদি n1 এর মান n2 এর চেয়ে বড় হয় তাহলে ২য় স্টেপে n1 প্রিন্ট করবে আর কন্ডিশন মিথ্যা হলে n2 প্রিন্ট করবে।

বিষয়টি আরো সহজেই বুঝার জন্য নিচের সি কোডটি দেখুন-

```c
#include <stdio.h>

int main()
{
    int x1 = 10, x2 = 20, maximum;      // variable declaration 

    maximum = (x1>x2) ? x1: x2;             // Maximum among x1 and x2 
    
    printf("Maximum Number: %d", maximum);      // Print the Maximum number 

    return 0;
}
```

**আউটপুট** 

```c
Maximum Number: 20
```

এখন আমরা যদি মিনিমাম নাম্বার বের করতে চাই তখন কোডের জাস্ট একটা অপারেটর পরিবর্তন করে দিলেই হবে, সেটা হচ্ছে **\(x1&gt;x2\)** এই অংশে জাস্ট বৃহত্তর থেকে ক্ষুদ্রতর **\(x1&lt;x2\)** করে দিলেই হবে।

```c
#include <stdio.h>

int main()
{
    int x1 = 10, x2 = 20, minimum;      // variable declaration

    minimum = (x1<x2) ? x1: x2;             // Minimum among x1 and x2

    printf("Minimum Number: %d", minimum);      // Print the Minimum number

    return 0;
}

```

**আউটপুট** 

```c
Minimum Number: 10
```

এখন আমরা যদি কিবোর্ড থেকে প্রিন্ট নিয়ে অর্থাৎ **scanf** ফাংশন ব্যবহার করে এই কন্ডিশনের কাজটি করতে চাই তখন-

```c
#include <stdio.h>

int main()
{
    int x1, x2, maximum, minimum;   // variable declaration

    printf("Enter two values: ");
    scanf("%d %d", &x1, &x2);       // take x1 & x2 value from keyboard

    maximum = (x1>x2) ? x1: x2;         // Maximum among x1 and x2
    minimum = (x1<x2) ? x1: x2;         // Minimum among x1 and x2

    printf("Maximum Number: %d\n", maximum);  // Print the Minimum number
    printf("Minimum Number: %d\n", minimum);  // Print the Minimum number

    return 0;
}
```

**আউটপুট** 

```c
Enter two values: 15 19
Maximum Number: 19
Minimum Number: 15 
```

### Bit-wise Operator \(বিটওয়াইজ অপারেটর\)

সি প্রোগ্রামিং এ বিট নিয়ে কাজ করার জন্য বা কোনো অপারেশন চালানোর জন্য বা কোনো বিট ডানে-বামে সরানোর জন্য বিটওয়াইজ অপারেটর ব্যবহার করা হয়। আরো সহজ ভাবে বললে আমাদের কম্পিউটারের CPU তে একটি গুরুত্বপূর্ন অংশ রয়েছে যাকে আমরা গাণিতিক যুক্তি ইউনিট বা ALU বলে থাকি। এই অংশে আমাদের সকল গাণিতিক কার্যক্রম সম্পন্ন হয়ে থাকে। যেমন- যোগ, বিয়োগ, গুণ, ভাগ ইত্যাদি আর এইসব ALU তে বিট লেভেলে সম্পন্ন হয়। আর এই বিট-লেভেল \(bit-level\) অপারেশন সম্পন্ন করার কাজেই বিটওয়াইজ অপারেটর ব্যবহৃত হয়। Float বা Double টাইপের ডেটার ক্ষেত্রে বিটওয়াইজ অপারেটর ব্যবহার করা যায় না।

**নিচে বিটওয়াইজ অপারেটর এর চার্টটি লক্ষ্য করুন-**

| অপারেটর | উচ্চারণ | উদাহরণ |
| :---: | :---: | :---: |
| & | Bit-wise AND  | \(x & y\) |
| \| | Bit-wise OR | \(x \| y\) |
| ^ | Bit-wise exclusive OR | \(x ^ y\) |
| ~ | BIt-wise complement | ~x |
| &lt;&lt; | Shift Left | x&lt;&lt;2 |
| &gt;&gt; | Shift Right | x&gt;&gt;2 |

**নিচে & \(অ্যান্ড\), \| \(অর\), এবং ^ \(এক্সঅর\) এর ট্রুথ টেবিলটি লক্ষ্য করুন-**

| x | y | x & y | x \| y | x ^ y |
| :---: | :---: | :---: | :---: | :---: |
| 0 | 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 | 1 |
| 1 | 1 | 1 | 1 | 0 |
| 1 | 0 | 0 | 1 | 1 |

#### বিটওয়াইজ AND অপারেটর

Bit-wise AND Operator এর দুটি অপারেন্ডের বিট যদি 1 হয় তাহলে বিটওয়াইজ AND অপারেটর এর আউটপুট 1 হবে। কিন্তু Bit-wise AND Operator এর যেকোনো একটি অপারেন্ড শূন্য হলে আউটপুট শূন্য হবে।

এখানে ডেসিম্যাল থেকে বাইনারি [কনভার্ট ](https://www.rapidtables.com/convert/number/binary-to-decimal.html)করা যাবে। 

**গাণিতিক ব্যাখ্যা**

```c
20 = 00010100 (20 কে বাইনারিতে রুপান্তরের পর)
25  = 00011001 (25 কে বাইনারিতে রুপান্তরের পর)

20 ও 25 এর বিট অপারেশন
   00010100 
&  00011001 
  _________
   00010000  = 16 (00010000 কে ডেসিম্যালে রুপান্তরের পর)
```

এই গাণিতিক সমস্যাকে সি প্রোগ্রামিং এর মাধ্যমে এইভাবে করতে হয়-

```c
#include <stdio.h>

int main()
{
    int x = 20, y = 25;
    printf("AND Operator = %d", x&y);

    return 0;
}
```

**আউটপুট**

```c
AND Operator: 16
```

#### বিটওয়াইজ OR অপারেটর

Bit-wise OR Operator এর দুটি অপারেন্ডের যেকোনো একটি বিট যদি 1 হয় তাহলে বিটওয়াইজ OR অপারেটর এর আউটপুট 1 হবে। কিন্তু Bit-wise OR Operator এর উভয়ই অপারেন্ড শূন্য হলে আউটপুট শূন্য হবে।

**গাণিতিক ব্যাখ্যা**

```c
15 = 00001111 (15 কে বাইনারিতে রুপান্তরের পর)
20 = 00010100 (20 কে বাইনারিতে রুপান্তরের পর)

15 ও 20 এর বিট অপারেশন
   00001111 
|  00010100 
  _________
   00011111  = 31 (00011111 কে ডেসিম্যালে রুপান্তরের পর)
```

এই গাণিতিক সমস্যাকে সি প্রোগ্রামিং এর মাধ্যমে এইভাবে করতে হয়-

```c
#include <stdio.h>

int main()
{
    int x = 15, y = 20;
    printf("OR Operator = %d", x|y);

    return 0;
}
```

**আউটপুট**

```c
OR Operator = 31
```

#### বিটওয়াইজ XOR অপারেটর

বিটওয়াইজ XOR\(^\) অপারেটর সম্পূর্ণ বিপরীতমুখী। অর্থাৎ এর দুটি অপারেন্ড যদি পরস্পর বিপরীতধর্মী হয় তাহলে বিটওয়াইজ XOR অপারেটর এর আউটপুট 1 হবে। কিন্তু যদি বিটওয়াইজ XOR\(^\) অপারেটরের দুটি অপারেন্ড একই রকম হয় তাহলে আউটপুট শূন্য হবে।

**গাণিতিক ব্যাখ্যা**

```c
30 = 00011110 (30 কে বাইনারিতে রুপান্তরের পর)
35 = (35 কে বাইনারিতে রুপান্তরের পর)

30 ও 35 এর বিট অপারেশন
   00011110
|  00100011
  _________
   00111101  = 61 (00111101 কে ডেসিম্যালে রুপান্তরের পর)

```

এই গাণিতিক সমস্যাকে সি প্রোগ্রামিং এর মাধ্যমে এইভাবে করতে হয়-

```c
#include <stdio.h>

int main()
{
    int x = 30, y = 35;
    printf("XOR Operator = %d", x^y);

    return 0;
}
```

**আউটপুট**

```c
XOR Operator = 61
```

#### কমা অপারেটর

সি প্রোগ্রামিং এ আমরা প্রায়ই কমা অপারেটরটি ব্যবহার করে থাকি। একই সম্পর্কযুক্ত এক্সপ্রেশনসমূহকে একসাথে ডিক্লেয়ার করার ক্ষেত্রে সবচেয়ে বেশী এই ব্যবহৃত হয়। যেমন-

```c
int x, y, z, o, p = 30; 
```

#### sizeof অপারেটর

sizeof অপারেটর দিয়ে কোনো কিছুর সাইজ নির্ধারন করা হয় যেমন- কনস্ট্যান্ট, ভ্যারিয়েবল, অ্যারে, স্ট্রাকচার ইত্যাদির সাইজ রিটার্ন করার ক্ষেত্রে এটি ব্যবহৃত হয়।

আমরা যদি sizeof অপারেটর ব্যবহার করে **int, float, double, char** এর সাইজ বের করতে চাই তাহলে এইভাবে নিচের সি প্রোগ্রামটি লিখতে হবে-

```c
#include <stdio.h>

int main()
{
    printf("Character Size: %lu byte\n", sizeof(char));
    printf("Integer Size: %lu byte\n", sizeof(int));
    printf("Float Size: %lu byte\n", sizeof(float));
    printf("Double Size: %lu byte\n", sizeof(double));

    return 0;
}
```

**আউটপুট**

```c
Character Size: 1 byte
Integer Size: 4 byte
Float Size: 4 byte
Double Size: 8 byte
```
