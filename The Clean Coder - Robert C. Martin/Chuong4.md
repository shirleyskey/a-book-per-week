# CODING 
## Chương 4: CODING
Trong một cuốn sách trước đây, tôi đã viết rất nhiều về cấu trúc và bản chất của Clean Code.
Chương này thảo luận về hành động mã hóa và bối cảnh xung quanh hành động đó. 

Khi tôi 18 tuổi, tôi có thể đánh máy khá tốt, nhưng tôi phải nhìn vào các phím. Tôi không thể gõ mù. Vì vậy, vào một buổi tối, tôi đã dành vài giờ đồng hồ dài trên bàn phím IBM 029 không nhìn vào các ngón tay của mình khi tôi gõ một chương trình mà tôi đã viết trên một số hình thức mã hóa. Tôi kiểm tra từng thẻ sau khi tôi gõ nó và loại bỏ những thẻ bị gõ sai.

Lúc đầu, tôi gõ khá nhiều lỗi. Vào cuối buổi tối, tôi đã đánh máy tất cả chúng với mức độ gần như hoàn hảo. Tôi nhận ra rằng, trong suốt đêm dài, việc đánh máy mù mịt là vì sự tự tin. Các ngón tay của tôi biết vị trí của các phím, tôi chỉ cần có được sự tự tin rằng tôi không mắc lỗi. Một trong những điều giúp tôi tự tin đó là tôi có thể cảm nhận được khi mình mắc lỗi. Đến cuối buổi tối, nếu tôi mắc lỗi, tôi gần như biết ngay lập tức và chỉ cần rút thẻ ra mà không cần nhìn vào.
Có thể nhận ra lỗi của bạn thực sự quan trọng. Không chỉ trong việc đánh máy, mà còn trong mọi thứ. 

Có khả năng nhận biết lỗi có nghĩa là bạn nhanh chóng đóng vòng phản hồi và học hỏi từ lỗi của mình nhanh hơn. Tôi đã nghiên cứu và thành thạo một số lĩnh vực kể từ ngày đó vào ngày 029. Tôi nhận thấy rằng trong mỗi trường hợp, chìa khóa để thành thạo là sự tự tin và nhận thức sai lầm.

Chương này mô tả bộ quy tắc và nguyên tắc viết mã của cá nhân tôi. Những quy tắc và nguyên tắc này không phải về bản thân mã của tôi; chúng là về hành vi, tâm trạng và thái độ của tôi trong khi viết mã. Họ mô tả bối cảnh tinh thần, đạo đức và cảm xúc của riêng tôi để viết mã. Đây là nguồn gốc của sự tự tin và cảm giác sai lầm của tôi.
Bạn có thể sẽ không đồng ý với tất cả những gì tôi nói ở đây. Rốt cuộc, đây là công cụ cá nhân sâu sắc. 
Trên thực tế, bạn có thể không đồng ý một cách mãnh liệt với một số thái độ và nguyên tắc của tôi. Không sao cả — chúng không nhằm mục đích trở thành sự thật tuyệt đối cho bất kỳ ai khác ngoài tôi. Họ là gì là cách tiếp cận của một người để trở thành một lập trình viên chuyên nghiệp.

Có lẽ, bằng cách nghiên cứu và suy ngẫm về quy trình mã hóa cá nhân của tôi, bạn có thể học cách giật viên sỏi từ tay tôi.

### Chuẩn Bị
Viết mã là một hoạt động đầy thử thách và mệt mỏi về trí tuệ. Nó đòi hỏi một mức độ tập trung và tập trung mà ít ngành học khác yêu cầu. Lý do cho điều này là việc viết mã đòi hỏi bạn phải kết hợp nhiều yếu tố cạnh tranh cùng một lúc.

1. Đầu tiên, mã của bạn phải hoạt động. Bạn phải hiểu mình đang giải quyết vấn đề gì và hiểu cách giải quyết vấn đề đó. Bạn phải đảm bảo rằng mã bạn viết là đại diện trung thực cho giải pháp đó. Bạn phải quản lý mọi chi tiết của giải pháp đó trong khi vẫn nhất quán trong ngôn ngữ, nền tảng, kiến ​​trúc hiện tại và tất cả các vấn đề của hệ thống hiện tại.

2. Mã của bạn phải giải quyết được vấn đề do khách hàng đặt ra cho bạn. Thường thì các yêu cầu của khách hàng không thực sự giải quyết được vấn đề của khách hàng. Bạn phải xem điều này và thương lượng với khách hàng để đảm bảo rằng nhu cầu thực sự của khách hàng được đáp ứng.

3. Mã của bạn phải vừa khít với hệ thống hiện có. Nó không được làm tăng độ cứng, tính dễ vỡ hoặc độ mờ của hệ thống đó. Các phụ thuộc phải được quản lý tốt. Tóm lại, mã của bạn cần tuân theo các nguyên tắc kỹ thuật vững chắc.

4. Các lập trình viên khác phải đọc được mã của bạn. Đây không chỉ là vấn đề viết những lời bình luận hay. Thay vào đó, nó đòi hỏi bạn phải tạo mã theo cách để nó tiết lộ ý định của bạn. Điều này thật khó thực hiện. Thật vậy, đây có thể là điều khó khăn nhất mà một lập trình viên có thể thành thạo. Giải quyết tất cả những mối quan tâm này là khó. Về mặt sinh lý, rất khó để duy trì sự tập trung và tập trung cần thiết trong thời gian dài. Thêm vào đó là những vấn đề và sự xao lãng khi làm việc trong một nhóm, trong một tổ chức cũng như những mối quan tâm và lo lắng trong cuộc sống hàng ngày. Điểm mấu chốt là cơ hội để mất tập trung là rất cao.

Khi bạn không thể tập trung và tập trung đầy đủ, mã bạn viết sẽ sai. Nó sẽ có lỗi. Nó sẽ có cấu trúc sai. Nó sẽ mờ đục và phức tạp. Nó sẽ không giải quyết được các vấn đề thực sự của khách hàng. Tóm lại, nó sẽ phải được làm lại hoặc làm lại. Làm việc trong khi bị phân tâm sẽ tạo ra sự lãng phí.
Nếu bạn đang mệt mỏi hoặc mất tập trung, đừng viết mã. Bạn sẽ chỉ làm lại những gì bạn đã làm. Thay vào đó, hãy tìm cách loại bỏ những phiền nhiễu và ổn định tâm trí. 

### 3 A M C O D E
Đoạn mã tệ nhất mà tôi từng viết là lúc 3 giờ sáng. Đó là năm 1988, và tôi đang làm việc tại một công ty khởi nghiệp viễn thông tên là Clear Communications. Tất cả chúng tôi đã dành nhiều giờ để xây dựng “công bằng mồ hôi”. Tất nhiên, chúng tôi đã mơ ước giàu có.

Vào một buổi tối rất muộn — hay đúng hơn là một buổi sáng rất sớm, để giải quyết vấn đề về thời gian — tôi đã yêu cầu mã của mình gửi một tin nhắn đến chính nó thông qua hệ thống điều phối sự kiện (chúng tôi gọi đây là “gửi thư”). Đây là một giải pháp sai lầm, nhưng lúc 3 giờ sáng, nó trông khá tuyệt. Thật vậy, sau 18 giờ mã hóa vững chắc (chưa kể 60-70 giờ tuần), đó là tất cả những gì tôi có thể nghĩ đến. Tôi nhớ mình đã cảm thấy rất hài lòng về bản thân trong suốt thời gian dài làm việc. emoij🙂

Tôi nhớ cảm giác tận tâm Tôi nhớ mình đã nghĩ rằng làm việc lúc 3 giờ sáng là điều mà các chuyên gia nghiêm túc làm. Tôi đã sai làm sao!
Mã đó quay lại cắn chúng tôi hết lần này đến lần khác. Nó thiết lập một cấu trúc thiết kế bị lỗi mà mọi người đều sử dụng nhưng luôn phải sửa chữa. Nó gây ra tất cả các loại lỗi thời gian kỳ lạ và vòng lặp phản hồi kỳ lạ. Chúng ta sẽ đi vào vòng lặp thư vô hạn khi một thư khiến một thư khác được gửi và sau đó là vô hạn thư khác. Chúng tôi chưa bao giờ có thời gian để viết lại bài viết này (vì vậy chúng tôi nghĩ vậy) nhưng chúng tôi luôn dường như có thời gian để thêm một mụn cóc hoặc miếng vá khác để khắc phục nó. Mối nguy lớn dần và lớn dần, xung quanh đoạn mã 3 giờ sáng đó với ngày càng nhiều hành lý và tác dụng phụ. Nhiều năm sau, nó đã trở thành một trò đùa của cả đội. Bất cứ khi nào tôi mệt mỏi hoặc thất vọng, họ sẽ nói: “Hãy chú ý! Bob sắp gửi thư cho chính mình! ”

Đạo lý của câu chuyện này là: Đừng viết mã khi bạn mệt mỏi. Sự tận tâm và chuyên nghiệp là tính kỷ luật hơn giờ. Đảm bảo rằng giấc ngủ, sức khỏe và lối sống của bạn được điều chỉnh để bạn có thể thực hiện tám giờ tốt mỗi ngày.

### WORRY CODE
Bạn đã bao giờ gây gổ với người bạn đời hoặc bạn bè của mình, và sau đó cố gắng lập trình? Bạn có nhận thấy rằng có một quy trình nền đang chạy trong đầu bạn đang cố gắng giải quyết, hoặc ít nhất là xem lại cuộc chiến? Đôi khi bạn có thể cảm thấy căng thẳng của quá trình nền đó trong lồng ngực hoặc trong dạ dày.
Nó có thể khiến bạn cảm thấy lo lắng, chẳng hạn như khi bạn uống quá nhiều cà phê hoặc coca ăn kiêng. Nó gây mất tập trung.
Khi tôi lo lắng về một cuộc tranh cãi với vợ, khủng hoảng khách hàng hoặc một đứa con ốm, tôi không thể duy trì sự tập trung. Sự tập trung của tôi dao động. Tôi thấy mình dán mắt vào màn hình và các ngón tay trên bàn phím, không làm gì cả.

Bị tê liệt. Một triệu dặm làm việc thông qua các vấn đề trong
nền tảng chứ không phải thực sự giải quyết vấn đề mã hóa trước mặt tôi.
Đôi khi tôi buộc bản thân phải nghĩ về mã. Tôi có thể tự lái xe để viết một hoặc hai dòng. Tôi có thể thúc đẩy bản thân phải vượt qua một hoặc hai bài kiểm tra. Nhưng tôi không thể theo kịp. Chắc chắn tôi thấy mình rơi vào trạng thái vô cảm sững sờ, không nhìn thấy gì qua đôi mắt đang mở của mình, trong nội tâm đang trào lên nỗi lo lắng trên nền.
Tôi đã học được rằng đây không phải là thời gian để viết mã. Bất kỳ mã nào tôi sản xuất sẽ là thùng rác. Vì vậy, thay vì viết mã, tôi cần giải quyết nỗi lo.

Tất nhiên, có rất nhiều lo lắng mà chỉ đơn giản là không thể giải quyết trong một hoặc hai giờ. Hơn nữa, người sử dụng lao động của chúng tôi có khả năng không chấp nhận được việc chúng tôi không thể làm việc được lâu khi chúng tôi giải quyết các vấn đề cá nhân của mình. Bí quyết là tìm hiểu cách tắt quy trình nền hoặc ít nhất là giảm mức độ ưu tiên của nó để nó không phải là
mất tập trung liên tục.

Tôi làm điều này bằng cách phân chia thời gian của mình. Thay vì ép bản thân viết mã trong khi nỗi lo về nền tảng đang đeo bám tôi, tôi sẽ dành một khoảng thời gian chuyên dụng, có lẽ là một giờ, để giải quyết vấn đề đang tạo ra nỗi lo lắng. Nếu con tôi bị ốm, tôi sẽ gọi điện về nhà và kiểm tra. Nếu tôi cãi nhau với vợ, tôi sẽ gọi
cô ấy và nói chuyện thông qua các vấn đề. Nếu gặp vấn đề về tiền bạc, tôi sẽ dành thời gian suy nghĩ về cách giải quyết các vấn đề tài chính. Tôi biết mình không có khả năng giải quyết các vấn đề trong giờ này, nhưng rất có thể tôi có thể giảm bớt sự lo lắng và làm dịu quá trình xử lý nền.
Lý tưởng nhất là thời gian dành cho vật lộn với các vấn đề cá nhân sẽ là thời gian cá nhân. Sẽ là một điều đáng tiếc nếu dành một giờ tại văn phòng theo cách này. Các nhà phát triển chuyên nghiệp phân bổ thời gian cá nhân của họ để đảm bảo rằng thời gian ở văn phòng hiệu quả nhất có thể. Điều đó có nghĩa là bạn nên dành thời gian cụ thể tại
về nhà để giải quyết những lo lắng của bạn để bạn không phải mang chúng đến văn phòng.
Mặt khác, nếu bạn thấy mình đang ở văn phòng và những lo lắng về nền tảng đang làm giảm năng suất của bạn, thì tốt hơn là bạn nên dành một giờ để làm yên chúng hơn là sử dụng vũ lực để viết mã mà bạn sẽ phải vứt bỏ sau đó ( hoặc tệ hơn, sống với).

### THE FLOW ZONE
Nhiều người đã viết về trạng thái siêu năng suất được gọi là “dòng chảy”.
Một số lập trình viên gọi nó là “Vùng”. Dù nó được gọi là gì, bạn có thể đã quen thuộc với nó. Đó là trạng thái ý thức tập trung cao độ, tầm nhìn đường hầm mà các lập trình viên có thể đạt được khi họ viết mã. Ở trạng thái này họ cảm thấy hiệu quả. Trong trạng thái này, họ cảm thấy không thể sai lầm. Và vì vậy, họ mong muốn đạt được trạng thái đó, và thường đo lường giá trị bản thân bằng khoảng thời gian họ có thể dành ở đó.
Đây là một gợi ý nhỏ từ một người đã ở đó và quay lại: Tránh Khu vực. Trạng thái ý thức này không thực sự siêu năng suất và chắc chắn là không thể sai lầm. Đó thực sự chỉ là một trạng thái thiền định nhẹ nhàng, trong đó một số năng lực lý trí nhất định bị suy giảm để có cảm giác tốc độ.
Hãy để tôi nói rõ về điều này. Bạn sẽ viết nhiều mã hơn trong Zone. Nếu bạn đang tập TDD, bạn sẽ đi vòng lặp red / green / refactor nhanh hơn.
Và bạn sẽ cảm thấy hưng phấn nhẹ hoặc cảm giác muốn chinh phục. Vấn đề là bạn đánh mất một số bức tranh lớn khi bạn ở trong Zone, vì vậy bạn có thể sẽ đưa ra những quyết định mà sau đó bạn sẽ phải quay lại và đảo ngược. Mã được viết trong Zone có thể ra mắt nhanh hơn, nhưng bạn sẽ quay lại để thăm nó nhiều hơn.

Ngày nay, khi tôi cảm thấy mình bị trượt vào Khu vực này, tôi đã bỏ đi vài phút.
Tôi giải tỏa đầu óc bằng cách trả lời một vài email hoặc xem một số dòng tweet. Nếu gần đến trưa, tôi sẽ nghỉ ăn trưa. Nếu tôi đang làm việc trong một nhóm, tôi sẽ tìm một đối tác theo cặp.
Một trong những lợi ích lớn của lập trình cặp là hầu như không thể cho một cặp vào Vùng. Khu vực là một trạng thái không cộng đồng, trong khi việc ghép nối đòi hỏi giao tiếp liên tục và cường độ cao. Thật vậy, một trong những phàn nàn tôi
thường nghe nói về việc ghép nối là nó chặn sự xâm nhập vào Zone. Tốt! Zone không phải là nơi bạn muốn.
Chà, điều đó không hoàn toàn đúng. Có những lúc Khu vực chính xác là nơi bạn muốn. Khi bạn đang luyện tập. Nhưng chúng ta sẽ nói về điều đó trong một chương khác.

### MUSIC 
Tại Teradyne, vào cuối những năm 70, tôi có một văn phòng riêng. Tôi là quản trị viên hệ thống của PDP 11/60 của chúng tôi và vì vậy tôi là một trong số ít lập trình viên được phép có một thiết bị đầu cuối riêng. Thiết bị đầu cuối đó là VT100 chạy ở 9600 baud và được kết nối
tới PDP 11 với cáp RS232 dài 80 feet mà tôi đã mắc trên trần nhà từ văn phòng đến phòng máy tính.
Tôi đã có một hệ thống âm thanh nổi trong văn phòng của mình. Đó là một bàn xoay, amp và loa sàn cũ. Tôi đã có một bộ sưu tập vinyl đáng kể, bao gồm Led Zeppelin, Pink Floyd, và…. Vâng, bạn có được hình ảnh.

Tôi đã từng quay âm thanh nổi đó và sau đó viết mã. Tôi nghĩ nó đã giúp tôi
sự tập trung. Nhưng tôi đã nhầm. Một ngày nọ, tôi quay lại một mô-đun mà tôi đã chỉnh sửa trong khi nghe đoạn mở đầu của Bức tường. Các bình luận trong đoạn mã đó chứa lời bài hát và các chú thích biên tập về máy bay ném bom bổ nhào và những đứa trẻ đang khóc.
Đó là khi nó đánh tôi. Là một người đọc mã, tôi đang tìm hiểu về bộ sưu tập âm nhạc của tác giả (tôi) hơn là tìm hiểu về vấn đề mà mã đang cố gắng giải quyết.

Tôi nhận ra rằng tôi chỉ viết mã không tốt khi nghe nhạc. Âm nhạc không giúp tôi tập trung. Thật vậy, hành động nghe nhạc dường như tiêu tốn một số tài nguyên quan trọng mà tâm trí tôi cần để viết mã sạch và được thiết kế tốt.
Có thể nó không hoạt động theo cách đó cho bạn. Có lẽ âm nhạc giúp bạn viết mã. Tôi biết rất nhiều người viết mã khi đeo tai nghe. Tôi chấp nhận rằng âm nhạc có thể giúp ích cho họ, nhưng tôi cũng nghi ngờ rằng điều thực sự đang xảy ra là âm nhạc đang giúp họ bước vào Khu vực.

### INTERRUPTIONS
Hình dung bản thân khi bạn đang viết mã tại máy trạm của mình. Bạn trả lời thế nào khi ai đó hỏi bạn một câu hỏi? Bạn có chụp chúng không? Bạn có trừng mắt không? Ngôn ngữ cơ thể của bạn có bảo họ biến đi vì bạn bận không? Tóm lại, bạn có thô lỗ không?
Hoặc, bạn có dừng việc bạn đang làm và lịch sự giúp đỡ ai đó đang gặp khó khăn? Làm bạn đối xử với họ như bạn sẽ đối xử với bạn nếu bạn gặp khó khăn?
Phản ứng thô lỗ thường đến từ Zone. Bạn có thể bực bội khi bị lôi ra khỏi Khu vực, hoặc bạn có thể bực bội khi ai đó can thiệp vào nỗ lực vào Khu vực của bạn. Dù bằng cách nào, sự thô lỗ thường xuất phát từ mối quan hệ của bạn với khu vực. Tuy nhiên, đôi khi không phải do lỗi của Zone mà chỉ là bạn đang cố gắng hiểu điều gì đó phức tạp đòi hỏi sự tập trung. Có một số giải pháp cho điều này.

Ghép nối có thể rất hữu ích như một cách để đối phó với sự gián đoạn. Đối tác trong cặp của bạn có thể nắm được bối cảnh của vấn đề trong khi bạn giải quyết một cuộc gọi điện thoại hoặc một câu hỏi từ đồng nghiệp. Khi bạn quay lại với người bạn đời của mình, anh ấy nhanh chóng giúp bạn xây dựng lại bối cảnh tinh thần mà bạn đã có trước khi bị gián đoạn.
TDD là một trợ giúp lớn khác. Nếu bạn có một bài kiểm tra không đạt, bài kiểm tra đó sẽ giữ được bối cảnh của bạn đang ở đâu. Bạn có thể quay lại nó sau khi bị gián đoạn và tiếp tục làm cho bài kiểm tra thất bại đó vượt qua.
Cuối cùng, tất nhiên sẽ có những gián đoạn khiến bạn mất tập trung và mất thời gian. Khi chúng xảy ra, hãy nhớ rằng lần sau, bạn có thể là người cần phải ngắt lời người khác. Vì vậy, thái độ chuyên nghiệp là một thái độ lịch sự sẵn sàng giúp đỡ.

### WRITER’S BLOCK
Đôi khi mã không đến. Tôi đã để điều này xảy ra với tôi và tôi đã thấy nó xảy ra với những người khác. Bạn ngồi tại máy trạm của mình và không có gì xảy ra.
Thường thì bạn sẽ tìm công việc khác để làm. Bạn sẽ đọc email. Bạn sẽ đọc các tweet. Bạn sẽ xem qua sách, lịch biểu hoặc tài liệu. Bạn sẽ gọi các cuộc họp. Bạn sẽ bắt đầu cuộc trò chuyện với những người khác. Bạn sẽ làm bất cứ điều gì để bạn không phải đối mặt với máy trạm đó và xem mã từ chối xuất hiện.

Nguyên nhân nào gây ra tắc nghẽn như vậy? Chúng tôi đã nói về nhiều yếu tố rồi.
Đối với tôi, một yếu tố chính khác là giấc ngủ. Nếu tôi không ngủ đủ giấc, tôi chỉ đơn giản là không thể viết mã. Những người khác lo lắng, sợ hãi và trầm cảm.
Thật kỳ lạ là có một giải pháp rất đơn giản. Nó hoạt động hầu như mọi lúc. Việc này rất dễ thực hiện và nó có thể cung cấp cho bạn động lực để viết nhiều mã. Giải pháp: Tìm một cặp đôi.
Thật kỳ lạ rằng điều này hoạt động tốt như thế nào. Ngay khi bạn ngồi xuống cạnh người khác, những vấn đề cản trở bạn sẽ tan biến. Có một sự thay đổi sinh lý diễn ra khi bạn làm việc với ai đó. Tôi không biết nó là gì, nhưng tôi chắc chắn có thể cảm nhận được. Có một số loại thay đổi hóa học trong não hoặc cơ thể của tôi giúp tôi vượt qua sự tắc nghẽn và giúp tôi đi lại.
Đây không phải là một giải pháp hoàn hảo. Đôi khi sự thay đổi kéo dài một hoặc hai giờ, chỉ sau đó là kiệt sức nghiêm trọng đến mức tôi phải rời khỏi người bạn cặp của mình và tìm một số lỗ hổng để phục hồi. Đôi khi, ngay cả khi ngồi với ai đó, tôi không thể làm gì hơn chỉ đồng ý với những gì người đó đang làm. Nhưng đối với tôi, phản ứng điển hình đối với việc ghép đôi là sự phục hồi động lực của tôi.

### CREATIVE INPUT
Có những việc khác tôi làm để ngăn chặn sự tắc nghẽn. Tôi đã học cách đây rất lâu rằng đầu ra sáng tạo phụ thuộc vào đầu vào sáng tạo.
Tôi đọc rất nhiều, và tôi đọc tất cả các loại tài liệu. Tôi đọc tài liệu về phần mềm, chính trị, sinh học, thiên văn học, vật lý, hóa học, toán học và nhiều hơn nữa. Tuy nhiên, tôi thấy rằng điều khiến bộ bơm đầu ra sáng tạo tốt nhất là khoa học viễn tưởng.

Đối với bạn, nó có thể là một cái gì đó khác. Có lẽ là một cuốn tiểu thuyết bí ẩn hay, hoặc thơ, hoặc thậm chí là một cuốn tiểu thuyết lãng mạn. Tôi nghĩ vấn đề thực sự là sự sáng tạo nuôi dưỡng sự sáng tạo. Ngoài ra còn có một yếu tố của chủ nghĩa thoát ly. Những giờ tôi dành ra khỏi những vấn đề thường ngày của mình, đồng thời được kích thích tích cực bởi những ý tưởng đầy thử thách và sáng tạo, dẫn đến một áp lực gần như không thể cưỡng lại để tự mình tạo ra thứ gì đó.

Không phải tất cả các hình thức đầu vào sáng tạo đều phù hợp với tôi. Xem TV thường không giúp tôi sáng tạo. Đi xem phim thì hay hơn nhưng chỉ một chút thôi. Nghe nhạc không giúp tôi tạo mã, nhưng giúp tôi tạo bản trình bày, bài nói và video. Trong tất cả các hình thức đầu vào sáng tạo, không gì phù hợp với tôi hơn là vở opera không gian cổ hay.

### DEBUGGING
Một trong những phiên gỡ lỗi tồi tệ nhất trong sự nghiệp của tôi xảy ra vào năm 1972. Các thiết bị đầu cuối kết nối với hệ thống kế toán của Teamsters từng bị đóng băng một hoặc hai lần mỗi ngày. Không có cách nào để buộc điều này xảy ra. Lỗi không thích bất kỳ thiết bị đầu cuối cụ thể nào hoặc bất kỳ ứng dụng cụ thể nào. Không quan trọng người dùng đã làm gì trước khi đóng băng. Một phút thiết bị đầu cuối hoạt động tốt, và phút tiếp theo nó bị đóng băng vô vọng.
Phải mất nhiều tuần để chẩn đoán vấn đề này. Trong khi đó các Teamster ngày càng khó chịu hơn. Mỗi khi có sự cố, người ở thiết bị đầu cuối đó sẽ phải ngừng hoạt động và đợi cho đến khi họ có thể điều phối tất cả những người dùng khác để hoàn thành nhiệm vụ của mình. Sau đó, họ sẽ gọi cho chúng tôi và chúng tôi sẽ khởi động lại. Đó là một cơn ác mộng.

Chúng tôi đã dành vài tuần đầu tiên chỉ để thu thập dữ liệu bằng cách phỏng vấn những người đã trải qua các đợt khóa. Chúng tôi sẽ hỏi họ xem họ đang làm gì vào thời điểm đó và họ đã làm gì trước đây. Chúng tôi đã hỏi những người dùng khác xem họ có nhận thấy bất kỳ điều gì trên thiết bị đầu cuối của họ tại thời điểm đóng băng hay không. Những cuộc phỏng vấn được thực hiện tất cả qua điện thoại vì các thiết bị đầu cuối được đặt tại trung tâm thành phố Chicago, trong khi chúng tôi làm việc 30 dặm về phía bắc trong những cánh đồng ngô.
Chúng tôi không có nhật ký, không có bộ đếm, không có trình gỡ lỗi. Quyền truy cập duy nhất của chúng tôi vào phần bên trong của hệ thống là đèn và công tắc bật tắt trên bảng điều khiển phía trước. Chúng tôi có thể dừng máy tính, và sau đó nhìn vào bộ nhớ từng từ một. Nhưng chúng tôi không thể thực hiện việc này trong hơn năm phút vì các Đội viên cần sao lưu hệ thống của họ.

Chúng tôi đã dành vài ngày để viết một trình kiểm tra thời gian thực đơn giản có thể được vận hành từ loại viễn thông ASR-33 đóng vai trò là bảng điều khiển của chúng tôi. Với điều này, chúng tôi có thể nhìn trộm và tìm kiếm xung quanh bộ nhớ trong khi hệ thống đang chạy. Chúng tôi đã thêm các thông báo nhật ký được in trên teletype vào những thời điểm quan trọng. Chúng tôi đã tạo các bộ đếm trong bộ nhớ để đếm các sự kiện và ghi nhớ lịch sử trạng thái mà chúng tôi có thể kiểm tra với thanh tra. Và tất nhiên, tất cả những điều này phải được viết từ đầu trong trình lắp ráp và được kiểm tra vào buổi tối khi hệ thống không được sử dụng.

Các thiết bị đầu cuối đã được điều khiển gián đoạn. Các ký tự được gửi đến các thiết bị đầu cuối được giữ trong các bộ đệm tròn. Mỗi khi một cổng nối tiếp hoàn tất việc gửi một ký tự, một ngắt sẽ kích hoạt và ký tự tiếp theo trong bộ đệm tròn sẽ là
đã sẵn sàng để gửi. Cuối cùng, chúng tôi phát hiện ra rằng khi một thiết bị đầu cuối bị đóng băng là do ba biến quản lý bộ đệm tròn không đồng bộ. Chúng tôi không biết tại sao điều này lại xảy ra, nhưng ít nhất đó là một manh mối. Một nơi nào đó trong 5 KSLOC giám sát
có một lỗi đã xử lý sai một trong những con trỏ đó.

Kiến thức mới này cũng cho phép chúng tôi giải phóng các thiết bị đầu cuối theo cách thủ công! Chúng tôi có thể chọc các giá trị mặc định vào ba biến đó bằng trình kiểm tra và các thiết bị đầu cuối sẽ bắt đầu chạy lại một cách kỳ diệu. Cuối cùng, chúng tôi đã viết một bản hack nhỏ để xem xét tất cả các quầy để xem chúng có bị lệch và sửa chữa chúng. Lúc đầu, chúng tôi gọi ra bản hack đó bằng cách nhấn vào một công tắc ngắt người dùng đặc biệt trên bảng điều khiển phía trước bất cứ khi nào Nhóm nghiên cứu gọi điện để báo cáo sự cố. Sau đó, chúng tôi chỉ cần chạy tiện ích sửa chữa mỗi giây một lần.
Một tháng sau, vấn đề đóng băng đã không còn nữa, theo như những gì các Teamster lo ngại. Đôi khi một trong các thiết bị đầu cuối của họ sẽ tạm dừng trong khoảng nửa giây hoặc lâu hơn, nhưng ở tốc độ cơ bản là 30 ký tự mỗi giây, dường như không ai nhận ra.
Nhưng tại sao các quầy lại bị lệch? Tôi mười chín tuổi và quyết tâm tìm hiểu.
Mã giám sát được viết bởi Richard, người đã học đại học. Không ai trong số chúng tôi quen thuộc với mã đó bởi vì Richard đã rất sở hữu nó. Mã đó là của anh ấy và chúng tôi không được phép biết nó. Nhưng bây giờ Richard đã ra đi, vì vậy tôi thoát ra khỏi danh sách dày hàng inch và bắt đầu xem qua từng trang.

Hàng đợi vòng tròn trong hệ thống đó chỉ là cấu trúc dữ liệu FIFO, tức là hàng đợi. Các chương trình ứng dụng đã đẩy các ký tự vào một đầu của hàng đợi cho đến khi hàng đợi đầy. Các đầu ngắt sẽ xuất hiện các ký tự ở đầu kia của hàng đợi khi máy in đã sẵn sàng cho chúng. Khi hàng đợi trống, máy in sẽ dừng. Lỗi của chúng tôi khiến các ứng dụng nghĩ rằng hàng đợi đã đầy, nhưng lại khiến các đầu ngắt nghĩ rằng hàng đợi trống.
Các đầu ngắt chạy trong một “luồng” khác với tất cả các mã khác. Vì vậy các bộ đếm và biến được thao tác bởi cả đầu ngắt và mã khác phải được bảo vệ khỏi cập nhật đồng thời. Trong trường hợp của chúng tôi, điều đó có nghĩa là tắt các ngắt xung quanh bất kỳ mã nào thao tác ba biến đó. Khi tôi ngồi xuống với mã đó, tôi biết rằng tôi đang tìm kiếm một nơi nào đó trong mã đã chạm vào các biến nhưng không vô hiệu hóa các ngắt trước.

Tất nhiên, ngày nay, chúng tôi sẽ sử dụng rất nhiều công cụ mạnh mẽ theo ý mình để tìm tất cả các vị trí mà mã đã chạm vào các biến đó. Trong vài giây, chúng tôi sẽ biết mọi dòng mã đã chạm vào chúng. Trong vòng vài phút, chúng tôi sẽ biết cái nào
đã không vô hiệu hóa các ngắt. Nhưng đây là năm 1972, và tôi không có bất kỳ công cụ nào như vậy. Những gì tôi có là đôi mắt của tôi.
Tôi nghiền ngẫm từng trang của mã đó, tìm kiếm các biến. Thật không may, các biến đã được sử dụng ở khắp mọi nơi. Gần như mọi trang đều chạm vào chúng theo cách này hay cách khác. Nhiều người trong số các tham chiếu đó đã không vô hiệu hóa các ngắt vì chúng là các tham chiếu chỉ đọc và do đó vô hại. Vấn đề là, trong trình hợp dịch cụ thể đó, không có cách nào tốt để biết liệu một tham chiếu chỉ được đọc mà không tuân theo logic của mã. Bất cứ khi nào một biến được đọc, nó sau này có thể được cập nhật và lưu trữ. Và nếu điều đó xảy ra trong khi kích hoạt ngắt, các biến có thể bị hỏng.
Tôi đã mất nhiều ngày học tập căng thẳng, nhưng cuối cùng tôi đã tìm thấy nó. Ở đó, ở giữa đoạn mã, là một nơi mà một trong ba biến đang được cập nhật trong khi các ngắt được kích hoạt.
Tôi đã làm toán. Lỗ hổng bảo mật dài khoảng hai micro giây. Có một tá thiết bị đầu cuối đang chạy ở tốc độ 30 cps, vì vậy cứ sau 3 ms lại có một ngắt. Với kích thước của trình giám sát và tốc độ xung nhịp của CPU, chúng tôi dự kiến ​​sẽ đóng băng lỗ hổng này một hoặc hai lần một ngày. Chơi lô tô!
Tất nhiên, tôi đã khắc phục sự cố, nhưng không bao giờ có đủ can đảm để tắt tính năng hack tự động kiểm tra và sửa các quầy. Cho đến ngày nay, tôi không tin là không có lỗ hổng nào khác.

### DEBUGGING TIME
Vì một số lý do mà các nhà phát triển phần mềm không coi thời gian gỡ lỗi là thời gian viết mã. Họ nghĩ về thời gian gỡ lỗi như một cuộc gọi của tự nhiên, một cái gì đó t

điều đó chỉ cần được thực hiện. Nhưng thời gian gỡ lỗi cũng tốn kém đối với doanh nghiệp như thời gian viết mã, và do đó, bất cứ điều gì chúng ta có thể làm để tránh hoặc giảm bớt nó đều tốt.
Ngày nay, tôi dành ít thời gian hơn để gỡ lỗi so với cách đây mười năm. Tôi chưa đo lường sự khác biệt, nhưng tôi tin rằng đó là hệ số mười. Tôi đã đạt được mức giảm thực sự triệt để trong thời gian gỡ lỗi bằng cách áp dụng thực hành Kiểm tra
Phát triển theo định hướng (TDD), mà chúng ta sẽ thảo luận trong một chương khác. Cho dù bạn áp dụng TDD hoặc một số kỷ luật khác có hiệu quả như nhau, thì bạn là một chuyên gia có trách nhiệm giảm thời gian gỡ lỗi càng gần
về 0 như bạn có thể nhận được. Rõ ràng số 0 là một mục tiêu tiệm cận, nhưng nó vẫn là mục tiêu.
Các bác sĩ không muốn mở lại bệnh nhân để sửa chữa điều gì đó họ đã làm sai. Các luật sư không muốn thử lại các trường hợp mà họ đã trả lời. Một bác sĩ hoặc luật sư làm điều đó quá thường xuyên sẽ không được coi là chuyên nghiệp. Tương tự như vậy, một nhà phát triển phần mềm
người tạo ra nhiều lỗi đang hành động thiếu chuyên nghiệp

### PACING YOUR SELF
Phát triển phần mềm là một cuộc chạy marathon, không phải chạy nước rút. Bạn không thể chiến thắng cuộc đua bằng cách cố gắng chạy nhanh nhất có thể ngay từ đầu. Bạn giành chiến thắng bằng cách bảo toàn tài nguyên của mình và điều chỉnh tốc độ của bản thân. Một vận động viên marathon chăm sóc cơ thể của mình cả trước và trong cuộc đua. Các lập trình viên chuyên nghiệp bảo tồn năng lượng và sự sáng tạo của họ với sự cẩn thận.

### KNOW WHEN TO WALK AWAY
Không thể về nhà cho đến khi bạn giải quyết được vấn đề này? Ồ vâng, bạn có thể, và có lẽ bạn nên làm như vậy! Sáng tạo và trí thông minh là trạng thái thoáng qua của tâm trí. Khi bạn mệt mỏi, họ bỏ đi. Nếu sau đó, bạn đập bộ não không hoạt động của mình hàng giờ đồng hồ sau đêm khuya cố gắng giải quyết một vấn đề, bạn sẽ đơn giản làm cho mình nhiều hơn
mệt mỏi và giảm cơ hội rằng vòi hoa sen, hoặc xe hơi, sẽ giúp bạn giải quyết vấn đề.
Khi bạn bế tắc, khi bạn mệt mỏi, hãy thư giãn một lúc. Cung cấp cho tiềm thức sáng tạo của bạn một vết nứt trước vấn đề. Bạn sẽ hoàn thành được nhiều việc hơn trong thời gian ngắn hơn và ít nỗ lực hơn nếu bạn cẩn thận với nguồn lực của mình. Đánh giá bản thân và nhóm của bạn. Tìm hiểu các mẫu sáng tạo và thông minh của bạn, và tận dụng chúng thay vì làm việc chống lại chúng.

### DRIVE HOME
Một nơi mà tôi đã giải quyết được một số vấn đề là chiếc xe của tôi trên đường đi làm về. Lái xe đòi hỏi rất nhiều nguồn lực trí óc. Bạn phải dành đôi mắt, đôi tay và phần trí óc của mình cho nhiệm vụ; do đó, bạn phải thoát khỏi những rắc rối trong công việc. Có điều gì đó về sự thảnh thơi cho phép tâm trí bạn tìm kiếm các giải pháp theo một cách khác và sáng tạo hơn.

### SHOWER
Tôi đã giải quyết được vô số vấn đề trong phòng tắm. Có lẽ tia nước đó vào sáng sớm đã đánh thức tôi và giúp tôi xem lại tất cả
giải pháp mà bộ não của tôi nghĩ ra khi tôi đang ngủ.
Khi bạn đang giải quyết một vấn đề, đôi khi bạn đến gần vấn đề đó đến mức bạn không thể nhìn thấy tất cả các tùy chọn. Bạn bỏ lỡ những giải pháp thanh lịch bởi vì phần sáng tạo trong tâm trí của bạn bị đè nén bởi cường độ tập trung của bạn. Đôi khi cách tốt nhất để giải quyết một vấn đề là về nhà, ăn tối, xem TV, đi ngủ, và sau đó thức dậy vào sáng hôm sau và đi tắm.

### LATE 
Bạn sẽ bị trễ. Nó xảy ra tốt nhất của chúng tôi. Nó xảy ra với những người tận tâm nhất trong chúng ta. Đôi khi chúng ta chỉ ước tính của mình và kết thúc muộn. Mẹo để quản lý việc đi trễ là phát hiện sớm và minh bạch. Trường hợp xấu nhất xảy ra khi bạn tiếp tục nói với mọi người, cho đến cuối cùng, rằng bạn sẽ đến đúng giờ — và sau đó khiến họ thất vọng. Đừng làm điều này. Thay vào đó, hãy thường xuyên đo lường sự tiến bộ của bạn so với mục tiêu và đưa ra ba4
ngày kết thúc dựa trên thực tế: trường hợp tốt nhất, trường hợp danh nghĩa và trường hợp xấu nhất. Hãy trung thực nhất có thể về cả ba cuộc hẹn hò. Đừng kết hợp hy vọng vào ước tính của bạn!
Trình bày tất cả ba con số cho nhóm của bạn và các bên liên quan. Cập nhật những con số này hàng ngày.

### HOPE
Điều gì sẽ xảy ra nếu những con số này cho thấy bạn có thể bỏ lỡ thời hạn? Ví dụ: giả sử 10 ngày nữa sẽ có triển lãm thương mại và chúng tôi cần có sản phẩm của mình tại đó.
Nhưng cũng giả sử rằng ước tính ba con số của bạn cho tính năng bạn đang làm việc là 8/12/20.
Đừng hy vọng rằng bạn có thể hoàn thành tất cả trong mười ngày! Hy vọng là kẻ giết người trong dự án. Hy vọng phá hủy lịch trình và hủy hoại danh tiếng. Hy vọng sẽ khiến bạn gặp rắc rối sâu sắc. Nếu triển lãm thương mại diễn ra trong mười ngày và ước tính danh nghĩa của bạn là 12, bạn sẽ không thực hiện được. Đảm bảo rằng nhóm và các bên liên quan hiểu rõ tình hình và không bỏ cuộc cho đến khi có kế hoạch dự phòng. Đừng để bất kỳ ai khác có hy vọng.

### RUSHING 
Điều gì sẽ xảy ra nếu người quản lý của bạn ngồi xuống và yêu cầu bạn cố gắng hoàn thành thời hạn?
Điều gì sẽ xảy ra nếu người quản lý của bạn khăng khăng rằng bạn “làm những gì cần làm”? Giữ theo ước tính của bạn! Ước tính ban đầu của bạn chính xác hơn bất kỳ thay đổi nào bạn thực hiện Có nhiều điều về điều này trong chương Ước tính.
sếp của bạn đang đối đầu với bạn. Hãy nói với sếp của bạn rằng bạn đã cân nhắc các lựa chọn (vì bạn có) và cách duy nhất để cải thiện lịch trình là giảm phạm vi. Đừng để bị cám dỗ vội vàng.
Khốn thay cho nhà phát triển kém cỏi chịu áp lực và đồng ý cố gắng hoàn thành thời hạn. Nhà phát triển đó sẽ bắt đầu sử dụng các phím tắt và làm việc thêm giờ với hy vọng vô vọng sẽ tạo ra một điều kỳ diệu. Đây là một công thức cho thảm họa vì nó mang lại cho bạn, nhóm của bạn và các bên liên quan của bạn hy vọng sai lầm. Nó cho phép mọi người tránh phải đối mặt với vấn đề và trì hoãn các quyết định khó khăn cần thiết.
Không có cách nào để vội vàng. Bạn không thể tự tạo mã nhanh hơn. Bạn không thể bắt mình giải quyết vấn đề nhanh hơn. Nếu bạn cố gắng, bạn sẽ chỉ làm chậm bản thân và tạo ra một mớ hỗn độn khiến những người khác cũng chậm lại.
Vì vậy, bạn phải trả lời sếp, nhóm của bạn và các bên liên quan bằng cách tước đi hy vọng của họ.

### OVERTIME
Vì vậy, sếp của bạn nói, “Điều gì sẽ xảy ra nếu bạn làm thêm hai giờ một ngày? Nếu bạn làm việc vào thứ Bảy thì sao? Cố lên, chỉ cần có một cách dành đủ giờ để hoàn thành tính năng đúng thời gian. "
Làm thêm có thể làm việc, và đôi khi nó là cần thiết. Đôi khi bạn có thể tạo ra một ngày không thể khác bằng cách đặt một số ngày mười giờ và một hoặc hai ngày thứ Bảy. Nhưng điều này rất rủi ro. Bạn không có khả năng hoàn thành thêm 20% công việc bằng cách làm thêm 20% giờ. Hơn nữa, thời gian làm thêm chắc chắn sẽ không thành công nếu nó kéo dài hơn hai hoặc ba tuần. Vì vậy, bạn không nên đồng ý làm thêm giờ trừ khi 
(1) bạn có đủ khả năng cá nhân
(2) thời gian ngắn hạn, hai tuần hoặc ít hơn
(3) sếp của bạn có kế hoạch dự phòng trong trường hợp nỗ lực làm thêm không thành công.
Tiêu chí cuối cùng đó là một sự phá vỡ thỏa thuận. Nếu sếp của bạn không thể nói rõ cho bạn biết ông ấy sẽ làm gì nếu nỗ lực làm thêm giờ không thành công, thì bạn không nên đồng ý làm thêm giờ.

### FALSE DELIVERY
Trong số tất cả những hành vi thiếu chuyên nghiệp mà một lập trình viên có thể mắc phải, có lẽ điều tồi tệ nhất là nói rằng bạn đã hoàn thành khi bạn biết mình chưa làm. Đôi khi đây chỉ là một lời nói dối công khai và điều đó đã đủ tệ. Nhưng trường hợp tối nghĩa hơn rất nhiều là khi chúng ta cố gắng hợp lý hóa một định nghĩa mới về “đã xong”. Chúng tôi tự thuyết phục mình rằng chúng tôi đã làm đủ và chuyển sang nhiệm vụ tiếp theo. Chúng tôi hợp lý hóa
rằng bất kỳ công việc nào còn lại có thể được giải quyết sau khi chúng tôi có thêm thời gian.

Đây là một thực hành dễ lây lan. Nếu một lập trình viên làm điều đó, những người khác sẽ thấy và làm theo. Một trong số họ sẽ mở rộng định nghĩa “đã hoàn thành” hơn nữa, và những người khác sẽ áp dụng định nghĩa mới. Tôi đã thấy điều này bị đưa đến cực điểm khủng khiếp. Một trong những khách hàng của tôi thực sự đã định nghĩa “hoàn thành” là “đăng ký”. Mật mã
thậm chí không cần phải biên dịch. Rất dễ dàng để được “hoàn thành” nếu không có việc gì phải làm! Khi một đội rơi vào bẫy này, các nhà quản lý nghe thấy rằng mọi thứ vẫn ổn. Tất cả các báo cáo trạng thái cho thấy rằng tất cả mọi người đều đúng giờ. Nó giống như những người mù đi dã ngoại trên đường ray: Không ai nhìn thấy chuyến tàu chở hàng của những công việc dở dang đang đè nặng lên họ cho đến khi quá muộn.

### DEFINE DONE
Bạn tránh được vấn đề phân phối sai bằng cách tạo ra một định nghĩa độc lập về “đã hoàn thành”. Cách tốt nhất để làm điều này là yêu cầu các nhà phân tích kinh doanh và người kiểm tra của bạn tạo ra các bài kiểm tra chấp nhận tự động phải vượt qua trước khi bạn có thể nói rằng bạn đã hoàn thành. Các bài kiểm tra này phải được viết bằng ngôn ngữ kiểm tra như FitNesse,
Selenium, RobotFX, Cucumber, v.v. Các bên liên quan và nhân viên kinh doanh phải hiểu được các bài kiểm tra và phải được thực hiện thường xuyên.

### HELP
Lập trình thật khó. Bạn càng trẻ càng ít tin vào điều này. Rốt cuộc, đó chỉ là một loạt các câu lệnh if và while. Nhưng khi bạn có được kinh nghiệm, bạn bắt đầu nhận ra rằng cách bạn kết hợp các câu lệnh if và while đó là
quan trọng. Bạn không thể chỉ tập hợp chúng lại với nhau và hy vọng điều tốt nhất. Thay vào đó, bạn phải cẩn thận phân chia hệ thống thành các đơn vị nhỏ dễ hiểu và càng ít liên quan đến nhau càng tốt — và điều đó thật khó.
Thực tế, việc lập trình khó đến mức vượt quá khả năng của một người. Bất kể bạn có kỹ năng như thế nào, bạn chắc chắn sẽ được hưởng lợi từ những suy nghĩ và ý tưởng của một lập trình viên khác.

### HELPING OTHERS
Vì điều này, các lập trình viên có trách nhiệm sẵn sàng giúp đỡ lẫn nhau. Vi phạm đạo đức nghề nghiệp nếu tự cô lập mình trong buồng hoặc văn phòng và từ chối yêu cầu của người khác. Công việc của bạn không quá quan trọng nên bạn không thể cho người khác mượn chút thời gian của mình. Thật vậy, là một chuyên gia, bạn rất vinh dự được cung cấp sự giúp đỡ đó bất cứ khi nào cần.
Điều này không có nghĩa là bạn không cần thời gian ở một mình. Tất nhiên là bạn có. Nhưng bạn phải công bằng và lịch sự về điều đó. Ví dụ, bạn có thể cho biết rằng trong khoảng thời gian từ 10 giờ sáng đến trưa bạn không nên bị làm phiền, nhưng từ 1 giờ chiều đến 3 giờ chiều thì cửa của bạn vẫn mở.
Bạn nên có ý thức v
ề tình trạng của đồng đội của bạn. Nếu bạn thấy ai đó có vẻ như đang gặp khó khăn, bạn nên đề nghị giúp đỡ. Bạn có thể sẽ khá ngạc nhiên về hiệu quả sâu sắc mà sự giúp đỡ của bạn có thể mang lại. Không phải bạn thông minh hơn người khác quá nhiều mà chỉ là quan điểm mới mẻ có thể là chất xúc tác sâu sắc để giải quyết vấn đề.
Khi bạn giúp ai đó, hãy ngồi xuống và viết mã cùng nhau. Lên kế hoạch dành phần tốt hơn của một giờ hoặc hơn. Có thể mất ít thời gian hơn, nhưng bạn không muốn tỏ ra vội vàng. Hãy cam kết với nhiệm vụ và nỗ lực hết mình. Bạn có thể sẽ ra đi khi học được nhiều hơn những gì bạn đã cho.

### BEING HELP
Khi ai đó đề nghị giúp đỡ bạn, hãy hài lòng về điều đó. Hãy chấp nhận sự giúp đỡ một cách biết ơn và cống hiến hết mình cho sự giúp đỡ đó. Không bảo vệ sân cỏ của bạn. Đừng thúc ép
sự giúp đỡ đi vì bạn đang ở dưới họng súng. Cho nó ba mươi phút hoặc lâu hơn. Nếu đến thời điểm đó mà người đó không thực sự giúp đỡ bạn nhiều như vậy thì bạn hãy lịch sự xin lỗi và kết thúc buổi làm việc bằng lời cảm ơn. Hãy nhớ rằng, bạn có vinh dự được đề nghị giúp đỡ, bạn cũng có vinh dự được nhận giúp đỡ.

Tìm hiểu cách yêu cầu giúp đỡ. Khi bạn gặp khó khăn, bối rối hoặc không thể giải quyết vấn đề của mình, hãy nhờ ai đó giúp đỡ. Nếu bạn đang ngồi trong phòng tập thể, bạn có thể chỉ cần ngồi lại và nói, "Tôi cần một số trợ giúp." Nếu không, hãy sử dụng yammer, twitter hoặc email, hoặc điện thoại trên bàn của bạn. Gọi sự giúp đỡ. Một lần nữa, đây là vấn đề đạo đức nghề nghiệp. Sẽ không chuyên nghiệp nếu bạn vẫn bị mắc kẹt khi sự trợ giúp có thể dễ dàng tiếp cận.

Vào lúc này, bạn có thể mong đợi tôi bật lên một bản hợp ca của Kumbaya trong khi những chú thỏ mờ ảo nhảy lên lưng kỳ lân và tất cả chúng ta vui vẻ bay qua cầu vồng của hy vọng và thay đổi. Không, không hoàn toàn. Bạn thấy đấy, các lập trình viên có xu hướng kiêu ngạo, hướng nội tự thu mình. Chúng tôi không tham gia vào lĩnh vực kinh doanh này vì chúng tôi thích mọi người. Hầu hết chúng ta tham gia vào lập trình vì chúng ta thích tập trung sâu vào
trên những điều vụn vặt vô trùng, tung hứng đồng thời rất nhiều khái niệm và nói chung chứng minh cho bản thân rằng chúng ta có bộ não có kích thước như một hành tinh, trong khi không phải tiếp xúc với những phức tạp lộn xộn của người khác.

Vâng, đây là một khuôn mẫu. Vâng, đó là sự tổng quát hóa với nhiều ngoại lệ. Nhưng thực tế là các lập trình viên không có xu hướng trở thành cộng tác viên. Tuy nhiên, sự hợp tác là rất quan trọng để lập trình hiệu quả. Do đó, đối với nhiều người trong chúng ta sự cộng tác
không phải là một bản năng, chúng tôi yêu cầu các kỷ luật thúc đẩy chúng tôi cộng tác.

### MENTORING
Tôi có cả một chương về chủ đề này ở phần sau của cuốn sách. Bây giờ, tôi xin nói một cách đơn giản rằng việc đào tạo các lập trình viên ít kinh nghiệm hơn là trách nhiệm của những người có nhiều kinh nghiệm hơn. Các khóa đào tạo không cắt giảm nó. Sách không cắt nó.
Không gì có thể đưa một nhà phát triển phần mềm trẻ đạt hiệu suất cao nhanh hơn. Điều này đúng với nam giới hơn phụ nữ. Tôi đã có một cuộc trò chuyện tuyệt vời với @desi (Desi McAdam, người sáng lập DevChix) về động lực thúc đẩy các lập trình viên nữ. Tôi nói với cô ấy rằng khi tôi có một chương trình hoạt động, nó giống như giết chết con thú lớn. Cô ấy nói với tôi rằng đối với cô ấy và những người phụ nữ khác mà cô ấy đã nói chuyện, hành động viết mã là một hành động nuôi dưỡng sự sáng tạo.
hơn động lực của chính mình và sự cố vấn hiệu quả của các tiền bối. Do đó, một lần nữa, vấn đề đạo đức nghề nghiệp đối với các lập trình viên cao cấp là dành thời gian để dẫn dắt các lập trình viên trẻ dưới sự dìu dắt của họ và kèm cặp họ. 
Đồng thời, những lập trình viên trẻ tuổi đó có nhiệm vụ chuyên nghiệp là phải tìm kiếm sự cố vấn như vậy từ các tiền bối của họ.