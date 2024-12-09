
Here is an [article](https://www.linkedin.com/pulse/%D6%85%D5%A2%D5%B5%D5%A5%D5%AF%D5%BF-%D5%AF%D5%B8%D5%B2%D5%B4%D5%B6%D5%B8%D6%80%D5%B8%D5%B7%D5%BE%D5%A1%D5%AE-%D5%AE%D6%80%D5%A1%D5%A3%D6%80%D5%A1%D5%BE%D5%B8%D6%80%D5%B8%D6%82%D5%B4-oop-hovhannes-khachatryan-jxnoe/) of [Hovhannes Khachatryan](https://www.linkedin.com/in/khachatryan-hovhannes?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3B31D%2BLLa2TCq9ljrEsWW7Xg%3D%3D) in Linkedin.


**Օբյեկտ-կողմնորոշված ծրագրավորումը** (**ՕԿԾ**, անգլերենում՝ **Object-oriented programming - OOP**) ծրագրավորման մոտեցում է, մեխանիզմ՝ որի հիմնական գաղափարներն են **class**-ը և **object**-ը։ Object-ը կարող ենք պատկերացնել որպես տվյալների ամբողջություն, իսկ class-ը որպես կաղապար object-ը ստեղծելու համար։ Որպես օրինակ ամբողջ հոդվածի համար ընտրել եմ խաղալիքի արտադրման գաղափարը, նյութը ավելի հասանելի դարձնելու համար։ Հոդվածում չեմ կենտրոնանում ծրագրավորման լեզուներին հատուկ կոդային, կամ գաղափարական հատկանիշների վրա, դրա փոխարեն շեշտը դնում եմ բուն OOP-ի գաղափարների հասանելի մատուցման վրա։

Պատկերացնենք, որ որոշել ենք խաղալիք պատրաստել և վաճառել։ Սկզբում որոշում ենք հատ-հատ պատրաստել դրա բոլոր դետալները, միացնել իրար, փաթեթավորել ու պատրաստել վաճառքի։ Մեր խաղալիքը կունենա հետևյալ հատկությունները․

```cpp
#include <string> // Include this to use std::string

const int toy_height = 150; // Integer constant
const int toy_width = 150;  // Integer constant
const std::string toy_color = "red"; // String constant
const std::string toy_description = "Red toy description"; 
// String constant

```

Մի տեսակ թափափված է, չէ՞։ Եթե փորձենք ինչ-որ պահի հետ գալ ու ավելացնել ինչ-որ հատկություն, պետք է ստեղծենք նոր փոփոխական, դրան վերագրենք արժեք․․․

Դե եկեք տեսնենք թե ինչպիսի կլինի մեր խաղալիքը, եթե այն ներկայացնենք object-ի տեսքով․

```cpp
#include <iostream>
#include <string>

class Toy {
public:
    // Properties
    int height;
    int width;
    std::string color;
    std::string description;

    // Constructor
    Toy(int h, int w, const std::string& c, const std::string& d)
        : height(h), width(w), color(c), description(d) {}

    // Method
    void sayHy() const {
        std::cout << "Hi, I am a toy car!" << std::endl;
    }
};

int main() {
    // Create an instance of the Toy class
    Toy toy(200, 200, "blue", "A small toy car");

    // Access properties
    std::cout << "Height: " << toy.height << std::endl;
    std::cout << "Width: " << toy.width << std::endl;
    std::cout << "Color: " << toy.color << std::endl;
    std::cout << "Description: " << toy.description << std::endl;

    // Call the method
    toy.sayHy();

    return 0;
}
```