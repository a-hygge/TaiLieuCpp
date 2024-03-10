**C++ Buổi 4**

<a name="_heading=h.gjdgxs"></a>[I. Khái niệm hướng đối tượng (OOP)	1](#_heading=h.30j0zll)

[1, Khái niệm :	1](#_heading=h.1fob9te)

[2, Lợi ích của Lập trình hướng đối tượng là gì?	1](#_heading=h.3znysh7)

[3,Các khái niệm cơ bản	2](#_heading=h.2et92p0)

[a) Đối tượng( Object )	2](#_heading=h.tyjcwt)

[b) Lớp học( Class )	2](#_heading=h.3dy6vkm)

[Access modifier trong C++	3](#_heading=h.1t3h5sf)

[Constructor	7](#_heading=h.4d34og8)

[Destructor	9](#_heading=h.2s8eyo1)

[II. Các tính chất của OOP	12](#_heading=h.17dp8vu)

[1.Tính đóng gói (Encapsulation):	12](#_heading=h.3rdcrjn)

[2.Tính kế thừa (Inheritance):	13](#_heading=h.26in1rg)

[3.Tính trừu tượng(Abstraction):	15](#_heading=h.lnxbz9)

[4.Tính đa hình (Polymorphism ):	18](#_heading=h.35nkun2)

[Dạng 1 – Compile time Polymorphism:	18](#_heading=h.1ksv4uv)

[Dạng 2 – Runtime Polymorphism:	18](#_heading=h.44sinio)

<a name="_heading=h.30j0zll"></a>**I. Khái niệm hướng đối tượng (OOP)**

<a name="_heading=h.1fob9te"></a>**1, Khái niệm :**

**Lập trình hướng đối tượng** là một phương pháp hoặc mô hình để thiết kế một chương trình sử dụng classes và objects. 

Lập trình thủ tục là về các hàm (thủ tục, hàm con, thuật toán) thực hiện các thao tác trên các biến (thuộc tính). Trong khi OOP nói về các đối tượng có lớp xác định chứa cả thuộc tính và chức năng. OOP là một cách hiện đại để sử dụng cả biến và hàm một cách an toàn.

<a name="_heading=h.3znysh7"></a>**2, Lợi ích của Lập trình hướng đối tượng là gì?**

- Nhanh hơn và dễ thực hiện hơn.
- Cung cấp một cấu trúc rõ ràng cho các chương trình.
- Làm cho mã dễ bảo trì, sửa đổi và gỡ lỗi hơn.
- Có tính bảo mật cao

<a name="_heading=h.2et92p0"></a>**3,Các khái niệm cơ bản** 

![Khái niệm OOPS trong C++](Aspose.Words.d5ab77ae-eaed-44f9-a67a-fbcd12b818a7.001.jpeg) 

<a name="_heading=h.tyjcwt"></a>**a) Đối tượng( Object )**

Đối tượng là một thực thể có thể nhận dạng với một số đặc điểm và hành vi.

Ví dụ : cây, nhà, ...

- Gồm 2 thành phần chính :
- Thuộc tính( Attribute ) : thông tin, đặc điểm của đối tượng
- Phương thức( method ) : những gì mà đối tượng thực hiện được

Ví dụ : Thuộc tính của xe : màu sắc, chất liệu, độ bền,…

`	 `Phương thức : chạy ,..

<a name="_heading=h.3dy6vkm"></a>**b) Lớp học( Class )**

Nó là kiểu dữ liệu do người dùng định nghĩa, chứa các thành viên dữ liệu và hàm thành viên riêng để mô tả lại các đối tượng trong thực tế vào chương trình của mình.

Chúng ta có thể nói rằng **Lớp trong C++** là một bản thiết kế đại diện cho một nhóm đối tượng chia sẻ một số thuộc tính và hành vi chung.

Ví dụ: Hãy xem xét loại **Ô tô** . Có thể có nhiều ô tô với các tên và nhãn hiệu khác nhau nhưng tất cả chúng sẽ chia sẻ một số thuộc tính chung như tất cả chúng sẽ có *4 bánh* , *Giới hạn tốc độ* , *Phạm vi quãng đường* , v.v. 

![Lightbox](Aspose.Words.d5ab77ae-eaed-44f9-a67a-fbcd12b818a7.002.png)

<a name="_heading=h.1t3h5sf"></a>**Access modifier trong C++** 

- Là các toán tử có tác dụng chỉ định quyền truy cập đối với các biến và hàm thành viên có trong một class.

Nhờ có Access modifier mà chúng ta có thể quyết định việc một thành phần ở bên ngoài một class có thể truy cập tới các thành viên bên trong class hay không, qua đó bảo vệ được thông tin chứa trong class đó.

Có 3 kiểu Access modifier là **public- protected - private trong C++.**

Lưu ý: Trong chương trình, nếu chúng ta lược bỏ hoặc không chỉ rõ access modifier khi khai báo thành viên của lớp  mặc định là access modifier Private sẽ được chỉ định.

**Public trong C++**

**Public trong C++** là Access modifier có tác dụng chỉ định thành viên của class có thể được truy cập từ bất cứ đâu trong chương trình.

Ví dụ : biến num của class TestClass ở dạng public, do vậy nó không những có thể được truy cập và sử dụng từ các hàm bên trong clas, mà còn có thể được truy cập từ hàm func() nằm ngoài class:

|<p>#include<iostream><br>using namespace std;<br>class TestClass<br>{<br>`    `public:    <br>`       `int num; //Khai báo biến public num <br>`       `TestClass ( ) {num = 100;} //Hàm khởi tạo<br>`       `void print()</p><p>`      `{</p><p>`            `cout << num <<endl;</p><p>`       `} //Hàm thành viên<br>};<br>//Khai báo hàm bên ngoài class<br>void func(int x){cout << 2\*x <<endl;}<br>int main()<br>{   <br>`    `/\*Truy cập biến num từ hàm print() trong class\*/<br>`    `TestClass obj;<br>`    `obj.print();     //100<br>`    `/\*Truy cập biến num từ hàm func() ngoài class\*/<br>`    `func(obj.num);   //200<br>`    `return 0;<br>}</p>|
| :- |

**Private** **trong** C++

**Private trong C++** là Access modifier có tác dụng chỉ định thành viên của class chỉ có thể được truy cập từ bên trong class mà thôi.

Ví dụ :biến num của class TestClass ở dạng private, do vậy nó có thể được truy cập từ hàm bên trong class. Tuy nhiên nếu chúng ta cố truy cập nó từ hàm func() nằm ngoài class, lỗi sẽ bị xảy ra.

|<p>#include<iostream><br>using namespace std;<br><br>class TestClass<br>{<br>private:  <br>`    `int num; /\*Khai báo biến private num \*/<br>public:      <br>`    `TestClass(){num = 100;} /\*Hàm khởi tạo\*/<br>`    `void print(){cout << num <<endl;} /\*Hàm thành viên\*/<br>};<br><br>/\*Khai báo hàm bên ngoài class\*/<br>void func(int x){cout << 2\*x <<endl;}<br><br>int main()<br>{   <br>`    `/\*Truy cập biến num từ hàm print() trong class\*/<br>`    `TestClass obj;<br>`    `obj.print();     //100<br><br>`    `/\*Truy cập biến num từ hàm func() ngoài class\*/<br>`    `func(obj.num);   //error: ‘int TestClass::num’ is private within<br>   </p><p>` `return 0;<br>}</p>|
| :- |

**Nên cách khai báo biến private ở trên cũng có thể được viết như sau:**

|<p>class TestClass<br>{<br>`    `int num; /\*Khai báo biến private num \*/</p><p>public:      <br>`    `TestClass(){num = 100;} /\*Hàm khởi tạo\*/<br>`    `void print(){cout << num <<endl;} /\*Hàm thành viên\*/<br>};</p>|
| :- |

**Protect trong C++**

**Protect trong C++** là Access modifier có tác dụng chỉ định thành viên của class chỉ có thể được truy cập từ bên trong class và từ các class con (class kế thừa) mà thôi.

Ví dụ :biến num của class TestClass ở dạng protect, do vậy nó có thể được truy cập từ hàm bên trong class, cũng như từ class con của nó. Tuy nhiên nếu chúng ta cố truy cập nó từ hàm func() nằm ngoài class, lỗi sẽ bị xảy ra.

|#include<iostream><br>using namespace std;<br><br>/\*Khai báo class\*/<br>class TestClass<br>{<br>`    `int num; /\*Khai báo biến public num \*/<br>public:      <br>`    `TestClass(){num = 100;} /\*Hàm khởi tạo\*/<br>`    `void print(){cout << num <<endl;} /\*Hàm thành viên\*/<br>};<br>/\*Khai báo class con được kế thừa từ class TestClass\*/<br>class DerivedClass : public TestClass<br>{<br>public:<br>`    `void printNew(int x) {cout << 3\*x <<endl;}<br>};<br><br>/\*Khai báo hàm bên ngoài class\*/<br>void func(int x){cout << 2\*x <<endl;}<br><br><br>int main()<br>{   <br>`    `/\*Truy cập biến num từ hàm print() trong class\*/<br>`    `TestClass obj;<br>`    `obj.print();     //100<br>    <br>`    `/\*Truy cập biến num từ class con\*/<br>`    `DerivedClass obj2;<br>`    `obj2.print();    //100<br><br>`    `/\*Truy cập biến num từ hàm func() ngoài class\*/<br>`    `func(obj.num);   //error: ‘int TestClass::num’ is private within<br>`    `return 0;<br>}|
| :- |

Ví dụ :

![](Aspose.Words.d5ab77ae-eaed-44f9-a67a-fbcd12b818a7.003.png)

<a name="_heading=h.4d34og8"></a>**Constructor**

Constructor hay hàm dựng là một hàm đặc biệt, nó sẽ được gọi ngay khi chúng ta khởi tạo một object. Vậy thì tại sao chúng ta lại cần có constructor?

Nếu bạn để ý ví dụ trên bạn sẽ thấy ta phải khởi tạo một object sau đó gán các property và sử dụng, việc này rất tốn thời gian. Constructor sẽ giúp chúng ta giải quyết việc này. Cú pháp khai báo một constructor giống với hàm nhưng không có kiểu dữ liệu trả về:

class MyClass 

{

`  `public:

`    `MyClass() { // constructor

`      `cout << "Hello World!";

`    `}

};

// sử dụng

MyClass object; // sẽ in ra màn hình "Hello World"

Lưu ý constructor phải được khai báo public. Công dụng chính của constructor chính là khởi gán các thuộc tính, vậy nên constructor thường được định nghĩa như sau:

class Person {

`	`public:

`	    `string firstName;

`	    `string lastName;

`	    `int age;

`	    `Person(string \_firstName, string \_lastName, int \_age)

`	    `{

`	        `firstName = \_firstName;

`	        `lastName = \_lastName;

`	        `age = \_age;

`	    `}

`	    `void fullname() 

`	   `{

`		`cout << firstName << ' ' << lastName;

`	    `}

};

Constructor cũng có thể định nghĩa thi hành bên ngoài class giống như phương thức vậy:

class Person 

{

`	`public:

`	    `string firstName;

`	    `string lastName;

`	    `int age;

`	    `Person(string \_firstName, string \_lastName, int \_age);

`	    `void fullname() {

`	        `cout << firstName << ' ' << lastName;

`	    `}

};

Person::Person(string \_firstName, string \_lastName, int \_age)

{

`	`firstName = \_firstName;

`	`lastName = \_lastName;

`	`age = \_age;

}

Để khởi tạo một object thông qua constructor, ta làm như sau:

Person person("Anh", "Tu", 20);

person.fullname(); // Anh Tu

Như vậy chúng ta không cần phải set từng thuộc tính cho object đó mà khởi tạo trực tiếp qua constructor.

<a name="_heading=h.2s8eyo1"></a>**Destructor**

Hàm **hủy** là một hàm thành viên đặc biệt của một lớp được thực thi bất cứ khi nào một đối tượng của lớp đó nằm ngoài phạm vi hoặc bất cứ khi nào biểu thức xóa được áp dụng cho một con trỏ tới đối tượng của lớp đó.

Một hàm hủy sẽ có cùng tên với lớp có tiền tố là dấu ngã (~) và nó không thể trả về một giá trị cũng như không thể nhận bất kỳ tham số nào. Destructor có thể rất hữu ích để giải phóng tài nguyên trước khi ra khỏi chương trình như đóng tệp, giải phóng bộ nhớ, v.v.

Ví dụ sau giải thích khái niệm hàm hủy 

|<p>class Test {</p><p>public:</p><p>`    `Test() { cout << "\n Constructor executed"; }</p><p> </p><p>`    `~Test() { cout << "\n Destructor executed"; }</p><p>};</p><p>main()</p><p>{</p><p>`    `Test t;</p><p>`    `return 0;</p><p>}</p>|
| :- |

**đầu ra**

Trình xây dựng được thực thi

` `Hàm hủy đã thực thi

|<p>class Test {</p><p>public:</p><p>`    `Test() { cout << "\n Constructor executed"; }</p><p> </p><p>`    `~Test() { cout << "\n Destructor executed"; }</p><p>};</p><p> </p><p>main()</p><p>{</p><p>`    `Test t, t1, t2, t3;</p><p>`    `return 0;</p><p>}</p>|
| :- |

**đầu ra**

Trình xây dựng được thực thi

` `Trình xây dựng được thực thi

` `Trình xây dựng được thực thi

` `Trình xây dựng được thực thi

` `Hàm hủy đã thực thi

` `Hàm hủy đã thực thi

` `Hàm hủy đã thực thi

` `Hàm hủy đã thực thi

|<p>int count = 0;</p><p>class Test {</p><p>public:</p><p>`    `Test()</p><p>`    `{</p><p>`        `count++;</p><p>`        `cout << "\n No. of Object created:\t" << count;</p><p>`    `}</p><p>`    `~Test()</p><p>`    `{</p><p>`        `cout << "\n No. of Object destroyed:\t" << count;</p><p>`        `--count;</p><p>`    `}</p><p>};</p><p>main()</p><p>{</p><p>`    `Test t, t1, t2, t3;</p><p>`    `return 0;</p><p>}</p>|
| :- |

**đầu ra**

Số đối tượng được tạo: 1

` `Số đối tượng được tạo: 2

` `Số đối tượng được tạo: 3

` `Số đối tượng được tạo: 4

` `Số đối tượng bị phá hủy: 4

` `Số đối tượng bị phá hủy: 3

` `Số đối tượng bị phá hủy: 2

` `Số đối tượng bị phá hủy: 1

<a name="_heading=h.17dp8vu"></a>**II. Các tính chất của OOP**

<a name="_heading=h.3rdcrjn"></a>**1.Tính đóng gói (Encapsulation):**

Là cách để che dấu những tính chất xử lý bên trong của đối tượng, những đối tượng khác không thể tác động trực tiếp làm thay đổi trạng thái  mà chỉ có thể tác động thông qua các method public của đối tượng đó. Mình sẽ tạo ra 2 class để thể hiện điều này:

`    `class hinhchunhat

`   `{

`        `Private :

`		 `int height;

`         	 `int width;

`        `public :

`	`void setHinhChuNhat(int newHeight, int newWidth) 

`	`{

`            `height = newHeight;

`            `width = newWidth;

`        `}

`        `int tinhdientich() 

`            `return height \* width;

`   `}

- height và width ở đây chính là các tính chất (**properties**) của đối  tượng **class** **hinhchunhat**
- **tinhdientich()** là method được public nhằm mục đích tương tác với các đối tượng khác. Tạo một **class mới** thay đổi tính chất  của đối tượng thông qua các method public:

int main()

{

`    `Hinhchunhat Anh;

Anh.setHinhChuNhat(10, 5);

cout << Anh.tinhdientich() ;

}

Như vậy khi ta muốn thay đổi các tính chất (properties) không thể tương tác trực tiếp với properties mà phải thông qua các method public được định nghĩa bên trong class.

- Người khác không thể biết luồng xử lý logic bên trong của đối tượng.

<a name="_heading=h.26in1rg"></a>**2.Tính kế thừa (Inheritance):**

Là kỹ thuật cho phép kế thừa lại những tính năng mà một đối tượng khác đã có, giúp tránh việc code lặp dư thừa mà chỉ xử lý công việc tương tự.

Cú pháp sử dụng tính kế thừa

Cú pháp chung để khai báo kế thừa như sau:

|<p>1</p><p>2</p><p>3</p><p>4</p>|<p>class subclass\_name : access\_mode base\_class\_name</p><p>{</p><p>`  `//body of subclass</p><p>};</p>|
| :-: | :- |

Trong đó:

- subclass\_name là tên lớp con sẽ áp dụng kế thừa
- base\_class\_name là tên lớp cha
- access\_mode có thể là public, private hoặc protected

Nếu các bạn không chỉ rõ access\_mode thì mặc định sẽ là private.

Dưới đây là một ví dụ về sử dụng tính kế thừa trong C++.

Sau khi chạy chương trình ta có kết quả sau

![](Aspose.Words.d5ab77ae-eaed-44f9-a67a-fbcd12b818a7.004.png)

|<p>1</p><p>2</p>|<p>Child id is 7</p><p>Parent id is 91</p>|
| :-: | :- |

Trong chương trình trên, class Child là lớp con, nó sẽ được kế thừa các thành viên dữ liệu dạng public từ class Parent
Nếu để các thành viên dữ liệu trên dạng private thì sẽ không thể dùng kế thừa

<a name="_heading=h.lnxbz9"></a>**3.Tính trừu tượng(Abstraction):**

Là phương pháp trừu tượng hóa định nghĩa lên những hành động, tính chất của loại đối tượng nào đó cần phải có. 

- Ví dụ khi bạn định nghĩa một lớp động vật(Animal), Animal thì có rất nhiều loại, làm sao để xác định đó là một loại động vật? lúc này bạn sẽ hình dung trong đầu động vật có những tính chất hành vi cơ bản nhất định phải có như ăn, nói khi bất kỳ một developer nào định viết một đối tượng thuộc lớp động vật sẽ kế thừa lại lớp Animal có 2 hành vi ăn, nói,đối tượng được tạo ra có thể khác nhau như chó hoặc mèo nhưng đều có những hành vi của động vật là ăn và nói. 

  **=>** Trong ví dụ trên nhìn vào hành vi ăn và nói của chó và mèo ta có thể khẳng định nó thuộc lớp động vật. 

  Vậy chốt lại rõ ràng tính trừu tượng ở đây sinh ra chủ yếu để trừu tượng hóa và định nghĩa các tính chất hành vi phải có để xác định đó là đối tượng gì dựa vào tính chất hành vi của đối tượng. 

  **=>** Các method trừu tượng đều rỗng không thực hiện bất kỳ hành vi nào, hành vi sẽ được triển khai cụ thể do các đối tượng kế thừa. 

Có 2 phương pháp để triển khai tính trừu tượng này:

1. Abstract class
- trong abstract class có 2 loại method:
- abstract method (là method rỗng không thực hiện gì)
- method thường (là vẫn có logic trả về data hoặc thực thi hành động nào đó, nó được sử dụng cho mục đích dùng chung)

Abstract class Animal và 2 class Dog, Cat kế thừa lại những method được public 

**2.** Interface 

` `Khá giống với abstract class nhưng interface không phải là class, trong interface chỉ  có khai báo những method/properties trống không có thực thi, thực thi sẽ được thể hiện trong các lớp kế thừa, interface giống như một cái khung mẫu để các lớp thực hiện và làm theo.

Ví dụ về Lớp trừu tượng trong C++

Bạn xem xét ví dụ sau: lớp cha cung cấp một Interface tới lớp cơ sở để triển khai một hàm **tinhDienTich()** trong C++:

#include <iostream>



using namespace std;



// day la lop co so (base class)

class Hinh 

{

public:

`   `// khai bao pure virtual function

`   `virtual int tinhDienTich() = 0;

`   `void setChieuRong(int rong)

`   `{

`      `chieurong = rong;

`   `}

`   `void setChieuCao(int cao)

`   `{

`      `chieucao = cao;

`   `}

protected:

`   `int chieurong;

`   `int chieucao;

};



// cac lop ke thua

class HinhChuNhat: public Hinh

{

public:

`   `int tinhDienTich()

`   `{ 

`      `return (chieurong \* chieucao); 

`   `}

};

class TamGiac: public Hinh

{

public:

`   `int tinhDienTich()

`   `{ 

`      `return (chieurong \* chieucao)/2; 

`   `}

};



int main(void)

{

`   `HinhChuNhat hcn;

`   `TamGiac  tag;



`   `hcn.setChieuRong(25);

`   `hcn.setChieuCao(4);

`   `// in dien tich cua doi tuong

`   `cout << "Tong dien tich HinhChuNhat la: " << hcn.tinhDienTich() << endl;

`   `tag.setChieuRong(20);

`   `tag.setChieuCao(15);

`   `// in dien tich cua doi tuong.

`   `cout << "Tong dien tich TamGiac la: " << tag.tinhDienTich() << endl; 

`   `return 0;

}

![Interface trong C++](Aspose.Words.d5ab77ae-eaed-44f9-a67a-fbcd12b818a7.005.png)

<a name="_heading=h.35nkun2"></a>**4.Tính đa hình (Polymorphism ):**

Là một đối tượng thuộc các lớp khác nhau có thể hiểu cùng một thông điệp theo cách khác nhau.

Ví dụ, cùng là một người nhưng tuỳ từng ngữ cảnh sẽ đóng vai trò khác nhau, một người đàn ông vừa là nhân viên (khi đi làm), vừa là một người chồng (đối với vợ) và là người cha (đối với con),… nói chung là anh ta sẽ biến hình thành con người khác nhau tuỳ từng ngữ cảnh.

Trong OOP và cụ thể là trọng ngôn ngữ C++ thì Polymorphism có 2 dạng:

<a name="_heading=h.1ksv4uv"></a>**Dạng 1 – Compile time Polymorphism:** 

- Một class có nhiều hàm cùng tên nhưng khác nhau về số lượng tham số hoặc kiểu dữ liệu của tham số. Khi call hàm cùng tên đó thì trong quá trình biên dịch, compiler sẽ quyết định hàm nào (trong số các hàm cùng tên) sẽ được call dựa trên số lượng tham số và kiểu dữ liệu của tham số truyển vào hàm. Việc định nghĩa các hàm cùng tên được gọi là **overloading – nạp chồng hàm**.

<a name="_heading=h.44sinio"></a>**Dạng 2 – Runtime Polymorphism:** 

- Cùng một class có thể cho ra nhiều biến thể, không phải được định nghĩa bởi lớp đó, mà bởi các lớp con của nó. Đây là một phương pháp để định nghĩa lại hành vi của lớp cơ sở mà không phải sửa code của lớp cơ sở. Nếu call hàm của đối tượng của lớp dẫn xuất thông qua con trỏ của lớp cơ sở thì việc hàm nào được call sẽ được quyết định lúc Runtime. Runtime Polymorphism được thực hiện bằng phương pháp **overriding – ghi đè phương thức.**

. — **Sample 1 – Compile time Polymorphism**

![](Aspose.Words.d5ab77ae-eaed-44f9-a67a-fbcd12b818a7.006.png)

<a name="_heading=h.2jxsxqh"></a>Ta có class *PrintData* có 3 phương thức cùng tên là *print(),* 3 phương thức này cùng có một tham số nhưng kiểu của tham số thì khác nhau, lần lượt là ***int, double*** và ***char\*.*** Trong hàm ***main*** gọi đến phương thức *print()* 3 lần với 3 tham số khác nhau*,* khi đó trình biên dịch sẽ dựa vào kiểu ‘(hoặc giá trị) của tham số truyền vào và tự quyết định phương thức nào trong 3 phương thức cùng tên sẽ được gọi. Chương trình này chạy sẽ ra kết quả trên console như sau:

![](Aspose.Words.d5ab77ae-eaed-44f9-a67a-fbcd12b818a7.007.png)

— **Sample 2 – Runtime Polymorphism**




![](Aspose.Words.d5ab77ae-eaed-44f9-a67a-fbcd12b818a7.008.png)

Chương trình này sẽ xuất ra màn hình nội dung như sau :

|![](Aspose.Words.d5ab77ae-eaed-44f9-a67a-fbcd12b818a7.009.png)||
| :- | :- |
Ở đây ta có class cha là *Pet* định nghĩa phương thức *makeSound*(), phương thức này đưa ra mô tả về tiếng kêu của con vật. Tiếng kêu được định nghĩa bởi hàm *getSound*(), hàm này được khai báo là hàm ảo (***virtual***) ở class cha, điều đó cho phép các class con như *Cat*, *Dog* định nghĩa lại (overriding) hàm này cho phù hợp với đặc điểm riêng của chúng. Chính vì vậy ở hàm ***main*** dù cùng là con trỏ *a\_pet* nhưng khi gọi hàm *makeSound*() 2 lần lại ra 2 nội dung khác nhau tuỳ thuộc vào đối tượng đang được trỏ tới lúc đó là đối tượng của class con nào (*Dog* hay *Cat*)

