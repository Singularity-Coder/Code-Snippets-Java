![alt text](https://github.com/Singularity-Coder/Code-Snippets-Java/blob/main/assets/banner_java.png)
# Code Snippets Java 8
List of Java 8 topics and their code snippets!


## Package definition and imports
* **Import Class**
```Java
import java.util.Scanner;
```
* **Import Package**
```Java
import java.util.*;
```


## Comments
* **Single line comment**
```Java
// Single line comment or End-of-line comment
```
* **Multi-line comment**
```Java
/* Multi-line comment
or Inline comment 
or Block comment */
```
* **Documentation comment**
```Java
/**
* 
* Documentation comment used for explaining code
* Spans multiple lines
*
**/
```


## Printing to Console
```Java
System.out.println("Hello World");
```


## Data Types
* **Primitive or Value types**
```Java
byte myByte = 6;
short myShort = 7;
int myInt = 5234;
long myLong = 232245;
float myFloat = 5.99F;
double myDouble = 2.55;
char myChar = 'S';
boolean myBool = true;
```
* **Non-primitive or Reference or Object types**
```Java
Byte myByte = 6;
Short myShort = 7;
Integer myInt = 5234;
Long myLong = 2322L;
Float myFloat = 5.99F;
Double myDouble = 2.55;
Character myChar = 'S';
Boolean myBool = true;
String myString = "Hello World!";
```


## Constants and Variables
```Java
final String name = "Hithesh";
int age = 75;
static String profession = "Android Developer";
```


## Operators
* **Arithmetic Operators**
```Java
6 + 2
6 - 2
6 * 2
6 / 2
6 % 2
++6
--6
```
* **Assignment Operators**
```Java
int a = 6;
a = 5;
a += 3;
a -= 1;
a *= 6;
a /= 2;
a %= 3;
a &= 2;
a |= 3;
a ^= 5;
a >>= 3;
a <<= 5;
```
* **Comparison Operators**
```Java
int a = 6, b = 2;
a == b
a != b
a > b
a < b
a >= b
a <= b
```
* **Logical Operators**
```Java
int a = 6, b = 2;
a < 5 && b > 4
a < 5 || b > 4 
!(a < 5 && b > 4)
```


## Conditionals
* **If, else and else if statements**
```Java
int a = 6, b = 2;
if (a > 3 && b > 1) {
    System.out.println("Allowed");
} else if (a == 3 || b > 1) {
    System.out.println("Allowed");
} else {
    System.out.println("Not Allowed");
}
```
* **Ternary Operator**
```Java
String result = (a > 3 && b > 1) ? "Allowed" : "Not Allowed";
```
* **switch statements**
```Java
switch (a) {
    case 3:
        System.out.println("Not Allowed");
        break;
    case 4:
        System.out.println("Allowed");
        break;
    default:
        System.out.println("Not Allowed");
        break;
}
```


## Loops
* **For Loop**
```Java
final int[] arr = new int[]{1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
final int[] arrCharAsciiNums = new int[]{'a', 'b', 'c', 'd', 'e', 'f'};  // this also gives ASCII nums of the chars
final char[] arrChars = new char[]{'a', 'b', 'c', 'd', 'e', 'f'};
final List<Integer> list = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
final Map<Integer, String> map = new HashMap<Integer, String>();
map.put(1, "Hithesh");
map.put(2, "Iitesh");
map.put(3, "Jitesh");

for (int i = 0; i < arr.length; i++) {
    System.out.print(arr[i] + " "); // 1 2 3 4 5 6 7 8 9 10
}

for (int i = 0; i <= arr.length - 1; i++) {
    System.out.print(arr[i] + " "); // 1 2 3 4 5 6 7 8 9 10
}

for (int i = arr.length - 1; i >= 0; i--) {
    System.out.print(arr[i] + " "); // 10 9 8 7 6 5 4 3 2 1
}

for (int i = 0; i <= arr.length - 1; i += 2) {
    System.out.print(arr[i] + " "); // 1 3 5 7 9
}

for (int i = arr.length - 1; i >= 0; i -= 2) {
    System.out.print(arr[i] + " "); // 10 8 6 4 2
}

for (int num : arr) {
    System.out.print(num + " "); // 1 2 3 4 5 6 7 8 9 10
}

for (Map.Entry<Integer, String> num : map.entrySet()) {
    System.out.print(num + " "); // 1=Hithesh 2=Iitesh 3=Jitesh
}

for (Map.Entry<Integer, String> num : map.entrySet()) {
    System.out.print(num.getKey() + " "); // 1 2 3
}

for (Map.Entry<Integer, String> num : map.entrySet()) {
    System.out.print(num.getValue() + " "); // Hithesh Iitesh Jitesh
}
```
* **For-Each Loop**
```Java
for (int num : arr) {
	System.out.print(num + " ");	// 1 2 3 4 5 6 7 8 9 10 
}
```
* **While Loop**
```Java
int i = 0;
while (i < 5) {
    System.out.println(i);
    i++;
}
```
* **Do-While Loop**
```Java
int i = 1;
do {
    System.out.print(i + " ");	// 1 2 3 4 5 6 7 8 9 10 
    i++;
} while (i <= 10);
```
* **Break**
```Java
for (int i = 0; i < arr.length; i++) {
    if (i == 6) break;
    System.out.print(i + " ");	// 0 1 2 3 4 5 
}
```
* **Continue**
```Java
for (int i = 0; i < arr.length; i++) {
    if (i == 2) continue;
    if (i == 6) continue;
    System.out.print(i + " ");	// 0 1 3 4 5 7 8 9
}
```
* **Label**
```Java
Work1:
for (int i = 0; i < 5; i++) {
    Work2:
    for (int j = 0; j < 6; j++) {
        if (i == 3) continue Work1;
        System.out.print("i=" + i + ", j=" + j + " | ");	// i=0, j=0 | i=0, j=1 | i=0, j=2 | i=0, j=3 | i=0, j=4 | i=0, j=5 | i=1, j=0 | i=1, j=1 | i=1, j=2 | i=1, j=3 | i=1, j=4 | i=1, j=5 | i=2, j=0 | i=2, j=1 | i=2, j=2 | i=2, j=3 | i=2, j=4 | i=2, j=5 | i=4, j=0 | i=4, j=1 | i=4, j=2 | i=4, j=3 | i=4, j=4 | i=4, j=5 |
    }
}
```
* **Compute Loop time**
```Java
final long startTime = System.nanoTime();

int y = 0;
while (y < 100) {
    y++;
}

final long endTime = System.nanoTime();
final long timeTaken = endTime - startTime;
System.out.println("Time taken for this loop: " + timeTaken / 1.0E9 + " seconds"); // 48.387187825 seconds
System.out.printf("Time to compute: %5.1f seconds.%n", timeTaken / 1.0e9); // 48.4 seconds.
```
* **For loop as While loop**
```Java
for (long x = 0; ; ) {	// for loop that acts like while loop
    System.out.println("Iteration: " + x);
    if (x == 100000000000L) break;
    x++;
}
```


## Collections
* **ArrayList**
```Java
// Create
final ArrayList<String> myAnimeList = new ArrayList<String>();
myAnimeList.add("Code Geass");
myAnimeList.add("Death Note");
myAnimeList.add("Eccentric Family");
myAnimeList.add("Steins;Gate");
myAnimeList.add("Attack On Titan");
myAnimeList.add("Made In Abyss");
myAnimeList.add("Dragon Ball Z");
myAnimeList.add("Fate/Zero");
myAnimeList.add("Ghost In The Shell");
myAnimeList.add("One Punch Man");
myAnimeList.add("Mobile Suit Gundam 00");
myAnimeList.add("Monster");
myAnimeList.add("School Rumble");

// Print
System.out.println(myAnimeList);

// Read
myAnimeList.get(0);
myAnimeList.size();

// Update
myAnimeList.set(0, "Code Geass R2");

// Iterate
for (int i = 0; i < myAnimeList.size(); i++) {
    System.out.println(myAnimeList.get(i));
}
for (String anime : myAnimeList) {
    System.out.println(anime);
}

// Sort
Collections.sort(myAnimeList);

// Delete specific element
myAnimeList.remove(6);

// Delete All
myAnimeList.clear();
```
* **HashMap**
```Java
// Create, Update
final HashMap<Integer, String> myAnimeList = new HashMap<Integer, String>();
myAnimeList.put(1, "Code Geass");
myAnimeList.put(2, "Death Note");
myAnimeList.put(3, "Eccentric Family");
myAnimeList.put(4, "Steins;Gate");
myAnimeList.put(5, "Attack On Titan");

// Print
System.out.println(myAnimeList);

// Read
myAnimeList.get(1); // get by key
myAnimeList.size();

// Iterate
for (Map.Entry<Integer, String> animeSet : myAnimeList.entrySet()) {
    System.out.println(animeSet.getKey() + " " + animeSet.getValue());
}

// Iterate For-each
myAnimeList.forEach((key, value) -> System.out.println(key + " = " + value));

// Iterate with Iterator
final Iterator<Map.Entry<Integer, String>> it = myAnimeList.entrySet().iterator();
while (it.hasNext()) {
    Map.Entry<Integer, String> set = (Map.Entry<Integer, String>) it.next();
    System.out.println(set.getKey() + " = " + set.getValue());
}

// Iterate over Keys
for (Integer animeRank : myAnimeList.keySet()) {
    System.out.println(animeRank);
}

// Iterate over Values
for (String anime : myAnimeList.values()) {
    System.out.println(anime);
}

// Delete specific element
myAnimeList.remove(5);  // Remove by key

// Delete All
myAnimeList.clear();
```


## Classes
```Java

```


## Functions
```Java

```


## Instantiation and Intitialization
```Java

```


## Inheritance 
```Java

```


## Composition
```Java

```
