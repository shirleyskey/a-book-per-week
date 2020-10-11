# Chapter 10: Estimate 
Ước tính là một trong những hoạt động đơn giản nhưng đáng sợ nhất mà phần mềm
các chuyên gia phải đối mặt. Vì vậy, nhiều giá trị kinh doanh phụ thuộc vào nó. Rất nhiều
danh tiếng đi trên nó. Rất nhiều nỗi lo lắng và thất bại của chúng ta là do nó gây ra. Nó là
kênh chính được thúc đẩy giữa doanh nhân và nhà phát triển.
Nó là nguồn gốc của gần như tất cả sự ngờ vực chi phối mối quan hệ đó.
135C CHƯƠNG 10
ƯỚC LƯỢNG
Năm 1978, tôi là nhà phát triển chính cho chương trình Z-80 nhúng 32K được viết
trong hợp ngữ. Chương trình đã được ghi vào 32 1K ́ 8 EEprom
khoai tây chiên. 32 con chip này được lắp vào ba bảng, mỗi bảng chứa 12
khoai tây chiên.
Chúng tôi đã có hàng trăm thiết bị tại hiện trường, được lắp đặt trong các văn phòng trung tâm điện thoại
trên toàn nước Mỹ. Bất cứ khi nào chúng tôi sửa lỗi hoặc thêm một tính năng, chúng tôi sẽ
phải gửi công nghệ phục vụ hiện trường đến từng đơn vị đó và để chúng thay thế
tất cả 32 chip!
Đây là một cơn ác mộng. Các chip và bảng mỏng manh. Các chân trên
chip có thể bị cong và gãy. Sự uốn cong liên tục của bảng có thể làm hỏng
mối hàn. Nguy cơ vỡ và lỗi là rất lớn. Chi phí cho
công ty quá cao.
Ông chủ của tôi, Ken Finder, đến gặp tôi và yêu cầu tôi sửa lỗi này. Điều anh ấy muốn là
một cách để thực hiện thay đổi đối với một chip mà không yêu cầu tất cả các chip khác
thay đổi. Nếu bạn đã đọc sách của tôi, hoặc nghe những bài nói chuyện của tôi, bạn biết tôi không hiểu nhiều về
khả năng triển khai độc lập. Đây là nơi đầu tiên tôi học được bài học đó.
Vấn đề của chúng tôi là phần mềm là một tệp thực thi được liên kết duy nhất. Nếu một dòng mới
mã đã được thêm vào chương trình, tất cả địa chỉ của các dòng sau
mã đã thay đổi. Vì mỗi chip chỉ giữ 1K không gian địa chỉ nên nội dung
hầu như tất cả các chip sẽ thay đổi.
Giải pháp khá đơn giản. Mỗi chip phải được tách ra khỏi tất cả
khác. Mỗi đơn vị phải được biến thành một đơn vị biên dịch độc lập có thể
được đốt cháy độc lập với tất cả những người khác.
Vì vậy, tôi đã đo kích thước của tất cả các chức năng trong ứng dụng và viết
chương trình đơn giản phù hợp với chúng, như trò chơi ghép hình, vào mỗi con chip,
để lại 100 byte không gian hoặc lâu hơn để mở rộng. Ở đầu mỗi chip
Tôi đặt một bảng con trỏ đến tất cả các chức năng trên con chip đó. Lúc khởi động những
con trỏ đã được chuyển vào RAM. Tất cả mã trong hệ thống đã được thay đổi vì vậy
rằng các chức năng chỉ được gọi thông qua các vectơ RAM này và không bao giờ
trực tiếp.
TIM MẠCH 136E
Vâng, bạn đã hiểu. Những con chip là những đồ vật, với những chiếc bàn. Tất cả các chức năng là đa
mor được triển khai phically. Và, vâng, đây là cách tôi học được một số nguyên tắc của
OOD, rất lâu trước khi tôi biết vật thể là gì.
Những lợi ích là rất lớn. Chúng tôi không chỉ có thể triển khai các chip riêng lẻ, chúng tôi
cũng có thể tạo các bản vá trong lĩnh vực này bằng cách chuyển các chức năng vào RAM và
định tuyến lại các vectơ. Điều này làm cho việc gỡ lỗi trường và vá nóng dễ dàng hơn nhiều.
Nhưng tôi lạc đề. Khi Ken đến gặp tôi và yêu cầu tôi khắc phục sự cố này, anh ấy
đề xuất điều gì đó về con trỏ đến các hàm. Tôi đã dành một hoặc hai ngày
chính thức hóa ý tưởng và sau đó trình bày với anh ta một kế hoạch chi tiết. Anh ấy đã hỏi tôi
nó sẽ mất bao lâu, và tôi trả lời rằng tôi sẽ mất khoảng một tháng.
Phải mất ba tháng.
Tôi chỉ say hai lần trong đời và chỉ thực sự say một lần. Nó đã ở
bữa tiệc Giáng sinh ở Teradyne năm 1978. Tôi 26 tuổi.
Bữa tiệc được tổ chức tại văn phòng Teradyne, nơi chủ yếu là không gian phòng thí nghiệm mở.
Mọi người đều đến đó sớm, và sau đó có một trận bão tuyết lớn ngăn cản
ban nhạc và người phục vụ ăn uống từ đó. May mắn thay, có rất nhiều rượu.
Tôi không nhớ nhiều về đêm đó. Và điều tôi nhớ là tôi ước gì tôi không làm vậy.
Nhưng tôi sẽ chia sẻ một khoảnh khắc sâu sắc với bạn.
Tôi đang ngồi xếp bằng trên sàn với Ken (sếp của tôi, tất cả đều 29 tuổi
năm tuổi và không say rượu) khóc về quá trình vector hóa được bao lâu
công việc đã đưa tôi. Rượu đã giải phóng nỗi sợ hãi và bất an dồn nén của tôi
về ước tính của tôi. Tôi không nghĩ rằng đầu tôi ở trong lòng anh ấy, nhưng trí nhớ của tôi chỉ
không rõ ràng lắm về loại chi tiết đó.
Tôi nhớ đã hỏi anh ấy liệu anh ấy có giận tôi không, và liệu anh ấy có nghĩ rằng điều đó đang diễn ra
tôi quá lâu. Mặc dù màn đêm mờ ảo, nhưng phản ứng của anh ấy vẫn rõ ràng
trong những thập kỷ tiếp theo. Anh ấy nói, "Vâng, tôi nghĩ bạn đã mất nhiều thời gian,
nhưng tôi có thể thấy rằng bạn đang làm việc chăm chỉ và tiến bộ tốt. Nó là
thứ mà chúng ta thực sự cần. Vì vậy, không, tôi không đi

## W H AT I S AN E S T I M AT E ?
Vấn đề là chúng ta xem ước tính theo những cách khác nhau. Doanh nghiệp thích xem
ước tính như cam kết. Các nhà phát triển muốn xem các ước tính dưới dạng phỏng đoán. Các
sự khác biệt là sâu sắc.
### A C OMMITMENT
Cam kết là điều bạn phải đạt được. Nếu bạn cam kết nhận được
một cái gì đó được hoàn thành vào một ngày nhất định, thì bạn chỉ cần hoàn thành nó vào ngày đó
ngày. Nếu điều đó có nghĩa là bạn phải làm việc 12 giờ một ngày, vào cuối tuần, bỏ qua gia đình
kỳ nghỉ, sau đó là nó. Bạn đã thực hiện cam kết và bạn phải tôn trọng nó.
Các chuyên gia không đưa ra cam kết trừ khi họ biết rằng họ có thể đạt được chúng.
Nó thực sự đơn giản như vậy. Nếu bạn được yêu cầu cam kết điều gì đó mà bạn
bạn không chắc chắn mình có thể làm được, thì danh dự của bạn chắc chắn sẽ giảm sút. Nếu bạn được hỏi
cam kết một ngày mà bạn biết rằng bạn có thể đạt được, nhưng sẽ đòi hỏi nhiều thời gian
giờ, cuối tuần và các kỳ nghỉ gia đình bị bỏ qua, sau đó lựa chọn là của bạn; nhưng
tốt hơn hết bạn nên sẵn sàng làm những gì cần thiết.
Cam kết là về sự chắc chắn. Những người khác sẽ chấp nhận cam kết của bạn
và lập kế hoạch dựa trên chúng. Cái giá phải trả cho việc bỏ lỡ những cam kết đó, đối với họ,
và danh tiếng của bạn, là rất lớn. Bỏ lỡ một cam kết là một hành động
không trung thực chỉ bớt ác hơn một chút so với nói dối công khai.

### A N E S T I M AT E
Một ước tính là một phỏng đoán. Không có cam kết nào được ngụ ý. Không có lời hứa nào được thực hiện.
Thiếu một ước tính không phải là điều đáng trách. Lý do chúng tôi làm
ước tính là do chúng tôi không biết một cái gì đó sẽ mất bao lâu.
Thật không may, hầu hết các nhà phát triển phần mềm đều là những nhà ước tính tồi tệ. Đây không phải là vì
có một số kỹ năng bí mật để ước tính — thì không. Lý do chúng ta thường rất tệ
ước tính là do chúng tôi không hiểu bản chất thực sự của ước tính.
Một ước tính không phải là một con số. Một ước tính là một phân phối. Xem xét:
138W CÓ TÔI S
AN
ƯỚC TÍNH ?
Mike: "Ước tính của bạn để hoàn thành nhiệm vụ Frazzle là gì?"
Peter: "Ba ngày."
Peter có thực sự sẽ hoàn thành trong ba ngày? Có thể, nhưng khả năng xảy ra là bao nhiêu?
Câu trả lời là: Chúng tôi không biết. Ý của Peter là gì, và điều gì đã
Mike đã học? Nếu Mike trở lại sau ba ngày, anh ấy có ngạc nhiên không nếu Peter
chưa xong? Tại sao anh ta lại như vậy? Peter đã không thực hiện một cam kết. Peter có
không cho anh ta biết khả năng ba ngày so với bốn ngày hoặc năm ngày.
Điều gì sẽ xảy ra nếu Mike hỏi Peter về khả năng ước tính của anh ta về
ba ngày là?
Mike: “Khả năng là bạn sẽ hoàn thành trong ba ngày?
Peter: "Rất có thể."
Mike: "Bạn có thể đặt một con số vào nó?"
Peter: "Năm mươi hay sáu mươi phần trăm."
Mike: "Vì vậy, rất có thể bạn sẽ mất bốn ngày."
Peter: “Đúng vậy, thực tế thì tôi có thể mất đến năm hoặc sáu, mặc dù tôi nghi ngờ điều đó.”
Mike: "Bạn nghi ngờ điều đó đến mức nào?"
Peter: "Ồ, tôi không biết ... tôi chắc chắn chín mươi lăm phần trăm là tôi sẽ xong việc
trước khi sáu ngày trôi qua. ”
Mike: "Ý bạn là nó có thể là bảy ngày?"
Peter: “Chà, chỉ khi mọi thứ không ổn. Heck, nếu mọi thứ diễn ra
sai, tôi có thể mất mười hoặc thậm chí mười một ngày. Nhưng nó không phải là
Có thể là rất nhiều điều sẽ sai. "
Bây giờ chúng tôi đang bắt đầu trau dồi sự thật. Ước tính của Peter là một xác suất
sự phân phối. Trong tâm trí của mình, Peter thấy khả năng hoàn thành giống như những gì
Hình 10-1.
Bạn có thể thấy tại sao Peter đưa ra ước tính ban đầu là ba ngày. Nó là cao nhất
thanh trên biểu đồ. Vì vậy, trong tâm trí của Phi-e-rơ, đó là khoảng thời gian có thể xảy ra nhất cho nhiệm vụ.
Nhưng Mike nhìn nhận mọi thứ theo cách khác. Anh ấy nhìn vào phần đuôi bên phải của biểu đồ và
lo lắng rằng Peter có thể thực sự mất mười một ngày để hoàn thành.

### I MPLIED C OMMITMENTS
Vì vậy, bây giờ Mike có một vấn đề. Anh ấy không chắc chắn về thời gian mà Peter sẽ
hoàn thành nhiệm vụ. Để giảm thiểu sự không chắc chắn đó, anh ta có thể yêu cầu Peter cho một
lời cam kết. Đây là điều mà Phi-e-rơ không có tư cách để cho.
Mike: "Peter, bạn có thể cho tôi một cuộc hẹn khó khi bạn xong việc không?"
Peter: “Không, Mike. Như tôi đã nói, nó có thể sẽ được thực hiện trong ba, có thể là bốn,
ngày. ”
Mike: "Vậy chúng ta có thể nói bốn không?"
Peter: "Không, có thể là năm hoặc sáu."
Cho đến nay, mọi người đều cư xử công bằng. Mike đã yêu cầu một cam kết và Peter
đã cẩn thận từ chối đưa cho anh ta một cái. Vì vậy, Mike thử một cách khác:
1. Định luật Murphy cho rằng nếu bất cứ điều gì có thể sai, nó sẽ sai.
140PERT
Mike: "OK, Peter, nhưng bạn có thể cố gắng làm nó không quá sáu ngày không?"
Lời cầu xin của Mike nghe có vẻ vô tội và Mike chắc chắn không có ý định xấu.
Nhưng chính xác thì Mike đang yêu cầu Peter làm gì? “Thử” nghĩa là gì?
Chúng ta đã nói về điều này trước đây, trở lại trong Chương 2. Từ try là một thuật ngữ được nạp. Nếu
Peter đồng ý “thử” sau đó anh ta cam kết sáu ngày. Không có cách nào khác để
diễn giải nó. Đồng ý cố gắng là đồng ý thành công.
Có thể có cách giải thích nào khác? Chính xác thì Peter là gì
sẽ làm gì để "thử"? Anh ấy sẽ đi làm hơn tám giờ? Đó là
ngụ ý rõ ràng. Cuối tuần anh ấy có đi làm không? Vâng, điều đó cũng được ngụ ý. Anh ấy sẽ
bỏ qua kỳ nghỉ gia đình? Vâng, đó cũng là một phần của hàm ý. Tất cả những thứ đó
là một phần của "cố gắng". Nếu Peter không làm những điều đó, thì Mike có thể buộc tội
anh ấy không cố gắng đủ nhiều.
Các nhà chuyên môn phân biệt rõ ràng giữa ước tính và cam kết.
Họ không cam kết trừ khi họ biết chắc chắn rằng họ sẽ thành công. họ đang
cẩn thận không đưa ra bất kỳ cam kết ngụ ý nào. Họ giao tiếp với các proba-
phân phối nhanh các ước tính của họ càng rõ ràng càng tốt, để các nhà quản lý có thể
lập kế hoạch phù hợp.

## PE RT
Năm 1957, Kỹ thuật Đánh giá và Đánh giá Chương trình (PERT) được tạo ra để
hỗ trợ dự án tàu ngầm Polaris của Hải quân Hoa Kỳ. Một trong những yếu tố của PERT là
cách tính toán ước tính. Đề án cung cấp một cách rất đơn giản, nhưng rất
cách hiệu quả để chuyển đổi các ước tính thành phân phối xác suất phù hợp với các nhà quản lý.
Khi bạn ước tính một nhiệm vụ, bạn cung cấp ba con số. Đây được gọi là tam biến
phân tích:
• O: Ước tính Lạc quan. Con số này thật lạc quan. Bạn chỉ có thể
hoàn thành nhiệm vụ này một cách nhanh chóng nếu mọi thứ hoàn toàn suôn sẻ. Thật,
để phép toán hoạt động, con số này phải nhỏ hơn nhiều
141C CHƯƠNG 10
ƯỚC LƯỢNG
1% cơ hội xuất hiện. 2 Trong trường hợp của Phi-e-rơ, đây sẽ là 1 ngày, như thể hiện trong
Hình 10-1.
• N: Ước tính Danh nghĩa. Đây là ước tính có cơ hội thành công lớn nhất.
Nếu bạn định vẽ biểu đồ thanh, nó sẽ là thanh cao nhất, như được hiển thị trong
Hình 10-1. Đó là 3 ngày.
• P: Ước tính Bi quan. Một lần nữa điều này là cực kỳ bi quan. Nó nên
bao gồm mọi thứ ngoại trừ bão, chiến tranh hạt nhân, lỗ đen đi lạc và
các thảm họa khác. Một lần nữa, phép toán chỉ hoạt động nếu con số này ít hơn nhiều
hơn 1% cơ hội thành công. Trong trường hợp của Peter, con số này nằm ngoài bảng xếp hạng
bên phải. Vậy là 12 ngày.
Với ba ước lượng này, chúng ta có thể mô tả phân phối xác suất là
sau:
• μ =
O + 4 N + P
6
μ là thời gian dự kiến ​​của nguyên công. Trong trường hợp của Phi-e-rơ, nó là (1 + 12 + 12) / 6, hoặc
khoảng 4,2 ngày. Đối với hầu hết các nhiệm vụ, đây sẽ là một con số hơi bi quan
bởi vì phần đuôi bên phải của phân phối dài hơn phần bên trái
đuôi. 3
• σ =
P - O
6
s là độ lệch chuẩn 4 của phân phối xác suất cho nhiệm vụ. Nó là một
đo lường mức độ không chắc chắn của nhiệm vụ. Khi con số này lớn,
sự không chắc chắn cũng lớn. Đối với Peter, con số này là (12 - 1) / 6, tức khoảng 1,8 ngày.
Với ước tính của Peter là 4,2 / 1,8, Mike hiểu rằng nhiệm vụ này có thể sẽ
hoàn thành trong vòng năm ngày nhưng cũng có thể mất 6, thậm chí 9 ngày để hoàn thành.
2. Con số chính xác cho phân phối chuẩn là 1: 769, hoặc 0,13%, hoặc 3 sigma. Tỷ lệ một trong một nghìn là
có lẽ an toàn.
3. PERT giả định rằng điều này gần đúng với phân phối beta. Điều này có ý nghĩa vì thời lượng tối thiểu
đối với một nhiệm vụ thường chắc chắn hơn nhiều so với mức tối đa. [McConnell2006] Hình 1-3.
4. Nếu bạn không biết độ lệch chuẩn là gì, bạn nên tìm một bản tóm tắt tốt về xác suất và thống kê-
tics. Khái niệm này không khó hiểu, và nó sẽ phục vụ bạn rất tốt.
142PERT
Nhưng Mike không chỉ quản lý một nhiệm vụ. Anh ấy đang quản lý một dự án gồm nhiều nhiệm vụ.
Peter có ba nhiệm vụ mà anh ấy phải thực hiện theo trình tự. Peter có
ước tính các nhiệm vụ này như trong Bảng 10-1.
Bảng 10-1 Nhiệm vụ của Peter
Nhiệm vụ Lạc quan Danh nghĩa Bi quan μ σ
Alpha
Beta
Gamma 1
1
3 3
1,5
6,25 12
14
11 4.2
3.5
6,5 1,8
2,2
1,3
Có chuyện gì với nhiệm vụ "beta" đó? Có vẻ như Peter khá tự tin về điều đó,
nhưng điều gì đó có thể xảy ra sẽ khiến anh ta trật bánh đáng kể.
Mike nên giải thích điều đó như thế nào? Mike nên lên kế hoạch cho Peter trong bao lâu
hoàn thành cả ba nhiệm vụ?
Hóa ra chỉ với một vài phép tính đơn giản, Mike có thể kết hợp tất cả các
nhiệm vụ và đưa ra phân phối xác suất cho toàn bộ nhiệm vụ. Các
toán học khá đơn giản:
• μ dãy = ∑ μ nhiệm vụ
Đối với bất kỳ chuỗi nhiệm vụ nào, thời lượng dự kiến ​​của chuỗi đó là
tổng đơn giản của tất cả các khoảng thời gian dự kiến ​​của các nhiệm vụ trong trình tự đó. Vì vậy nếu
Peter có ba nhiệm vụ phải hoàn thành và ước tính của chúng là 4,2 / 1,8, 3,5 / 2,2,
và 6,5 / 1,3, thì Peter có thể sẽ hoàn thành cả ba trong khoảng 14 ngày:
4,2 + 3,5 + 6,5.
• σ dãy =
∑ σ
2
bài tập
Độ lệch chuẩn của dãy là căn bậc hai của tổng
bình phương độ lệch chuẩn của các nguyên công. Vì vậy, độ lệch chuẩn cho
cả ba nhiệm vụ của Phi-e-rơ là khoảng 3.
(1,8 2 + 2,2 2 + 1,3 2) 1/2 =
(3,24 + 2,48 + 1,69) 1/2 =
9,77 1/2 = ∼ 3,13
143C CHƯƠNG 10
ƯỚC LƯỢNG
Điều này cho Mike biết rằng nhiệm vụ của Peter có thể sẽ mất 14 ngày, nhưng rất có thể
17 ngày (1 giây) và thậm chí có thể mất 20 ngày (2 giây). Nó thậm chí có thể mất
lâu hơn, nhưng điều đó khá khó xảy ra.
Nhìn lại bảng ước lượng. Bạn có cảm thấy áp lực khi đạt được cả ba không
nhiệm vụ hoàn thành trong năm ngày? Rốt cuộc, các ước tính trường hợp tốt nhất là 1, 1 và 3. Ngay cả
ước tính danh nghĩa chỉ thêm tối đa 10 ngày. Làm thế nào chúng ta có được tất cả các con đường đến 14
ngày, với khả năng là 17 hoặc 20? Câu trả lời là sự không chắc chắn trong những
hợp chất nhiệm vụ theo cách bổ sung tính hiện thực cho kế hoạch.
Nếu bạn là một lập trình viên có hơn một vài năm kinh nghiệm, bạn có thể đã thấy
các dự án đã được ước tính một cách lạc quan, và điều đó đã mất từ ​​ba đến năm lần
lâu hơn hy vọng. Sơ đồ PERT đơn giản vừa được hiển thị là một cách hợp lý
để giúp ngăn chặn việc đặt ra những kỳ vọng lạc quan. Các chuyên gia phần mềm rất
cẩn thận để đặt kỳ vọng hợp lý mặc dù áp lực để cố gắng đi nhanh.




## E S T I M AT I N G T A S K S
Mike và Peter đã mắc một sai lầm khủng khiếp. Mike đã hỏi Peter bao lâu
nhiệm vụ của anh ấy sẽ thực hiện. Phi-e-rơ đã đưa ra những câu trả lời ba ngôi trung thực, nhưng còn
ý kiến của đồng đội của mình? Họ có thể có một ý tưởng khác?
Nguồn lực ước tính quan trọng nhất mà bạn có là những người xung quanh bạn.
Họ có thể thấy những thứ mà bạn không thấy. Họ có thể giúp bạn ước tính nhiệm vụ của mình nhiều hơn
chính xác hơn bạn có thể ước tính chúng một mình.
### W I D E B A N D D E L P H I
Vào những năm 1970, Barry Boehm đã giới thiệu cho chúng ta một kỹ thuật ước tính được gọi là
"Delphi băng rộng." 5 Đã có nhiều biến thể trong những năm qua. Một số thì
chính thức, một số là không chính thức; nhưng tất cả đều có một điểm chung: đồng thuận.
Chiến lược rất đơn giản. Một nhóm người tập hợp, thảo luận về một nhiệm vụ, ước tính
nhiệm vụ và lặp lại cuộc thảo luận và ước tính cho đến khi họ đi đến thống nhất.
5. [Boehm81]
144E KÍCH THÍCH T NHƯ KS
Phương pháp ban đầu do Boehm vạch ra liên quan đến một số cuộc họp và
tài liệu liên quan đến quá nhiều nghi lễ và chi phí cho sở thích của tôi. tôi thích
các phương pháp tiếp cận chi phí thấp đơn giản như sau.

### Flying Fingers
Mọi người ngồi quanh bàn. Các nhiệm vụ được thảo luận tại một thời điểm. Đối với mỗi nhiệm vụ
có thảo luận về những gì nhiệm vụ liên quan, những gì có thể gây khó hiểu hoặc
làm phức tạp nó và cách nó có thể được triển khai. Sau đó, những người tham gia đặt
bàn tay của họ ở dưới bàn và giơ từ 0 đến 5 ngón tay dựa trên thời gian họ
nghĩ rằng nhiệm vụ sẽ thực hiện. Người kiểm duyệt đếm 1-2-3 và tất cả những người tham gia
chỉ tay của họ cùng một lúc.
Nếu mọi người đồng ý thì họ làm tiếp nhiệm vụ tiếp theo. Nếu không họ tiếp tục
cuộc thảo luận để xác định lý do tại sao họ không đồng ý. Họ lặp lại điều này cho đến khi họ đồng ý.
Thỏa thuận không cần phải tuyệt đối. Miễn là các ước tính gần nhau, nó
đủ tốt. Vì vậy, ví dụ, một sự nhập nhèm của 3s và 4s là đồng ý. Tuy nhiên
nếu mọi người giơ 4 ngón tay ngoại trừ một người giơ 1 ngón tay, thì
họ có một cái gì đó để nói về.
Quy mô của ước tính được quyết định vào đầu cuộc họp. Nó có thể
là số ngày cho một nhiệm vụ hoặc có thể là một số thang đo thú vị hơn
chẳng hạn như "ngón tay nhân ba lần" hoặc "ngón tay vuông góc".
Đồng thời của việc hiển thị các ngón tay là quan trọng. Chúng tôi không muốn mọi người
thay đổi ước tính của họ dựa trên những gì họ thấy người khác làm.

### Planning Poker
Năm 2002, James Grenning đã viết một bài báo thú vị 6 mô tả “Lập kế hoạch Poker”.
Biến thể này của delphi băng rộng đã trở nên phổ biến đến mức một số
các công ty đã sử dụng ý tưởng này để tạo quà tặng tiếp thị dưới dạng
lập kế hoạch cho bộ bài poker. 7 Thậm chí còn có một trang web tên là Planningpoker.com
mà bạn có thể sử dụng để lập kế hoạch chơi poker trên Mạng với các đội phân tán.
6. [Grenning2002]
7. http://store.mountaingoatsoftware.com/products/planning-poker-cards
145C CHƯƠNG 10
ƯỚC LƯỢNG
Ý tưởng rất đơn giản. Đối với mỗi thành viên của nhóm ước tính, hãy xử lý một tay
thẻ có các số khác nhau trên chúng. Các số từ 0 đến 5 hoạt động tốt,
và làm cho hệ thống này về mặt logic tương đương với ngón tay bay.
Chọn một nhiệm vụ và thảo luận về nó. Tại một số điểm, người kiểm duyệt yêu cầu mọi người chọn một
Thẻ. Các thành viên của nhóm rút ra một thẻ phù hợp với ước tính của họ và
giữ nó với mặt sau hướng ra ngoài để không ai khác có thể thấy giá trị của
lá bài. Sau đó, người kiểm duyệt yêu cầu mọi người xuất trình thẻ của họ.
Phần còn lại chỉ như ngón tay bay. Nếu có sự thống nhất, thì ước tính là
Đã được chấp nhận. Nếu không, các lá bài sẽ được trả về tay và người chơi
tiếp tục thảo luận về nhiệm vụ.
Nhiều "khoa học" đã được dành riêng để chọn các giá trị thẻ chính xác cho
tay. Một số người đã tiến xa đến mức sử dụng các thẻ dựa trên chuỗi Fibonacci.
Những người khác đã bao gồm thẻ cho vô cực và dấu hỏi. Cá nhân tôi nghĩ
năm thẻ có nhãn 0, 1, 3, 5, 10 là đủ.

### Affinity Estimation
Một biến thể đặc biệt độc đáo của delphi băng rộng đã được cho tôi thấy một số
năm trước của Lowell Lindstrom. Tôi đã có một chút may mắn với điều này
tiếp cận với nhiều khách hàng và nhóm khác nhau.
Tất cả các nhiệm vụ được ghi vào thẻ, không có bất kỳ ước tính nào hiển thị. Các
nhóm ước tính đứng xung quanh bàn hoặc tường với các thẻ được trải rộng
ngẫu nhiên. Các thành viên trong nhóm không nói chuyện, họ chỉ bắt đầu phân loại các thẻ
tương đối với nhau. Các tác vụ mất nhiều thời gian hơn được chuyển sang bên phải. Nhỏ hơn
nhiệm vụ di chuyển sang trái.
Mọi thành viên trong nhóm đều có thể di chuyển bất kỳ thẻ nào bất kỳ lúc nào, ngay cả khi nó đã được
do một thành viên khác chuyển đến. Bất kỳ thẻ nào được di chuyển hơn h lần sẽ được dành cho
thảo luận.
Cuối cùng, việc phân loại im lặng và thảo luận có thể bắt đầu. Bất đồng
về thứ tự của các thẻ được khám phá. Có thể có một số thiết kế nhanh
phiên hoặc một số khung dây vẽ tay nhanh để giúp đạt được sự đồng thuận.
146C ONC LUS ION
Bước tiếp theo là vẽ các đường thẳng giữa các thẻ biểu thị kích thước nhóm.
Các nhóm này có thể là ngày, tuần hoặc điểm. Năm thùng trong một Fibonacci
trình tự (1, 2, 3, 5, 8) là truyền thống.

### Trivariate Estimates
Các kỹ thuật delphi băng rộng này rất tốt cho việc chọn một danh nghĩa duy nhất
ước tính cho một nhiệm vụ. Nhưng như chúng tôi đã nói trước đó, hầu hết thời gian chúng tôi muốn ba
ước tính để chúng ta có thể tạo phân phối xác suất. Người lạc quan và
các giá trị bi quan cho mỗi nhiệm vụ có thể được tạo ra rất nhanh chóng bằng cách sử dụng bất kỳ
các biến thể delphi băng rộng. Ví dụ: nếu bạn đang lập kế hoạch chơi poker, bạn
chỉ cần yêu cầu nhóm giơ thẻ cho ước tính bi quan của họ và sau đó
lấy cao nhất. Bạn làm tương tự để ước tính lạc quan và lấy mức thấp nhất.

## T H E L AW OF L ARGE N UMBERS
Các ước tính đầy sai sót. Đó là lý do tại sao chúng được gọi là ước tính. Một cách của
quản lý lỗi là lợi dụng Luật Số lớn. 8 Một hàm ý
của luật này là nếu bạn chia một nhiệm vụ lớn thành nhiều nhiệm vụ nhỏ hơn và ước tính
chúng một cách độc lập, tổng các ước tính của các nhiệm vụ nhỏ sẽ nhiều hơn
chính xác hơn một ước tính duy nhất của nhiệm vụ lớn hơn. Lý do cho sự gia tăng này trong
chính xác là các lỗi trong các nhiệm vụ nhỏ có xu hướng tích hợp ra ngoài.
Thành thật mà nói, điều này là lạc quan. Sai số trong ước tính có xu hướng đánh giá thấp và
không được đánh giá quá cao nên việc tích hợp khó hoàn hảo. Điều đó đang được nói,
chia các nhiệm vụ lớn thành các nhiệm vụ nhỏ và ước tính các nhiệm vụ nhỏ một cách độc lập
vẫn là một kỹ thuật tốt. Một số lỗi được tích hợp và phá vỡ
hoàn thành nhiệm vụ là một cách hay để hiểu rõ hơn về những nhiệm vụ đó và khám phá những điều bất ngờ.

## C ONCLUSION
Các nhà phát triển phần mềm chuyên nghiệp biết cách cung cấp cho doanh nghiệp
ước tính thực tế mà doanh nghiệp có thể sử dụng cho mục đích lập kế hoạch. Họ không
đưa ra những lời hứa mà họ không thể giữ và họ không cam kết
họ không chắc mình có thể gặp nhau.
8. http://en.wikipedia.org/wiki/Law_of_large_numbers
147C CHƯƠNG 10
ƯỚC LƯỢNG
Khi các chuyên gia đưa ra cam kết, họ cung cấp những con số cứng và sau đó
họ đưa ra những con số đó. Tuy nhiên, trong hầu hết các trường hợp, các chuyên gia không làm
cam kết như vậy. Thay vào đó, chúng cung cấp các ước tính xác suất mô tả
thời gian hoàn thành dự kiến ​​và phương sai có thể xảy ra.
Các nhà phát triển chuyên nghiệp làm việc với các thành viên khác trong nhóm của họ để đạt được
nhất trí về các ước tính được đưa ra cho ban lãnh đạo.
Các kỹ thuật được mô tả trong chương này là ví dụ về một số
cách mà các nhà phát triển chuyên nghiệp tạo ra các ước tính thực tế. Đây không phải là
chỉ những kỹ thuật như vậy và không nhất thiết phải là tốt nhất. Họ chỉ đơn giản là
kỹ thuật mà tôi đã tìm thấy để làm việc tốt cho tôi.