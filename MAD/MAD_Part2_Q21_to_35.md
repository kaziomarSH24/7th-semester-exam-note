# Mobile Application Development (MAD) - Part 2
**Questions 21 to 35: Descriptive Questions (Updated with Tricks)**

এই অংশে পিডিএফের মতো হুবহু পয়েন্ট করে দেওয়া হলো, সাথে **Memory Tricks** অ্যাড করা হয়েছে যেন পরীক্ষার হলে পয়েন্টগুলো জাস্ট জাদুর মতো মনে পড়ে যায়!

---

### 21. Explain key features of Android.
**English:**
1. **Open Source** – Android is an open-source operating system.
2. **User Friendly** – It has an easy and simple user interface.
3. **Multitasking** – It can run multiple applications at the same time.
4. **Connectivity** – It supports Wi-Fi, Bluetooth, mobile network, and USB.
5. **Multimedia Support** – It supports audio, video, images, and games.
6. **Large App Support** – Android supports a large number of applications.
7. **Hardware Support** – It supports camera, GPS, sensors, and other hardware.

**💡 Mnemonic (মনে রাখার ট্রিক): "MOM CHUL"** (মম চুল)
*   **M** - Multitasking
*   **O** - Open Source
*   **M** - Multimedia Support
*   **C** - Connectivity
*   **H** - Hardware Support
*   **U** - User Friendly
*   **L** - Large App Support

**বাংলা সামারি:** ট্রিকটা মনে রাখলেই ৭টা পয়েন্ট খাতায় নামিয়ে দিতে পারবেন। 

### 22. Describe Android architecture layers briefly.
**English:** Android architecture is divided into five main layers:
1. **Applications** – Contains apps like Phone, Camera, etc.
2. **Application Framework** – Provides services for developing apps.
3. **Android Runtime and Native Libraries** – Runs applications and provides important functions.
4. **Hardware Abstraction Layer (HAL)** – Connects Android software with hardware devices.
5. **Linux Kernel** – The base layer. Manages memory, security, and hardware drivers.

**💡 Mnemonic (মনে রাখার ট্রিক): "AA AHL"** (আহাল)
*   **A** - Applications
*   **A** - Application Framework
*   **A** - Android Runtime
*   **H** - HAL
*   **L** - Linux Kernel

### 23. Explain the role of HAL in Android.
**English:** 
* It works between Android software and hardware.
* It provides a standard interface for hardware devices.
* It helps applications use hardware features (like camera, Bluetooth).
* It hides hardware-specific details from the Android system.
* **So, HAL makes communication between Android software and hardware easier.**
**বাংলা সামারি:** HAL হলো একটা ট্রান্সলেটর। এটা সফটওয়্যার আর হার্ডওয়্যারের মাঝখানে বসে। সফটওয়্যার যখন ক্যামেরাকে ছবি তুলতে বলে, HAL সেই কমান্ডটা ক্যামেরার ভাষায় বুঝিয়ে দেয়।

### 24. Explain Activity lifecycle.
**English:** The main lifecycle methods are:
1. `onCreate()` – Called when the Activity is created.
2. `onStart()` – The Activity becomes visible to the user.
3. `onResume()` – The Activity is ready for user interaction.
4. `onPause()` – The Activity is partially hidden.
5. `onStop()` – The Activity is no longer visible.
6. `onDestroy()` – The Activity is removed from memory.

**💡 Mnemonic (মনে রাখার ট্রিক): "CSR PSD"** (ধরুন, কাস্টমার সার্ভিস রিপ্রেজেন্টেটিভ - CSR, ফটোশপ ফাইল - PSD নিয়ে কাজ করছে)
*   **C** - Create
*   **S** - Start
*   **R** - Resume
*   **P** - Pause
*   **S** - Stop
*   **D** - Destroy

### 25. Explain the purpose of AndroidManifest file.
**English:** Its main purposes are:
1. It contains basic information about the application.
2. It declares activities, services, and broadcast receivers.
3. It defines required permissions.
4. It specifies the application components.
5. It tells Android how the application should work.
**বাংলা সামারি:** এটা অ্যাপের রুট বা মেইন ফাইল। অ্যাপে কয়টা পেজ আছে, অ্যাপটা ক্যামেরা বা ইন্টারনেট ইউজ করবে কি না (Permissions)— এসব এই ফাইলে বলে দিতে হয়।

### 26. Describe how Intents work.
**English:** 
* It can start another Activity or Service.
* It can send data from one Activity to another.
* It can request an action, such as opening a website.
* Intents can be **Explicit** or **Implicit**.
* **Example:** An Intent can open the second Activity from the first Activity.
**বাংলা সামারি:** Intent হলো এক পেজ থেকে অন্য পেজে বা অন্য অ্যাপে যাওয়ার মাধ্যম। 

### 27. Explain LinearLayout with example.
**English:** 
* It can arrange views **horizontally** or **vertically**.
* In vertical layout, views are placed from top to bottom.
* In horizontal layout, views are placed from left to right.
* It is simple and easy to use.
**Example:**
```xml
<LinearLayout android:orientation="vertical">
    <TextView android:text="Name" />
    <Button android:text="Submit" />
</LinearLayout>
```

### 28. Explain ConstraintLayout features.
**English:** 
1. **Flexible Design** – It can create complex UI designs easily.
2. **Constraints** – Views can be connected to other views or the parent.
3. **Responsive UI** – It works well on different screen sizes.
4. **Less Nested Layouts** – It can reduce the need for many nested layouts.
5. **Better Performance** – Fewer nested layouts can improve performance.
**বাংলা সামারি:** এটা সবচেয়ে আধুনিক লেআউট। এখানে একটা বাটনের সাথে স্প্রিংয়ের মতো টেনে আরেকটা বাটন বা স্ক্রিনের সীমানা কানেক্ট করে দেওয়া যায় (Constraints)।

### 29. Describe View vs ViewGroup.
**English:**
* **View:** It is a single UI element (e.g., Button, TextView). It can be seen and interacted with.
* **ViewGroup:** It is a container for UI elements (e.g., LinearLayout). It manages and arranges child views.
**বাংলা সামারি:** View হলো একটা সিঙ্গেল জিনিস (যেমন বাটন)। আর ViewGroup হলো একটা কন্টেইনার, যার ভেতরে অনেকগুলো View রাখা যায়।

### 30. Explain abstraction in Java.
**English:** 
* It makes programs easier to understand.
* It reduces complexity.
* Abstraction can be achieved using **abstract classes** and **interfaces**.
* The user can use the required function without knowing its internal details.
**Example:**
```java
abstract class Animal {
    abstract void sound();
}
```
**বাংলা সামারি:** ভেতরের কঠিন মেকানিজম লুকিয়ে শুধু দরকারি জিনিসটা ইউজারকে দেখানো। 

### 31. Explain polymorphism with example.
**English:** Polymorphism means **one name can have many forms**.
* It allows the same method to perform different actions.
* It makes Java programs more flexible.
* Polymorphism can be achieved by **method overloading** and **method overriding**.
**Example:**
```java
class Animal {
    void sound() { System.out.println("Animal makes sound"); }
}
class Dog extends Animal {
    void sound() { System.out.println("Dog barks"); }
}
```

### 32. Describe constructor usage in Java.
**English:** A constructor is a special method used to initialize an object.
* It has the same name as the class.
* It has no return type.
* It is called automatically when an object is created.
* It is used to give initial values to object data.
* A class can have more than one constructor.
**Example:**
```java
class Student {
    Student() {
        System.out.println("Student created");
    }
}
```

### 33. Explain how ListView works.
**English:** 
* It displays items in a vertical list.
* It uses an **Adapter** to provide data.
* The Adapter connects the data with the ListView.
* Users can scroll through the list.
* Users can also click an item to perform an action.

### 34. Explain RecyclerView basics.
**English:** RecyclerView is an Android UI component used to display large lists efficiently. Its main parts are:
1. **RecyclerView** – Displays the list.
2. **Adapter** – Provides data to the list.
3. **ViewHolder** – Holds the views of each item.
4. **LayoutManager** – Controls how items are arranged.
*RecyclerView reuses old item views instead of creating new ones. So, it is fast and efficient.*

**💡 Mnemonic (মনে রাখার ট্রিক): "RAVL"** (রাভেল)
*   **R** - RecyclerView
*   **A** - Adapter
*   **V** - ViewHolder
*   **L** - LayoutManager

### 35. Explain Adapter in Android.
**English:** An Adapter connects data with a UI component like RecyclerView or ListView.
* It takes data from a data source.
* It creates or provides item views.
* It puts data into the views.
* It helps display many items in a list.
* It also helps update the UI when data changes.
