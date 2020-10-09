# Chapter 02: Meanings Full Names
## Introduction
Tên có ở khắp mọi nơi trong phần mềm. Chúng tôi đặt tên biến của chúng tôi, các chức năng của chúng tôi, lập luận của chúng tôi, các lớp học, và các gói. Chúng tôi đặt tên cho các tệp nguồn của mình và các thư mục chứa chúng. Chúng tôi đặt tên cho các tệp jar và tệp chiến tranh và tệp tai. Chúng tôi đặt tên và đặt tên và đặt tên. Bởi vì chúng tôi làm rất nhiều điều đó, chúng tôi nên làm tốt hơn. Sau đây là một số quy tắc đơn giản để tạo
những cái tên hay.

## Use Intention-Revealing Names
Có thể dễ dàng nói rằng những cái tên nên bộc lộ ý định. Điều chúng tôi muốn gây ấn tượng với bạn là chúng tôi rất nghiêm túc về vấn đề này. Việc chọn những cái tên hay tuy mất thời gian nhưng tiết kiệm được nhiều thời gian.
Vì vậy, hãy cẩn thận với tên của bạn và thay đổi chúng khi bạn tìm thấy những tên tốt hơn. Mọi người đọc mã của bạn (kể cả bạn) sẽ hạnh phúc hơn nếu bạn làm vậy.
Tên của một biến, hàm hoặc lớp, phải trả lời tất cả các câu hỏi lớn. Nó sẽ cho bạn biết tại sao nó tồn tại, nó làm gì và nó được sử dụng như thế nào. Nếu một cái tên yêu cầu một sự kết hợp, thì cái tên đó không thể hiện ý định của nó.
int d; // thời gian trôi qua tính bằng ngày
Tên d không tiết lộ gì. Nó không gợi lên cảm giác về thời gian đã trôi qua, cũng không phải ngày. Chúng tôi
nên chọn một cái tên chỉ định những gì đang được đo lường và đơn vị của phép đo đó-
đề cập:
int
int
int
int
elapsedTimeInDays;
ngàySinceCreation;
ngàySinceModification;
fileAgeInDays;
Chọn tên thể hiện ý định có thể giúp bạn dễ hiểu và dễ thay đổi hơn nhiều
mã. Mục đích của mã này là gì?
danh sách công khai <int []> getThem () {
List <int []> list1 = new ArrayList <int []> ();
cho (int [] x: theList)
nếu (x [0] == 4)
list1.add (x);
danh sách trả về1;
}
Tại sao rất khó để biết mã này đang làm gì? Không có biểu thức phức tạp.
Khoảng cách và thụt lề hợp lý. Chỉ có ba biến và hai hằng được đề cập. Thậm chí không có bất kỳ lớp hay phương thức đa hình ưa thích nào, chỉ là một danh sách các mảng (hoặc có vẻ như vậy). Vấn đề không phải là sự đơn giản của mã mà là sự không rõ ràng của mã (thành một cụm từ): mức độ mà ngữ cảnh không rõ ràng trong chính mã. Mã ngụ ý- nó yêu cầu chúng ta biết câu trả lời cho các câu hỏi như:
1. Những loại thứ gì trong danh sách?
2. Ý nghĩa của chỉ số con thứ 0 của một mục trong Danh sách là gì?
3. Ý nghĩa của giá trị 4 là gì?
4. Tôi sẽ sử dụng danh sách đang được trả về như thế nào?
www.it-ebooks.info19
Tránh thông tin sai lệch
Câu trả lời cho những câu hỏi này không có trong mẫu mã, nhưng chúng có thể có. Giả sử rằng chúng tôi đang làm việc trong trò chơi quét mìn. Chúng tôi thấy rằng bảng là một danh sách
các ô được gọi là danh sách. Hãy đổi tên nó thành gameBoard.
Mỗi ô trên bảng được biểu diễn bằng một mảng đơn giản. Chúng tôi còn nhận thấy rằng chỉ số con thứ 0 là vị trí của giá trị trạng thái và giá trị trạng thái bằng 4 có nghĩa là “được gắn cờ”. Chỉ
bằng cách đặt tên cho các khái niệm này, chúng tôi có thể cải thiện mã đáng kể:
public List <int []> getFlaggedCells () {
Danh sách <int []> flaggedCells = new ArrayList <int []> ();
cho (int [] cell: gameBoard)
if (ô [STATUS_VALUE] == FLAGGED)
flaggedCells.add (ô);
trả về flaggedCells;
}
Lưu ý rằng tính đơn giản của mã không thay đổi. Nó vẫn có cùng một số toán tử và hằng số, với cùng một số cấp độ lồng nhau. Nhưng mã đã trở nên rõ ràng hơn nhiều.
Chúng ta có thể đi xa hơn và viết một lớp đơn giản cho các ô thay vì sử dụng một mảng int s.
Nó có thể bao gồm một chức năng tiết lộ ý định (gọi là isFlagged) để ẩn số ma thuật. Nó dẫn đến một phiên bản mới của hàm:
danh sách công khai <Cell> getFlaggedCells () {
Danh sách <Cell> flaggedCells = new ArrayList <Cell> ();
cho (Ô ô: gameBoard)
if (cell.isFlagged ())
flaggedCells.add (ô);
trả về flaggedCells;
}
Với những thay đổi tên đơn giản này, không khó để hiểu chuyện gì đang xảy ra. Đây là sức mạnh của việc chọn tên hay.


## Avoid Disinformation
Lập trình viên phải tránh để lại các manh mối sai làm che khuất ý nghĩa của mã. Chúng ta nên tránh những từ có nghĩa cố định khác với ý nghĩa của chúng ta. Ví dụ,
hp, aix, và sco sẽ là các tên biến kém vì chúng là tên của các dạng hoặc biến thể Unix. Ngay cả khi bạn đang mã hóa một cạnh huyền và hp trông giống như một chữ viết tắt hay-
tion, nó có thể không đúng định dạng.
Không đề cập đến một nhóm tài khoản là một Danh sách tài khoản trừ khi nó thực sự là một Danh sách.
Danh sách từ có nghĩa là một cái gì đó cụ thể cho các lập trình viên. Nếu vùng chứa tài khoản thực sự không phải là Danh sách, nó có thể dẫn đến kết luận sai. 1 Vì vậy accountGroup hoặc
chùmOfAccounts hoặc chỉ là tài khoản thuần túy sẽ tốt hơn.
1. Như chúng ta sẽ thấy ở phần sau, ngay cả khi vùng chứa là một Danh sách, có lẽ tốt hơn là không nên mã hóa loại vùng chứa thành tên.

Hãy cẩn thận khi sử dụng các tên khác nhau theo những cách nhỏ. Mất bao lâu để phát hiện ra sự khác biệt nhỏ giữa XYZControllerForEnoughHandlingOfStrings trong một mô-đun
và ở đâu đó xa hơn một chút, XYZControllerForEnoughStorageOfStrings? Các
các từ có hình dạng giống nhau một cách đáng sợ.
Đánh vần các khái niệm tương tự tương tự là thông tin. Sử dụng cách viết không nhất quán là thiếu thông tin. Với môi trường Java hiện đại, chúng tôi tận hưởng khả năng hoàn thành mã tự động. Chúng tôi
viết một vài ký tự của tên và nhấn một số tổ hợp phím nóng (nếu có) và được thưởng bằng một danh sách hoàn thành có thể có cho tên đó. Sẽ rất hữu ích nếu tên cho
những thứ rất giống nhau sắp xếp với nhau theo thứ tự bảng chữ cái và nếu sự khác biệt là rất rõ ràng,
bởi vì nhà phát triển có thể chọn một đối tượng theo tên mà không thấy các nhận xét phong phú của bạn hoặc thậm chí danh sách các phương thức được cung cấp bởi lớp đó.
Một ví dụ thực sự khủng khiếp về tên không đúng định dạng sẽ là việc sử dụng chữ thường L hoặc chữ hoa O làm tên biến, đặc biệt là khi kết hợp. Tất nhiên, vấn đề là chúng trông gần như hoàn toàn giống các hằng số một và số không.
int a = l;
nếu (O == l)
a = O1;
khác
l = 01;
Người đọc có thể nghĩ rằng đây là một sự liên quan, nhưng chúng tôi đã kiểm tra mã ở những nơi có nhiều thứ như vậy. Trong một trường hợp, tác giả của mã đề xuất sử dụng một phông chữ khác để sự khác biệt rõ ràng hơn, một giải pháp sẽ phải được chuyển cho
tất cả các nhà phát triển tương lai dưới dạng truyền khẩu hoặc trong một tài liệu văn bản. Vấn đề được chinh phục một cách rốt ráo và không cần tạo ra các sản phẩm công việc mới bằng một cách đổi tên đơn giản.


## Make Meaningful
## Distinctions
Lập trình viên tạo ra vấn đề cho họ-
bản thân khi họ chỉ viết mã cho sat-
isfy một trình biên dịch hoặc trình thông dịch. Ví dụ,
bởi vì bạn không thể sử dụng cùng một tên để giới thiệu
đến hai thứ khác nhau trong cùng một phạm vi,
bạn có thể bị cám dỗ để thay đổi một cái tên
một cách tùy ý. Đôi khi điều này được thực hiện bằng cách viết sai chính tả, dẫn đến tình huống đáng ngạc nhiên là sửa lỗi chính tả dẫn đến không thể biên dịch. 2
Không đủ để thêm chuỗi số hoặc các từ nhiễu, mặc dù trình biên dịch đã hài lòng. Nếu các tên phải khác nhau, thì chúng cũng phải có nghĩa khác.
2. Hãy xem xét, ví dụ, hành động thực sự ghê tởm là tạo một biến có tên klass chỉ vì lớp tên đã được sử dụng
cho một cái gì khác.

Đặt tên theo dãy số (a1, a2, .. aN) là ngược lại với đặt tên có chủ đích. Những cái tên như vậy không phải là sai định dạng — chúng không có định dạng; chúng không cung cấp manh mối nào về ý định của tác giả. Xem xét:
public static void copyChars (char a1 [], char a2 []) {
for (int i = 0; i <a1.length; i ++) {
a2 [i] = a1 [i];
}
}
Hàm này đọc tốt hơn nhiều khi nguồn và đích được sử dụng cho tên đối số.
Các từ nhiễu là một sự phân biệt vô nghĩa khác. Hãy tưởng tượng rằng bạn có một lớp Sản phẩm. Nếu bạn có một tên gọi khác là ProductInfo hoặc ProductData, bạn đã đặt những cái tên khác nhau mà không làm cho chúng có ý nghĩa khác biệt. Thông tin và Dữ liệu là tiếng ồn không rõ ràng
những từ như a, an và the.
Lưu ý rằng không có gì sai khi sử dụng các quy ước tiền tố như a và miễn là chúng tạo ra sự khác biệt có ý nghĩa. Ví dụ, bạn có thể sử dụng a cho tất cả các biến cục bộ và cho tất cả các đối số của hàm. 3 Vấn đề xảy ra khi bạn quyết định gọi một Zork có thể thay đổi bởi vì bạn đã có một biến khác có tên là zork.
Những từ ồn ào là thừa. Biến từ không bao giờ được xuất hiện trong tên biến. Bảng từ không bao giờ được xuất hiện trong tên bảng. NameString tốt hơn Name như thế nào? Tên có bao giờ là một số dấu phẩy động không? Nếu vậy, nó phá vỡ một quy tắc trước đó về thông tin sai lệch. Hãy tưởng tượng bạn tìm thấy một lớp có tên là Khách hàng và một lớp khác có tên là CustomerObject. Bạn nên hiểu sự phân biệt là gì? Cái nào sẽ đại diện cho đường dẫn tốt nhất đến lịch sử thanh toán của khách hàng?
Có một ứng dụng mà chúng tôi biết về điều này được minh họa. chúng tôi đã thay đổi tên
để bảo vệ người có tội, nhưng đây là dạng chính xác của lỗi:
getActiveAccount ();
getActiveAccounts ();
getActiveAccountInfo ();
Làm thế nào để các lập trình viên trong dự án này biết được hàm nào trong số các hàm này cần gọi?
Trong trường hợp không có quy ước cụ thể, biến moneyAmount không thể phân biệt được với tiền, customerInfo không thể phân biệt được với khách hàng, accountData không thể phân biệt với tài khoản và TheMessage không thể phân biệt với tin nhắn. Phân biệt tên theo cách mà người đọc biết những gì khác biệt cung cấp.

## Use Pronounceable Names
Con người giỏi ngôn từ. Một phần đáng kể bộ não của chúng ta được dành riêng cho khái niệm về từ. Và các từ, theo định nghĩa, có thể phát âm được. Sẽ thật tiếc nếu không lấy
Bác Bob đã từng làm điều này trong C ++ nhưng đã từ bỏ thực hành này vì các IDE hiện đại khiến nó không cần thiết.

lợi thế của phần lớn bộ não của chúng ta đã phát triển để xử lý ngôn ngữ nói. Vì vậy, hãy làm cho tên của bạn có thể phát âm được.
Nếu bạn không thể phát âm nó, bạn không thể thảo luận về nó mà không nghe như một tên ngốc. "Chà, đằng này, trên con ong ba cee enn tee chúng ta có một bài báo tiểu luận zee kyew int, thấy không?" Điều này
vì lập trình là một hoạt động xã hội.
Một công ty mà tôi biết có genymdhms (ngày, năm, tháng, ngày, giờ, phút và giây) nên họ đi vòng quanh và nói “gen tại sao emm dee aich emm ess”. tôi có một
Thói quen khó chịu khi phát âm mọi thứ như đã viết, vì vậy tôi bắt đầu nói “gen-yah-mudda- ông chủ.” Sau đó, nó được nhiều nhà thiết kế và nhà phân tích gọi là điều này, và chúng tôi vẫn
nghe thật ngớ ngẩn. Nhưng chúng tôi đã tham gia vào trò đùa, vì vậy nó rất vui. Vui hay không, chúng tôi đã dung thứ cho việc đặt tên kém. Các nhà phát triển mới phải có các biến giải thích cho họ, và sau đó

## Use Searchable Names
Tên một chữ cái và hằng số có một vấn đề cụ thể là chúng không dễ định vị trên toàn bộ nội dung văn bản.
Người ta có thể dễ dàng tìm kiếm MAX_CLASSES_PER_STUDENT, nhưng số 7 có thể rắc rối hơn. Các tìm kiếm có thể tạo ra chữ số như một phần của tên tệp, các định nghĩa hằng số khác và trong các biểu thức khác nhau trong đó giá trị được sử dụng với mục đích khác nhau. Nó thậm chí
tệ hơn khi hằng số là một số dài và ai đó có thể đã hoán vị các chữ số, do đó tạo ra lỗi đồng thời trốn tránh tìm kiếm của lập trình viên.
Tương tự như vậy, tên e là một lựa chọn tồi cho bất kỳ biến nào mà một lập trình viên có thể cần tìm kiếm. Đây là chữ cái phổ biến nhất trong tiếng Anh và có khả năng xuất hiện
trong mỗi đoạn văn bản trong mọi chương trình. Về mặt này, tên dài hơn chiếm ưu thế so với tên ngắn hơn và bất kỳ tên nào có thể tìm kiếm được sẽ chiếm ưu thế trong mã hằng số.
Sở thích cá nhân của tôi là các tên chỉ có một chữ cái CHỈ có thể được sử dụng làm biến thể cục bộ bên trong các phương thức ngắn. Độ dài của tên phải tương ứng với kích thước phạm vi của nó

[N5]. Nếu một biến hoặc hằng số có thể được nhìn thấy hoặc sử dụng ở nhiều nơi trong một nội dung mã,
bắt buộc phải đặt cho nó một cái tên thân thiện với tìm kiếm. Một lần nữa so sánh


## Avoid Encodings
Chúng tôi có đủ các mã hóa để xử lý mà không làm tăng thêm gánh nặng cho chúng tôi. Mã hóa loại hoặc phạm vi thông tin thành tên chỉ đơn giản là thêm một gánh nặng giải mã. Nó
dường như không hợp lý khi yêu cầu mỗi nhân viên mới phải học thêm một mã hóa khác "lan-guage" ngoài việc học phần nội dung mã (thường là đáng kể) mà họ sẽ làm việc-
đó là một gánh nặng tinh thần không cần thiết khi cố gắng giải quyết một vấn đề. Tên được mã hóa hiếm khi phát âm được và dễ nhập sai.

### Hungarian Notation
Ngày xưa, khi chúng ta làm việc bằng những ngôn ngữ bị thách thức về độ dài tên, chúng ta đã vi phạm quy tắc này vì cần thiết và rất hối tiếc. Mã hóa bắt buộc Fortran bằng cách đặt chữ cái đầu tiên làm mã cho loại. Các phiên bản đầu tiên của BASIC chỉ cho phép một chữ cái cộng với một chữ số. Hungary Notation (HN) đã đưa điều này lên một tầm cao mới.
HN được coi là khá quan trọng trong Windows C API, khi mọi thứ là một xử lý số nguyên hoặc một con trỏ dài hoặc một con trỏ void, hoặc một trong một số ứng dụng của “string” (với các công dụng và thuộc tính khác nhau). Những ngày đó, trình biên dịch không kiểm tra các kiểu, vì vậy các lập trình viên cần một cái nạng để giúp họ ghi nhớ các kiểu.
Trong các ngôn ngữ hiện đại, chúng ta có các hệ thống kiểu phong phú hơn nhiều và các trình biên dịch ghi nhớ và thực thi các kiểu. Hơn nữa, có xu hướng đối với các lớp nhỏ hơn và các hàm ngắn hơn để mọi người thường có thể thấy điểm khai báo của từng biến mà họ đang sử dụng.

Lập trình viên Java không cần mã hóa kiểu. Các đối tượng được gõ mạnh và môi trường chỉnh sửa đã nâng cao để chúng phát hiện ra lỗi kiểu rất lâu trước khi bạn có thể chạy biên dịch! Vì vậy, ngày nay HN và các hình thức mã hóa kiểu khác chỉ đơn giản là trở ngại.
Chúng khiến việc thay đổi tên hoặc kiểu của một biến, hàm hoặc lớp khó hơn. Chúng làm cho việc đọc mã khó hơn. Và chúng tạo ra khả năng hệ thống mã hóa sẽ đánh lừa người đọc.
### Member Prefixes

### Interfaces and Implementations
Đây đôi khi là một trường hợp đặc biệt cho các bảng mã. Ví dụ: giả sử bạn đang xây dựng A BSTRACT F ACTORY để tạo các hình dạng. Nhà máy này sẽ là một giao diện và sẽ
được thực hiện bởi một lớp cụ thể. Bạn nên đặt tên cho chúng là gì? IShapeFactory và ShapeFactory? Tôi thích để các giao diện không được trang trí. I trước đó, rất phổ biến trong
di sản của ngày nay, tốt nhất là gây mất tập trung và tệ nhất là quá nhiều thông tin. Tôi không muốn người dùng của mình biết rằng tôi đang giao cho họ một giao diện. Tôi chỉ muốn họ biết rằng đó là một ShapeFactory. Vì vậy, nếu tôi phải mã hóa giao diện hoặc triển khai, tôi chọn
việc thực hiện. Gọi nó là ShapeFactoryImp, hoặc thậm chí là CShapeFactory gớm ghiếc, có thể sẵn sàng mã hóa giao diện.

## Avoid Mental Mapping
Người đọc không cần phải dịch tên của bạn sang những tên khác mà họ đã biết. Vấn đề này thường phát sinh từ sự lựa chọn không sử dụng các thuật ngữ miền có vấn đề hoặc các điều khoản miền giải pháp.
Đây là vấn đề với các tên biến chỉ có một chữ cái. Chắc chắn một bộ đếm vòng lặp có thể được đặt tên là i hoặc j hoặc k (mặc dù không bao giờ là l!) Nếu phạm vi của nó rất nhỏ và không có tên nào khác có thể kết hợp với nó. Điều này là do những tên đơn của bộ đếm vòng lặp là truyền thống.
Tuy nhiên, trong hầu hết các ngữ cảnh khác, một cái tên chỉ có một chữ cái là một lựa chọn tồi; nó chỉ là một nơi giữ chỗ mà người đọc phải lập bản đồ về khái niệm thực tế. Không thể có trường hợp nào tồi tệ hơn khi sử dụng tên c hơn là vì a và b đã được sử dụng.
Nói chung lập trình viên là những người khá thông minh. Những người thông minh đôi khi thích thể hiện sự thông minh của mình bằng cách thể hiện khả năng vận động trí óc của họ. Rốt cuộc, nếu bạn có thể tin tưởng-
Hãy nhớ rằng r là phiên bản có cấu trúc thấp hơn của url với máy chủ và lược đồ đã bị xóa, thì rõ ràng bạn phải rất thông minh.
Một sự khác biệt giữa một lập trình viên thông minh và một lập trình viên chuyên nghiệp là người chuyên nghiệp hiểu rằng sự rõ ràng là vua. Các chuyên gia sử dụng quyền hạn của họ cho mục đích tốt và viết mã mà người khác có thể hiểu được.

## Class Names
Các lớp và đối tượng phải có tên danh từ hoặc cụm danh từ như Khách hàng, WikiPage, Tài khoản và AddressParser. Tránh các từ như Người quản lý, Bộ xử lý, Dữ liệu hoặc Thông tin trong tên
của một lớp. Tên lớp không được là động từ.


## Method Names
Các phương thức phải có tên động từ hoặc cụm động từ như postPayment, deletePage hoặc save. Các trình truy cập, trình đột biến và vị từ phải được đặt tên theo giá trị của chúng và có tiền tố là get, set và theo tiêu chuẩn javabean. 4 string name = worker.getName ();
customer.setName ("mike");
if (paycheck.isPosted ()) ... Khi các hàm tạo bị quá tải, hãy sử dụng các phương thức nhà máy tĩnh với tên mô tả các đối số. Ví dụ: Điểm tựa phức hợp = Complex.FromRealNumber (23.0);
nói chung là tốt hơn Điểm tựa phức hợp = new Complex (23.0);
Xem xét việc thực thi việc sử dụng chúng bằng cách đặt các hàm tạo tương ứng ở chế độ riêng tư.

## Don’t Be Cute
Nếu những cái tên quá thông minh, chúng sẽ
đáng nhớ chỉ với những người chia sẻ
khiếu hài hước của tác giả và chỉ miễn là
như những người này nhớ về trò đùa. Sẽ
họ biết hàm có tên là gì
HolyHandGrenade phải làm gì? Chắc chắn rồi,
nó dễ thương, nhưng có thể trong trường hợp này
DeleteItems có thể là một cái tên tốt hơn.
Chọn sự rõ ràng hơn giá trị giải trí.
Sự dễ thương trong mã thường xuất hiện dưới dạng thông tục hoặc tiếng lóng. Ví dụ: không sử dụng tên whack () để có nghĩa là giết (). Đừng kể những câu chuyện cười phụ thuộc vào văn hóa như eatMyShorts () có nghĩa là hủy bỏ ().
Nói những gì bạn có nghĩa là. Có nghĩa là những gì bạn nói.

## Pick One Word per Concept
Chọn một từ cho một khái niệm trừu tượng và gắn bó với nó. Ví dụ: thật khó hiểu khi tìm nạp, truy xuất và lấy như các phương thức tương đương của các lớp khác nhau. Làm thế nào để bạn nhớ tên phương thức nào đi với lớp nào? Đáng buồn thay, bạn thường phải nhớ
công ty, nhóm hoặc cá nhân nào đã viết thư viện hoặc lớp học để ghi nhớ thuật ngữ nào đã được sử dụng. Nếu không, bạn sẽ mất rất nhiều thời gian để duyệt qua các tiêu đề và các mẫu mã trước đó.
Các môi trường chỉnh sửa hiện đại như Eclipse và IntelliJ cung cấp các manh mối nhạy cảm với ngữ cảnh, chẳng hạn như danh sách các phương thức bạn có thể gọi trên một đối tượng nhất định. Nhưng lưu ý rằng danh sách không đồng minh cung cấp cho bạn những nhận xét bạn đã viết về tên hàm và danh sách tham số của bạn.
Bạn thật may mắn nếu nó cung cấp tên tham số từ các khai báo hàm. Các tên hàm phải đứng một mình và chúng phải nhất quán để bạn có thể chọn phương pháp chính xác mà không cần khám phá thêm.
Tương tự như vậy, thật khó hiểu khi có một bộ điều khiển và một người quản lý và một trình điều khiển trong cùng một cơ sở mã. Sự khác biệt cơ bản giữa DeviceManager và Protocol- Controller là gì? Tại sao cả hai đều không phải là người kiểm soát hoặc cả hai đều không phải là người quản lý? Cả hai đều là Trình điều khiển
có thật không? Tên khiến bạn mong đợi hai đối tượng có kiểu rất khác nhau cũng như có các lớp khác nhau.
Một từ vựng nhất quán là một lợi ích tuyệt vời cho các lập trình viên, những người phải sử dụng mã của bạn.

## Don’t Pun
Tránh sử dụng cùng một từ cho hai mục đích. Sử dụng cùng một thuật ngữ cho hai ý tưởng khác nhau về bản chất là một cách chơi chữ.

Nếu bạn tuân theo quy tắc "một từ cho mỗi khái niệm", bạn có thể kết thúc với nhiều lớp, ví dụ, có một phương thức thêm. Miễn là danh sách tham số và giá trị trả về của các phương thức thêm khác nhau tương đương nhau về mặt ngữ nghĩa, tất cả đều tốt.
Tuy nhiên, một người có thể quyết định sử dụng từ thêm cho “nhất quán” khi thực tế người đó không thêm theo cùng một nghĩa. Giả sử chúng ta có nhiều lớp trong đó thêm sẽ tạo ra một giá trị mới bằng cách thêm hoặc nối hai giá trị hiện có. Bây giờ giả sử chúng tôi đang viết một
lớp mới có một phương thức đặt tham số duy nhất của nó vào một tập hợp. Chúng ta có nên gọi phương thức này là add không? Nó có vẻ nhất quán vì chúng ta có rất nhiều phương thức add khác, nhưng trong trường hợp này, ngữ nghĩa khác nhau, vì vậy chúng ta nên sử dụng tên như insert hoặc append để thay thế. Để gọi phương thức mới, add sẽ là một cách chơi chữ.
Với tư cách là tác giả, mục tiêu của chúng tôi là làm cho mã của chúng tôi dễ hiểu nhất có thể. Chúng tôi muốn mã của mình là một bản đọc lướt nhanh, không phải là một nghiên cứu căng thẳng. Chúng tôi muốn sử dụng bìa mềm phổ biến
mô hình theo đó tác giả có trách nhiệm làm cho bản thân rõ ràng chứ không phải mô hình học thuật, nơi mà công việc của học giả là đào sâu ý nghĩa ra khỏi bài báo.


## Use Solution Domain Names
Hãy nhớ rằng những người đọc mã của bạn sẽ là lập trình viên. Vì vậy, hãy tiếp tục và sử dụng các thuật ngữ khoa học máy tính (CS), tên thuật toán, tên mẫu, thuật ngữ toán học, v.v. Nó
không khôn ngoan khi rút mọi tên khỏi miền có vấn đề vì chúng tôi không muốn đồng nghiệp của mình phải chạy đi chạy lại để khách hàng hỏi ý nghĩa của mọi tên
khi họ đã biết khái niệm bằng một tên khác.
Tên AccountVisitor có ý nghĩa rất lớn đối với một lập trình viên đã quen thuộc với mẫu V ISITOR. Lập trình viên nào không biết JobQueue là gì? Có rất nhiều thứ rất kỹ thuật mà các lập trình viên phải làm. Chọn tên kỹ thuật cho những thứ đó thường là khóa học thích hợp nhất.

## Use Problem Domain Names
Khi không có "lập trình viên" cho những gì bạn đang làm, hãy sử dụng tên từ miền xác thực. Ít nhất thì lập trình viên duy trì mã của bạn có thể hỏi một chuyên gia tên miền
ý nghĩa của nó.
Tách các khái niệm miền giải pháp và miền vấn đề là một phần công việc của một chuyên gia phân loại và thiết kế giỏi. Mã liên quan nhiều hơn đến khái niệm miền có vấn đề nên có tên được rút ra từ miền có vấn đề.

## Add Meaningful Context
Có một vài cái tên có ý nghĩa về bản thân - hầu hết đều không. Thay vào đó, bạn cần đặt tên theo ngữ cảnh cho người đọc của mình bằng cách đặt chúng bằng tên phù hợp
các lớp, hàm hoặc không gian tên. Khi tất cả những cách khác không thành công, thì tiền tố tên có thể không cần thiết như một phương sách cuối cùng.

Hãy tưởng tượng rằng bạn có các biến có tên firstName, lastName, street, houseNumber, city, state và zipcode. Tổng hợp lại, chúng ta thấy khá rõ ràng rằng chúng tạo thành một địa chỉ. Nhưng điều gì sẽ xảy ra nếu bạn chỉ thấy biến trạng thái được sử dụng một mình trong một phương thức? Bạn có tự động không
suy ra rằng nó là một phần của địa chỉ?
Bạn có thể thêm ngữ cảnh bằng cách sử dụng các tiền tố: addrFirstName, addrLastName, addrState, v.v. Ít nhất người đọc sẽ hiểu rằng các biến này là một phần của cấu trúc lớn hơn. Của
nhiên, một giải pháp tốt hơn là tạo một lớp có tên Địa chỉ. Sau đó, ngay cả trình biên dịch cũng biết rằng các biến thuộc về một khái niệm lớn hơn.
Hãy xem xét phương pháp trong Liệt kê 2-1. Các biến có cần một văn bản có ý nghĩa hơn không? Tên hàm chỉ cung cấp một phần ngữ cảnh; thuật toán cung cấp phần còn lại.
Sau khi bạn đọc qua hàm, bạn sẽ thấy rằng ba biến, number, verb và pluralModifier, là một phần của thông báo "đoán thống kê". Thật không may, bối cảnh phải được suy ra. Khi bạn lần đầu tiên nhìn vào phương pháp này, ý nghĩa của các biến là không rõ ràng.


## Don’t Add Gratuitous Context
Trong một ứng dụng tưởng tượng có tên “Gas Station Deluxe”, bạn nên đặt tiền tố cho mọi lớp bằng GSD. Thành thật mà nói, bạn đang làm việc chống lại các công cụ của bạn. Bạn gõ G và nhấn phím kết hợp và được thưởng bằng một danh sách dài hàng dặm về mọi lớp trong hệ thống. Đó là khôn ngoan? Tại sao IDE khó giúp bạn?
Tương tự như vậy, giả sử bạn đã phát minh ra lớp MailingAddress trong mô-đun kế toán của GSD và bạn đặt tên nó là GSDAccountAddress. Sau đó, bạn cần một địa chỉ gửi thư cho khách hàng của bạn-
ứng dụng nguyên vẹn. Bạn có sử dụng GSDAccountAddress không? Nghe có giống như tên đúng không? Mười ký tự là thừa hoặc không liên quan.

Tên ngắn hơn thường tốt hơn tên dài hơn, miễn là chúng rõ ràng. Không thêm ngữ cảnh nào vào tên hơn mức cần thiết.
Tên accountAddress và customerAddress là những tên phù hợp cho các trường hợp của Địa chỉ lớp nhưng có thể là tên nghèo cho các lớp. Địa chỉ là một cái tên tốt cho một lớp học. Nếu tôi cần phân biệt giữa địa chỉ MAC, địa chỉ cổng và địa chỉ Web, tôi có thể
hãy xem xét địa chỉ bưu điện, MAC và URI. Các tên kết quả chính xác hơn, đó là điểm của tất cả các cách đặt tên.


## Final Words
Điều khó nhất của việc chọn tên hay là nó đòi hỏi kỹ năng mô tả tốt và nền tảng văn hóa chung. Đây là một vấn đề giảng dạy hơn là một vấn đề kỹ thuật, kinh doanh hoặc
vấn đề quản lý. Do đó, nhiều người trong lĩnh vực này không học cách làm tốt.
Mọi người cũng sợ đổi tên mọi thứ vì sợ rằng một số nhà phát triển khác sẽ phản đối. Chúng tôi không chia sẻ nỗi sợ hãi đó và thấy rằng chúng tôi thực sự biết ơn khi tên thay đổi (tốt hơn). Hầu hết thời gian chúng ta không thực sự ghi nhớ tên của các lớp và meth-ods. Chúng tôi sử dụng các công cụ hiện đại để xử lý các chi tiết như vậy để chúng tôi có thể tập trung vào việc mã đọc giống như đoạn văn và câu hay ít nhất là giống như bảng và cấu trúc dữ liệu (thông thường không phải lúc nào cũng là cách tốt nhất để hiển thị dữ liệu). Bạn có thể sẽ gây ngạc nhiên cho một số người khi bạn đổi tên, giống như bạn có thể làm với bất kỳ cải tiến mã nào khác. Đừng để nó cản bước bạn.
Thực hiện theo một số quy tắc này và xem liệu bạn có không cải thiện khả năng đọc của mã của mình hay không. Nếu bạn đang duy trì mã của người khác, hãy sử dụng các công cụ tái cấu trúc để giúp giải quyết những vấn đề này. Nó sẽ trả hết trong ngắn hạn và tiếp tục trả về lâu dài.
