# Mobile Application Development (MAD) - Part 2
**Questions 21 to 35: Descriptive Questions**

এই অংশে মূলত Android এর কোর কনসেপ্ট এবং Java OOP এর কিছু ব্যাখ্যামূলক প্রশ্নের উত্তর দেওয়া হলো।

---

### 21. Explain key features of Android.
**English:** Some key features of Android are:
1. Open-source and highly customizable.
2. Supports a wide variety of hardware and multiple languages.
3. Uses SQLite database for lightweight data storage.
4. Supports background services and rich multimedia formats.
**বাংলা সামারি:** অ্যান্ড্রয়েড ফ্রি এবং ওপেন-সোর্স, ইচ্ছামতো কাস্টমাইজ করা যায়, অনেক ভাষা সাপোর্ট করে, আর ডাটা সেভ করার জন্য এতে SQLite নামের একটা ছোট ডাটাবেস থাকে।

### 22. Describe Android architecture layers briefly.
**English:** The Android architecture consists of 5 layers from bottom to top:
1. **Linux Kernel:** Manages hardware drivers (camera, battery).
2. **HAL:** Bridges hardware with the software.
3. **Android Runtime (ART) & Libraries:** Runs apps and provides core C/C++ libraries.
4. **Java API Framework:** Provides Java APIs for developers to build apps.
5. **System Apps:** The top layer containing user and built-in apps (e.g., Dialer, Browser).
**বাংলা সামারি:** ৫টা লেয়ার। লিনাক্স কার্নেল হার্ডওয়্যার সামলায়, HAL সেটাকে সফটওয়্যারের সাথে জোড়া লাগায়, ART অ্যাপ রান করে, API ফ্রেমওয়ার্ক ডেভেলপারদের কোড করতে সাহায্য করে, আর System Apps হলো আমাদের নরমাল অ্যাপগুলো।

### 23. Explain the role of HAL in Android.
**English:** Hardware Abstraction Layer (HAL) acts as a bridge between the physical hardware components and the Android software framework. It allows the software to interact with the hardware without knowing its internal implementation details.
**বাংলা সামারি:** HAL হলো একটা ব্রিজ বা অনুবাদক। সফটওয়্যার যখন ক্যামেরাকে ছবি তুলতে বলে, HAL সেই কমান্ডটা ক্যামেরার ভাষায় বুঝিয়ে দেয়।

### 24. Explain Activity lifecycle.
**English:** The Activity lifecycle consists of 7 main callback methods that manage the state of an activity from its creation to destruction:
1. `onCreate()`: Called when the activity is first created (Initial setup).
2. `onStart()`: Called when the activity becomes visible to the user.
3. `onResume()`: Called when the user starts interacting with the app.
4. `onPause()`: Called when the activity is partially hidden (e.g., a popup appears or a call comes in).
5. `onStop()`: Called when the activity is completely hidden (e.g., pressing the home button).
6. `onRestart()`: Called when the activity is coming back from the stopped state.
7. `onDestroy()`: Called when the activity is completely closed or killed by the system.

**বাংলা সামারি:** একটা অ্যাপ ওপেন করা থেকে শুরু করে ক্লোজ করা পর্যন্ত ৭টা ধাপ পার হয়। 
*(মনে রাখার ট্রিক: CSR PSD $\rightarrow$ Create, Start, Resume, Pause, Stop, Destroy)*
*   **অ্যাপ ওপেন করলে সিরিয়ালি:** `onCreate` $\rightarrow$ `onStart` $\rightarrow$ `onResume` কল হয়।
*   **মিনিমাইজ করলে বা অন্য অ্যাপে গেলে:** `onPause` $\rightarrow$ `onStop` কল হয়।
*   **পুরোপুরি কেটে দিলে:** `onDestroy` কল হয়।

### 25. Explain the purpose of AndroidManifest file.
**English:** It acts as the control center of the app. It declares the app's components (Activities, Services), requires permissions (like internet or camera access), and defines the minimum API level needed to run the app.
**বাংলা সামারি:** এটা অ্যাপের রুট বা মেইন ফাইল। অ্যাপে কয়টা পেজ আছে, অ্যাপটা ক্যামেরা বা ইন্টারনেট ইউজ করবে কি না (Permissions)— এসব এই ফাইলে বলে দিতে হয়।

### 26. Describe how Intents work.
**English:** Intents are used to communicate between Android components. 
* **Explicit Intent:** Used to start a specific component within the same app (e.g., jumping from Screen A to Screen B). 
* **Implicit Intent:** Asks the system to find another app that can handle the request (e.g., opening a web link in Chrome).
**বাংলা সামারি:** Intent হলো এক পেজ থেকে অন্য পেজে বা অন্য অ্যাপে যাওয়ার মাধ্যম। Explicit Intent নিজের অ্যাপের ভেতরেই কাজ করে, আর Implicit Intent অন্য অ্যাপকে (যেমন ব্রাউজার বা ক্যামেরা) ওপেন করতে বলে।

### 27. Explain LinearLayout with example.
**English:** LinearLayout arranges its child views in a single straight line, either vertically (top to bottom) or horizontally (left to right).
**Example (XML snippet):**
```xml
<LinearLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">
    <Button android:text="Button 1" />
    <Button android:text="Button 2" />
</LinearLayout>
```
**বাংলা সামারি:** এটা বাটন বা টেক্সটগুলোকে সোজা এক লাইন ধরে সাজায়। লম্বালম্বি (Vertical) বা পাশাপাশি (Horizontal)।

### 28. Explain ConstraintLayout features.
**English:** ConstraintLayout allows developers to create complex layouts with a flat view hierarchy. Features include positioning views relative to each other (using constraints), using guidelines, and optimizing performance by avoiding nested layouts.
**বাংলা সামারি:** এটা সবচেয়ে আধুনিক লেআউট। এখানে একটা বাটনের সাথে স্প্রিংয়ের মতো টেনে আরেকটা বাটন বা স্ক্রিনের সীমানা কানেক্ট করে দেওয়া যায়। এতে স্ক্রিন সাইজ বদলালেও ডিজাইন ভাঙে না।

### 29. Describe View vs ViewGroup.
**English:**
* **View:** A single UI element like a Button, TextView, or ImageView.
* **ViewGroup:** A container that holds multiple Views or other ViewGroups inside it (like LinearLayout or ConstraintLayout).
**বাংলা সামারি:** View হলো একটা সিঙ্গেল জিনিস (যেমন একটা বাটন)। আর ViewGroup হলো একটা বাক্স বা কন্টেইনার, যার ভেতরে অনেকগুলো View (বাটন, টেক্সট) একসাথে রাখা যায়।

### 30. Explain abstraction in Java.
**English:** Abstraction is the process of hiding the internal implementation details and showing only the essential features to the user. It is achieved using abstract classes and interfaces.
**Example (Java Code):**
```java
abstract class Vehicle {
    abstract void brake(); // Implementation is hidden
}
```
**বাংলা সামারি:** ভেতরের কঠিন মেকানিজম লুকিয়ে শুধু দরকারি জিনিসটা ইউজারকে দেখানো। যেমন- ব্রেক চাপলে গাড়ি থামে, কিন্তু ভেতরের তার বা গিয়ার কীভাবে কাজ করে সেটা আপনার জানার দরকার নেই।

### 31. Explain polymorphism with example.
**English:** Polymorphism means "many forms." It allows one method to perform different tasks based on the object that invokes it.
**Example (Java Code):**
```java
Animal myAnimal = new Dog();
myAnimal.makeSound(); // Outputs: Bark!

Animal myOtherAnimal = new Cat();
myOtherAnimal.makeSound(); // Outputs: Meow!
```
**বাংলা সামারি:** বহুরূপী! একই ফাংশন বিভিন্ন জায়গায় বিভিন্ন রূপ নেয়। যেমন `makeSound()` ফাংশন ডাকলে কুকুর 'ঘেউ' করবে, আর বিড়াল 'মিউ' করবে।

### 32. Describe constructor usage in Java.
**English:** A constructor is a special block of code used to initialize an object when it is created. It has the exact same name as the class and has no return type.
**Example (Java Code):**
```java
public class Car {
    String color;
    // This is the constructor
    public Car() {
        color = "Red"; // Default value
    }
}
```
**বাংলা সামারি:** যখন কোনো ক্লাসের অবজেক্ট তৈরি করা হয়, তখন শুরুতেই কিছু ডিফল্ট ভ্যালু (যেমন- গাড়ির ডিফল্ট কালার লাল) সেট করে দেওয়ার জন্য কনস্ট্রাক্টর ব্যবহার করা হয়।

### 33. Explain how ListView works.
**English:** ListView displays a vertically scrollable list of items. It works with an Adapter, which acts as a bridge to pull data from a source (like an array) and convert each data item into a view row inside the list.
**বাংলা সামারি:** স্ক্রিনে অনেকগুলো আইটেম লিস্ট আকারে দেখায়। ডাটা (যেমন নামের লিস্ট) থেকে একটা একটা করে নাম নিয়ে স্ক্রিনে দেখানোর কাজটা Adapter করে দেয়।

### 34. Explain RecyclerView basics.
**English:** RecyclerView is an advanced and highly flexible version of ListView. It improves performance by "recycling" the views that scroll off the screen instead of creating new ones, which saves memory.
**বাংলা সামারি:** এটা ListView এর প্রো-ম্যাক্স ভার্সন! লিস্ট স্ক্রল করার সময় যে আইটেমগুলো স্ক্রিনের উপরে চলে যায়, সেগুলোকে মেমরি থেকে ডিলিট না করে, ওই একই বক্সকে নিচের নতুন আইটেম দেখানোর জন্য রি-ইউজ বা রিসাইকেল করে। এতে ফোন হ্যাং হয় না।

### 35. Explain Adapter in Android.
**English:** An Adapter acts as a bridge between a UI component (like ListView or RecyclerView) and the data source. It converts raw data items into UI view items so they can be displayed on the screen.
**বাংলা সামারি:** ডাটাবেস বা অ্যারেতে থাকা ডাটাগুলোকে টেনে এনে স্ক্রিনে সুন্দরভাবে দেখানোর জন্য Adapter একটা ব্রিজ বা মাধ্যম হিসেবে কাজ করে।
