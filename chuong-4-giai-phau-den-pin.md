# Chương 4: Giải phẫu đèn pin

Đèn pin rất có ích cho nhiều việc mà trong đó đọc sách trong đêm và gửi các tin nhắn dạng mã là hai dẫn chứng rõ ràng nhất. Đèn pin gia dụng cũng có thể đóng vai chính trong một buổi kể chuyện đề tài giáo dục trên lớp về một thứ cực kỳ diệu được biết đến là điện.

Điện là một hiện tượng quái lạ, được sử dụng rộng rãi trong khi còn nhiều điều mù mờ về nó, thậm chí có một số người còn vờ như ta đây biết rõ nó hoạt động ra sao. Nhưng dù gì thì gì tôi e là chúng ta phải lăn lộn với nó thôi. Nhưng may thay, ta chỉ cần hiểu một vài khái niệm cơ bản để hiểu thấu đáo việc nó được dùng như thế nào bên trong máy tính.

Đèn pin chắc chắn là một dụng cụ điện đơn giản có ở hầu hết các gia đình. Tháo một cái đèn pin bình thường ra và bạn sẽ thấy nó bao gồm một cặp pin, một bóng đèn, một công tắt, vài mảnh kim loại, và một khung nhựa để giữ mọi thứ với nhau.

![1](https://tukhucxuan.files.wordpress.com/2016/12/1.png)

Để ý hai đầu cuối của dây dẫn phía bên phải sơ đồ. Đó là công tắc của chúng ta. Giả sử pin còn tốt và bóng đèn chưa cháy, cho hai đầu cuối này chạm vào nhau đèn sẽ sáng.

Những gì ta vừa xây dựng ở đây là một mạch điện đơn giản, và điều đầu tiên cần lưu ý đó là mạch điện là một vòng khép kín. Bóng đèn chỉ sáng khi đường đi từ pin sang dây dẫn tới bòng đèn qua công tắc rồi quay trở lại pin liền nhau. Bất cứ chỗ hở nào trên mạch sẽ không làm bóng sáng được. Mục đích của công tắc là để điều khiển quá trình này.

Tính truyền tiếp này của mạch điện gợi ra là phải có một cái gì đó chảy xung quanh mạch, có lẽ là cũng tương tự như nước chảy qua ống dẫn. Sự phân tích "nước và ống dẫn" thì khá phổ biến trong việc giải thích hoạt động của điện, nhưng cũng tới lúc cách giải thích ấy không còn đúng nữa, cũng giống như những phép so sánh khác. Điện không giống với bất cứ thứ gì trong vũ trụ và ta phải hiểu theo cách riêng của chính nó.

Kiến thức khoa học hiện hành liên quan tới hoạt động của điện được gọi là _lý thuyết điện tử \(electron theory\)_, cho rằng điện có từ sự chuyển động của các electron.

Như ta biết, tất cả vật chất - thứ ta thấy và cảm nhận \(thông thường\) - được tạo ra từ những vật cực kỳ nhỏ gọi là nguyên tử. Mỗi nguyên tử là tổ hợp của ba loại thành phần; chúng được gọi là nơtron, proton và electron. Bạn có thể hình dung nguyên tử như là một hệ mặt trời thu nhỏ với các nơtron, prôton dính chặt vào nhau tạo thành nhân cùng với các electron quay xung quanh hạt nhân như hành tinh quay quanh mặt trời:

![2](https://tukhucxuan.files.wordpress.com/2016/12/2.png)

Tôi xin nhắc các bằng là điều này không thật sự chính xác với những gì bạn thấy nếu như khả năng bạn có một cái kính hiển vi đủ mạnh có thể nhìn thấy các nguyên tử "bằng xương bằng thịt", nhưng được cái là nó như một mô hình vận hành tiện lợi.

Nguyên tử được bày ra ở trang trước có 3 electron, 3 proton và 4 nơtron và là nguyên tử lithium. Lithium là 1 trong 112 các _nguyên tố_ đã biết, mỗi một nguyên tố có một số hiệu nguyên tử trong khoảng từ 1 tới 112. Số hiệu nguyên tử của một nguyên tố biểu thị số lượng proton có trong hạt nhân của các nguyên tử trong mỗi nguyên tố và cũng \(thường\) là số lượng các electron trong mỗi nguyên tử. Số hiệu nguyên tử của lithium là 3.

Nguyên tử có thể được tổng hợp theo phương pháp hóa học với các nguyên tử khác để thành phân tử. Phân tử thường có các đặc tính khác với các nguyên tử cấu thành. Ví dụ, phân tử nước bao gồm hai nguyên tử hidro và một nguyên tử oxy \(hay H2O\). Rõ ràng nước rất khác với hidro và oxy. Tương tự, các phân tử muối gồm một nguyên tử natri và một nguyên tử clo, mà có lẽ sẽ không được ngon miệng cho lắm khi được nêm với khoai tây chiên.

Hidro, oxy, natri và clo đều là những nguyên tố. Nước và muối gọi là hợp chất. Tuy nhiên nước muối là một hỗn hợp hơn là hợp chất vì riêng nước và muỗi đều giữ các tính chất riêng của mình.

Số lượng electron trong nguyên tử thường bằng với số proton. Nhưng trong vài trường hợp cụ thể, các electron có thể bị rơi ra khỏi nguyên tử. Đó là khi điện vào cuộc chơi.

Các từ _electron_ và _electricity_ đều bắt nguồn từ ngôn ngữ Hi Lạp cổ là ηλεκτρον \(elektron\) mã có thể bạn sẽ đoán nghĩa kiểu như "một thứ vô hình tí hon". Nhưng không - ηλεκτρον thực ra là một từ Hi Lạp chỉ "hổ phách \(amber\)", là nhựa cây đông cứng trông như gương. Lý do của việc bắt nguồn kì lạ này là vì những người Hi Lạp cổ từng thử cọ sát hổ phách với len và đã làm sản sinh ra thứ mà ngay nay ta gọi là tĩnh điện. Cọ len vào hổ phách khiến len lấy đi electron trên hổ phách. Len giờ có nhiều electron hơn proton và hổ phách có ích electron hơn proton. Trong đời sống ngày nay thì giống như việc thảm lấy bớt electron từ đế giày của ta vậy.

Proton và electon có đặc tính được gọi là _điện tích_. Proton được gán điện tích dương \(+\) và electron là điện tích âm \(-\). Nơtron trung tính nên không mang điện tích. Nhưng việc chúng ta dùng dấu \(+\) và \(-\) cho proton và electron không mang nghĩa toán học và cũng không có nghĩa là proton có gì đó còn electron thì không. Việc dùng này chỉ để biểu thị cho việc proton và electron đối nghịch nhau theo một nghĩa nào đó thôi. Đặc điểm đối nghịch này tự nó thể hiện trong cách proton và electron liên quan với nhau.

Khi sóng sánh bên nhau với cùng một số hiệu thì các proton và electron đều có được hạnh phúc tột cùng với sự yên lành tột bật. Đến khi thế cân bằng bị phá vỡ thì tự chúng sẽ cố gắng cân đối cho nhau. Tấm thảm lấy đi electron từ giày của bạn thì sau cùng mọi thứ cũng cân bằng trở lại khi bạn chạm vào thứ khác và cùng lúc nhìn thấy một tia lửa. Tia lửa tĩnh điện là sự chuyển động của các electron khi đi một vòng ngoằn ngoèo từ tấm thảm qua cơ thể bạn rồi quay trở lại gót giày.

Một cách khác để mô tả mối quan hệ giữa electron và proton là chú ý vào việc các điện tích trái dấu thì hút nhau và cùng dấu thì đẩy nhau. Nhưng đó không phải là những gì ta đoán được khi nhìn vào giản đồ nguyên tử. Nó trông như là các proton chen chúc trong hạt nhân kia đang hấp dẫn lẫn nhau vậy. Các proton được giữ chặt bằng một lực nào đó còn mạnh hơn cả lực đẩy của các điện tích cùng dấu, và lực nào đó ấy được gọi là _lực tương tác mạnh \(strong force\)_. Giỡn chơi với lực tương tác mạnh trong việc chia tách các hạt nhân sẽ sản sinh ra năng lượng hạt nhân. Trong chương này, ta chỉ đùa với các electron tạo điện thôi.

Tĩnh điện không phải chỉ được giới hạn ở các tia lửa nhỏ xíu được tạo ra khi ngón tay chạm vào nắm đấm cửa. Trong cơn bão, tầng dưới các đám mây tích trữ các eletron trong khi tầng trên làm thất thoát đi; cuối cùng thế mất cân bằng được cân đối trở lại bằng một tia sét. Sét là do một đống các electron di chuyển cực nhanh từ nơi này qua nơi khác.

Điện trong mạch đèn pin rõ ràng là dễ diễn tả hơn một tia chớp. Đèn sáng đều đặn và liên tục vì các electron không phải chỉ nhảy từ chỗ này sang chỗ khác. Khi một nguyên tử trong mạch điện mất một electron cho một nguyên tử khác sát bên, chúng sẽ lấy một electron khác từ một nguyên tử liền kề rồi nguyên tử kề đó lại lấy một electron khác từ nguyên tử kề bên và cứ thế. Điện trong mạch là dòng chảy các electron giữa các nguyên tử.

Tất cả không phải đều tự xảy ra. Chúng ta không thể chỉ việc nối một đống thứ cũ kỹ và mong chờ có điện. Chúng ta cần một thứ gì đó để đẩy các electron chuyển động xung quanh mạch điện. Hãy nhìn lại giản đồ đèn pin của chúng ta, ta có thể dễ dàng giả định thứ bắt đầu cho sự chuyển động của điện không phải là đây điện cũng như bóng đèn, rất có thể đó là pin.

Hầu hết mọi người đều biết các loại pin được dùng cho đèn pin:

♥   Chúng có hình trụ và nhiều kích thước khác nhau như D, C, A, AA và AAA.

♥   Bất kể kích thước nào thì chúng đều có nhãn "1,5 volts".

♥   Một đầu viên pin phẳng có dấu trừ \(-\) in trên đó; đầu còn lại có một phần nhỏ trồi lên và được in dấu cộng \(+\).

♥   Nếu bạn muốn áp dụng đúng, thì tốt hơn hết gắn các dấu cộng của viên pin nằm đúng hướng.

♥   Dùng đã rồi thì cũng hết điện. Đôi khi chúng được sạc lại tiếp, còn không thì bỏ luôn.

♥   Và cuối cùng, ta mới ngờ ngợ là bằng một cách kì cục nào đó viên pin sản sinh ra điện.

Trong tất cả các viên pin, đều có phản ứng hóa học dự phần, có nghĩa là có những phân tử sẽ tách ra thành các phân tử khác hoặc chúng sẽ kết họp để tạo thành những phân tử mới. Các chất hóa học trong pin được lựa chọn để sao mà phản ứng giữa chúng tạo ra các electron tự do ở đầu trừ viên pin \(được gọi là cực âm hay anode a nốt\) và cần thêm các electron ở đầu bên kia \(cực dương hay cathode ca tốt\). Bằng cách này năng lượng hóa học chuyển hóa thành năng lượng điện. Phản ứng hóa học không thể xảy ra trừ khi có cách nào đó để các electron mới được giải phóng có thể được lấy đi khỏi cực âm và vận chuyển về lại cực dương. Cho nên nếu pin không được nối với bất cứ thứ gì thì sẽ chẳng có gì xảy ra \(thực ra thì phản ứng hóa học vẫn có nhưng chậm như rùa ấy\). Phản ứng xảy ra chỉ khi có một mạch điện được nối để lấy các electron từ cực âm và cung cấp chúng cho cực dương. Các electron chạy quanh mạch ngược chiều kim đồng hồ.

![3](https://tukhucxuan.files.wordpress.com/2016/12/3.png)

Trong quyển sách này, màu đỏ được dùng để diễn đạt dòng điện đang chảy qua dây dẫn.

Các electron từ các chất hóa học trong pin không thể nào dễ dàng lẫn lộn với các electron trong dây đồng nếu không vì một sự thật là: tất cả các electron bất kể là được tìm thấy ở đâu đều giống nhau. Không có cách nào để phân biệt một electron đồng với một electron của chất khác.

Để ý cả hai viên pin đều xoay cùng hướng. Cực dương của pin đứng dưới lấy electron từ cực âm của pin đứng trên như là hai viên pin được gộp lại thành một viên to hơn với một đầu dương và một đầu âm. Viên pin gộp lại thành 3 vôn hơn là 1,5 vôn so với lúc ban đầu.

Nếu ta đổi chiều một viên pin, mạch sẽ không hoạt động:

![4](https://tukhucxuan.files.wordpress.com/2016/12/4.png)

Hai đầu dương đều cần electron cho các phản ứng hóa học, thế nhưng làm sao các electron có thể đến được với chúng khi chúng dính chặt vào nhau thế kia. Nếu hai cực dương nối với nhau thì hai cực âm cũng phải vậy:

![5](https://tukhucxuan.files.wordpress.com/2016/12/5.png)

Lúc này thì hoạt động được. Các viên pin được nối _song song_ còn các viên pin được trình bày trước đó được nối _nối tiếp_. Điện thế gộp giờ là 1,5 vôn tương đương với điện thế của mỗi viên pin. Đèn có thể vẫn sáng nhưng sẽ không sáng bằng khi hai viên pin được nối tiếp. Nhưng chúng sẽ sáng lâu hơn gấp đôi.

Ta thường thích nghĩ các viên pin như là nguồn cấp điện cho mạch. Tuy nhiên ta vừa thấy rằng cũng có thể hiểu mạch như là nguồn cấp một lối đi để các phản ứng hóa học trong pin xảy ra. Mạch lấy đi các electron từ cực âm và vận chuyển chúng tới cực dương. Phản ứng đó xảy ra cho tới khi cạn hết các chất hóa học, tới đó một là sạc lại hai là ném luôn.

Từ cực âm sang cực dương viên pin, các electron chảy qua dây dẫn và bóng đèn. Thế nhưng sao ta lại cần dây dẫn? Dòng điện không thể truyền qua không khí được sao? Chà, có hay không đây. Là có, dòng điện có thể truyền qua không khí \(cụ thể là khí ẩm\) bằng không thì ta đã chẳng thấy tia sét rồi. Nhưng điện không thể đi qua không khí một cách dễ dàng được.

Một số chất thì tốt hơn đáng kể so với chất khác trong việc mang các electron. Khả năng một nguyên tố mang điện liên quan đến cấu trúc hạ nguyên tử của nó. Các electron quay xung quanh hạt nhân trong nhiều cấp, được gọi là các vỏ. Một nguyên tử chỉ có một electron ở lớp vỏ ngoài cùng có thể dễ dàng từ bỏ electron đó, đấy là điều cần thiết để mang điện được. Những chất này lợi thế trong việc mang điện và do đó được gọi là _chất dẫn điện conductors._ Chất dẫn tốt nhất là đồng, bạc và vàng. Cũng không trùng hợp gì khi chúng được tìm thấy trong cùng một cột của bảng tuần hoàn. Đồng là chất phổ biến nhất để dùng làm dây dẫn.

Đối nghịch với tính dẫn điện là _tính kháng điện resistance_. Vài chất gây trở ngại nhiều cho dòng điện truyền hơn các chất khác chúng được biết đến là _điện trở resistors._ Nếu một chất có điện trở kháng cao - nghĩa là chúng không dẫn điện tốt cho lắm - chúng được gọi là _chất cách điện insulator_. Cao su và nhựa là các chất cách điện tốt, đó là lý do tại sao chúng được dùng để bọc dây điện. Quần áo hay vải len cũng là các chất cách điện tốt khi tiết trời khô. Chỉ vài thứ sẽ dẫn được điện khi điện áp đủ cao.

Đồng có điện trở kháng rất thấp, nhưng nó vẫn có _một ít_ tính trở. Dây dẫn càng dài thì điện trở kháng càng lớn. Nếu bạn thử nối dây đèn pin với dây dẫn dài tới hàng dặm thì điện trở trong dây dẫn sẽ rất lớn và do đó đèn pin sẽ không sáng được.

Dây dẫn càng dày, điện trở kháng càng thấp. Nghe thì hơi ngược đời xíu. Bạn có thể tưởng tượng rằng một dây dẫn dày thì phải cần rất là nhiều điện để mà "lấp đầy nó". Nhưng thực ra thì độ dày dây dẫn tạo điều kiện để càng nhiều electron chạy qua.

Nãy tôi có nhắc tới điện thế mà lại chưa định nghĩa nó. Khi một viên pin có dòng chữ 1,5 vôn thì điều đó có nghĩa là gì? Thực ra thì điện áp \(voltage\) - được đặt theo tên của Count Alessandro Volta \(1745-1827\), người đầu tiên phát minh ra viên pin vào năm 1800 - là một trong những khái niệm khó nhất của điện cơ sở. Điện áp ám chỉ đến _thế năng \(potential\)_ để làm việc. Điện áp luôn tồn tại dù có hay không có thứ gì đó nối với pin.

Thử xem xét một viên gạch. Khi nằm trên bàn, viên gạch có thế năng rất thấp. Khi giữ nó trong tay bạn ở độ cao 1,2 mét \(nguyên bản là 4 feet, nhưng mình dịch ra mét luôn cho tiện, à 1 foot xấp xỉ 0,3 mét nhé\) so với mặt đất, viên gạch sẽ có nhiều thế năng hơn. Tất cả những gì bạn cần để biết là có thế năng không đó là chỉ việc thả viên gạch. Nắm nó trong tay khi ở đỉnh một tòa nhà cao tầng thì viên gạch càng có nhiều thế năng hơn nữa. Trong cả ba trường hợp đó, bạn giữ viên gạch trong tay và nó chẳng có làm gì cả, nhưng _thế năng_ lại khác nhau.

Một khái niệm dễ hình dung hơn trong điện đó là khái niệm _cường độ dòng điện_ _\(current\)_. Cường độ dòng điện liên quan tới lượng electron thật sự chạy xung quanh mạch. Cường độ dòng điện được đo bằng _ampe \(amperes\)_, được đặt theo tên của André Marie Ampère \(1775–1836\), nhưng mọi người hay đọc là _amps_, như trong "cầu chì 10-amp" \(mấy cái đọc nhanh này ở bên tiếng anh, tiếng việt mình cứ đọc ampe đi, khỏi màu mè\). Để có được cường độ 1 ampe bạn cần 6.240.000.000.000.000.000 electron chảy qua một điểm cụ thể trong một giây.

Sự phân tích ống-và-nước sẽ giúp ích ở đây: Cường độ dòng điện tương tự như _lượng_ nước chảy qua một ống. Điện thế thì tương tự như _áp lực_ nước. Điện trở thì giống với chiều dài của ống - ống càng nhỏ, điện trở càng lớn. Do đó áp lực nước càng lớn thì càng có nhiều nước chảy qua ống. Ống càng nhỏ thì có ít nước chảy qua hơn. Lượng nước chảy qua một ống \(cường độ\) tỉ lệ thuận với áp lực nước \(điện áp\) và tỉ lệ nghịch với độ gầy của ống \(điện trở\).

Trong điện, bạn có thể tính độ lớn cường độ dòng điện khi chảy qua một mạch nếu bạn biết điện áp và điện trở. Điện trở - khuynh hướng một chất cản trở dòng điện chạy - được đo bằng _ôm \(ohms\)_, đặt theo tên của Georg Simon Ohm \(1789–1854\), người đã đề xuất ra định luật Ôm nổi tiếng. Định luật chỉ ra rằng:

I = E / R

trong đó I thường được dùng để đại diện cho cường độ bằng ampe, E đại diện cho điện áp \(đại diện cho _electromotive force_\) và R là điện trở.

Ví dụ, hãy nhìn vào một viên pin đứng một mình không nối với bất cứ thứ gì:

![6](https://tukhucxuan.files.wordpress.com/2016/12/6.png)

Điện áp E bằng 1,5 vôn. Đó là thế năng để hoạt động. Nhưng vì hai cực âm dương chỉ liên kết với không khí, nên điện trở \(ký hiệu R\) là rất rất rất lớn có nghĩa là cường độ dòng điện \(I\) bằng 1,5 vôn chia cho một số cực bự. Hay cường độ chỉ vào khoảng 0 ampe.

Nào giờ hãy nối hai đầu viên pin với một cọng dây dẫn ngắn bằng đồng \(và từ đây trở đi, chất cách điện trên dây dẫn sẽ không được vẽ nữa\):

![7](https://tukhucxuan.files.wordpress.com/2016/12/7.png)

Đây được biết là một mạch điện ngắn. Điện áp vẫn là 1,5 vôn, nhưng điện trở giờ đã rất là thấp rồi. Cường độ giờ bằng 1,5 vôn chia cho một số rất nhỏ. Có nghĩa là cường độ sẽ rất rất lớn. Hàng đống hàng đống electron sẽ chảy qua dây dẫn. Trong thực tế, thì cường độ thật sẽ bị giới hạn bởi kích thước vật lý của viên pin. Pin sẽ không đủ khả năng để vận chuyển một cường độ cao như vậy, và điện áp sẽ rớt xuống dưới 1,5 vôn. Nếu viên pin đủ lớn, dây dẫn sẽ nóng lên vì điện năng được chuyển hóa thành nhiệt. Nếu dây dẫn càng nóng, nó sẽ phát sáng và thậm chí có thể tan chảy.

Đa số các mạch điện nằm ở giữa hai thái cực này. Ta có thể ký hiệu nó như sau:

![8](https://tukhucxuan.files.wordpress.com/2016/12/8.png)

Đường gãy khúc được nhận ra trong kỹ thuật điện là ký hiệu cho điện trở. Ở đây mang nghĩa là mạch điện có một điện trở không quá thấp cũng như không quá cao.

Nếu một dây dẫn có điện trở thấp, nó có thể nóng dần lên và phát sáng. Đó là cách bóng đèn hoạt động. Bóng đèn thường được ghi nhận cho nhà phát minh nổi tiếng nhất của Mỹ, Thomas Alva Edison \(1847–1931\), nhưng khái niệm đã nổi tiếng lúc ông cấp bằng sáng chế bóng đèn \(1879\) và nhiều nhà phát minh khác đương đầu với nó.

Trong bóng đèn có một dây dẫn mỏng được gọi là sợi tóc, thường được làm từ vonfram. Một đầu sợi tóc nối với tiếp nối ở phía dưới đế; đầu kia dây tóc được nối với cạnh của đế kim loại, cách biệt với tiếp nối bởi chất cách điện. Điện trở của dây làm nó nóng lên. Trong không gian bình thường, vonfram nóng tới mức bốc cháy, nhưng trong môi trường chân không trong bóng đèn, vonfram phát quang và sản sinh ánh sáng.

Đa phần các bóng đèn phổ thông có hai viên pin được nối nối tiếp. Tổng điện áp là 3 vôn. Một bóng đèn loại thông thường được sử dụng trong đèn pin có điện trở vào khoảng 4 ôm. Do đó cường độ bằng 3 vôn chia 4 ôm, hay 0,75 ampe, cũng có thể đổi thành 750 miliampe. Có nghĩa là 4.680.000.000.000.000.000 electron chảy qua bóng đèn mỗi giây.

\(Một bài kiểm tra thực tế nhỏ: Nếu bạn thật sự cố đếm điện trở của một bóng đèn pin với ôm kế, bạn sẽ nhận được con số nhỏ hơn 4 ôm. Điện trở của vonfram còn phụ thuộc vào nhiệt độ của chính nó và điện trở sẽ tăng lên khi bóng nóng lên.\)

Như bạn có thể đã biết, bóng đèn bạn mua cho sinh hoạt gia đình được gắn nhãn với một số wat nhất định. Wat được đặt theo tên của James Watt \(1736-1819\) người được biết đến nhiều nhất vì thành quả của ông trong công nghệ hơi nước. Wat là một đại lượng đo lường mức năng lượng \(P\) và có thể được tính theo công thức:

P = E x I

Đèn pin 3 vôn và 1,5 ampe của chúng ta chỉ ra rằng ta đang dùng một bóng đèn 2,25 wat.

Nhà bạn có thể được thắp sáng bởi một bóng đèn 100 wat. Chúng được thiết kế cho dòng điện gia dụng 120 vôn. Do đó, cường độ qua chúng bằng 100 wat chia cho 120 vôn hay khoảng chừng 0,83 ampe. Vì vậy, điện trở của bóng đèn 100 wat là 120 vôn chia cho 0,83 ampe hay 144 ôm.

Dường như nãy giờ ta đã phân tích mọi thứ về đèn pin rồi - pin, dây dẫn và bóng đèn. Nhưng ta lại quên mất phần quan trọng nhất!

Vâng, nó chính là công tắc. Công tắc điều khiển việc dòng điện có chạy qua mạch hay không. Khi công tắc cho phép dòng điện đi qua, được nói là _bật_ hay công tắc _đóng._ Một công tắc _tắt_ hay _mở_ không cho dòng điện chạy qua. \(Cách ta dùng từ đóng và mở cho công tắc đối nghịch với cách ta dùng chúng cho cửa. Một cánh cửa đã đóng không cho phép bất cứ thứ gì đi qua; trong khi một công tắc đóng lại cho dòng điện chạy qua\)

Công tắc có thể đóng hoặc mở. Dòng điện có thể truyền qua hoặc không. Bóng đèn có thể sáng hoặc tối. Như mã nhị phân được phát minh bởi Morse và Braille, đèn pin đơn giản có thể bật hoặc tắt. Không có giá trị nào ở giữa cả. Sự giống nhau giữa mã nhị phân và mạch điện đơn giản sẽ được chứng minh là rất có ích trong các chương tiếp theo đây.

