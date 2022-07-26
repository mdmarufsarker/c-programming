## সি প্রোগ্রামিং এর হাতেখড়ি

আজকে আমরা কিভাবে একটা সি প্রোগ্রাম build করে run করতে হয় তা জানার চেষ্টা করবো।

## শুরুর আগে
সি প্রোগ্রাম শুরুর আগে আমাদের ২ টা বিষয় ensure করতে হবে। প্রথমত আমাদের কম্পিউটার এ কোনো টেক্সট এডিটর আছে কিনা। দ্বিতীয়ত আমাদের কম্পিউটার এ কম্পাইলার আছে কিনা।

সভাবতই আমরা বেশিরভাগই উইন্ডোজ ইউজার। এই ক্ষেত্রে আমাদের প্রত্যেকের কম্পিউটার এ নোটপ্যাড নামক একটি টেক্সট এডিটর built in থাকে। আমরা সেটা ইউজ করতে পারি কোড লিখার জন্য। 

যারা লিনাক্স ইউজার আছেন তাদের ক্ষেত্রেও `nano` নামক একটা টেক্সট এডিটর built in থাকে maximum টাইম। অনেকের আবার `vim` ও ইনস্টল করা থাকে। তবে উপরোক্ত ২ তাই টার্মিনাল based। তাই আমরা gui ইউজ করবো। একত্রে একেকজনের এক এক এডিটর থাকতে পারে যেমন `geany`, `leafpad` ইত্যাদি। 

এখন এগুলা সব কিছু নিজেদেরকেই টাইপ করে লিখতে হয়। যদি এরকম টা না চাই তবে আমাদের জন্য আছে `IDE (Integrated Development Environment)` এবং `কোড এডিটর`। 

**IDE আবার ২ ধরনের।** একটা আমরা সফটওয়্যার হিসেবে ইনস্টল করে ব্যাবহার করি। অন্যটা ওয়েব based। 
For Example: [Online Gdb](https://www.onlinegdb.com/online_c_compiler)। যেটায় functionality limited থাকে। বেশিরভাগ programmer রাই IDE হিসেবে [codeblocks](https://www.codeblocks.org/) ব্যাবহার করে থাকে। আমরা সেটাই ব্যাবহার করবো। আর যদি মনে চায় যে কোড এডিটর এ কোড করবেন তাহলে [ভিজুয়্যাল স্টুডিও কোড](https://code.visualstudio.com/) ব্যাবহার করতে পারেন।

## এখন আসি কম্পাইলার এর ক্ষেত্রে
আমাদের সি প্রোগ্রামিং হচ্ছে একটি কম্পাইল্ড ল্যাঙ্গুয়েজ(বিস্তারিত পরবর্তী পর্বে থাকছে)। এজন্য আমাদের একটি কম্পাইলার ব্যাবহার করতে হবে। আমরা এই ক্ষেত্রে gcc কম্পাইলার ব্যাবহার করবো।
প্রথমেই আমাদের এই [লিংক](https://sourceforge.net/projects/codeblocks/files/Binaries/20.03/Windows/codeblocks-20.03mingw-setup.exe/download) থেকে compiler এর executable file টা ডাউনলোড করে নিতে হবে। পরবর্তীতে এটা ইনস্টল করে ফেলবো যেভাবে আমরা অন্যান্য সফটওয়্যার ইনস্টল করি। ইনস্টল করার পর আমাদের যেতে হবে সি ড্রাইভ এ। সেখানে আমরা codeblocks নাম এ একটা ফোল্ডার খুঁজে পাবো। আপনি যদি ডাইরেক্টলি সেটা খুজে না পান তাহলে প্রোগ্রাম ফাইলস ফোল্ডার এর ভিতর পেয়ে যাবেন। পরে আমাদের যেতে হবে বিন নামক ফোল্ডার এর ভিতর। 
এখানে আমাদের কে পুরো path টা copy করে নিতে হবে। 

এটা এমন হবে দেখতে: `C:\MinGW\bin`
অথবা, `C:\Program Files\MinGW\bin`

Copy করার পর আমরা উইন্ডোজ এর সার্চ মেনু তে সার্চ করবো environment variable যেটা সামনে আসবে সেটা ওপেন করবো। পরে উপরের দিকে user variable section থেকে path select করে এডিট বাটন এ ক্লিক করতে হবে।পড়ে নিউ তে ক্লিক করে কপি করা path টা paste করে এন্টার বাটন এ ক্লিক করতে হবে। পরে ok করতে হবে। পরে সেভ/ok/Apply করে বের হয়ে যাবো। এখন আবার সার্চ করবো cmd লিখে যেটা আসবে সেটা ওপেন করতে হবে।সেখানে গিয়ে লিখতে হবে `gcc --version` এখানে একটা ভার্সন নম্বর দেখাবে এখন। এখন আমাদের কাছে g++ command টা available হয়ে গেছে। আমাদের মূল কাজ শেষ। 

## এখন আপনি যদি লিনাক্স ইউজার হয়ে থাকেন তাহলে নিচের পদ্ধতি গুলো অনুসরণ করেন

আপনি যদি dabian based distribution ব্যাবহার করে থাকেন,(`Ubuntu`, `Kali`, `Popos`, `Linux mint`, `Zorin Os`)
`sudo apt install gcc`

আপনি যদি আর্চ based distribution ব্যাবহার করে থাকেন,(`Manjaro`, `Arco Linux`, `Endeavour Os`, `Garuda Linux`, `Xero Linux`, `Arch Craft`, `Vanilla Arch`)
`sudo pacman -S gcc`

Congratulations এই পর্যন্ত কমপ্লিট করার জন্য।

এখন আমরা চাইলে কোড ব্লকস বা ভিজুয়্যাল স্টুডিও কোড ওপেন করে কোড লিখা শুরু করে দিতে পারি।  

## Codeblocks এর ক্ষেত্রে:
সফটওয়্যার টি ওপেন করে ফাইল মেনু থেকে নিউ ফাইল সিলেক্ট করতে হবে। এখন কোথায় ফাইল টি সেভ করতে চান সেটা সিলেক্ট করবেন। ধরি আমরা ডেস্কটপ সিলেক্ট করলাম। এখন এখানে আমরা একটা ফোল্ডার খুলবো সি প্রোগ্রাম নাম দিয়ে। এখন এই ফোল্ডার এর ভিতরে যাবো এবং right click করে একটা টেক্সট ফাইল create করবো। ফাইল টা rename করে নাম দিবো `main.c` কারণ সি প্রোগ্রাম ফাইল এর এক্সটেনশন .c হয়ে থাকে।  সবার শেষে ওপেন বাটন এ ক্লিক করে ওপেন করে নিবো code blocks এ। 

এখন নিচের কোড টুকু লিখে ফেলি। 

```
// c program to print hello world in the terminal
#include <stdio.h>

int main(){
  printf("Hello World!");
  
  return 0;
}
```


কন্ট্রোল + S চেপে ফাইল টা সেভ করে নেই। এখন উপরের দিকে খেয়াল করে build menu পাবেন। Hover করে build and run অপশন টা তে ক্লিক করেন। দেখবেন আপনার কমান্ড প্রমট টা ওপেন হয়ে সেখানে Hello World! লেখাটি প্রিন্ট হয়েছে। 

Congratulations Again আপনি আপনার প্রথম সি প্রোগ্রাম এর কোড build করে রান করতে পেরেছেন। 


## ভিজুয়াল স্টুডিও কোড এর ক্ষেত্রে:
আগের মতই আপনার সি প্রোগ্রাম ফোল্ডার টি ওপেন করে ফেলেন। এখন মেনুবার থেকে টার্মিনাল ক্লিক করে নিউ টার্মিনাল ক্লিক করেন। নিচে ওপেন হওয়া টার্মিনাল এ টাইপ করেন `g++ main.c`। উক্ত কমান্ড টি আপনার সি প্রোগ্রাম ফাইল টিকে build করে দিবে। এখন build করা ফাইল টা রান করার জন্য টাইপ করেন `./a.exe`। দেখবেন আগের মতই আপনার টার্মিনাল এ `Hello World!` লেখাটি প্রিন্ট হয়েছে। 

আজকের পর্ব এই পর্যন্তই থাকবে। পরবর্তী পর্বে আমরা কম্পাইল্ড ল্যাঙ্গুয়েজ বনাম ইন্টারপ্রেটেড ল্যাঙ্গুয়েজ সম্পর্কে জানবো।