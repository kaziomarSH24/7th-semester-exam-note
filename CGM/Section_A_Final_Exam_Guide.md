# Section A: Final Exam Guide (Matched with PDF)

এই নোটটি আপনার দেওয়া পিডিএফ (সাজেশন) এর সাথে হুবহু মিলিয়ে তৈরি করা হয়েছে। পরীক্ষার খাতায় কোন প্রশ্নে ডায়াগ্রাম দিতে হবে আর কোনটায় লাগবে না, তা প্রতিটি উত্তরের নিচে **[Exam Tip]** আকারে দেওয়া আছে।

---

### 1. 4/8 connected region
*   **4-connected region:** From a given pixel, the region that you can get to by a series of 4-way moves (N, S, E, and W).
*   **8-connected region:** From a given pixel, the region that you can get to by a series of 8-way moves (N, S, E, W, NE, NW, SE, and SW).
> 📌 **[Exam Tip: ডায়াগ্রাম দিতে হবে!]** খাতায় অবশ্যই ছোট করে ডট বা গোল্লা দিয়ে প্লাস (+) আকৃতির 4-connected এবং চারকোনা বক্সের মতো 8-connected এর ডায়াগ্রামটি এঁকে দেবেন। এতে কোনো মার্কস কাটা যাবে না।

---

### 2. Flood fill algorithm
*   Used when an area defined with multiple color boundaries.
*   Start at a point inside a region.
*   Replace a specified interior color (old color) with fill color.
*   Fill the 4-connected or 8-connected region until all interior points being replaced.
```c
void FloodFill4(int x, int y, color newcolor, color oldColor) {
    if(ReadPixel(x, y) == oldColor) {
        FloodFill4(x+1, y, newcolor, oldColor);
        FloodFill4(x-1, y, newcolor, oldColor);
        FloodFill4(x, y+1, newcolor, oldColor);
        FloodFill4(x, y-1, newcolor, oldColor);
    }
}
```
> 📌 **[Exam Tip: ডায়াগ্রাম লাগবে না।]** শুধু পয়েন্টগুলো লিখবেন আর ব্র্যাকেটে ছোট করে উপরের ৫ লাইনের কোডটুকু লিখে দেবেন।

---

### 3. Scanline Fill algorithm and its special cases
*   Intersect scanline with polygon edges.
*   Fill between pairs of intersections.
*   **Basic algorithm:** For y = ymin to ymax:
    1. intersect scanline y with each edge
    2. sort intersections by increasing x [p0, p1, p2, p3]
    3. fill pairwise (p0->p1, p2->p3, ...)
*   **Special Case (Intersection is an edge end point):**
    *   **Case 1:** Intersection points: (p0, p1, p2). In this case we compute the intersection of the scanline with edge e1 and e2 separately, we will get the intersection point p1 twice. So we keep both of the p1 -> (p0, p1, p1, p2) so we can still fill pairwise.
    *   **Case 2:** However, in this case we don’t want to count p1 twice (p0, p1, p1, p2, p3), otherwise we will fill pixels between p1 and p2, which is wrong.
> 📌 **[Exam Tip: ডায়াগ্রাম দিতে হবে!]** Case 1 এবং Case 2 বোঝানোর জন্য পাহাড়ের বা জিগজ্যাগ লাইনের ওপর দিয়ে যাওয়া Scanline-এর ছবিটা (p0, p1, p2 চিহ্নিত করে) অবশ্যই দিতে হবে। ছবি ছাড়া Special Case বোঝানো সম্ভব নয়।

---

### 4. Straight forward approach
*   **Concept:** It uses the basic mathematical equation of a straight line: $y = mx + b$.
*   **How it works:** For every $x$ coordinate from $x_1$ to $x_2$, it calculates the exact $y$ coordinate using multiplication and division.
*   **Disadvantage:** Multiplication is very slow for computers. Doing this for every single pixel makes this approach very inefficient.

**A Straightforward Implementation:**
```c
DrawLine(int x1,int y1, int x2,int y2, int color) {
    float y;
    int x;
    for (x=x1; x<=x2; x++) {
        y = y1 + (x-x1)*(y2-y1)/(x2-x1);
        WritePixel(x, Round(y), color);
    }
}
```
> 📌 **[Exam Tip: ডায়াগ্রাম লাগবে না।]** শুধু এই ফর্মুলা বা কোডটুকু লিখে দিলেই হবে।

---

### 5. Steps of DDA and its advantages
DDA is a line drawing algorithm used to generate a straight line by calculating intermediate pixel positions.
**Steps:**
1. Calculate the differences: $\Delta x = x_2 - x_1$ and $\Delta y = y_2 - y_1$
2. Calculate the slope: $m = \frac{\Delta y}{\Delta x}$
3. Check the condition to find increments:
   *   **Case 1 (If $|m| \le 1$):** 
       *   $x$ increments by 1: $x_{k+1} = x_k + 1$
       *   $y$ increments by $m$: $y_{k+1} = y_k + m$
   *   **Case 2 (If $|m| > 1$):** 
       *   $y$ increments by 1: $y_{k+1} = y_k + 1$
       *   $x$ increments by $\frac{1}{m}$: $x_{k+1} = x_k + \frac{1}{m}$
4. Start from the initial point $(x_1, y_1)$.
5. Plot the current pixel after rounding the calculated coordinates.
6. Add the increments to get the next position.
7. Repeat until the endpoint $(x_2, y_2)$ is reached.

**Advantages of DDA:**
*   Simple and easy to implement.
*   Uses incremental calculations.
*   Faster than repeatedly calculating the complete line equation.
*   Can draw lines in different slopes.
> 📌 **[Exam Tip: ডায়াগ্রাম লাগবে না।]** থিওরি প্রশ্নে শুধু এই ৭টি স্টেপ এবং সুবিধাগুলো পয়েন্ট আকারে লিখলেই হবে।

---

### 6. Types of light
1.  **Ambient Light:** Background light. It has no specific source and no direction. It makes everything slightly visible.
2.  **Point Light:** Like a lightbulb. Light spreads out equally in all directions from one single point.
3.  **Directional Light:** Like the Sun. The light source is so far away that all light rays travel in straight, parallel lines.
4.  **Spotlight:** Like a flashlight. Light only shines inside a specific cone shape.
> 📌 **[Exam Tip: ডায়াগ্রাম লাগবে না।]**

---

### 7. Intensity calculation procedure for a pixel
1. Apply the illumination (lighting) model to calculate the intensity of light at a point on the object surface.
2. Consider the light sources and their color and intensity.
3. Calculate the reflection components: Ambient reflection, Diffuse reflection, Specular reflection.
4. Add the contributions from all light sources and reflected light.
5. Apply intensity attenuation, if required.
6. Calculate each RGB component separately to obtain the final pixel intensity/color.
*   *Surface rendering applies the lighting model to obtain pixel intensities for all projected surface positions in a scene. The intensity is calculated by considering ambient, diffuse, and specular reflections, along with multiple light sources, attenuation, and RGB color components.*
> 📌 **[Exam Tip: ডায়াগ্রাম লাগবে না।]** শুধু এই ৬টি পয়েন্ট সিরিয়ালি লিখে দেবেন।91724

9172491724

9172491724

91724