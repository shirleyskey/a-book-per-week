# Chapter 12: Collabration 
Hầu hết phần mềm được tạo ra bởi các nhóm. Nhóm hoạt động hiệu quả nhất khi nhóm
các thành viên cộng tác một cách chuyên nghiệp. Thật không chuyên nghiệp khi trở thành một người cô đơn hoặc
ẩn dật trong một đội.
Năm 1974, tôi 22 tuổi. Cuộc hôn nhân của tôi với người vợ tuyệt vời của tôi, Ann Marie, chỉ mới sáu tuổi
vài tháng tuổi. Ngày sinh đứa con đầu lòng của tôi, Angela, vẫn còn một năm nữa. Và tôi
làm việc tại một bộ phận của Teradyne được gọi là Chicago Laser Systems.
157C CHƯƠNG 12
C OLL ABOR ATION
Làm việc bên cạnh tôi là người bạn thời trung học của tôi, Tim Conrad. Tim và tôi đã có
đã làm việc khá nhiều phép lạ trong thời đại của chúng ta. Chúng tôi đã cùng nhau xây dựng máy tính trong
tầng hầm. Chúng tôi đã xây dựng những chiếc thang của Jacob ở của tôi. Chúng tôi đã dạy nhau cách
lập trình PDP-8 và cách đấu dây các mạch tích hợp và bóng bán dẫn vào
máy tính hoạt động.
Chúng tôi là những lập trình viên làm việc trên một hệ thống sử dụng tia laser để cắt điện tử
các linh kiện như điện trở và tụ điện với độ chính xác cực cao. Đối với
ví dụ, chúng tôi đã cắt tinh thể cho chiếc đồng hồ kỹ thuật số đầu tiên, Motorola Pulsar.
Máy tính chúng tôi lập trình là bản sao M365, PDP-8 của Teradyne. Chúng tôi
được viết bằng hợp ngữ và các tệp nguồn của chúng tôi được lưu trên băng từ
hộp mực. Mặc dù chúng tôi có thể chỉnh sửa trên màn hình, nhưng quá trình này khá liên quan,
vì vậy chúng tôi đã sử dụng danh sách in cho hầu hết việc đọc mã và sơ bộ
chỉnh sửa.
Chúng tôi không có cơ sở nào để tìm kiếm cơ sở mã. Không có cách nào để tìm
tất cả những nơi mà một hàm đã cho đã được gọi hoặc một hằng số đã cho là
đã sử dụng. Như bạn có thể tưởng tượng, đây là một trở ngại khá lớn.
Vì vậy, một ngày Tim và tôi quyết định chúng tôi sẽ viết một trình tạo tham chiếu chéo. Điều này
chương trình sẽ đọc trong các băng nguồn của chúng tôi và in ra danh sách mọi ký hiệu,
cùng với tệp và số dòng nơi ký hiệu đó đã được sử dụng.
Chương trình ban đầu khá đơn giản để viết. Nó chỉ đơn giản là đọc trong băng nguồn,
đã phân tích cú pháp trình hợp dịch, tạo một bảng ký hiệu và thêm các tham chiếu vào
mục. Nó hoạt động tốt, nhưng nó chậm kinh khủng. Phải mất hơn một giờ để xử lý
Chương trình Điều hành Chính của chúng tôi (MOP).
Lý do nó quá chậm là do chúng tôi đang giữ bảng biểu tượng ngày càng tăng trong
một bộ nhớ đệm duy nhất. Bất cứ khi nào chúng tôi tìm thấy một tham chiếu mới, chúng tôi sẽ chèn nó vào
bộ đệm, di chuyển phần còn lại của bộ đệm xuống một vài byte để nhường chỗ.
Tim và tôi không phải là chuyên gia về cấu trúc dữ liệu và thuật toán. Chúng tôi chưa bao giờ nghe thấy
bảng băm hoặc tìm kiếm nhị phân. Chúng tôi không có manh mối nào về cách tạo một thuật toán
Nhanh. Chúng tôi chỉ biết rằng những gì chúng tôi đang làm là quá chậm.
158P ROGR AM MER S
ĐẤU VỚI
MỌI NGƯỜI
Vì vậy, chúng tôi đã thử hết thứ này đến thứ khác. Chúng tôi đã thử đưa các tham chiếu vào liên kết
danh sách. Chúng tôi đã cố gắng để lại khoảng trống trong mảng và chỉ tăng bộ đệm khi
những khoảng trống được lấp đầy. Chúng tôi đã thử tạo danh sách các khoảng trống được liên kết. Chúng tôi đã thử tất cả các loại ý tưởng điên rồ.
Chúng tôi đứng trên bảng trắng trong văn phòng và vẽ sơ đồ dữ liệu của chúng tôi
cấu trúc và các phép tính đã thực hiện để dự đoán hiệu suất. Chúng tôi sẽ đến
văn phòng mỗi ngày với một ý tưởng mới. Chúng tôi đã hợp tác như những con quái vật.
Một số điều chúng tôi đã thử giúp tăng hiệu suất. Một số làm chậm nó. Nó
đang bực bội. Đây là lần đầu tiên tôi phát hiện ra việc tối ưu hóa khó khăn như thế nào
phần mềm và quy trình không trực quan như thế nào.
Cuối cùng, chúng tôi đã giảm thời gian xuống dưới 15 phút, rất gần với
mất bao lâu đơn giản để đọc băng nguồn. Vì vậy, chúng tôi đã hài lòng.

## P ROGR AMMERS VERSUS P EOPLE
Chúng tôi không trở thành lập trình viên vì chúng tôi muốn làm việc với mọi người. Như một quy luật
chúng ta thấy mối quan hệ giữa các cá nhân lộn xộn và khó đoán. Chúng tôi thích sạch sẽ
và hành vi có thể dự đoán được của các máy mà chúng tôi lập trình. Chúng tôi hạnh phúc nhất
khi chúng ta ở một mình trong phòng hàng giờ tập trung sâu vào một số
vấn đề thú vị.
OK, đó là một sự tổng quát hóa quá lớn và có vô số trường hợp ngoại lệ. Có
rất nhiều lập trình viên giỏi làm việc với mọi người và tận hưởng
thử thách. Nhưng điểm trung bình của nhóm vẫn có xu hướng theo hướng tôi đã nêu. Chúng tôi,
lập trình viên, tận hưởng cảm giác thiếu hụt nhẹ nhàng và đắm chìm trong kén
tiêu điểm.
### P ROGR AMMERS VERSUS E M P L OY E R S
Vào những năm 70 và 80, khi đang làm việc như một lập trình viên tại Teradyne, tôi
đã học cách gỡ lỗi thực sự giỏi. Tôi thích thử thách và sẽ ném
bản thân tôi trước những vấn đề với sự mạnh mẽ và nhiệt tình. Không có lỗi nào có thể ẩn nấp lâu
từ tôi!
159C CHƯƠNG 12
C OLL ABOR ATION
Khi tôi giải quyết được một lỗi, nó giống như chiến thắng hoặc giết chết Jabberwock!
Tôi sẽ đến gặp ông chủ của tôi, Ken Finder, trong tay thanh kiếm Vorpal, và một cách say mê
mô tả cho anh ta thấy lỗi thú vị như thế nào. Một ngày cuối cùng Ken cũng bùng nổ
thất vọng: “Lỗi không thú vị. Các lỗi chỉ cần được sửa chữa! ”
Tôi đã học được điều gì đó vào ngày hôm đó. Thật tốt khi đam mê những gì chúng ta làm. Nhưng
bạn cũng nên theo dõi mục tiêu của những người trả tiền cho bạn.
Trách nhiệm đầu tiên của lập trình viên chuyên nghiệp là đáp ứng nhu cầu của
chủ nhân của mình. Điều đó có nghĩa là cộng tác với người quản lý, doanh nghiệp của bạn
nhà phân tích, người kiểm tra và các thành viên khác trong nhóm để hiểu sâu sắc về doanh nghiệp
bàn thắng. Điều này không có nghĩa là bạn phải trở thành một người kinh doanh giỏi. Nó có nghĩa là
bạn cần hiểu lý do tại sao bạn viết mã bạn đang viết và làm thế nào
doanh nghiệp sử dụng bạn sẽ được hưởng lợi từ nó.
Điều tồi tệ nhất mà một lập trình viên chuyên nghiệp có thể làm là tự chôn vùi bản thân một cách hạnh phúc
trong một ngôi mộ công nghệ trong khi công việc kinh doanh sụp đổ và bùng cháy xung quanh anh ta. Của bạn
công việc là giữ cho doanh nghiệp phát triển!
Vì vậy, các lập trình viên chuyên nghiệp hãy dành thời gian để hiểu doanh nghiệp. Họ
trao đổi với người dùng về phần mềm họ đang sử dụng. Họ nói chuyện với bán hàng và tiếp thị
mọi người về các vấn đề và vấn đề mà họ có. Họ nói chuyện với người quản lý của họ để
hiểu các mục tiêu ngắn hạn và dài hạn của nhóm.
Tóm lại, họ chú ý đến con tàu mà họ đang chèo.
Lần duy nhất tôi bị sa thải khỏi công việc lập trình là vào năm 1976. Tôi đang làm việc
cho Outboard Marine Corp vào thời điểm đó. Tôi đã giúp viết một nhà máy
hệ thống tự động hóa sử dụng Hệ thống IBM / 7s để giám sát hàng chục nhôm
máy đúc trên sàn cửa hàng.
Về mặt kỹ thuật, đây là một công việc đầy thử thách và bổ ích. Kiến trúc của
System / 7 thật hấp dẫn và bản thân hệ thống tự động hóa của nhà máy đã thực sự
hấp dẫn.
Chúng tôi cũng có một đội tốt. Trưởng nhóm, John, là người có năng lực và động lực.
Hai đồng đội lập trình của tôi rất vui vẻ và hữu ích. Chúng tôi đã có một phòng thí nghiệm
160P ROGR AM MER S
ĐẤU VỚI
MỌI NGƯỜI
dành riêng cho dự án của chúng tôi và tất cả chúng tôi đã làm việc trong phòng thí nghiệm đó. Đối tác kinh doanh
đã tham gia và trong phòng thí nghiệm với chúng tôi. Quản lý của chúng tôi, Ralph, là người có năng lực,
tập trung và phụ trách.
Mọi thứ lẽ ra phải tuyệt vời. Vấn đề là tôi. Tôi đã nhiệt tình
đủ về dự án và về công nghệ, nhưng ở độ tuổi lớn của
24 Tôi chỉ đơn giản là không thể quan tâm đến công việc kinh doanh hoặc về nó
cơ cấu chính trị nội bộ.
Sai lầm đầu tiên của tôi là vào ngày đầu tiên của tôi. Tôi xuất hiện mà không đeo cà vạt. Tôi đã có
đã đeo một chiếc trong cuộc phỏng vấn của tôi và tôi đã thấy rằng những người khác đều đeo cà vạt, nhưng tôi
không kết nối được. Vì vậy, vào ngày đầu tiên của tôi, Ralph đã đến với tôi và rõ ràng là
nói, "Chúng tôi đeo cà vạt ở đây."
Tôi không thể nói với bạn rằng tôi đã phẫn nộ như thế nào. Nó làm phiền tôi ở một mức độ sâu sắc. Tôi đã mặc
cà vạt hàng ngày, và tôi ghét nó. Nhưng tại sao? Tôi biết những gì tôi đang tham gia. tôi biết
các quy ước mà họ đã thông qua. Tại sao tôi lại khó chịu như vậy? Bởi vì tôi là một
đôi chút ích kỷ, tự ái.
Tôi chỉ đơn giản là không thể đi làm đúng giờ. Và tôi nghĩ nó không quan trọng. Rốt cuộc,
Tôi đã làm "một công việc tốt." Và đó là sự thật, tôi đã viết rất tốt
các chương trình của tôi. Tôi dễ dàng trở thành lập trình viên kỹ thuật giỏi nhất trong nhóm. Tôi có thể
viết mã nhanh hơn và tốt hơn những cái khác. Tôi có thể chẩn đoán và giải quyết
vấn đề nhanh hơn. Tôi biết tôi có giá trị. Vì vậy ngày giờ không quan trọng lắm
với tôi.
Quyết định sa thải tôi được đưa ra vào một ngày khi tôi không có mặt đúng giờ cho một
cột mốc. Rõ ràng John đã nói với tất cả chúng tôi rằng anh ấy muốn có một bản demo làm việc
các tính năng vào thứ Hai tới. Tôi chắc chắn rằng tôi biết về điều này, nhưng ngày và giờ chỉ đơn giản là
không quan trọng đối với tôi.
Chúng tôi đang phát triển tích cực. Hệ thống không được sản xuất. Có
không có lý do gì để hệ thống chạy khi không có ai trong phòng thí nghiệm. tôi phải có
là người cuối cùng rời khỏi thứ sáu đó và dường như tôi đã rời khỏi hệ thống trong một
trạng thái không hoạt động. Thực tế là thứ Hai quan trọng đơn giản là không
mắc kẹt trong não của tôi.
Chương 161: Chương 12
C OLL ABOR ATION
Tôi đến muộn một giờ vào thứ Hai hôm đó và thấy mọi người tụ tập vui vẻ xung quanh
một hệ thống không hoạt động. John hỏi tôi, "Tại sao hệ thống không hoạt động
hôm nay, Bob? ” Câu trả lời của tôi: "Tôi không biết." Và tôi đã ngồi gỡ lỗi nó. tôi đã
vẫn không biết gì về bản demo thứ Hai, nhưng tôi có thể biết được bằng cơ thể của những người khác
ngôn ngữ mà có gì đó sai. Sau đó John đến và thì thầm
vào tai tôi, "Điều gì sẽ xảy ra nếu Stenberg quyết định đến thăm?" Sau đó, anh ấy đi vào
ghê tởm.
Stenberg là Phó chủ tịch phụ trách tự động hóa. Ngày nay, chúng tôi gọi anh ấy là CIO.
Câu hỏi không có ý nghĩa gì đối với tôi. "Vậy thì sao?" Tôi đã nghĩ. “Hệ thống không
trong sản xuất, vấn đề lớn là gì? ”
Tôi nhận được lá thư cảnh báo đầu tiên của mình vào cuối ngày hôm đó. Nó nói với tôi rằng tôi phải thay đổi
tại


titude ngay lập tức hoặc "kết thúc nhanh chóng sẽ là kết quả." tôi đã
kinh hoàng!
Tôi đã mất một thời gian để phân tích hành vi của mình và bắt đầu nhận ra những gì tôi đã
làm sai. Tôi đã nói chuyện với John và Ralph về nó. Tôi quyết tâm rẽ
bản thân tôi và công việc của tôi xung quanh.
Và tôi đã! Tôi không đến muộn nữa. Tôi bắt đầu chú ý đến nội bộ
chính trị. Tôi bắt đầu hiểu tại sao John lại lo lắng cho Stenberg. Tôi đã bắt đầu
để xem tình huống tồi tệ mà tôi đã đưa anh ta vào khi hệ thống đó không hoạt động
Thứ Hai.
Nhưng đó là quá ít, quá muộn. Cái chết đã được đúc. Tôi nhận được một lá thư cảnh báo thứ hai a
tháng sau vì một lỗi nhỏ mà tôi đã mắc phải. Tôi nên nhận ra vào thời điểm đó
rằng các bức thư là một hình thức và quyết định chấm dứt hợp đồng với tôi
đã được thực hiện. Nhưng tôi đã quyết tâm giải cứu tình hình. Vì vậy, tôi đã làm việc
thậm chí khó khăn hơn.
Cuộc họp chấm dứt diễn ra sau đó vài tuần.
Hôm đó tôi về nhà với người vợ 22 tuổi đang mang thai của mình và phải nói với cô ấy rằng
Tôi đã bị sa thải. Đó không phải là trải nghiệm mà tôi muốn lặp lại.

### P ROGR AMMERS VERSUSVER SUSP EOPLEP ROGR AMMERS
Các lập trình viên thường gặp khó khăn khi làm việc chặt chẽ với các lập trình viên khác.
Điều này dẫn đến một số vấn đề thực sự khủng khiếp.

#### Owned Code
Một trong những triệu chứng tồi tệ nhất của một nhóm rối loạn chức năng là khi mỗi lập trình viên
xây dựng một bức tường xung quanh mã của mình và từ chối để các lập trình viên khác chạm vào nó.
Tôi đã đến những nơi mà các lập trình viên thậm chí không cho phép
lập trình viên xem mã của họ. Đây là một công thức cho thảm họa.
Tôi từng tư vấn cho một công ty chế tạo máy in cao cấp. Những máy này
có nhiều thành phần khác nhau như bộ nạp, máy in, bộ xếp chồng, kim bấm,
máy cắt, v.v. Doanh nghiệp đánh giá mỗi thiết bị này khác nhau. Người cho ăn
quan trọng hơn ngăn xếp và không có gì quan trọng hơn
máy in.
Mỗi lập trình viên đã làm việc trên thiết bị của mình. Một anh chàng sẽ viết mã cho
feeder, một người khác sẽ viết mã cho kim bấm. Mỗi người trong số họ giữ
công nghệ cho chính họ và ngăn không cho bất kỳ ai khác chạm vào mã của họ.
Ảnh hưởng chính trị mà những lập trình viên này sử dụng có liên quan trực tiếp đến cách
nhiều doanh nghiệp đánh giá cao thiết bị. Lập trình viên đã làm việc trên
máy in không khả dụng.
Đây là một thảm họa cho công nghệ. Với tư cách là một nhà tư vấn, tôi có thể thấy rằng ở đó
là sự trùng lặp lớn trong mã và giao diện giữa các mô-đun
đã bị lệch hoàn toàn. Nhưng không có lý lẽ nào về phía tôi có thể thuyết phục
các lập trình viên (hoặc doanh nghiệp) để thay đổi cách thức của họ. Rốt cuộc, lương của họ
đánh giá gắn liền với tầm quan trọng của các thiết bị mà họ duy trì
#### Collective Ownership
Tốt hơn là phá bỏ tất cả các bức tường về quyền sở hữu mã và có nhóm của riêng mình
tất cả các mã. Tôi thích các đội trong đó bất kỳ thành viên nào trong nhóm có thể kiểm tra bất kỳ
và thực hiện bất kỳ thay đổi nào mà họ cho là phù hợp. Tôi muốn đội
sở hữu mã, không phải cá nhân.
163C HÀM 12
C OLL ABOR ATION
Các nhà phát triển chuyên nghiệp không ngăn cản người khác làm việc trong mã. Họ
không xây tường sở hữu xung quanh mã. Đúng hơn, chúng làm việc với nhau
trên nhiều hệ thống nhất có thể. Họ học hỏi lẫn nhau bằng cách làm việc
với nhau trên các phần khác của hệ thống.
#### Pairing
Nhiều lập trình viên không thích ý tưởng lập trình cặp. Tôi thấy điều này kỳ lạ
vì hầu hết các lập trình viên sẽ ghép nối trong những trường hợp khẩn cấp. Tại sao? Bởi vì nó rõ ràng là
cách hiệu quả nhất để giải quyết vấn đề. Nó chỉ quay trở lại câu ngạn ngữ cũ:
Hai cái đầu tốt hơn một cái. Nhưng nếu ghép nối là cách hiệu quả nhất để giải quyết
một vấn đề trong trường hợp khẩn cấp, tại sao đó không phải là cách hiệu quả nhất để giải quyết
giai đoạn vấn đề?
Tôi sẽ không trích dẫn các nghiên cứu về bạn, mặc dù có một số có thể
trích dẫn. Tôi sẽ không kể cho bạn nghe bất kỳ giai thoại nào, mặc dù tôi có thể
nói. Tôi thậm chí sẽ không cho bạn biết bạn nên ghép nối bao nhiêu. Tất cả những gì tôi sẽ làm
nói với bạn là cặp chuyên gia. Tại sao? Bởi vì đối với một số vấn đề, nó là
cách hiệu quả nhất để giải quyết chúng. Nhưng đó không phải là lý do duy nhất.
Các chuyên gia cũng bắt cặp vì đây là cách tốt nhất để chia sẻ kiến ​​thức với mỗi
khác. Các chuyên gia không tạo ra kho kiến ​​thức. Đúng hơn, họ học những điều khác nhau
các bộ phận của hệ thống và nghiệp vụ bằng cách ghép nối với nhau. Họ nhận ra rằng
mặc dù tất cả các thành viên trong nhóm đều có vị trí để chơi, tất cả các thành viên trong nhóm phải
cũng có thể chơi một vị trí khác trong một chụm.
Các chuyên gia ghép đôi vì đó là cách tốt nhất để xem lại mã. Không có hệ thống nên
bao gồm mã chưa được các lập trình viên khác xem xét. Có
nhiều cách để tiến hành đánh giá mã; hầu hết chúng đều kém hiệu quả một cách kinh khủng.
Cách hiệu quả và hiệu quả nhất để xem lại mã là cộng tác viết mã.

### C EREBELLUMS
Tôi đi tàu đến Chicago vào một buổi sáng năm 2000 trong thời kỳ đỉnh cao của dấu chấm
com bùng nổ. Khi tôi bước xuống tàu xuống sân ga, tôi đã bị tấn công bởi một
bảng quảng cáo khổng lồ treo phía trên cửa thoát hiểm. Dấu hiệu dành cho một người nổi tiếng
164C EREBELLUM S
công ty phần mềm đang tuyển dụng lập trình viên. Nó đọc: Hãy chà xát tiểu não
với điều tốt nhất.
Tôi ngay lập tức bị ấn tượng bởi sự ngu ngốc cấp bậc của một dấu hiệu như thế. Những người nghèo
những người quảng cáo không biết gì đã cố gắng thu hút một kỹ thuật cao, thông minh,
và dân số hiểu biết của các lập trình viên. Đây là những người
đặc biệt đừng chịu đựng sự ngu ngốc. Các nhà quảng cáo đang cố gắng gợi lên
hình ảnh chia sẻ kiến ​​thức với những người thông minh khác. không may
họ đề cập đến một phần của não, tiểu não, liên quan đến cơ tốt
kiểm soát chứ không phải thông minh. Vì vậy, những người mà họ đang cố gắng thu hút đã
chế nhạo một lỗi ngớ ngẩn như vậy.
Nhưng một điều gì đó khác khiến tôi tò mò về dấu hiệu đó. Nó khiến tôi nghĩ về một nhóm
của những người cố gắng xoa bóp tiểu não. Vì tiểu não nằm ở phía sau của
não, cách tốt nhất để cọ xát các tiểu não là quay mặt ra xa nhau. Tôi
tưởng tượng một nhóm lập trình viên ngồi trong các buồng nhỏ, ngồi quay lưng lại với nhau
nhìn nhau, nhìn chằm chằm vào màn hình trong khi đeo tai nghe. Đó là cách bạn cọ xát
tiểu não. Đó cũng không phải là một đội.
Các chuyên gia làm việc cùng nhau. Bạn không thể làm việc cùng nhau khi bạn đang ngồi trong
góc đeo tai nghe. Vì vậy, tôi muốn bạn ngồi quanh bàn đối diện với từng
khác. Tôi muốn các bạn có thể cảm nhận được nỗi sợ hãi của nhau. Tôi muốn bạn có thể
nghe được những lời lẩm bẩm bực bội của ai đó. Tôi muốn giao tiếp tình cờ,
cả ngôn ngữ bằng lời nói và cơ thể. Tôi muốn bạn giao tiếp như một đơn vị.
Có lẽ bạn tin rằng bạn làm việc tốt hơn khi bạn làm việc một mình. Điều đó có thể
là đúng, nhưng không có nghĩa là nhóm hoạt động tốt hơn khi bạn làm việc một mình.
Và trên thực tế, rất khó có khả năng bạn làm việc tốt hơn khi làm việc
một mình.
Có những lúc làm việc một mình là điều nên làm. Có những lúc
khi bạn chỉ cần suy nghĩ lâu và khó về một vấn đề. Có những lúc
khi nhiệm vụ quá tầm thường đến nỗi có một người khác sẽ thật lãng phí
làm việc với các bạn. Tuy nhiên, nói chung, tốt nhất là cộng tác chặt chẽ với những người khác
và để ghép nối với họ một phần lớn thời gian.

## C ONCLUSIO
Có lẽ chúng tôi không thích lập trình để làm việc với mọi người. May mắn cho
chúng ta. Lập trình là tất cả về làm việc với mọi người. Chúng tôi cần làm việc với
và chúng ta cần làm việc với nhau.
Tôi biết rồi mà. Sẽ không tuyệt nếu họ chỉ nhốt chúng ta vào một căn phòng có sáu người
màn hình lớn, ống T3, một dãy song song các bộ xử lý siêu nhanh, không giới hạn
ram và đĩa, và một nguồn cung cấp không bao giờ cạn gồm cola ăn kiêng và khoai tây chiên cay? Chao ôi,
nó không phải là được. Nếu chúng tôi thực sự muốn dành cả ngày để lập trình, chúng tôi sẽ
phải học cách nói chuyện với — mọi người.