# Chapter02: Working with Feedback
Các thay đổi trong hệ thống có thể được thực hiện theo hai cách chính. Tôi thích gọi họ là Chỉnh sửa
và Cầu nguyện và Bao bọc và Sửa đổi. Thật không may, Chỉnh sửa và Cầu nguyện khá nhiều
tiêu chuẩn ngành. Khi bạn sử dụng Chỉnh sửa và Cầu nguyện, bạn lập kế hoạch cẩn thận
những thay đổi bạn sẽ thực hiện, bạn đảm bảo rằng bạn hiểu mã
bạn sẽ sửa đổi, và sau đó bạn bắt đầu thực hiện các thay đổi. Khi bạn
xong, bạn chạy hệ thống để xem thay đổi đã được kích hoạt chưa, sau đó bạn chọc
xa hơn để đảm bảo rằng bạn không làm vỡ bất cứ thứ gì. Sự chọc ngoáy
xung quanh là chủ yếu. Khi bạn thực hiện những thay đổi của mình, bạn đang hy vọng và cầu nguyện
rằng bạn sẽ làm đúng và bạn mất thêm thời gian khi hoàn thành
chắc chắn rằng bạn đã làm.
Bề ngoài, Chỉnh sửa và Cầu nguyện có vẻ như "làm việc cẩn thận", một điều rất đặc biệt-
điều cần làm. "Sự quan tâm" mà bạn đặt lên hàng đầu và
bạn cần chăm sóc thêm khi những thay đổi rất xâm lấn vì nhiều
có thể đi sai. Nhưng an toàn không chỉ là một chức năng của việc chăm sóc. Tôi không nghĩ là ai trong chúng ta
sẽ chọn một bác sĩ phẫu thuật đã phẫu thuật bằng dao cắt bơ chỉ vì anh ta
đã làm việc cẩn thận. Thay đổi phần mềm hiệu quả, giống như phẫu thuật hiệu quả, thực sự
liên quan đến các kỹ năng sâu hơn. Làm việc cẩn thận sẽ không giúp ích gì nhiều cho bạn nếu bạn không làm
sử dụng các công cụ và kỹ thuật phù hợp.
Cover and Modify là một cách thực hiện thay đổi khác. Ý tưởng đằng sau nó là
rằng có thể làm việc với mạng an toàn khi chúng tôi thay đổi phần mềm. Các
mạng lưới an toàn chúng tôi sử dụng không phải là thứ mà chúng tôi đặt bên dưới bàn để bắt chúng tôi
nếu chúng ta ngã ra khỏi ghế. Thay vào đó, nó giống như một chiếc áo choàng mà chúng tôi khoác lên
mã chúng tôi đang làm việc để đảm bảo rằng các thay đổi xấu không bị rò rỉ và
lây nhiễm phần còn lại của phần mềm của chúng tôi. Che phần mềm có nghĩa là bao phủ nó bằng các bài kiểm tra.
Khi chúng tôi có một bộ kiểm tra tốt xung quanh một đoạn mã, chúng tôi có thể thực hiện các thay đổi
và tìm ra rất nhanh xem tác động tốt hay xấu. Chúng tôi vẫn áp dụng
chăm sóc như nhau, nhưng với phản hồi nhận được, chúng tôi có thể thực hiện các thay đổi nhiều hơn
cẩn thận.
Nếu bạn không quen với việc sử dụng các bài kiểm tra này, tất cả những điều này có nghĩa là
hơi kỳ quặc. Theo truyền thống, các bài kiểm tra được viết và thực thi sau khi phát triển. Một nhóm lập trình viên viết mã và một nhóm người kiểm tra chạy các bài kiểm tra đối với
mã sau đó để xem liệu nó có đáp ứng một số thông số kỹ thuật hay không. Trong một số rất truyền thống
cửa hàng phát triển, đây chỉ là cách mà phần mềm được phát triển. Đội
có thể nhận được phản hồi, nhưng vòng lặp phản hồi lớn. Làm việc trong vài tuần hoặc
tháng, và sau đó những người trong nhóm khác sẽ cho bạn biết liệu bạn đã hiểu được chưa
đúng.
Thử nghiệm được thực hiện theo cách này thực sự là “thử nghiệm để cố gắng thể hiện tính đúng đắn”.
Mặc dù đó là một mục tiêu tốt, các bài kiểm tra cũng có thể được sử dụng theo một cách rất khác. Chúng tôi
có thể thực hiện "thử nghiệm để phát hiện thay đổi."
Theo thuật ngữ truyền thống, đây được gọi là kiểm thử hồi quy. Chúng tôi chạy thử nghiệm định kỳ
kiểm tra hành vi tốt đã biết để tìm hiểu xem liệu phần mềm của chúng tôi có còn
hoạt động theo cách mà nó đã làm trong quá khứ.
Khi bạn có các bài kiểm tra xung quanh các lĩnh vực mà bạn sẽ thực hiện
thay đổi, chúng hoạt động như một phần mềm. Bạn có thể giữ hầu hết các hành vi cố định
và biết rằng bạn chỉ đang thay đổi những gì bạn dự định.
Phần mềm Vise
vise (n.). Một thiết bị kẹp, thường bao gồm hai hàm đóng hoặc mở bằng một
vít hoặc đòn bẩy, được sử dụng trong nghề mộc hoặc gia công kim loại để giữ một chi tiết ở vị trí. Các
Từ điển Di sản Hoa Kỳ bằng tiếng Anh, Ấn bản thứ tư
Khi chúng tôi có các bài kiểm tra phát hiện sự thay đổi, nó giống như có một cái nhìn xung quanh mã của chúng tôi. Các
hành vi của mã được cố định tại chỗ. Khi chúng tôi thực hiện các thay đổi, chúng tôi có thể biết rằng
chúng tôi chỉ thay đổi một phần hành vi tại một thời điểm. Tóm lại, chúng tôi kiểm soát
công việc của chúng tôi.
Kiểm tra hồi quy là một ý tưởng tuyệt vời. Tại sao mọi người không làm điều đó thường xuyên hơn? Đó
đây là vấn đề nhỏ với thử nghiệm hồi quy. Thường khi mọi người thực hành nó, họ
thực hiện tại giao diện ứng dụng. Nó không quan trọng cho dù nó là một ứng dụng web-
tion, một ứng dụng dòng lệnh hoặc một ứng dụng dựa trên GUI; kiểm tra hồi quy-
ing theo truyền thống được xem như một phong cách kiểm thử cấp ứng dụng. Nhưng đây là
thật không may. Phản hồi mà chúng tôi có thể nhận được từ nó là rất hữu ích. Nó trả tiền để làm điều đó tại một
mức độ mịn.

Hãy làm một thử nghiệm nhỏ. Chúng tôi đang bước vào một chức năng lớn
chứa một lượng lớn logic phức tạp. Chúng tôi phân tích, chúng tôi nghĩ, chúng tôi
nói chuyện với những người biết nhiều về đoạn mã đó hơn chúng ta, và sau đó
chúng tôi thực hiện một sự thay đổi. Chúng tôi muốn đảm bảo rằng thay đổi không bị phá vỡ bất kỳ-
nhưng làm thế nào chúng ta có thể làm điều đó? May mắn thay, chúng tôi có một nhóm chất lượng có một bộ
kiểm tra hồi quy mà nó có thể chạy qua đêm. Chúng tôi gọi điện và yêu cầu họ lên lịch
chạy, và họ nói rằng, vâng, họ có thể chạy các bài kiểm tra trong đêm, nhưng đó là một
điều mà chúng tôi đã gọi sớm. Các nhóm khác thường cố gắng lên lịch chạy hồi quy
vào giữa tuần và nếu chúng tôi đợi lâu hơn nữa, có thể sẽ không có khung thời gian và máy cho chúng tôi. Chúng tôi thở phào nhẹ nhõm rồi đi
trở lại công việc. Chúng tôi có khoảng năm thay đổi nữa để thực hiện như lần cuối cùng. Tất cả
chúng nằm trong những khu vực phức tạp như nhau. Và chúng tôi không đơn độc. Chúng tôi biết rằng sev-
eral những người khác cũng đang thực hiện thay đổi.
Sáng hôm sau, chúng tôi nhận được một cuộc điện thoại. Daiva trong quá trình thử nghiệm cho chúng tôi biết rằng
kiểm tra AE1021 và AE1029 không thành công trong một đêm. Cô ấy không chắc liệu đó có phải là của chúng tôi
nhưng cô ấy đang gọi cho chúng tôi vì cô ấy biết chúng tôi sẽ giải quyết cho cô ấy.
Chúng tôi sẽ gỡ lỗi và xem lỗi có phải do một trong những thay đổi của chúng tôi hay do một số-
của người khác.
Điều này nghe có thật không? Thật không may, nó rất thực tế.
Hãy xem xét một kịch bản khác.
Chúng ta cần thay đổi một hàm khá dài và phức tạp. May mắn thay,
chúng tôi tìm thấy một tập hợp các bài kiểm tra đơn vị dành cho nó. Những người cuối cùng chạm vào mã
đã viết một bộ gồm khoảng 20 bài kiểm tra đơn vị để thực hiện nó một cách triệt để. Chúng tôi điều hành chúng và
khám phá ra rằng tất cả họ đều vượt qua. Tiếp theo, chúng tôi xem xét các bài kiểm tra để có được cảm giác
hành vi thực tế của mã là gì.
Chúng tôi đã sẵn sàng để thực hiện thay đổi của mình, nhưng chúng tôi nhận ra rằng rất khó để tìm ra ...
Ure ra làm thế nào để thay đổi nó. Mã không rõ ràng và chúng tôi thực sự muốn
chịu đựng tốt hơn trước khi thực hiện thay đổi của chúng tôi. Các bài kiểm tra sẽ không nắm bắt được tất cả mọi thứ, vì vậy
chúng tôi muốn làm cho mã thật rõ ràng để chúng tôi có thể tự tin hơn vào
sự thay đổi của chúng tôi. Bên cạnh đó, chúng tôi không muốn bản thân hoặc bất kỳ ai khác phải
đi qua công việc chúng tôi đang làm để cố gắng hiểu nó. Thật lãng phí
thời gian!
Chúng tôi bắt đầu cấu trúc lại mã một chút. Chúng tôi trích xuất một số phương pháp và di chuyển một số
logic điều kiện. Sau mỗi thay đổi nhỏ mà chúng tôi thực hiện, chúng tôi chạy bộ nhỏ đó
của các bài kiểm tra đơn vị. Chúng vượt qua hầu hết mọi thời điểm mà chúng tôi chạy chúng. Một vài phút trước,
chúng tôi đã mắc sai lầm và đảo ngược logic với một điều kiện, nhưng một thử nghiệm không thành công và
chúng tôi đã phục hồi trong khoảng một phút. Khi chúng tôi hoàn tất cấu trúc lại, mã là
rõ ràng hơn nhiều. Chúng tôi thực hiện thay đổi mà chúng tôi đã đặt ra và chúng tôi tự tin
rằng nó là đúng. Chúng tôi đã thêm một số thử nghiệm để xác minh hành vi mới. Chương trình tiếp theo-
những người soạn nhạc làm việc trên đoạn mã này sẽ có thời gian dễ dàng hơn và sẽ có
kiểm tra chức năng của nó.
Bạn muốn phản hồi của mình trong một phút hay qua đêm? Kịch bản nào là
hiệu quả hơn?
Kiểm thử đơn vị là một trong những thành phần quan trọng nhất trong công việc mã kế thừa.
Các bài kiểm tra hồi quy cấp hệ thống là rất tốt, nhưng các bài kiểm tra nhỏ, được bản địa hóa là vô giá.
Họ có thể cung cấp cho bạn phản hồi khi bạn phát triển và cho phép bạn tái cấu trúc
an toàn hơn nhiều.

## What Is Unit Testing?
Thuật ngữ kiểm thử đơn vị có một lịch sử lâu đời trong phát triển phần mềm. Thông thường đối với
hầu hết các quan niệm về các bài kiểm tra đơn vị là ý tưởng rằng chúng là các bài kiểm tra tách biệt với
các thành phần vidual của phần mềm. Các thành phần là gì? Định nghĩa khác nhau,
nhưng trong thử nghiệm đơn vị, chúng tôi thường quan tâm đến hành vi nguyên tử nhất
đơn vị của một hệ thống. Trong mã thủ tục, các đơn vị thường là các hàm. Trong đối tượng-
mã định hướng, các đơn vị là các lớp.

> Test Harnesses
> Trong cuốn sách này, tôi sử dụng thuật ngữ khai thác thử nghiệm làm thuật ngữ chung cho mã thử nghiệm mà chúng tôi
> viết để thực hiện một số phần mềm và mã cần thiết để chạy nó. Chúng ta có thể
> sử dụng nhiều loại dây kiểm tra khác nhau để làm việc với mã của chúng tôi. Trong Chương 5, Công cụ,
> Tôi thảo luận về khung thử nghiệm xUnit và khung FIT. Cả hai đều có thể
> được sử dụng để làm bài kiểm tra mà tôi mô tả trong cuốn sách này.

Chúng ta có thể kiểm tra chỉ một hàm hoặc một lớp không? Trong các hệ thống thủ tục, nó là
thường khó kiểm tra các chức năng một cách cô lập. Các chức năng cấp cao nhất gọi func-
tions, gọi các chức năng khác, hoàn toàn xuống cấp độ máy. Trong
hệ thống hướng đối tượng, việc kiểm tra các lớp riêng biệt sẽ dễ dàng hơn một chút, nhưng thực tế
là, các lớp học thường không sống biệt lập. Hãy nghĩ về tất cả các lớp học mà bạn đã học
đã từng được viết rằng không sử dụng các lớp khác. Chúng khá hiếm, phải không? Usu-
đồng minh chúng là các lớp dữ liệu nhỏ hoặc các lớp cấu trúc dữ liệu như ngăn xếp và
hàng đợi (và thậm chí chúng có thể sử dụng các lớp khác).
Thử nghiệm tách biệt là một phần quan trọng trong định nghĩa của thử nghiệm đơn vị, nhưng
tại sao nó lại quan trọng? Rốt cuộc, nhiều lỗi có thể xảy ra khi các phần mềm
được tích hợp. Không nên thử nghiệm lớn bao gồm các vùng chức năng rộng của mã
quan trọng hơn? Chà, chúng rất quan trọng, tôi không phủ nhận điều đó, nhưng có một
một số vấn đề với các thử nghiệm lớn:
• Bản địa hóa lỗi — Khi các bài kiểm tra tiến xa hơn so với những gì chúng kiểm tra, sẽ khó hơn
xác định ý nghĩa của lỗi thử nghiệm. Thường thì phải làm việc đáng kể để
xác định nguồn gốc của lỗi kiểm tra. Bạn phải xem các đầu vào kiểm tra,
xem xét sự cố và xác định vị trí dọc theo con đường từ đầu vào đến đầu ra-
đặt sự thất bại xảy ra. Có, chúng tôi cũng phải làm điều đó cho các bài kiểm tra đơn vị, nhưng
thường thì công việc tầm thường.
• Thời gian thực thi — Các thử nghiệm lớn hơn có xu hướng mất nhiều thời gian hơn để thực thi. Điều này có xu hướng
làm cho chạy thử nghiệm khá khó chịu. Các bài kiểm tra mất quá nhiều thời gian để chạy
không được chạy.
• Mức độ phù hợp — Khó có thể thấy mối liên hệ giữa một đoạn mã và
các giá trị thực hiện nó. Chúng tôi thường có thể tìm hiểu xem một đoạn mã có
được thực hiện bằng một bài kiểm tra bằng cách sử dụng các công cụ phù hợp, nhưng khi chúng tôi thêm mã mới, chúng tôi
có thể phải làm những công việc đáng kể để tạo ra các bài kiểm tra cấp cao
mã mới.

Một trong những điều khó chịu nhất về các thử nghiệm lớn hơn là chúng tôi có thể có lỗi cục bộ-
nếu chúng tôi chạy các thử nghiệm thường xuyên hơn, nhưng rất khó đạt được. Nếu chúng tôi điều hành
các bài kiểm tra và chúng vượt qua, sau đó chúng tôi thực hiện một thay đổi nhỏ và chúng thất bại, chúng tôi biết trước
chính xác nơi mà vấn đề đã được kích hoạt. Đó là điều chúng tôi đã làm trong lần cuối cùng
thay đổi. Chúng tôi có thể quay lại thay đổi và thử lại. Nhưng nếu các thử nghiệm của chúng tôi lớn, thực thi-
thời gian có thể quá dài; xu hướng của chúng tôi sẽ là tránh chạy các bài kiểm tra thường xuyên
đủ để thực sự khoanh vùng các lỗi.
Các bài kiểm tra đơn vị lấp đầy khoảng trống mà các bài kiểm tra lớn hơn không thể. Chúng tôi có thể kiểm tra các đoạn mã không hạn chế-
lơ lửng; chúng tôi có thể nhóm các thử nghiệm để có thể chạy một số trong một số điều kiện
và những người khác trong các điều kiện khác. Với chúng, chúng tôi có thể khoanh vùng các lỗi một cách nhanh chóng. Nếu
chúng tôi nghĩ rằng có lỗi trong một số đoạn mã cụ thể và chúng tôi có thể sử dụng nó trong
khai thác kiểm tra, chúng tôi thường có thể viết mã kiểm tra nhanh chóng để xem liệu lỗi có thực sự là
ở đó.
Dưới đây là những phẩm chất của bài kiểm tra đơn vị tốt:
1. Họ chạy nhanh.
2. Chúng giúp chúng tôi khoanh vùng các vấn đề.
Trong ngành, mọi người thường nói đi nói lại xem
các bài kiểm tra là các bài kiểm tra đơn vị. Một bài kiểm tra có thực sự là một bài kiểm tra đơn vị nếu nó sử dụng một lớp sản xuất khác không?
Tôi quay lại hai phẩm chất: Chạy thử có nhanh không? Nó có thể giúp chúng tôi bản địa hóa không
lỗi nhanh chóng? Đương nhiên, có một sự liên tục. Một số thử nghiệm lớn hơn và chúng
sử dụng nhiều lớp với nhau. Trên thực tế, chúng có vẻ là những bài kiểm tra tích hợp nhỏ.
Tự bản thân chúng có vẻ chạy nhanh, nhưng điều gì sẽ xảy ra khi bạn chạy
tất cả chúng cùng nhau? Khi bạn có một bài kiểm tra bao gồm một lớp học cùng với một số
cộng tác viên của nó, nó có xu hướng phát triển. Nếu bạn không dành thời gian để làm
lớp có thể khởi tạo riêng biệt trong bộ khai thác thử nghiệm, sẽ dễ dàng như thế nào khi bạn thêm
thêm mã? Nó không bao giờ trở nên dễ dàng hơn. Mọi người dập tắt nó đi. Theo thời gian, bài kiểm tra có thể kết thúc
mất tới 1/10 giây để thực thi.
> Một bài kiểm tra đơn vị mất 1/10 giây để chạy là bài kiểm tra đơn vị chậm.

Vâng tôi rất nghiêm túc. Tại thời điểm tôi viết bài này, 1/10 giây là
eon cho một bài kiểm tra đơn vị. Hãy làm phép toán. Nếu bạn có một dự án với 3.000 lớp
và có khoảng 10 bài kiểm tra mỗi người, tức là 30.000 bài kiểm tra. Nó sẽ mất bao lâu để
chạy tất cả các bài kiểm tra cho dự án đó nếu chúng chiếm 1/10 của mỗi giây? Đóng o một giờ. Đó là một thời gian dài để chờ đợi phản hồi. Bạn không có 3.000
các lớp học? Cắt nó làm đôi. Đó vẫn là một nửa giờ. Mặt khác, điều gì sẽ xảy ra nếu
kiểm tra mất 1/100 của mỗi giây? Bây giờ chúng ta đang nói về 5 đến 10 phút-
utes. Khi họ mất nhiều thời gian, tôi đảm bảo rằng tôi sử dụng một tập hợp con để làm việc với,
nhưng tôi không ngại chạy tất cả chúng vài giờ một lần.
Với sự trợ giúp của Định luật Moore, tôi hy vọng sẽ thấy phản hồi về thử nghiệm gần như tức thời
cho cả những hệ thống lớn nhất trong đời tôi. Tôi nghi ngờ rằng làm việc trong hệ thống đó-
tems sẽ giống như làm việc trong mã có thể cắn lại. Nó sẽ có khả năng cho phép
chúng tôi biết khi nào nó đang bị thay đổi theo hướng xấu.
Các bài kiểm tra đơn vị chạy nhanh. Nếu chúng không chạy nhanh, chúng không phải là bài kiểm tra đơn vị.
Các loại kiểm tra khác thường giả dạng như kiểm tra đơn vị. Một bài kiểm tra không phải là một bài kiểm tra đơn vị nếu:
1. Nó nói chuyện với một cơ sở dữ liệu.
2. Nó giao tiếp qua mạng.
3. Nó chạm vào hệ thống tệp.
4. Bạn phải làm những điều đặc biệt cho môi trường của bạn
(chẳng hạn như chỉnh sửa tệp cấu hình) để chạy nó.
Các thử nghiệm thực hiện những điều này không tệ. Thường thì chúng rất đáng để viết và bạn nói chung
sẽ viết chúng trong khai thác thử nghiệm đơn vị. Tuy nhiên, điều quan trọng là có thể tách
chúng từ các bài kiểm tra đơn vị thực để bạn có thể giữ một tập hợp các bài kiểm tra mà bạn có thể chạy nhanh
bất cứ khi nào bạn thực hiện thay đổi.

### Higher-Level Testing
Bài kiểm tra đơn vị là tuyệt vời, nhưng có một nơi dành cho các bài kiểm tra cấp cao hơn, các bài kiểm tra bao gồm
các tình huống và tương tác trong một ứng dụng. Các bài kiểm tra cấp cao hơn có thể được sử dụng để
ghim hành vi cho một tập hợp các lớp tại một thời điểm. Khi bạn có thể làm điều đó,
thường thì bạn có thể viết bài kiểm tra cho từng lớp dễ dàng h

### Test Coverings
Nhân loại. Nhưng khi chúng tôi kiểm tra mã của mình trước khi thay đổi, chúng tôi còn
có khả năng mắc phải bất kỳ sai lầm nào mà chúng tôi mắc phải.
Hình 2.1 cho chúng ta thấy một tập hợp nhỏ của các lớp. Chúng tôi muốn thực hiện các thay đổi đối với
Phương thức getResponseText của InvoiceUpdateResponder và phương thức getValue của
Hóa đơn . Những phương pháp đó là điểm thay đổi của chúng tôi. Chúng ta có thể che chúng bằng cách viết
kiểm tra cho các lớp học mà họ cư trú.
Để viết và chạy thử nghiệm, chúng tôi phải có khả năng tạo các phiên bản InvoiceUpdate-
Người trả lời và Hóa đơn trong bộ khai thác thử nghiệm. Chúng ta có thể làm được không? Chà, có vẻ như nó
phải đủ dễ dàng để tạo Hóa đơn; nó có một hàm tạo mà không
chấp nhận bất kỳ lập luận nào. Tuy nhiên, InvoiceUpdateResponder có thể phức tạp. Nó chấp nhận
một DBConnection, một kết nối thực với cơ sở dữ liệu trực tiếp. Chúng ta sẽ xử lý như thế nào
điều đó trong một bài kiểm tra? Chúng ta có phải thiết lập cơ sở dữ liệu với dữ liệu cho các bài kiểm tra của mình không? Đó là một
rất nhiều công việc. Kiểm tra thông qua cơ sở dữ liệu có bị chậm không? Chúng tôi không đặc biệt
quan tâm đến cơ sở dữ liệu ngay bây giờ dù sao; chúng tôi chỉ muốn đề cập đến những thay đổi của mình
trong InvoiceUpdateResponder và Invoice. Chúng tôi còn có một vấn đề lớn hơn. Con-
structor cho InvoiceUpdateResponder cần một InvoiceUpdateServlet làm đối số.
Nó sẽ dễ dàng như thế nào để tạo một trong những thứ đó? Chúng tôi có thể thay đổi mã để nó

không sử dụng servlet đó nữa. Nếu InvoiceUpdateResponder chỉ cần một chút
bit thông tin từ InvoiceUpdateServlet, chúng tôi có thể chuyển nó thay vì
chuyển toàn bộ servlet vào, nhưng chúng tôi không nên có một bài kiểm tra để đảm bảo
rằng chúng tôi đã thực hiện thay đổi đó một cách chính xác?
Tất cả những vấn đề này đều là vấn đề phụ thuộc. Khi các lớp học phụ thuộc
trực tiếp vào những thứ khó sử dụng trong bài kiểm tra, chúng khó sửa đổi và
khó làm việc với.
Sự phụ thuộc là một trong những vấn đề quan trọng nhất trong phát triển phần mềm. Nhiều chân-
công việc mã acy liên quan đến việc phá vỡ các phụ thuộc để thay đổi có thể dễ dàng hơn.
Vì vậy, làm thế nào để làm điều đó? Làm cách nào để chúng tôi có được các bài kiểm tra tại chỗ mà không cần thay đổi mã?
Thực tế đáng buồn là, trong nhiều trường hợp, nó không thực tế lắm. Trong một số trường hợp, nó có thể
thậm chí là không thể. Trong ví dụ vừa thấy, chúng ta có thể cố gắng vượt qua
vấn đề DBConnection bằng cách sử dụng cơ sở dữ liệu thực, còn vấn đề về servlet thì sao?
Chúng ta có phải tạo một servlet đầy đủ và chuyển nó đến hàm tạo của InvoiceUpdat-
eResponder? Chúng ta có thể đưa nó vào đúng trạng thái không? Nó có thể có thể. Sẽ ra sao
chúng tôi làm gì nếu chúng tôi đang làm việc trong một ứng dụng GUI trên máy tính để bàn? Chúng tôi có thể không có
bất kỳ giao diện lập trình nào. Logic có thể được gắn ngay vào các lớp GUI.
chúng ta làm gì sau đó?
Thế tiến thoái lưỡng nan về mã kế thừa
Khi chúng tôi thay đổi mã, chúng tôi nên có các thử nghiệm tại chỗ. Để thực hiện các thử nghiệm, chúng tôi thường
phải thay đổi mã.
Trong ví dụ về Hóa đơn, chúng tôi có thể thử kiểm tra ở cấp độ cao hơn. Nếu nó khó
viết các bài kiểm tra mà không thay đổi một lớp cụ thể, đôi khi kiểm tra một lớp
sử dụng nó dễ dàng hơn; bất kể, chúng tôi thường phải phá vỡ sự phụ thuộc giữa
các lớp học ở đâu đó. Trong trường hợp này, chúng ta có thể phá vỡ sự phụ thuộc vào InvoiceUpdate-
Servlet bằng cách chuyển một thứ mà InvoiceUpdateResponder thực sự cần. Nó cần
tập hợp các ID hóa đơn mà InvoiceUpdateServlet nắm giữ. Chúng tôi cũng có thể
phá vỡ sự phụ thuộc mà InvoiceUpdateResponder có trên DBConnection bằng cách giới thiệu
tạo giao diện (IDBConnection) và thay đổi InvoiceUpdateResponder để
mà nó sử dụng giao diện thay thế. Hình 2.2 cho thấy trạng thái của các lớp này sau
những thay đổi

Điều này có an toàn để thực hiện những tái cấu trúc này mà không cần thử nghiệm không? Nó có thể. Cơ cấu lại này-
ings được đặt tên là Primitivize Parameter (385) và Extract Interface (362), tương ứng
cẩn thận. Chúng được mô tả trong danh mục kỹ thuật phá vỡ phụ thuộc tại
cuối sách. Khi chúng tôi phá vỡ các phụ thuộc, chúng tôi thường có thể viết các bài kiểm tra
thực hiện nhiều thay đổi xâm lấn an toàn hơn. Bí quyết là thực hiện những tái cấu trúc ban đầu này
rất thận trọng.
Bảo thủ là điều đúng đắn cần làm khi chúng ta có thể giới thiệu
nhưng đôi khi khi chúng tôi phá vỡ các phần phụ thuộc để bao gồm mã, nó không
hóa ra độc đáo như những gì chúng ta đã làm trong ví dụ trước. Chúng tôi có thể giới thiệu
các tham số cho các phương pháp không hoàn toàn cần thiết trong mã sản xuất hoặc chúng tôi
có thể phá vỡ các lớp học theo những cách kỳ lạ chỉ để có thể thực hiện các bài kiểm tra tại chỗ. Khi nào
chúng tôi làm điều đó, chúng tôi có thể làm cho mã trông kém hơn một chút trong lĩnh vực đó. Nếu
chúng tôi đã bớt thận trọng hơn, chúng tôi sẽ sửa nó ngay lập tức. Chúng tôi có thể làm điều đó, nhưng nó phụ thuộc vào mức độ rủi ro có liên quan. Khi lỗi là một vấn đề lớn, và
họ thường như vậy, nó trả tiền để được bảo thủ.
Di sản
Thay đổi mã
Thuật toán
Khi bạn phá vỡ sự phụ thuộc trong mã kế thừa, bạn thường phải tạm dừng ý thức của mình
của thẩm mỹ một chút. Một số phụ thuộc phá vỡ rõ ràng; những người khác cuối cùng trông ít hơn
lý tưởng từ quan điểm thiết kế. Chúng giống như các điểm rạch trong phẫu thuật:
có thể là một vết sẹo để lại trong mã của bạn sau khi bạn làm việc, nhưng mọi thứ bên dưới nó có thể nhận được
tốt hơn.
Nếu sau này, bạn có thể bao gồm mã xung quanh điểm mà bạn đã phá vỡ các phụ thuộc, bạn
cũng có thể chữa lành vết sẹo đó.

### The Legacy Code Change Algorithm
Khi bạn phải thực hiện thay đổi trong cơ sở mã kế thừa, đây là một thuật toán
bạn có thể dùng.
1. Xác định các điểm thay đổi.
2. Tìm điểm kiểm tra.
3. Phá vỡ các phụ thuộc.
4. Viết các bài kiểm tra.
5. Thực hiện thay đổi và tái cấu trúc.
Mục tiêu hàng ngày trong mã kế thừa là thực hiện các thay đổi, nhưng không chỉ là bất kỳ
những thay đổi. Chúng tôi muốn thực hiện các thay đổi chức năng mang lại giá trị đồng thời mang lại
nhiều hệ thống đang được thử nghiệm. Vào cuối mỗi tập chương trình, chúng tôi
không chỉ có thể trỏ đến mã cung cấp một số tính năng mới, mà còn
cũng như các thử nghiệm của nó. Theo thời gian, các khu vực được thử nghiệm của bề mặt cơ sở mã giống như những hòn đảo nổi lên
ngoài đại dương. Công việc ở những hòn đảo này trở nên dễ dàng hơn nhiều. Theo thời gian,
đảo trở thành bãi đất liền lớn. Cuối cùng, bạn sẽ có thể làm việc trong
nents của mã được kiểm tra.
Hãy xem xét từng bước này và cách cuốn sách của anh ấy sẽ giúp bạn thực hiện chúng.

### Identify Change Points
Những nơi bạn cần thực hiện thay đổi phụ thuộc một cách nhạy cảm vào
ngành kiến trúc. Nếu bạn không hiểu rõ về thiết kế của mình để cảm thấy rằng bạn đang
thay đổi đúng chỗ, hãy xem Chương 16, Tôi Không Dưới-
Giữ cho Mã Đủ Tốt Để Thay Đổi Nó, và Chương 17, Ứng Dụng Của Tôi
Không có cấu trúc.

### Find Test Points
Trong một số trường hợp, việc tìm kiếm nơi để viết các bài kiểm tra rất dễ dàng, nhưng trong mã kế thừa, nó thường có thể
cứng rắn. Hãy xem Chương 11, Tôi Cần Thay Đổi. Phương pháp nào
Tôi Có Nên Kiểm Tra Không ?, và Chương 12, Tôi Cần Thực Hiện Nhiều Thay Đổi Trong Một Lĩnh Vực.
Tôi Có Phải Phá Bỏ Sự Phụ Thuộc Cho Tất Cả Các Lớp Tham Gia Không? Những chương này
đưa ra các kỹ thuật mà bạn có thể sử dụng để xác định nơi bạn cần viết
kiểm tra các thay đổi cụ thể.

### Break Dependencies
Sự phụ thuộc thường là trở ngại rõ ràng nhất đối với thử nghiệm. Hai cách
vấn đề này biểu hiện chính nó là khó khởi tạo đối tượng trong khai thác thử nghiệm
và khó chạy các phương pháp trong khai thác thử nghiệm. Thông thường trong mã kế thừa, bạn có
để phá vỡ sự phụ thuộc để có được các bài kiểm tra tại chỗ. Tốt nhất, chúng tôi sẽ có các bài kiểm tra cho biết
chúng tôi liệu những điều chúng tôi làm để phá vỡ sự phụ thuộc có gây ra xác suất không-
lems, nhưng thường thì không. Hãy xem Chương 23, Làm thế nào để tôi biết rằng tôi là
Không phá vỡ bất cứ điều gì ?, để xem một số phương pháp có thể được sử dụng để làm cho
vết rạch đầu tiên trong một hệ thống an toàn hơn khi bạn bắt đầu mang nó đi kiểm tra. Khi bạn
đã làm được điều này, hãy xem Chương 9, Tôi không thể đưa lớp này vào một bài kiểm tra Har-
ness và Chương 10, Tôi không thể chạy phương pháp này trong khai thác thử nghiệm, cho các tình huống
cho thấy cách vượt qua các vấn đề phụ thuộc phổ biến. Những phần này
tham khảo nhiều danh mục các kỹ thuật phá vỡ sự phụ thuộc ở phía sau
nhưng chúng không bao gồm tất cả các kỹ thuật. Hãy dành chút thời gian để xem xét
thông qua danh mục để biết thêm ý tưởng về cách phá vỡ sự phụ thuộc.
Sự phụ thuộc cũng xuất hiện khi chúng tôi có ý tưởng cho một thử nghiệm nhưng chúng tôi không thể
viết nó một cách dễ dàng. Nếu bạn thấy rằng bạn không thể viết các bài kiểm tra vì sự phụ thuộc vào
các phương pháp lớn, xem Chương 22, Tôi Cần Thay đổi Phương pháp Quái vật và Tôi
Không thể viết bài kiểm tra cho nó. Nếu bạn thấy rằng bạn có thể phá vỡ các phụ thuộc, nhưng nó
mất quá nhiều thời gian để xây dựng các bài kiểm tra của bạn, hãy xem Chương 7, Mất Mãi Mãi
Thay đổi. Chương đó mô tả công việc phá vỡ sự phụ thuộc bổ sung
mà bạn có thể làm để làm cho thời gian xây dựng trung bình của mình nhanh hơn.

### Write Tests
Tôi thấy rằng các bài kiểm tra tôi viết bằng mã kế thừa hơi khác so với các bài kiểm tra tôi
viết cho mã mới. Hãy xem Chương 13, Tôi Cần Thay Đổi Nhưng Tôi
Không biết bài kiểm tra nào cần viết, để tìm hiểu thêm về vai trò của bài kiểm tra trong kế thừa
công việc mã.

### Make Changes and Refactor
Tôi ủng hộ việc sử dụng phát triển theo hướng thử nghiệm (TDD) để thêm các tính năng trong mã kế thừa.
Có một mô tả về TDD và một số kỹ thuật bổ sung tính năng khác trong
Chương 8, Làm cách nào để thêm một tính năng? Sau khi thực hiện các thay đổi trong mã kế thừa, chúng tôi
thường thành thạo hơn với các vấn đề của nó và các bài kiểm tra chúng tôi đã viết để bổ sung
tures thường cung cấp cho chúng tôi một số vỏ bọc để thực hiện một số tái cấu trúc. Chương 20, lớp này là
Quá lớn và tôi không muốn nó lớn hơn nữa; Chương 22, tôi cần thay đổi
một phương pháp quái vật và tôi không thể viết thử nghiệm cho nó; và Chương 21, Tôi là Chang-
ing Mã giống nhau ở khắp nơi bao gồm nhiều kỹ thuật bạn có thể sử dụng
để bắt đầu chuyển mã kế thừa của bạn sang cấu trúc tốt hơn. Hãy nhớ rằng
những điều tôi mô tả trong các chương này là “các bước của em bé”. Họ không chỉ cho bạn cách
để làm cho thiết kế của bạn trở nên lý tưởng, sạch sẽ hoặc phong phú. Rất nhiều sách cho thấy
làm thế nào để thực hiện những điều đó và khi bạn có cơ hội sử dụng những công nghệ đó-
niques, tôi khuyến khích bạn làm như vậy. Các chương này hướng dẫn bạn cách thiết kế
tốt hơn, trong đó “tốt hơn” phụ thuộc vào ngữ cảnh và thường chỉ cần thêm một vài bước
có thể bảo trì hơn thiết kế trước đây. Nhưng đừng giảm giá công việc này. Thường
những điều đơn giản nhất, chẳng hạn như chia nhỏ một lớp lớn chỉ để làm cho nó dễ dàng hơn
làm việc với, có thể tạo ra sự khác biệt đáng kể trong các ứng dụng, mặc dù
hơi máy móc.

### The Rest of This Book
Phần còn lại của cuốn sách này hướng dẫn bạn cách thực hiện các thay đổi trong mã kế thừa. Tiếp theo
hai chương chứa một số tài liệu cơ bản về ba khái niệm quan trọng trong
công việc kế thừa: cảm biến, phân tách và đường nối.

