# เนื้อหาค่าย 1 สอวน.คอมพิวเตอร์

ปล. นี่เป็นภาษา opal_Inwza007x ถ้าไม่เข้าใจ ก็ไปถาม [opal_Inwza007x](https://www.facebook.com/profile.php?id=100002974790342)

ปล2. ตัวฟ้าๆกดได้นะครับ เป็นเรื่องเพิ่มเติม

## เปิดมาหน้าแรก แต่ละอันเอาไว้ทำไร

```c++
1. #include <iostream>

2. using namespace std;

3. int main() {
4.     // process   
5.     return 0;
6. }
```
    
* บรรทัดที่ 1 เป็นการประกาศหัวเรื่องให้โปรแกรมรู้ ว่าเราจะใช้ฟังก์ชันในหัวเรื่องนี้นะ อารมณ์เหมือนโหลด mod เข้าเกมเลย

* บรรทัดที่ 2 เป็นการย่อโค้ดให้สั้นลง เช่น ถ้าไม่มีบรรทัดนี้เราจะต้องพิมพ์คำสั่ง `cin >> x;` เฉยๆ กลายเป็น `std::cin >> x;`

* บรรทัดที่ 3-6 เป็นฟังก์ชันที่ต้องมีทุกบ้าน ถ้าไม่มีจะ compile ไม่ติด ยกเว้นโจทย์แนว interactive ที่จะไม่มี main ก็ได้

* บรรทัดที่ 4 คือการคอมเม้นใน c++ โดยเราจะพิมอะไรหลัง // ก็ได้ 

* บรรทัดที่ 6 อันนี้ต้องอธิบายก่อนว่า ตัว compile จะอ่านโค้ดเราจากบนลงล่าง ถ้ามันเจออะไรแปลกๆมันจะบอกเราว่าตรงนี้ผิด ซึ่ง `return 0;` ที่เราเอาไว้ล่างสุดของการทำงาน จะทำให้ตัว compile รู้ว่าโปรแกรมนี้คืนค่า 0 ออกมา ซึ่งความหมายก็คือโค้ดนี้ไม่มีไรผิดพลาด แล้วเรายังสามารถใช้คำสั่งนี้ในการจบการทำงานโค้ดเราตอนไหนก็ได้ด้วย

## Variable

| ชื่อ | เอาไว้รับค่า | การนำไปใช้ | Bytes |
| :---: | :---: | :---: | :---: |
| int | -2,147,483,647 ถึง 2,147,483,647 | ไว้รับค่าตัวเลขเฉยๆตั้งแต่ -(2<sup>31</sup>-1) ถึง 2<sup>31</sup>-1 | 4 |
| signed int | 0 ถึง 4,294,967,295 | นิยมใช้ int มากกว่าอะ | 4 |
| long long | -9,223,372,036,854,775,807 ถึง 9,223,372,036,854,775,807 | ไว้รับค่าตัวเลขที่กว้างๆ ตั้งแต่ -(2<sup>63</sup>-1) ถึง 2<sup>63</sup>-1 | 8 |
| unsigned long long | 0 ถึง 18,446,744,073,709,551,615 | เอาไว้รับโจทย์ที่เลขมันมากๆๆ ถ้าอันนี้ยังรับค่าไม่ไหวก็หนีไปใช้ [bignum](https://www.geeksforgeeks.org/bigint-big-integers-in-c-with-example/) ซะ | 8 |
| float | 1.175E-38 ถึง 3.402E+38 | เอาไว้รับค่าเป็นทศนิยม | 4 |
| double | 2.225E-308 ถึง 1.797E+308 | ทศนิยมเหมือนกันแค่ดีกว่า | 8 |
| bool | true/false | เอาไว้เก็บค่าว่าจริงหรือเท็จ โดยถ้าให้ค่าเป็น 0 จะ false นอกนั้นถือว่า true หมด แม้แต่เลขติดลบ | 1 |
| char | เอาไว้เก็บตัวอักษรเป็น [ascii](https://th.wikipedia.org/wiki/%E0%B9%81%E0%B8%AD%E0%B8%AA%E0%B8%81%E0%B8%B5) | รับค่าตัวอักษรที่มีแค่ตัวเดียวแน่ๆ | 1 |
| string | เป็น char หลายตัวๆ เหมือนเป็น dynamic char [array](https://github.com/opalInwza007x/TEST#colorgreenarray) | รับค่าตัวอักษรที่มีหลายๆตัวได้ | 1 * (ขนาดของ string) |

ในการประกาศชื่อตัวแปรก็ทำแบบด้านล่างเลย ขอแค่ชื่อไม่ตรงกับ[ฟังก์ชัน](https://www.informit.com/articles/article.aspx?p=2755729&seqNum=7)ที่ที่เขามีให้ก็ตั้งได้แน่นอนครับ ไม่งั้นคุณอาจจะได้นั่งแก้โค้ดของคุณข้ามวัน >:3 

```c++
<ชนิดตัวแปร> ชื่อตัวแปร;
long long n;
bool amogus;
```
    
โดยเราสามารถกำหนดค่าของแต่ละตัวได้ด้วย โดยจะมีรูปแบบตามนี้เลย

```c++
int n = 96;
long long n2 = 696969;
float sum = 0.0;
double sum2 = 0.001;
bool flg = true;
char a = 'F'; // ในการเก็บ character ตัวเดียวจะใช้แบบนี้ 'x';
string s = "Bro_What??!!"; // ถ้าเก็บเป็นหลายตัวค่อยใช้ "xyz" ดู " กับ ' ดีๆด้วย!!!
```

ในเรื่องของ ' กับ " ก็ใช้เขียนได้แบบทั้งมีหลายตัวหรือตัวเดียวก็ได้นะครับ แต่จะใช้ ' กับตัวอักษรเดียวในกรณีต้องการใช้สมบัติของ [ascii](https://th.wikipedia.org/wiki/%E0%B9%81%E0%B8%AD%E0%B8%AA%E0%B8%81%E0%B8%B5) ซึ่งถ้าเซียนๆหน่อย แทบจะใช้อันนี้เป็นตัวเลขเลย

แล้วก็เราสามารถใช้ const <variable> <name> = <number>; เป็นการกำหนดให้ตัวแปรนั้นเป็นค่าคงที่ ผมชอบใช้นะดูเท่ดี

```c++
const int maxn = 69420;
// <int> is read/write while <const int> is read-only
```

ระวังอย่าไปเปลี่ยนค่ามันล่ะ ไม่งั้นระเบิดแน่!!!

## input/output

### cin

เป็นคำสั่งรับค่าเข้ามาง่ายๆครับ เป็นการรับค่าเข้ามาตรงๆเลย แต่อย่าลืมประกาศตัวแปรก่อนรับค่าล่ะ

```c++
long long n;
cin >> n;
string s;
cin >> s;
```

ถ้าต้องการรับค่าหลายตัวในบรรทัดเดียวก็ทำแบบนี้เลยครับ

```c++
long long n;
string s;
char amogus;
cin >> n >> s >> amogus;
```

### cout

เป็นคำสั่งพิมพ์ออกทางหน้าจอ หลังจากรับ input ทั้งหมดแล้ว โดยเราจะพิมพ์ข้อความจากตัวแปรหรือคำอะไรลงไปก็ได้

```c++
long long n;
cout << "please insert n : ";
cin >> n;
cout << "value of n = ";
cout << n;
```

ถ้าต้องการแสดงผลค่าหลายตัวในบรรทัดเดียวก็ทำแบบนี้เลยครับ

```c++
char a = 'a';
string s = "abc"
cout << a << " " << s;
```

โดยในภาษา c++ จะมีการพิมพ์แบบพิเศษเรียกว่า Escape Sequences

| Escape Sequences | ความหมาย |
| :---: | :---: |
| \n | ขึ้นบรรทัดใหม่ |
| endl | ขึ้นบรรทัดใหม่ แต่ช้ากว่ามากๆ social credit -999 |

หลักๆก็มีแค่นี้แหละครับที่ได้ใช้บ่อย แต่ไปหาดู[เพิ่มเติม](https://www.ibm.com/docs/en/i/7.3?topic=set-escape-sequences)ได้

ซึ่งเมื่อเรามีการใช้ \n ก็จะทำให้ปัดบรรทัดลงได้ตามเงื่อนไขโจทย์ส่วนใหญ่

```c++
string s = "amogus", s2 = "is", s3 = "sus";
cout << s << "\n" << s2 << "\n" << s3;
```

โดยถ้าเราต้องการแสดงค่าออกมาเป็นทศนิยมก็ใช้คำสั่ง

```c++
cout << fixed << setprecision(x); // โดย x คือจำนวนทศนิยมที่เราต้องการ เมื่อ x เป็นจำนวนเต็มที่มากกว่าเท่ากับ 0
```

### scanf

มาจาก `include <cstdio>` เป็นคำสั่งที่มาจากภาษา C ใช้รับค่าเข้ามาเหมือนกันแต่จะยากกว่า แลกมากับความเร็วนิดนึง โดยแต่ละตัวจะมี format specifiers หรือตัวระบุรูปแบบของแต่ละชนิดของตัวแปร 

| ชื่อ | format specifiers |
| :---: | :---: |
| int | %d |
| long long | %lld |
| unsigned long long | %llu |
| float | %f |
| double | %lf |
| bool | ไม่มีง่ะ |
| char | %c |
| string | %s (เนื่องจากในภาษา C ไม่มี string มาให้ เราจึงต้องตั้งเป็น char array แทน) |

ตัวอย่างการใช้งาน

```c++
long long n;
char amogus;
scanf("%lld %c", &n, &c); // อย่าลืม & ด้วย ไม่งั้นได้แก้ยาวแน่
```

โดย scanf สามารถรับค่ามาโดยตัดส่วนที่ไม่ต้องการได้ อย่างเช่น โจทย์ให้รับค่ามาเป็น xAyB เมื่อ x, y คือตัวเลขที่เราต้องการ เราสามารถรับค่าแบบนี้ได้

```c++
scanf("%lldA%lldB", &n, &n2);
```

### printf

มาจาก `include <cstdio>` เป็นคำสั่งมาจากภาษา C เหมือนกัน ก็แค่สะดวกกว่าในบางกรณี โดยเรายังคงใช้ format specifiers เหมือนเดิม

```c++
ll n = 20;
char a = 'z';
printf("%lld\n%c", n, c); // ส่วนอันนี้ไม่มี & อย่าไปงงในห้องสอบล่ะ
```

## Conditions and if Statements

ในภาษา c++ เนี่ยก็จะใช้ตรรกะเหมือนคณิตศาสตร์เลย โดยหลักๆมีดังนี้ (Colon : เป็นเครื่องหมายที่มีการใช้เฉพาะทาง มีความหมายว่า "ดังต่อไปนี้")

* a น้อยกว่า b :  ${\color{red}a < b}$
* a น้อยกว่าเท่ากับ b : ${\color{red}a <= b}$
* a มากกว่า b : ${\color{red}a > b}$
* a มากกว่าเท่ากับ b : ${\color{red}a >= b}$
* a เท่ากับ b : ${\color{red}a == b}$
* a ไม่เท่ากับ b : ${\color{red}a != b}$

ในภาษา c++ มีการเขียนคำสั่ง if ดังนี้

```c++
if (condition) { // if condition == true do this!!!
    // process
}
else if (condition) {
    // process
}
else {
    // process
}
```

* ${\color{red}if}$ ไว้อันแรกเลย ถ้าเกิด condtion เรา true จะทำ process ของย่อหน้า if เลย
* ${\color{red}else}$ ${\color{red}if}$ เอาไว้ใช้อันรองๆมา ถ้า condition ข้างบน false แล้วอันนี้ true จะทำ process ของย่อหน้า else if นั้นๆต่อเลย
* ${\color{red}else}$ เอาไว้ใส่อันท้ายสุด ถ้า condition ข้างบน false หมดเลย จะทำ process ของ else ต่อโดยไม่ลังเล

แล้วก็เรามีทริคพิเศษ ทำให้โค้ดเราสั้นลงมากเลยครับ

```c++
cout << (condition ? if_true_do_this : if_false_do_this);

// ย่อมาจาก

if (condition) {
    // if_true_do_this
}
else {
    // if_false_do_this
}
```

โดย variable ของ `if_true_do_this` กับ `if_false_do_this` ต้องเหมือนกัน เช่น

```c++
cout << (is_prime ? "Yes" : "No");

for (int i = 0; i < n; i++) {
    int sum[i] += (i == 0 ? 0 : sum[i - 1]); // Beware index out of bounds
}
```

## Math in C++

กำหนดให้ a, b คือ constant number

| เครื่องหมาย | ค่าที่ได้ |
| :---: | :---: |
| a + b | เอา a, b มาบวกกัน |
| a - b | เอา a, b มาลบกัน |
| a * b | เอา a, b มาคูณกัน |
| a / b | เอา a, b มาหารกัน |
| a % b | เศษเหลือจากการหาร a ด้วย b |
| aeb | a * $10^b$ |

จะมีฟังก์ชันช่วยที่ได้ใช้บ่อยๆตามนี้ โดยต้อง `#include <cmath>` หรือ `#include <bits/stdc++.h>` ก่อน

| ฟังก์ชัน | ค่าที่ได้ |
| :---: | :---: |
| abs(x) | ถ้า x < 0 ได้ค่า -x นอกนั้นได้ค่า x |
| sqrt(x) | ได้ค่า $\sqrt{x}$ |
| pow(x, y) | ได้ค่า $x^y$ |
| __gcd(x, y) | หรม.ของ x, y |

ตัวอย่างการใช้งาน

```c++
long long a = 6;
long long b = 9;
a = a + b; // สำหรับเด็กคณิตอาจจะเศร้าหน่อย แต่บรรทัดนี้หมายถึง เพิ่มค่า a ไปอีก b
a = a * 6; // อันนี้คือคูณค่า a ไปอีก 6
```

โดยมีการเขียนสั้นๆด้วย อย่างเช่น

```c++
long long a = 8;
long long b = 4;
a /= b; // ย่อมาจาก a = a / b
a -= 2; // ย่อมาจาก a = a - 2
    
// special cases ได้แค่ + กับ -

a++; // ย่อมาจาก a = a + 1
++a; // ย่อมาจาก a = a + 1
a--; // ย่อมาจาก a = a - 1
--a; // ย่อมาจาก a = a - 1
```

ถ้าถามว่า `a++`/`a--` กับ `++a`/`--a` ต่างกันตรงไหน ถ้าในการใช้งาน `++a`/`--a` คือ บวกค่า a ไป 1 ก่อนแล้วค่อยเอาไปใช้งาน ส่วน `a++`/`a--` คือ เอาไปใช้งานก่อนค่อยบวกค่า `a` เพิ่มอีก 1 ยกตัวอย่างเช่น

```c++
long long a = 1, b = 2;
long long x = 1, y = 2;

b += a++ + 2;
// ค่า a = 2, b = 5
   
y += ++x + 2;
// ค่า x = 2, b = 6
```

แล้วก็ ++a/--a เร็วกว่า a++/a-- นะ [ลองไปอ่านดูว่าทำไม](https://www.quora.com/Gurus-say-in-C-incrementing-with-I-is-faster-than-with-I-Is-it-true-How-could-you-explain-this)

## Loops

### for

ในภาษา c++ มีการเขียนคำสั่ง for แบบธรรมดาดังนี้

```c++
for (int i = 0; i < n; ++i) {
    // process
}
```

* `int i = 0` คือ กำหนดให้ i = 0
* `i < n` คือ ถ้า i < n จะทำงานไปเรื่อยๆ จนกว่า `!(i < n)` AKA. `i >= n`
* `i++` คือ ค่า i จะเพิ่มทีละหนึ่งเมื่อจบการทำงานใน process

ถ้าให้อ่านเป็นภาษาคนก็ ตั้งแต่ i = 0 จนกระทั่ง i น้อยกว่า n ค่า i จะเพิ่มขึ้นทีละ 1

<img src="https://github.com/opalInwza007x/OCOM-1/assets/114739286/b639880f-b177-4ed8-9a9b-2981562a35f2" width="385px" align="center">

โดย for loop สามารถทำแบบหลายๆชั้นได้ด้วย นิยมไล่เป็น i j k...

```c++
for (int i = 0; i < n; ++i) {
    for (int j = 0; j < m; ++j) {
        // process
    }
}
```

ถ้าให้อธิบายก็ กำหนดให้ $a_i$ เป็นการทำงานลำดับที่ i เมื่อค่าของ i = 1, 2, 3, ...n และให้ $b_j$ เป็นการทำงานลำดับที่ j เมื่อค่าของ j = 1, 2, 3, ...m โดย for แรกจะทำงานตั้งแต่ $a_1$ จนถึง $a_n$ (ทั้งหมด n ครั้ง) โดยในการทำงานแต่ละครั้งของ $a_i$ ก็จะทำงาน $b_1$ จนถึง $b_m$ (ทั้งหมด m ครั้ง) อารมณ์เหมือนเพิ่มมิติให้ภาพเลย

### while

ในภาษา c++ มีการเขียนคำสั่ง while แบบธรรมดาดังนี้

```c++
while (condition) {
    // process
}
```

หลักการง่ายๆก็ ถ้า condition == true ก็จะทำงานใน process จนกว่าจะ false ต่อมาคือตัวอย่างการใช้งาน

```c++
ll q;
cin >> q;
while (q--) {
    // process
}

// ย่อมาจาก

while (q != 0) {
    // process
    q = q - 1;
}
```

ในเคสนี้สมมติมาน่าจะง่ายกว่า ถ้าหลังจากการรับค่ามา แล้วได้ค่า q = 4 ในขณะที่ q ยังไม่ false (q != 0) ก็จะทำงานใน process แล้ว q = 3 เช็คอีกว่า false รึยัง ถ้ายัง q = 2 วนไปเรื่อยจนกระทั่ง q = 0 แล้วจบการวน 

โดยเราสามารถใช้ while รับค่าจนกว่าจะ End of File ได้ด้วย [ไปอ่านเลย](https://p0ndja.medium.com/otog-eof-end-of-file-8da9534d93a5)

### do...while

ในภาษา c++ มีการเขียนคำสั่ง while แบบธรรมดาดังนี้

```c++
do {
    // process
} while (condition);
```

ไม่ค่อยได้เห็นบ่อยครับ นิยมใช้กันแค่ตอนมี next_permutation กัน วิธีการใช้งานก็เหมือนอันบนๆเลย ถ้า condition == true ก็จะทำจนกว่าจะ false

## Time Complexity

<img src="https://github.com/opalInwza007x/TEST/assets/114739286/99bd4e6d-f1f8-4808-b533-e56aff5dc503" width="385px" align="center">

มีเว็บที่อธิบายแล้วผมชอบอยู่ ไปดูกันได้ครับ [เข้าใจ Big O Notation แบบไฟลุกตีนไหม้](https://rayriffy.com/blog/big-o-notation)

ว่างๆเดี๋ยวมาเขียน เข้าเกมแปป

## Data structure

### Array

Array เอาไว้ใช้ตอนที่โจทย์จะนำค่าที่รับมาหลายๆอันไปใช้ต่อ โดยมีการประกาศตัวแปรแบบนี้

```c++
<variable> <name>[max_index + 1];
// เช่น
long long arr[505];
```

โดยเราสามารถกำหนดค่าเองได้ตามนี้เลย

```c++
long long arr[5] = {2, 4, 3, 5, 7};

// หรือว่า
    
ll arr[5];
arr[0] = 2;
arr[1] = 4;
arr[2] = 3;
arr[3] = 5;
arr[4] = 7;
```

มาทำความรู้จักกับ index ดีกว่า ในทางคอมพิวเตอร์เนี่ยจะเริ่มที่ index 0, 1, 2, ... , n - 1 ถ้าอิงตามข้างบนค่าแต่ละตำแหน่งจะเป็นแบบนี้

| indexs | ค่าของ index | Array Members |
| :---: | :---: | :---: |
| 0 | 2 | arr[0] |
| 1 | 4 | arr[1] |
| 2 | 3 | arr[2] |
| 3 | 5 | arr[3] |
| 4 | 7 | arr[4] |

อย่างเช่นถ้าโจทย์อยากนำค่าไปเก็บไว้ใน array แล้วแสดง output ทั้งหมด

```c++
const long long maxn = 1e5 + 5; // แล้วแต่เรากำหนด จะเปลี่ยนแปลงตามโจทย์
    
long long arr[maxn];
long long n;
cin >> n; // ความยาว arr ที่โจทย์ให้มา

// ***case1***
for (int i = 0; i < n; i++) {
    ll x;
    cin >> x; // รับค่า
    arr[i] = x; // กำหนดค่า
}

// ***case2***
for (int i = 0; i < n; i++) {
    cin >> arr[i]; // รับค่าเหมือนกัน แต่สั้นกว่า
}

for (int i = 0; i < n; i++) {
    cout << arr[i] << " "; // แสดง output
}
```

โดยเราสามารถเพิ่มมิติให้ array เราได้ด้วย ตัวอย่าง

```c++
long long arr[5][5];
```

การกำหนดค่าก็จะดูน่าสนใจขึ้นหน่อย แต่ส่วนใหญ่ใช้รับค่ามากกว่า

```c++
long long arr[3][3] = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

ถ้าเราจะนำไปใช้จริงก็ใช้ for loop มาช่วยตามจำนวนมิติมันเลยครับ

```c++
const long long maxn = 1005;
    
long long arr[maxn][maxn];
long long row, col;
cin >> row >> col; // ความยาว arr ที่โจทย์ให้มา ในแบบ 2 มิติ ส่วนใหญ่จะให้มาเป็น row col

for (int i = 0; i < row; i++) {
    for (int j = 0; j < col; j++) {
        cin >> arr[i][j];
    }
}
```

__ข้อควรระวัง__ หากเราเผลอเอาค่า index ติดลบ เราจะได้ค่า alien มา

```c++
ll n = arr[-69];
// right now n = 👽;
```

บางทีเห็นมันได้ค่า 0 แต่ก็อย่าไว้ใจมันเกินไปครับ ผมติดบั๊กมาหลายวันเพราะมันเลย T^T แล้วก็การที่เราใช้ index เกินกว่าที่ประกาศไว้ AKA. index Out Of Bounds จะทำให้มันระเบิด เพราะฉะนั้น อย่าหาทำ!!!

แล้วก็อีกอย่างนึง ถ้าเราประกาศ array เป็น global แล้วไม่ได้กำหนดค่า เวลาเราเรียกค่า index มาจะได้ 0 แต่ถ้าประกาศไว้ในฟังก์ชันแล้วยังไม่ได้กำหนดค่า เวลาเราเอาออกมาใช้จะได้ออกมาเป็นค่า alien แทน

### Vector

มาจาก `include <vector>` vector ใช้เหมือนกับ array เลย นิยมใช้ตอนไม่สนใจค่า index ถ้าอธิบายสั้นๆเลย vector คือ dynamic array ใช้สะดวกกว่าแต่ว่าเปราะบางกว่ามาก ทำผิดนิดหน่อยก็ระเบิดละ โดยมีการประกาศตัวแปรดังนี้

```c++
vector<<variable>> <name>;
// เช่น
vector<long long> vec;
```

ส่วนการกำหนดค่าเองก็

```c++
vector<long long> vec = {1, 2, 3...}; // ได้เรื่อยๆ ไม่มีจำกัด

const long long maxn = 1e5;
vector<long long> vec(maxn, 0); // กำหนดให้ตั้งแต่ index ที่ 0 ถึง maxn - 1 เป็นค่า 0
```

ถามว่าถ้าเราทำอะไรสักอย่างกับ index ที่เราไม่ได้กำหนดค่าไว้ หรือ index ติดลบ จะเกิดอะไรขึ้น? ซึ่งแน่นอนว่า...ระเบิดครับ

โดยเราจะมีคำสั่งพิเศษมาใช้กับ vector ด้วย ซึ่งแน่นอนว่าต้องจำครับ โดยต่อจากนี้จะเริ่มมีการใช้ pointer ละ ซึ่งผมใช้ไม่เป็นลองไปหาดูได้ครับ

| Function | คำอธิบาย | Time Complexity |
| :---: | :---: | :---: |
| .push_back(x) | เป็นการใส่ค่า x เข้าไปใน vector ต่อกันไปเรื่อยๆ | O(1) |
| .size() | เราจะได้ค่าของจำนวนสมาชิกใน vector ในตอนนั้น | O(1) |
| .clear() | เคลียสมาชิกทั้งหมดใน vector | O(n) |
| .front() | เข้าถึงสมาชิกตัวหน้าสุดของ vector | O(1) |
| .back() | เข้าถึงสมาชิกตัวหลังสุดของ vector | O(1) |
| .empty() | จะได้ค่า 1 ถ้าไม่มีสมาชิกใดๆใน vector นอกนั้นได้ค่า 0 | O(1) |
| .pop_back() | ลบค่าตัวข้างหลังสุด | O(1) |
| .begin() | เข้าถึงสมาชิกตัวหน้าสุดของ vector แต่เป็น iterator | O(1) |
| .end() | เข้าถึงสมาชิกตัวหลังสุดของ vector แต่เป็น iterator | O(1) |
| .erase() | ลบค่าตรงที่ค่าในวงเล็บชี้อยู่ โดยค่าในวงเล็บต้องเป็น iterator | O(n) |

สำหรับผมที่ไม่ค่อยเก่งเรื่อง pointer ตัว iterator ก็คือค่าๆนึงที่การจะใช้มัน ต้องทำวิธีพิเศษให้ได้ค่าแบบปกติมา

โดยการใช้งานในการรับค่าของผมก็จะทำประมาณนี้ครับ

```c++
vector<long long> vec;
long long n;
cin >> n; // รับค่าเข้ามา n ตัว
for (int i = 0; i < n; i++) {
    long long x;
    cin >> x;
    vec.push_back(x);
}

// หรือแบบนี้

const long long maxn = 1e5 + 5; // ค่า n จากโจทย์ที่สูงสุด
    
vector<long long> vec(maxn); // เหมือนเป็นการประกาศ index สูงสุดที่เราจะใช้
long long n;
cin >> n;
for (int i = 0; i < n; i++) {
    cin >> vec[i];
}
```

 แต่ส่วนใหญ่ผมใช้แบบข้างบน ขี้เกียจไปดู maxn ของโจทย์555 ส่วนการปริ้นค่า

    vector<int>::iterator itr;
    for (itr = vec.begin(); itr != vec.end(); itr++) {
        cout << *itr << "  ";
    }

    // หรือว่า

    for (auto e : vec) {
        cout << e << " ";
    }

    // หรืออีกแบบ

    for (auto &e : vec) {
        cout << e << " ";
    }

* แบบแรกผมไม่เคยใช้เพราะมันยาวเกิน

* แบบที่สองผมใช้บ่อยเลย เพราะมันค่ด EZ

* แบบที่สามต่างจากแบบที่สองแค่ตรง & ในแบบนี้พิเศษตรงที่เราสามารถเปลี่ยนค่า vector จาก e ได้เลย แต่ถ้าเป็นแบบนั้นผมจะย้ายไปใช้ array แทนดีกว่า555

โดย string ค่อนข้างคล้ายกับ vector มากๆ พูดง่ายๆเลย string ก็คือ vector<char> แต่แค่ optimize กว่า

### Set

มาจาก `include <set>` Set ก็เป็น Data structure ที่มีประโยชน์อยู่ โดย Set มีคุณสมบัติคือ ไม่มีสมาชิกที่ซ้ำกัน และเรียงจากน้อยไปมาก โดยมีการประกาศตัวแปรดังนี้

    set<<variable>> <name>;
    // เช่น
    set<long long> st;

โดยเราจะมีคำสั่งพิเศษมาใช้กับ Set ด้วย แนะนำให้จำๆๆๆ โดย C คือค่า constant ที่เพิ่มมานิดหน่อย

| Function | คำอธิบาย | Time Complexity |
| :---: | :---: | :---: |
| .insert(x) | เป็นการใส่ค่า x เข้าไปใน set โดยตัว set จะเรียงให้เรียบร้อบ | O(log(n) + C) |
| .size() | เราจะได้ค่าของจำนวนสมาชิกใน set ในตอนนั้น | O(1) |
| .clear() | เคลียสมาชิกทั้งหมดใน set | O(n) |
| .empty() | จะได้ค่า 1 ถ้าไม่มีสมาชิกใดๆใน set นอกนั้นได้ค่า 0 | O(1) |
| .begin() | เข้าถึงสมาชิกตัวหน้าสุดของ set แต่เป็น iterator | O(1) |
| .erase(itr) | ลบค่าตรงที่ค่าในวงเล็บชี้อยู่ โดยค่าในวงเล็บต้องเป็น iterator | O(logn + C) |
| .find() | หาค่าใน set ว่าอยู่ตำแหน่งใด | O(log(n)) |

โดยเซตสามาถให้งานได้หลายสายตามนี้เลย ส่วนใหญ่เวลาใช้ set ก็เพราะอยากได้คุณสมบัตินี่ล่ะ

* mutiset สมาชิกสามารถซ้ำกันได้ และเรียงจากน้อยไปมาก
* unordered_set ไม่มีสมาชิกที่ซ้ำกัน และไม่ได้เรียงจากข้อมูลให้
* unordered_multiset สมาชิกสามารถซ้ำกันได้ และไม่ได้เรียงจากข้อมูลให้ (มีมาทำไม)
* set<variable, greater<variable>> อันนี้จะทำให้ set เรียงจากมากไปน้อย

ถ้าโจทย์อยากให้เรียงส่วนใหญ่จะไปใช้ priority queue มากกว่า แต่อันนั้นเนื้อหาค่าย 2 อะเนอะ แต่รู้ไว้ก็ดีครับ ของโกง

### Stack

<img src="https://github.com/opalInwza007x/TEST/assets/114739286/1c1c6d87-d834-4c59-abf4-776e18b9b13d" width="385px" align="center">

มาจาก `include <stack>` Stack ก็คล้ายๆ vector เลย แต่มีคุณสมบัติ __เข้าก่อนออกหลัง__ ให้นึกภาพว่าเรามีกล่องทรงกระบอกสูงๆ พอใส่ของเข้าไปแน่นๆ เวลาเราเอาออกมาอันแรกก็จะได้อันที่ใส่เข้าไปล่าสุดเสมอ โดยใช้งานได้ตามนี้

```c++
stack<int> stk;
for (int i = 0; i < 5; i++) {
    stk.push(i);
}
while (!stk.empty()) {
    cout << stk.top() << "\n";
    stk.pop();
}
```

โดยในโค้ดจะใส่ค่า 0 1 2 3 4 ตามลำดับ แต่เวลาปริ้นออกมาจะได้ 4 3 2 1 0 จะใช้ได้ดีกว่า vector ตรงที่ pop ประหยัดเวลากว่า erase มากกกกก

| Function | คำอธิบาย | Time Complexity |
| :---: | :---: | :---: |
| .push(x) | เป็นการใส่ค่า x เข้าไปใน stack | O(1) |
| .top() | เป็นการเรียกค่าที่อยู่บนสุดออกมาใช้ | O(1) |
| .pop() | ลบตัวที่อยู่ข้างบนสุด ก็คือตัวที่ใส่ไปล่าสุดนั่นเอง | O(1) |
| .size() | เราจะได้ค่าของจำนวนสมาชิกใน stack ในตอนนั้น | O(1) |
| .clear() | เคลียสมาชิกทั้งหมดใน stack | O(n) |
| .empty() | จะได้ค่า 1 ถ้าไม่มีสมาชิกใดๆใน stack นอกนั้นได้ค่า 0 | O(1) |

โดย recursive จะคิดเป็นแบบนี้แหละ แต่ผมถนัดดูเป็นแบบแตกเป็น Tree มากกว่า

### Queue

<img src="https://github.com/opalInwza007x/TEST/assets/114739286/7d62c549-bd34-4e48-8784-957c617409fe" width="385px" align="center"> 

มาจาก `include <queue>` Queue ก็คล้ายๆ vector เหมือนกัน แต่มีคุณสมบัติ __เข้าก่อนออกก่อน__ อันนี้ก็นึกภาพเราไปซื้อข้าวมันไก่ร้านรองสุดท้ายที่โรงเรียนสารคามพิทยาคม แล้วเจอแถวยาวๆ เวลาเราไปก็ต้องต่อที่ท้ายแถว คนที่อยู่ข้างหน้าสุดพอได้ข้าวแล้วก็จะได้ออกก่อน ส่วนเราก็รอจนกว่าจะถึงหน้าแถว ค่อยได้กินข้าวมันไก่สุดให้เยอะที่เหมือนกลัวไม่อิ่มยันพรุ่งนี้ โดยใช้งานได้ตามนี้

```c++
queue<int> qu;
for (int i = 0; i < 5; i++) {
    qu.push(i);
}
while (!qu.empty()) {
    cout << qu.front() << "\n";
    qu.pop();
}
```

โดยในโค้ดจะใส่ค่า 0 1 2 3 4 ตามลำดับ เวลาปริ้นออกมาจะได้ 0 1 2 3 4 เหมือนเดิม แล้วก็เหมือนเดิมครับ pop ของ queue เวลาดีกว่า erase มาก

| Function | คำอธิบาย | Time Complexity |
| :---: | :---: | :---: |
| .push(x) | เป็นการใส่ค่า x เข้าไปใน queue | O(1) |
| .front() | เป็นการเรียกค่าที่อยู่หน้าแถวออกมาใช้ | O(1) |
| .pop() | ลบตัวที่อยู่หน้าแถว | O(1) |
| .size() | เราจะได้ค่าของจำนวนสมาชิกใน queue ในตอนนั้น | O(1) |
| .clear() | เคลียสมาชิกทั้งหมดใน queue | O(n) |
| .empty() | จะได้ค่า 1 ถ้าไม่มีสมาชิกใดๆใน queue นอกนั้นได้ค่า 0 | O(1) |

## Function and Recursive Function

### Function

ฟังก์ชันจะทำให้โค้ดเราเขียนสั้นแล้วก็มีระเบียบมากขึ้น โดยส่วนใหญ่จะเขียนไว้ข้างบน main เลย ในภาษา c++ เราก็จะมีการสร้างฟังก์ชันง่ายๆโดยแบ่งตามฉบับผมได้ 2 แบบ

```c++
void <function_name>() {
    // process;
}

// เช่น

void solve() {
    // process;
}
```

หรืออีกแบบนึง

```c++
<variable> <function_name>() {
    // process
    return solution;
}

// เช่น

int find_segment3() {
    // process
    return 0;
}

string get_abc() {
    return "abc";
}
```

โดยใน () เราจะใช้รับค่า ตามที่เราจะส่งขึ้นไปได้เลยแต่ห้ามขาดห้ามเกิน

* แบบที่ 1 void เป็นฟังก์ชันเราไม่ต้องการค่ากลับมา ไม่เปลือง memory ใช้ดีครับเยี่ยมๆ

* แบบที่ 2 เป็น variable ไรก็ได้ โดยเราจะตั้งตามค่าที่เราอยากได้ตอน return กลับ

### Recursive Function

เป็นฟังก์ชันที่เรียกใช้ฟังก์ชันตัวมันเอง ใช้เอามาลองทุกวิธีที่เป็นไปได้ ที่นิยมนำมาอธิบายที่สุดเลยก็ Fibonacci Number ซึ่ง fibo คือเลขที่เอาสองตัวก่อนหน้านั้นบวกกันต่อกันไปเรื่อยๆ มี Base Case คือ 0 และ 1 
โดยลำดับเริ่มที่ 0 เป็น 0 1 1 2 3 5 8 13 21 34... 

<img src="https://github.com/opalInwza007x/TEST/assets/114739286/0b3a0627-75dd-46a1-9094-cf0c9c1f0a7b" width="385px" align="center">

```c++
    long long fibo(long long n) {
        if (n == 0) {
            return 0;
        }
        if (n == 1) {
            return 1;
        }
        ll path1 = fibo(n - 2);
        ll path2 = fibo(n - 1);
        return path1 + path2;
    }
```

การทำงานของโค้ดเราดูได้ตามภาพเลยครับ ในโค้ดนี้จะใต่ซ้ายเรื่อยๆจนกว่าจะเจอ Base Case เลย แล้วค่อยไต่ขวาอันล่าสุดหลังจากซ้ายตัน เป็นแนวคิดแบบ stack ลองเอาไปคิดดูครับ

https://www.youtube.com/watch?v=P8Xa2BitN3I อันนี้อธิบายดีอยู่ครับ ปูทางไป Dynamic programming ด้วย ซึ่งก็คือถ้า format recursive เราถูก แค่ใส่ memorization ก็ไวขึ้นละ แล้วเราก็จะเรียกมันว่า Top-Down Approach

## Tips from opal_Inwza007x

ต่อจากนี้คือ คำแนะนำหรือฟังก์ชันโกงๆ พวกนี้จำเอาไว้ก็ดีครับ

### Basic setup

```c++
#include <bits/stdc++.h>

using namespace std;

typedef long long ll;

int main() {
    ios_base::sync_with_stdio(0);
    cin.tie(0);

    return 0;
}
```

* ตรง include ถ้า memory ไม่เกินก็ยัด `#include<bits/stdc++.h>` ให้เลยก็ดีครับ สะดวกดี
* `typedef long long ll` ก็เอามาใช้แทน int เลยก็ได้ครับ ได้ดักไว้ตอนเขาให้ค่ามามากกว่า INT_MAX ด้วย ถ้าความจำเกินอาจจะเป็นที่ Algorithm เรา หรือไม่ก็ลองเปลี่ยนเป็น typedef int ll ดูก็ได้ครับ แต่ส่วนใหญ่จะผิดที่ Algorithm
* ตรง `ios_base -> cin.tie(0)` เป็นการทำให้เรา cout ไวขึ้น __คำเตือน__ จากท่านปาล์มปาล์มปาล์ม ไม่ควรใช้กับ printf scanf ไม่งั้นจะระเบิด(เพิ่มเติม scanf/printf จะดีกว่าสำหรับโจทย์ที่รับค่าเยอะๆ ส่วน ios_base + cin/cout จะดีกว่าสำหรับโจทย์ที่ปริ้นค่าเยอะๆ)


### string input

<img src="https://github.com/opalInwza007x/OCOM-1/assets/114739286/d4f87683-16f1-4dde-91b7-99d8265ce350" width="385px" align="center">

สำหรับการรับค่าแบบนี้ หลายคนอาจจะทำแบบ

```c++
ll row, col;
cin >> row >> col;
char arr[row + 5][col + 5];
for (int i = 0; i < row; i++) {
    for (int j = 0; j < col; j++) {
        cin >> arr[i][j];
    }
}
```

ซึ่งโค้ดก็ทำงานได้ปกติครับ แต่ว่าถ้ามี row, col เยอะมากๆจะทำให้ได้ Time Limit Exceed กลับบ้านไปแก้ แนะนำให้รับมาเป็น string ดีกว่าครับ

```c++
for (int i = 0; i < row; i++) {
    string s;
    cin >> s;
    for (int j = 0; j < col; j++) {
        arr[i][j] = s[j];
    }
}
```

### function โกงๆ

ต่อจากนี้ถ้าทุกคน `include <bits/stdc++.h>` ไว้แล้วก็ไม่ต้องสนใจ `include` อื่นก็ได้ครับ

${\color{green}min}$

__(Time Complexity O(1) and Space O(1))__

มาจาก `include <algorithm>` เอาไว้เทียบค่าว่าใน min ว่าตัวไหนมีค่าน้อยกว่า โดย __ค่าที่เทียบต้องเป็น variable เดียวกัน__ ถ้าเขียนสดก็ประมาณนี้

```c++
ll min(ll x, ll y) {
    return x < y ? x : y;
}
```

ส่วนใน c++ เราก็ใช้ได้เลย เขามีไว้ให้

```c++
    ll a = 1, b = 5, c = 4;
    cout << min(a, min(b, c)) << "\n"; // ส่วนตัวชอบแบบนี้
    cout << min({a, b, c}) << "\n";
```

${\color{green}max}$

__(Time Complexity O(1) and Space O(1))__

มาจาก `include <algorithm>` เอาไว้เทียบค่าว่าใน max ว่าตัวไหนมีค่ามากกว่า โดย __ค่าที่เทียบต้องเป็น variable เดียวกัน__ ถ้าเขียนสดก็ประมาณนี้

```c++
ll max(ll x, ll y) {
    return x > y ? x : y;
}
```

อันนี้เหมือนกันครับ c++ เขามีไว้ให้ ไม่ต้องเขียนเอง

```c++
    ll a = 1, b = 5, c = 4;
    cout << max(a, max(b, c)) << "\n"; // ส่วนตัวชอบแบบนี้
    cout << max({a, b, c}) << "\n";
```

${\color{green}sort}$

__(Time Complexity O(1) and Space O(1))__

มาจาก `include <algorithm>` เอาไว้ใช้เรียงค่าได้เลย ไม่ต้องเสียเวลาไปเขียนพวก Heap sort หรือ Merge sort บลาๆๆเอง ตัวอย่างการใช้งาน

```c++
    vector<ll> vec = {-69, 1, 2, -1, 420};
    sort(vec.begin(), vec.end()); // น้อยไปมาก

    int arr[3] = {-69, 1, 420};
    sort(arr, arr + 3, greater<int>()); // มากไปน้อย
```

ถ้าเรียงตัวอักษรก็จะเรียงตาม ascii เลย แล้วก็เราสามารถ custom การ sort ได้ด้วย แต่ส่วนใหญ่เอาได้ใช้กับ pair ไว้เจอกันในค่าย 2 ละกัน

${\color{green}gcd}$

__(Time Complexity O(log(min(a, b))) and Space O(log(min(a, b)))__

[เขียนสดๆได้ตามนี้](https://www.geeksforgeeks.org/euclidean-algorithms-basic-and-extended/)

มาจาก `include <algorithm>` เอาไว้หาค่า GCD หรือ greatest common divisor หรือ ห.ร.ม. หรือ หารร่วมมาม นั่นเอง ตัวอย่างการใช้งาน

```c++
    vector<ll> vec = {5, 15, 30};
    ll gcd = 0;
    for (int i = 0; i < vec.size(); i++) {
        gcd = __gcd(gcd, vec[i]);
    }
    cout << gcd;
```

แล้วก็ LCM หรือ least common multiple หรือ ค.ร.น. หรือ คูณร่วมน้อยเราก็หาได้จากสมการนี้เลย

    GCD(x, y) * LCM(x, y) = x * y
                LCM(x, y) = x * y / GCD(x, y);



__(Time Complexity O(log(n)) and Space O(1))__

มาจาก `include <algorithm>` เป็นฟังก์ชันที่คืนค่า 0 กับ 1 ถ้าเรา binary search เจอค่านั้น ก็จะได้ 1 นอกนั้น 0

```c++
vector<ll> vec = {6, 7, 9, 11, 13, 15, 19}; // need to be sorted

if (binary_search(vec.begin(), vec.end(), 7)) { // true
    // process
}

if (binary_search(vec.begin(), vec.end(), 17)) { // false
    // process
}
```

ถึงเขาจะมีฟังก์ชันให้แต่เราก็ควรที่จะเขียนเองเป็นครับ พอเอาไปประยุกต์ได้แล้วมีประโยชน์มากๆ 

${\color{green}lower_bound }$ ${\color{green}and }$ ${\color{green}upper_bound}$

__(Time Complexity O(log(n)) and Space O(1))__

มาจาก `include <algorithm>` เหมือนอันข้างบนเลยครับ แต่จะได้ค่าตำแหน่งที่เป็น iterator แทน ยังไม่อธิบายละกันครับ ไว้เจอกันค่าย 2

```c++
vector<ll> vec = {6, 7, 9, 11, 13, 15, 19}; // need to be sorted

vector<ll>::iterator itr = lower_bound(vec.begin(), vec.end(), 9);
cout << *itr << "\n";

ll pos = lower_bound(vec.begin(), vec.end(), 17) - vec.begin();
cout << pos << "\n";
```

ก็เหมือนเดิมครับควรที่จะเขียนเองเป็นครับ

${\color{green}fill }$ ${\color{green}and }$ ${\color{green}fill_n}$

fill ค่าเป็น 0 วู้วววว เดี่๋ยวมาเขียนนอนแปป

## Algorithms

ต่อจากนี้คือ Algorithm ที่พบเจอได้บ่อยในค่าย 1 รู้ไว้ก็ดีเหมือนกันครับ :)

### Binary Search

คลิปที่อธิบายดีมากๆ https://www.youtube.com/watch?v=MFhxShGxHWc

Binary Search คือการหาค่าที่เราต้องการรู้ภายใน O(log(n)) โดยใช้หลักการ divide-and-conquer แล้วก็มีเงื่อนไขคือ array ที่เราจะ search ต้อง sort มาก่อน 
โดย Algorithm นี้จะหาค่าตรงกลาง แล้วเอาไปเปรีบยเทียบกับค่าที่เราต้องการหา แล้วจะแบ่งครึ่งไปเรื่อยๆ ลองดูตัวอย่างน่าจะเข้าใจกว่า 

โดยในชีวิตประจำวันเราก็ใช้ Binary Search บ่อยอยู่นะครับ เช่นการที่คุณต้องอ่านหนังสือชีวะก่อนสอบที่มี 1000 หน้า ถ้าหน้าที่ต้องอ่านคือหน้า 2-3 ก็ไม่เป็นไรหรอกครับ เปิดไปทีละหน้าก็ได้ แต่ถ้าต้องการเปิดไปหน้า 420 ล่ะครับ? แน่นอนว่าคนส่วนใหญ่จะเลือกเปิดไปกลางๆเล่มแล้วเช็คว่าหน้าที่เราต้องการมากหรือน้อยกว่าหน้าที่เราเปิดเจอ สมมติให้ตอนนี้เปิดหน้า 500 ละกัน เราก็จะรู้ว่าควรจะเปิดไปหน้าซ้ายๆต่อ แล้วหน้าขวาที่มีอีก 500 แผ่นก็จะไม่ถูก search เลย ลดไปได้ตั้งครึ่งนึง ทำแบบนี้ไปเรื่อยๆจนเจอหน้าที่เราต้องการ

__ตัวอย่างโจทย์ใน OTOG__

[ไบนารีเสิร์ช](https://api.otog.cf/problem/doc/285)

กำหนดให้แถวลำดับ (array) ของตัวเลขจำนวนเต็มบวกที่แตกต่างกัน N ตัว หน้าที่ของคุณคือ รับคำสั่ง
จำนวน M คำสั่ง แต่ละคำสั่งจะกำหนดจำนวนเต็ม $x_i$ มาให้โปรแกรมของคุณต้องหาสมาชิกในแถว
ลำดับที่มีค่ามากที่สุดที่ไม่เกินค่าของ $x_i$ แต่หากหาไม่ได้แล้วไซร้ก็ให้ตอบว่า -1 แทน

__Method 1 Linear Search__

ข้อนี้ถ้าเราเทียบค่าไปทีละตัว ลองคิดถึงเคสที่ที่ต้อง search แล้วค่าที่ต้องการอยู่อันท้ายๆทุกอันดูครับ ถ้าเขาดักไว้แบบนั้นทุก M คำถาม Time Complexity เราจะกลายเป็น O(NM) เลย ซึ่งค่อนข้างแย่เลย 

__Method 2 Binary Search__

ถ้าหากเรา sort array แล้ว binary search m ครั้งแทน Time Complexity จะกลายเป็น sort + ฺBinary_search m ครั้ง = O(nlog(n) + mlog(n)) ดีขึ้นเยอะครับ 
โดยถ้าค่าที่จะ search น้อยกว่าค่าที่น้อยที่สุดใน array เราจะตอบ -1 นอกนั้นเราก็ตอบค่าที่เรา search ได้เลย

สามารถสรุปเป็นโค้ดดังนี้

```c++
#include <bits/stdc++.h>
    
using namespace std;
    
typedef long long ll;
    
int main(){
    ios_base::sync_with_stdio(0);
    cin.tie(0);
    
    ll n, m;
    cin >> n >> m;
    for (int i = 0; i < n; i++) {
        ll x;
        cin >> x;
        vec.push_back(x);
    }
    sort(vec.begin(),vec.end());
    for (int i = 0; i < m; i++) {
        ll x;
        cin >> x;
        if (x < vec[0]) {
            cout << -1 << "\n";
            continue;
        }
        ll l = 0, r = vec.size() - 1;
        while (l < r) {
            ll mid = l + (r - l) / 2;
            if (x >= vec[mid]) {
                l = mid + 1;
            }
            else {
               	r = mid;
            }
        }
        cout << vec[l - 1] << "\n";
    }
    return 0;
}
```

### Range Sum Query // Quick Sum

<img src="https://github.com/opalInwza007x/TEST/assets/114739286/fa8860c2-849a-4238-b56a-a930a353e296" width="385px" align="center">

โจทย์แนวนี้จะเกี่ยวกับการที่เราจะถามการบวกตั้งแต่ช่วง [l, r] ถาม Q ครั้ง ใน array ขนาด N

__ตัวอย่างโจทย์ใน OTOG__

[Problem G Range Sum Query](https://api.otog.cf/problem/doc/154)

Given a list L containing n integers, find the Range Sum Query (RSQ) between index i and j,
inclusive, i.e. RSQ(i, j) = L[i] + L[i+1] + L[i+2] + ... + L[j]. 

__Method 1 Brute-Force__

ถ้าเราบวกไปแบบปกติเนี่ย เขาสามารถดักมาแบบทุกคำถาม ถามถึงช่วง 0 ถึงใกล้ๆ N ตลอด จะทำให้ Time Complexity เป็น O(NQ)

__Method 2 Quick Sum__

เราจะตั้ง array ให้ชื่อเป็น rsq ละกัน แล้วกำหนดค่าตำแหน่งที่ i คือ 

$$\left( \sum_{k=1}^i arr[k] \right)$$ 

คราวนี้พอโจทย์ถามหาผลบวกช่วง [l, r] เราก็สามารถตอบได้จาก rsq[r + 1] - rsq[l] โดยมีการ Precompute เป็น O(n) และพอถาม Q ครั้ง ก็ตอบได้ใน O(1) ทำให้ Time Complexity เหลือแค่ O(N + Q) นั่นเองเองเองเอง แต่ผมชอบเริ่มที่ index 0 มากกว่าเลยยุ่งยากหน่อย555

```c++
#include <bits/stdc++.h>

using namespace std;

typedef long long ll;

const ll maxn = 1e5 + 5;

ll rsq[maxn];

int main() {
    ios_base::sync_with_stdio(0);
    cin.tie(0);

    ll t;
    cin >> t;
    for (int i = 0; i < t; i++) {
        ll n, q;
        cin >> n >> q;
        for (int j = 0; j < n; j++) {
            cin >> rsq[j];
            rsq[j] += (j == 0 ? 0 : rsq[j - 1]);
        }
        for (int j = 0; j < q; j++) {
            ll a, b;
            cin >> a >> b;
            cout << rsq[b] - (a == 0 ? 0 : a - 1) << "\n";
        }
    }
    return 0;
}
```

### Maximum Contiguous Array Sum // Kadane's algorithm

ภาษาไทยก็คือ ผลบวกที่มากสุดของตัวเลขที่มีตำแหน่งต่อเนื่องกัน โจทย์จะให้ array ขนาด N มาตัวนึง เช่น

```c++
int arr[7] = {1, 2, 5, -3, -8, 2, -6};
```

Maximum Contiguous Array Sum ก็คือ arr[0] + arr[1] + arr[2] = 1 + 2 + 5 = 8 โดยเราจะไปเอา 2 ที่ index 5 ไม่ได้เพราะมันไม่ต่อเนื่อง 

__Method 1 Brute-Force__

เราก็เช็คไปทุกช่วงเลย

```c++
[l, r] = index[l] + index[l + 1] + ...index[r]

[0, 0] = index[0]
[0, 1] = index[0] + index[1]
.
.
.
[0, 6] = index[0] + index[1] + ...index[6]

[1, 1] = index[1]
[1, 2] = index[1] + index[2]
.
.
.
[1, 6] = index[1] + index[2] + ...index[6]

.
.
.

เรื่อยๆจนถึง [6, 6]
```

เราก็จะใช้เวลาวนหาคำตอบ O($N^2$) แล้วก็ในนั้นหาผลบวกอีก O(N) ทำให้ Time Complexity เป็น O($N^3$)

__Method 2 Brute-Force + Quick Sum__

จาก Algorithm ข้างบนเรานำมาหาผลบวกล่วงหน้าได้ ทำให้ Time Complexity เหลือแค่ O($N^2$)

__Method 3 Kadane's algorithm__

[แปะไว้เผื่อใครอ่านของผมไม่รู้เรื่อง](https://leetcode.com/problems/maximum-subarray/solutions/1595097/java-kadane-s-algorithm-explanation-using-image/)

เราสามารถลดให้เหลือแค่ O(N) ได้โดยใช้ Algorithm นี้เลยครับ

```c++
int maxSubArray(vector<int>& nums) {
    int best = -1e9, most = -1e9;
    for (auto e : nums) {
        most = max(e, e + most);
        best = max(best, most);
    }
    cout << best;
}
```

ลองทดใส่กระดาษดูก็ได้นะครับ เพราะผมก็อธิบายไม่ค่อยถูก ผมจำเอาไปใช้เลยสั้นดี555

__special thanks : krist7599555__
