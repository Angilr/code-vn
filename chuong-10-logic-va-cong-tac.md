# Chương 10 - Logic và công tắc

Chân lý là gì? Aristotle cho rằng logic có liên quan đến nó. Tuyển tập các bài giảng của ông được biết đến với cái tên _Organon_ \(thế kỉ thứ tư trước CN\) là những bài viết sâu về đề tài logic sớm nhất. Với người Hi Lạp cổ, logic là phương tiện phân tích ngôn ngữ cho việc truy tìm chân lý do đó được xem là một dạng triết học. Nền tảng logic của Aristotle là _tam đoạn luận_. Tam đoạn luận nổi tiếng nhất \(thực tế không được tìm thấy trong công trình của Aristotle\) là

_Tất cả mọi người đều sẽ chết;  
Socrates là người;  
Do đó, Socrates sẽ chết._

Trong một tam đoạn luận, hai tiền đề được giả định là đúng, rồi từ đó rút ra được kết luận.  
Tính khả tử của Socrates có vẻ dễ hiểu, nhưng ngoài kia còn nhiều kiểu tam đoạn luận nữa. Ví dụ, xem xét hai tiền đề sau đây, được đề xướng bởi nhà toán học thế kỉ mười chín Charles Dogson \(còn được biết tới là Lewis Carroll\):

_Tất cả triết gia đều lý luận  
Một người vô lý thì lúc nào cũng cứng đầu._

Kết luận không được rõ ràng lắm. \(Nó là "Vài người cứng đầu thì không phải là triết gia." Để ý chữ "vài" tự nhiên xuất hiện.\)  
Đã hai ngàn năm trôi qua, các nhà toán học vẫn đang vật lộn với logic của Aristotle, cố ghém nó lại chỉ với các ký tự và phép toán. Trước thế kỷ mười chín, người duy nhất đến được gần là Gottfried Wilhelm von Leibniz \(1648-1716\), người đã thử chơi với logic khi còn trẻ nhưng sau lại chuyện sang thú vui khác \(như độc lập phát minh ra máy tính cùng thời điểm với Newton\).  
Rồi đến George Boole.

![Screen Shot 2018-07-14 at 23.26.08.png](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-14-at-23-26-08.png)  
George Boole sinh ra ở Anh vào năm 1815 vào một thế giới mà chắc hẳn ông sẽ khó mà thành đạt. Bởi ông là con của một thợ đóng giày và người hầu. Giai tầng cứng nhắc của Anh thường sẽ ngăn Boole đạt được bất cứ thứ gì khác với tổ tiên của mình. Nhưng nhờ trí tò mò và người cha tận tình \(người có sở thích lớn với toán học, khoa học và văn học\), chàng George trẻ tuổi tự cho mình một kiểu giáo dục đặc quyền của tầng lớp trên; cậu học cả tiếng Latin, Hi Lạp và toán. Kết quả từ các bài viết sớm về toán học là vào năm 1849 Boole được chỉ làm Giáo Sư toán đầu tiên của Queen's College, ở Cork, Ireland.  
Vài nhà toán học giữa thế kỉ thứ mười chín đang tìm định nghĩa toán học của logic \(nổi bật nhất là Augustus De Morgan\), nhưng Boole mới là người đầu tiên có khám phá lý thuyết, đầu tiên là trong cuốn sách ngắn _The Mathematical Analysis of Logic, Being an Essay Towards a Calculus of Deductive Reasoning_ \(1847\) và rất lâu sau với những con chữ đầy khát vọng, _An Investigation of the Law of Thought on Which Are Founded the Mathematical Theories of Logic and Probabilities_ \(1854\), được nhắc đến tiện hơn với tên _The Laws of Thought_. Boole mất năm 1864 lúc 49 tuổi sau khi vội đến lớp dưới trời mưa rồi bị sưng phổi.  
Tựa đề cuốn sách 1854 của Bool đề xuất một bước tiến tham vọng: Bởi vì não người dùng logic để suy nghĩ, nếu ta tìm ra cách nào đó đại diện logic bằng toán học thì ta cũng sẽ có được mô tả toán học cách hoạt động của não bộ. Tất nhiên ngày nay, cách nhìn nhận tâm trí như này khá là ngây thơ. \(Hoặc cũng có thể đã vượt trước thời đại\)  
Boole phát minh ra kiểu đại số thể hiện rất giống với đại số cũ. Trong đại số, các _toán hạng_ \(thường là chữ\) đại diện cho số, _toán tử_ \(thường là + và x\) thể hiện cách các số được kết hợp. Thường thì ta dùng đại số thể giải quyết bài toán kiểu này: An có 3 quả táo. Bin có nhiều táo gấp đôi An. Công có nhiều hơn Bin 5 quả táo. Đạt có gấp 3 lần số táo của Công. Hỏi Đạt có mấy quả táo?  
Để giải bài toán, trước tiên ta chuyển tiếng Việt thành mệnh đề toán học, dùng bốn chữ cái để đại diện cho số táo của bốn người:

A = 3  
B = 2 x A  
C = B + 5  
D = 3 x C

Ta có thể kết hợp 4 mệnh đề này lại thành một bằng phương pháp thế sau đó thực hiện tính cộng và nhân:

D = 3 x C  
D = 3 x \(B + 5\)  
D = 3 x \(\(2 x A\) + 5\)  
D = 3 x \(\(2 x 3\) + 5\)  
D = 33

Khi ta thực hiện đại số, ta tuân theo một số quy tắc. Những quy tắc này ăn trong máu chúng ta nên nhiều khi ta không còn nghĩ nó là quy tắc nữa và có khi còn quên luôn tên rồi. Nhưng hoá ra quy tắc lại chính là nền tảng cho tất cả các công trình của tất cả các dạng toán học.  
Quy tắc thứ nhất là cộng và nhân có tính _giao hoán_. Có nghĩa là ta có thể đổi chỗ xung quanh các kí tự mỗi bên toán toán tử:

A + B = B + A  
A x B = B x A

Ngược lại, trừ và chia _không_ có tính giao hoán.  
Cộng và nhân còn có tính _kết hợp_, đó là

A + \(B + C\) = \(A + B\) + C  
A x \(B x C\) = \(A x B\) x C

Và cuối cùng, là _nhân phân phối_:

A x \(B + C\) = \(A x B\) + \(A x C\)

Một đặc điểm khác của đại số là nó luôn dính tới số, như là số táo, số vịt hay khoảng cách mà tàu lửa đi được hay số tuổi của mỗi thành viên trong gia đình. Thiên tài của Bool ở chỗ làm cho đại số trừu tượng hơn bằng cách gỡ bỏ nó khỏi các con số. Trong đại số Boolean \(đại số của Boole sau này được gọi\), toán hạng không ám chỉ các con số nữa mà là các _lớp_. Một lớp là một nhóm vật mà theo thời gian được biết tới là _tập hợp \(set\)_.  
Thử nói về mèo xem sao. Mèo có thể là con đực hay cái. Để thuận tiện, ta dùng chữ M để ám chỉ lớp mèo đực \(male\) và F cho lớp mèo cái \(female\). Luôn nhớ là hai chữ này không hề ám chỉ tới số lượng mèo. Số lượng mèo có thể thay đổi theo thời gian khi mèo con cứ tiếp tục ra đời và mèo già thì \(thật đáng tiếc\) cứ tiếp tục qua đời. Chữ cái đại diện cho lớp của mèo - mèo với đặc điểm cụ thể. Thay vì nói mèo cái, ta có thể chỉ cần nói "F".

Ta cũng có thể dùng chữ cái để đại diện cho màu sắc của mèo: ví dụ, T có thể ám chỉ mèo vàng \(tan\), B ám chỉ mèo đen \(black\), W cho mèo trắng \(white\) và O cho mèo màu "khác" \(other\) - tất cả mèo ngoài class T, B, W.  
Cuối cùng \(xa nhất mà ví dụ này có thể đến\), mèo có thể bị tiệt sản hoặc không. Hãy dùng N cho lớp mèo tiệt sản \(neutered\) và U cho lớp còn đẻ được \(unneutered\). Trong đại số thường, toán tử + và x đại diện cho phép cộng và nhân. Trong đại số Boolean, + và x vẫn được dùng, và đây là lúc mọi thứ có vẻ rối. Mọi người đều biết cộng và nhân trong đại số thường thế cộng và nhân _các lớp_ như thế nào?  
Chà, thật ra thì ta không cộng và nhân trong đại số Boolean. Thay vào đó, + và x mang một nghĩa hoàn toàn khác.  
Kí hiệu + trong đại số Boolean mang nghĩa là _hợp_ của hai lớp. Một hợp của hai lớp là mọi thứ trong lớp một hợp với mọi thứ trong lớp hai. Ví dụ, B + W là tập hợp tất cả mèo đen hoặc trắng.  
Dấu x trong đại số Boolean mang nghĩa là _giao_ của hai lớp. Một giao của hai lớp là mọi thứ có trong _cả_ lớp đầu _và_ lớp thứ hai. Ví dụ, F x T là tập hợp lớp các con mèo cái màu vàng. Như trong đại số, ta có thể viết F x T thành F.T, hoặc gọn hơn là FT \(cách mà Boole thích hơn\). Bạn có thể nghĩ hai chữ cái như là hai tính từ đi liền nhau: mèo cái vàng.  
Để tránh nhầm lẫn giữa đại số và Boolean, đôi khi kí hiệu ∪ và ∩ đại diện hợp và giao thay cho + và x. Nhưng một phần từ sức ảnh hưởng giải phóng của Boole vào toán học là làm cho công dụng của các toán tử tương tự trực quan hơn, nên tôi quyết định tuân theo quyết định của ông không giới thiệu thêm các kí hiệu mới.  
Quy tắc giao hoán, kết hợp và phân phối được giữ nguyên trong đại số Boolean. Thêm nữa là, trong Boolean phân phối có thể áp dụng cho dấu +. Như này là không đúng trong đại số thường:

W + \(B x F\) = \(W + B\) x \(W + F\)

Hợp của mèo trắng với mèo cái đen bằng với giao của hai hợp: hợp mèo trắng mèo đen và hợp mèo trắng mèo cái. Có hơi khó nắm bắt một chút, nhưng là đúng đấy.  
Có thêm hai kí tự nữa để hoàn thành đại số Boolean. Hai kí hiệu nay trông khá giống với số nhưng lại không phải bởi vì đôi khi chúng được dùng khác với số. Kí hiệu 1 trong Boolean nghĩa là "toàn thể" - có nghĩa là, mọi thứ ta nói về nó. Trong ví dụ này, 1 có nghĩa là lớp của tất cả loài mèo. Do đó,

M + F = 1

Có nghĩa là hợp của mèo cái và mèo đực là lớp tất cả mèo. Tương tự như vậy cho hợp của lớp mèo vàng, đen, trắng và màu khác.

T + B + W + O = 1

Và bạn cũng có được lớp tất cả mèo bằng cách này:

N + U = 1

Kí hiệu 1 có thể được dùng với dấu - để thể hiện toàn thể _trừ_ ra. Ví dụ,

1 - M

là lớp tất cả mèo trừ mèo đực. Bằng với lớp mèo cái

1 - M = F

Kí hiệu khác ta cần là 0, trong Boolean 0 biểu thị cho lớp rỗng - lớp không có gì. Lớp rỗng là kết quả từ việc giao hai lớp hoàn toàn trái ngược nhau, như giao của mèo đực và mèo cái:

F x M = 0

Để ý là 1 và 0 hoạt động đơi khi tương tự như trong đại số thường. Ví dụ giao của tất cả mèo và mèo cái là mèo cái

1 x F = F

Giao của không mèo và mèo cái là không có mèo:

0 x F = 0

Hợp của không mèo và tất cả mèo cái là mèo cái

0 + F = F

Nhưng đôi khi kết quả lại không giống trông đại số lắm. Ví dụ, hợp của tất cả mèo và mèo cái tất cả mèo:

1 + F = 1

Vô nghĩa trong đại số thường.  
Vì F là lớp mèo cái, \(1 - F\) là lớp mèo không phải cái, nên hợp của 2 lớp này là lớp toàn thể:

F + \(1 - F\) = 1

và giao của 2 lớp là 0:

F x \(1 - F\) = 0

Trước giờ, biểu thức này đại diện cho một khái niệm quan trọng trong logic: được gọi là Luật Mâu Thuẫn và biểu thị một vật không thể vừa là nó vừa không phải là nó.  
Boolean khác với đại số nhiều nhất ở chỗ:

F x F = F

Mệnh đề có ý nghĩa trong Boolean. Giao của mèo cái với mèo cái vẫn là lớp mèo cái. Nhưng nếu là số thì chắc hẳn là sai rồi. Bool xem

X2 = X

là mệnh đề đơn làm cho đại số của ông khác với đại số cũ. Một mệnh đề khác trông cũng khá ngộ khi đem so với đại số là:

F + F = F

Hợp của mèo cái với mèo cái vẫn là lớp mèo cái.  
Boolean cung cấp một phương pháp toán học để giải quyết tam đoạn luận của Aristotle. Hãy nhìn vào hai câu đầu của tam đoạn luận nổi tiếng một lần nữa, nhưng lần này dùng ngôn ngữ người:

Tất cả người đều chết;  
Socrates là người.

Ta dùng P để đại diện cho lớp người \(persons\), M đại diện cho lớp khả tử \(mortal\) và S đại diện cho lớp Socrates. Khi nói "tất cả người đều chết" thì là ý gì? Có nghĩa là giao của lớp người với lớp khả tử là lớp người.

P x M = P

Sẽ sai khi nói rằng P x M = M, vì lớp khả tử có cả chó, mèo và cây du.  
Để nói, "Socrates là người" có nghĩa là giao của lớp chứa Socrates và lớp tất cả người là lớp chứa Socrates:

S x P = S

Vì ta biết là P = P x M, nên ta sẽ thế P vào:

S x \(P x M\) = S

Dùng kết hợp, ta được

\(S x P\) x M = S

Mà ta lại biết là S x P = S, thế vào

S x M = S

Xong. Biểu thức này cho ta biết là giao của Socrates với lớp khả tử là S, Socrates sẽ chết. Nếu ta tìm ra kết quả \(S x M\) bằng 0, ta kết luận rằng Socrates không chết được. Nếu bằng M, kết luận phải là Socrates là điều duy nhất khả tử và mọi thứ khác đều bất tử!  
Dùng Boolean để chứng minh sự thật hiển nhiên thì như giết gà dùng dao mổ trâu vậy \(cụ thể là để chứng minh Socrates sẽ chết cách đây 2400 năm\), Boolean còn có thể xác định xem thứ gì đó có thoả điều kiện cho trước không. Một ngày nào đó bạn sẽ vào tiệm thú cưng và nói với nhân viên bán hàng là "Tôi muốn một con mèo đực đã thiến trắng hay vàng gì cũng được; không thì mèo cái đã tiệt sản màu nào cũng được trừ trắng; không có nữa thì tôi sẽ lấy con mèo nào cũng được miễn màu đen. Và nhân viên sẽ nói với bạn là "Vậy là bạn muốn một con mèo thuộc lớp được đại diện bởi biểu thức sau:

\(M x N x \(W + T\)\) + \(F x N x \(1 - W\)\) + B

Đúng chứ?" Bạn đáp, "Chuẩn cơm mẹ nấu!"  
Để xác minh là nhân viên đó đúng, bạn đành phải từ bỏ khái niệm hợp với giao mà thay vào dùng OR với AND. Tôi viết hoa hai chữ này vì nó mang nghĩa bình thường trong ngôn ngữ, nhưng chúng cũng có thể đại diện cho các toán tử trong Boolean. Khi bạn hợp hai lớp có nghĩa là bạn thật sự chấp nhận các thứ từ lớp đầu OR lớp sau. Và khi bạn muốn giao hai lớp có nghĩa là bạn chỉ muốn những thứ có trong lớp đầu AND lớp sau. Hơn nữa bạn có thể dùng từ NOT khi bạn gặp một với dấu trừ theo sau. Tóm lại,

* Dấu + \(trước đó là hợp\) giờ là OR.
* Dấu x \(trước là giao\) giờ là AND.
* 1 - \(trước đây là toàn thể trừ gì đó\) giờ là NOT.

Nên biểu thức lúc nãy có thể viết lại là:

\(M AND N AND \(W OR T\)\) OR \(F AND N AND \(NOT W\)\) OR B

Đã rất gần với những gì bạn nói. Để ý cách dấu ngoặc thể hiện độ ưu tiên bạn muốn. Bạn muốn mèo thuộc một trong ba lớp này:

M AND N AND \(W OR T\)\)  
**OR**  
\(F AND N AND \(NOT W\)\)  
**OR**  
B

Với cách viết biểu thức như này, nhân viên đã có thể thực hiện _bài kiểm tra Boolean_. Để không tập trung quá mức vào nó, tôi sẽ chuyển sang một dạng hơi khác của Boolean. Chữ giờ sẽ có thể gán được số. Mấu chốt là nó chỉ gán được 1 và 0. Số 1 có nghĩa là Đúng, con mèo này thoả các tiêu chí. 0 nghĩa là Sai, Trật không phải con mèo này.  
Đầu tiên nhân viên đem ra một con mèo đực vàng còn đẻ được. Đây là biểu thức tìm mèo:

\(M x N x \(W + T\)\) + \(F x N x \(1 - W\)\) + B

và khi thay 0, 1 vào thành thế này:

\(1 x 0 x \(0 + 1\)\) + \(0 x 0 x \(1 - 0\)\) + 0

Để ý là kí tự được gán 1 là M và T vì mèo này đực và nâu.  
Giờ ta cần đơn giản bớt biểu thức. Nếu thành 1 thì đúng mèo, còn 0 thì trật. Lúc đơn giản ta phải nhớ trong đầu là không phải ta đang thực hiện cộng hay nhân mặc dù thường thì ta vờ như thế. Đa phần các quy tắc dùng được từ + sang OR từ x sang AND. \(Đôi khi trong văn bản hiện đại kí hiệu ∧ và ∨ cho AND với OR thay vì x với +. Nhưng ở đây + với x dễ hiểu hơn.\)  
Khi dấu x nghĩa là AND, kết quả có thể là

0 x 0 = 0  
0 x 1 = 0  
1 x 0 = 0  
1 x 1 = 1

Nói cách khác, kết quả là 1 chỉ khi cả toán hạng trái VÀ phải đều là 1. Phép tính này cho kết quả tương tự với phép nhân thông thường, và có thể được tóm tắt lại bằng bảng, tương tự như bảng cho cộng và trừ ở Chương 8:

| AND | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 0 | 0 |
| 1 | 0 | 1 |

Khi dấu + nghĩa là OR, kết quả là

0 + 0 = 0  
0 + 1 = 1  
1 + 0 = 1  
1 + 1 = 1

Kết quả là 1 khi toán hạng trái HOẶC phải là 1. Tương tự như phép cộng thông thường, trừ trường hợp 1 + 1 = 1. Phép OR có thể tóm tắt thành bảng:

| OR | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 0 | 1 |
| 1 | 1 | 1 |

Ta đã sẵn sàng dùng bảng tính để hoàn thành biểu thức

\(1 x 0 x 1\) + \(0 x 0 x 1\) + 0 = 0 + 0 + 0 = 0

Kết quả là 0, không phải cậu mèo này rồi.  
Tiếp, nhân viên đem ra cô mèo trắng đã tiệt sản. Biểu thức gốc là

\(M x N x \(W + T\)\) + \(F x N x \(1 - W\)\) + B

Thay 0, 1 vô

\(0 x 1 x \(1 + 0\)\) + \(1 x 1 x \(1 - 1\)\) + 0

tối giản thành

\(0 x 1 x 1\) + \(1 x 1 x 0\) + 0 = 0 + 0 + 0 = 0

Và cô mèo tội nghiệp này đã bị từ chối.  
Lần này nhân viên đem ra một cô mèo xám đã tiệt sản. \(Màu xám trong lớp màu "khác" - không đen, trắng, vàng\). Đây là biểu thức:

\(0 x 1 x \(0 + 0\)\) + \(1 x 1 x \(1 - 0\) + 0

tối giản thành

\(0 x 1 x 0\) + \(1 x 1 x 1\) + 0 = 0 + 1 + 0 = 1

Cuối cùng đã được 1, vâng, cô mèo con đã tìm thấy tổ ấm của mình. \(Và cũng là cô mèo dễ thương nhất!\)  
Tối muộn, khi cô mèo cuộn trong ngủ trong lòng bạn, bạn tự hỏi liệu mình có thể dùng bóng đèn với công tắc để nối thành mạch điện giúp xác định con mèo nào thoả các tiêu chí không nhỉ. \(Vâng, bạn là một đứa nhóc kì lạ.\) Bạn có chút nào cảm nhận là mình sắp tạo ra một đột phá tầm cỡ. Bạn sắp sửa thực hành vài trải nghiệm mà sẽ thống nhất đại số của George Boole với mạch điện và sau đó là khả năng thiết kệ và xây dựng máy tính nhị phân. Nhưng cũng đừng để chúng mê hoặc bạn quá.  
Để bắt đầu bạn nối đèn với pin như mạch thông thường, nhưng dùng hai công tắc thay vì một:  
![Screen Shot 2018-07-14 at 23.34.41.png](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-14-at-23-34-41.png)  
Công tắc nối như này, một cái tiếp sau cái kia, là mạch _nối tiếp_. Nếu bạn đóng công tắc trái, không có gì xảy ra:  
![Screen Shot 2018-07-14 at 23.35.40.png](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-14-at-23-35-40.png)  
Tương tự nếu mở công tắc trái và đóng công tắc phải cũng không có gì hết. Bóng đèn chỉ sáng khi cả hai công tắc đều đóng, như trong hình.  
![Screen Shot 2018-07-14 at 23.36.19.png](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-14-at-23-36-19.png)  
Từ khoá là _và_. Cả công tắc trái và phải phải đóng để dòng điện chạy trong mạch.  
Mạch này trình diễn một thực nghiệm nhỏ trong logic. Thực tế bóng đèn đã trả lời cho câu hỏi "Cả hai công tắc đều đóng phải không?" Ta có thể tóm tắt hoạt động của mạch bằng bảng sau

| Công tắc trái | Công tắc phải | Bóng đèn |
| :--- | :--- | :--- |
| Mở | Mở | Không sáng |
| Mở | Đóng | Không sáng |
| Đóng | Mở | Không sáng |
| Đóng | Đóng | Sáng |

Ở trương trước, chúng ta đã biết là số nhị phân, hay bit có thể biểu diễn thông tin - mọi thứ từ số tới hướng ngón tay của Roger Ebert. Ta đã có thể nói rằng 0 là "ngón cái trỏ xuống" và 1 là " ngón cái trỏ lên". Công tắc có hai lựa chọn, nên nó đại diện cho 1 bit. Ta có thể nói 0 là bóng đèn tắt và 1 cho bóng đèn sáng. Ta chỉ cần viết lại bảng

| Công tắc trái | Công tắc phải | Bóng đèn |
| :--- | :--- | :--- |
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

Để ý là nếu ta đổi chỗ hai công tắc thì kết quả vẫn không đổi. Ta thật ra chẳng cần phân biệt hai công tắc. Nên ta có thể tái lập lại bảng AND và OR trước đây:

| Công tắc nối tiếp | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 0 | 0 |
| 1 | 0 | 1 |

Thật ra thì nó giống với bảng AND. Kiểm tra thử

| AND | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 0 | 0 |
| 1 | 0 | 1 |

Mạch đơn giản này thực sự biểu diễn một phép tính AND.  
Giờ thử nối hai công tắc khác đi một chút:  
![Screen Shot 2018-07-14 at 23.36.55.png](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-14-at-23-36-55.png)  
Công tắc này đang được nối _song song_. Sự khác nhau giữa mạch này và mạch trước đó là nếu ta đóng công tắc trên thì đèn sẽ sáng:  
![Screen Shot 2018-07-14 at 23.37.29.png](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-14-at-23-37-29.png)  
hay đóng công tắc dưới  
![Screen Shot 2018-07-14 at 23.37.56](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-14-at-23-37-56.png)  
hoặc là cả hai:  
![Screen Shot 2018-07-14 at 23.38.23](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-14-at-23-38-23.png)  
Đèn sáng khi công tắc trên _hoặc_ dưới đóng. Từ khoá ở đây là _hoặc_.  
Lần nữa, mạch biểu diễn một thực hành trong logic. Đèn sáng trả lời cho câu hỏi, "Cả hai công tắc đóng phải không?" Bảng sau tóm tắt cách hoạt động của mạch:

| Công tắc trái | Công tắc phải | Bóng đèn |
| :--- | :--- | :--- |
| Mở | Mở | Không sáng |
| Mở | Đóng | Sáng |
| Đóng | Mở | Sáng |
| Đóng | Đóng | Sáng |

Lần nữa, 0 cho công tắc mở và đèn tắt, 1 cho công tắc đóng và đèn sáng, có thể viết lại:

| Công tắc trái | Công tắc phải | Bóng đèn |
| :--- | :--- | :--- |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

Lần nữa không quan trọng thứ tự hai bóng đèn, viết lại bảng:

| Công tắc song song | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 0 | 1 |
| 1 | 1 | 1 |

Và có lẽ bạn cũng đoán được là nó giống với bảng OR:

| OR | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 0 | 1 |
| 1 | 1 | 1 |

có nghĩa là hai công tắc song song biểu diễn biểu thức AND.  
Khi bạn đến quán thú cưng, bạn nói với nhân viên bán hàng là, "Tôi muốn một con mèo đực đã thiến trắng hoặc vàng; hoặc là mèo cái còn sinh sản được không phải màu trắng; hoặc là mèo gì cũng được miễn là đen.", và nhân viên cho bạn một biểu thức:

\(M x N x \(W + T\)\) + \(F x N x \(1 - W\)\) + B

Giờ bạn biết là hai công tắc mắc nối tiếp biểu diễn logic AND \(đại diện bởi dấu x\) và logic OR nếu nối song song \(đại diện bởi dấu +\), bạn có thể nối tám công tắc như sau:  
![Screen Shot 2018-07-14 at 23.39.05](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-14-at-23-39-05.png)  
Mỗi công tắc trong mạch được gắn chữ - giống trong biểu thức Boolean. \(-W có nghĩa là NOT W là cách viết khác của 1 - W\). Thế ra, nếu bạn đi theo mạch điện từ trái sang phải bắt từ từ phía trên đi xuống dưới, bạn sẽ gặp các chữ cái theo thứ tự trong biểu thức. Mỗi dấu x trong biểu thức tương ứng với điểm mà hai công tắc \(hay nhóm các công tắc\) nối nối tiếp. Mỗi dấu + là điểm mà hai công tắc \(hay nhóm công tắc\) nối song song.  
Bạn nhớ lại là nhân viên đem ra một cậu mèo vàng đã thiến. Đóng các công tắc tương ứng  
![Screen Shot 2018-07-14 at 23.39.38](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-14-at-23-39-38.png)  
Mặc dù M, T và NOT W đều đóng, ta chưa được mạch hoàn chỉnh đề thắp sáng đèn. Tiếp nhân viên đem ra một cô mèo trắng đã tiệt sản:  
![Screen Shot 2018-07-14 at 23.40.13](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-14-at-23-40-13.png)  
Một lần nữa, công tắc cần thiết đã không đóng để đèn sáng. Nhưng sau cùng, nhân viên đem ra một cô mèo xám đã cắt trứng:  
![Screen Shot 2018-07-14 at 23.40.49](https://tukhucxuan.files.wordpress.com/2018/07/screen-shot-2018-07-14-at-23-40-49.png)  
Và nhiêu đó đã đủ hoàn thành mạch, thắp sáng đèn vào báo cô mèo đã thoả điều kiện của bạn.  
George Boole chưa từng nối mach như này. Ông chưa bao giờ có được cảm xúc khi nhìn biểu thức Boolean được hiểu nhờ công tắc, mạch điện và bóng đèn. Một rào chắn, tất nhiên đó là bóng đèn mãi 15 năm sau khi Boole qua đời mới được phát minh. Nhưng Samuel Morse đã mô tả máy điện báo vào năm 1844 - mười năm trước khi cuốn The Laws of Thought được xuất bản - và sẽ đơn giản nếu thay thế tiếng máy điện báo bằng đèn sáng trong mạch như trên.  
Nhưng chẳng có ai vào thế kỉ mười chín từng nghĩ đến việc kết nối biểu thức AND, OR với cách nối công tắc trong mạch điện kiểu nối tiếp hay song song. Không một nhà toán học, kĩ thuật điện, điều hành máy điện tín, không một ai cả. Thậm chí biểu tượng của cuộc cách mạng máy tính Charles Babbage \(1792-1871\), người đã hồi đáp với Boole và biết công trình này, và là người đã dành gần cả đời để thiết kế đầu tiên là Difference Engine và kế đến là Analytical Engine cái mà một thế kỉ sau sẽ là tiền thân của máy tính ngày nay. Điều có lẽ đã giúp Babbage, mà ngày nay chúng ta biết được là sự nhận thức được có thể thay vì dùng thanh gỗ\(1\) để tính toán, một máy tính có thể được tạo ra tốt hơn từ rơle điện báo.  
Vâng, rơle điện báo.

\(1\): gears and levers, mình không biết dịch sao để sát nghĩa nữa.   

