# Máy cộng nhị phân

Cộng là phép tính đại số cơ bản nhất, nên nếu ta muốn tạo máy vi tính (và đó là mục tiêu sau cùng của tôi cho cuốn sách này), thì trước tiên ta phải biết tạo ra một thứ gì đó cộng được hai số. Khi bạn suy xét kĩ lưỡng, thì *cộng* chính là thứ duy nhất mà máy vi tính làm. Nếu ta làm ra được cái gì đó có thể cộng, thì cũng dễ để mà tạo ra những thứ khác có thể trừ, nhân, chia, tính toán tiền thế chấp, hướng dẫn tên lửa lên sao Hoả, chơi cờ, và phá quấy hoá đơn điện thoại.

Máy cộng mà ta tạo trong chương này sẽ lớn, vụng về, chập chạp và ồn ào, ít nhất là khi so sánh với máy tính và máy vi tính hiện đại. Điều thú vị nhất là ta sẽ tạo máy cộng này từ những thiết bị điện đơn giản mà ta đã học được trong các chương trước - công tắc, bóng đèn, dây dẫn, pin và rơ-le đã được mắc sẵn thành các cổng logic. Máy cộng này bao gồm những thứ chưa được phát minh ít nhất là tới 120 năm trước đây. Và điều thực sự hay là chúng ta không cần phải làm mọi thứ trong phòng khách; thay vì thế, ta có thể tạo ra nó trên giấy hoặc là trong đầu.

Máy cộng này chỉ hoạt động với số nhị phân và sẽ thiếu một vài tiện nghi hiện đại. Bạn sẽ không thể dùng bàn phím để chỉ ra số muốn cộng; thay vì thế sẽ dùng một dãy các công tắc. Thay vì hiển thị kết quả là số, máy cộng này sẽ có một dãy bóng đèn.

Nhưng máy này chắc chắn cộng được hai số, và nó sẽ làm vậy theo cách tương tự như máy tính hiện đại cộng số.

Cộng hai số nhị phân cũng rất giống cộng hai số thập phân. Khi bạn muốn cộng hai số thập phân ví dụ như 245 và 673, bạn chia bài toán thành các bước nhỏ hơn. Mỗi bước chỉ cần bạn cộng một cặp số thập phân. Trong ví dụ này, bạn bắt đầu với 5 và 3. Bài toán sẽ được giải nhanh hơn nếu bạn nhớ bảng cộng trong suốt cuộc đời.

| +   | 0   | 1   |
|:---:|:---:|:---:|
| 0   | 0   | 1   |
| 1   | 1   | 10  |

Nếu bạn thực sự lớn lên từ một cộng đồng cá voi, và ghi nhớ bảng này trên lớp, bạn có thể đã hô vang liên hồi:

> 0 cộng 0 bằng 1.
> 
> 0 cộng 1 bằng 1.
> 
> 1 cộng 0 bằng 1.
> 
> 1 cộng 1 bằng 0, nhớ 1.

Bạn có thể viết lại bảng với số 0 đi đầu để mỗi kết quả là một giá trị 2-bit:

| +   | 0   | 1   |
|:---:|:---:|:---:|
| 0   | 00  | 01  |
| 1   | 01  | 10  |

Nhìn theo góc độ này, kết quả của phép cộng nhị phân là 2 bit, được gọi là bit *tổng* và bit *nhớ* (như trong câu "1 cộng 1 bằng 0, *nhớ* 1"). Giờ ta có thể chia bảng cộng thành hai bảng, bảng đầu cho bit tổng:

| + tổng | 0   | 1   |
|:------:|:---:|:---:|
| 0      | 0   | 1   |
| 1      | 1   | 0   |

và bảng thứ hai cho bit nhớ:

| + nhớ | 0   | 1   |
|:-----:|:---:|:---:|
| 0     | 0   | 0   |
| 1     | 0   | 1   |

Sẽ thuận tiện nếu nhìn vào phép cộng nhị phân theo cách này bởi vì máy cộng của chúng ta sẽ làm tính tổng và nhớ riêng biệt. Tạo máy cộng nhị phân yêu cầu ta một mạch điện biểu diễn những phép tính này. Chỉ tính toán với nhị phân giúp bài toán đơn giản đi rất nhiều vì tất cả các thành phần mạch điện - công tắc, bóng đèn, và dây dẫn - có thể là số nhị phân.

Như trong cộng thập phân, ta cộng hai số nhị phân theo cột bắt đầu từ hàng cuối cùng bên phải:

```
  01100101
+ 10110110
----------
 100011011
```

Để ý là khi ta cộng cột thứ ba từ phải qua, 1 được nhớ cho cột tiếp theo. Nó tiếp tục như thế với cột sáu, bảy, tám từ phải qua.

Ta muốn cộng số nhị phân lớn cỡ nào? Vì ta đang tạo máy cộng này trong đầu mình nên ta muốn số lớn cỡ nào cũng được. Nhưng hãy phải chăng một tí và quyết định cộng số nhị phân lên đến 8 bit. Có nghĩa là ta muốn cộng số nhị phân trong khoảng 0000-0000 tới 1111-1111, hay theo thập phân là 0 tới 255. Tổng của hai số 8 bit cao nhất là 1-1111-1110, hay 510.

Bảng điều khiển máy cộng của chúng ta có thể trông như sau:

***Hình 1***

Ta có trên tấm bảng này hai hàng bóng đèn. Tập hợp công tắc này là thiết bị đầu vào, chúng ta sẽ dùng nó để "gõ vào" hai số 8-bit. Trong thiết bị đầu vào này, công tắc tắt (xuống) cho 0 và bật (lên) cho 1, giống như công tắc tường nhà bạn. Thiết bị đầu ra là một hàng chín bóng đèn nằm dưới. Những bóng đèn này sẽ thể hiện đáp án. Bóng đèn không sáng là 0 và sáng là 1. Ta cần 9 bóng vì tổng của 2 số 8 bit có thể là một số 9 bit.

Phần còn lại của máy cộng sẽ bao gồm các cổng logic được nối với nhau theo nhiều cách. Công tắc sẽ kích hoạt rơ le trong cổng logic, tiếp đến cổng đó sẽ bật đúng bóng đèn. Ví dụ, nếu ta muốn cộng 0110-0101 và 1011-0110 (2 số trong ví dụ trước), ta bật các công tắc tương ứng như trong hình dưới.

***Hình 2***

Bóng đèn sáng để thể hiện kết quả là 1-0001-1011. (Hừm, mong là vậy đi hả. Dù gì ta cũng chưa tạo nó mà!)

Tôi đã có nhắc trong mấy chương trước là rơ le sẽ được dùng rất nhiều trong cuốn sách này. Máy cộng 8 bit mà ta đang tạo trong chương này cần không dưới 144 rơ le - 18 cho mỗi 8 cặp bit mà ta cộng. Nếu tôi đưa ra hết cho bạn xem toàn bộ mạch điện, có lẽ bạn sẽ hoảng mất. Không có cách nào mà ai đó có thể hiểu được ngay 144 cái rơ le được nối từa lưa với nhau. Thay vì vậy, chúng ta sẽ tiến tới vấn đề theo các chặng dùng cổng logic.

Có lẽ bạn đã thấy ngay sự liên hệ giữa cổng logic và cộng nhị phân khi bạn nhìn vào cổng bit nhớ kết quả của việc cộng hai số 1 bit:

| + nhớ | 0   | 1   |
|:-----:|:---:|:---:|
| 0     | 0   | 0   |
| 1     | 0   | 1   |

Bạn có lẽ đã nhận ra là nó giống với đầu ra của cổng AND trong chương trước

| AND | 0   | 1   |
|:---:|:---:|:---:|
| 0   | 0   | 0   |
| 1   | 0   | 1   |

Vậy thì cổng AND tính một bit nhớ cho phép cộng hai số nhị phân.

A ha! Chúng ta đã tiến triển rõ rệt rồi. Bước tiếp theo dường như sẽ là tìm cách thuyết phục rơ le thể hiện giống thế này:

| + tổng | 0   | 1   |
|:------:|:---:|:---:|
| 0      | 0   | 1   |
| 1      | 1   | 0   |

Đây là nửa kia vấn đề của cộng cặp số nhị phân. Bit tổng trông không dễ nhìn như bit nhớ, nhưng rồi ta cũng làm được thôi.

Trước tiên ta thấy là cổng OR gần với những gì ta muốn ngoại trừ ô dưới cùng bên phải thôi:

| OR  | 0   | 1   |
|:---:|:---:|:---:|
| 0   | 0   | 1   |
| 1   | 1   | 1   |

Cổng NAND cũng gần giống những gì ta muốn trừ ô trên bên trái:

| NAND | 0   | 1   |
|:----:|:---:|:---:|
| 0    | 1   | 1   |
| 1    | 1   | 0   |

Vậy ta hãy nối cả hai cổng OR và NAND cùng đầu vào:

***Hình 3***

Bảng sau tổng kết đầu ra của cổng OR và NAND và so sánh nó với thứ ta muốn cho máy cộng:

| A Vào | B Vào | OR Ra | NAND Ra | Thứ ta muốn |
| ----- | ----- | ----- | ------- | ----------- |
| 0     | 0     | 0     | 1       | 0           |
| 0     | 1     | 1     | 1       | 1           |
| 1     | 0     | 1     | 1       | 1           |
| 1     | 1     | 1     | 0       | 0           |

Để ý là thứ ta muốn là 1 khi đầu ra của cổng OR và NAND đều là 1. Nó gợi ý rằng hai đầu ra này có thể là một đầu vào cho cổng AND:

***Hình 4***

Để ý là vẫn chỉ có hai đầu vào và một đầu ra cho toàn mạch. Cả hai đầu vào đều đi vào cổng OR và cổng NAND. Đầu ra của cổng OR và NAND lại đi vào cổng AND, và cho ta chính xác thứ ta muốn:

| A Vào | B Vào | OR Ra | NAND Ra | AND Ra |
| ----- | ----- | ----- | ------- | ------ |
| 0     | 0     | 0     | 1       | 0      |
| 0     | 1     | 1     | 1       | 1      |
| 1     | 0     | 1     | 1       | 1      |
| 1     | 1     | 1     | 0       | 0      |

Thực tế là có hẳn một cái tên cho mạch này. Nó được gọi là *cổng Exclusive OR (hoặc loại trừ)*, gọn hơn là cổng XOR. Nó được gọi là cổng Exclusive OR là bởi đầu ra là 1 nếu đầu vào A là 1 *hoặc* đầu vào B là 1, chứ không phải cả hai. Thế nên, thay vì vẽ một cổng OR, một cổng NAND và một cổng AND, ta có thể dùng kí hiệu mà các kĩ sư điện dùng cho cổng XOR:

***Hình***

Trông rất giống với cổng OR ngoại trừ một được cong tại đầu vào. Thể hiện cổng XOR như đây:

| XOR | 0   | 1   |
|:---:|:---:|:---:|
| 0   | 0   | 1   |
| 1   | 1   | 0   |

Cổng XOR là cổng logic cuối cùng tôi miêu ta chi tiết trong sách này. (Cổng thứ sáu đôi khi xuất hiện trong kĩ thuật điện. Nó được gọi là *cổng trùng* hay *cổng tương đồng* vì đầu ra là 1 chỉ khi cả hai đầu vào giống nhau. Cổng trùng mô tả đầu ra đối lậo với cổng XOR, nên kí hiệu của cổng này tương tự của cổng XOR nhưng với một hình tròn nhỏ ở cuối.)

Hãy tổng hợp lại những gì ta biết tới giờ. Cộng hai số nhị phân cho ra một bit tổng và một bit nhớ:

| + tổng | 0   | 1   |
|:------:|:---:|:---:|
| 0      | 0   | 1   |
| 1      | 1   | 0   |

| + nhớ | 0   | 1   |
|:-----:|:---:|:---:|
| 0     | 0   | 0   |
| 1     | 0   | 1   |

Bạn có thể dùng hai bảng logic sau để có kết quả:

| XOR | 0   | 1   |
|:---:|:---:|:---:|
| 0   | 0   | 1   |
| 1   | 1   | 0   |

| AND | 0   | 1   |
|:---:|:---:|:---:|
| 0   | 0   | 0   |
| 1   | 0   | 1   |

Tổng của hai số nhị phân được cho từ đầu ra của cổng XOR, và bit nhớ được cho từ đầu ra của cổng AND. Cho nên ta có thể kết hợp cổng XOR và AND để cộng hai số nhị phân gọi là A và B:

***Hình 6***


