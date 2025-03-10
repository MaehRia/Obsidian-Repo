
Վիրտուալ ֆունկցիաները կամ վիրտուալ մեթոդները  ՕԿԾ-ի կարևորագույն տարրերից է, քանի որ օգնում է իրականացնել պոլիմորֆիզմ, որի մասին մանրամասն կնկարագրվի ստորև։

### Պոլիմորֆիզմ 

C++ ծրագրավորման լեզվում պոլիմորֆիզմի մեխանիզմը թույլ է տալիս, որ որոշակի ֆունկցիա իրեն դրսևորում է տարբեր ձևով կախված նրանից, թե որ օբյեկտ է հանդիսանում կանչող։ Ինքնին ․․․ ունի հունարեն ծագում և նշանակում է <<ունենալ տարբեր ֆորմաներ>>։ Դա տեղի ունենում այն դեպքում, երբ ունենք դասերի հիերարքիա, կապված ժառանգականությամբ։

Օրինակ՝ ունենք ֆունկցիա makeSound()։ երբ կատուն է կանչում ֆունկցիան այն կարտաբերի "meow", իսկ երբ կովը՝ "moow"․

![[Pasted image 20241218004958.png]]

Որպես արդյունք ֆունկցիան իրեն դրսևորեց տարբեր ձևերով, այսինք մենք դիտարկեցինք պոլիմորֆիզմի գաղափարի պարզագույն նկարագրության օրինակ։

### Պոլիմորֆիզմի տեսակները

![[Pasted image 20241218005350.png|550]]

Առանձնացվում է 2 հիմնականում ճյուղավորում․
1. Կոմպիլյացիայի ժամանակի պոլիմորֆիզմ
2. Կատարման ժամանակի պոլիմորֆիզմ

### Compile Time polymorphism

Գերբեռնված ֆունկցիաները տարբերվում են սովորական ֆունկցիաներից նրանով, որ համադրում են մի քանի արգումենտների քանակը և տեսակը։ Տեղեկատվությունը առկա է կոմպիլյացիայի ժամանակ։ Սա նշանակում է, որ C++ կոմպիլյատորը ճիշտ ֆունկցիան կընտրի կոմպիլյացիայի ընթացքում։

Կոմպիլյացիայի ժամանակի պոլիմորֆիզմը ձեռք է բերվում ֆունկցիաների գերբեռնման կամ օպերատորների գերբեռնման միջոցով։

### 1. Method Overloading (function overloading)

Մեթոդի կամ ֆունկցիայի գերբեռնումը տեղի է ունենում այն դեպքերում, երբ ունենք նույն անունով,բայց տարբեր արգումենտներով մի քանի ֆունկցիաներ։ Տարբեր արգումենտներ ասելով, ենթադրվում է, որ արգումենտները տարբեր տիպեր ունեն, ինչպես բերված է հաջորդ օրինակում։

```cpp
#include <iostream> 
using namespace std;

void test(int i) {
	cout << " The int is " << i << endl;
}
void test(float  f) {
	cout << " The float is " << f << endl;
}
void test(char const *ch) {
	cout << " The char* is " << ch << endl;
}

int main() {
	test(5);
	test(5.5);
	test("five");
	return 0;
}
```

Output:
![[Pasted image 20241218152533.png|300]]

### 2. Operator Overloading

Օպերատորների բեռնումը թույլ է տալիս փոխել C++-ում օպերատորների ստանդարտ պահվածքը և դրանց գործառույթները՝ օգտագործելով օգտատերերի դաշտեր։ Սա նշանակում է, որ մենք կարող ենք սահմանել, թե ինչպես պետք է աշխատեն օպերատորները, օրինակ՝ `+`, `-`, `*` և այլերը՝ մեր ստեղծած դասերի օբյեկտների հետ։

Օրինակ՝ + օպերատորի բեռնումը՝ տողերը միացնելու համար։

Ամենայն դեպքո, + օպերատորը սովորաբար օգտագործվում է թվերի գումարման համար։ Սակայն մենք կարող ենք բեռնել այդ օպերատորը՝ օգտագործելու համար տողերի միացման համար։

Օպերատորի բեռնումից հետո, եթե այն կիրառվում է թվերի վրա, այն կգումարի դրանք, իսկ եթե կիրառվում է տողերի վրա՝ կհամակցի դրանք։

```cpp
#include <iostream>
#include <string>
using namespace std;

class MyString {
private:
    string value;
public:
    MyString(string val) : value(val) {}

    // Օպերատոր + բեռնում՝ տողերը միացնելու համար
    MyString operator + (const MyString& other) {
        return MyString(value + other.value);  // տողերը միացնում ենք
    }

    void print() {
        cout << value << endl;
    }
};

int main() {
    MyString str1("Hello, ");
    MyString str2("World!");
    
    MyString result = str1 + str2;  // տողերի միացում՝ օգտագործելով բեռնված օպերատոր +
    result.print();  // Արդյունք՝ "Hello, World!"
    
    return 0;
}

```

Output: 
![[Pasted image 20241221183628.png]]


#### Օպերատորի բեռնում թվերի համար:

Օպերատորի բեռնումը կարող է օգտագործվել նաև այլ տվյալների տեսակների համար, օրինակ՝ թվերի։

```cpp
#include <iostream>
using namespace std;

class ComplexNum {
private:
    int real, imag;
public:
    ComplexNum(int r, int i) : real(r), imag(i) {}

    // Օպերատոր + բեռնում՝ համալիրված թվերի գումարման համար
    ComplexNum operator + (const ComplexNum& other) {
        return ComplexNum(real + other.real, imag + other.imag);
    }

    void print() {
        cout << real << " + " << imag << "i" << endl;
    }
};

int main() {
    ComplexNum num1(2, 3);
    ComplexNum num2(4, 5);
    ComplexNum result = num1 + num2;  // Համալիրված թվերի գումարում
    result.print();  // Արդյունք՝ "6 + 8i"
    
    return 0;
}

```

### Կատարման ժամանակի պոլիմորֆիզմ

Սա տեղի է ունենում, երբ օբյեկտի մեթոդը կանչվում է ծրագրի կատարման ժամանակ, այլ ոչ թե կոմպիլյացիայի ժամանակ։ Կատարման ժամանակի պոլիմորֆիզմը իրականացվում է ֆունկցիաների վերասահմանման միջոցով։ Կանչվող ֆունկցիան որոշվում է ծրագրի կատարման ընթացքում։

1. Ֆունկցիայի վերասահմանում

```cpp
#include <iostream>
using namespace std;

class Animal {

public:
    void speak() {
        cout << "Animals make sounds..." << endl;
    }
};

class Dog : public Animal {

public:
    void speak() {
        cout << "Dogs bark..." << endl;
    }
};

int main() {
    Dog myDog;

    myDog.speak();  // Կանչում ենք Dog դասի speak() ֆունկցիան։

    return 0;
}

```


2. Վիրտուալ ֆունկցիա

Վիրտուալ ֆունկցիան C++-ում կատարման ժամանակի պոլիմորֆիզմի իրականացման ևս մեկ մեխանիզմ է։ Այն հատուկ ֆունկցիա է, որը սահմանվում է բազային դասում և վերասահմանվում է ժառանգորդ դասում։ Վիրտուալ ֆունկցիա հայտարարելու համար պետք է օգտագործել **`virtual`** բանալին։ Այս բանալին պետք է նախորդի բազային դասի ֆունկցիայի հայտարարությանը։

Երբ վիրտուալ ֆունկցիան ժառանգվում է, ժառանգորդ դասը կարող է վերասահմանել այն՝ ըստ իր պահանջների։

```cpp
#include <iostream>
using namespace std;

// Ծնող դաս
class Animal {
public:
    virtual void speak() {
        cout << "Animals make sounds." << endl;
    }
};

// Ժառանգորդ դաս 1
class Dog : public Animal {
public:
    void speak() override {
        cout << "Dogs bark." << endl;
    }
};

// Ժառանգորդ դաս 2
class Cat : public Animal {
public:
    void speak() override {
        cout << "Cats meow." << endl;
    }
};

int main() {
    Animal* animal;  // Բազային դասի ցուցիչ

    Dog dog;
    Cat cat;

    animal = &dog;  // Ցուցիչը ուղղում ենք Dog օբյեկտին
    animal->speak();  // Կանչում է Dog դասի speak()

    animal = &cat;  // Ցուցիչը ուղղում ենք Cat օբյեկտին
    animal->speak();  // Կանչում է Cat դասի speak()

    return 0;
}

```