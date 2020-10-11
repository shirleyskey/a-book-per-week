# Chapter 08: Strategies Testing 
Các nhà phát triển chuyên nghiệp kiểm tra mã của họ. Nhưng kiểm tra không chỉ đơn giản là vấn đề
viết một vài bài kiểm tra đơn vị hoặc một vài bài kiểm tra chấp nhận. Viết những bài kiểm tra này là một điều tốt
nhưng nó còn lâu mới đủ. Điều mà mọi nhóm phát triển chuyên nghiệp
nhu cầu là một chiến lược kiểm tra tốt.
Năm 1989, tôi đang làm việc tại Rational với bản phát hành đầu tiên của Rose. Hàng tháng hoặc
vì vậy người quản lý QA của chúng tôi sẽ gọi là ngày “Săn lỗi”. Mọi người trong nhóm, từ
lập trình viên cho người quản lý đến thư ký cho người quản trị cơ sở dữ liệu, sẽ ngồi
xuống với Rose và cố gắng làm cho nó thất bại. Giải thưởng được trao cho nhiều loại
lỗi. Người phát hiện ra lỗi có thể giành được một bữa tối cho hai người. Các
người tìm ra nhiều lỗi nhất có thể giành được một kỳ nghỉ cuối tuần ở Monterrey.

## QA S H O U L D F I N D N O T H I N G
Tôi đã nói điều này trước đây và tôi sẽ nói lại lần nữa. Mặc dù thực tế là công ty của bạn
có thể có một nhóm QA riêng để kiểm tra phần mềm, nó phải là mục tiêu của
nhóm phát triển mà QA thấy không có gì sai.
Tất nhiên, không có khả năng mục tiêu này sẽ liên tục đạt được. Rốt cuộc, khi
bạn có một nhóm người thông minh ràng buộc và quyết tâm tìm ra tất cả
các nếp nhăn và thâm hụt trong một sản phẩm, họ có thể sẽ tìm thấy một số. Tuy nhiên, mọi
thời gian QA tìm thấy thứ gì đó mà nhóm phát triển nên phản ứng kinh hoàng. Họ
nên tự hỏi bản thân xem nó đã xảy ra như thế nào và thực hiện các bước để ngăn chặn nó trong tương lai

### QA I s P A R TOF THET E A M
Phần trước có thể cho thấy rằng QA và Phát triển đang ở
mâu thuẫn với nhau, rằng mối quan hệ của họ là đối nghịch. Đây không phải là mục đích.
Thay vào đó, QA và Development nên làm việc cùng nhau để đảm bảo chất lượng
của hệ thống. Vai trò tốt nhất đối với phần QA của nhóm là hoạt động như những người chỉ định
và đặc điểm.


### QA as Specifiers
QA nên làm việc với doanh nghiệp để tạo ra sự chấp nhận tự động
các bài kiểm tra trở thành tài liệu đặc tả và yêu cầu thực sự cho
hệ thống. Lặp đi lặp lại họ thu thập các yêu cầu từ kinh doanh và
chuyển chúng thành các bài kiểm tra mô tả cho các nhà phát triển cách hệ thống nên
hành xử (Xem Chương 7, “Kiểm tra sự chấp nhận”). Nói chung, doanh nghiệp viết
kiểm tra con đường hạnh phúc, trong khi QA viết các thử nghiệm góc, ranh giới và đường dẫn không hạnh phúc.

### QA as Characterizers



## T H E T E S T A U T O M AT I O N P Y R A M I D
Các nhà phát triển chuyên nghiệp sử dụng kỷ luật Phát triển theo hướng kiểm tra
để tạo các bài kiểm tra đơn vị. Các nhóm phát triển chuyên nghiệp sử dụng các bài kiểm tra chấp nhận để
chỉ định hệ thống của họ và tích hợp liên tục (Chương 7, trang 110) để
ngăn chặn sự thoái lui. Nhưng những thử nghiệm này chỉ là một phần của câu chuyện. Tốt như nó là
có một bộ các đơn vị và các bài kiểm tra chấp nhận, chúng tôi cũng cần các bài kiểm tra cấp cao hơn để
đảm bảo rằng QA không tìm thấy gì. Hình 8-1 cho thấy Kim tự tháp tự động hóa thử nghiệm, 2
mô tả đồ họa về các loại bài kiểm tra mà một sự phát triển chuyên nghiệp
nhu cầu của tổ chức.

### U N I T T E S T S
Ở dưới cùng của kim tự tháp là các bài kiểm tra đơn vị. Các bài kiểm tra này được viết bởi
lập trình viên, dành cho người lập trình, bằng ngôn ngữ lập trình của hệ thống.
Mục đích của các thử nghiệm này là chỉ định hệ thống ở mức thấp nhất. Nhà phát triển
viết các bài kiểm tra này trước khi viết mã sản xuất như một cách để chỉ định những gì chúng
sắp viết. Chúng được thực thi như một phần của Tích hợp liên tục để
đảm bảo rằng ý định của các lập trình viên được tuân thủ.
Các bài kiểm tra đơn vị cung cấp mức độ bao phủ gần 100% như thực tế. Nói chung là cái này
số nên ở đâu đó trong những năm 90. Và nó phải là phạm vi thực sự như
đối lập với các thử nghiệm sai thực thi mã mà không xác nhận hành vi của nó.

### C O M P O N E N T T E S T S
Đây là một số thử nghiệm chấp nhận được đề cập trong chương trước.
Nói chung chúng được viết dựa trên các thành phần riêng lẻ của hệ thống. Các
các thành phần của hệ thống đóng gói các quy tắc kinh doanh, vì vậy các bài kiểm tra cho những
các thành phần là các bài kiểm tra chấp nhận cho các quy tắc kinh doanh đó
Như được mô tả trong Hình 8-2, kiểm tra thành phần bao bọc một thành phần. Nó vượt qua đầu vào
dữ liệu vào thành phần và thu thập dữ liệu đầu ra từ nó. Nó kiểm tra rằng
đầu ra khớp với đầu vào. Bất kỳ thành phần hệ thống nào khác được tách ra khỏi
thử nghiệm bằng cách sử dụng các kỹ thuật mô phỏng và nhân đôi thử nghiệm thích hợp.
Hình 8-2 ​​Kiểm tra nghiệm thu thành phần
116
ComponentT HE T EST A UTOMATION P YR AMID
Các bài kiểm tra thành phần được viết bởi QA và Business với sự hỗ trợ từ nhà phát triển-
cố vấn. Chúng được tạo ra trong một môi trường kiểm tra thành phần như FitNesse,
JBehave, hoặc Dưa chuột. (Các thành phần GUI được kiểm tra với môi trường kiểm tra GUI
chẳng hạn như Selenium hoặc Watir.) Mục đích là doanh nghiệp sẽ có thể
để đọc và giải thích các bài kiểm tra này, nếu không phải là tác giả của chúng.
Kiểm tra thành phần bao gồm gần một nửa hệ thống. Họ hướng tới nhiều hơn
tình huống con đường hạnh phúc và góc, ranh giới và con đường thay thế rất rõ ràng
các trường hợp. Phần lớn các trường hợp đường dẫn không vui được bao gồm bởi các bài kiểm tra đơn vị và
vô nghĩa ở cấp độ các bài kiểm tra thành phần.

### I N T E G R AT I O N T E S T S
Các thử nghiệm này chỉ có ý nghĩa đối với các hệ thống lớn hơn có nhiều thành phần.
Như trong Hình 8-3, các thử nghiệm này lắp ráp các nhóm thành phần và kiểm tra
họ giao tiếp với nhau tốt như thế nào. Các thành phần khác của
hệ thống được tách rời như bình thường với các mocks và test-double thích hợp.
Bài kiểm tra tích hợp là bài kiểm tra vũ đạo. Họ không kiểm tra các quy tắc kinh doanh. Hơn,
họ kiểm tra xem việc lắp ráp các thành phần nhảy với nhau tốt như thế nào. họ đang
kiểm tra hệ thống ống nước để đảm bảo rằng các bộ phận được kết nối đúng cách và
rõ ràng có thể giao tiếp với nhau.
Thành phần
Thành phần
Thành phần
Thành phần
Hình 8-3 Kiểm tra tích hợp
117C CHƯƠNG 8
T ESTING S TR ATEGIES
Các bài kiểm tra tích hợp thường được viết bởi kiến ​​trúc sư hệ thống hoặc nhà thiết kế chính,
của hệ thống. Các bài kiểm tra đảm bảo rằng cấu trúc kiến ​​trúc của hệ thống là
âm thanh. Ở cấp độ này, chúng ta có thể thấy các bài kiểm tra hiệu suất và thông lượng.
Các bài kiểm tra tích hợp thường được viết bằng cùng một ngôn ngữ và môi trường
như các bài kiểm tra thành phần. Chúng thường không được thực thi như một phần của
Bộ tích hợp, vì chúng thường có thời gian chạy lâu hơn. Thay vào đó, những thử nghiệm này
được chạy định kỳ (hàng đêm, hàng tuần, v.v.) khi họ cho là cần thiết
các tác giả.

### S Y S T E M T E S T S
Đây là các bài kiểm tra tự động thực thi trên toàn bộ hệ thống tích hợp.
Chúng là những bài kiểm tra tích hợp cuối cùng. Họ không kiểm tra các quy tắc kinh doanh trực tiếp.
Thay vào đó, họ kiểm tra xem hệ thống đã được kết nối với nhau một cách chính xác và các bộ phận của nó
liên thông theo kế hoạch. Chúng tôi mong đợi sẽ thấy thông lượng và
kiểm tra hiệu suất trong bộ phần mềm này.
Các bài kiểm tra này được viết bởi các kiến trúc sư hệ thống và các trưởng nhóm kỹ thuật. Thông thường
chúng được viết bằng ngôn ngữ và môi trường giống như các bài kiểm tra tích hợp cho
giao diện người dùng. Chúng được thực hiện tương đối không thường xuyên tùy thuộc vào thời lượng của chúng,
nhưng càng thường xuyên càng tốt.
Kiểm tra hệ thống có lẽ bao gồm 10% hệ thống. Điều này là do mục đích của họ không
để đảm bảo hành vi của hệ thống chính xác, nhưng xây dựng hệ thống chính xác. Chính xác
hành vi của mã cơ bản và các thành phần đã được xác định chắc chắn
bởi các lớp bên dưới của kim tự tháp.
### M A N U A L E X P L O R AT O R Y T E S T S
Đây là nơi con người đặt tay trên bàn phím và mắt của họ trên
màn hình. Các bài kiểm tra này không tự động, cũng không phải theo kịch bản. Mục đích của những
kiểm tra là để khám phá hệ thống về các hành vi không mong muốn trong khi xác nhận
hành vi cư xử. Để đạt được mục tiêu đó, chúng ta cần bộ não của con người, với sự sáng tạo của con người,
làm việc để điều tra và khám phá hệ thống. Tạo một kế hoạch kiểm tra bằng văn bản cho
loại thử nghiệm này đánh bại mục đích.
118B IBLIOGR THÁNG 4
Một số nhóm sẽ có chuyên gia thực hiện công việc này. Các đội khác sẽ chỉ cần khai báo
ngày hoặc hai ngày "săn lỗi" trong đó càng nhiều người càng tốt, bao gồm
các nhà quản lý, thư ký, lập trình viên, người kiểm tra và người viết công nghệ, hãy "đập" vào
hệ thống để xem liệu họ có thể làm cho nó bị hỏng.
Mục tiêu không phải là phạm vi bảo hiểm. Chúng tôi sẽ không chứng minh mọi quy tắc kinh doanh và
mọi con đường thực thi với các thử nghiệm này. Thay vào đó, mục tiêu là đảm bảo rằng
hệ thống hoạt động tốt dưới sự vận hành của con người và để tìm ra nhiều
"Đặc biệt" càng tốt.


### C ONCLUSION
TDD là một kỷ luật mạnh mẽ và Kiểm tra chấp nhận là những cách có giá trị để thể hiện
và thực thi các yêu cầu. Nhưng chúng chỉ là một phần của chiến lược kiểm tra tổng thể. Đến
thực hiện tốt mục tiêu “QA sẽ không tìm thấy gì”, các nhóm phát triển cần
làm việc song song với QA để tạo ra một hệ thống phân cấp của đơn vị, thành phần,
kiểm tra đo lường, hệ thống và khám phá. Các bài kiểm tra này nên được chạy thường xuyên như
có thể để cung cấp phản hồi tối đa và để đảm bảo rằng hệ thống vẫn
liên tục làm sạch.