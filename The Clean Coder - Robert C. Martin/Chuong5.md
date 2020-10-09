# Chapter 05: Test Driven Development 
Đã hơn mười năm kể từ khi Phát triển theo hướng thử nghiệm (TDD) ra mắt lần đầu
trong ngành công nghiệp. Nó là một phần của làn sóng Lập trình Cực đoan (XP), nhưng
kể từ đó đã được Scrum áp dụng và hầu như tất cả các phương pháp Agile khác.
Ngay cả các nhóm không Agile cũng thực hành TDD.
Vào năm 1998, lần đầu tiên tôi nghe nói về “Lập trình thử nghiệm đầu tiên”, tôi đã nghi ngờ. WHO
sẽ không? Viết bài kiểm tra đơn vị của bạn trước? Ai sẽ làm một điều ngốc nghếch như thế?
77C CHƯƠNG 5
HƯỚNG PHÁT TRIỂN THỬ NGHIỆM
Nhưng tôi đã là một lập trình viên chuyên nghiệp được ba mươi năm rồi và tôi đã thấy
mọi thứ đến và đi trong ngành. Tôi biết tốt hơn là nên gạt bỏ bất cứ điều gì
đặc biệt là khi một người như Kent Beck nói điều đó.
Vì vậy, vào năm 1999, tôi đã đến Medford, Oregon, để gặp Kent và tìm hiểu
kỷ luật từ anh ta. Toàn bộ trải nghiệm là một cú sốc!
Kent và tôi ngồi xuống văn phòng của anh ấy và bắt đầu giải mã một số vấn đề nhỏ đơn giản
trong Java. Tôi chỉ muốn viết điều ngớ ngẩn. Nhưng Kent chống lại và đưa tôi, bước
từng bước, thông qua quy trình. Đầu tiên, anh ấy viết một phần nhỏ của bài kiểm tra đơn vị, hầu như không
đủ điều kiện làm mã. Sau đó, anh ấy viết mã vừa đủ để thực hiện bài kiểm tra đó
biên dịch. Sau đó, anh ấy viết thêm một bài kiểm tra nhỏ, rồi nhiều mã hơn.
Thời gian chu kỳ hoàn toàn nằm ngoài kinh nghiệm của tôi. Tôi đã quen với việc viết
viết mã cho phần tốt hơn của một giờ trước khi cố gắng biên dịch hoặc chạy nó. Nhưng Kent
theo nghĩa đen đang thực thi mã của mình cứ sau 30 giây hoặc lâu hơn. Tôi đã kinh ngạc!
Hơn nữa, tôi đã nhận ra thời gian chu kỳ! Đó là loại thời gian chu kỳ tôi đã sử dụng
những năm trước khi còn là một đứa trẻ, 1 lập trình trò chơi bằng các ngôn ngữ thông dịch như Basic hoặc
Logo. Trong các ngôn ngữ đó, không có thời gian xây dựng, vì vậy bạn chỉ cần thêm một dòng mã
và sau đó thực thi. Bạn đi vòng quanh chu kỳ rất nhanh. Và vì lý do đó,
bạn có thể rất hiệu quả bằng những ngôn ngữ đó.
Nhưng trong lập trình thực tế, loại thời gian chu kỳ đó là vô lý. Trong thực tế
lập trình, bạn đã phải dành nhiều thời gian để viết mã, và sau đó là nhiều hơn nữa
thời gian để biên dịch. Và sau đó thậm chí nhiều thời gian hơn để gỡ lỗi nó. Tôi là một C ++
lập trình viên, chết tiệt! Và trong C ++, chúng tôi có thời gian xây dựng và liên kết
phút, đôi khi hàng giờ. Thời gian chu kỳ ba mươi giây là không thể tưởng tượng được.
Tuy nhiên, đã có Kent, nấu ăn chương trình Java này trong chu kỳ ba mươi giây
và không có bất kỳ dấu hiệu nào cho thấy anh ta sẽ sớm giảm tốc độ. Vì vậy, nó đã bắt đầu
tôi, trong khi tôi ngồi đó trong văn phòng của Kent, rằng sử dụng kỷ luật đơn giản này, tôi có thể
mã bằng ngôn ngữ thực với thời gian chu kỳ của Logo! Tôi đã bị mắc câu!


## T H E J U R Y I S I N
Kể từ những ngày đó, tôi đã biết rằng TDD không chỉ là một thủ thuật đơn giản để
rút ngắn thời gian chu kỳ của tôi. Kỷ luật có rất nhiều lợi ích mà tôi sẽ
mô tả trong các đoạn văn sau.
Nhưng trước tiên tôi cần nói điều này:
• Ban giám khảo đã vào cuộc!
• Cuộc tranh cãi đã kết thúc.
•
ĐI ĐẾN
Là có hại.
• Và TDD hoạt động.
Có, đã có rất nhiều blog và bài báo gây tranh cãi viết về TDD
trong những năm qua và vẫn còn. Trong những ngày đầu họ đã cố gắng nghiêm túc
phê bình và hiểu biết. Tuy nhiên, ngày nay chúng chỉ là những lời khen ngợi. Dưới cùng
là TDD hoạt động và mọi người cần phải vượt qua nó.
Tôi biết điều này nghe có vẻ cứng rắn và đơn phương, nhưng với thành tích thì tôi không nghĩ
bác sĩ phẫu thuật phải bảo vệ việc rửa tay và tôi không nghĩ rằng các nhà lập trình
nên phải bênh vực TDD.
Làm sao bạn có thể coi mình là một người chuyên nghiệp nếu bạn không biết tất cả
mã của bạn hoạt động? Làm thế nào bạn có thể biết tất cả mã của bạn hoạt động nếu bạn không kiểm tra nó
mỗi khi bạn thực hiện một thay đổi? Làm thế nào bạn có thể kiểm tra nó mỗi khi bạn thực hiện
thay đổi nếu bạn không có thử nghiệm đơn vị tự động với mức độ phù hợp rất cao? Có thể như thế nào
bạn nhận được các bài kiểm tra đơn vị tự động với độ phủ rất cao mà không cần thực hành TDD?
Câu cuối cùng đòi hỏi một số công phu. Chỉ TDD là gì?

### T H E T H R E E L AW S OF TD D
1. Bạn không được phép viết bất kỳ mã sản xuất nào cho đến khi bạn viết lần đầu tiên
một bài kiểm tra đơn vị không đạt.
2. Bạn không được phép viết nhiều bài kiểm tra đơn vị hơn mức đủ để không đạt — và
không biên dịch là không thành công.
3. Bạn không được phép viết thêm mã sản xuất đủ để vượt qua
bài kiểm tra đơn vị hiện đang thất bại.
Ba định luật này khóa bạn vào một chu kỳ, có lẽ dài ba mươi giây. Bạn
bắt đầu bằng cách viết một phần nhỏ của bài kiểm tra đơn vị. Nhưng trong vòng vài giây, bạn
phải đề cập đến tên của một số lớp hoặc hàm mà bạn chưa viết,
từ đó khiến unit test không biên dịch được. Vì vậy, bạn phải viết sản xuất
mã thực hiện biên dịch thử nghiệm. Nhưng bạn không thể viết nhiều hơn thế, vì vậy bạn
bắt đầu viết thêm mã kiểm tra đơn vị.
Làm tròn và làm tròn chu kỳ bạn đi. Thêm một chút vào mã kiểm tra. Thêm một chút vào
Mã sản xuất. Hai dòng mã phát triển đồng thời thành bổ sung
các thành phần. Các xét nghiệm phù hợp với mã sản xuất giống như kháng thể phù hợp với kháng nguyên.

### T H E L I TA N Y OF B ENEFITS
#### Certainty
Nếu bạn áp dụng TDD như một kỷ luật chuyên nghiệp, thì bạn sẽ viết hàng tá
bài kiểm tra mỗi ngày, hàng trăm bài kiểm tra mỗi tuần và hàng nghìn bài kiểm tra mỗi năm.
Và bạn sẽ giữ tất cả các bài kiểm tra đó trong tay và chạy chúng bất kỳ lúc nào bạn thực hiện
thay đổi mã.
Tôi là tác giả chính và người duy trì FitNesse, 2 chấp nhận dựa trên Java
công cụ kiểm tra. Tính đến thời điểm này, FitNesse viết được 64.000 dòng mã, trong đó 28.000
chỉ có trong hơn 2.200 bài kiểm tra đơn vị riêng lẻ. Các bài kiểm tra này bao gồm ít nhất
90% của mã sản xuất 3 và mất khoảng 90 giây để chạy.
Bất cứ khi nào tôi thay đổi bất kỳ phần nào của FitNesse, tôi chỉ cần chạy các bài kiểm tra đơn vị. Nếu
chúng vượt qua, tôi gần như chắc chắn rằng thay đổi tôi đã thực hiện không phá vỡ bất cứ điều gì.
"Gần như chắc chắn" đến mức nào? Chắc chắn đủ để xuất xưởng!
Quy trình QA cho FitNesse là lệnh: ant release. Lệnh đó
xây dựng FitNesse từ đầu và sau đó chạy tất cả các đơn vị và kiểm tra chấp nhận.
Nếu những bài kiểm tra đó đều vượt qua, tôi sẽ gửi nó.

#### Defect Injection Rate
Bây giờ, FitNesse không phải là một ứng dụng quan trọng. Nếu có lỗi, không ai
chết, và không ai mất hàng triệu đô la. Vì vậy, tôi có thể đủ khả năng giao hàng dựa trên
không có gì ngoài việc vượt qua các bài kiểm tra. Mặt khác, FitNesse có hàng nghìn người dùng,
và bất chấp việc bổ sung 20.000 dòng mã mới vào năm ngoái, danh sách lỗi của tôi chỉ
có 17 lỗi trên đó (nhiều trong số đó là mỹ phẩm trong tự nhiên). Vì vậy tôi biết khuyết điểm của mình
tỷ lệ tiêm rất thấp.
Đây không phải là một hiệu ứng cô lập. Đã có một số báo cáo 4 và nghiên cứu 5 cho rằng
mô tả sự giảm thiểu khuyết tật đáng kể. Từ IBM, đến Microsoft, từ Sabre đến
Symantec, hết công ty này đến công ty khác và đội ngũ này đến đội khác đã trải qua những khiếm khuyết
giảm 2X, 5X và thậm chí 10X. Đây là những con số mà không chuyên
nên bỏ qua.

#### Courage
Tại sao bạn không sửa mã lỗi khi bạn nhìn thấy nó? Phản ứng đầu tiên của bạn khi nhìn thấy
hàm lộn xộn là "Đây là một mớ hỗn độn, nó cần được làm sạch." Phản ứng thứ hai của bạn
là "Tôi không chạm vào nó!" Tại sao? Bởi vì bạn biết rằng nếu bạn chạm vào nó, bạn có nguy cơ
phá vỡ nó; và nếu bạn phá vỡ nó, nó sẽ trở thành của bạn.
Nhưng điều gì sẽ xảy ra nếu bạn có thể chắc chắn rằng việc dọn dẹp của bạn không bị hỏng hóc gì? Gì
nếu bạn có loại chắc chắn mà tôi vừa đề cập? Điều gì sẽ xảy ra nếu bạn có thể nhấp vào
và biết trong vòng 90 giây rằng các thay đổi của bạn không bị ảnh hưởng gì, và
đã chỉ làm tốt?
Đây là một trong những lợi ích mạnh mẽ nhất của TDD. Khi bạn có một bộ
các bài kiểm tra mà bạn tin tưởng, sau đó bạn không còn lo sợ về việc thay đổi. Khi bạn thấy xấu
mã, bạn chỉ cần làm sạch nó ngay tại chỗ. Mã trở thành đất sét mà bạn có thể an toàn
điêu khắc thành các cấu trúc đơn giản và đẹp mắt.
Khi các lập trình viên mất đi nỗi sợ hãi về việc dọn dẹp, họ làm sạch! Và mã sạch là
dễ hiểu hơn, dễ thay đổi và dễ mở rộng hơn. Khiếm khuyết trở thành
4. http://www.objectmentor.com/omSolutions/agile_customers.html
5. [Maximilien], [George2003], [Janzen2005], [Nagappan2008]

thậm chí ít khả năng hơn vì mã trở nên đơn giản hơn. Và cơ sở mã ổn định
cải thiện thay vì mục nát bình thường mà ngành công nghiệp của chúng ta đã quen thuộc.
Lập trình viên chuyên nghiệp nào sẽ cho phép sự thối rữa tiếp tục?

#### Documentation
Bạn đã bao giờ sử dụng khuôn khổ của bên thứ ba chưa? Thường thì bên thứ ba sẽ gửi
bạn một hướng dẫn được định dạng độc đáo được viết bởi các nhà văn công nghệ. Sách hướng dẫn điển hình
sử dụng 27 bức ảnh bóng tám x mười màu với các vòng tròn và mũi tên và
ở mặt sau của mỗi phần giải thích cách định cấu hình, triển khai,
thao túng và sử dụng khuôn khổ đó. Ở phía sau, trong phần phụ lục,
thường có một phần nhỏ xấu xí chứa tất cả các ví dụ mã.
Nơi đầu tiên bạn đến trong sách hướng dẫn đó là đâu? Nếu bạn là một lập trình viên, bạn đi
đối với các ví dụ mã. Bạn đi đến mã vì bạn biết mã sẽ cho biết
bạn là sự thật. 27 bức ảnh bóng màu 8 x 10 với các vòng tròn và
mũi tên và một đoạn ở mặt sau có thể khá đẹp, nhưng nếu bạn muốn biết
cách sử dụng mã bạn cần đọc mã.
Mỗi bài kiểm tra đơn vị bạn viết khi bạn tuân theo ba luật là một ví dụ,
được viết bằng mã, mô tả cách sử dụng hệ thống. Nếu bạn làm theo
ba luật, sau đó sẽ có một bài kiểm tra đơn vị mô tả cách tạo mọi đối tượng
trong hệ thống, mọi cách mà các đối tượng đó có thể được tạo. Sẽ có một đơn vị
kiểm tra mô tả cách gọi mọi chức năng trong hệ thống theo mọi cách
các hàm có thể được gọi một cách có ý nghĩa. Đối với bất cứ điều gì bạn cần biết cách
làm, sẽ có một bài kiểm tra đơn vị mô tả nó chi tiết.
Các bài kiểm tra đơn vị là tài liệu. Họ mô tả thiết kế cấp thấp nhất của
hệ thống. Chúng rõ ràng, chính xác, được viết bằng ngôn ngữ
khán giả hiểu và trang trọng đến mức họ thực thi. Họ la tuyệt nhât
loại tài liệu cấp thấp có thể tồn tại. Những gì chuyên nghiệp sẽ không
cung cấp tài liệu đó?

#### Design
Khi bạn tuân theo ba luật và viết các bài kiểm tra của mình trước, bạn phải đối mặt với
tình trạng khó xử. Thường thì bạn biết chính xác mã bạn muốn viết, nhưng ba

luật yêu cầu bạn viết một bài kiểm tra đơn vị không thành công vì mã đó không tồn tại! Điều này
có nghĩa là bạn phải kiểm tra mã mà bạn sắp viết.
Vấn đề với mã thử nghiệm là bạn phải cô lập mã đó. Nó thường
khó kiểm tra một hàm nếu hàm đó gọi các hàm khác. Để viết điều đó
kiểm tra, bạn phải tìm ra cách nào đó để tách chức năng khỏi tất cả
khác. Nói cách khác, nhu cầu kiểm tra trước tiên buộc bạn phải nghĩ đến
thiết kế.
Nếu bạn không viết các bài kiểm tra của mình trước, không có lực lượng nào ngăn cản bạn ghép nối
các chức năng kết hợp với nhau thành một khối không thể kiểm tra được. Nếu bạn viết các bài kiểm tra của mình sau đó, bạn
có thể kiểm tra đầu vào và đầu ra của tổng khối lượng, nhưng nó sẽ
có lẽ khá khó để kiểm tra các chức năng riêng lẻ.
Do đó, tuân theo ba luật và viết các bài kiểm tra của bạn trước, sẽ tạo ra một lực
điều đó thúc đẩy bạn đến một thiết kế tách rời tốt hơn. Những gì chuyên nghiệp sẽ không
sử dụng các công cụ giúp họ hướng tới những thiết kế tốt hơn?
"Nhưng tôi có thể viết các bài kiểm tra của mình sau," bạn nói. Không, bạn không thể. Không hẳn vậy. Ồ, bạn có thể
viết một số bài kiểm tra sau. Bạn thậm chí có thể tiếp cận mức độ bao phủ cao sau này nếu bạn cẩn thận
để đo lường nó. Nhưng các bài kiểm tra bạn viết sau khi thực tế là biện hộ. Các bài kiểm tra bạn viết
đầu tiên là sự xúc phạm. Các bài kiểm tra sau thực tế được viết bởi một người đã được giao
trong mã và đã biết cách giải quyết vấn đề. Không có cách nào
những bài kiểm tra đó có thể ở bất kỳ đâu gần giống như những bài kiểm tra được viết trước.

### T H E P R O F E S I O N A L O P T I O N
Kết quả của tất cả những điều này là TDD là lựa chọn chuyên nghiệp. Nó là một kỷ luật
giúp tăng cường sự chắc chắn, can đảm, giảm thiểu sai sót, tài liệu và thiết kế.
Với tất cả những gì đang xảy ra, việc không sử dụng nó có thể được coi là không chuyên nghiệp.

## W H AT TD D I S N O T
Đối với tất cả những điểm tốt của nó, TDD không phải là một tôn giáo hay một công thức ma thuật. Theo dõi
ba luật không đảm bảo bất kỳ lợi ích nào trong số này. Bạn vẫn có thể viết mã xấu
ngay cả khi bạn viết bài kiểm tra của mình trước. Thật vậy, bạn có thể viết các bài kiểm tra tồi.

Đồng thời, có những lúc việc tuân theo ba luật chỉ đơn giản là
không thực tế hoặc không phù hợp. Những tình huống này rất hiếm, nhưng chúng tồn tại. Không
nhà phát triển chuyên nghiệp nên tuân theo một kỷ luật khi kỷ luật đó
nhiều nguy hại hơn là tốt.