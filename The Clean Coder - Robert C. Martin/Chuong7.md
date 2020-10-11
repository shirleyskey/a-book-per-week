# Chapter 07: Acceptance Testing 
Vai trò của nhà phát triển chuyên nghiệp là vai trò truyền thông cũng như phát triển
vai trò lựa chọn. Hãy nhớ rằng tính năng đổ rác / đổ rác cũng áp dụng cho các lập trình viên,
vì vậy các lập trình viên chuyên nghiệp hãy cẩn thận để đảm bảo rằng giao tiếp của họ
với các thành viên khác của nhóm và doanh nghiệp, là chính xác và lành mạnh.

Một trong những vấn đề giao tiếp phổ biến nhất giữa các lập trình viên và
kinh doanh là các yêu cầu. Những người kinh doanh tuyên bố những gì họ tin tưởng
cần, và sau đó các lập trình viên xây dựng những gì họ tin rằng doanh nghiệp đã mô tả.
Ít nhất đó là cách nó phải hoạt động. Trong thực tế, giao tiếp của
yêu cầu cực kỳ khó và quy trình này có rất nhiều lỗi.
Năm 1979, khi đang làm việc tại Teradyne, tôi được Tom, người quản lý của
lắp đặt và dịch vụ hiện trường. Anh ấy yêu cầu tôi chỉ cho anh ấy cách sử dụng ED-402
trình soạn thảo văn bản để tạo một hệ thống xử lý sự cố đơn giản.
ED-402 là một trình soạn thảo độc quyền được viết cho máy tính M365,
Bản sao PDP-8 của Teradyne. Là một trình soạn thảo văn bản, nó rất mạnh mẽ. Nó đã được tích hợp sẵn
ngôn ngữ kịch bản mà chúng tôi đã sử dụng cho tất cả các loại ứng dụng văn bản đơn giản.
Tom không phải là một lập trình viên. Nhưng ứng dụng anh ấy nghĩ rất đơn giản, vì vậy
anh ấy nghĩ tôi có thể dạy anh ấy nhanh chóng và sau đó anh ấy có thể viết đơn
bản thân anh ấy. Trong sự ngây thơ của mình, tôi đã nghĩ điều tương tự. Rốt cuộc, ngôn ngữ kịch bản
không chỉ là một ngôn ngữ macro cho các lệnh chỉnh sửa, với rất
quyết định thô sơ và cấu trúc lặp.
Vì vậy, chúng tôi đã ngồi lại với nhau và tôi hỏi anh ấy muốn ứng dụng của anh ấy làm gì.
Anh ấy bắt đầu với màn hình nhập cảnh ban đầu. Tôi đã chỉ cho anh ấy cách tạo một tệp văn bản
điều đó sẽ chứa các câu lệnh script và cách nhập biểu tượng
biểu diễn các lệnh chỉnh sửa vào tập lệnh đó. Nhưng khi tôi nhìn vào
mắt anh, không có gì nhìn lại. Lời giải thích của tôi đơn giản là vô nghĩa
với anh ta ở tất cả.
Đây là lần đầu tiên tôi gặp phải điều này. Đối với tôi, đó là một điều đơn giản để
biểu diễn các lệnh của trình soạn thảo một cách tượng trưng. Ví dụ: để đại diện cho một điều khiển-B
lệnh (lệnh đặt con trỏ ở đầu dòng
dòng) bạn chỉ cần nhập ^ B vào tệp script. Nhưng điều này không có ý nghĩa gì đối với Tom. Anh ta
không thể thực hiện bước nhảy vọt từ chỉnh sửa tệp sang chỉnh sửa tệp đã chỉnh sửa tệp.
Tom không ngốc. Tôi nghĩ rằng anh ấy chỉ đơn giản nhận ra rằng điều này sẽ rất nhiều
tham gia nhiều hơn những gì anh ấy nghĩ ban đầu và anh ấy không muốn đầu tư thời gian
và năng lượng tinh thần cần thiết để học một thứ gì đó phức tạp đến nỗi
sử dụng một trình soạn thảo để chỉ huy một trình soạn thảo.
Vì vậy, từng chút một, tôi thấy mình đang triển khai ứng dụng này trong khi anh ấy ngồi đó
đã xem. Trong vòng hai mươi phút đầu tiên, rõ ràng là sự nhấn mạnh của anh ấy đã
đã thay đổi từ việc học cách tự làm điều đó sang việc đảm bảo rằng những gì tôi đã làm là
những gì anh ấy muốn.

Chúng tôi đã mất cả ngày. Anh ấy sẽ mô tả một tính năng và tôi sẽ triển khai nó
khi anh ấy quan sát. Thời gian chu kỳ là năm phút hoặc ít hơn, vì vậy không có lý do
để anh ta đứng dậy và làm bất cứ điều gì khác. Anh ấy sẽ yêu cầu tôi làm X và trong vòng năm
phút tôi đã có X làm việc.
Thường thì anh ấy sẽ vẽ những gì anh ấy muốn trên một tờ giấy nháp. Một số điều
anh ấy muốn khó thực hiện trong ED-402, vì vậy tôi muốn đề xuất một cái gì đó khác. Thứ Tư
cuối cùng đồng ý về một cái gì đó sẽ hoạt động và sau đó tôi sẽ làm cho nó hoạt động.
Nhưng sau đó chúng tôi sẽ thử và anh ấy sẽ thay đổi quyết định. Anh ấy sẽ nói điều gì đó như, "Vâng,
điều đó chỉ không có luồng mà tôi đang tìm kiếm. Hãy thử theo một cách khác. "
Giờ này qua giờ khác, chúng tôi mày mò, chọc ngoáy và thúc đẩy ứng dụng đó thành hình.
Chúng tôi đã thử cái này, rồi cái khác, rồi cái khác. Nó trở nên rất rõ ràng với tôi
rằng anh ấy là nhà điêu khắc, và tôi là công cụ anh ấy đang sử dụng.
Cuối cùng, anh ấy đã nhận được ứng dụng mà anh ấy đang tìm kiếm nhưng không biết làm thế nào để
đi về việc xây dựng cái tiếp theo cho chính mình. Mặt khác, tôi đã học được một
bài học mạnh mẽ về cách khách hàng thực sự khám phá những gì họ cần. tôi đã học
rằng tầm nhìn của họ về các tính năng thường không tồn tại khi tiếp xúc thực tế với
máy vi tính.
## P R E M AT U R E P R E C I S I O N
Cả doanh nghiệp và lập trình viên đều bị cám dỗ để rơi vào bẫy của
độ chính xác. Những người kinh doanh muốn biết chính xác những gì họ sẽ nhận được trước khi
họ cho phép một dự án. Các nhà phát triển muốn biết chính xác những gì họ được cho là
để cung cấp trước khi họ ước tính dự án. Cả hai bên đều muốn có độ chính xác đơn giản
không thể đạt được, và thường sẵn sàng lãng phí một gia tài để cố gắng đạt được nó.
#### Nguyên tắc không chắc chắn
Vấn đề là mọi thứ xuất hiện trên giấy khác với chúng trong một
hệ thống. Khi doanh nghiệp thực sự thấy những gì họ chỉ định đang chạy trong một hệ thống,
họ nhận ra rằng đó không phải là điều họ muốn. Khi họ thấy yêu cầu
thực sự đang chạy, họ có ý tưởng tốt hơn về những gì họ thực sự muốn — và đó là
thường không phải những gì họ đang thấy.

Có một loại hiệu ứng người quan sát, hay nguyên tắc bất định, đang diễn ra. Khi bạn
thể hiện một tính năng cho doanh nghiệp, nó cung cấp cho họ nhiều thông tin hơn
đã có trước đó và thông tin mới đó ảnh hưởng đến cách họ nhìn toàn bộ hệ thống.
Cuối cùng, bạn đưa ra các yêu cầu của mình càng chính xác thì chúng càng ít liên quan hơn
trở thành khi hệ thống được thực hiện.
#### Ước tính Lo lắng
Các nhà phát triển cũng có thể mắc vào cái bẫy chính xác. Họ biết họ phải
ước lượng hệ thống và thường nghĩ rằng điều này đòi hỏi độ chính xác. Nó không.
Đầu tiên, ngay cả với thông tin hoàn hảo, ước tính của bạn sẽ có một phương sai rất lớn.
Thứ hai, nguyên tắc không chắc chắn làm cho băm không chính xác sớm. Các
yêu cầu sẽ thay đổi làm cho cuộc tranh luận chính xác đó.
Các nhà phát triển chuyên nghiệp hiểu rằng các ước tính có thể và nên được thực hiện
dựa trên các yêu cầu về độ chính xác thấp và nhận ra rằng những ước tính đó
ước tính. Để củng cố điều này, các nhà phát triển chuyên nghiệp luôn bao gồm các thanh lỗi
với các ước tính của họ để doanh nghiệp hiểu được sự không chắc chắn. (Xem
Chương 10, “Ước tính.”)
### L AT E A M B I G U I T Y
Giải pháp cho độ chính xác sớm là trì hoãn độ chính xác càng lâu càng tốt.
Các nhà phát triển chuyên nghiệp không đưa ra yêu cầu cho đến khi họ vừa
để phát triển nó. Tuy nhiên, điều đó có thể dẫn đến một chứng bệnh khác: sự mơ hồ muộn màng.
Thường thì các bên liên quan không đồng ý. Khi họ làm như vậy, họ có thể thấy dễ dàng hơn khi luyện chữ
cách của họ để giải quyết bất đồng hơn là giải quyết nó. Họ sẽ tìm ra cách nào đó
diễn đạt yêu cầu mà tất cả họ có thể đồng ý, mà không thực sự
giải quyết tranh chấp. Tôi đã từng nghe Tom DeMarco nói, “Một sự mơ hồ trong
tài liệu yêu cầu đại diện cho một cuộc tranh luận giữa các bên liên quan. " 1
Tất nhiên, không cần tranh cãi hay bất đồng để tạo ra sự mơ hồ.
Đôi khi các bên liên quan chỉ đơn giản cho rằng độc giả của họ biết họ muốn nói gì.

Nó có thể hoàn toàn rõ ràng với họ trong ngữ cảnh của họ, nhưng có nghĩa là
hoàn toàn khác với lập trình viên đọc nó. Loại ngữ cảnh này
sự mơ hồ cũng có thể xảy ra khi khách hàng và lập trình viên nói chuyện trực diện
đối mặt.
Sam (bên liên quan): "OK, bây giờ các tệp nhật ký này cần được sao lưu."
Paula: "OK, bao lâu một lần?"
Sam: "Hàng ngày."
Paula: “Đúng vậy. Và bạn muốn nó được lưu ở đâu? ”
Sam: "Ý bạn là gì?"
Paula: "Bạn có muốn tôi lưu nó vào một thư mục con cụ thể không?"
Sam: "Vâng, điều đó sẽ tốt."
Paula: "Chúng ta sẽ gọi nó là gì?"
Sam: "Còn về" backup "thì sao?"
Paula: “Chắc chắn rồi, sẽ ổn thôi. Vì vậy, chúng tôi sẽ ghi tệp nhật ký vào bản sao lưu
thư mục mỗi ngày. Mấy giờ?"
Sam: "Mỗi ngày."
Paula: "Không, ý tôi là bạn muốn nó viết vào thời gian nào trong ngày?"
Sam: "Bất cứ lúc nào."
Paula: "Buổi trưa?"
Sam: “Không, không phải trong giờ giao dịch. Nửa đêm sẽ tốt hơn. ”
Paula: "OK, vậy là nửa đêm."
Sam: "Tuyệt vời, cảm ơn!"
Paula: "Luôn luôn là một niềm vui."
Sau đó, Paula đang nói với đồng đội Peter về nhiệm vụ.
Paula: “OK, chúng tôi cần sao chép tệp nhật ký vào một thư mục con có tên
sao lưu hàng đêm vào lúc nửa đêm. ”
Peter: "OK, chúng ta nên sử dụng tên tệp nào?"
Paula: "log.backup phải làm điều đó."
Peter: "Bạn hiểu rồi."

Trong một văn phòng khác, Sam đang nói chuyện điện thoại với khách hàng của mình.
Sam: "Vâng, vâng, các tệp nhật ký sẽ được lưu."
Carl: “Được rồi, điều quan trọng là chúng tôi không bao giờ mất bất kỳ nhật ký nào. Chúng ta cần quay lại
thông qua tất cả các tệp nhật ký đó, thậm chí vài tháng hoặc vài năm sau, bất cứ khi nào
có sự cố, sự kiện hoặc tranh chấp. "
Sam: “Đừng lo, tôi vừa nói chuyện với Paula. Cô ấy sẽ lưu nhật ký vào một
thư mục có tên là sao lưu hàng đêm lúc nửa đêm. ”
Carl: "Được rồi, nghe hay đấy."
Tôi cho rằng bạn đã phát hiện ra sự không rõ ràng. Khách hàng mong đợi tất cả các tệp nhật ký được
đã lưu và Paula chỉ nghĩ rằng họ muốn lưu tệp nhật ký của đêm qua. Khi nào
khách hàng tìm kiếm bản sao lưu tệp nhật ký trị giá hàng tháng, họ sẽ chỉ
tìm đêm qua.
Trong trường hợp này, cả Paula và Sam đều bỏ bóng. Đó là trách nhiệm của
các nhà phát triển chuyên nghiệp (và các bên liên quan) để đảm bảo rằng mọi sự mơ hồ là
bị loại bỏ khỏi các yêu cầu.
Điều này thật khó và chỉ có một cách tôi biết cách thực hiện.
## A C C E P TA N C E T E S T S
Thuật ngữ kiểm tra chấp nhận bị quá tải và sử dụng quá mức. Một số người cho rằng
đây là những bài kiểm tra mà người dùng thực hiện trước khi họ chấp nhận bản phát hành. Những người khác
nghĩ rằng đây là các bài kiểm tra QA. Trong chương này, chúng ta sẽ định nghĩa các bài kiểm tra chấp nhận là các bài kiểm tra
được viết bởi sự hợp tác của các bên liên quan và các lập trình viên để
xác định khi nào một yêu cầu được thực hiện.
### ĐỊNH NGHĨA CỦA "LÀM XONG "
Một trong những sự mơ hồ phổ biến nhất mà chúng ta phải đối mặt với tư cách là các chuyên gia phần mềm là
không rõ ràng về "đã xong". Khi một nhà phát triển nói rằng anh ta đã hoàn thành một nhiệm vụ, điều đó làm gì
nghĩa là? Nhà phát triển có thực hiện theo nghĩa là anh ta đã sẵn sàng triển khai tính năng không
với sự tự tin đầy đủ? Hay ý của anh ấy là anh ấy đã sẵn sàng cho QA? Hoặc có lẽ anh ấy là
viết xong và đã chạy một lần nhưng chưa thực sự kiểm tra

Tôi đã làm việc với các nhóm có định nghĩa khác cho từ "đã hoàn thành"
và "hoàn thành". Một nhóm cụ thể đã sử dụng các thuật ngữ “đã hoàn thành” và “đã hoàn thành”.
Các nhà phát triển chuyên nghiệp có một định nghĩa duy nhất về done: Done có nghĩa là đã hoàn thành.
Hoàn thành nghĩa là tất cả mã được viết, tất cả các bài kiểm tra đều vượt qua, QA và các bên liên quan có
Đã được chấp nhận. Làm xong.
Nhưng làm thế nào bạn có thể đạt được mức độ hoàn thành công việc này và vẫn đạt được tiến bộ nhanh chóng từ
lặp đến lặp? Bạn tạo một tập hợp các bài kiểm tra tự động, khi chúng vượt qua,
đáp ứng tất cả các tiêu chí trên! Khi các bài kiểm tra chấp nhận cho tính năng của bạn vượt qua,
Bạn xong việc rồi.
Các nhà phát triển chuyên nghiệp luôn định nghĩa các yêu cầu của họ để
kiểm tra chấp nhận tự động. Họ làm việc với các bên liên quan và QA để đảm bảo
rằng các bài kiểm tra tự động này là một đặc điểm kỹ thuật hoàn chỉnh.
Sam: “OK, bây giờ các tệp nhật ký này cần được sao lưu.”
Paula: "OK, bao lâu một lần?"
Sam: "Hàng ngày."
Paula: “Đúng vậy. Và bạn muốn nó được lưu ở đâu? ”
Sam: "Ý bạn là gì?"
Paula: "Bạn có muốn tôi lưu nó vào một thư mục con cụ thể không?"
Sam: "Vâng, điều đó sẽ tốt."
Paula: "Chúng ta sẽ gọi nó là gì?"
Sam: “Thế còn‘ backup ’”?
Tom (người thử nghiệm): “Chờ đã, sao lưu là một cái tên quá phổ biến. Bạn thực sự là gì
lưu trữ trong thư mục này? ”
Sam: "Các bản sao lưu."
Tom: "Sao lưu cái gì?"
Sam: "Các tệp nhật ký."
Paula: “Nhưng chỉ có một tệp nhật ký.”
Sam: “Không, có rất nhiều. Một cho mỗi ngày. "
Tom: “Ý của bạn là có một tệp nhật ký hoạt động và nhiều tệp nhật ký
sao lưu? ”

Sam: "Tất nhiên."
Paula: “Ồ! Tôi đã nghĩ rằng bạn chỉ muốn một bản sao lưu tạm thời ”.
Sam: "Không, khách hàng muốn giữ tất cả chúng mãi mãi."
Paula: “Đó là một cái mới đối với tôi. OK, rất vui vì chúng tôi đã giải quyết được vấn đề đó. ”
Tom: "Vì vậy, tên của thư mục phụ sẽ cho chúng tôi biết chính xác những gì có trong đó."
Sam: "Nó có tất cả các nhật ký cũ không hoạt động."
Tom: “Vậy hãy gọi nó là old_inactive_logs.”
Sam: "Tuyệt vời."
Tom: "Vậy khi nào thì thư mục này được tạo ra?"
Sam: "Hả?"
Paula: “Chúng ta nên tạo thư mục khi hệ thống khởi động, nhưng chỉ khi
thư mục chưa tồn tại. "
Tom: “OK, đây là bài kiểm tra đầu tiên của chúng tôi. Tôi sẽ cần khởi động hệ thống và xem nếu
thư mục old_inactive_logs được tạo. Sau đó, tôi sẽ thêm một tệp vào đó
danh mục. Sau đó, tôi sẽ tắt và bắt đầu lại và đảm bảo cả hai
thư mục và tập tin vẫn còn đó. ”
Paula: “Bài kiểm tra đó sẽ khiến bạn mất nhiều thời gian để thực hiện. Khởi động hệ thống là
đã 20 giây và đang tăng lên. Hơn nữa, tôi thực sự không muốn có
để xây dựng toàn bộ hệ thống mỗi khi tôi chạy các bài kiểm tra chấp nhận. ”
Tom: "Bạn đề nghị gì?"
Paula: “Chúng tôi sẽ tạo một lớp SystemStarter. Chương trình chính sẽ tải cái này
khởi động với một nhóm các đối tượng StartupCommand, sẽ theo sau
Mẫu lệnh. Sau đó, trong quá trình khởi động hệ thống, SystemStarter
sẽ chỉ cho tất cả các đối tượng StartupCommand chạy. Một trong những
Các dẫn xuất StartupCommand sẽ tạo old_inactive_logs
nhưng chỉ khi nó chưa tồn tại. "
Tom: “Ồ, được rồi, tất cả những gì tôi cần kiểm tra là dẫn xuất StartupCommand đó.
Tôi có thể viết một bài kiểm tra FitNesse đơn giản cho điều đó. ”
Tom lên bảng.
"Phần đầu tiên sẽ giống như thế này":
đã đưa ra lệnh LogFileDirectoryStartupCommand
cho rằng thư mục old_inactive_logs không tồn tại

khi lệnh được thực hiện
thì thư mục old_inactive_logs sẽ tồn tại
và nó phải trống
“Phần thứ hai sẽ trông như thế này”:
đã đưa ra lệnh LogFileDirectoryStartupCommand
cho rằng thư mục old_inactive_logs tồn tại
và nó chứa một tệp có tên x
Khi lệnh được thực thi
Sau đó, thư mục old_inactive_logs sẽ vẫn tồn tại
và nó vẫn phải chứa một tệp có tên x
Paula: "Phải, điều đó nên che đi."
Sam: "Chà, tất cả những thứ đó có thực sự cần thiết không?"
Paula: “Sam, câu nào trong hai câu này không đủ quan trọng để
chỉ rõ? ”
Sam: “Ý tôi là có rất nhiều việc phải suy nghĩ và viết ra tất cả
những bài kiểm tra này. "
Tom: “Đúng vậy, nhưng không việc gì hơn là viết một kế hoạch kiểm tra thủ công. Và
việc thực hiện lặp đi lặp lại một bài kiểm tra thủ công còn nhiều công việc hơn. ”
### GIAO TIẾP
Mục đích của kiểm tra chấp nhận là giao tiếp, rõ ràng và chính xác. Bởi
đồng ý với họ, các nhà phát triển, các bên liên quan và người kiểm tra đều hiểu
kế hoạch cho hành vi của hệ thống là. Để đạt được sự rõ ràng này là trách nhiệm
của tất cả các bên. Các nhà phát triển chuyên nghiệp khiến họ có trách nhiệm phải làm việc với
các bên liên quan và người kiểm tra để đảm bảo rằng tất cả các bên đều biết những gì sắp được xây dựng.
### A U T O M AT I O N
Kiểm tra chấp nhận phải luôn được tự động hóa. Có một nơi để hướng dẫn sử dụng
thử nghiệm ở những nơi khác trong vòng đời phần mềm, nhưng những loại thử nghiệm này sẽ không bao giờ
được thủ công. Lý do rất đơn giản: chi phí.
Xem xét hình ảnh trong Hình 7-1. Bàn tay bạn thấy ở đó thuộc về QA
giám đốc của một công ty Internet lớn. Tài liệu anh ấy đang giữ là bảng của

nội dung cho kế hoạch kiểm tra thủ công của mình. Anh ta có một đội quân gồm những người kiểm tra thủ công ở nước ngoài
các địa điểm thực hiện kế hoạch này sáu tuần một lần. Nó tiêu tốn của anh ta hơn một triệu
đô la mọi lúc. Anh ấy đang giữ nó cho tôi vì anh ấy vừa trở về từ
một cuộc họp trong đó người quản lý của anh ấy đã nói với anh ấy rằng họ cần phải cắt giảm ngân sách của anh ấy
giảm 50%. Câu hỏi của anh ấy đối với tôi là, "Tôi không nên chạy nửa bài kiểm tra nào trong số này?"


Gọi đây là một thảm họa sẽ là một cách nói thô thiển. Chi phí vận hành
kế hoạch kiểm tra thủ công quá lớn đến nỗi họ đã quyết định hy sinh nó và
chỉ đơn giản là sống với thực tế rằng họ sẽ không biết liệu một nửa sản phẩm của họ có hoạt động hay không!
Các nhà phát triển chuyên nghiệp không để xảy ra tình trạng kiểu này. Giá của
tự động hóa các thử nghiệm chấp nhận là quá nhỏ so với chi phí thực hiện
các kế hoạch kiểm tra thủ công mà việc viết script cho con người không có ý nghĩa kinh tế
để thực hiện. Các nhà phát triển chuyên nghiệp chịu trách nhiệm về phần của họ trong việc đảm bảo
rằng các thử nghiệm chấp nhận được tự động hóa.

Có nhiều công cụ mã nguồn mở và thương mại hỗ trợ quá trình tự động hóa
của các bài kiểm tra chấp nhận. FitNesse, Cucumber, cuke4duke, khung robot và
Selenium, chỉ để đề cập đến một số ít. Tất cả các công cụ này cho phép bạn chỉ định
kiểm tra ở dạng mà những người không phải lập trình viên có thể đọc, hiểu và thậm chí là tác giả.
### E X T R A W O R K
Quan điểm của Sam về công việc là điều dễ hiểu. Nó trông giống như rất nhiều công việc phụ
để viết các bài kiểm tra chấp nhận như thế này. Nhưng với Hình 7-1, chúng ta có thể thấy rằng nó không
thực sự làm việc thêm ở tất cả. Viết các bài kiểm tra này chỉ đơn giản là công việc xác định
hệ thống. Chỉ định ở mức chi tiết này là cách duy nhất mà chúng tôi, với tư cách là các lập trình viên, có thể
biết “đã hoàn thành” nghĩa là gì. Chỉ định ở mức chi tiết này là cách duy nhất
các bên liên quan có thể đảm bảo rằng hệ thống mà họ đang trả tiền thực sự làm những gì
họ cần. Và chỉ định ở mức chi tiết này là cách duy nhất để thành công
tự động hóa các bài kiểm tra. Vì vậy, đừng xem những thử nghiệm này là công việc phụ. Hãy nhìn họ như
tiết kiệm thời gian và tiền bạc lớn. Những thử nghiệm này sẽ ngăn bạn triển khai
hệ thống sai và sẽ cho phép bạn biết khi nào bạn hoàn thành.

## W H O W R I T E S A C C E P TA N C E T E S T S , AND W H E N ?
Trong một thế giới lý tưởng, các bên liên quan và QA sẽ hợp tác để viết những
kiểm tra và các nhà phát triển sẽ xem xét chúng để đảm bảo tính nhất quán. Trong thế giới thực,
các bên liên quan hiếm khi có thời gian hoặc khuynh hướng đi sâu vào mức độ yêu cầu
của chi tiết. Vì vậy, họ thường giao trách nhiệm cho các nhà phân tích kinh doanh, QA hoặc
ngay cả các nhà phát triển. Nếu các nhà phát triển phải viết các bài kiểm tra này, thì hãy
lưu ý rằng nhà phát triển viết thử nghiệm không giống với nhà phát triển
triển khai tính năng đã thử nghiệm.
Thông thường, các nhà phân tích kinh doanh viết các phiên bản "con đường hạnh phúc" của các bài kiểm tra, bởi vì
những thử nghiệm đó mô tả các tính năng có giá trị kinh doanh. QA thường viết
Kiểm tra "con đường không hạnh phúc", điều kiện biên, ngoại lệ và trường hợp góc.
Điều này là do nhiệm vụ của QA là giúp suy nghĩ về những gì có thể xảy ra sai.
Tuân theo nguyên tắc “độ chính xác trễ”, các bài kiểm tra chấp nhận phải được viết là
trễ nhất có thể, thường là vài ngày trước khi tính năng này được triển khai. Nhanh nhẹn
các dự án, các bài kiểm tra được viết sau khi các tính năng đã được chọn cho phần tiếp theo
Lặp lại hoặc Sprint.

Một vài thử nghiệm chấp nhận đầu tiên sẽ sẵn sàng vào ngày đầu tiên của lần lặp lại.
Mỗi ngày phải hoàn thành nhiều việc khác cho đến điểm giữa của lần lặp khi tất cả
trong số họ đã sẵn sàng. Nếu tất cả các bài kiểm tra chấp nhận chưa sẵn sàng vào thời điểm giữa của
sự lặp lại, sau đó một số nhà phát triển sẽ phải tham gia để hoàn thành chúng. Nếu điều này
thường xuyên xảy ra, khi đó cần thêm nhiều BA và / hoặc QA vào nhóm.
### T H E D E V E L O P E R ’S R O L E
Công việc triển khai trên một tính năng bắt đầu khi kiểm tra chấp nhận cho tính năng đó
tính năng đã sẵn sàng. Các nhà phát triển thực hiện các bài kiểm tra chấp nhận cho
và xem chúng thất bại như thế nào. Sau đó, họ làm việc để kết nối kiểm tra chấp nhận với
hệ thống, và sau đó bắt đầu vượt qua thử nghiệm bằng cách triển khai
đặc tính.
Paula: "Peter, bạn có thể giúp tôi một tay với câu chuyện này không?"
Peter: "Chắc chắn rồi, Paula, có chuyện gì vậy?"
Paula: “Đây là bài kiểm tra chấp nhận. Như bạn có thể thấy, nó đang thất bại. "
đã đưa ra lệnh LogFileDirectoryStartupCommand
cho rằng thư mục old_inactive_logs không tồn tại
khi lệnh được thực hiện
thì thư mục old_inactive_logs sẽ tồn tại
và nó phải trống
Peter: “Ừ, toàn màu đỏ. Không có kịch bản nào được viết. Hãy để tôi viết
đầu tiên."
| kịch bản | đã cho lệnh _ | cmd |
| tạo lệnh | @cmd |
Paula: "Chúng ta đã có hoạt động createCommand chưa?"
Peter: “Đúng vậy, nó nằm trong CommandUtilitiesFixture mà tôi đã viết tuần trước.”
Paula: “OK, vậy chúng ta hãy chạy thử nghiệm ngay bây giờ.”
Peter: (chạy thử). “Vâng, dòng đầu tiên có màu xanh lục, hãy chuyển sang dòng tiếp theo.”
Đừng lo lắng quá nhiều về Kịch bản và Đồ đạc. Đó chỉ là một số
đường ống dẫn nước bạn phải viết để kết nối các bài kiểm tra với hệ thống là teste
Đủ để nói rằng tất cả các công cụ đều cung cấp một số cách để sử dụng đối sánh mẫu để
nhận ra và phân tích cú pháp các câu lệnh của bài kiểm tra, sau đó gọi các hàm
cung cấp dữ liệu trong thử nghiệm vào hệ thống đang được thử nghiệm. Số lượng nỗ lực là
nhỏ, và các Kịch bản và Đồ đạc có thể sử dụng lại trong nhiều thử nghiệm khác nhau.
Mục đích của tất cả những điều này là nhiệm vụ của nhà phát triển là kết nối sự chấp nhận
kiểm tra hệ thống, và sau đó vượt qua các kiểm tra đó.
### T E S T N E G O T I AT I O N
### VÀ
### P A S S I V E A G G R E S I O N
Tác giả thử nghiệm là con người và mắc sai lầm. Đôi khi các bài kiểm tra như được viết không
rất có ý nghĩa khi bạn bắt đầu thực hiện chúng. Họ cũng có thể
phức tạp. Họ có thể khó xử. Chúng có thể chứa những giả định ngớ ngẩn.
Hoặc họ có thể sai. Điều này có thể rất khó chịu nếu bạn là
nhà phát triển phải vượt qua bài kiểm tra.
Là một nhà phát triển chuyên nghiệp, nhiệm vụ của bạn là thương lượng với tác giả thử nghiệm để có
kiểm tra tốt hơn. Điều bạn không bao giờ nên làm là chọn phương án tích cực thụ động và
tự nói với chính mình, "Chà, đó là những gì bài kiểm tra nói, vì vậy đó là những gì tôi sẽ làm."
Hãy nhớ rằng, là một chuyên gia, nhiệm vụ của bạn là giúp nhóm của bạn tạo ra những điều tốt nhất
phần mềm họ có thể. Điều đó có nghĩa là mọi người cần phải đề phòng các lỗi và
và làm việc cùng nhau để sửa chúng.
Paula: “Tom, bài kiểm tra này không đúng lắm.”
đảm bảo rằng hoạt động đăng kết thúc sau 2 giây.
Tom: “Với tôi thì có vẻ ổn. Yêu cầu của chúng tôi là người dùng không nên có
chờ hơn hai giây. Vấn đề là gì? ”
Paula: “Vấn đề là chúng tôi chỉ có thể đảm bảo điều đó trong một thống kê
giác quan."
Tom: “Hả? Điều đó nghe giống như lời chồn. Yêu cầu là hai
giây. ”
Paula: "Đúng vậy, và chúng tôi có thể đạt được 99,5% thời gian đó."
Tom: "Paula, đó không phải là yêu cầu."
Paula: “Nhưng đó là thực tế. Tôi không thể đảm bảo bằng bất kỳ cách nào khác ”.

Tom: “Sam sắp phát tài.”
Paula: “Không, thực ra, tôi đã nói chuyện với anh ấy về điều đó. Anh ấy ổn miễn là
như trải nghiệm người dùng bình thường là hai giây hoặc ít hơn. "
Tom: “OK, vậy tôi viết bài kiểm tra này như thế nào? Tôi không thể chỉ nói rằng bài đăng
hoạt động thường kết thúc sau hai giây. ”
Paula: "Bạn nói nó theo thống kê."
Tom: “Ý bạn là bạn muốn tôi chạy một nghìn bài đăng và tạo
chắc chắn không quá năm là hơn hai giây? Đó là vô lý."
Paula: “Không, tốt hơn là mất một giờ để chạy. Làm thế nào về
điều này?"
thực hiện 15 giao dịch sau và cộng dồn số lần.
đảm bảo rằng điểm Z trong 2 giây ít nhất là 2,57
Tom: "Chà, điểm Z là bao nhiêu?"
Paula: “Chỉ là một chút thống kê. Đây, thế này thì sao? ”
thực hiện 15 giao dịch sau và cộng dồn số lần.
đảm bảo tỷ lệ cược là 99,5% mà thời gian sẽ ít hơn 2 giây.
Tom: “Vâng, điều đó có thể đọc được, đại loại, nhưng tôi có thể tin tưởng vào toán học đằng sau
cảnh? ”
Paula: “Tôi sẽ đảm bảo hiển thị tất cả các phép tính trung gian trong bài kiểm tra
báo cáo để bạn có thể kiểm tra toán nếu bạn có bất kỳ nghi ngờ nào. ”
Tom: "OK, điều đó phù hợp với tôi."
### A C C E P TA N C E T E S T S
### VÀ
### U N I T T E S T S
Các bài kiểm tra chấp nhận không phải là bài kiểm tra đơn vị. Các bài kiểm tra đơn vị được viết bởi các lập trình viên cho
lập trình viên. Chúng là các tài liệu thiết kế chính thức mô tả mức thấp nhất
cấu trúc và hành vi của mã. Đối tượng là các lập trình viên, không phải doanh nghiệp.
Các bài kiểm tra chấp nhận được doanh nghiệp viết cho doanh nghiệp (ngay cả khi bạn,
nhà phát triển, hãy viết chúng). Chúng là các tài liệu yêu cầu chính thức
chỉ định cách hệ thống sẽ hoạt động theo quan điểm của doanh nghiệp. Các
khán giả là doanh nghiệp và các lập trình viên.

Có thể bị cám dỗ khi cố gắng loại bỏ “việc làm thêm” bằng cách giả định rằng hai
các loại thử nghiệm là dư thừa. Mặc dù đúng là đơn vị và nghiệm thu
thường thử nghiệm những thứ giống nhau, chúng không thừa chút nào.
Đầu tiên, mặc dù họ có thể kiểm tra những thứ giống nhau, nhưng họ làm như vậy thông qua các
cơ chế và con đường. Bài kiểm tra đơn vị đào sâu vào ruột của hệ thống tạo ra
lời gọi đến các phương thức trong các lớp cụ thể. Kiểm tra chấp nhận gọi hệ thống nhiều
xa hơn, ở cấp API hoặc đôi khi thậm chí là cấp độ giao diện người dùng. Vì vậy, các con đường thực thi
mà các bài kiểm tra này thực hiện rất khác nhau.
Nhưng lý do thực sự mà các thử nghiệm này không thừa là vì chức năng chính của chúng là
không thử nghiệm. Thực tế là chúng là thử nghiệm là ngẫu nhiên. Kiểm tra đơn vị và nghiệm thu
kiểm tra là tài liệu đầu tiên và kiểm tra thứ hai. Mục đích chính của họ là chính thức
ghi lại thiết kế, cấu trúc và hành vi của hệ thống. Thực tế là họ
tự động xác minh thiết kế, cấu trúc và hành vi mà chúng chỉ định là
cực kỳ hữu ích, nhưng đặc điểm kỹ thuật là mục đích thực sự của chúng.
### GUI S
### VÀ
### O T H E R C O M P L I C AT I O N S
Thật khó để chỉ định GUI từ trước. Nó có thể được thực hiện, nhưng nó hiếm khi được thực hiện tốt. Các
lý do là tính thẩm mỹ là chủ quan và do đó dễ thay đổi. Mọi người muốn
nghịch ngợm với GUI. Họ muốn xoa bóp và thao túng chúng. Họ muốn thử
phông chữ, màu sắc, bố cục trang và quy trình làm việc khác nhau. GUI liên tục thay đổi.
Điều này làm cho việc viết các thử nghiệm chấp nhận cho GUI trở nên khó khăn. Bí quyết là
thiết kế hệ thống để bạn có thể coi GUI như thể nó là một API
hơn một tập hợp các nút, thanh trượt, lưới và menu. Điều này nghe có vẻ lạ, nhưng nó là
thực sự chỉ là thiết kế tốt.
Có một nguyên tắc thiết kế được gọi là Nguyên tắc Trách nhiệm Đơn lẻ (SRP). Điều này
nguyên tắc nói rằng bạn nên tách những thứ thay đổi để thay đổi
và nhóm lại những thứ thay đổi vì cùng một lý do.
GUI cũng không ngoại lệ.
Bố cục, định dạng và quy trình làm việc của GUI sẽ thay đổi theo thẩm mỹ và
lý do hiệu quả, nhưng khả năng cơ bản của GUI sẽ vẫn như cũ

bất chấp những thay đổi này. Do đó, khi viết các bài kiểm tra chấp nhận cho một GUI, bạn
tận dụng các yếu tố cơ bản không thay đổi thường xuyên.
Ví dụ, có thể có một số nút trên một trang. Thay vì tạo thử nghiệm
nhấp vào các nút đó dựa trên vị trí của chúng trên trang, bạn có thể
có thể nhấp vào chúng dựa trên tên của chúng. Tốt hơn, có lẽ mỗi người đều có
một ID duy nhất mà bạn có thể sử dụng. Sẽ tốt hơn nhiều nếu viết một bài kiểm tra chọn
nút có ID ok_button hơn nó để chọn nút trong cột 3 của hàng
4 của lưới điều khiển.

### Testing through the Right Interface
Vẫn tốt hơn là viết các bài kiểm tra gọi các tính năng của hệ thống cơ bản
thông qua một API thực thay vì thông qua GUI. API này phải giống nhau
API được GUI sử dụng. Điều này không có gì mới. Các chuyên gia thiết kế đã nói với chúng tôi
trong nhiều thập kỷ để tách GUI ra khỏi các quy tắc kinh doanh của chúng tôi.
Kiểm tra thông qua GUI luôn có vấn đề trừ khi bạn chỉ kiểm tra
GUI. Nguyên nhân là do GUI có thể sẽ thay đổi, khiến các bài kiểm tra rất mong manh.
Khi mỗi thay đổi GUI phá vỡ một nghìn lần kiểm tra, bạn sẽ bắt đầu
vứt bỏ các bài kiểm tra hoặc bạn sẽ ngừng thay đổi GUI. Không phải của
đó là những lựa chọn tốt. Vì vậy, hãy viết các bài kiểm tra quy tắc kinh doanh của bạn để thông qua một API
ngay bên dưới GUI.
Một số thử nghiệm chấp nhận chỉ định hành vi của chính GUI. Các bài kiểm tra này phải đi
thông qua GUI. Tuy nhiên, các thử nghiệm này không kiểm tra các quy tắc kinh doanh và do đó
không yêu cầu các quy tắc kinh doanh phải được kết nối với GUI. Do đó, nó là một
ý tưởng hay để tách GUI và các quy tắc kinh doanh và thay thế công việc kinh doanh
các quy tắc có sơ khai trong khi thử nghiệm chính GUI.
Giữ các thử nghiệm GUI ở mức tối thiểu. Chúng rất mỏng manh, bởi vì GUI dễ bay hơi.
Bạn càng có nhiều thử nghiệm GUI thì khả năng bạn giữ chúng càng ít.

## C O N T I N U O U S I N T E G R AT I O N 
Đảm bảo rằng tất cả các bài kiểm tra đơn vị và kiểm tra chấp nhận của bạn được chạy nhiều lần mỗi
ngày trong một hệ thống tích hợp liên tục. Hệ thống này phải được kích hoạt bởi

hệ thống điều khiển mã nguồn. Mỗi khi ai đó thực hiện một mô-đun, CI
hệ thống sẽ bắt đầu một bản dựng, và sau đó chạy tất cả các bài kiểm tra trong hệ thống. Các
kết quả của lần chạy đó phải được gửi qua email cho mọi người trong nhóm.
Dừng máy ép
Điều rất quan trọng là phải giữ cho các bài kiểm tra CI chạy mọi lúc. Họ không bao giờ nên
Thất bại. Nếu họ thất bại, thì cả nhóm nên dừng việc họ đang làm và tập trung
về việc vượt qua các bài kiểm tra bị hỏng một lần nữa. Một bản dựng bị hỏng trong hệ thống CI
nên được xem như một trường hợp khẩn cấp, một sự kiện “ngừng ép”.
Tôi đã tham khảo ý kiến ​​cho các đội không thực hiện nghiêm túc các bài kiểm tra hỏng. Họ đã
"Quá bận" để sửa các bài kiểm tra bị hỏng nên họ đặt chúng sang một bên, hứa sẽ sửa chúng
một lát sau. Trong một trường hợp, nhóm thực sự đã thực hiện các thử nghiệm hỏng ra khỏi bản dựng vì
thật bất tiện khi thấy chúng thất bại. Sau đó, sau khi phát hành cho khách hàng,
họ nhận ra rằng họ đã quên đưa những thử nghiệm đó trở lại bản dựng. Họ
biết được điều này bởi vì một khách hàng giận dữ đã gọi cho họ với các báo cáo lỗi.
## PHẦN KẾT LUẬN
Giao tiếp về chi tiết là khó. Điều này đặc biệt đúng đối với các lập trình viên
và các bên liên quan trao đổi về chi tiết của một ứng dụng. Nó thật quá
dễ dàng để mỗi bên vẫy tay và cho rằng bên kia
hiểu. Thông thường, cả hai bên đều đồng ý rằng họ hiểu và rời đi
với những ý tưởng hoàn toàn khác.
Cách duy nhất tôi biết để loại bỏ hiệu quả các lỗi giao tiếp giữa
lập trình viên và các bên liên quan là viết các bài kiểm tra chấp nhận tự động. Những
các bài kiểm tra chính thức đến mức chúng thực thi. Chúng hoàn toàn không rõ ràng và
chúng không thể thoát ra khỏi sự đồng bộ với ứng dụng. Họ là hoàn hảo
tài liệu yêu cầu.

