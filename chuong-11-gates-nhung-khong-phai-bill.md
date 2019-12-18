# Chương 11: Gates \(nhưng không phải Bill\)

Cách đây khá lâu, khi máy tính nguyên thuỷ đầu thế kỉ hai mươi chỉ là một bộ nhớ mờ đục, ai đó sẽ cho là thiết bị nhớ này có tên _cổng logic \(logic gates\)_ được đặt theo tên của nhà đồng sáng lập tập đoàn Microsoft. Không hẳn. Như ta sẽ sớm thấy, cổng logic tương đồng nhiều với cổng thông dụng cho người hay nước qua lại. Cổng logic thục hiện các tác vụ đơn giản trong logic bằng cách cản hay để dòng điện đi qua.  
Bạn sẽ nhớ lại trong chương trước mình đã đi vào cửa hàng thú cưng và nói như thế nào, "Tôi muốn một cậu mèo trắng hoặc vàng đã thiến; hoặc là một cô mèo cái tiệt sản màu gì cũng được trừ trắng; hoặc tôi sẽ lấy bất kì con mèo nào bạn có mà không phải đen." Tóm tắt cho câu nói trên bằng biểu thức:

\(M x N x \(W + T\)\) + \(F x N x \(1 - W\)\) + B

hoặc bằng mạch từ công tắc và bóng đèn:

![Screen Shot 2018-07-20 at 14.47.48](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-47-48.png)

Mạch như này đôi khi được gọi là _mạng_, ngoại trừ ngày nay thường được dùng nhiều để ám chỉ các máy tính được kết nối hơn là tập hợp chỉ mỗi công tắc. Mặc dù mạch này chẳng dùng những thứ mà không được phát minh trong thế kỷ mười chín, thế nhưng khi ấy chẳng ai cảm nhận được là biểu thức Boolean có thể được thể hiện trực tiếp từ mạch điện. Sự tương xứng này mãi tới những năm 1930 mới được khám phá, nổi bật nhất là bởi Claude Elwood Shannon \(sinh 1916\), luận văn thạc sĩ M.I.T nổi tiếng năm 1938 của ông được đặt tên "A Symbolic Analysis of Relay and Switching Circuits." \(Mười năm sau, bài viết của Shannon "The Mathematical Theory of Communication" là công bố đầu tiên dùng _bit_ để chỉ _số nhị phân_.\)  
Trước 1938, người ta biết là khi nối hai công tắc nối tiếp thì cần phải đóng cả hai công tắc thì dòng điện mới chạy qua mạch được và khi nối song song thì chỉ cần một trong hai công tắc đóng. Nhưng không ai cùng có sự sáng suốt của Shannon đó là các kĩ sư điện có thể dùng tất cả công cụ của Boolean để thiết kế mạch với công tắc. Cụ thể nếu bạn có thể tối giản các biểu thức Boolean mô tả mạng thì mạng cũng sẽ được tối giản theo.  
Ví dụ, biểu thức thể hiện đặc điểm bạn muốn con mèo của mình có:

\(M x N x \(W + T\)\) + \(F x N x \(1 - W\)\) + B

Dùng quy tắc giao hoán ta có thể sắp xếp lại các biến kết hợp bởi AND \(x\) và viết lại biểu thức:

\(N x M x \(W + T\)\) + \(N x F x \(1 - W\)\) + B

Nhằm cố làm rõ những gì tôi sẽ làm tiếp đây, hai kí hiệu mới được định nghĩa tên X và Y:

X = M x \(W + T\)  
Y = F x \(1 - W\)

Giờ biểu thức viết lại là:

\(N x X\) + \(N x Y\) + B

Bước cuối ta sẽ thay X và Y lại.  
Để ý là N xuất hiện hai lần. Dùng quy tắc phân phối ta có thể viết lại với chỉ một N:

\(N x \(X + Y\)\) + B

Giờ đặt X và Y vào lại:

\(N x \(\(M x \(W + T\)\) + \(F x \(1 - W\)\)\)\) + B

Do có nhiều ngoặc quá nên biểu thức trông có vẻ không đơn giản hơn tẹo nào. Nhưng đã có ít hơn một biến, có nghĩa là mạng cũng có ít hơn một công tắc. Phiên bản mới:  
![Screen Shot 2018-07-20 at 14.51.50](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-51-50.png)  
Thật sự thì, có lẽ là sẽ dễ nhìn thấy sư tương đồng của mạng này với mạng cũ hơn là xác minh các biểu thức như nhau.  
Thật ra vẫn còn có tới ba công tắc thừa. Theo lý thuyết, bạn chỉ cần có bốn công tắc để miêu tả con mèo. Sao lại bốn? Mỗi công tắc là một bit. Bạn có thể dùng một công tắc cho giới tính \(tắt cho đực, mở cho cái\), một công tắc khác cho khả năng sinh sản, mở cho có thể và đóng cho không thể, và thêm hai công tắc cho màu. Có bốn khả năng màu \(vàng, đen, trắng và "khác"\), ta biết là bốn lựa chọn có thể định nghĩa từ 2 bit, nên tất cả chỉ cần 2 công tắc. Ví dụ hai công tắc đóng là màu trắng, một cái mở là đen, cái kia là vàng, và mở hết cho màu khác.  
Hãy tạo một tấm điều khiển ngay để chọn mèo nào. Tấm điều khiển đơn giản là bốn công tắc \(giống với công tắc tắt/mở trên tường nhà bạn để điều khiển đèn\) và một bóng đèn gắn trong một tấm bảng.  
![Screen Shot 2018-07-20 at 14.52.30](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-52-30.png)  
Công tắc mở \(đóng\) khi được đẩy lên, và tắt \(mở\) khi xuống. Tôi sợ là hai công tắc cho màu sắc được gắn nhãn hơi khó hiểu, nhưng đó là mặt trái để tối giản tấm này: Công tắc trái của cặp gắn nhãn B; có nghĩa là công tắc trái hướng lên \(như hình\) chỉ màu đen. Công tắc phải gắn nhãn T; công tắc đó hướng xuống chỉ màu vàng. Cả hai cùng lên nghĩa là màu khác; lựa chọn này gắn nhãn là O. Cả hai cùng xuống là màu trắng, thể hiện bởi chữ W, chữ cái ở dưới.  
Trong thuật ngữ máy tính, công tắc là _thiết bị đầu vào_. Đầu vào là thông tin điều khiển cách mạch hoạt động. Trong trường hợp này, công tắc đầu vào tương ứng với 4 bit thông tin mô tả mèo. _Thiết bị đầu ra_ là bóng đèn. Đèn sáng nếu công tắc mô tả đúng con mèo. Công tắc trên bảng trước đó được thiết lập cho mèo cái màu đen còn đẻ được. Đã thoả mãn yêu cầu nên đèn sáng.  
Việc ta cần làm giờ là thiết kế mạch làm tấm điều khiển hoạt động.  
Bạn sẽ nhớ lại là luận văn của Claude Shannon có tên là "A Symbolic Analysis of Relay and Switching Circuits." Rơle ông đề cập khá giống với rơle điện báo ta gặp ở chương 6. Cùng thời điểm với bài viết của Shannon thì rơle lại được dùng cho mục đích khác, mà cụ thể là mạng lưới rộng lớn hệ thống điện thoại.  
Như công tắc, rơle có thể được nối nối tiếp hoặc song song để biểu diễn tác vụ đơn giản của logic. Những kiểu kết hợp như này của rơle được gọi là _cổng logic_. Khi tôi nói những cổng logic này biểu diễn những tác vụ đơn giản trong logic, ý tôi là đơn giản nhất có thể. Rơle có lợi thế hơn công tắc đó là rơle có thể bật tắt bằng một rơle khác chứ không nhất thiết là bằng ngón tay. Có nghĩa là cổng logic có thể kết hợp để thực hiện nhiều tác vụ phức tạp hơn, như các hàm đơn giản trong số học. Thật ra thì chương tiếp sẽ mô tả cách nối công tắc, bóng đèn, pin và rơle điện báo thành một máy cộng \(mặc dù là chỉ cộng được số nhị phân\).  
Như bạn sẽ nhớ lại, rơle là tối quan trọng với hoạt động của hệ thống điện báo. Trên một quãng đường dài, dây dẫn nối các trạm điện báo có một điện trở rất lớn. Vài phương pháp cần thiết cho việc nhận tín hiệu yếu và gửi đi tín hiệu mạnh giống cũ. Rơle làm được điều này bằng việc dùng nam châm điện điều khiển công tắc. Kết quả là, rơle _phóng đại_ tín hiệu yếu và tạo tín hiệu mạnh.  
Với mục đích của ta, ta không tập trung vô việc dùng rơle để phóng đại tín hiệu yếu. Mà vào ý tưởng một rơle có thể được điều khiển bằng nguồn điện chứ không cần ngón tay. Ta có thể nối rơle với công tắc, bóng đèn và một cặp pin như sau:  
![Screen Shot 2018-07-20 at 14.53.00](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-53-00.png)  
Để ý là công tắc trái mở và bóng đèn không sáng. Khi đóng công tắc, viên pin bên trái làm dòng điện chạy qua rất nhiều vòng quấn vanh thanh sắt. Thanh sắt nhiễm từ rồi kéo khớp nối kim loại động xuống hoàn thành mạch khiến đèn sáng:  
![Screen Shot 2018-07-20 at 14.53.43.png](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-53-43.png)  
Khi nam chậm điện kéo nối kim loại, rơle được nói là đã được _kích hoạt_. Khi công tắc tắt, thanh sắt mất từ, và nối kim loại quay trở về vị trí cũ.  
Có vẻ như đây là cách gián tiếp để bật đèn, và thực tế là vậy. Nếu ta chỉ thích làm cho đèn sáng thôi, ta có thể bỏ đi hết toàn bộ rơle. Nhưng ta lại không muốn thắp đèn. Ta có một mục tiêu xa hơn nữa kìa.  
Ta sẽ dùng tới rơle rất nhiều trong chương này \(rồi hầu như là chẳng đụng gì nữa khi tạo được cổng logic\), nên tôi muốn đơn giản sơ đồ này lại. Ta có thể bỏ bớt dây dẫn nhờ nền đất. Trong trường hợp này mặt đất đơn giản đại diện cho kết nối thông thường; không cần phải nối hẳn với bề mặt trái đất.  
![Screen Shot 2018-07-20 at 14.54.50.png](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-54-50.png)  
Tôi biết nhìn chẳng đơn giản bớt chút nào, bởi ta còn chưa xong mà. Để ý là cực âm của hai viên pin đều nối với bề mặt. Nên lúc nào ta thấy cái này  
![Screen Shot 2018-07-20 at 14.55.13.png](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-55-13.png)  
hãy thay nó bằng chữ V in hoa \(đại diện cho _điện thế_\), như ta làm trong chương 5 và 6. Giờ rơle của ta trông vầy:  
![Screen Shot 2018-07-20 at 14.56.32](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-56-32.png)  
Khi công tắc đóng, một dòng điện chảy từ V xuống đất tới các vòng dây của nam châm điện. Khiến nam châm điện kéo thanh nối động xuống. Việc này đã kết nối mạch giữa V, bóng đèn và bề mặt. Đèn sáng:  
![Screen Shot 2018-07-20 at 14.56.49](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-56-49.png)  
Những đồ hình rơle này vẽ hai nguồn điện thế và hai bề mặt, nhưng trong suốt chương này, tất cả V có thể nối với nhau và tương tự cho bề mặt. Tất cả mạng của rơle và cổng logic trong chương này và kế tiếp chỉ cần một viên pin, mặc dù có thể nó phải to lắm. Ví dụ, mạch khi nãy có thể vẽ lại với chỉ một viên pin:  
![Screen Shot 2018-07-20 at 14.57.10](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-57-10.png)  
Nhưng với những gì ta cần làm với rơle thì mạch chưa rõ ràng lắm. Tốt hơn là tránh các đường dây dẫn và nhìn vào rơle - như tấm điều khiển trước đó - theo khái niệm _đầu vào_ và _đầu ra_:  
![Screen Shot 2018-07-20 at 14.57.35](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-57-35.png)  
Nếu một dòng chạy qua đầu vào \(ví dụ, công tắc nối đầu vào với V\), nam châm điện được kích hoạt và đầu ra là một điện thế.  
Đầu vào của rơle không nhất thiết là công tắc còn đầu ra thì không nhất thiết là bóng đèn. Đầu ra của một rơle có thể là đầu vào của một rơle khác, ví dụ như sau:  
![Screen Shot 2018-07-20 at 14.58.00](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-58-00.png)  
Khi ta bật công tắc trái, rơle đầu kích hoạt, sau đó cung cấp điện thế cho rơle sau. Rơle thứ hai này được kích hoạt và đèn sáng.  
![Screen Shot 2018-07-20 at 14.58.23](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-58-23.png)  
Nối rơle là chìa khoá để dựng cổng logic.  
Thực tế, bóng đèn có thể nối với rơle theo hai cách. Để ý thanh nối động kim loại được kéo xuống bởi nam châm điện. Khi nghỉ, nó chạm vào một khớp; khi nam châm điện kéo đi, nó chạm đầu khác. Ta đang dùng khớp dưới để làm đầu ra rơle, nhưng ta cũng có thể làm vậy với khớp trên. Khi ta dùng khớp này, đầu ra của rơle bị ngược và bóng đèn sáng khi công tắc đầu vào mở.  
![Screen Shot 2018-07-20 at 14.58.51](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-58-51.png)  
Và khi công tắc đầu vào đóng, đèn tắt mất.  
![Screen Shot 2018-07-20 at 14.59.21](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-59-21.png)  
Dùng thuật ngữ công tắc, kiểu rơle này được gọi là rơle _hai tiếp điểm \(double-throw\)_. Nó có hai đầu ra ngược về điện - khi một đầu có điện đầu kia không.  
Nhân tiện, nếu bạn đang vắt óc tưởng tượng hình dạng rơle hiện đại, bạn có thể nhìn vào vài cái được gói trong suốt tiện lợi trong máy Radio Shack. Một vài, như rơle với số phần Radio Shack 275-206 và 275-214, vào khoảng cỡ một cục đá lạnh. Phần bên trong được bọc bởi một vỏ nhựa rõ, nên bạn có thể thấy được nam châm điện và nối kim loại. Mạch tôi mô tả trong chương này và chương sau dùng rơle số phần 275-240 Radio Shack, nhỏ hơn \(vào khoảng kích cỡ một nút bàn phím\) và rẻ hơn \(2.99$ một miếng\).  
Cũng như công tắc có thể nối nối tiếp, rơle cũng vậy:  
![Screen Shot 2018-07-20 at 14.59.45](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-14-59-45.png)  
Đầu ra của rơle trên cung cấp điện thế cho rơle thứ hai. Như bạn thấy, khi hai công tắc đều mở, đèn tối. Ta thử đóng công tắc trên:  
![Screen Shot 2018-07-20 at 15.00.18](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-00-18.png)  
Bóng đèn vẫn không sáng vì công tắc dưới vẫn mở và rơ le đó không được kích hoạt. Ta có thể thử mở công tắc trên và đóng công tắc dưới:  
![Screen Shot 2018-07-20 at 15.00.44](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-00-44.png)  
Đèn vẫn không sáng. Dòng điện không đi tới được đèn vì rơle trên chưa được kích hoạt. Cách duy nhất để sáng đèn là đóng cả hai công tắc:  
![Screen Shot 2018-07-20 at 15.01.02](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-01-02.png)  
Giờ hai rơle được kích hoạt và dòng điện chạy qua V, bóng đèn và mặt đất.  
Như hai công tắc nối nối tiếp, hai rơle này có thể biểu diễn một thực tế logic nhỏ. Đèn sáng chỉ khi hai rơle được kích hoạt. Hai rơle này được nối nối tiếp được gọi là _cổng AND_. Để tránh vẽ nhiều quá mỏi tay, các kĩ sư điện có một kí hiệu cho cổng AND. Như thế này:  
![Screen Shot 2018-07-20 at 15.01.22](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-01-22.png)  
Cổng đầu tiên trong bốn cổng logic. Cổng AND có hai đầu vào \(bên trái\) và một đầu ra \(bên phải\). Bạn sẽ thường thấy cổng AND được vẽ như này với đầu vào bên trái và đầu ra bên phải. Bởi vì người ta quen với viễc đọc từ trái sang phải cũng như đọc sơ đồ mạch điện. Nhưng cổng AND vẽ đầu ra trên đầu hay trái phải gì cũng ổn thôi.  
Mạch cũ với hai rơle được nối nối tiếp với hai công tắc và một bóng đèn như này:  
![Screen Shot 2018-07-20 at 15.01.44](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-01-44.png)  
Dùng kí hiệu cho cổng AND sẽ được mạch như này:  
![Screen Shot 2018-07-20 at 15.02.06](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-02-06.png)  
Để ý là kí hiệu cho cổng AND không chỉ thay thế cho mỗi hai rơle nối nối tiếp mà còn ngầm hiểu là rơle trên được nối với một nguồn điện thế, và cả hai rơle đều nối với đất. Một lần nữa, đèn chỉ sáng khi cả hai rơle trên _và_ dưới đều đóng. Đó là lí do nó được gọi là _cổng AND_.  
Đầu vào của cổng AND không nhất thiết phải nối với công tắc, và đầu ra cũng không nhất thiết phải nối với bóng đèn. Thứ ta quan tâm tới ở đây là điện thế đầu vào và đầu ra. Ví dụ, đầu ra của một cổng AND có thể là đầu vào của cổng AND khác, như này:  
![Screen Shot 2018-07-20 at 15.02.24](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-02-24.png)  
Đèn chỉ sáng khi cả ba công tắc đều đóng. Chỉ nếu khi hai công tắc trên được đóng đầu ra của cổng AND thứ nhất sẽ kích hoạt rơle đầu của cổng AND thứ hai. Công tắc dưới kích hoạt rơle thứ hai.  
Nếu ta xem không có điện thế là 0, và có là 1, đầu ra cổng AND phụ thuộc vào đầu vào như sau:  
![Screen Shot 2018-07-20 at 15.02.48](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-02-48.png)  
Cũng như hai công tắc nối nối tiếp, cổng AND có thể mô tả trong bảng sau:

| AND | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 0 | 0 |
| 1 | 0 | 1 |

Cũng có thể làm cho cổng AND có nhiều hơn hai đầu vào. Ví dụ, bạn nối ba rơle nối tiếp:  
![Screen Shot 2018-07-20 at 15.03.17](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-03-17.png)  
Đèn sáng chỉ khi cả ba công tắc đóng. Cấu hình mô tả bằng kí hiệu này:  
![Screen Shot 2018-07-20 at 15.03.40](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-03-40.png)  
Nó được gọi là cổng AND 3 đầu vào.  
Cổng logic tiếp theo gồm liên quan tới hai rơle nối song song.  
![Screen Shot 2018-07-20 at 15.03.59](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-03-59.png)  
Để ý là đầu ra của hai rơle được nối với nhau. Đầu ra chùm này sau đó cung cấp điện cho đèn. Một trong hai rơle là đủ để đèn sáng. Ví dụ, nếu ta đóng công tắc trên, đèn sáng. Đèn nhận năng lượng từ rơle trái.  
![Screen Shot 2018-07-20 at 15.04.18](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-04-18.png)  
Tương tự, nếu ta để mở công tắc trên và đóng công tắc dưới, bóng đèn sáng:  
![Screen Shot 2018-07-20 at 15.04.47](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-04-47.png)  
Đèn cũng sáng khi nếu đóng cả hai công tắc:  
![Screen Shot 2018-07-20 at 15.05.11](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-05-11.png)  
Ta có ở đây là tình huống đèn sáng nếu công tắc trên _hoặc_ dưới đóng. Từ khoá ở đây là _hoặc_, nên cổng này được gọi là _cổng OR_. Kĩ sư điện dùng kí hiệu cho cổng OR như thế này:  
![Screen Shot 2018-07-20 at 15.05.36](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-05-36.png)  
Trông nó hơi giống với kí hiệu cho cổng AND chỉ có khác là phía đầu vào tròn, giống với chữ O trong OR. \(Điều này có thể giúp bạn dễ liên tưởng hơn.\)  
Đầu ra của cổng OR được cung cấp một điện thế nếu một trong hai đầu vào có điện. Một lần nữa, nếu ta cho không có điện là 0 và có là 1 thì cổng OR có bốn trạng thái:  
![Screen Shot 2018-07-20 at 15.05.56](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-05-56.png)  
Giống với cách ta tóm tắt đầu ra cổng AND, ta có thể làm như thế với cổng OR:

| OR | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 0 | 1 |
| 1 | 1 | 1 |

Cổng OR cũng có thể có nhiều hơn 2 đầu vào. \(Đầu ra là 1 nếu bất kì đầu vào nào là 1; đầu ra là 0 chỉ khi cả hai đầu vào là 0.\)  
Khi nãy tôi có giải thích tại sao rơle mà ta dùng được gọi là rơle hai tiếp điểm vì đầu ra có thể được nối theo hai cách. Thường thì bóng đèn sẽ không sáng nếu công tắc mở:  
![Screen Shot 2018-07-20 at 15.06.23](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-06-23.png)  
Khi công tắc đóng, bóng đèn sáng:  
Thay vì vậy, bạn có thể dùng khớp nối khác để làm bóng đèn sáng khi công tắc _mở_:  
![Screen Shot 2018-07-20 at 15.06.46](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-06-46.png)  
Trong trường hợp này, đèn tắt nếu công tắc đóng. Một rơle đơn được nối theo kiểu này được gọi là _inverter\(1\)_. Inverter không phải là cổng logic \(cổng logic luôn luôn có hai đầu vào trở lên\), nhưng dù vậy nó vẫn rất có ích. Nó được đại diện bởi kí hiệu trông thế này:  
![Screen Shot 2018-07-20 at 15.07.05](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-07-05.png)  
Nó được gọi là inverter vì nó đổi 0 \(không điện thế\) thành 1 \(có điện thế\) và ngược lại:  
![Screen Shot 2018-07-20 at 15.07.27](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-07-27.png)  
Với inverter, cổng AND và cổng OR ta có thể bắt đầu nối tấm điều khiển tự động tìm mèo. Hãy bắt đầu với công tắc. Công tắc đầu đóng mèo cái và mở cho mèo đực. Do đó ta có thể tạo ra hai tín hiệu gọi là F và M, như sau:  
![Screen Shot 2018-07-20 at 15.07.42](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-07-42.png)  
Khi F là 1 M là 0 và ngược lại. Tương tự, công tắc thứ hai đóng cho mèo đã mất khả năng sinh sản và mở cho còn:  
![Screen Shot 2018-07-20 at 15.07.59](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-07-59.png)  
Hai công tắc còn lại thì phức tạp hơn tí. Trong vài kiểu kết hợp, hai công tắc này phải thể hiện được bốn màu. Đây là 2 công tắc được nối với nguồn:  
![Screen Shot 2018-07-20 at 15.08.22](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-08-22.png)  
Khi cả hai công tắc mở \(như hình\) chúng thể hiện màu trắng. Đây là cách dùng hai inverter và một cổng AND để tạo tín hiệu gọi là W, có điện \(1\) khi bạn chọn mèo trắng và không \(0\) nếu không phải:  
![Screen Shot 2018-07-20 at 15.08.46](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-08-46.png)  
Khi cả hai đều mở, đầu vào cả hai inverter là 0. Đầu ra của inverter \(là đầu vào của cổng AND\) do đó là 1. Có nghĩa là đầu ra của cổng AND là 1. Nếu một trong hai công tắc đóng, đầu ra của cổng AND là 0.  
Để biểu thị màu đen, ta đóng công tắc đầu. Dễ nhận ra là dùng một inverter và một cổng AND:  
![Screen Shot 2018-07-20 at 15.09.04](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-09-04.png)  
Đầu ra của cổng AND sẽ là 1 chỉ khi công tắc đầu đóng và công tắc sau mở.  
Tương tự nếu công tắc thứ hai đóng ta muốn mèo màu vang:  
![Screen Shot 2018-07-20 at 15.09.24](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-09-24.png)  
Và nếu cả hai công tắc đều đóng ta muốn mèo màu "khác":  
![Screen Shot 2018-07-20 at 15.09.42](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-09-42.png)  
Nào giờ hãy kết hợp bốn mạch nhỏ này thành một mạch lớn. \(Như thường, chấm đen thể hiện chỗ nối của dây dẫn; dây đi qua nhau mà không có chấm đen thì _không được nối với nhau_\):  
![Screen Shot 2018-07-20 at 15.10.01](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-10-01.png)  
Vâng, tôi biết là giờ trông cái đám dây nhợ này khá rối. Nhưng nếu bạn dõi theo thật kĩ - nếu bạn nhìn vào hai đầu vào của cổng AND và dõi từ nơi nó xuất phát mà bỏ qua hết những nơi mà nó cũng đi qua đi - bạn sẽ thấy mạch hoạt động đúng. Nếu cả hai công tắc tắt, đầu ra W là 1 và những đầu ra còn lại là 0. Nếu công tắc đầu đóng, đầu ra B là 1 và là 0 cho còn lại, tương tự cho những đầu ra khác.  
Vài quy tắc đơn giản chi phối cách ta nối cổng và inverter: Đầu ra của một cổng \(hay inverter\) có thể là đầu vào của một hay nhiều cổng \(hay inverter\) khác. Nhưng đầu ra của hai hay nhiều cổng \(hay inverter\) không bao giờ được nối với nhau.  
Mạch với bốn cổng AND và hai inverter được gọi là _bộ giải mã 2-ra-4\(2\)_. Đầu vào là 2 bit theo vài kiểu kết hợp có thể tạo ra bốn giá trị khác nhau. Đầu ra là bốn tín hiệu, chỉ có một tín hiệu là 1 tại bất kì thời điểm nào, dựa trên hai đầu vào. Theo lí thuyết tương tự, có thể tạo ra bộ giải mã 3-ra-8 hay 4-ra-16\(3\), vâng vâng.  
Phiên bản tối giản của biểu thức chọn mèo là:

\(N x \(\(M x \(W + T\)\) + \(F x \(1 - W\)\)\)\) + B

Cho mỗi dấu + trong biểu thức là một cổng OR trong mạch. Còn với mỗi dấu x là một cổng AND.  
![Screen Shot 2018-07-20 at 15.10.23](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-10-23.png)  
Kí hiệu theo thứ tự đi xuống nằm bên trái mạch được xếp theo thứ tự xuất hiện trong biểu thức. Những tín hiệu này đến từ các công tắc nối với các inverter và bộ giải mã 2-ra-4. Để ý cách dùng inverter cho \(1 - W\) của biểu thức.  
Bạn có thể thốt lên là, "Quá trời rơle thế này", và vâng, đúng vậy đấy. Có hai rơle cho mỗi một cổng AND và OR, và một cho mỗi inverter. Tôi sẽ nói một câu rất thực tế là, "Hãy tập quen dần đi." Chúng ta sẽ còn dùng nhiều hơn nữa trong những chương tới. Được cái khoẻ là bạn không cần phải mua rồi nối chúng ha.  
Ta sẽ đi vào thêm hai cổng logic nữa. Cả hai dùng đầu ra của rơle có điện khi rơle không được kích hoạt. \(Là đầu ra được dùng trong inverter.\) Ví dụ, trong cấu hình này đầu ra từ một rơle cung cấp năng lượng cho rơle khác. Với cả hai đầu vào tắt, đèn sáng:  
![Screen Shot 2018-07-20 at 15.10.46](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-10-46.png)  
Nếu công tắc trên đóng lại, đèn tắt:  
![Screen Shot 2018-07-20 at 15.11.09](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-11-09.png)  
Đèn tắt là bởi vì rơle thứ hai không còn được cung cấp điện nữa. Tương tự, nếu công tắc thứ hai đóng, đèn cúng tắt luôn:  
![Screen Shot 2018-07-20 at 15.11.32](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-11-32.png)  
Và nếu hai công tắc đều đóng thì cũng vậy:  
![Screen Shot 2018-07-20 at 15.12.02](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-12-02.png)  
Hoạt động này đối lập hoàn toàn với cổng OR. Nó được gọi là _NOT OR_, hay gọn hơn là NOR. Đây là kí hiệu cho cổng NOR:  
![Screen Shot 2018-07-20 at 15.12.32](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-12-32.png)  
Trông tương tự với cổng OR trừ điểm tròn nằm ở đầu ra. Hình tròn này nghĩa là _đảo ngược_. Cổng NOR tương đương với:  
![Screen Shot 2018-07-20 at 15.12.51](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-12-51.png)  
Đầu ra cổng NOR được thể hiện trong bảng:

| NOR | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 1 | 0 |
| 1 | 0 | 0 |

Bảng có kết quả ngược hẳn bảng OR, khi là nếu chỉ cần một đầu vào là 1 và 0 khi cả hai đầu vào là 0.  
Và còn một cách nối khác cho hai rơle là:  
![Screen Shot 2018-07-20 at 15.13.07](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-13-07.png)  
Trong trường hợp này cả hai đầu vào được nối với nhau tương tự như cổng OR trừ việc dùng khơp nối khác. Đèn sáng khi cả hai công tắc đều mở.  
Đèn vẫn sáng khi công tắc trên đóng  
![Screen Shot 2018-07-20 at 15.13.27](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-13-27.png)  
Tương tự khi công tắc dưới đóng  
![Screen Shot 2018-07-20 at 15.16.06](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-16-06.png)  
Chỉ khi cả hai công tắc đều đóng thì đèn mới ngủm:  
![Screen Shot 2018-07-20 at 15.16.31](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-16-31.png)  
Hoạt động này đối lập hoàn toàn với cổng AND. Nên được gọi là _NOT AND_, gọn hơn là NAND. Cổng NAND được vẽ giống cổng AND ngoài việc thêm hình tròn ở đầu ra, hình tròn mang nghĩa nghich với cổng AND:  
![Screen Shot 2018-07-20 at 15.16.49](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-16-49.png)  
Cổng NAND có cách hoạt động như sau:

| NAND | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 1 | 1 |
| 1 | 1 | 0 |

Để ý là đầu ra cổng NAND ngược với cổng AND. Đầu ra cho cổng AND là 1 chỉ khi cả hai đầu vào là 1; bằng không sẽ là 0.  
Tới đây, ta đã thấy là có bốn cách khác nhau để nối rơle từ hai đầu thành một đầu ra. Mỗi cấu hình hoạt động theo một cách hơi khác nhau. Để tránh vẽ đi vẽ lại rơle, ta gọi chúng là cổng logic và quyết định dùng kí hiệu như của các kĩ sư điện để đại diện chúng. Đầu ra của một cổng logic bất kì phụ thuộc vào đầu vào, được tóm tắt trong bảng sau:

| AND | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 0 | 0 |
| 1 | 0 | 1 |

| OR | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 0 | 1 |
| 1 | 1 | 1 |

| NAND | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 1 | 1 |
| 1 | 1 | 0 |

| NOR | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 1 | 0 |
| 1 | 0 | 0 |

Vậy là giờ ta có bốn cổng logic và một inverter. Nhân tố cuối cùng hoàn thành chuỗi công cụ này chỉ là một rơle bình thường cũ kĩ:  
![Screen Shot 2018-07-20 at 15.17.10](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-17-10.png)  
Đây được gọi là _buffer_, và đây là kí hiệu cho nó:  
![Screen Shot 2018-07-20 at 15.17.42](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-17-42.png)  
Tương tự với inverter nhưng không có chấm tròn.  
Ấn tượng của nó là hổng làm được gì nhiều. Đầu ra của buffer tương tự đầu vào  
![Screen Shot 2018-07-20 at 15.18.00](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-18-00.png)  
Nhưng bạn có thể dùng buffer khi tín hiệu đầu vào yếu. Bạn nhớ lại đây là lí do vì sao rơle được dùng máy điện báo nhiều năm trước. Hoặc có thể được dùng để làm trễ tín hiệu. Là bởi rơle cần thời gian để - vài phần giây - để được kích hoạt.  
Từ đây trở đi, bạn sẽ ít thấy hình vẽ rơle. Thay vào đó mạch sẽ được dựng từ buffer, inverter, bốn cổng logic cơ bản, và các mạch tinh vi hơn \(như bộ giải mã 2-ra-4\) được tạo từ những cổng logic này. Tất cả những phần tử khác này được làm từ rơle, tất nhiên rồi, nhưng ta không cần phải nhìn thấy chúng.  
Trước đó khi ta tạo bộ giải mã 2-ra-4, ta thấy một mạch nhỏ như này:  
![Screen Shot 2018-07-20 at 15.18.19](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-18-19.png)  
Hai đầu vào bị đảo điện và thành đầu vào cho cổng AND. Đôi khi cấu hình như này được vẽ mà không có inverter.  
![Screen Shot 2018-07-20 at 15.18.35](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-18-35.png)  
Để ý hình tròn nhỏ nơi đầu vào của cổng AND. Hình tròn nhỏ này có nghĩa là tín hiệu bị đảo tại điểm đó - 0 \(không điện thế\) thành 1 \(có điện thế\) và ngược lại.  
Một cổng AND với hai đầu vào bị đảo tương tự với cổng NOR:  
![Screen Shot 2018-07-20 at 15.19.16](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-19-16.png)  
Đầu ra là 1 chỉ khi cả hai đầu vào là 0.  
Tương tự, cổng OR với hai đầu vào bị đảo điện tương đương với cổng NAND:  
![Screen Shot 2018-07-20 at 15.19.29](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-19-29.png)  
Đầu ra là 0 chỉ khi cả hai đầu vào là 1.  
Hai nhóm mạch tương đồng này đại diện cho một thi triển điện của _Luật De Morgan_. Augustus De Morgan là một nhà toán học Victoria khác, lớn hơn Boole chín tuổi, cuốn sách _Formal Logic_ của ông xuất bản năm 1847, cùng ngày với \(như người đời bảo nhau\) _The Mathematical Analysis of Logic_ của Boole. Thật ra Boole có cảm hứng phát minh cổng logic từ thù hằn công khai được phát động giữa De Morgan và một nhà toán học người Anh khác về việc cáo buộc ăn cắp ý tưởng. \(De Morgan đã được minh chứng bởi lịch sử.\) Từ rất sớm, De Morgan nhận ra tầm quan trọng tầm nhìn của Boole. Ông đã động viên không ích kỉ Boole, và giúp ông một chặng, và ngày nay buồn thay hầu hết đã quên mất điều đó ngoại trừ định luật nổi tiếng của ông.  
Luật De Morgan được mô tả giản đơn thế này:  
![Screen Shot 2018-07-20 at 15.19.48](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-20-at-15-19-48.png)  
A và B là hai toán hạng Boolean. Trong biểu thức đầu, chúng bị đảo và kết hợp với toán tử AND. Tương đương với kết hợp hai toán hạng với toán tử OR rồi đảo kết quả \(NOR\). Trong biểu thức thứ hai, chúng cũng bị đảo nhưng kết hợp với toán tử OR. Lần này tương đương với kết hợp toán hạng với toán tử AND rồi đảo lại \(NAND\).  
Luật De Morgan là công cụ quan trọng để đơn giản biểu thức Boolean và do đó đơn giản hoá luôn mạch. Đã từ lâu, đây là ý nghĩa dành cho kĩ sư điện từ bài viết của Shannon. Nhưng việc tối giản mạch không phải là mối quan tâm chính trong cuốn sách này. Sẽ thú vị hơn nếu làm cho thứ gì đó hoạt động được chứ không phải là hoạt động đơn giản nhất có thể. Và thứ ta muốn khởi động tiếp theo đó là máy tính cộng.

_\(1\) Từ này mình chưa nghĩ ra từ tiếng việt nào cho hay để dùng nên mình để nguyên tiếng anh, bạn nào biết thì nhắn mình chỉnh lại nhé.  
\(2\) nguyên gốc là 2-Line-to-4-Line Decoder bạn nào dân kĩ thuật có thuật ngữ chính xác hơn nhắn mình nhé.  
\(3\) 3-Line-to-8-Line Decoder, 4-Line-to-16-Line Decoder_

