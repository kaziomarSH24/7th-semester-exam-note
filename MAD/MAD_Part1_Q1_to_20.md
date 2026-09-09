# Mobile Application Development (MAD) - Part 1
**Questions 1 to 20: Basic Definitions**

এই নোটে প্রথম ২০টি বেসিক প্রশ্নের উত্তর খুব সহজ ভাষায় দেওয়া হলো। পরীক্ষার খাতায় লেখার জন্য **English Answer** এবং কনসেপ্ট ক্লিয়ার করার জন্য **বাংলা সামারি** দেওয়া আছে।

---

### 1. Define Android OS.
**English:** Android is an open-source, Linux-based operating system designed primarily for touchscreen mobile devices such as smartphones and tablets.
**বাংলা সামারি:** অ্যান্ড্রয়েড হলো গুগলের তৈরি একটা ওপেন-সোর্স অপারেটিং সিস্টেম, যেটা লিনাক্স (Linux) এর ওপর ভিত্তি করে বানানো হয়েছে। 

### 2. What is Android SDK?
**English:** Android SDK (Software Development Kit) is a collection of software tools and libraries required to build, test, and debug Android applications.
**বাংলা সামারি:** SDK হলো একটা টুলবক্স। রাজমিস্ত্রির যেমন হাতুড়ি-কোদাল লাগে, তেমনি অ্যান্ড্রয়েড অ্যাপ বানাতে ডেভেলপারদের এই SDK বা টুলবক্সটা লাগে। 

### 3. What is JDK?
**English:** JDK (Java Development Kit) is a software development environment used for developing Java applications and applets. It includes JRE and development tools.
**বাংলা সামারি:** যেহেতু অ্যান্ড্রয়েড অ্যাপ জাভা (Java) দিয়ে লেখা যায়, তাই জাভায় কোড করার জন্য এই JDK টুলকিটটা দরকার হয়।

### 4. What is Android Runtime (ART)?
**English:** Android Runtime (ART) is the managed runtime used by applications and some system services on Android. It replaces the older Dalvik virtual machine and executes Dalvik Executable format (DEX) files.
**বাংলা সামারি:** ART হলো সেই ইঞ্জিন যেটা আপনার লেখা কোডগুলোকে রান করে বা চালায়। এটা আগের 'Dalvik' ইঞ্জিনকে রিপ্লেস করেছে যেন অ্যাপ আরও ফাস্ট চলে।

### 5. Name the layers of Android architecture.
**English:** The 5 main layers are:
1. Linux Kernel
2. Hardware Abstraction Layer (HAL)
3. Android Runtime & Native Libraries
4. Java API Framework
5. System Apps
**💡 Mnemonic:** "L H A J S" (লুকিং হ্যান্ডসাম অ্যান্ড জাস্ট স্মার্ট)

### 6. What is Linux Kernel in Android?
**English:** The Linux Kernel is the bottom-most layer of the Android architecture. It provides core system services such as memory management, power management, and device drivers (camera, bluetooth, etc.).
**বাংলা সামারি:** এটা একদম নিচের লেয়ার যেটা মোবাইলের হার্ডওয়্যার (যেমন: ক্যামেরা, ব্যাটারি) এর সাথে সরাসরি কথা বলে।

### 7. Define Activity.
**English:** An Activity represents a single screen with a user interface in an Android application.
**বাংলা সামারি:** অ্যাপ ওপেন করলে আপনি মোবাইলে যে স্ক্রিনটা দেখতে পান, সেটাই হলো Activity। একটা অ্যাপে অনেকগুলো Activity (স্ক্রিন) থাকতে পারে।

### 8. What is Service?
**English:** A Service is an application component that can perform long-running operations in the background, and it does not provide a user interface.
**বাংলা সামারি:** Service হলো ব্যাকগ্রাউন্ডে চলা কাজ। যেমন: আপনি অ্যাপ থেকে বের হয়ে গেলেও স্পটিফাইতে গান বাজতে থাকে, এটা Service এর কাজ।

### 9. What is Broadcast Receiver?
**English:** A Broadcast Receiver is an Android component that allows an application to respond to system-wide broadcast announcements (e.g., low battery, screen turned off).
**বাংলা সামারি:** এটা অ্যাপের 'কান' হিসেবে কাজ করে। মোবাইলে চার্জ কমে গেলে বা ওয়াইফাই অন হলে সিস্টেম যে সিগন্যাল দেয়, সেটা শোনার কাজ করে Broadcast Receiver।

### 10. What is Content Provider?
**English:** A Content Provider manages access to a structured set of data and allows sharing data securely between different applications.
**বাংলা সামারি:** এক অ্যাপের ডাটা অন্য অ্যাপকে সিকিউরলি দেওয়ার কাজ করে। যেমন: হোয়াটসঅ্যাপ যখন আপনার মোবাইলের কন্ট্যাক্ট লিস্ট (Phonebook) পড়তে চায়, তখন Phonebook তার Content Provider দিয়ে ডাটা শেয়ার করে।

### 11. What is AndroidManifest.xml?
**English:** It is an essential XML file in every Android project that provides critical information about the app to the Android system, such as permissions, activities, and app version.
**বাংলা সামারি:** এটা হলো অ্যাপের "জাতীয় পরিচয়পত্র"। অ্যাপে কী কী স্ক্রিন আছে, কী কী পারমিশন লাগবে— সব এই ফাইলে লেখা থাকে।

### 12. Define Intent.
**English:** An Intent is a messaging object used to request an action from another app component, such as starting a new Activity or starting a Service.
**বাংলা সামারি:** Intent মানে হলো 'উদ্দেশ্য' বা 'চিঠি'। এক স্ক্রিন থেকে অন্য স্ক্রিনে (Activity) যাওয়ার জন্য এই Intent বা চিঠি ব্যবহার করা হয়।

### 13. What is LinearLayout?
**English:** LinearLayout is a view group that aligns all its children in a single direction, either vertically or horizontally.
**বাংলা সামারি:** এটা এমন একটা লেআউট যেটা স্ক্রিনের বাটন বা টেক্সটগুলোকে সোজা এক লাইনে (হয় লম্বালম্বি, না হয় পাশাপাশি) সাজিয়ে রাখে।

### 14. What is RelativeLayout?
**English:** RelativeLayout is a view group that displays child views in relative positions (e.g., to the right of another view, or below another view).
**বাংলা সামারি:** এই লেআউটে একটা বাটনের সাপেক্ষে আরেকটা বাটন বসানো যায়। যেমন: "লগিন বাটনের ঠিক নিচে পাসওয়ার্ড ফিল্ড বসাও।"

### 15. What is View in Android?
**English:** A View is the basic building block of a UI in Android. It is a small rectangular area on the screen that draws something (like text or a button) and handles events.
**বাংলা সামারি:** স্ক্রিনে যা কিছু দেখা যায় (বাটন, টেক্সট, ইমেজ) তার সবই হলো এক একটা View।

### 16. Define class in Java.
**English:** A class is like a paper blueprint or design. We use it to create real objects. It contains variables and methods.
**Example:**
```java
public class Car {
    String brand;
    void drive() { }
}
```
**বাংলা সামারি:** ক্লাস হলো কোনো কিছু বানানোর 'নকশা' বা 'ছাঁচ'। যেমন: গাড়ির ব্লু-প্রিন্ট হলো ক্লাস, আর আসল গাড়িটা হলো অবজেক্ট।

### 17. What is object?
**English:** An object is a real thing made from a class. If a class is a house plan, the object is the actual house. It takes up space in memory.
**Example:**
```java
Car myCar = new Car(); // myCar is the object
```
**বাংলা সামারি:** অবজেক্ট হলো ক্লাসের বাস্তব রূপ। নকশা (Class) দেখে যে আসল গাড়িটা বানানো হলো, সেটাই Object।

### 18. What is encapsulation?
**English:** Encapsulation means hiding the sensitive data of a class. It combines data (variables) and functions (methods) into a single unit (like a capsule) to keep the data safe from outside changes.
**Example:** Using `private` variables and public `getter/setter` methods.
```java
class Person {
    private String name; // Hidden data
    public String getName() { return name; } // Public access
}
```
**বাংলা সামারি:** ক্যাপসুলের ভেতরে যেমন ওষুধ লুকানো থাকে, তেমনি ডাটা আর কোডকে একটা ক্লাসের ভেতরে লুকিয়ে রাখাকে Encapsulation বলে। 

### 19. What is inheritance?
**English:** Inheritance means one class takes the features of another class. It works like a child getting properties from a parent. It helps us reuse old code.
**Example:** Using the `extends` keyword.
```java
class Animal { }
class Dog extends Animal { } // Dog inherits from Animal
```
**বাংলা সামারি:** বাবার সম্পত্তি যেমন ছেলে পায়, তেমনি এক ক্লাসের কোড অন্য ক্লাস যখন হুবহু ব্যবহার করতে পারে, তাকে Inheritance বলে। এতে বারবার কোড লিখতে হয় না।

### 20. What is ListView?
**English:** ListView is a UI element that shows many items in a long vertical list. Users can scroll the list up and down. It gets its data from an Adapter.
**বাংলা সামারি:** স্ক্রিনে অনেকগুলো আইটেম লিস্ট আকারে (যেমন: মেসেঞ্জারের চ্যাট লিস্ট বা কন্ট্যাক্ট লিস্ট) দেখানোর জন্য ListView ব্যবহার করা হয়, যা স্ক্রল করা যায়।
