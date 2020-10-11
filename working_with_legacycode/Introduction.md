# Introduction 
Loạt bài này hướng đến các nhà phát triển phần mềm, trưởng nhóm,
các nhà phân tích kinh doanh và các nhà quản lý muốn tăng
kỹ năng và sự thành thạo đến cấp độ của một Thợ thủ công bậc thầy.

Bộ sách bao gồm các cuốn sách hướng dẫn các chuyên gia phần mềm
về các nguyên tắc, mẫu và thực hành lập trình,
quản lý dự án phần mềm, thu thập yêu cầu,
thiết kế, phân tích, thử nghiệm và những thứ khác.

#### Cuốn sách có 3 phần, mỗi phần có nhiều chương, mỗi chương có nhiều section 
## Foreword

"... sau đó nó bắt đầu ..."
Trong phần giới thiệu cuốn sách này, Michael Feathers sử dụng cụm từ đó để
mô tả sự khởi đầu của niềm đam mê với phần mềm của anh ấy.
"... sau đó nó bắt đầu ..."
Bạn có biết cảm giác đó không? Bạn có thể chỉ vào một khoảnh khắc trong cuộc sống của bạn và
nói: "... sau đó nó bắt đầu ..."? Có một sự kiện duy nhất làm thay đổi tiến trình của
cuộc sống của bạn và cuối cùng đã dẫn bạn đến với cuốn sách này và bắt đầu đọc
từ?
Tôi đang học lớp sáu thì nó xảy ra với tôi. Tôi quan tâm đến khoa học và
không gian và tất cả những thứ kỹ thuật. Mẹ tôi tìm thấy một chiếc máy tính bằng nhựa trong một danh mục
và đặt hàng cho tôi. Nó được gọi là Digi-Comp I. Bốn mươi năm sau đó
máy tính nhựa giữ một vị trí danh dự trên giá sách của tôi. Nó là chất xúc tác
điều đó đã khơi dậy niềm đam mê bền bỉ của tôi đối với phần mềm. Nó đã cho tôi lần đầu tiên viết về
thật vui biết bao khi viết ra những chương trình giải quyết vấn đề cho mọi người. Nó chỉ là
ba chiếc dép xỏ ngón S-R bằng nhựa và sáu chiếc cổng nhựa và cổng, nhưng nó là đủ - nó
được phục vụ. Sau đó ... đối với tôi ... nó bắt đầu ...
Nhưng niềm vui mà tôi cảm thấy nhanh chóng bị kiềm hãm khi nhận ra rằng hệ thống phần mềm-
hầu như luôn luôn suy thoái thành một mớ hỗn độn. Bắt đầu như một kết tinh sạch
thiết kế trong tâm trí của các lập trình viên bị thối rữa theo thời gian, giống như một thứ tồi tệ
thịt. Hệ thống nhỏ xinh mà chúng tôi đã xây dựng năm ngoái biến thành một mớ hỗn độn khủng khiếp
các hàm và biến số rối trong năm tới.
Lý do tại sao điều này xảy ra? Tại sao hệ thống thối rữa? Tại sao họ không thể giữ sạch?
Đôi khi chúng ta đổ lỗi cho khách hàng của mình. Đôi khi chúng tôi buộc tội họ thay đổi
những yêu cầu. Chúng tôi tự an ủi mình với niềm tin rằng nếu khách hàng đã
chỉ cần hài lòng với những gì họ nói rằng họ cần, thiết kế sẽ
khỏe. Đó là lỗi của khách hàng khi thay đổi các yêu cầu đối với chúng tôi.
Chà, đây là một tin nhanh: Các yêu cầu thay đổi. Kiểu dáng không thể chịu đựng được
yêu cầu thay đổi là thiết kế kém để bắt đầu. Đó là mục tiêu của mọi
nhà phát triển phần mềm có năng lực để tạo ra các thiết kế chịu được sự thay đổi.
Đây dường như là một vấn đề khó giải quyết. Thực tế là rất khó
gần như mọi hệ thống từng được sản xuất đều bị thối rữa, suy nhược. Thối là
phổ biến đến nỗi chúng tôi đã nghĩ ra một cái tên đặc biệt cho các chương trình thối nát. Chúng tôi
gọi chúng: Mã kế thừa.

Mã kế thừa. Cụm từ gây phẫn nộ trong lòng các lập trình viên. Nó có ...
jures hình ảnh của việc slogging qua một đầm lầy âm u với những cây cối rậm rạp bị rối
rỉa bên dưới và đốt ruồi bên trên. Nó gợi lên mùi âm u, chất nhờn,
nancy và nội tạng. Mặc dù niềm vui lập trình đầu tiên của chúng tôi có thể rất mãnh liệt,
sự khốn khổ của việc xử lý mã kế thừa thường đủ để dập tắt điều đó
ngọn lửa.
Nhiều người trong chúng ta đã cố gắng khám phá các cách để ngăn mã trở thành chân-
acy. Chúng tôi đã viết sách về các nguyên tắc, mẫu và thực hành có thể giúp
lập trình viên giữ cho hệ thống của họ sạch sẽ. Nhưng Michael Feathers có một cái nhìn sâu sắc rằng
nhiều người trong số chúng tôi đã bỏ lỡ. Phòng ngừa là không hoàn hảo. Ngay cả những người kỷ luật nhất
nhóm phát triển, biết các nguyên tắc tốt nhất, sử dụng các mô hình tốt nhất và fol-
hạ thấp các phương pháp hay nhất sẽ tạo ra tình trạng lộn xộn theo thời gian. Thối vẫn chính xác-
giao phối. Cố gắng ngăn chặn sự thối rữa là chưa đủ — bạn phải có khả năng
đảo ngược nó lại.
Đó là những gì cuốn sách này nói về. Đó là về việc đảo ngược sự thối rữa. Đó là về việc lấy
một hệ thống rối rắm, mờ đục, phức tạp và từ từ, dần dần, từng mảnh, từng bước
từng bước, biến nó thành một hệ thống đơn giản, có cấu trúc độc đáo, được thiết kế tốt. Nó là
về đảo ngược entropy.
Trước khi bạn quá phấn khích, tôi cảnh báo bạn; đảo ngược thối không dễ dàng, và nó không
nhanh chóng. Các kỹ thuật, mẫu và công cụ mà Michael trình bày trong cuốn sách này
hiệu quả, nhưng chúng cần công sức, thời gian, sức bền và sự cẩn thận. Cuốn sách này không phải là một
viên đạn ma thuật. Nó sẽ không cho bạn biết làm thế nào để loại bỏ tất cả thối rữa tích lũy trong
hệ thống qua đêm. Đúng hơn, cuốn sách này mô tả một tập hợp các nguyên tắc, khái niệm và
thái độ mà bạn sẽ mang theo trong suốt phần còn lại của sự nghiệp và điều đó sẽ
giúp bạn biến những hệ thống đang dần suy thoái thành những hệ thống dần dần
cải tiến.

Robert C. Martin
9 tháng 6, 2004


## Preface

Bạn có nhớ chương trình đầu tiên bạn đã viết? Tôi nhớ của tôi. Nó là một chút
chương trình đồ họa tôi đã viết trên PC đời đầu. Tôi bắt đầu lập trình muộn hơn
hầu hết các bạn của tôi. Chắc chắn, tôi đã nhìn thấy máy tính khi tôi còn nhỏ. tôi nhớ
thực sự bị ấn tượng bởi một chiếc máy tính mini mà tôi từng thấy trong văn phòng, nhưng trong nhiều năm
Tôi chưa bao giờ có cơ hội ngồi vào máy tính. Sau này, khi tôi còn là một thiếu niên,
một số người bạn của tôi đã mua một vài chiếc TRS-80 đầu tiên. Tôi đã quan tâm, nhưng
Tôi thực sự cũng hơi e ngại. Tôi biết điều đó nếu tôi bắt đầu chơi với com-
tôi sẽ bị cuốn vào nó. Nó chỉ trông quá tuyệt. Tôi không biết tại sao tôi biết
bản thân tôi rất tốt, nhưng tôi đã kìm chế. Sau đó, ở trường đại học, một người bạn cùng phòng của tôi đã
và tôi đã mua một trình biên dịch C để có thể tự học lập trình.
Sau đó, nó bắt đầu. Tôi thức đêm này qua đêm khác để thử mọi thứ, nghiền ngẫm
mã nguồn của trình soạn thảo emacs đi kèm với trình biên dịch. Thật là nghiện-
tive, nó là một thử thách, và tôi yêu nó.
Tôi hy vọng bạn đã có những trải nghiệm như thế này — chỉ là niềm vui thô sơ khi làm ra mọi thứ
làm việc trên máy tính. Gần như mọi lập trình viên tôi yêu cầu đều có. Niềm vui đó là một phần của
điều gì đã đưa chúng tôi vào công việc này, nhưng nó đang ở đâu hàng ngày?
Một vài năm trước, tôi đã gọi cho bạn tôi Erik Meade sau khi tôi hoàn thành công việc
một đêm. Tôi biết rằng Erik vừa mới bắt đầu hợp đồng tư vấn với một nhóm mới, vì vậy
Tôi hỏi anh ta, "Họ thế nào?" Anh ấy nói, "Họ đang viết mã kế thừa,
Đàn ông." Đó là một trong số ít lần trong đời tôi bị đấm bởi
tuyên bố của đồng nghiệp. Tôi cảm thấy nó ngay trong ruột của tôi. Erik đã đưa ra những lời nói trước
cảm giác cise mà tôi thường có khi tôi đến thăm các đội lần đầu tiên. Họ đang cố gắng
rất vất vả, nhưng vào cuối ngày, vì áp lực lịch trình, trọng lượng của
lịch sử hoặc thiếu bất kỳ mã nào tốt hơn để so sánh nỗ lực của họ với, nhiều người
đang viết mã kế thừa.
Mã kế thừa là gì? Tôi đã sử dụng thuật ngữ mà không định nghĩa nó. Hãy nhìn vào
định nghĩa chặt chẽ: Mã kế thừa là mã mà chúng tôi đã nhận được từ người khác.
Có thể công ty của chúng tôi đã mua lại mã từ một công ty khác; có thể mọi người trên
nhóm ban đầu đã chuyển sang các dự án khác. Mã kế thừa là của người khác
mã. Nhưng trong ngôn ngữ lập trình viên, thuật ngữ này có nghĩa nhiều hơn thế. Các
thuật ngữ mã kế thừa đã mang nhiều sắc thái ý nghĩa hơn và có trọng lượng hơn
thời gian.

Bạn nghĩ về điều gì khi nghe đến thuật ngữ mã kế thừa? Nếu bạn đang ở
tất cả giống như tôi, bạn nghĩ về cấu trúc rối rắm, khó hiểu, mã mà bạn phải
thay đổi nhưng không thực sự hiểu. Bạn nghĩ đến những đêm mất ngủ cố gắng thêm
trong các tính năng nên dễ dàng thêm vào và bạn nghĩ đến việc giảm tinh thần,
cảm thấy rằng tất cả mọi người trong nhóm quá chán ngán với cơ sở mã đến nỗi nó dường như vượt quá
quan tâm, loại mã mà bạn chỉ muốn sẽ chết. Một phần của bạn cảm thấy tồi tệ vì
thậm chí nghĩ về việc làm cho nó tốt hơn. Nó có vẻ không xứng đáng với những nỗ lực của bạn. Cái đó
định nghĩa về mã kế thừa không liên quan gì đến việc ai đã viết nó. Mã có thể
suy giảm theo nhiều cách và nhiều trong số chúng không liên quan gì đến việc
mã đến từ một nhóm khác.
Trong ngành, mã kế thừa thường được sử dụng như một thuật ngữ tiếng lóng chỉ những mã khó thay đổi
mã mà chúng tôi không hiểu. Nhưng qua nhiều năm làm việc với nhóm, giúp
chúng vượt qua các vấn đề nghiêm trọng về mã, tôi đã đi đến một định nghĩa khác.
Đối với tôi, mã kế thừa chỉ đơn giản là mã không có kiểm tra. Tôi đã nhận được một số đau buồn cho
định nghĩa này. Các bài kiểm tra có liên quan gì đến việc mã có xấu hay không? Đối với tôi,
câu trả lời là đơn giản và đó là một điểm mà tôi đã giải thích trong suốt
sách:
Mã không có kiểm tra là mã xấu. Nó được viết tốt như thế nào không quan trọng; nó không thành vấn đề-
ter đẹp hoặc hướng đối tượng hoặc được đóng gói tốt như thế nào. Với các bài kiểm tra, chúng tôi có thể thay đổi
hành vi của mã của chúng tôi một cách nhanh chóng và có thể xác minh được. Nếu không có họ, chúng tôi thực sự không biết
nếu mã của chúng tôi ngày càng tốt hơn hoặc tệ hơn.
Bạn có thể nghĩ rằng điều này là nghiêm trọng. Còn mã sạch thì sao? Nếu cơ sở mã là
rất rõ ràng và có cấu trúc tốt, vậy vẫn chưa đủ sao? Chà, đừng nhầm lẫn. tôi yêu
mã sạch. Tôi yêu nó hơn hầu hết những người tôi biết, nhưng trong khi mã sạch thì
tốt, vẫn chưa đủ. Các đội có cơ hội nghiêm túc khi họ cố gắng tạo ra
thay đổi mà không cần thử nghiệm. Nó giống như tập thể dục trên không mà không có lưới. Nó
đòi hỏi kỹ năng đáng kinh ngạc và sự hiểu biết rõ ràng về những gì có thể xảy ra ở mọi
bươc. Biết chính xác điều gì sẽ xảy ra nếu bạn thay đổi một vài biến là
thường muốn biết liệu một vận động viên thể dục khác sẽ bắt lấy cánh tay của bạn sau khi
bạn thoát ra khỏi một cú lộn nhào. Nếu bạn thuộc một nhóm có mã rõ ràng, bạn
ở vị trí tốt hơn hầu hết các lập trình viên. Trong công việc của mình, tôi nhận thấy rằng
các nhóm có mức độ rõ ràng như vậy trong tất cả các mã của họ là rất hiếm. Họ có vẻ như một
bất thường thống kê. Và bạn biết những gì? Nếu họ không có các bài kiểm tra hỗ trợ,
các thay đổi mã của họ dường như vẫn chậm hơn so với các thay đổi của các nhóm.
Có, các nhóm làm tốt hơn và bắt đầu viết mã rõ ràng hơn, nhưng phải mất nhiều thời gian
thời gian để mã cũ rõ ràng hơn. Trong nhiều trường hợp, nó sẽ không bao giờ xảy ra
chắc chắn. Do đó, tôi không gặp vấn đề gì khi xác định mã kế thừa là mã không có
các bài kiểm tra. Đó là một định nghĩa hoạt động tốt và nó chỉ ra một giải pháp.
Tôi đã nói về các bài kiểm tra khá nhiều cho đến nay, nhưng cuốn sách này không nói về bài kiểm tra-
ing. Cuốn sách này nói về việc có thể tự tin thực hiện các thay đổi trong bất kỳ mã nào
Từ Thư viện của Brian WattersonP REFACE
xvii
căn cứ. Trong các chương sau, tôi mô tả các kỹ thuật mà bạn có thể sử dụng để-
đứng mã, kiểm tra nó, cấu trúc lại nó và thêm các tính năng.
Một điều mà bạn sẽ nhận thấy khi đọc cuốn sách này là nó không phải là một cuốn sách
về mã đẹp. Các ví dụ mà tôi sử dụng trong sách là bịa đặt bởi vì tôi
làm việc theo thỏa thuận không tiết lộ với khách hàng. Nhưng trong nhiều kỳ thi-
xin vui lòng, tôi đã cố gắng duy trì tinh thần của mã mà tôi đã thấy trong lĩnh vực này. Tôi sẽ không
nói rằng các ví dụ luôn mang tính đại diện. Chắc chắn có những ốc đảo của
mã tuyệt vời ngoài đó, nhưng, thành thật mà nói, cũng có những đoạn mã khác xa
tệ hơn bất cứ điều gì tôi có thể lấy làm ví dụ trong cuốn sách này. Ngoài khách hàng
tính bảo mật, tôi chỉ đơn giản là không thể viết mã như vậy vào cuốn sách này mà không gây nhàm chán
bạn rơi nước mắt và chôn vùi những điểm quan trọng trong một mớ chi tiết. Kết quả là,
nhiều ví dụ tương đối ngắn gọn. Nếu bạn nhìn vào một trong số chúng và nghĩ
“Không, anh ấy không hiểu — các phương pháp của tôi lớn hơn nhiều và nhiều
tệ hơn, ”hãy xem lời khuyên mà tôi đang đưa ra theo mệnh giá và xem nó có
áp dụng, ngay cả khi ví dụ có vẻ đơn giản hơn.
Các kỹ thuật ở đây đã được thử nghiệm trên các đoạn mã lớn về cơ bản. Nó
chỉ là một hạn chế của định dạng sách làm cho các ví dụ nhỏ hơn. Cụ thể-
lar, khi bạn nhìn thấy các dấu chấm lửng (...) trong một đoạn mã như thế này, bạn có thể đọc chúng là
"Chèn 500 dòng mã xấu vào đây":
m_pDispatcher-> register (người nghe);
...
m_nMargins ++;
Nếu cuốn sách này không nói về mã đẹp, thì nó thậm chí còn kém về thiết kế đẹp. Tốt
thiết kế phải là mục tiêu cho tất cả chúng ta, nhưng trong mã kế thừa, nó là thứ mà chúng ta
đến từng bước rời rạc. Trong một số chương, tôi mô tả các cách thêm
mã mới vào các cơ sở mã hiện có và chỉ ra cách thêm mã đó với các thiết kế đẹp-
ciples trong tâm trí. Bạn có thể bắt đầu phát triển các khu vực mã chất lượng cao rất tốt trong
cơ sở mã kế thừa, nhưng đừng ngạc nhiên nếu một số bước bạn thực hiện
thay đổi liên quan đến việc làm cho một số mã xấu hơn một chút. Công việc này giống như phẫu thuật. Chúng tôi
phải rạch, và chúng tôi phải mổ ruột và đình chỉ
một số nhận định thẩm mỹ. Có thể cá các cơ quan và nội tạng chính của bệnh nhân này-
ter hơn họ? Đúng. Vì vậy, chúng ta chỉ cần quên đi vấn đề trước mắt của anh ấy, may
anh ta lại dậy, và bảo anh ta ăn uống đúng cách và tập luyện để chạy marathon? Chúng tôi có thể, nhưng
những gì chúng ta thực sự cần làm là coi bệnh nhân là chính mình, sửa chữa những gì sai và
chuyển anh ta sang trạng thái khỏe mạnh hơn. Anh ấy có thể không bao giờ trở thành vận động viên Olympic, nhưng
chúng ta không thể để “tốt nhất” là kẻ thù của “tốt hơn”. Cơ sở mã có thể trở nên lành mạnh hơn
và dễ dàng hơn để làm việc. Khi bệnh nhân cảm thấy tốt hơn một chút, thường là lúc
khi bạn có thể giúp anh ấy cam kết với một lối sống lành mạnh hơn. Đó là
những gì chúng tôi đang tìm kiếm với mã kế thừa.
mà chúng ta thường dùng để giảm bớt; chúng tôi mong đợi điều đó và tích cực cố gắng tạo mã
thay đổi dễ dàng hơn. Khi chúng ta có thể duy trì ý thức đó trong một nhóm, thiết kế sẽ trở nên tốt hơn.
Các kỹ thuật tôi mô tả là những kỹ thuật tôi đã khám phá và học hỏi
đồng nghiệp và khách hàng trong suốt nhiều năm làm việc với khách hàng để cố gắng
thiết lập quyền kiểm soát đối với các cơ sở mã ngỗ ngược. Tôi đã nhấn mạnh mã kế thừa này
vô tình. Khi tôi lần đầu tiên bắt đầu làm việc với Object Mentor, phần lớn
làm việc liên quan đến việc giúp các nhóm có vấn đề nghiêm trọng phát triển kỹ năng của họ và
tương tác đến mức chúng có thể thường xuyên cung cấp mã chất lượng. Chúng tôi thường
đã sử dụng các phương pháp Lập trình khắc nghiệt để giúp các nhóm kiểm soát công việc của họ,
cộng tác chuyên sâu và phân phối. Tôi thường cảm thấy rằng Lập trình cực đoan là
không phải là một cách để phát triển phần mềm hơn là một cách để tạo ra một nhóm làm việc tốt
điều đó chỉ xảy ra để cung cấp phần mềm tuyệt vời hai tuần một lần.
Ngay từ đầu, đã có một vấn đề. Nhiều XP đầu tiên
các dự án là dự án “greenfield”. Những khách hàng mà tôi đang gặp có
các cơ sở mã lớn, và họ đang gặp rắc rối. Họ cần một số cách để có được ...
đẩy công việc của họ và bắt đầu giao hàng. Theo thời gian, tôi thấy rằng tôi đang làm
những điều tương tự lặp đi lặp lại với khách hàng. Ý thức này lên đến đỉnh điểm ở một số
công việc tôi đã làm với một nhóm trong ngành tài chính. Trước khi tôi đến,
họ nhận ra rằng thử nghiệm đơn vị là một điều tuyệt vời, nhưng thử nghiệm mà họ
thực thi là các bài kiểm tra kịch bản đầy đủ thực hiện nhiều chuyến đi đến cơ sở dữ liệu và
thực hiện các đoạn mã lớn. Các bài kiểm tra khó viết, và nhóm
không chạy chúng thường xuyên vì chúng mất quá nhiều thời gian để chạy. Khi tôi ngồi xuống với
chúng để phá vỡ sự phụ thuộc và nhận được các đoạn mã nhỏ hơn đang được thử nghiệm, tôi đã có
cảm giác khủng khiếp của déjà vu. Có vẻ như tôi đang làm loại công việc này với mọi
nhóm mà tôi đã gặp, và đó là điều mà không ai thực sự muốn nghĩ
trong khoảng. Nó chỉ là công việc grunge mà bạn làm khi bạn muốn bắt đầu làm việc
với mã của bạn một cách có kiểm soát, nếu bạn biết cách thực hiện. Tôi đã quyết định sau đó
rằng nó thực sự đáng để suy ngẫm về cách chúng tôi đã giải quyết những vấn đề này và
viết chúng ra để các nhóm có thể chuẩn bị và bắt đầu tạo mã của họ
căn cứ dễ sống hơn.
Lưu ý về các ví dụ: Tôi đã sử dụng các ví dụ trong một số chương trình khác nhau-
ngôn ngữ giao phối. Phần lớn các ví dụ được viết bằng Java, C ++ và C. I
đã chọn Java vì nó là một ngôn ngữ rất phổ biến và tôi đã bao gồm C ++ vì nó
đưa ra một số thách thức đặc biệt trong môi trường kế thừa. Tôi chọn C vì nó
nêu bật nhiều vấn đề nảy sinh trong mã kế thừa thủ tục. Ở giữa
chúng, những ngôn ngữ này bao hàm phần lớn các mối quan tâm nảy sinh trong-
mã acy. Tuy nhiên, nếu các ngôn ngữ bạn sử dụng không được đề cập trong các ví dụ,
hãy nhìn vào chúng. Nhiều kỹ thuật mà tôi trình bày có thể được sử dụng trong
các ngôn ngữ khác, chẳng hạn như Delphi, Visual Basic, COBOL và FORTRAN.

Tôi hy vọng rằng bạn thấy các kỹ thuật trong cuốn sách này hữu ích và chúng cho phép
bạn trở lại những gì thú vị về lập trình. Lập trình có thể rất
công việc bổ ích và thú vị. Nếu bạn không cảm thấy điều đó trong công việc hàng ngày của mình, tôi
hy vọng rằng những kỹ thuật tôi cung cấp cho bạn trong cuốn sách này sẽ giúp bạn tìm ra nó và phát triển nó đội của bạn.

## Acknowledgments
Trước hết, tôi nợ vợ tôi, Ann và các con tôi, Deborah.
và Ryan. Tình yêu và sự ủng hộ của họ đã khiến cuốn sách này và tất cả những gì học được
trước nó có thể. Tôi cũng muốn cảm ơn “Uncle Bob” Martin, chủ tịch và
người sáng lập Object Mentor. Cách tiếp cận thực dụng nghiêm ngặt của ông để phát triển
và thiết kế, tách biệt điều quan trọng khỏi điều không quan trọng, đã mang lại cho tôi thứ gì đó
để nắm bắt khoảng 10 năm trước, trở lại khi có vẻ như tôi sắp
chết chìm trong làn sóng lời khuyên phi thực tế. Và cảm ơn, Bob, đã cho tôi
cơ hội để xem thêm mã và làm việc với nhiều người hơn trong năm qua
nhiều năm hơn tôi từng tưởng tượng có thể.
Tôi cũng phải cảm ơn Kent Beck, Martin Fowler, Ron Jeffries và Ward Cun-
ningham đã thỉnh thoảng đưa ra lời khuyên cho tôi và dạy tôi rất nhiều điều về
làm việc nhóm, thiết kế và lập trình. Đặc biệt cảm ơn tất cả những người
đã xem xét các bản nháp. Những người đánh giá chính thức là Sven Gorts, Robert C. Martin,
Erik Meade, và Bill Wake; những người đánh giá không chính thức là Tiến sĩ Robert Koss,
James Grenning, Lowell Lindstrom, Micah Martin, Russ Rufer và Silicon
Valley Patterns Group và James Newkirk.
Cũng xin cảm ơn những người đánh giá những bản nháp rất sớm mà tôi đã đăng trên Internet.
Phản hồi của họ ảnh hưởng đáng kể đến hướng đi của cuốn sách sau khi tôi sửa lại-
nized định dạng của nó. Tôi xin lỗi trước bất kỳ ai trong số các bạn mà tôi có thể đã bỏ qua. Các
những người đánh giá ban đầu là: Darren Hobbs, Martin Lippert, Keith Nicholas, Phlip
Plumlee, C. Keith Ray, Robert Blum, Bill Burris, William Caputo, Brian Mar-
ick, Steve Freeman, David Putman, Emily Bache, Dave Astels, Russel Hill,
Christian Sepulveda và Brian Christopher Robinson.
Cũng xin cảm ơn Joshua Kerievsky, người đã sớm đánh giá quan trọng và Jeff Langr
người đã giúp đưa ra lời khuyên và đánh giá tại chỗ trong suốt quá trình.
Những người đánh giá đã giúp tôi đánh bóng bản nháp đáng kể, nhưng nếu có sai sót
còn lại, chúng chỉ là của tôi.
Cảm ơn Martin Fowler, Ralph Johnson, Bill Opdyke, Don Roberts, và
John Brant cho công việc của họ trong lĩnh vực tái cấu trúc. Nó đã được truyền cảm hứng.

Tôi cũng nợ Jay Packlick, Jacques Morel và Kelly Mower of
Sabre Holdings và Graham Wright của Workshare Technology đã hỗ trợ họ
và phản hồi.
Đặc biệt cảm ơn Paul Petralia, Michelle Vincenti, Lori Lyons, Krista
Hansing, và phần còn lại của nhóm tại Prentice-Hall. Cảm ơn Paul vì tất cả
sự giúp đỡ và động viên mà tác giả lần đầu tiên này cần.
Cũng xin gửi lời cảm ơn đặc biệt đến Gary và Joan Feathers, April Roberts, Tiến sĩ Raimund
Ege, David Lopez de Quintana, Carlos Perez, Carlos M. Rodriguez, và những người quá cố
Tiến sĩ John C. An ủi sự giúp đỡ và động viên trong những năm qua. Tôi cũng phải
cảm ơn Brian Button về ví dụ trong Chương 21, Tôi cũng đang thay đổi
Mã khắp nơi. Anh ấy đã viết mã đó trong khoảng một giờ khi chúng tôi
cùng nhau phát triển một khóa học tái cấu trúc và nó trở thành phần yêu thích của tôi
mã giảng dạy.
Ngoài ra, đặc biệt cảm ơn Janik Top, người có nhạc cụ De Futura đã phục vụ như
nhạc nền cho vài tuần làm việc cuối cùng của tôi trên cuốn sách này.
Cuối cùng, tôi muốn cảm ơn tất cả những người mà tôi đã làm việc cùng trong vài năm qua
những năm mà những hiểu biết sâu sắc và thách thức đã củng cố tài liệu trong cuốn sách này.

**Michael Feathers**
*mfeathers@objectmentor.com*
*www.objectmentor.com*
*www.michaelfeathers.com*

## Introduction
### How to Use This Book
Tôi đã thử một số định dạng khác nhau trước khi chọn định dạng hiện tại cho cuốn sách này.
Nhiều kỹ thuật và thực hành khác nhau hữu ích khi làm việc
với mã kế thừa rất khó để giải thích một cách cô lập. Những thay đổi đơn giản nhất thường đi
dễ dàng hơn nếu bạn có thể tìm thấy các đường nối, tạo các đối tượng giả mạo và phá vỡ các phần phụ thuộc bằng cách sử dụng
một số kỹ thuật phá vỡ sự phụ thuộc. Tôi quyết định rằng cách dễ nhất để
làm cho cuốn sách dễ tiếp cận và tiện dụng sẽ là sắp xếp phần lớn của nó
(Phần II, Thay đổi phần mềm) ở định dạng FAQ (câu hỏi thường gặp).
Vì các kỹ thuật cụ thể thường yêu cầu sử dụng các kỹ thuật khác, Câu hỏi thường gặp
các chương được liên kết với nhau rất nhiều. Trong hầu hết mọi chương, bạn sẽ tìm thấy tài liệu tham khảo,
cùng với số trang, cho các chương và phần khác mô tả cụ thể
kỹ thuật ấu trùng và tái cấu trúc. Tôi xin lỗi nếu điều này khiến bạn lật lọng
thông qua cuốn sách khi bạn cố gắng tìm câu trả lời cho câu hỏi của mình, nhưng tôi
cho rằng bạn thích làm điều đó hơn là đọc hết bìa sách, cố gắng
hiểu tất cả các kỹ thuật hoạt động như thế nào.
Trong Thay đổi phần mềm, tôi đã cố gắng giải quyết những câu hỏi rất phổ biến
xuất hiện trong công việc mã kế thừa. Mỗi chương được đặt tên theo một
vấn đề. Điều này làm cho tiêu đề chương khá dài, nhưng hy vọng, chúng sẽ
cho phép bạn nhanh chóng tìm thấy phần giúp bạn giải quyết các vấn đề cụ thể
bạn đang gặp phải.
Thay đổi Phần mềm được liên kết bởi một tập hợp các chương giới thiệu (Phần I,
Cơ học thay đổi) và một danh mục tái cấu trúc, rất hữu ích
trong công việc mã kế thừa (Phần III, Kỹ thuật phá vỡ sự phụ thuộc). Xin vui lòng đọc
các chương giới thiệu, đặc biệt là Chương 4, Mô hình đường may. Những
các chương cung cấp bối cảnh và danh pháp cho tất cả các kỹ thuật mà fol-
Thấp. Ngoài ra, nếu bạn tìm thấy một thuật ngữ không được mô tả trong ngữ cảnh, hãy tìm nó trong
Bảng chú giải thuật ngữ.
Việc tái cấu trúc trong Kỹ thuật Phá vỡ Phụ thuộc đặc biệt ở chỗ chúng
được thực hiện mà không cần thử nghiệm, nhằm phục vụ cho việc đưa các thử nghiệm vào đúng vị trí. Tôi
khuyến khích bạn đọc từng cái để bạn có thể thấy nhiều khả năng hơn như
bạn bắt đầu chế ngự mã kế thừa của mình.

