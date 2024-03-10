**C++ - Buổi 2**

[I. Lớp string trong C++	1](#_heading=h.gjdgxs)

[II. Thao tác với string	1](#_heading=h.30j0zll)

[1) Chức năng nhập xuất	1](#_heading=h.1fob9te)

[2) Thao tác chuỗi	4](#_heading=h.3znysh7)

[*  Stringstream	5](#_heading=h.2et92p0)

[III. Các hàm thường dùng trong thư viện algorithm	6](#_heading=h.tyjcwt)



<a name="_heading=h.gjdgxs"></a>**I. Lớp string trong C++**

Trong C++, bạn có thể tạo ra một **đối tượng string** để lưu trữ chuỗi ký tự. Không giống mảng ký tự, đối tượng string và có thể mở rộng không có kích thước cố định nếu cần

Đối tượng string được tạo bởi lớp string trong thư viện **#include <string>**.

Cú pháp : string  ten\_bien;

**Chú ý:** *Khi khởi tạo giá trị là số cho một chuỗi, chuỗi đó không được coi là một số, và không có những thao tác như một biến số học ( cộng, trừ, nhân, chia …).* **C++ không tự động chuyển một chuỗi số về giá trị số nguyên (integer) hoặc số chấm động (floating point)***.*

<a name="_heading=h.30j0zll"></a>**II. Thao tác với string**

<a name="_heading=h.1fob9te"></a>**1) Chức năng nhập xuất**

Giống như việc nhập các loại dữ liệu khác, chúng ta sử dụng lệnh cin để nhập và sử dụng lệnh cout để xuất một string trong C++ :

![](Aspose.Words.910e155c-dbce-475f-9099-9a2924ec603c.001.png)

**Nhập nhiều string trong C++**

Để nhập nhiều string trong C++ cách nhau bởi dấu cách, chúng ta viết các string nhập vào cách nhau bởi toán tử >>, khi dùng lệnh cin với cú pháp sau đây:

string str1, str1, str3;
cin >> str1 >> str2 >>str3 ;

**Nhập string có khoảng trắng trong C++ bằng hàm getline**

Cin trong C++ chỉ có tác dụng nhập các string không chứa khoảng trắng. Trong trường hợp cần nhập string chứa khoảng trắng tạo bởi dấu cách, tab chúng ta sẽ dùng hàm getline() để thay thế.

**Hàm getline** là một hàm thành viên trong class std:string, có tác dụng **nhập toàn bộ một string từ bàn phím** vào chương trình C++. Hàm getline sẽ nhận và lưu trữ toàn bộ string nhập vào cho tới khi tìm thấy ký tự phân cách chỉ định hoặc là ký tự xuống dòng \n.

Cú pháp: getline(std::cin, name);

Đây là ví dụ về khai báo thư viện string và sử dụng getline

![](Aspose.Words.910e155c-dbce-475f-9099-9a2924ec603c.002.png)

Đối với nhập 1 giá trị thì không bị trôi lệnh, nhưng khi bạn nhập nhiều chuỗi hãy đề phòng bị trôi lệnh. Sau khi nhập số tuổi thì không thể nhập được chuỗi và chương trình tự kết thúc. 

- Lí do là nó sẽ gắn giá trị  tuổi cho biến tuổi và giá trị ‘\n’ cho chuỗi ten. Để khắc phục điều này thì trước khi nhập chuỗi ta phải xóa bộ nhớ đệm bằng câu lệnh **cin.ignore** (so luong ki tu).
- **Cách sử dụng câu lệnh** cin.ignore

![](Aspose.Words.910e155c-dbce-475f-9099-9a2924ec603c.003.png)

**Cách nhập chuỗi trong c++ dùng hàm gets**

Nếu bạn khai báo là một con trỏ char hay một mảng char thì bạn có thể dùng hàm gets() để nhập. **Ví dụ cách sử dụng hàm** gets()

![](Aspose.Words.910e155c-dbce-475f-9099-9a2924ec603c.004.png)

Nhưng nếu bạn biên dịch chương trình trên bằng Visual Studio thì sẽ bị lỗi ngay. Lý do bị lỗi là chương trình không thể biết bạn nhập bao nhiêu kí tự. Vì vậy bạn có thể nhập bằng **hàm fgets()** thay vì hàm gets() .

Cú pháp nhập: fgets( name, count, file) trong đó

- name là tên biến cần nhập.
- count là số kí tự tối đa nhập vào.
- file là tên file cần nhập, trong trường hợp này ta sẽ dùng stdin.

  <a name="_heading=h.3znysh7"></a>**2) Thao tác chuỗi** 

  Một số hàm thao tác chuỗi thường dùng của thư viện chuỗi trong C++

1. **s.length() // s.size() :** tìm độ dài của một chuỗi đã cho. 
1. **Phương pháp nối**
       1. Toán tử **“+”:**  Chúng ta có thể nối hai chuỗi và gán chúng cho một chuỗi khác mà không ảnh hưởng đến giá trị của các chuỗi ban đầu bằng toán tử này.
   2. **Toán tử “+=”:**  Chúng ta có thể nối hai chuỗi và gán chúng cho một trong hai chuỗi đó bằng cách sử dụng toán tử này.
1. **s.clear():** Chức năng của thư viện chuỗi xóa tất cả nội dung của một chuỗi đã cho.
1. **s.empty ():**  Hàm này kiểm tra xem giá trị đã cho có trống hay không và trả về True hoặc false làm đầu ra.
1. **a.compare(b) :** so sánh 2 string
1. **s.substr(start\_index, no\_of\_characters\*):** Hàm này trả về chuỗi con của một chuỗi bắt đầu từ chỉ mục bắt đầu cho đến số ký tự đã cho. Nếu đối số thứ hai tùy chọn không được cung cấp, nó sẽ trả về một chuỗi con cho đến cuối chuỗi.
1. **s.at(index) // s[ index ]:**  Hàm này tìm nạp và trả về một ký tự tại một chỉ mục nhất định trong chuỗi.
1. **replace(start\_index, no\_of\_characters, replace\_by):** Điều này thay thế số ký tự đã cho bắt đầu từ chỉ mục bắt đầu bằng đối số replce\_by.
1. **find(substring):**  Hàm này trả về chỉ số của lần xuất hiện đầu tiên của chuỗi con và trả về -1 nếu không tìm thấy chuỗi con.
1. s.**push\_back()** : thêm một phần tử vào sau chuỗi
1. **s.pop\_back() :** sẽ xóa đi ký tự cuối cùng hiện tại của chuỗi.
1. **stoi(s) :** chuyển xâu sang số int 
1. **to\_string(a) :** chuyển số sang xâu
1. **a.find(b) :** hàm trả về index đầu tiên của xâu con trong xâu ban đầu trong trường hợp xâu con xuất hiện 1 hoặc nhiều lần trong xâu ban đầu. Nếu xâu con không tồn tại trong xâu ban đầu hàm trả về giá trị string::npos

![](Aspose.Words.910e155c-dbce-475f-9099-9a2924ec603c.005.png)

<a name="_heading=h.2et92p0"></a>**\*  Stringstream**

Cho phép chuyển đổi giữa các kiểu dữ liệu khác nhau và chuỗi. Nó cung cấp các hàm hỗ trợ như <<, >>, getline() và str() để chuyển đổi dữ liệu và làm việc với chuỗi. stringstream cũng có thể dùng để đọc hoặc ghi dữ liệu từ hoặc vào một luồng (stream).

![](Aspose.Words.910e155c-dbce-475f-9099-9a2924ec603c.006.png)

![](Aspose.Words.910e155c-dbce-475f-9099-9a2924ec603c.007.png)

<a name="_heading=h.tyjcwt"></a>**III. Các hàm thường dùng trong thư viện algorithm**

1\. min( a , b ) : trả về số bé hơn

2\. max( a , b ) : trả về số lớn hơn 

![](Aspose.Words.910e155c-dbce-475f-9099-9a2924ec603c.008.png)

3\. min\_element( a, a + n) : trả về con trỏ vị trí của phần tử nhỏ nhất trong mảng.

4\. max\_element( a, a + n) : trả về con trỏ vị trí của phần tử lớn nhất trong mảng.

5\. swap( a, b) : giúp bạn nhanh chóng hoán đổi giá trị của a và b.

6\. sort(a , a + n)

Một hàm rất hay trong thư viện algorithm đó chính là hàm sắp xếp này(o(nlog(n))). Hàm này có tốc độ sắp xếp còn nhanh hơn [thuật toán quick sort](https://nguyenvanhieu.vn/thuat-toan-sap-xep-quick-sort/) đấy.

Sắp xếp dãy theo thứ tự tăng dần(mặc định). Nếu muốn sắp xếp theo thứ tự ngược lại, bạn sẽ cần truyền vào hàm comp.

Với các kiểu dữ liệu nguyên thủy, có hàm comp mặc định là std::greater và std::less.

7\.find( a, a + n, gia\_tri\_can\_tim) : trả về it 

8\.binary\_search( a, a + n, gia\_tri\_can\_tim)

Trả về true nếu tồn tại phần tử trong [first, last) bằng với val. Ngược lại, trả về false.

9\.lower\_bound( a, a + n, gia\_tri\_can\_tim)

Trả về iterator trỏ đến phần tử đầu tiên trong [first, last) không nhỏ hơn val. Nếu tất cả các phần tử nhỏ hơn val, trả về last

10\.upper\_bound( bat\_dau, end, gia\_tri\_can\_tim)

Trả về iterator đầu tiên trong [first, last) lớn hơn val. Nếu không tồn tại, trả về last

11\.memset( a, 0, sizeof(a)) : gán các phần tử của a bằng 0 hoặc -1 thôi

10\.v(s.rbegin(), s.rend())
