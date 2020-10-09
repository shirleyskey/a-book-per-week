# Chapter 03: Function 


## Small!
## Do One Thing

### Sections within Functions

## One Level of Abstraction per Function

### Reading Code from Top to Bottom: The Stepdown Rule

## Switch Statements

## Use Descriptive Names

## Function Arguments
Số đối số lý tưởng cho một hàm là
không (niladic). Tiếp theo là một (đơn nguyên), theo sau
gần bằng hai (dyadic). Ba đối số (bộ ba)
nên tránh nếu có thể. Hơn ba
(polyadic) yêu cầu sự biện minh rất đặc biệt — và
sau đó không nên được sử dụng.
Lập luận thật khó. Họ mất rất nhiều ...
năng lượng tinh thể. Đó là lý do tại sao tôi đã loại bỏ gần như tất cả
chúng từ ví dụ. Ví dụ, hãy xem xét
StringBuffer trong ví dụ. Chúng ta có thể có
thông qua nó như một cuộc tranh cãi hơn là mak-
nhập vào nó một biến phiên bản, nhưng sau đó người đọc
sẽ phải giải thích nó mỗi khi họ nhìn thấy
nó. Khi bạn đang đọc câu chuyện được kể bởi
module, includeSetupPage () dễ hiểu hơn includeSetupPageInto (newPage-
Nội dung) . Đối số ở cấp độ trừu tượng khác với tên hàm và buộc bạn phải biết một chi tiết (nói cách khác, StringBuffer) không đặc biệt quan trọng tại thời điểm đó.
Lập luận thậm chí còn khó hơn từ quan điểm thử nghiệm. Hãy tưởng tượng khó khăn khi viết tất cả các trường hợp kiểm thử để đảm bảo rằng tất cả các kết hợp khác nhau của các đối số hoạt động đúng. Nếu không có đối số, điều này là tầm thường. Nếu có một lập luận, nó không quá khó.
Với hai đối số, vấn đề trở nên khó khăn hơn một chút. Với hơn hai lập luận, việc kiểm tra mọi kết hợp của các giá trị thích hợp có thể khó khăn.

Đối số đầu ra khó hiểu hơn đối số đầu vào. Khi chúng ta đọc một hàm, chúng ta đã quen với ý tưởng thông tin đi vào hàm thông qua các đối số và đi ra ngoài thông qua giá trị trả về. Chúng tôi thường không mong đợi thông tin sẽ xuất hiện
thông qua các lập luận. Vì vậy, các đối số đầu ra thường khiến chúng ta thực hiện phép tính kép.
Một đối số đầu vào là điều tốt nhất tiếp theo để không có đối số. SetupTeardown- includeer.render (pageData) khá dễ hiểu. Rõ ràng là chúng tôi sẽ kết xuất
dữ liệu trong đối tượng pageData.

### Common Monadic Forms
Các dạng đơn nguyên phổ biến
Có hai lý do rất phổ biến để truyền một đối số vào một hàm. Bạn có thể đặt câu hỏi về đối số đó, như trong tệp boolean fileExists (“MyFile”). Hoặc bạn có thể
hoạt động trên đối số đó, biến đổi nó thành một thứ khác và trả lại nó. Đối với
ví dụ, InputStream fileOpen (“MyFile”) biến đổi chuỗi tên tệp thành chuỗi
Giá trị trả về InputStream. Hai cách sử dụng này là những gì người đọc mong đợi khi họ nhìn thấy một func-
sự. Bạn nên chọn những cái tên giúp phân biệt rõ ràng và luôn sử dụng cả hai
hình thành trong một bối cảnh nhất quán. (Xem Phân tách Truy vấn Lệnh bên dưới.)
Một dạng hơi ít phổ biến hơn, nhưng vẫn rất hữu ích cho một hàm đối số,
là một sự kiện. Trong biểu mẫu này có một đối số đầu vào nhưng không có đối số đầu ra. Tổng thể
chương trình có nghĩa là giải thích lời gọi hàm như một sự kiện và sử dụng đối số để thay đổi
trạng thái của hệ thống, ví dụ: void passwordAttemptFailedNtimes (int lần thử). Sử dụng
biểu mẫu này một cách cẩn thận. Người đọc phải rất rõ ràng rằng đây là một sự kiện. Chọn
tên và ngữ cảnh cẩn thận.
Cố gắng tránh bất kỳ hàm đơn nguyên nào không tuân theo các biểu mẫu này, ví dụ: void
includeSetupPageInto (StringBuffer pageText). Sử dụng một đối số đầu ra thay vì một
giá trị trả về cho một phép biến đổi là khó hiểu. Nếu một hàm sẽ chuyển đổi đầu vào của nó
đối số, phép biến đổi sẽ xuất hiện dưới dạng giá trị trả về. Thật vậy, StringBuffer
biến đổi (StringBuffer in) tốt hơn void biến đổi- (StringBuffer out), ngay cả khi
việc triển khai trong trường hợp đầu tiên chỉ đơn giản là trả về đối số đầu vào. Ít nhất nó vẫn theo sau
dạng của một phép biến hình.
### Flag Arguments
Đối số cờ là xấu. Truyền một boolean vào một hàm là một việc thực sự khủng khiếp. Nó ngay lập tức làm phức tạp chữ ký của phương thức, lớn tiếng tuyên bố rằng hàm này thực hiện nhiều hơn một việc. Nó thực hiện một việc nếu cờ đúng và một việc khác nếu cờ sai!
Trong Liệt kê 3-7, chúng tôi không có lựa chọn nào khác vì những người gọi đã chuyển cờ đó và tôi muốn giới hạn phạm vi tái cấu trúc cho hàm và bên dưới. Tuy nhiên, phương thức gọi render (true) dễ gây nhầm lẫn cho người đọc kém. Di chuột qua cuộc gọi và xem kết xuất (boolean isSuite) giúp một chút, nhưng không nhiều. Chúng ta nên chia hàm thành hai: renderForSuite () và renderForSingleTest ().
### Dyadic Functions
Một hàm có hai đối số khó hiểu hơn một hàm đơn nguyên. Đối với exam-ple, writeField (tên) dễ hiểu hơn writeField (output-Stream, name). 10
Mặc dù ý nghĩa của cả hai đều rõ ràng, nhưng cái nhìn đầu tiên lướt qua mắt, dễ dàng lắng đọng ý nghĩa của nó. Thứ hai yêu cầu tạm dừng ngắn cho đến khi chúng ta học cách bỏ qua tham số đầu tiên.
Và điều đó, tất nhiên, cuối cùng dẫn đến các vấn đề vì chúng ta không bao giờ được bỏ qua bất kỳ phần nào của mã. Những phần chúng tôi bỏ qua là nơi mà các lỗi sẽ ẩn.
Tất nhiên, có những lúc, hai đối số là thích hợp. Ví dụ,
Point p = new Point (0,0); là hoàn toàn hợp lý. Điểm Descartes đương nhiên có hai đối số. Thật vậy, chúng tôi sẽ rất ngạc nhiên khi thấy Điểm mới (0). Tuy nhiên, hai đối số trong trường hợp này là các thành phần có thứ tự của một giá trị duy nhất! Trong khi đầu ra-Luồng và
tên không có sự gắn kết tự nhiên, cũng không có thứ tự tự nhiên.
Ngay cả các hàm dyadic rõ ràng như khẳng định Equals (dự kiến, thực tế) cũng có vấn đề.
Đã bao nhiêu lần bạn đặt thực tế ở nơi mong đợi? Hai người lập luận không có trật tự tự nhiên. Thứ tự mong đợi, thực tế là một quy ước đòi hỏi thực hành để học hỏi.
Dyads không phải là ác, và bạn chắc chắn sẽ phải viết chúng. Tuy nhiên, bạn nên biết rằng chúng phải trả giá và nên tận dụng những gì mà thợ cơ khí có thể
có sẵn cho bạn để chuyển đổi chúng thành monads. Ví dụ: bạn có thể làm cho
writeField phương thức một thành viên của outputStream để bạn có thể nói outputStream.
writeField (tên). Hoặc bạn có thể đặt outputStream thành một biến thành viên của dòng
lớp để bạn không phải vượt qua nó. Hoặc bạn có thể trích xuất một lớp mới như FieldWriter
lấy outputStream trong hàm tạo của nó và có một phương thức ghi.

### Triads
Các hàm sử dụng ba đối số khó hiểu hơn đáng kể so với hàm hàm. Các vấn đề về thứ tự, tạm dừng và bỏ qua tăng hơn gấp đôi. Tôi khuyên bạn nên suy nghĩ thật kỹ trước khi tạo một bộ ba.
Ví dụ, hãy xem xét tình trạng quá tải thông thường của khẳng định có ba đối số: khẳng địnhEquals (thông báo, dự kiến, thực tế). Đã bao nhiêu lần bạn đọc tin nhắn và nghĩ rằng nó đúng như mong đợi? Tôi đã vấp ngã và tạm dừng về điều đó
bộ ba nhiều lần. Trên thực tế, mỗi khi tôi nhìn thấy nó, tôi thực hiện hai lần và sau đó học cách bỏ qua thông báo.
Mặt khác, đây là một bộ ba không quá xảo quyệt: khẳng địnhEquals (1,0, số tiền, 0,001). Mặc dù điều này vẫn yêu cầu thực hiện hai lần, nhưng đó là một trong những điều đáng để thực hiện. Luôn luôn tốt khi được nhắc nhở rằng sự bình đẳng của các giá trị dấu phẩy động là một điều tương đối.


### Argument Objects
Khi một hàm dường như cần nhiều hơn hai hoặc ba đối số, có khả năng là một số đối số đó phải được gói vào một lớp của riêng chúng. Hãy xem xét, ví dụ,
sự khác biệt giữa hai khai báo sau:
Circle makeCircle (gấp đôi x, gấp đôi y, gấp đôi bán kính);
Circle makeCircle (Tâm điểm, bán kính gấp đôi);
Giảm số lượng đối số bằng cách tạo các đối tượng từ chúng có vẻ giống như gian lận, nhưng không phải vậy. Khi các nhóm biến được chuyển cùng nhau, theo cách x và y trong ví dụ trên, chúng có thể là một phần của một khái niệm xứng đáng với tên riêng của nó.

### Argument Lists
Đôi khi chúng ta muốn truyền một số biến đối số vào một hàm. Ví dụ, hãy xem xét phương thức String.format:
String.format ("% s đã làm việc% .2f giờ.", Tên, giờ);
Nếu tất cả các đối số biến đều được xử lý giống nhau, như trong ví dụ trên, thì chúng tương đương với một đối số duy nhất của kiểu Danh sách. Theo lý luận đó, String.format là
thực sự là loạn. Thật vậy, khai báo của String.format như hình dưới đây rõ ràng là không hợp lý.
định dạng chuỗi công khai (Định dạng chuỗi, Đối tượng ... args)
Vì vậy, tất cả các quy tắc tương tự được áp dụng. Các hàm nhận đối số thay đổi có thể là monads, dyads hoặc thậm chí là triads. Nhưng sẽ là một sai lầm nếu đưa ra nhiều lý lẽ hơn thế.
void monad (Số nguyên ... args);
void dyad (Tên chuỗi, Số nguyên ... args);
void triad (String name, int count, Integer ... args);

### Verbs and Keywords
Việc chọn tên hay cho một hàm có thể giúp bạn giải thích mục đích của hàm cũng như thứ tự và ý định của các đối số. Trong trường hợp đơn nguyên, chức năng và đối số sẽ tạo thành một cặp động từ / danh từ rất đẹp. Ví dụ, viết (tên) rất gợi. Dù thứ “tên” này là gì, nó đang được “viết”. An
thậm chí tên tốt hơn có thể là writeField (tên), cho chúng ta biết rằng thứ “tên” là
"cánh đồng."
Cuối cùng, đây là một ví dụ về dạng từ khóa của một tên hàm. Sử dụng biểu mẫu này, chúng tôi mã hóa tên của các đối số thành tên hàm. Ví dụ: khẳng định
tốt hơn có thể được viết dưới dạng khẳng định là SwiftEqualsActual (dự kiến, thực tế). Điều này giúp giảm nhẹ vấn đề phải nhớ thứ tự của các đối số.


## Have No Side Effects
Tác dụng phụ là dối trá. Hàm của bạn hứa hẹn làm một việc, nhưng nó cũng làm những việc ẩn khác. Đôi khi nó sẽ thực hiện những thay đổi bất ngờ đối với các biến của lớp riêng của nó.
Đôi khi, nó sẽ biến chúng thành các tham số được truyền vào hàm hoặc đến các trang hệ thống. Trong cả hai trường hợp, chúng là những sai lầm quanh co và gây tổn hại thường dẫn đến các mối ghép thời gian kỳ lạ và sự phụ thuộc vào trật tự.
Ví dụ, hãy xem xét hàm dường như vô hại trong Liệt kê 3-6. Chức năng này
sử dụng một thuật toán chuẩn để đối sánh userName với mật khẩu. Nó trả về true nếu chúng khớp và false nếu có gì sai. Nhưng nó cũng có một tác dụng phụ. Bạn có thể phát hiện ra nó không?
Liệt kê 3-6
UserValidator.java
lớp công khai UserValidator {
chuyên gia mật mã Cryptographer riêng;
public boolean checkPassword (String userName, String password) {
Người dùng người dùng = UserGateway.findByName (userName);
if (user! = User.NULL) {
String codedPhrase = user.getPhraseEncodedByPassword ();
Cụm từ chuỗi = cryptographer.decrypt (mã hóaPhrase, mật khẩu);
if ("Mật khẩu hợp lệ" .equals (cụm từ)) {
Session.initialize ();
trả về true;
}
}
trả về sai;
}
}
Tất nhiên, tác dụng phụ là lệnh gọi Session.initialize (). Tên func-tion checkPassword nói rằng nó kiểm tra mật khẩu. Tên không ngụ ý rằng nó viết tắt-
izes phiên. Vì vậy, một người gọi tin vào những gì tên của hàm nói sẽ có nguy cơ
xóa dữ liệu phiên hiện có khi người đó quyết định kiểm tra tính hợp lệ của người dùng.
Tác dụng phụ này tạo ra một khớp nối thời gian. Nghĩa là, checkPassword chỉ có thể được gọi vào những thời điểm nhất định (nói cách khác, khi an toàn để khởi tạo phiên). Nếu nó được gọi không theo thứ tự, dữ liệu phiên có thể vô tình bị mất. Các khớp nối tạm thời là
hợp nhất, đặc biệt là khi ẩn dưới dạng tác dụng phụ. Nếu bạn phải có một khớp nối thời gian, bạn nên làm rõ nó trong tên của hàm. Trong trường hợp này, chúng tôi có thể đổi tên
function checkPasswordAndInitializeSession, mặc dù điều đó chắc chắn vi phạm “Do one
Điều."

### Output Arguments
Các đối số được hiểu một cách tự nhiên nhất là đầu vào cho một hàm. Nếu bạn đã lập luận trong hơn một vài năm, tôi chắc chắn rằng bạn đã lập luận kỹ lưỡng
đó thực sự là một đầu ra hơn là một đầu vào. Ví dụ:
appendFooter (các);
Hàm này có nối s làm chân trang cho một cái gì đó không? Hay nó nối một số footer vào s? S là đầu vào hay đầu ra? Không mất nhiều thời gian để nhìn vào chữ ký hàm và thấy:
public void appendFooter (báo cáo StringBuffer)
Điều này làm rõ vấn đề, nhưng chỉ ở chi phí kiểm tra khai báo của chức năng. Bất cứ điều gì buộc bạn phải kiểm tra chữ ký hàm tương đương với việc thực hiện hai lần. Nó là
một sự phá vỡ nhận thức và nên tránh.
Trong những ngày trước khi lập trình hướng đối tượng, đôi khi cần có các đối số đầu ra. Tuy nhiên, phần lớn nhu cầu đối số đầu ra biến mất trong OO lan-
guages ​​vì ​​điều này nhằm hoạt động như một đối số đầu ra. Nói cách khác, sẽ tốt hơn nếu appendFooter được gọi là
report.appendFooter ();
Nói chung nên tránh các đối số đầu ra. Nếu hàm của bạn phải thay đổi trạng thái của một thứ gì đó, hãy yêu cầu nó thay đổi trạng thái của đối tượng sở hữu nó

## Command Query Separation
Các hàm nên làm một cái gì đó hoặc trả lời một cái gì đó, nhưng không phải cả hai. Hàm của bạn sẽ thay đổi trạng thái của một đối tượng hoặc nó sẽ trả về một số thông tin về đối tượng đó. Làm cả hai thường dẫn đến nhầm lẫn. Ví dụ, hãy xem xét những điều sau
chức năng:
public boolean set (Thuộc tính chuỗi, Giá trị chuỗi);
Hàm này đặt giá trị của một thuộc tính được đặt tên và trả về true nếu nó thành công và
false nếu không có thuộc tính như vậy tồn tại. Điều này dẫn đến các tuyên bố kỳ quặc như sau:
if (set ("tên người dùng", "Unclebob")) ...
Hãy tưởng tượng điều này từ quan điểm của người đọc. Nó có nghĩa là gì? Nó đang hỏi liệu
thuộc tính "tên người dùng" trước đây đã được đặt thành "Unclebob"? Hay nó đang hỏi liệu
Thuộc tính "tên người dùng" đã được đặt thành công thành "Unclebob"? Thật khó để suy ra ý nghĩa từ
cuộc gọi vì không rõ từ “set” là động từ hay tính từ.
Tác giả dự định đặt là một động từ, nhưng trong ngữ cảnh của câu lệnh if, cảm giác như
một tính từ. Vì vậy, câu lệnh đọc là "Nếu thuộc tính tên người dùng trước đó được đặt thành
Unclebob ”chứ không phải“ đặt thuộc tính tên người dùng thành Unclebob và nếu điều đó hoạt động sau đó. . . . ” Chúng tôi

có thể cố gắng giải quyết vấn đề này bằng cách đổi tên hàm set thành setAndCheckIfExists, nhưng điều đó không giúp ích nhiều cho khả năng đọc của câu lệnh if. Giải pháp thực sự là tách
lệnh từ truy vấn để không thể xảy ra sự mơ hồ.
if (thuộc tínhExists ("tên người dùng")) {
setAttribute ("tên người dùng", "Unclebob");
...
}

## Prefer Exceptions to Returning Error Codes
Trả lại mã lỗi từ các hàm lệnh là một vi phạm nhỏ đối với truy vấn lệnh
tách biệt. Nó thúc đẩy các lệnh được sử dụng làm biểu thức trong các vị từ của trạng thái if-
ments.
if (deletePage (trang) == E_OK)
Điều này không gây nhầm lẫn động từ / tính từ nhưng dẫn đến cấu trúc lồng nhau sâu sắc
chữa bệnh. Khi bạn trả về mã lỗi, bạn tạo ra sự cố mà người gọi phải giải quyết
lỗi ngay lập tức.
if (deletePage (trang) == E_OK) {
if (registry.deleteReference (page.name) == E_OK) {
if (configKeys.deleteKey (page.name.makeKey ()) == E_OK) {
logger.log ("trang bị xóa");
} khác {
logger.log ("configKey không bị xóa");
}
} khác {
logger.log ("deleteReference from registry failed");
}
} khác {
logger.log ("xóa không thành công");
trả về E_ERROR;
}
Mặt khác, nếu bạn sử dụng ngoại lệ thay vì mã lỗi trả về, thì lỗi
mã xử lý có thể được tách khỏi mã đường dẫn hạnh phúc và có thể được đơn giản hóa:
thử {
deletePage (trang);
registry.deleteReference (page.name);
configKeys.deleteKey (page.name.makeKey ());
}
bắt (Ngoại lệ e) {
logger.log (e.getMessage ());
}
### Extract Try/Catch Blocks
Các khối try / catch là xấu theo đúng nghĩa của chúng. Họ nhầm lẫn cấu trúc của mã và
trộn xử lý lỗi với xử lý thông thường. Vì vậy, tốt hơn là trích xuất các cơ quan của thử
và bắt các khối thành các chức năng của riêng chúng.
www.it-ebooks.info Dự phòng Ngoại lệ để Trả lại Mã Lỗi
47
public void delete (Trang page) {
thử {
deletePageAndAllRefferences (trang);
}
bắt (Ngoại lệ e) {
logError (e);
}
}
private void deletePageAndAllRefutions (Trang page) ném Exception {
deletePage (trang);
registry.deleteReference (page.name);
configKeys.deleteKey (page.name.makeKey ());
}
private void logError (Exception e) {
logger.log (e.getMessage ());
}
Ở trên, chức năng xóa là tất cả về xử lý lỗi. Dễ hiểu rồi bỏ qua. Chức năng deletePageAndAllRefferences là tất cả về quá trình xóa hoàn toàn một trang. Xử lý lỗi có thể được bỏ qua. Điều này cung cấp một sự tách biệt tốt đẹp
làm cho mã dễ hiểu và dễ sửa đổi hơn.


### Error Handling Is One Thing
Các hàm nên làm một việc. Giao lỗi là một chuyện. Vì vậy, một chức năng xử lý lỗi không nên làm gì khác. Điều này ngụ ý (như trong ví dụ trên) rằng nếu từ khóa
try tồn tại trong một hàm, nó phải là từ đầu tiên trong hàm và không được có gì sau các khối catch / final.


###  The Error.java Dependency Magnet
Các hàm nên làm một việc. Giao lỗi là một chuyện. Vì vậy, một chức năng xử lý lỗi không nên làm gì khác. Điều này ngụ ý (như trong ví dụ trên) rằng nếu từ khóa try tồn tại trong một hàm, thì nó phải là từ đầu tiên trong hàm và rằng ở đó
sẽ không có gì sau khối bắt / cuối cùng.
Nam châm phụ thuộc Error.java
Trả về mã lỗi thường ngụ ý rằng có một số lớp hoặc enum trong đó tất cả các mã lỗi được xác định.
public enum Error {
ĐỒNG Ý,
KHÔNG HỢP LỆ,
KHÔNG CÓ NHƯ VẬY,
ĐÃ KHÓA,
OUT_OF_RESOURCES,
CHỜ_NGỢI_PHẦN;
}
Các lớp học như thế này là một nam châm phụ thuộc; nhiều lớp khác phải nhập và sử dụng chúng. Do đó, khi Error enum thay đổi, tất cả các lớp khác cần được biên dịch lại
và triển khai lại. 11 Điều này gây áp lực tiêu cực lên lớp Lỗi. Các lập trình viên không muốn Những người cảm thấy rằng họ có thể bỏ đi mà không cần biên dịch lại và sử dụng lại đã được tìm thấy — và bị xử lý.

để thêm lỗi mới vì sau đó họ phải xây dựng lại và triển khai lại mọi thứ. Vì vậy, họ sử dụng lại các mã lỗi cũ thay vì thêm mã mới.
Khi bạn sử dụng các ngoại lệ thay vì mã lỗi, thì các ngoại lệ mới là các dẫn xuất của lớp ngoại lệ. Chúng có thể được thêm vào mà không cần phải biên dịch lại hoặc triển khai lại. 12

## Don’t Repeat Yourself 13
Nhìn lại Liệt kê 3-1 một cách cẩn thận và bạn
sẽ nhận thấy rằng có một thuật toán
được lặp lại bốn lần, một lần cho mỗi
SetUp, SuiteSetUp, TearDown và
Các trường hợp SuiteTearDown. Không dễ phát hiện
sự trùng lặp này bởi vì bốn trường hợp
được trộn lẫn với mã khác và không
nhân bản đồng nhất. Tuy nhiên, sự trùng lặp
là một vấn đề vì nó làm phồng mã và
sẽ yêu cầu sửa đổi gấp bốn lần nếu thuật toán phải thay đổi. Đó cũng là một cơ hội gấp bốn lần cho một lỗi sơ sót.
Sự trùng lặp này đã được khắc phục bằng phương thức include trong Liệt kê 3-7. Đọc lại đoạn mã đó và để ý xem khả năng đọc của toàn bộ mô-đun được nâng cao như thế nào nhờ việc giảm sự trùng lặp đó.
Sao chép có thể là gốc rễ của mọi điều xấu trong phần mềm. Nhiều nguyên tắc và thực hành đã được tạo ra với mục đích kiểm soát hoặc loại bỏ nó. Ví dụ: hãy xem xét rằng tất cả các biểu mẫu bình thường trong cơ sở dữ liệu của Codd đều dùng để loại bỏ sự trùng lặp trong dữ liệu. Cũng hãy xem xét cách lập trình hướng đối tượng phục vụ để tập trung mã vào các lớp cơ sở mà nếu không sẽ là dư thừa. Lập trình có cấu trúc, Lập trình hướng theo khía cạnh, Lập trình định hướng tổng hợp, một phần là tất cả các chiến lược để loại bỏ sự trùng lặp. Có vẻ như kể từ khi phát minh ra chương trình con, các đổi mới trong phần mềm phát triển-
đã là một nỗ lực không ngừng để loại bỏ sự trùng lặp khỏi mã nguồn của chúng tôi.


## Structured Programming
Một số lập trình viên tuân theo các quy tắc lập trình có cấu trúc của Edsger Dijkstra.
nói rằng mọi hàm, và mọi khối trong một hàm, nên có một lối vào và một lối ra. Tuân theo các quy tắc này có nghĩa là chỉ nên có một câu lệnh trả về trong một hàm-
tion, không có câu lệnh break hoặc continue trong một vòng lặp và không bao giờ, bất kỳ câu lệnh goto nào.
12. Đây là một ví dụ về Nguyên tắc đóng mở (OCP) [PPP02].
13. Nguyên tắc KHÔ. [PRAG].
14. [SP72].

Mặc dù chúng ta thông cảm với các mục tiêu và nguyên tắc của lập trình có cấu trúc, nhưng những quy tắc đó không mang lại nhiều lợi ích khi các hàm rất nhỏ. Chỉ trong các chức năng lớn hơn, các quy tắc như vậy mới mang lại lợi ích đáng kể.
Vì vậy, nếu bạn giữ cho các hàm của mình nhỏ, thì câu lệnh return, break hoặc continue thường xuyên không gây hại gì và đôi khi thậm chí có thể biểu đạt nhiều hơn tội
quy tắc gle-entry, single-exit. Mặt khác, goto chỉ có ý nghĩa trong các chức năng lớn, vì vậy nó nên được tránh.

## How Do You Write Functions Like This?
Phần mềm viết cũng giống như bất kỳ loại văn bản nào khác. Khi bạn viết một bài báo hoặc một bài báo, trước tiên bạn phải đưa suy nghĩ của mình xuống, sau đó bạn xoa bóp nó cho đến khi nó đọc tốt. Bản nháp đầu tiên có thể vụng về và vô tổ chức, vì vậy bạn soạn thảo từ ngữ, cấu trúc lại và tinh chỉnh nó cho đến khi nó đọc theo cách bạn muốn.
Khi tôi viết các hàm, chúng dài và phức tạp. Chúng có rất nhiều vòng lặp thụt vào và lồng vào nhau. Họ có danh sách đối số dài. Tên là tùy ý và có mã trùng lặp. Nhưng tôi cũng có một bộ các bài kiểm tra đơn vị bao gồm mọi
dòng mã vụng về.
Vì vậy, sau đó tôi xoa bóp và tinh chỉnh mã đó, tách ra các chức năng, thay đổi tên, loại bỏ sự trùng lặp. Tôi thu nhỏ các phương pháp và sắp xếp lại chúng. Đôi khi tôi phá vỡ toàn bộ lớp học, trong khi vẫn giữ cho các bài kiểm tra trôi qua.
Cuối cùng, tôi kết thúc với các hàm tuân theo các quy tắc mà tôi đã trình bày trong chương này. Tôi không viết chúng theo cách đó để bắt đầu. Tôi không nghĩ có ai có thể làm được.

## Conclusion
Mọi hệ thống đều được xây dựng từ một ngôn ngữ dành riêng cho miền được lập trình viên thiết kế để mô tả hệ thống đó. Chức năng là động từ của ngôn ngữ đó, và các lớp là danh từ.
Đây không phải là một số quay ngược lại quan niệm cũ ghê tởm rằng danh từ và động từ trong tài liệu request-ments là dự đoán đầu tiên về các lớp và chức năng của một hệ thống. Đúng hơn, đây là
một sự thật cũ hơn nhiều. Nghệ thuật lập trình luôn là nghệ thuật của thiết kế ngôn ngữ.
Các lập trình viên bậc thầy nghĩ về hệ thống như những câu chuyện được kể hơn là những chương trình được viết. Họ sử dụng các phương tiện của ngôn ngữ lập trình mà họ đã chọn để xây dựng một ngôn ngữ phong phú và biểu cảm hơn nhiều có thể được sử dụng để kể câu chuyện đó. Một phần của điều đó
ngôn ngữ miền cụ thể là hệ thống phân cấp các chức năng mô tả tất cả các hành động diễn ra trong hệ thống đó. Trong một hành động đệ quy đầy nghệ thuật, những hành động đó được ghi vào
sử dụng ngôn ngữ theo miền cụ thể mà họ xác định để kể phần nhỏ câu chuyện của riêng họ.
Chương này đã nói về cơ chế viết hàm. Nếu bạn tuân theo các quy tắc ở đây, các hàm của bạn sẽ ngắn gọn, được đặt tên tốt và được tổ chức độc đáo. Nhưng

đừng bao giờ quên rằng mục tiêu thực sự của bạn là kể câu chuyện của hệ thống và các chức năng bạn viết cần phải khớp một cách rõ ràng với nhau thành một ngôn ngữ rõ ràng và chính xác để giúp bạn kể điều đó.

