# সি ডেটা টাইপ

আমরা পূর্বের পর্বে জেনেছি সি প্রোগ্রামিং ভেরিয়েবল ও লোকাল, গ্লোবাল, স্ট্যাটিক ও কন্সট্যান্ট ভেরিয়েবল নিয়ে বিস্তারিত। এই পর্বে আমরা ভেরিয়েবলের ডাটাটাইপ নিয়ে বিস্তারিত আলোচনা করব।

### **ডাটাটাইপ \(Data Type\)** 

আমাদের দৈনন্দিন জীবনে আমরা বিভিন্ন ধরনের ডেটা নিয়ে কাজ করি। আমরা যখন কাউকে তার নাম জিজ্ঞেস করি, তখন সে হয়তো তার নাম বলে X, Y, Z অথবা তার ফোন নাম্বার জানতে চাইলে সে বলে 01….., or 01….. etc. আবার আমরা যখন কাউকে টাকার হিসাব বলি, তখন 1234.50 Taka অথবা 1213… Taka ইত্যাদি বলে থাকি। এই যে X, Y, Z অথবা মোবাইল নাম্বার, অথবা টাকার এমাউন্ট কিন্তু এক ধরনের ডেটা নয়।

কিছু কিছু ক্ষেত্রে আমরা নাম ব্যবহার করছি যেটা আলফাবেট বা লেটারের সংমিশ্রণে হয়ে থাকে, আবার মোবাইল নাম্বার যেটা ডিজিটের সংমিশ্রণে হয়ে থাকে, আবার টাকার হিসাব এইগুলাও ডিজিটের সংমিশ্রণে হয়ে থাকে, ব্যবধান হচ্ছে অনেকক্ষেত্রে পূর্নাঙ্গ সংখ্যা, অনেকক্ষেত্রে ভগ্নাংশ সংখ্যা হয়ে থাকে।

এই যে বিভিন্ন ধরণের ডেটার সংমিশ্রণ। এই সংমিশ্রণকেই ডাটাটাইপ বলে। অর্থাৎ একটা ভেরিয়েবল যে টাইপের ডাটা স্টোর করে রাখে, সেই ডাটাটি হচ্ছে সেই টাইপের ডাটাটাইপ। অর্থাৎ Steve, Gates, Mark ইত্যাদি হচ্ছে ক্যারেক্টার ডাটাটাইপ, 111, 222, 543 ইত্যাদি হচ্ছে ইন্টিজার ডাটাটাইপ, আবার 12.355, 3.1416, 1.0999 ইত্যাদি হচ্ছে ফ্লোট অথবা ডাবল ডাটাটাইপ।

**সি তে মূলত চার ধরণের Data Type রয়েছে-**

* Basic Data Type \(int, char, float, double\)
* Derived Data Type \(array, pointer, structure, union\)
* Enumeration Data Type \(enum\)
* Void Data Type \(void\)

**সি প্রোগ্রামিং এ Basic বা মৌলিক চার ধরণের ডাটাটাইপ রয়েছে-**

* int data type
* float data type
* double data type
* char data type

বেসিক ডাটাটাইপ নিয়ে বিস্তারিত জানার আগে নিচের টেবিলটি ভাল করে লক্ষ্য করুন –

| ডাটাটাইপ | মেমরি | প্লেসহোল্ডার | রেঞ্জ |
| :--- | :--- | :--- | :--- |
| int | 2 or 4 byte | %d | -32,768 to 32,767 or -2,147,483,648 to 2,147,483,647 |
| float | 4 byte | %f | 1.2E-38 to 3.4E+38 \(6 decimal places\) |
| double | 8 byte | %lf | 2.3E-308 to 1.7E+308 \(15 decimal places\) |
| long double | 10 byte | %llf | 3.4E-4932 to 1.1E+4932 \(19 decimal places\) |
| char | 1 byte | %c | -128 to 127 or 0 to 255 |
| unsigned char | 1 byte | %c | 0 to 255 |
| signed char | 1 byte | %c | -128 to 127 |
| short int | 2 byte | %hd | -32,768 to 32,767 |
| unsigned short int | 2 byte | %hu | 0 to 65,535 |
| unsigned int | 2 or 4 byte | %u | 0 to 4,294,967,295 |
| long int  | 4 byte | %ld | -2,147,483,648 to 2,147,483,647 |
| long long int | 8 byte | %lld | -\(2^63\) to \(2^63\)-1 |
| unsigned long | 4 byte | %lu | 0 to 4,294,967,295 |

প্রত্যেকটি ডেটা টাইপের ভেল্যু রেঞ্জ চেক করতে নিচের কোডটি দেখেন –

```c
#include <stdio.h>
#include <stdlib.h>
#include <limits.h>
#include <float.h>
 
int main(int argc, char** argv) {
 
    printf("CHAR_BIT    :   %d\n", CHAR_BIT);
    printf("CHAR_MAX    :   %d\n", CHAR_MAX);
    printf("CHAR_MIN    :   %d\n", CHAR_MIN);
    printf("INT_MAX     :   %d\n", INT_MAX);
    printf("INT_MIN     :   %d\n", INT_MIN);
    printf("LONG_MAX    :   %ld\n", (long) LONG_MAX);
    printf("LONG_MIN    :   %ld\n", (long) LONG_MIN);
    printf("SCHAR_MAX   :   %d\n", SCHAR_MAX);
    printf("SCHAR_MIN   :   %d\n", SCHAR_MIN);
    printf("SHRT_MAX    :   %d\n", SHRT_MAX);
    printf("SHRT_MIN    :   %d\n", SHRT_MIN);
    printf("UCHAR_MAX   :   %d\n", UCHAR_MAX);
    printf("UINT_MAX    :   %u\n", (unsigned int) UINT_MAX);
    printf("ULONG_MAX   :   %lu\n", (unsigned long) ULONG_MAX);
    printf("USHRT_MAX   :   %d\n", (unsigned short) USHRT_MAX);
 
    return 0;
}
```

প্রোগ্রামটি রান করলে আউটপুট আসবে –

```c
CHAR_BIT : 8
CHAR_MAX : 127
CHAR_MIN : -128
INT_MAX : 2147483647
INT_MIN : -2147483648
LONG_MAX : 9223372036854775807
LONG_MIN : -9223372036854775808
SCHAR_MAX : 127
SCHAR_MIN : -128
SHRT_MAX : 32767
SHRT_MIN : -32768
UCHAR_MAX : 255
UINT_MAX : 4294967295
ULONG_MAX : 18446744073709551615
USHRT_MAX : 65535
```

### **ইন্টিজার ডেটা টাইপ \(int data type\)**

দশমিক সংখ্যা ব্যতীত সকল ধনাত্মক এবং ঋণাত্মক পূর্ণ সংখ্যাকেই মূলত ইন্টিজার ডেটা টাইপ বলে। যেমন- 0, -5, 300 ইত্যাদি। ইন্টিজার ডেটা টাইপ ডিক্লেয়ার করতে হয় int কিওয়ার্ড দিয়ে। যেমন-

```c
int id = 10;
```

এখানে id ভেরিয়েবলটি ইন্টিজার ডেটা স্টোর করবে, যেহেতু এর সামনে int কিওয়ার্ড দেওয়া আছে। এর মান হচ্ছে 10। **int** কিওয়ার্ডটি ডিক্লেয়ার করার সাথে সাথে কম্পিউটার তার জন্য ২ বাইট কিছু ক্ষেত্রে ৪ বাইট মেমরি স্পেস দিয়ে দিবে। এর রেঞ্জ হচ্ছে **-32,768 to 32,767**। আমরা চাইলে একই লাইনে ইচ্ছে মত ভেরিয়েবল ডিক্লেয়ার করতে পারি নিচের মত-

```c
int id, age, number;
```

সি প্রোগ্রামিং এ আমরা যেভাবে ইন্টিজার ডেটা টাইপ ব্যবহার করবো, তা বুঝার জন্য নিচের উদাহরণ লক্ষ্য করুন –

```c
#include <stdio.h>
 
int main()
{
    int a = 10; //integer variable 
    int b = 10; //integer variable
    int result; //integer variable
 
    result = a+b;
    printf("Result: %d", result);
 
    return 0;
}
```

প্রোগ্রামটি রান করার পর রেজাল্ট আসবে 20 অর্থাৎ 20 একটি ইন্টিজার ডাটাটাইপ।

### **ফ্লোট ডেটা টাইপ \(float data type\)**

আমরা ইন্টিজার ডাটাটাইপ বলতে জানি পূর্ণসংখ্যা কিন্তু ফ্লোট ডাটাটাইপ হচ্ছে বাস্তব সংখ্যা। অর্থাৎ যেকোনো দশমিকযুক্ত সংখ্যাই হচ্ছে ফ্লোট ডেটা টাইপ। আপনি কখনও ইন্টিজার ডেটাটাইপে দশমিক অর্থাৎ 30.55, 3.1416 ইত্যাদি নাম্বার রাখতে পারবেন না। এইসব রাখার জন্য আপনাকে ফ্লোট ডেটা টাইপ ব্যবহার করতে হবে। আর floating point ডেটা টাইপ দশমিকের পর ৬ ঘর পর্যন্ত নির্ভুল ভাবে সংরক্ষণ করতে পারে। ফ্লোট ডেটা টাইপ ডিক্লেয়ার করতে হয় float কিওয়ার্ড দিয়ে। যেমন-

```c
float salary = 50300.55;
```

এখানে **salary** ভেরিয়েবলটি ফ্লোট টাইপ ডেটা স্টোর করবে। যার মান বা ভেল্যু হচ্ছে **50300.55**। কম্পিউটার মেমরিতে ফ্লোটের জন্য ৪ বাইট অর্থাৎ ৩২ বিট স্পেস দিবে। এর রেঞ্জ হচ্ছে **1.2E-38 to 3.4E+38** \(6 decimal places\) অর্থাৎ ফ্লোট ডাটাটাইপ দশমিকের পর সর্বোচ্চ ৬ ঘর পর্যন্ত কাজ করে।

আমাদের উপরের ইন্টিজার ডাটাটাইপের প্রোগ্রামটির কোড আমরা আপডেট করে ফ্লোটে কনভার্ট করতে নিচের কোডটি লক্ষ্য করি-

```c
#include <stdio.h>
 
int main()
{
    float a = 10.55; //floating variable
    float b = 10.55; //floating variable
    float result; //floating variable
 
    result = a+b;
    printf("Result: %f", result);
 
    return 0;
}
```

প্রোগ্রামটি রান করলে রেজাল্ট আসবে 21.100000 কারন আমরা জানি ফ্লোট ডাটাটাইপ দশমিকের পর ৬ ঘর পর্যন্ত প্রিন্ট করে তাই দশমিকের পর ৬ ঘর পর্যন্ত আমরা উত্তর পেয়েছি। আপনি চাইলে আপনার মত করে যত ঘর মন চাই তত ঘর প্রিন্ট করতে পারেন। শুধু printf ফাংশনে গিয়ে প্লেসহোল্ডার %f এর মাঝে যত ঘর প্রিন্ট করতে চান পয়েন্ট তত লিখে দিলেই হবে। যেমন আমি দুই ঘর প্রিন্ট করতে চাই মানে আমার উত্তর 21.10 দেখাতে চাই। তাহলে নিচের মত করে কোডটি পরিবর্তন করুন-

```c
printf(“Result: %.2f”, result); // %f after %.2f
```

### **ডাবল ডেটা টাইপ \(double data type\)**

**double** ডেটা টাইপ আর float ডেটা টাইপ একই জিনিস। শুধু তাদের মধ্যে পার্থক্য মেমরি স্পেস আর রেঞ্জ নিয়ে। ডাবল ডেটা টাইপের জন্য কম্পিউটার ৮ বাইট অর্থাৎ ৬৪ বিট স্পেস দিয়ে থাকে। আর এর রেঞ্জ হচ্ছে **2.3E-308 to 1.7E+308** \(15 decimal places\)। এর মানে double ডেটা টাইপ দশমিকের পর ১৫ ঘর পর্যন্ত নির্ভুল মান সংরক্ষণ করতে পারে। ডাবল ডেটা টাইপ ডিক্লেয়ার করতে হয় double কিওয়ার্ড দিয়ে। যেমন-

```c
double pi = 3.141592653589793;
```

ডাবল ডেটা টাইপের ব্যপারটি সহজেই বুঝার জন্য নিচের প্রোগ্রামটি লক্ষ্য করুন-

```c
#include <stdio.h>
 
int main()
{
    double pi = 3.141592653589793;
    printf("%.15lf", pi);
 
    return 0;
}
```

প্রোগ্রামটি রান করলে পাই এর মান **3.141592653589793** দেখাবে কিন্তু আমরা যদি প্রোগ্রামটি float ডাটাটাইপে করতাম তাহলে আমরা কাঙ্খিত ফলাফলটি পেতাম না। আবার আমরা যদি প্লেসহোল্ডারে কত ঘর পর্যন্ত প্রিন্ট করতে হবে সেটা না বলে দিতাম তাহলে সে শুধু ৬ ঘর পর্যন্ত প্রিন্ট করতো। জিনিসটি চেক করার জন্য কোডগুলো পরিবর্তন করে দেখতে পারেন।

### **ক্যারেক্টার ডেটা টাইপ \(character data type\)**

ক্যারেক্টার ডেটা টাইপ বলতে ইংরেজিতে যতগুলো আলফাবেট বা লেটার আছে সবগুলোই এই ক্যারেক্টার ডেটা টাইপের অন্তর্ভুক্ত। অর্থাৎ আমাদের কীবোর্ডের প্রত্যেকটি চিহ্নই এক একটা character। ক্যারেক্টার ডেটা টাইপ ডিক্লেয়ার করতে হয় char কিওয়ার্ড দিয়ে। যেমন-

```c
char alphabet = ‘a’;
```

এখানে alphabet হচ্ছে ক্যারেক্টার ডেটা টাইপ আর ‘a’ হচ্ছে এর মান। ক্যারেক্টার ভ্যারিয়েবলের সাইজ 1 বাইট মানে 8 বিট আর এর রেঞ্জ হচ্ছে **-128 to 127 or 0 to 255**।

character ভ্যারিয়েবলে মাত্র একটি কারেকটার / লেটার বা বর্ণ সংরক্ষন করা যায়। নিচের প্রোগ্রাম দেখিঃ

```c
#include <stdio.h>
 
int main()
{
    char alphabet = 'M';
    printf("Alphabet: %c", alphabet);
 
    return 0;
}
```

প্রোগ্রামটি রান করলে আউটপুটে **M** দেখাবে।

**Tags:** _ইন্টিজার ডেটা টাইপ \(Int Data Type\), ক্যারেক্টার ডেটা টাইপ \(Character Data Type\), ডাবল ডেটা টাইপ \(Double Data Type\), ফ্লোট ডেটা টাইপ \(Float Data Type\), সি প্রোগ্রামিং ডাটাটাইপ \(Data Type\)_

