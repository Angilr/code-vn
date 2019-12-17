# Chương 2: Mã và những sự kết hợp

Mã Morse được phát minh bởi Samuel Finley Breese Morse \(1791-1872\), ta có thể sẽ gặp ông nhiều hơn ở các chương sau. Mã Morse ra đời cùng lúc với phát minh ra máy điện báo, tí nữa chúng ta sẽ nói kỹ hơn về phát minh này. Cũng như mã Morse đã cho ta một chỉ dẫn tốt về tính chất của mã, máy điện báo cũng là một bản hướng dẫn tốt về phần cứng máy tính.

Đa phần thì mọi người nghĩ mã Morse gửi đi dễ hơn là nhận. Đến nỗi mà bạn không cần thiết phải nhớ mã, đơn giản chỉ cần dùng bảng này, đã được xếp rất tiện theo thứ tự bảng chữ cái:

![](https://tukhucxuan.files.wordpress.com/2016/11/11.png)

Nhận và dịch mã Morse thành chữ khó hơn và tốn thời gian đáng kể so với gửi bởi bạn phải làm ngược lại để tìm ra chữ cái ứng với chuỗi mã cụ thể. Ví dụ, nếu bạn nhận ngang-chấm-ngang-ngang, bạn phải rà từng chữ từng chữ một trên bảng để mà tìm ra chữ Y cho mã đó.

Vấn đề ở chỗ ta có một bảng giúp dịch theo kiểu:

_Chữ cái theo thứ tự trong bảng chữ cái → Chấm và ngang của mã Morse_

Nhưng ta lại không có bảng giúp làm ngược lại:

_Chấm và ngang của mã Morse → Chữ cái theo thứ tự trong bảng chữ cái_

Khi mới bắt đầu học mã Morse thì một bảng như thế này chắc chắn sẽ rất tiện lợi. Tuy nhiên việc tạo ra nó lại không được rõ ràng cho lắm. Làm sao có thể xếp những chấm và ngang theo thứ tự bảng chữ cái.

Vậy nên hãy quên cái thứ tự đó đi. Có lẽ một cách tốt hơn để tổ chức đám mã này là nhóm chúng dựa theo số lượng chấm và ngang. Ví dụ, một chuỗi mã Morse chứa một chấm hoặc một ngang chỉ có thể biểu thị cho hai chữ cái, là E và T:

![](https://tukhucxuan.files.wordpress.com/2016/11/21.png)

Một sự kết hợp chuẩn xác hai chấm hoặc hai ngang cho ta bốn chữ nữa - I, A, N và M:

![](https://tukhucxuan.files.wordpress.com/2016/11/31.png)

Một tổ hợp của ba chấm hoặc ngang cho ta thêm tám chữ:

![](https://tukhucxuan.files.wordpress.com/2016/11/41.png)

Và cuối cùng \(nếu như ta muốn dừng bài kiểm tra này trước khi chơi với số và dấu\), chuỗi bốn chấm hay ngang cho ta thêm 16 ký tự:

![](https://tukhucxuan.files.wordpress.com/2016/11/5.png)

Cùng với nhau, bốn bảng này có 2 cộng 4 cộng 8 cộng 16 mã cho tổng cộng 30 ký tự, 4 chữ được thêm vào dùng cho 26 chữ cái trong bảng chữ cái Latin. Vì thế, bạn thấy thêm 4 mã trong bảng cuối là cho những chữ cái có dấu.

Với bốn bảng này sẽ giúp bạn dễ dàng hơn cho việc dịch khi có ai gửi mã Morse cho bạn. Sau khi nhận một mã cho một chữ cái cụ thể, bạn biết có bao nhiêu chấm và ngang trong đó để ít nhất bạn có thể tới đúng bảng mà tìm. Mỗi bảng đều được tổ chức theo kiểu mã toàn chấm ở trên bên trái và mã toàn ngang ở dưới bên phải.

Bạn có thấy một mẫu hình kích thước của bốn bảng? Để ý mỗi bảng đều nhiều hơn hai lần so với số mã bảng trước nó. Có nghĩa là: Mỗi bảng có tất cả các mã ở bảng trước thêm vào trước một dấu chấm hoặc ngang.

Ta có thể tóm tắt khuynh hướng thú vị này như sau:

![](https://tukhucxuan.files.wordpress.com/2016/11/6.png)

Mỗi bảng có nhiều hơn hai lẫn mã Morse so với bảng trước nó, nên nếu bảng đầu có 2 mã thì bảng thứ hai có 2 x 2 mã, và bảng thứ ba có 2 x 2 x 2 mã. Cách khác để mô phỏng là:

![](https://tukhucxuan.files.wordpress.com/2016/11/7.png)

Tất nhiên, khi một số nhân với chính nó, ta có thể dùng số mũ để biểu thị lũy thừa. Ví dụ, 2 x 2 x 2 x 2 có thể viết lại là 2^4 \(2 lũy thừa 4\). Các số 2, 4, 8 và 16 đều là lũy thừa của 2 bởi bạn có thể tính ra nó bằng cách nhân 2 với chính nó. Nên bảng tóm tắt có thể thành:

![](https://tukhucxuan.files.wordpress.com/2016/11/8.png)

Bảng này trở nên rất đơn giản. Số lượng mã đơn giản chỉ là 2 lũy thừa với số chấm và ngang. Có thể thu gọn bảng trên thành công thức đơn giản:

_số lượng mã = 2^số lượng chấm và ngang_

Lũy thừa 2 sẽ tạo ra rất nhiều mã, ta sẽ xem các ví dụ khác ở chương tới.

Để làm cho quá trình giãi mã Morse dễ dàng hơn, có thể ta sẽ muốn vẽ một cái gì đó đại loại như bảng dạng cây được mô phỏng dưới đây.

![](https://tukhucxuan.files.wordpress.com/2016/11/9.png)

Bảng này thể hiện các chữ cái tương ứng với mỗi trình tự liên tiếp cụ thể của các chấm và ngang. Để giải mã trình tự nào đó, hãy cứ theo hướng mũi tên từ trái qua phải. Giả sử bạn muốn biết chữ cái nào ứng với mã chấm-ngang-chấm. Bạn bắt đầu từ bên trái và chọn dấu chấm; sau đó tiếp tục sang phải theo đường mũi tên rồi chọn dấu ngang rồi một dấu chấm nữa. Chữ cái cần tìm là R,  đứng kế bên dấu chấm cuối cùng.

Nếu bạn nghĩ thế, lúc đầu có lẽ xây dựng một bảng như vậy là cần thiết cho việc xác định mã Morse. Trước tiên, nó đảm bảo rằng bạn không mắc phải những lỗi ngu ngơ như dùng một mã cho hai chữ cái khác nhau! Thứ hai, bạn có thể đảm bảo dùng tất cả các mã có nghĩa mà không tạo ra các chuỗi chấm ngang dài không cần thiết.

Nguy cơ từ việc mở rộng bảng này đến từ giới hạn các trang in, bạn có thể tiếp tục nó với những mã có năm chấm hay ngang hoặc nhiều hơn. Một trình tự chuẩn xác năm chấm và ngang cho ta thêm 32 mã \(2 x 2 x 2 x 2 x 2, hay 2^5\). Thường thì 10 chữ số và 16 ký tự dấu được dịch trong mã Morse là đã đủ, và thật ra các chữ số được mã hóa với 5 chấm và ngang. Tuy nhiên còn nhiều chuỗi năm chấm và ngang khác đại diện cho các chữ có dấu so với các dấu câu.

Muốn có thêm mấy dấu chấm câu thì hệ thống phải được mở rộng ra sáu chấm và ngang, khi đó ta có thêm 64 \(2 x 2 x 2 x 2 x 2 x 2 hay 2^6\) mã để được một tổng lên đến 2 + 4 + 8 + 16 + 32 + 64 hay 126 ký tự. Khi đó sẽ quá tải cho mã Morse, sẽ có thêm nhiều mã "chưa xác định \(undefined\)" dài thòng. Từ _chưa xác định_ được dùng ở đây để ám chỉ một mã không có nghĩa \(không đại diện cho ký tự nào hết\). Nếu bạn đang nhận mã Morse mà có một mã chưa xác định trong đó thì khác chắc chắn là ai đó mắc lỗi rồi.

Bời vì ta đủ thông minh để triển khai công thức nhỏ này,

_số lượng mã = 2^số lượng chấm và ngang_

ta có thể tiếp tục tính ra bao nhiêu mã nhận được khi dùng những chuỗi chấm ngang dài hơn:

![](https://tukhucxuan.files.wordpress.com/2016/11/10.png)

May mắn thay, ta không phải viết ra hết tất cả các mã có thể có để xác định số lượng bao nhiêu. Việc ta cần làm chỉ là tăng số lần nhân 2 với chính nó lên.

Mã Morse được gọi là mã _nhị phân_ \(nghĩa đen là _hai lần hai - two by two_\) vì những phần tử của mã chỉ gồm hai thứ - một chấm và một ngang. Cũng tương tự như đồng xu, khi đáp đất cũng chỉ hiện mặt sấp hoặc ngửa. Các vật thể nhị phân \(như đồng xu\) và mã nhị phân \(như mã Morse\) luôn được mô tả bởi lũy thừa hai.

Những gì ta đang đang làm bằng việc phân tích mã nhị phân là một bài tập đơn giản trong nhánh toán học được biết đến là _tổ hợp \(combinatorics\)_ hay _phân tích tổ hợp \(combinatorial analysis\)._ Lệ thường, phân tích tổ hợp thường được dùng nhiều trong lĩnh vực xác suất và thống kê vì nó liên quan tới việc xác định số cách mà một vật, như đồng xu hay xúc xắc chẳng hạn, có thể xảy ra. Nhưng cũng nhờ nó mà ta sẽ hiểu mã được kết hợp và tháo ra như thế nào.

