**C++ - Buổi 3**

[I. Lớp pair trong C++	2](#_heading=h.gjdgxs)

[Làm thế nào bạn có thể khởi tạo một pair ?	2](#_heading=h.30j0zll)

[Member Functions	2](#_heading=h.1fob9te)

[1.Make_pair	2](#_heading=h.3znysh7)

[2.Swap	3](#_heading=h.2et92p0)

[3.Get	3](#_heading=h.tyjcwt)

[Operators	4](#_heading=h.3dy6vkm)

[II. Một số cấu trúc dữ liệu có sẵn trong C++	4](#_heading=h.1t3h5sf)

[SET	4](#_heading=h.4d34og8)

[Tính chất	5](#_heading=h.17dp8vu)

[Một số hàm cơ bản liên quan đến set	6](#_heading=h.3rdcrjn)

[MULTISET	9](#_heading=h.26in1rg)

[Khai báo :	9](#_heading=h.lnxbz9)

[Truy cập phần tử trong multiset C++	10](#_heading=h.35nkun2)

[Một số chức năng cơ bản liên quan đến multiset:	12](#_heading=h.1ksv4uv)

[Unordered Set	13](#_heading=h.44sinio)

[Một số hàm trong set	13](#_heading=h.2jxsxqh)

[Một ví dụ thực tế dựa trên unordered_set	14](#_heading=h.z337ya)

[MAP	15](#_heading=h.3j2qqm3)

[Các hàm thường dùng trong map	15](#_heading=h.1y810tw)

[MULTIMAP	20](#_heading=h.4i7ojhp)

[Truy cập phần tử	22](#_heading=h.2xcytpi)

[Duyệt phần tử trong multi`map	22](#_heading=h.1ci93xb)

[Lấy kích thước multimap trong C++ bằng hàm size	24](#_heading=h.3whwml4)

[Tìm phần tử trong multimap C++ bằng hàm find	25](#_heading=h.2bn6wsx)

[Unordered_map	32](#_heading=h.qsh70q)

[BITSET	32](#_heading=h.3as4poj)

[Thao tác trên bitset:	33](#_heading=h.1pxezwc)

[Các hàm chuyển đổi:	33](#_heading=h.49x2ik5)

[Các hàm trên bitset	34](#_heading=h.2p2csry)

[Toán tử	37](#_heading=h.147n2zr)

[III. STRUCT	38](#_heading=h.3o7alnk)

[1. Tại sao phải sử dụng kiểu dữ liệu cấu trúc (struct)?	38](#_heading=h.23ckvvd)

[2. Khái niệm kiểu dữ liệu cấu trúc (struct)	38](#_heading=h.ihv636)

[3. Định nghĩa kiểu dữ liệu cấu trúc (struct) trong C++	39](#_heading=h.32hioqz)

[4. Một số lưu ý khi định nghĩa kiểu cấu trúc và khai báo biến cấu trúc	41](#_heading=h.1hmsyys)



<a name="_heading=h.gjdgxs"></a> **I. Lớp pair trong C++**

Pair cho phép gộp 2 đối tượng thành 1 cặp, 2 đối tượng có thẻ cùng kiểu hoặc khác kiểu, với thuộc tính first là key và second là value.

<a name="_heading=h.30j0zll"></a>**Làm thế nào bạn có thể khởi tạo một pair ?**

- pair< valueType1, valueType2> variableName;
- pair< valueType1, valueType2> variableName(gia\_tri1, gia\_tri2) // {};
- pair< valueType1, valueType2> copyPair(P1);

Lớp pair có các thuộc tính first và second cho phép lấy dữ liệu

pair<string, string> word("hello", "hi");

cout << word.first << " " << word.second;

![](Aspose.Words.223b3745-b5b0-4e93-9fc3-829c3c0bb600.001.png)

<a name="_heading=h.1fob9te"></a>**Member Functions**

<a name="_heading=h.3znysh7"></a>**1.Make\_pair**

Cho phép bạn xây dựng một cặp giá trị mà không cần phải viết trực tiếp .

Cú pháp :Pair\_name = make\_pair (giá trị1,giá trị2);

![](Aspose.Words.223b3745-b5b0-4e93-9fc3-829c3c0bb600.002.png)

<a name="_heading=h.2et92p0"></a>**2.Swap**

Hàm này hoán đổi nội dung của một pair với nội dung của pair khác. Các pair phải cùng loại. 

Cú pháp : <name\_pair1>.swap(<name\_pair2>);

![](Aspose.Words.223b3745-b5b0-4e93-9fc3-829c3c0bb600.003.png)

<a name="_heading=h.tyjcwt"></a>**3.Get**

Truy cập vào phần tử của pair 

Cú pháp : get < index> (<name\_pair>);

![](Aspose.Words.223b3745-b5b0-4e93-9fc3-829c3c0bb600.004.png)

<a name="_heading=h.3dy6vkm"></a>**Operators** 

![](Aspose.Words.223b3745-b5b0-4e93-9fc3-829c3c0bb600.005.png)

<a name="_heading=h.1t3h5sf"></a>**II. Một số cấu trúc dữ liệu có sẵn trong C++**

<a name="_heading=h.4d34og8"></a>**SET**

<a name="_heading=h.2s8eyo1"></a>**Cú pháp  :** set <data\_type> set\_name;

Ví dụ:

set<int> val; // định nghĩa một tập rỗng set 

set<int> val = {6, 10, 5, 1}; // khởi tạo với các giá trị

- Thêm một phần tử vào *set*:

s.insert(a); // thêm phần tử a vào set

![](Aspose.Words.223b3745-b5b0-4e93-9fc3-829c3c0bb600.006.png)

Lý do nó chỉ in F và G là vì set không nhận nhiều giá trị giống nhau, nó chỉ chấp nhận một giá trị duy nhất. Chúng ta có thể sử dụng [Multiset](http://www.geeksforgeeks.org/multiset-in-cpp-stl/) nếu chúng tôi muốn lưu trữ nhiều giá trị giống nhau.

**How to sắp xếp set theo thứ tự giảm dần :**

Theo mặc định, set được sắp xếp theo thứ tự tăng dần. Tuy nhiên, chúng ta có thể tùy chỉnh thứ tự sắp xếp bằng cách sử dụng cú pháp sau:

set <loại\_dữ\_liệu , greater<loại\_dữ\_liệu> > set\_name;

Ví dụ:

![](Aspose.Words.223b3745-b5b0-4e93-9fc3-829c3c0bb600.007.png)

**Độ phức tạp về thời gian:** O(N) // N là kích thước của tập hợp.

**Không gian phụ trợ:** O(N)

<a name="_heading=h.17dp8vu"></a>**Tính chất**

1. Set lưu trữ các phần tử theo thứ tự **đã sắp xếp** .
1. Tất cả các phần tử trong một set đều có **giá trị duy nhất** .
1. Không thể sửa đổi giá trị của phần tử sau khi nó được thêm vào tập hợp, mặc dù có thể xóa và sau đó thêm giá trị đã sửa đổi của phần tử đó. Do đó, các giá trị là **bất biến** .
1. **Set** tuân theo việc triển khai **Binary search tree** .
1. Các giá trị trong một set không được **lập chỉ mục** .

***Lưu ý:** Để lưu trữ các phần tử theo thứ tự chưa sắp xếp (ngẫu nhiên),  có thể sử dụng [**unordered_set() .***](https://www.geeksforgeeks.org/unordered_set-in-cpp-stl/)*

<a name="_heading=h.3rdcrjn"></a>**Một số hàm cơ bản liên quan đến set**

- Trả về số phần tử của *set*:

s.size();

- Kiểm tra *set* rỗng hoặc không:

s.empty(); // trả về true nếu rỗng, false nếu không rỗng

- Xóa tất cả phần tử của *set*:

s.clear();

- Kiểm tra một giá trị có tồn tại trong *set* hoặc không, nếu có sẻ trả về con trỏ trỏ đến *x*, nếu không trả về s.end():

s.find(x);

- Để xóa phần tử *x* trong *set*:

s.erase(x);

- Xóa phần tử thứ *k* trong *set*:

set<int>::iterator it = s.begin(); // tạo con trỏ trỏ vào phần tử đầu tiên

advance(dt,k); // trỏ đến số thứ k trong s

s.erase(it); //  xóa phần tử thứ k

- Con trỏ trỏ đến vị trí phần tử nhỏ nhất mà lớn hơn khóa *x*, nếu không tìm thấy trả về vị trí s.end():

s.upper\_bound(x);

- Con trỏ trỏ đến vị trí phần tử nhỏ nhất mà lớn hơn hoặc bằng khóa *x*, nếu không tìm thấy trả về vị trí s.end():

s.lower\_bound(x);

1. int main()
1. {
1. set<int, greater<int> > s1;
1. s1.insert(40);
1. s1.insert(30);
1. s1.insert(60);
1. s1.insert(20);
1. s1.insert(50);
1. s1.insert(50);
1. s1.insert(10);
1. set<int, greater<int> >::iterator itr;
1. cout << "s1: **\n**";
1. for (itr = s1.begin(); itr != s1.end(); itr++)
1. {
1. cout << \*itr << " ";
1. }
1. cout << endl;
1. *// gán các phần tử của s1 sang s2*
1. set<int> s2(s1.begin(), s1.end());
1. cout << "s2: **\n**";
1. for (itr = s2.begin(); itr != s2.end(); itr++)
1. {
1. cout << \*itr << " ";
1. }
1. cout << endl;
1. *// xoa cac phan truoc 30 trong s2*
1. s2.erase(s2.begin(), s2.find(30));
1. cout << "s2 sau khi xoa : " ;
1. for (itr = s2.begin(); itr != s2.end(); itr++)
1. {
1. cout << \*itr << " ";
1. }
1. *// xoa phan tu 50 trong s2*
1. int num;
1. num = s2.erase(50);
1. cout << "**\n**s2.erase(50) : ";
1. cout << num << " **\n**";
1. for (itr = s2.begin(); itr != s2.end(); itr++)
1. {
1. cout << \*itr << " ";
1. }
1. cout << endl;
1. cout << "s1.lower\_bound(40) : " << \*s1.lower\_bound(40) << endl;
1. cout << "s1.upper\_bound(40) : " << \*s1.upper\_bound(40) << endl;
1. cout << "s2.lower\_bound(40) : " << \*s2.lower\_bound(40) << endl;
1. cout << "s2.upper\_bound(40) : " << \*s2.upper\_bound(40) << endl;
1. return 0;
1. }

**đầu ra**

s1 là: 60 50 40 30 20 10 

s2 là: 10 20 30 40 50 60 

s2 sau khi xóa các phần tử nhỏ hơn 30: 

30 40 50 60 

s2.erase(50): 1 đã xóa 

30 40 60 

s1.lower\_bound(40) : 40 

s1.upper\_bound(40) : 30 

s2.lower\_bound(40) : 40 

s2.upper\_bound(40) : 60

<a name="_heading=h.26in1rg"></a>**MULTISET**

**Multiset trong C++** là một **tập hợp tương tự set nhưng các phần tử có thể trùng lặp được sắp xếp theo thứ tự cụ thể**.Các phần tử trong multiset có thể trùng với các phần tử khác, ngoài ra thì phần tử trong multiset **không thể** thay đổi giá trị, tuy nhiên chúng có thể được chèn hoặc xóa khỏi multiset.

-Các hàm trong multiset có độ phức tạp thuật toán  O(log N), và nó còn cao hơn cả vector với tốc là O(1). 

|**Loại**|**Truy cập ngẫu nhiên**|**Thêm xóa tìm kiếm ngẫu nhiên**|
| :- | :- | :- |
|vector|O(1)|O(N)|
|multiset, set|chậm|O(log N)|

<a name="_heading=h.lnxbz9"></a>**Khai báo :**

multiset<type> name;

#include <iostream>
#include <set>   
using namespace std;

int main()
{
`    `multiset<string> name, job, sex;
`    `multiset<int> age;
}


|struct Person {<br>`    `string m\_name;<br>`    `int    m\_height;<br>};<br>// Định nghĩa toán tử so sánh nội bộ của struct<br>bool operator<(const Person &lhs, const Person &rhs)<br>{<br>`    `return lhs.m\_name < rhs.m\_name;<br>}<br><br>/\*Khai báo multiset thuộc kiểu struct\*/<br>std::multiset<Person> st;  |
| :- |

Ngoài cách khai báo rồi gán giá trị cho multiset sau đó thì chúng ta cũng có thể khởi tạo multiset và gán luôn giá trị ban đầu cho multiset.

Chúng ta **khởi tạo multiset trong C++** cách sử dụng cặp dấu ngoặc {} với cú pháp sau đây:

multiset<type> st {value1, value2, value3, ...};

Trong đó

- type là kiểu dữ liệu
- st là tên biến multiset
- value là các giá trị của multiset

Ví dụ:

|std::multiset<string> user{"Kiyoshi", "male", "Tokyo"};<br>//{"Kiyoshi", "male", "Tokyo"}|
| :- |

<a name="_heading=h.35nkun2"></a>**Truy cập phần tử trong multiset C++**

Chúng ta cũng không thể sử dụng index của các phần tử để truy cập vào nó theo cách thông thường được.Thay vào đó, chúng ta cần phải tiến hành truy cập tuần tự vào các phần tử của multiset, thông qua vòng lặp hoặc là trình lặp.

Ví dụ, chúng ta có thể truy cập vào phần tử của multiset 1 chiều thông qua vòng lặp dựa trên phạm vi như sau:

|#include <iostream><br>#include <set>   <br>using namespace std;<br><br>int main()<br>{<br>`    `multiset<string> user{"Kiyoshi", "male", "Tokyo"};<br>`    `int n=0, index = 2;<br>`    `for (string x: user) {<br>`        `/\*Truy cập vào phần tử thứ 2 trong multiset và kết thúc khi tìm thấy\*/<br>`        `if (n == index) {<br>`            `cout << x << endl;<br>`            `break;<br>`        `}<br>`        `++n ;<br>`    `}<br>`    `return 0;<br>}<br>// male|
| :- |

Chúng ta cũng có thể truy cập và in ra toàn bộ các phần tử trong multiset 1 chiều như sau:

|#include <iostream><br>#include <set>   <br>using namespace std;<br><br>int main()<br>{<br>`    `multiset<string> user{"Kiyoshi", "male", "Tokyo"};<br>`    `for (string x: user) {<br>`        `cout << x << endl;<br>`    `}<br>`    `return 0;<br>}|
| :- |

Kết quả:

|Kiyoshi<br>Tokyo<br>male|
| :- |

Tương tự khi chúng ta cần truy cập vào phần tử trong multiset 2 chiều trong C++:

|#include <iostream><br>#include <set>   <br>using namespace std;<br><br>int main()<br>{<br>`    `/\*Khởi tạo các multiset 1 chiều làm phần tử trong multiset 2 chiều\*/<br>`    `multiset<string> user1{"Kiyoshi", "male", "Hanoi"};<br>`    `multiset<string> user2{"Honda", "male", "Tokyo"};<br>`    `multiset<string> user3{"Ajinomoto", "female", "Osaka"};<br><br>`    `/\*Khai báo multiset 2 chiều\*/<br>`    `multiset<multiset<string> > all\_user{ user1, user2, user3};<br><br><br>`    `for (auto x: all\_user) {<br>`        `for (auto y: x) {<br>`            `cout << y << endl;<br>`        `}<br>`    `}<br><br>`    `return 0;<br>}|
| :- |

Và kết quả:

|Honda<br>male<br>Tokyo<br>Ajinomoto<br>female<br>Osaka|
| :- |

<a name="_heading=h.1ksv4uv"></a>**Một số chức năng cơ bản liên quan đến multiset:** 

- [begin()](https://www.geeksforgeeks.org/multiset-begin-and-end-function-in-c-stl/) – Trả về một iterator cho phần tử đầu tiên trong multiset –> O(1)
- [end()](https://www.geeksforgeeks.org/multiset-begin-and-end-function-in-c-stl/) – Trả về một iterator cho phần tử lý thuyết theo sau phần tử cuối cùng trong multiset –> O(1)
- [size()](https://www.geeksforgeeks.org/multiset-size-in-c-stl-with-examples/) – Trả về số phần tử trong multiset –> O(1)
- [max_size()](https://www.geeksforgeeks.org/multiset-max_size-in-c-stl/) – Trả về số phần tử tối đa mà multiset có thể chứa –> O(1)
- [empty()](https://www.geeksforgeeks.org/multiset-empty-function-in-c-stl/) – Trả về liệu multiset có trống hay không –> O(1)
- insert (x) – Chèn phần tử x vào multiset –> O(log n)
- clear() – Xóa tất cả các phần tử khỏi multiset –> O(n)
- [a.erase()](https://www.geeksforgeeks.org/multiset-erase-in-c-stl/) – Xóa tất cả các phiên bản của phần tử khỏi nhiều bộ có cùng giá trị
- [a.erase(a.find())](https://www.geeksforgeeks.org/multiset-erase-in-c-stl/) – Chỉ xóa một phiên bản phần tử khỏi nhiều tập hợp có cùng giá trị

![](Aspose.Words.223b3745-b5b0-4e93-9fc3-829c3c0bb600.008.png)

<a name="_heading=h.44sinio"></a>**Unordered Set**

Unordered\_set là một tập hợp trong đó một khóa có thể được lưu trữ theo bất kỳ thứ tự nào, vì vậy không có thứ tự. Nó được định nghĩa bên trong tệp tiêu đề < **unordered\_set > dưới dạng lớp std::unordered\_set** .

**Cú pháp:** unordered\_set<data\_type> tên;

<a name="_heading=h.2jxsxqh"></a>**Một số hàm trong set** 

- size() và empty () cho dung lượng.
- find() để tìm kiếm một khóa.
- insert () và erase () để sửa đổi.

Ví dụ:

![](Aspose.Words.223b3745-b5b0-4e93-9fc3-829c3c0bb600.009.png)

***Lưu ý:** Unordered\_set chỉ cho phép các khóa duy nhất, đối với các khóa trùng lặp, nên sử dụng unordered\_multiset.*

<a name="_heading=h.z337ya"></a>**Một ví dụ thực tế dựa trên unordered\_set**

Đưa ra một mảng (danh sách) các số nguyên, hãy tìm tất cả các số trùng lặp trong số chúng (giả sử các số trùng lặp là cùng một số được đoán bởi những người ngẫu nhiên trong một thử nghiệm).

**Đầu vào:**

mảng[] = {1, 5, 2, 1, 4, 3, 1, 7, 2, 8, 9, 5}

**Đầu ra:**

Các mục trùng lặp là: 5 2 1

**Ví dụ:**

![](Aspose.Words.223b3745-b5b0-4e93-9fc3-829c3c0bb600.010.png)

<a name="_heading=h.3j2qqm3"></a>**MAP**

*Map* là một kiểu dữ liệu với mỗi phần tử là ánh xạ giữa yếu tố key (khóa) với giá trị (value) của nó. *Map* không chứa hai phần tử nào giống nhau và các phần tử trong *map* được sắp xếp theo một thứ tự nào đó. Mỗi phần tử trong *map* có yếu tố *key* dùng để xác định *value* của nó. *Map*  nằm trong thư viện *Map*  vì vậy muốn sử dụng trước tiên phải #include <map>.

Cú pháp khai báo: map<valueType1, valueType2> variableName;

**Ví dụ:**

map<string, string> dictionary;

dictionary["eat"] = "an";

dictionary["sleep"] = "ngu";

Biến dictionary được khai báo với cặp dữ liệu là <string, string>, vì vậy:

- key của dictionary phải là kiểu string - "eat" "sleep"...
- value của dictionary phải là kiểu string - "an" "ngu"...

Lớp map cũng giống như những lớp vector, list đều được định nghĩa các hàm thành viên hỗ trợ cho việc truy xuất, lấy kích thước, các constructor đã được override, …

<a name="_heading=h.1y810tw"></a>**Các hàm thường dùng trong map**

a) Constructor

Cũng giống với những lớp vector, list đều có:

- default constructor
- ranger constructor
- copy constructor.

Các hàm thành viên này hoạt động hoàn toàn giống với lớp vector, list.

Ví dụ:

// default constructor

map<char, int> character0;

character0['a'] = 97;

character0['b'] = 98;

character0['c'] = 99;

character0['d'] = 100;

// range constructor

map<char, int> character1(character0.begin(), character0.end());

// copy constructor

map<char, int> character2(character1);

Ngoài ra còn có operator= cho phép các lớp map có thể sao chép nội dung cấu trúc dữ liệu với nhau.

map<int, char\*> map0, map1;

map0[0] = "a";

map0[1] = "b";

map1 = map0;

b) Duyệt map

Thao tác iterators cho phép truy xuất đến phần tử trong map để lấy dữ liệu value và key cần thiết. Có các iterators đã được cung cấp như: begin(), end(), rbegin(), rend(), ... chúng hoạt động như nhau nhưng chỉ khác phần tử truy cập ở vị trí nào trong lớp map.

Ví dụ:

map<int, char\*> texes;

texts[0] = "ab";

texts[1] = "bc";

texts[0] = "cd";

map<int, char\*>::iterator i;

for (i = texts.begin(); i != texts.end(); i++)

`	`cout << \*i << endl;

// output (0, "cd"), (1, "bc")

*Kết quả tại sao không phải là: (0, "ab") (1, "bc")  hay (0, "ab") (1, "bc") (0, "cd"), ... đó là do trong lớp map quy định key chỉ được tồn tại duy nhất (không được trùng), vì vậy khi khai báo ở dòng texts[0] = "cd"; sẽ làm thay đổi dữ liệu của texts[0] từ "ab" thành "cd".*

c) Kích thước 

size() cho phép lấy kích thước của map.

Ví dụ:

map<int, char\*> mymap, copymymap;

mymap[0] = "a";

mymap[1] = "b";

mymap[0] = "c";

cout << mymap.size();

d) Kiểm tra map có rỗng hay không?

empty() cho phép kiểm tra map có rỗng hay không?

Ví dụ:

map<int, char\*> mymap, copymymap;

mymap[0] = "a";

mymap[1] = "b";

mymap[0] = "c";

if (copymymap.empty()) cout << "copymymap is empty";

e) Truy xuất theo chỉ số

[index] hay at(index) cho phép truy xuất trực tiếp đến key của từng phần tử.

map<int, char\*> mymap, copymymap;

mymap[0] = "a";

mymap[1] = "b";

cout << mymap[1] << " " << mymap.at(0);

f) Thêm dữ liệu vào map

insert() cho phép chèn thêm 1 đối tượng.

Ví dụ:

map<int, char\*> mymap, copymymap;

mymap[0] = "a";

mymap[1] = "b";

mymap[5] = "c";

// chèn vào copymymap cặp đối tượng (10, "c")	

copymymap.insert(pair<int, char\*>(10, "c"));

// chèn (-1, "d") vào copymymap từ vị trí bắt đầu của copymymap

copymymap.insert(copymymap.begin(), pair<int, char\*>(-1, "d"));

// chèn mymap vào copymymap

copymymap.insert(mymap.begin(), mymap.end());

// => copymymap = {(-1,"d"),(0,"a"),(1,"b"),(5,"c"),(10,"c")}

*Lưu ý* : việc chèn ở vị trí nào thật ra là vô nghĩa, vì vị trí của nó phụ thuộc vào key trong cặp đối tượng "key/ value", trong ví dụ trên thì "key" là kiểu số nguyên vì vậy vị trí của các cặp đối tượng key/value sẽ được xác định theo các key sắp xếp tăng dần.

g) Tìm kiếm phần tử

find() cho phép tìm kiếm theo key của cặp giá trị key/value

Ví dụ:

map<int, char\*> mymap;

mymap[0] = "a";

mymap[1] = "b";

mymap[5] = "c";

mymap[9] = "e";

map<int, char\*>::iterator var = mymap.find(5);

// var -> (5,"c")

h) Xóa bỏ 1 phần tử trong map

erase() cho phép xóa 1 phần tử.

Ví dụ:

map<int, char\*> mymap, copymymap;

mymap[0] = "a";

mymap[1] = "b";

mymap[5] = "c";

mymap[7] = "d";

mymap[9] = "e";

// xóa cặp đối tượng với "key" là 5

mymap.erase(5);		

// => mymap =  {(0,"a"),(1,"b"),(7,"d"),(9,"e")}

map<int, char\*>::iterator var = mymap.begin();

// xóa cặp đối tượng mà var đang truy cập

mymap.erase(var); // => mymap =  {(1,"b"),(7,"d"),(9,"e")}

var = mymap.find(7); // => var truy cập đến (7,"d")

// xóa từ vị trí var đang truy cập cho đến (9,"e") 

mymap.erase(var, mymap.end()); // => mymap = {(1,"b")}

i) Xóa tất cả phần tử trong map

clear() cho phép xóa tất cả phần tử.

Ví dụ:

map<int, char\*> mymap;

mymap[0] = "a";

mymap[1] = "b";

mymap[5] = "c";

mymap[7] = "d";

mymap[9] = "e";

mymap.clear();		

// => mymap =  {}

k) Hoán đổi nội dung 2 map

swap() cho phép hoán đổi nội dung của 2 map.

Ví dụ:

map<char,int> map1, map2;

map1['x'] = 100;

map1['y'] = 200;

map2['a'] = 11;

map2['b'] = 22;

map2['c'] = 33;

map1.swap(map2);

// => map1 = {("x",11),("b",22),("c",33)}

// => map2 = {("x",100),("y",200)}
## <a name="_heading=h.4i7ojhp"></a>**MULTIMAP**
**Multimap trong C++** là một **tập hợp các phần tử được sắp xếp theo thứ tự cụ thể, với mỗi phần tử được hình thành bởi sự kết hợp của một cặp khóa và giá trị (key & value), trong đó nhiều phần tử có thể có các khóa giống nhau**.Về mặt tốc độ xử lý thì multimap được cho là chậm hơn **unordered\_map** khi cần truy cập vào một phần tử ngẫu nhiên, nhưng lại nhanh hơn **unordered\_map** trong việc thực thi các trình lặp trỏ tới chúng.

**Khai báo multimap trong C** như sau:

using namespace std;
multimap<k\_type, v\_type> mp; 

|#include <iostream><br>#include <map>   <br>using namespace std;<br><br>int main()<br>{<br>`    `multimap<double, string> user; <br>`    `multimap<int, char> info;    <br>}|
| :- |

Còn khi khai báo 1 multimap không thuộc kiểu dữ liệu nguyên thủy, ví dụ như struct chẳng hạn thì chúng ta phải tự tạo ra toán tử so sánh nội bộ **operator<()** để làm rõ quan hệ lớn nhỏ giữa các phần tử như ví dụ sau:

|struct Person {<br>`    `string m\_name;<br>`    `int    m\_height;<br>};<br>// Định nghĩa toán tử so sánh nội bộ của struct<br>bool operator<(const Person &lhs, const Person &rhs)<br>{<br>`    `return lhs.m\_name < rhs.m\_name;<br>}<br><br>/\*Khai báo multimap thuộc kiểu struct\*/<br>std::multimap<Person, int> mp;  |
| :- |
||
*Ngoài cách khai báo rồi thêm giá trị cho multimap sau đó thì chúng ta cũng có thể khởi tạo multimap và gán luôn giá trị ban đầu cho multimap.*

Chúng ta **khởi tạo multimap trong C++** cách sử dụng cặp dấu ngoặc {} với cú pháp sau đây:

multimap<k\_type, v\_type> mp = { {k1, v1}, {k2, v2}, {k3, v3}, ...};

Trong đó

- mp là tên biến multimap
- k\_type, v\_type là kiểu dữ liệu của key và value
- k,v là các cặp key và value

Lưu ý khác với map thì khóa trong multimap có thể trùng lặp, nên nếu chúng ta chỉ định các phần tử có cùng khóa thì tất cả chúng cũng sẽ được lưu vào map.

Ví dụ:

|#include <iostream><br>#include <map><br>using namespace std;<br><br>int main ()<br>{<br>`    `multimap<string,int> mp = {<br>`                `{ "alpha", 10 },<br>`                `{ "alpha", 20 },<br>`                `{ "beta", 20 },<br>`                `{ "alpha", 10 },<br>`                `{ "gamma", 30 } <br>`            `};<br>`    `for (auto& x: mp) {<br>`        `cout << x.first << ": " << x.second << '\n';<br>`    `}<br>`    `return 0;<br>}|
| :- |

Kết quả:

|alpha: 10<br>alpha: 20<br>alpha: 10<br>beta: 20<br>gamma: 30|
| :- |

<a name="_heading=h.2xcytpi"></a>**Truy cập phần tử**

Khác với map thì trong multimap không tồn tại toán tử [] hoặc hàm thành viên at() giúp truy cập vào phần tử thông qua key, do đó để truy cập phần tử trong multimap C++, chúng ta cần phải sử dụng vòng lặp tuần 

Ví dụ, chúng ta sử dụng vòng lặp dựa trên phạm vi để truy cập vào phần tử theo key trong multimap C++ như sau:

|#include <iostream><br>#include <map><br>using namespace std;<br><br>int main ()<br>{<br>`    `multimap<string,int> mp = {<br>`                `{ "alpha", 10 },<br>`                `{ "alpha", 20 },<br>`                `{ "beta", 20 },<br>`                `{ "alpha", 10 },<br>`                `{ "gamma", 30 } <br>`            `};<br><br>`    `for (auto& x: mp) {<br>`        `if(x.first == "alpha") cout << x.first <<": " << x.second << '\n';<br>`    `}<br>`    `return 0;<br>}|
| :- |


<a name="_heading=h.1ci93xb"></a>**Duyệt phần tử trong multimap**

Chúng ta có 2 phương pháp duyệt multimap trong C++ như sau:

- Sử dụng vòng lặp dựa trên phạm vi
- Sử dụng iterator

Duyệt multimap trong C++ bằng vòng lặp dựa trên phạm vi

Ccú pháp như sau:

for ( auto& x : mp) {
`    `cout << x.first << “: “ << x.second << endl;
}

Trong đó:

- mp là tên multimap.
- auto là kiểu suy luận giúp tự xác định kiểu dữ liệu của giá trị lấy từ multimap.
- x là tên một biến dùng để gán từng phần tử được lấy từ multimap.
- x.first và x.second lần lượt được sử dụng để lấy key và value của phần tử

Ví dụ :

|#include <iostream><br>#include <map>   <br>using namespace std;<br><br>int main()<br>{<br>`    `multimap<string,int> mp = {<br>`                `{ "alpha", 10 },<br>`                `{ "beta", 20 },<br>`                `{ "alpha", 20 },<br>`                `{ "gamma", 30 } };<br><br>`    `for (auto x: mp) {<br>`        `cout << x.first << ": " << x.second << endl;<br>`    `}<br>}|
| :- |

Kết quả:

|alpha: 10<br>alpha: 20<br>beta: 20<br>gamma: 30|
| :- |

Duyệt multimap trong C++ bằng iterator

Cú pháp như sau:

for(auto itr = mp.begin(); itr != mp.end(); ++itr) {
`    `cout << itr->first << ": "<< itr->second << "\n";
}

Trong đó:

- mp là tên multimap
- itr là tên iterator dùng để trỏ đến phần tử
- itr->first và itr->second lần lượt được sử dụng để lấy key và value của phần tử

Ví dụ :

|#include <iostream><br>#include <map>   <br>using namespace std;<br><br>int main()<br>{<br>`    `multimap<string,int> mp = {<br>`                `{ "alpha", 10 },<br>`                `{ "beta", 20 },<br>`                `{ "alpha", 20 },<br>`                `{ "gamma", 30 } };<br>`    `for(auto itr = mp.begin(); itr != mp.end(); ++itr) {<br>`        `cout  << itr->first << ": "<< itr->second << "\n";<br>`    `}<br>}|
| :- |

Kết quả

|alpha: 10<br>alpha: 20<br>beta: 20<br>gamma: 30|
| :- |

<a name="_heading=h.3whwml4"></a>**Lấy kích thước multimap trong C++ bằng hàm size**

Chúng ta sử dụng hàm size để lấy kích thước multimap trong C++ với cú pháp như sau:

mp.size();

|<p>#include <iostream><br>#include <map><br>using namespace std;</p><p>int main ()<br>{<br>`    `multimap<string,int> mp = {<br>`                `{ "alpha", 20 },<br>`                `{ "beta", 20 },<br>`                `{ "alpha", 10 },<br>`                `{ "gamma", 30 },<br>`                `{ "alpha", 10 },<br>`                `};<br>`    `for (auto x: mp) {<br>`        `cout << x.first << ": " << x.second << endl;<br>`    `}<br>`    `cout<< mp.size() <<endl;  <br>`    `return 0;<br>}</p>|
| :- |

Kết quả:

|alpha: 20<br>alpha: 10<br>alpha: 10<br>beta: 20<br>gamma: 30<br>5|
| :- |

<a name="_heading=h.2bn6wsx"></a>**Tìm phần tử trong multimap C++ bằng hàm find**

**Hàm find** là một hàm thành viên trong class std:multimap, có tác dụng tìm vị trí phần tử đầu tiên có khóa chỉ định trong multimap.

Chúng ta sử dụng hàm find trong C++ với cú pháp sau đây:

mp.find(key);

Trong đó key là khóa của phần tử cần tìm trong multimap mp.

Hàm find() sẽ trả về trình lặp trỏ đến vị trí phần tử, nếu nó tồn tại trong multimap. Và nếu phần tử đó không tồn tại, hàm sẽ trả về trình lặp trỏ đến vị trí cuối cùng trong multimap.

Lưu ý là hàm find() chỉ trả về một trình lặp cho một phần tử duy nhất mà thôi. Để có được toàn bộ phạm vi các phần tử có khóa chỉ định, hãy dùng hàm equal\_range mà Kiyoshi sẽ giới thiệu ở phần dưới.

|#include <iostream><br>#include <map><br>using namespace std;<br><br>//Tạo hàm xuất multimap<br>void dump(multimap<char,int>& mp)<br>{<br>`    `for (auto x: mp) {<br>`        `cout << x.first << ":" << x.second << " ";<br>`    `}<br>`    `cout << endl;<br>}<br> <br>int main() {<br>`    `multimap<char,int> mp;<br>`    `mp.insert(make\_pair('a', 1));<br>`    `mp.insert(make\_pair('b', 2));<br>`    `mp.insert(make\_pair('e', 5));<br>`    `mp.insert(make\_pair('c', 3));  <br>`    `mp.insert(make\_pair('d', 1));<br>`    `mp.insert(make\_pair('e', 2));<br>`    `mp.insert(make\_pair('f', 3)); <br>`    `mp.insert(make\_pair('e', 8)); <br>`    `dump(mp);<br>`    `//Tìm phần tử có khóa bằng 'b' trong multimap<br>`    `auto itr = mp.find('e');<br>`    `//Xóa phần tử vừa tìm thấy<br>`    `mp.erase (itr);<br>`    `dump(mp);<br>`    `return 0;<br>}|
| :- |

Kết quả:

|a:1 b:2 c:3 d:1 e:5 e:2 e:8 f:3 <br>a:1 b:2 c:3 d:1 e:2 e:8 f:3 |
| :- |

Giống như trên, mặc dù có 3 phần tử có khóa ‘e’ giống với khóa chỉ định, nhưng hàm find() chỉ trả về trình lặp trỏ đến phần tử đầu tiên mà thôi.

Tìm phần tử trong multimap C++ bằng hàm equal\_range

Chúng ta sử dụng hàm equal\_range trong C++ với cú pháp sau đây:

mp.equal\_range(key);

Trong đó key là khóa của phần tử cần tìm trong multimap mp.

Hàm equal\_range() sẽ trả về một cặp giá trị, với giá trị đầu tiên trỏ đến đầu phạm vi, và giá trị thứ hai trỏ đến cuối phạm vi chứa tất cả các phần tử có khóa giống khóa chỉ định.

|#include <iostream><br>#include <map><br>using namespace std;<br><br>//Tạo hàm xuất multimap<br>void dump(multimap<char,int>& mp)<br>{<br>`    `for (auto x: mp) {<br>`        `cout << x.first << ":" << x.second << " ";<br>`    `}<br>`    `cout << endl;<br>}<br>int main() {<br>`    `multimap<char,int> mp;<br>`    `mp.insert(make\_pair('a', 1));<br>`    `mp.insert(make\_pair('b', 2));<br>`    `mp.insert(make\_pair('e', 5));<br>`    `mp.insert(make\_pair('c', 3));  <br>`    `mp.insert(make\_pair('d', 1));<br>`    `mp.insert(make\_pair('e', 2));<br>`    `mp.insert(make\_pair('f', 3)); <br>`    `mp.insert(make\_pair('e', 8)); <br>`    `dump(mp);<br>`    `//Tìm phần tử có khóa bằng 'b' trong multimap<br>`    `auto ret = mp.equal\_range('e');<br>`    `//Xóa phần tử vừa tìm thấy<br>`    `mp.erase (ret.first,ret.second);<br>`    `dump(mp);<br>`    `return 0;<br>}|
| :- |

Kết quả:

COPY

|a:1 b:2 c:3 d:1 e:5 e:2 e:8 f:3 <br>a:1 b:2 c:3 d:1 f:3 |
| :- |

Giống như trên, toàn bộ phạm vi chứa các phần tử có khóa giống khóa ‘e’ chỉ định đã được xác định bởi hàm equal\_range() và được xóa đi.

Tìm phần tử trong multimap C++ bằng hàm lower\_bound

**Hàm lower\_bound** là một hàm thành viên trong class std::multimap, có tác dụng tìm vị trí **phần tử đầu tiên** trong multimap có khóa lớn hơn hoặc bằng với khóa chỉ định.

Chúng ta sử dụng hàm lower\_bound trong C++ với cú pháp sau đây:

mp.lower\_bound(key);

Hàm lower\_bound() sẽ trả về trình lặp trỏ đến vị trí **phần tử đầu tiên** có khóa lớn hơn hoặc bằng với khóa chỉ định. Và nếu không tìm thấy, hàm sẽ trả về trình lặp trỏ đến vị trí cuối cùng trong map.

|#include <iostream><br>#include <map><br>using namespace std;<br>//Tạo hàm xuất multimap<br>void dump(multimap<char,int>& mp)<br>{<br>`    `for (auto x: mp) {<br>`        `cout << x.first << ":" << x.second << " ";<br>`    `}<br>`    `cout << endl;<br>}<br>int main() {<br>`    `multimap<char,int> mp;<br>`    `mp.insert(make\_pair('a', 1));<br>`    `mp.insert(make\_pair('b', 2));<br>`    `mp.insert(make\_pair('e', 5));<br>`    `mp.insert(make\_pair('c', 3));  <br>`    `mp.insert(make\_pair('d', 1));<br>`    `mp.insert(make\_pair('e', 2));<br>`    `mp.insert(make\_pair('f', 3)); <br>`    `mp.insert(make\_pair('e', 8));<br>`    `mp.insert(make\_pair('b', 9));    <br>`    `dump(mp);   //a:1 b:2 b:9 c:3 d:1 e:5 e:2 e:8 f:3<br>    <br>`    `/\*Tìm vị trí phần tử đầu tiên có khóa lớn hơn hoặc bằng 'b' trong multimap\*/<br>`    `auto itr1 = mp.lower\_bound('b'); // itr1 trỏ đến b:2<br>`    `//Tìm vị trí phần tử đầu tiên có khóa lớn hơn 'e' trong multimap<br>`    `auto itr2 = mp.upper\_bound('e'); // itr2 trỏ đến f:3 <br>` `//Xóa các phần tử trong phạm vi [itr1, itr2)<br>`    `mp.erase (itr1, itr2);<br>`    `dump(mp);   //a:1 f:3 <br>`    `return 0;<br>}|
| :- |

Kết quả, các phần tử trong phạm vi từ b:2 đến trước f:3 đã bị xóa đi.

|a:1 b:2 c:3 d:1 e:2 f:3 <br>a:1 f:3 |
| :- |

Tìm phần tử trong multimap C++ bằng hàm upper\_bound

Ngược với hàm lower\_bound chính là hàm upper\_bound trong C++.

**Hàm upper\_bound** là một hàm thành viên trong class std::multimap, có tác dụng tìm vị trí **phần tử đầu tiên** có khóa lớn hơn khóa chỉ định trong multimap.

Chúng ta sử dụng hàm upper\_bound trong C++ với cú pháp sau đây:

mp.upper\_bound(key);

Trong đó key là khóa của phần tử cần tìm trong multimap mp.

Hàm upper\_bound() sẽ trả về trình lặp trỏ đến vị trí **phần tử đầu tiên** có khóa lớn hơn khóa chỉ định. Và nếu không tìm thấy, hàm sẽ trả về trình lặp trỏ đến vị trí cuối cùng trong map.

|#include <iostream><br>#include <map><br>using namespace std;<br>int main() {<br>`    `multimap<char,int> mp;<br>`    `mp.insert(make\_pair('a', 1));<br>`    `mp.insert(make\_pair('b', 2));<br>`    `mp.insert(make\_pair('e', 5));<br>`    `mp.insert(make\_pair('c', 3));  <br>`    `mp.insert(make\_pair('d', 1));<br>`    `mp.insert(make\_pair('e', 2));<br>`    `mp.insert(make\_pair('f', 3)); <br>`    `mp.insert(make\_pair('e', 8));<br>`    `mp.insert(make\_pair('b', 9));  <br>    <br>`    `/\*Duyệt map mp\*/<br>`    `for (auto x: mp) {<br>`        `cout << x.first << ":" << x.second << " ";<br>`    `}<br>`    `cout << endl;<br>`    `//a:1 b:2 b:9 c:3 d:1 e:5 e:2 e:8 f:3<br>`    `/\*Tìm vị trí phần tử đầu tiên có khóa lớn hơn hoặc bằng 'b' trong map\*/<br>`    `auto itr1 = mp.lower\_bound('b'); // itr1 trỏ đến b:2<br>`    `//Tìm vị trí phần tử đầu tiên có khóa nhỏ hơn 'e' trong map<br>`    `auto itr2 = mp.upper\_bound('e'); // itr2 trỏ đến f:3 <br>`    `//In các phần tử trong phạm vi [itr1, itr2)<br>`    `for (auto it=itr1; it!=itr2; ++it)<br>`        `cout << (\*it).first << ":" << (\*it).second << ' ';<br>`    `return 0;<br>}|
| :- |

Kết quả:

|a:1 b:2 b:9 c:3 d:1 e:5 e:2 e:8 f:3 <br>b:2 b:9 c:3 d:1 e:5 e:2 e:8 |
| :- |

Đếm số lần xuất hiện của phần tử trong multimap C++ bằng hàm count

Chúng ta sử dụng hàm count trong C++ với cú pháp sau đây:

mp.count(key);

Trong đó key là khóa của phần tử cần đếm số lần xuất hiện trong multimap mp.

Hàm count() sẽ trả về số phần tử có khóa giống khóa chỉ định được tìm thấy trong multimap.

Ví dụ :

|#include <iostream><br>#include <map><br>using namespace std;<br>int main() {<br>`    `multimap<char,int> mp;<br>`    `mp.insert(make\_pair('a', 100));<br>`    `mp.insert(make\_pair('b', 200));<br>`    `mp.insert(make\_pair('e', 500));<br>`    `mp.insert(make\_pair('c', 300));  <br>`    `mp.insert(make\_pair('d', 100));<br>`    `mp.insert(make\_pair('e', 200));<br>`    `mp.insert(make\_pair('f', 300)); <br>`    `//Đếm số lần xuất hiện của phần tử tồn tại trong multimap<br>`    `cout << mp.count('e') <<endl;<br>`    `//Đếm số lần xuất hiện của phần tử không tồn tại trong multimap<br>`    `cout << mp.count('x') <<endl;<br>`    `return 0;<br>}|
| :- |

Kết quả:

|2<br>0|
| :- |

Xóa 1 phần tử trong multimap bằng hàm erase c++

mp.erase(itr);
OR
mp.erase(key);

Hàm multimap erase sẽ trả về số lượng phần tử đã được xóa đi từ multimap ban đầu.

Ví dụ :

|#include <iostream><br>#include <map><br>using namespace std;<br>//Tạo hàm xuất multimap<br>void dump(multimap<char,int>& mp)<br>{<br>`    `for (auto x: mp) {<br>`        `cout << x.first << ":" << x.second << " ";<br>`    `}<br>`    `cout << endl;<br>}<br>int main ()<br>{<br>`    `multimap<char,int> mp;<br>`    `mp.insert(make\_pair('a', 1));<br>`    `mp.insert(make\_pair('b', 2));<br>`    `mp.insert(make\_pair('c', 5));<br>`    `mp.insert(make\_pair('d', 5));<br>`    `mp.insert(make\_pair('e', 6));    <br>`    `dump(mp); <br>`    `/\*Tìm trình lặp trỏ đến phần tử có khóa bằng 'c' \*/<br>`    `auto itr = mp.find('c');<br>`    `//xóa phần tử tại vị trí itr chỉ đến<br>`    `mp.erase(itr);<br>`    `dump(mp);<br>`    `//xóa phần tử có khóa bằng 'd' trong multimap<br>`    `mp.erase('d');<br>`    `dump(mp);<br>`    `return 0;<br>}|
| :- |

Kết quả:

|a:1 b:2 c:5 d:5 e:6 <br>a:1 b:2 d:5 e:6 <br>a:1 b:2 e:6 |
| :- |
## <a name="_heading=h.qsh70q"></a>**Unordered\_map**
Ngoài map ra, nếu các bạn tìm hiểu sâu hơn về kiểu dữ liệu này sẽ phát hiện còn có thêm một kiểu dữ liệu với cái tên khá tương đồng:  *unordered*\_*map*. Qua tên thì chúng ta cũng đoán được phần nào về kiểu dữ liệu này rồi nhỉ, có thể tạm hiểu là *map* nhưng không thứ tự!
## <a name="_heading=h.3as4poj"></a>**BITSET**
1 bitset dùng để lưu trữ các bit (các phần tử chỉ có hai giá trị là 0 hoặc 1, đúng hoặc sai,..)

Một bitset là một mảng các bool nhưng thay vào đó, mỗi giá trị boolean không được lưu trữ trong một byte riêng biệt, bitset tối ưu hóa không gian sao cho mỗi **giá trị boolean chỉ chiếm không gian 1 bit** , vì vậy **dung lượng mà bitset chiếm ít hơn dung lượng của một mảng bool hoặc vectơ của bool** . 

Một hạn chế của bitset là **kích thước phải được biết tại thời điểm biên dịch, tức là kích thước của bitset là cố định.**

**std::bitset** là mẫu lớp cho bitset được xác định bên trong **tệp tiêu đề <bitset>** , vì vậy chúng tôi cần bao gồm tệp tiêu đề trước khi sử dụng bitset trong chương trình của mình.

**Cú pháp:**

bitset<size> tên\_biến(khởi tạo);

Chúng ta có thể khởi tạo bitset theo ba cách:

**1. Chưa khởi tạo:** Tất cả các bit sẽ được đặt thành 0.

bitset<size> tên\_biến;

**2. Khởi tạo với số nguyên thập phân:** Bitset sẽ biểu diễn số thập phân cho trước ở dạng nhị phân.

bitset<size> tên\_biến(DECIMAL\_NUMBER);

**3. Khởi tạo với chuỗi nhị phân:** Bitset sẽ đại diện cho chuỗi nhị phân đã cho.

bitset<size> tên\_biến(chuỗi("BINARY\_STRING");

bitset<size> tên\_biến("BINARY\_STRING");

**Ví dụ:**

![](Aspose.Words.223b3745-b5b0-4e93-9fc3-829c3c0bb600.011.png)

<a name="_heading=h.1pxezwc"></a>**Thao tác trên bitset:**

- **set()**: Chuyển bit tại ví trí chỉ định thành bit mong muốn, mặc định chuyển thành bit 1.
- `  `std::bitset<4> foo; //foo = 0000
- `  `foo.set();    // foo = 1111
- `  `foo.set(1,0);   // foo = 1101
- `  `foo.set(2,0); // foo = 1001

  `  `foo.set(1)   // foo = 1011​

- **reset()**: Chuyển bit chỉ định hoặc tất cả các bit thành bit 0.
- `	`std::bitset<4> foo; 
- `	`foo = 7; // foo = 0111
- `	`foo.reset(1); // foo = 0101

  `	`foo.reset(); // foo = 0000​

- **flip()**: Chuyển bit chỉ định hoặc tất cả các bit thành bit khác ( bit 0 thành bit 1 và ngược lại.

<a name="_heading=h.49x2ik5"></a>**Các hàm chuyển đổi:**

- **to\_string()**: Chuyển bitset về dạng chuỗi nhị phân.
- `	`std::bitset<4> foo; 
- `	`foo = 7;
- `	`cout << "String = " << foo.to\_string();

  // Kết quả là: String = 0111​

- **to\_ulong()**: Chuyển bitset về dạng số nguyên.
- `	`std::bitset<4> foo(string("0111"));
- `	`cout << foo.to\_ulong();

  // kết quả là: 7​

- **to\_ullong()**: Tương tự **to\_ulong()** (Chỉ hỗ trợ cho C++ 11).

<a name="_heading=h.2p2csry"></a>**Các hàm trên bitset**

1 . Hàm All :

Trả về True nếu tất cả các thành phần trong bitset đều là 1 và trả về false nếu có 1 phần tử khác 1

Ví dú :

// bitset::all

#**include** <iostream>       // std::cin, std::cout, std::boolalpha

#**include** <bitset>         // std::bitset

**int** **main** ()

{

`  `std::bitset<8> foo;

`  `std::cout << "Please, enter an 8-bit binary number: ";

`  `std::cin >> foo;

`  `std::cout << std::boolalpha;

`  `std::cout << "all: " << foo.all() << '\n';

`  `std::cout << "any: " << foo.any() << '\n';

`  `std::cout << "none: " << foo.none() << '\n';

`  `**return** 0;

}

Kết quả trả về :

Please, enter an 8-bit binary number: 11111111

all: true

any: true

none: false

2 . Hàm Any :

Trả về true nếu trong bitset có bất kì phần tử nào có giá trị là 1 và trả false trong trường hợp còn lại

Ví dụ :

// bitset::any

#**include** <iostream>       // std::cin, std::cout

#**include** <bitset>         // std::bitset

**int** **main** ()

{

`  `std::bitset<16> foo;

`  `std::cout << "Please, enter a binary number: ";

`  `std::cin >> foo;

`  `**if** (foo.any())

`    `std::cout << foo << " has " << foo.count() << " bits set.\n";

`  `**else**

`    `std::cout << foo << " has no bits set.\n";

`  `**return** 0;

}

Kết quả trả về :

Please, enter a binary number: 10110

0000000000010110 has 3 bits set.

3\. Hàm count :

Hàm sẽ trả về số lượng phần tử bằng 1 trong bitset

Ví dụ :

// bitset::count

#**include** <iostream>       // std::cout

#**include** <string>         // std::string

#**include** <bitset>         // std::bitset

**int** **main** ()

{

`  `std::bitset<8> **foo** (std::string("10110011"));

`  `std::cout << foo << " has ";

`  `std::cout << foo.count() << " ones and ";

`  `std::cout << (foo.size()-foo.count()) << " zeros.\n";

`  `**return** 0;

}

Kết quả trả về :

10110011 has 5 ones and 3 zeros

4\. Hàm size :

Trả về số lượng của các phần tử trong bitset

Code mẫu :

// bitset::size

#**include** <iostream>       // std::cout

#**include** <bitset>         // std::bitset

**int** **main** ()

{

`  `std::bitset<8> foo;

`  `std::bitset<4> bar;

`  `std::cout << "foo.size() is " << foo.size() << '\n';

`  `std::cout << "bar.size() is " << bar.size() << '\n';

`  `**return** 0;

}

Kết quả trả về :

foo.size() **is** 8

bar.size() **is** 4

<a name="_heading=h.147n2zr"></a>**Toán tử**

|**Toán tử** |**Chức năng**|
| :-: | :-: |
|[]|Toán tử **truy cập**|
|&|Bitwise **AND**|
|||Bitwise **HOẶC**|
|!|Bitwise **XOR**|
|<<=|**Dịch chuyển** nhị phân sang phải|
|>>=|Dịch trái nhị **phân**|
|&=|Gán giá trị của bitwise **AND** cho tập bit đầu tiên.|
||=|Gán giá trị của bitwise **OR** cho bitset đầu tiên.|
|^=|Gán giá trị của bitwise **XOR** cho bitset đầu tiên.|
|~|Bitwise **KHÔNG**|

<a name="_heading=h.3o7alnk"></a>**III. STRUCT**

<a name="_heading=h.23ckvvd"></a>**1. Tại sao phải sử dụng kiểu dữ liệu cấu trúc (struct)?**

Cần viết chương trình lưu thông tin **1 sinh viên** gồm các thông tin:

- MSSV: kiểu chuỗi
- Tên SV: kiểu chuỗi
- Ngày sinh: kiểu chuỗi
- Phái: kiểu luận lý
- Điểm Toán, Lý, Hóa: kiểu số thực

Khai báo các biến lưu thông tin **1 sinh viên**

- string mssv; **// “0306201123”**
- string hoten; **// “Nguyễn Văn Minh”**
- string ngaysinh; **// “16/08/2002”**
- bool phai; **// true: Nữ, false: Nam**
- float Toan, Ly, Hoa; **//8.5, 9, 7.5**
## <a name="_heading=h.ihv636"></a>**2. Khái niệm kiểu dữ liệu cấu trúc (struct)**
**Kiểu dữ liệu cấu trúc (struct)** là một nhóm các thành phần dữ liệu, được gom lại với nhau và đặt trong một tên. Trong đó:

– Mỗi thành phần dữ liệu gọi là **trường dữ liệu** hoặc thành viên.

– Các trường dữ liệu có thể có kiểu dữ liệu khác nhau.

– Lập trình viên **tự định nghĩa kiểu dữ liệu cấu trúc** gồm những thành phần dữ liệu.
## <a name="_heading=h.32hioqz"></a>**3. Định nghĩa kiểu dữ liệu cấu trúc (struct) trong C++**
#### ***Cú pháp định nghĩa một kiểu dữ liệu cấu trúc mới***
**struct <tên kiểu cấu trúc>**

**{**

`            `**<kiểu dữ liệu> <tên thành phần 1>;**

`            `**…**

`            `**<kiểu dữ liệu> <tên thành phần n>;**

**};//lưu ý phải có dấu ;**

**Ví dụ:**

struct DIEM

{

`	`int x;

`	`int y;

};

struct SINHVIEN

{

`	`string mssv;

`	`string hoten;

`	`string ngaysinh;

`	`bool phai;

`	`float Toan, Ly, Hoa;

Muốn sử dụng các kiểu cấu trúc đã định nghĩa để lưu trữ dữ liệu thì cần tạo ra các biến của kiểu cấu trúc đó. Cú pháp khai báo biến của kiểu cấu trúc là:

**<tên kiểu cấu trúc> <tên biến cấu trúc>;**

**Ví dụ:**

DIEM d1, d2;

SINHVIEN sv1, sv2;
#### ***Định nghĩa kiểu cấu trúc và khai báo biến cấu trúc cùng lúc***
Việc khai báo biến cấu trúc có thể được thực hiện đồng thời với việc định nghĩa cấu trúc. Muốn vậy, cần đặt **danh sách tên biến cấu trúc** cần khai báo sau dấu **}** theo cú pháp sau:

**struct <tên kiểu cấu trúc>**

**{**

`            `**<kiểu dữ liệu> <tên thành phần 1>;**

`            `**…**

`            `**<kiểu dữ liệu> <tên thành phần n>;**

**} <tên biến 1>, <tên biến 2>,…, <tên biến m>;**

**Ví dụ:**

struct DIEM

{

`	`int x;

`	`int y;

} d1, d2;

struct SINHVIEN

{

`	`string mssv;

`	`string hoten;

`	`string ngaysinh;

`	`bool phai;

`	`float Toan, Ly, Hoa;

} sv1, sv2;
#### ***Khởi tạo giá trị cho biến cấu trúc***
##### Cú pháp khởi tạo giá trị cho biến cấu trúc
**<tên biến cấu trúc> = {<giá trị 1>,…,<giá trị n>};**
##### – Khởi tạo biến cấu trúc khi định nghĩa cấu trúc
struct DIEM

{

`	`int x;

`	`int y;

} d1 = {5, 9}, d2 = {1, 1};

Copy
##### – Khởi tạo biến cấu trúc khi khai báo biến cấu trúc
struct DIEM

{

`	`int x;

`	`int y;

};

DIEM d1 = {5, 9};

DIEM d2 = {1, 1};

Copy

**Lưu ý**: Có thể chỉ khởi tạo giá trị cho một số **thành phần dữ liệu đầu tiên** trong cấu trúc

DIEM d1 = {99};//chỉ khởi tạo giá trị cho x = 99, y không được khởi tạo. y sẽ nhận giá trị mặc định hoặc giá trị rác.
## <a name="_heading=h.1hmsyys"></a>**4. Một số lưu ý khi định nghĩa kiểu cấu trúc và khai báo biến cấu trúc**
#### ***Thiếu dấu ; khi định nghĩa kiểu cấu trúc***
#### ***Khởi tạo biến cấu trúc sau khi khai báo sẽ gây lỗi***
struct DIEM

{

`	`int x;

`	`int y;

}d1, d2;

d1 = {1, 5};//lỗi

DIEM d3;

d3 = {1, 9};//lỗi
#### ***Không thể khởi tạo các thành phần cấu trúc trong khi định nghĩa cấu trúc***
struct HINH\_TRON

{

`	`float x = 5.5; //Không hợp lệ

`	`float y = 3.2; //Không hợp lệ

`	`float BanKinh = 6; //Không hợp lệ

};

