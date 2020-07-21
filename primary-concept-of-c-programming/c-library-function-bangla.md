# সি লাইব্রেরী ফাংশন

### সি লাইব্রেরী ফাংশন

আমরা পূর্বের পর্বে জেনেছি কিভাবে একটি সি প্রোগ্রামিং এর সিনট্যাক্সসহ, একটি পরিপূর্ন প্রোগ্রাম রান করতে হয় এবং এর প্রত্যেকটি লাইনের বিবরণ। এই পর্বে আমরা একটি সি প্রোগ্রামিং এর বিভিন্ন লাইব্রেরি ফাংশন, IDE সহ আরো অনেক কিছু জানবো।

আমরা যখন সি তে কোডিং করি, তখন আমাদের কোডিং এর স্বার্থে পূর্বে থেকেই অনেক প্রি-ডিফাইন্ড ফাংশন দেওয়া থাকে। যেগুলো বিভিন্ন হেডার ফাইলের অধীনে থাকে। হেডার ফাইল হচ্ছে এমন কিছু ফাইল যার অধীনে অংখ্য ছোট ছোট প্রোগ্রাম বা ফাংশন ফাইল কাজ করে। এবং প্রত্যেকটি স্বতন্ত্র ফাংশন নির্দিষ্ট কিছু কাজ সম্পন্ন করার জন্য সি তে ব্যবহার করা হয়।

যেমন আমাদের প্রতিটা প্রোগ্রামের শুরুতেই **\#include&lt;stdio.h&gt;** লেখাটি যুক্ত করে থাকি। আর এটি হচ্ছে একটা হেডার ফাইল যার অধীনে **printf\(\), scanf\(\), getchar\(\), putchar\(\)** ফাংশন রয়েছে। আর প্রত্যেকটি ফাংশন একটা নির্দিষ্ট কাজের জন্য আমরা সি তে ব্যবহার করে থাকি। যেমন আমাদের প্রোগ্রামের কোনো আউটপুট প্রিন্ট করার জন্য আমরা printf\(\) ফাংশন ব্যবহার করে থাকি। আবার কোনো ইউজার বা কিবোর্ড থেকে কোনো ডেটা নিতে চাইলে scanf\(\) ফাংশন ব্যবহার করি।

#### **stdio.h** হেডার ফাইলের অধীনে নিম্নোক্ত ফাংশনগুলো কাজ করে

* **printf\(\);** is output to the screen
* **scanf\(\);** is read input from the screen
* **putchar\(\);** is output a single character to the screen
* **getchar\(\);** is return characters typed on screen
* **fopen\(\);** is open a file
* **fclose\(\);** is close a file

#### **string.h** হেডার ফাইলের অধীনে নিম্নোক্ত ফাংশনগুলো কাজ করে

* **strlen\(\);** calculates the length of a string
* **strrev\(\);** reverse the string
* **strcat\(\);** concatenates \(joins\) one string to another string
* **strcmp\(\);** compares the contents of two strings
* **strcpy\(\);** copies a string’s content to another string

#### **math.h** হেডার ফাইলের অধীনে নিম্নোক্ত ফাংশনগুলো কাজ করে

* **rand\(\);** computes random number
* **pow\(\);** Computes power of a number
* **sqrt\(\);** computes square root of a number
* **log\(\);** computes natural logarithm of an argument
* **log10\(\);** computes the base 10 logarithm of an argument
* **exp\(\);** returns natural logarithm e
* **fabs\(\);** returns absolute value of number
* **floor\(\);** calculates the nearest integer less than argument
* **ceil\(\);** computes the nearest integer greater than argument
* **cbrt\(\);** computes cube root of a number
* **tan\(\);** computes tangent of a number
* **sin\(\);** computes sine of a number
* **cos\(\);** computes cosine of a number
* **atan\(\);** returns arc tangent of argument
* **acos\(\);** returns arc cosine of argument
* **asin\(\);** returns arc sine of argument

#### **ctype.h** হেডার ফাইলের অধীনে নিম্নোক্ত ফাংশনগুলো কাজ করে

* **isalnum\(\);** checks alphanumeric character
* **isalpha\(\);** checks whether a character is an alphabet or not
* **iscntrl\(\);** checks control character
* **isdigit\(\);** checks numeric character
* **isgraph\(\);** checks graphic character
* **islower\(\);** checks lowercase alphabet
* **isprint\(\);** checks printable character
* **ispunct\(\);** checks punctuation
* **isspace\(\);** check white-space character
* **isupper\(\);** checks uppercase alphabet
* **isxdigit\(\);** checks hexadecimal digit character
* **tolower\(\);** converts alphabet to lowercase
* **toupper\(\);** converts to lowercase alphabet

#### **time.h** হেডার ফাইলের অধীনে নিম্নোক্ত ফাংশনগুলো কাজ করে

* **time\(\);** returns current calendar time of system
* **difftime\(\);** returns difference in secs between two times
* **clock\(\);** returns a processor tick count associated with the process
* **localtime\(\);** converts a time\_t value to calendar time expressed as local time

#### **graphics.h** হেডার ফাইলের অধীনে নিম্নোক্ত ফাংশনগুলো কাজ করে

* **arc\(\);** for create a arc
* **bar\(\);** for create a bar
* **bar3d\(\);** for create a 3D bar
* **circle\(\);** for create a circle
* **rectangle\(\);** for create a rectangle
* **setcolor\(\);** for set color
* **setbkcolor\(\);** for set background-color

#### **conio.h** হেডার ফাইলের অধীনে নিম্নোক্ত ফাংশনগুলো কাজ করে

* **clrscr\(\);** used to clear the console screen
* **getch\(\);** used to hold the output screen

#### **stdlib.h** হেডার ফাইলের অধীনে নিম্নোক্ত ফাংশনগুলো কাজ করে

* **malloc\(\);** provides dynamic memory allocation
* **rand\(\);** generate a sequence of random number
* **srand\(\);** used to initialize the pseudo-random number

সি লাইব্রেরী ফাংশন বা হেডার ফাইল নিয়ে আরো বিস্তারিত জানতে [উইকিপিডিয়ার ](https://en.wikipedia.org/wiki/C_standard_library)এই পেইজটি দেখতে পারেন

### **IDE – Integrated development environment**

IDE হচ্ছে Integrated development environment। অর্থাৎ IDE হচ্ছে অন্যান্য সফটওয়্যারের মতই এক ধরনের সফটওয়্যার। যেখানে সাধারনত আমরা কোড করে থাকি এবং কোড করে কম্পাইল করে চেক করি আমাদের কোড অর্থাৎ প্রোগ্রাম ঠিকঠাক কাজ করছে কি না। আমাদের কোডে কোথাও যদি কোনো বিন্দু পরিমান ভুল হয় বা আমরা ভুল করে থাকি তাহলে কম্পাইলার সেটি চেক করে আমাদের জানাবে আমরা কোথায় কোথায় ভুল করেছি।

প্রতিটা প্রোগ্রামিং ভাষা লিখার জন্য আলাদা আলাদা IDE রয়েছে আবার এক IDE তে অনেক ধরনের প্রোগ্রাম করা যায়। আমরা যেহেতু সি প্রোগ্রামিং করবো, সেহেতু সবচেয়ে বেস্ট চয়েজ হচ্ছে CodeBlocks। CodeBlocks ডাউনলোড করতে চাইলে CodeBlocks এর অফিশিয়াল ওয়েব সাইটে গিয়ে ডাউনলোড করে নেওয়া যাবে।

CodeBlocks এর অফিশিয়াল ওয়েব সাইটে গেলে আপনি সেখানে ৩ ধরনের অপারেটিং সিস্টেমের জন্য ৩ ধরনের ডাউনলোড সেকশন পাবেন। আপনি যদি উইন্ডোজ ব্যবহারকারী হোন তাহলে আপনাকে mingw সহ ডাউনলোড করতে হবে। mingw হচ্ছে কম্পাইলার। কমপ্লাইলার সহ CodeBlocks ডাউনলোড না করলে প্রোগ্রাম রান হবে না। codeblocks-xx.0xmingw-setup.exe এরকম ফাইলটা ডাউনলোড করতে হবে। এখানে xx হচ্ছে ভার্শন সংখ্যা।

.exe ফাইলটি ডাউনলোড করার পর আর আট-দশটা সফটওয়্যারের মতই ইন্সটল দিতে হবে।

### লিনাক্সে যেভাবে **CodeBlocks** ইন্সটল দিবেন

প্রথমে সফটওয়্যার পেকেজলিস্ট আপডেট করে নিবেন  
‍**sudo apt-get update**  
তারপর কোডব্লোকস চালানোর জন্য একটি সাহায্যকারী পেকেজ ইন্সটল করব। এটি মুলত g++ ইন্সটল করে-  
**sudo apt-get install build-essential**  
এখন কোডব্লোকস ইন্সটল করার জন্য নিচের কমান্ডটি চালাবো  
**sudo apt-get install codeblocks**  
ইন্সটল করা হয়ে গেলে টার্মিনাল থেকে **codeblocks** এই কমান্ডটি দিলেই কোডব্লোকস রান করবে।

### **কম্পাইলার**

কম্পাইলার হচ্ছে এক ধরনের অনুবাদক যা এক ভাষা থেকে আরেক ভাষায় রুপান্তর করে থাকে। আমরা ইতিমধ্যে জানি যে, কম্পিউটার বাইনারি সিস্টেম অর্থাৎ 0 আর 1 ছাড়া কিছুই বুঝে না। আর বাইনারি সিস্টেমে যদি প্রোগ্রামিং করা খুবই বিরক্তিকর ও সময়সাধ্য ব্যাপার। মানুষ চাইলে খুব কম সময়ে নিখুঁত প্রোগ্রামিং করতে পারবে না আর এই দিকে কম্পিউটার বাইনারি ছাড়া কিছুই বুঝে না। এই সমস্যা সমাধান করার জন্য মূলত কম্পাইলার ব্যবহার করা হয়।

সোজা কথায়, কম্পাইলার কোন প্রোগ্রামের সোর্সকোডকে কম্পাইল করে মেশিনকোডে রূপান্তর করে যাতে কম্পিউটার প্রোগ্রামটির কাঙ্খিত ফলাফল দিতে পারে। আরো নিখুঁতভাবে বলতে গেলে, কম্পাইলার সোর্সকোডকে অ্যাসেম্বলি কোডে পরিনত করে, পরবর্তীকালে অ্যাসেম্বলার অ্যাসেম্বলি কোডকে মেশিনকোড এ পরিনত করে। কম্পিউটারের মাইক্রোপ্রসেসর এই মেশিনকোড বুঝতে পারে এবং সেই অনুযায়ী কর্মসম্পাদন করে।

