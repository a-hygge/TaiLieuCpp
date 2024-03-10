**C++ - Buổi 1**

**Kiến thức buổi 1:**

[I. Nhập xuất cơ bản trong  C++.	1](#_heading=h.gjdgxs)

[1. Các thư viện có sẵn trong C++ cho các thao tác Nhập/Xuất là:	1](#_heading=h.30j0zll)

[2. Cin, cout	2](#_heading=h.1fob9te)

[II. Độ phức tạp của thuật toán ( Big – O )	4](#_heading=h.3znysh7)

[1. Định nghĩa :	4](#_heading=h.2et92p0)

[2. Quy trình chung cho phân tích thời gian chạy Big-O:	4](#_heading=h.tyjcwt)

[III. Tìm hiểu về vector trong thư viện STL	6](#_heading=h.3dy6vkm)

[1. Cú pháp :	6](#_heading=h.4d34og8)

[2. Các hàm thường sử dụng trong VECTOR :	6](#_heading=h.2s8eyo1)

[3. Truy cập phần tử:	7](#_heading=h.17dp8vu)

[IV. Tìm hiểu biến lặp (iterator) và vòng lặp for – each	8](#_heading=h.3rdcrjn)

[0. Từ khóa auto	8](#_heading=h.26in1rg)

[1. Vòng lặp for - each	9](#_heading=h.lnxbz9)

[2. Biến lặp (iterator)	11](#_heading=h.1ksv4uv)

By : Nguyễn Thị Tú Anh

<a name="_heading=h.gjdgxs"></a>[**I. Nhập xuất cơ bản](#_heading=h.44sinio) **trong  C++.**

<a name="_heading=h.30j0zll"></a>**1. Các thư viện có sẵn trong C++ cho các thao tác Nhập/Xuất là:**

1. **iostream** : thư viện chuẩn của đầu vào-đầu ra. Thư viện này chứa định nghĩa của các đối tượng như cin, cout, cerr,...
1. **iomanip** : iomanip là viết tắt của bộ điều khiển đầu vào-đầu ra. Tệp này chứa các định nghĩa về setw, setprecision(Đặt độ chính xác thập phân),...
1. **fstream** : Thư viện fstream cung cấp cho lập trình viên C++ 3 class hoạt động cùng với file
1. Ofstream: Đại diện cho stream đầu ra. Nó dùng cho việc tạo và ghi thông tin vào file.
1. Ifstream: Đại diện cho stream đầu vào, được dùng để đọc thông tin từ file dữ liệu.
1. Fstream: Đại diện cho một stream file, có cả tính năng của ofstream/ifstream. Như vậy, nó vừa có khả năng tạo, viết, đọc dữ liệu trong file.

Để thực hiện tiến trình xử lý file trong C++, bạn bao các header file là <iostream> và <fstream> trong source file của chương trình C++ của bạn.

1. [**bits/stdc++.h:](https://www.geeksforgeeks.org/bitsstdc-h-c/#:~:text=C%2FC%2B%2B-,%3Cbits%2Fstdc%2B%2B.,h%3E%20in%20C%2B%2B&text=It%20is%20basically%20a%20header,your%20rank%20is%20time%20sensitive.)** Tệp tiêu đề này bao gồm mọi thư viện chuẩn. 

` `Trong C++ sau các tệp tiêu đề, chúng ta thường sử dụng **' *using namespace std;* '**. Vì tất cả các định nghĩa thư viện tiêu chuẩn đều nằm trong không gian tên std.Khi đó, ta không cần viết STD:: ở mọi dòng (ví dụ: STD::cout,...).

<a name="_heading=h.1fob9te"></a>**2. Cin, cout**

- C**out** và **cin trong C++**  của lớp iostream được sử dụng rất thường xuyên để in đầu ra và lấy đầu vào tương ứng. 
- **Câu lệnh cout** trong C++ là thể hiện của class ostream. Nó được sử dụng để tạo đầu ra trên thiết bị đầu ra tiêu chuẩn (thường là màn hình hiển thị). Dữ liệu cần hiển thị trên màn hình được chèn vào đầu ra tiêu chuẩn (cout) bằng cách sử dụng toán tử chèn ( **<<** ).

**Ví dụ:**

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.001.png)

**Đầu ra:**

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.002.png)

**Độ phức tạp thời gian:** O(1)

**Lệnh endl :** dùng để xuống dòng mới.

- **Câu lệnh cin** trong C++ là thể hiện của class istream. Nó được sử dụng để đọc đầu vào từ thiết bị đầu vào tiêu chuẩn (thường là bàn phím). Toán tử trích xuất ( >> ) được sử dụng cùng cin để đọc đầu vào.

**Đầu vào :**

18

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.003.png)

**Đầu ra:**

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.004.png)

**Độ phức tạp thời gian:** O(1)

- **Lệnh lỗi tiêu chuẩn không được đệm (cerr)** : C++ cerr là luồng lỗi tiêu chuẩn được sử dụng để xuất lỗi. Đây cũng là một thể hiện của lớp iostream. Vì cerr trong C++ không có bộ đệm nên nó được sử dụng khi cần hiển thị thông báo lỗi ngay lập tức. Nó không có bất kỳ bộ đệm nào để lưu thông báo lỗi .
  1. Sự khác biệt chính giữa cerr và cout xuất hiện khi bạn muốn chuyển hướng đầu ra bằng cách sử dụng “cout” sẽ được chuyển hướng đến tệp ,nếu bạn sử dụng “cerr” thì lỗi sẽ không được lưu trong tệp. (Đây là ý nghĩa của việc không lưu vào bộ đệm .. Nó không thể lưu trữ tin nhắn)

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.005.png)

**Đầu ra:**

Da xay ra loi

**Độ phức tạp thời gian:** O(1)

- **Lệnh lỗi tiêu chuẩn được đệm (clog)** : Đây cũng là một thể hiện của lớp ostream và được sử dụng để hiển thị lỗi nhưng không giống như cerr, lỗi đầu tiên được chèn vào bộ đệm và được lưu trữ trong bộ đệm cho đến khi nó không được lấp đầy. hoặc bộ đệm không được xóa rõ ràng (sử dụng flush()). Thông báo lỗi cũng sẽ được hiển thị trên màn hình.

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.006.png)

**Đầu ra:**

Da xay ra loi

**Độ phức tạp thời gian:** O(1)

<a name="_heading=h.3znysh7"></a>**II. Độ phức tạp của thuật toán ( Big – O )**

<a name="_heading=h.2et92p0"></a>**1. Định nghĩa :** 

Cho g và f là các hàm số từ tập hợp các số tự nhiên đến chính nó. Hàm f được gọi là O(g) (đọc là big-oh của g), nếu tồn tại một hằng số <b>c > 0</b> và một số tự nhiên <b>n <sub>0</sub></b> sao cho f(n) ≤ cg(n) với mọi n ≥ n <sub>0</sub> .

<a name="_heading=h.tyjcwt"></a>**2. Quy trình chung cho phân tích thời gian chạy Big-O:**  

1. Tìm hiểu đầu vào là gì và n đại diện cho cái gì.
1. Biểu thị số phép toán tối đa, thuật toán thực hiện theo n.
1. Loại các điều kiện ít quan trọng hơn.
1. Loại bỏ các hằng số.

❖Một số kết quả Big-O quan trọng: 

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.007.png)

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.008.png)

Ví dụ:

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.009.png)

Ở đây thời gian chạy của chúng ta là O(n + n <sup>2</sup> )  nhưng chúng ta sẽ gọi là O(n <sup>2</sup> ).

Tham khảo thêm tại : <https://developerinsider.co/big-o-notation-explained-with-examples/>

<a name="_heading=h.3dy6vkm"></a>**III. Tìm hiểu về vector trong thư viện STL**

Các vector giống như các mảng động với khả năng tự động thay đổi kích thước khi một phần tử được chèn hoặc xóa, với bộ nhớ của chúng được xử lý tự động bởi bộ chứa. 

<a name="_heading=h.1t3h5sf"></a>Khi nào nên sử dụng một Vector?

- Khi xử lý các yếu tố dữ liệu thay đổi nhất quán.
- Nếu kích thước của dữ liệu không được biết trước khi bắt đầu, vectơ sẽ không yêu cầu bạn đặt kích thước tối đa của vùng chứa.

Để sử dụng vector ta cần #include <vector>  hoặc sử dụng luôn #include <bits/stdc++.h>

<a name="_heading=h.4d34og8"></a>**1. Cú pháp :** 

- Cách 1: vector < kiểu dữ liệu >  name;
- Cách 2: vector < kiểu dữ liệu >  name( size );
- Cách 3: vector < kiểu dữ liệu >  vector A( vector B );

<a name="_heading=h.2s8eyo1"></a>**2. Các hàm thường sử dụng trong VECTOR :**

1. Trả về vị trí tham chiếu tới ... vector
   1. Đầu: vt.begin()
   1. Sau phần tử cuối: vt.end() // hoặc vt.begin() + vt.size()
1. Thêm phần tử
   1. Cách 1: vt.push\_back(value); //thêm phần tử vào cuối của vector
   1. Cách 2: vt[pos] = value; //gán giá trị như mảng
1. Chèn
   1. ` `vt.insert(pos, value); //chèn value vào vị trí pos
1. Xóa phần tử
   1. Cách 1: vt.pop\_back(); //xóa phần tử cuối của vector
   1. Cách 2: vt.erase(pos); //xóa 1 phần tử ở vị trí pos
   1. Cách 3: vt.erase(first , last); //xóa phần tử từ vị trí first tới last
   1. Cách 4: vt.clear(); //xóa tất cả phần tử trong vector
1. Lấy số lượng phần tử
   1. vt.size();
1. Lấy phần tử
   1. Cách 1: vt[pos] // truy cập trực tiếp vị trí pos (tính từ 0)
   1. Cách 2: vt.front(); //lấy phần tử đầu vector
   1. Cách 3: vt.back(); //lấy phần tử cuối vector
   1. Cách 4: vt.at(pos); lấy phần tử vị trí pos (tính từ 0)
1. Kiểm tra vector rỗng
   1. vt.empty();
1. Sắp xếp theo thứ tự tăng dần
   1. sort(first, last); // sắp xếp từ vị trí first tới last

      Ví dụ 1: sort(vt.begin(), vt.end()); //sắp xếp cả mảng

      Ví dụ 2: sort(vt.begin()+2, vt.begin()+5); //sắp xếp các phần tử từ vị trí 2 tới 5

1. Tìm kiếm
   1. Cách 1: find  
   1. Cách 2: search  
1. Đảo ngược  
   1. reverse(first, last);

      Ví dụ 1: reverse(vt.begin(), vt.end());  //đảo ngược cả vector 

      Ví dụ 2: reverse(vt.begin(), vt.begin()+2); //đảo ngược từ vị trí đầu tới vị trí đầu +2;

1. Đổi 2 vector
   1. swap(vta, vtb); //tất cả các phần tử của vta được gán cho vtb và ngược lại

<a name="_heading=h.17dp8vu"></a>**3. Truy cập phần tử:**

1. vt[g] – Trả về tham chiếu đến phần tử ở vị trí 'g' trong vectơ
1. vt.at(g) – Trả về tham chiếu đến phần tử ở vị trí 'g' trong vectơ
1. vt.font() – Trả về một tham chiếu đến phần tử đầu tiên trong vector
1. vt.back() – Trả về một tham chiếu đến phần tử cuối cùng trong vector
1. vt.data() – Trả về một con trỏ trực tiếp tới mảng bộ nhớ được vectơ sử dụng bên trong để lưu trữ các phần tử thuộc sở hữu của nó.

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.010.png)

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.011.png)

**Độ phức tạp về thời gian để thực hiện các thao tác khác nhau trên vectơ là :**

- Truy cập ngẫu nhiên – hằng số O(1)
- Chèn hoặc loại bỏ các phần tử ở cuối – hằng số O(1)
- Chèn hoặc loại bỏ các phần tử – tuyến tính trong khoảng cách đến cuối vectơ O(N)
- Biết độ lớn – hằng số O(1)
- Thay đổi kích thước của vectơ- Tuyến tính O(N)

<a name="_heading=h.3rdcrjn"></a>**IV. Tìm hiểu biến lặp (iterator) và vòng lặp for – each**

<a name="_heading=h.26in1rg"></a>**0. Từ khóa auto**

- Ý nghĩa : tự động nhận dạng kiểu dữ liệu thông qua kiểu dữ liệu của giá trị khởi tạo ra nó.

***Lưu ý:** Biến được khai báo với từ khóa auto chỉ được khởi tạo tại thời điểm khai báo, nếu không sẽ xảy ra lỗi khi biên dịch.* 

- Bạn có thể xem kiểu dữ liệu của biến khi sử dụng từ khóa auto thông qua hàm **typeid( ten\_bien ).name()**.

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.012.png)

- Từ khóa auto có thể được dùng cho giá trị trả về của 1 hàm:

Đối với những kiểu dữ liệu cơ bản, có thể bạn thấy từ khóa **auto** này chưa cần thiết. Trong tương lai, bạn sẽ gặp những kiểu dữ liệu khá **phức tạp** và **dài dòng**, lúc này sử dụng từ khóa auto sẽ **tiết kiệm thời gian**, và giúp code trở nên **đẹp** hơn.

**Từ khóa auto không thể sử dụng làm tham số hàm**

<a name="_heading=h.lnxbz9"></a>**1. Vòng lặp for - each**

<a name="_heading=h.35nkun2"></a>**For-each loop** được sử dụng để lặp qua các phần tử trên 1 mảng (hoặc các cấu trúc danh sách khác như **vector**, **linked lists**, **trees**, và **maps**).

-----
Cú pháp vòng lặp for-each

**for** (**element\_declaration** : **array**)

{

`	`Khối lệnh;

}                

Trong đó:

**element\_declaration**: là một khai báo biến hoặc tham chiếu có kiểu trùng với kiểu của các phần tử trong array. Thường sử dụng từ khóa auto.

**Ví dụ:** sử dụng **for-each loop** để truy cập vào từng phần tử của mảng:

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.013.png)

Trong chương trình trên, vòng lặp **for-each** sẽ lặp qua từng phần tử trong mảng **a**, gán giá trị phần tử hiện tại vào biến **x**. 

**Chú ý:** Biến **element\_declaration** đại diện cho phần tử của **array** ở vòng lặp hiện tại, **không phải** là chỉ số của **array**.

Vòng lặp for-each và từ khóa auto

Vì biến nên có cùng kiểu dữ liệu với phần tử trong mảng, nên cách tốt nhất là sử dụng từ khóa **auto** để khai báo. **Compiler** sẽ tự dộng xác định kiểu cho biến.

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.014.png)

Vòng lặp for-each và tham chiếu

Sử dụng biến tham chiếu cho vòng lặp for-each giúp CPU **truy cập trực tiếp** vào phần tử của mảng, không mất thời gian và vùng nhớ để **khởi tạo bản sao** cho biến. Tuy nhiên, tham chiếu có thể làm **thay đổi giá trị** của phần tử mảng.

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.015.png)

Trường hợp không muốn thay đổi giá trị của phần tử trong mảng, bạn có thể sử dụng **tham chiếu hằng (const reference)**.

Vòng lặp for-each không làm việc với con trỏ mảng

Để lặp qua 1 mảng, vòng lặp **for-each** phải biết được kích thước của mảng đó. Con trỏ đến 1 mảng không cho biết kích thước của mảng đó, nên vòng lặp for-each sẽ không làm việc.

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.016.png)

Xem chỉ số phần tử hiện tại trong vòng lặp for-each?

Vòng lặp **for-each** **không** cung cấp phương thức trực tiếp nào để xem được chỉ số phần tử hiện tại. Với những yêu cầu liên quan đến chỉ số phần tử, bạn có thể sử dụng [**VÒNG LẶP FOR TRONG C++**](http://www.howkteam.vn/course/khoa-hoc-lap-trinh-c-can-ban/vong-lap-for-trong-c-for-statements-1372) .

<a name="_heading=h.1ksv4uv"></a>**2. Biến lặp (iterator)**

Iterator được sử dụng để trỏ đến địa chỉ bộ nhớ của bộ chứa [STL](https://www.geeksforgeeks.org/the-c-standard-template-library-stl/) . Chúng chủ yếu được sử dụng trong các dãy số, ký tự, v.v. Chúng làm giảm độ phức tạp và thời gian thực hiện chương trình.

Thuộc thư viện : #include<iterator>

Với mỗi container class chúng ta sẽ có một kiểu iterator tương ứng. Mình sẽ lấy ví dụ về iterator của class std::vector như sau:

Cú pháp : vector < int >::iterator it;

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.017.png)

Các bạn có thể hình dùng Iterator giống như một con trỏ trỏ đến một phần tử nào đó bên trong container với một số toán tử đã được định nghĩa:

- \*it và trả về giá trị bên trong container tại vị trí mà iterator được đặt.
- it++ di chuyển iterator đến phần tử tiếp theo trong container.
- it-- ngược lại so với it++.
- it == và it != dùng để so sánh vị trí tương đối của 2 phần tử đang được trỏ đến bởi 2 iterator.
- it = dùng để gán vị trí mà iterator trỏ đến.

Và những container có chứa định nghĩa class iterator sẽ có những phương thức trả về giá trị kiểu iterator tương ứng:

- begin() trả về một iterator đại diện cho vị trí của phần tử đầu tiên trong container.
- end() trả về một iterator đại diện cho vị trí đứng ngay sau phần tử cuối cùng trong container.
- cbegin() trả về một hằng (read-only) iterator đại diện cho vị trí của phần tử đầu tiên trong container.
- cend() trả về một hằng (read-only) iterator đại diện cho vị trí đứng ngay sau phần tử cuối cùng trong container.

![](Aspose.Words.6a10c234-0ab3-4107-b35b-8f270a9234f5.018.png)
