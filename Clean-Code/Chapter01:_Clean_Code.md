# Chapter 01: Clean Code 
Bạn đang đọc cuốn sách này vì hai lý do. Đầu tiên, bạn là một lập trình viên. Thứ hai, bạn muốn trở thành một lập trình viên giỏi hơn. Tốt. Chúng tôi cần những lập trình viên giỏi hơn.

Đây là một cuốn sách về lập trình hay. Nó chứa đầy mã. Chúng ta sẽ xem xét mã từ mọi hướng khác nhau. Chúng tôi sẽ nhìn xuống nó từ trên xuống, từ dưới lên trên và nhìn qua nó từ trong ra ngoài. Vào thời điểm chúng tôi hoàn thành, chúng tôi sẽ biết một
rất nhiều về mã. Hơn nữa, chúng tôi sẽ có thể phân biệt được mã tốt và mã xấu. Chúng tôi sẽ biết cách viết mã tốt. Và chúng tôi sẽ biết cách chuyển đổi mã xấu thành
mã tốt.

## There will be code 
Người ta có thể tranh luận rằng một cuốn sách về mã bằng cách nào đó đã đi sau thời đại - mã đó không còn là vấn đề nữa; mà chúng ta nên quan tâm đến các mô hình và yêu cầu thay thế.
Thật vậy, một số người đã gợi ý rằng chúng ta sắp kết thúc mã. Điều đó sớm tất cả mã sẽ được tạo ra thay vì được viết. Đơn giản là những người lập trình đó sẽ không cần thiết vì những người bận rộn sẽ tạo ra các chương trình từ các thông số kỹ thuật.
Vô lý! Chúng tôi sẽ không bao giờ loại bỏ mã, bởi vì mã đại diện cho các chi tiết của các yêu cầu. Ở một mức độ nào đó, những chi tiết đó không thể bị bỏ qua hoặc trừu tượng hóa; chúng phải được chỉ định. Và xác định các yêu cầu chi tiết đến mức máy có thể thực hiện chúng là
lập trình. Một đặc điểm kỹ thuật như vậy là mã.
Tôi hy vọng rằng mức độ trừu tượng của các ngôn ngữ của chúng ta sẽ tiếp tục tăng lên. Tôi cũng hy vọng rằng số lượng ngôn ngữ dành riêng cho miền sẽ tiếp tục tăng. Đây sẽ là một điều tốt. Nhưng nó sẽ không loại bỏ mã. Thật vậy, tất cả các thông số kỹ thuật được viết bằng ngôn ngữ cấp cao hơn và theo miền cụ thể sẽ là mã! Nó vẫn sẽ cần
chặt chẽ, chính xác, trang trọng và chi tiết đến mức máy móc có thể hiểu và thực thi nó.
Những người nghĩ rằng một ngày nào đó mã sẽ biến mất cũng giống như các nhà toán học hy vọng một ngày nào đó sẽ khám phá ra một toán học không cần phải chính thức. Họ hy vọng rằng một ngày nào đó chúng ta sẽ khám phá ra cách tạo ra những cỗ máy có thể làm những gì chúng ta muốn
hơn những gì chúng tôi nói. Những cỗ máy này sẽ phải có khả năng hiểu chúng ta đến mức chúng có thể chuyển những nhu cầu được chỉ định một cách mơ hồ thành những chương trình thực thi hoàn hảo đáp ứng chính xác những nhu cầu đó.
Điều này sẽ không bao giờ xảy ra. Ngay cả con người, với tất cả trực giác và óc sáng tạo của mình, cũng không thể tạo ra những hệ thống thành công từ những cảm giác mơ hồ của khách hàng.
Thật vậy, nếu kỷ luật về đặc tả yêu cầu đã dạy chúng ta bất cứ điều gì, thì đó là các yêu cầu được chỉ định rõ ràng cũng chính thức như mã và có thể hoạt động như các bài kiểm tra thực thi của mã đó!
Hãy nhớ rằng mã thực sự là ngôn ngữ mà cuối cùng chúng ta thể hiện các yêu cầu. Chúng tôi có thể tạo các ngôn ngữ gần với yêu cầu hơn. Chúng tôi có thể tạo công cụ giúp chúng tôi phân tích cú pháp và tập hợp các yêu cầu đó thành các cấu trúc chính thức. Nhưng chúng tôi sẽ
không bao giờ loại bỏ độ chính xác cần thiết — vì vậy sẽ luôn có mã.


### Bad Code 
Gần đây tôi đã đọc lời tựa của Kent Beck’s
cuốn sách Các mô hình thực hiện. 1 Anh ấy nói, “. . . điều này
cuốn sách dựa trên một tiền đề khá mong manh: rằng
vấn đề mã tốt. . . . ” Một tiền đề mong manh? Tôi không
đồng ý! Tôi nghĩ tiền đề đó là một trong những tiền đề
mạnh mẽ, được hỗ trợ và quá tải của tất cả các
tiếng ồn trong nghề của chúng tôi (và tôi nghĩ Kent biết điều đó). Chúng tôi
biết mã tốt quan trọng vì chúng tôi phải
đối phó quá lâu với sự thiếu hụt của nó.
Tôi biết một công ty, vào cuối những năm 80,
đã viết một ứng dụng giết người. Nó rất phổ biến và rất nhiều
các chuyên gia đã mua và sử dụng nó. Nhưng sau đó
chu kỳ phát hành bắt đầu kéo dài. Lỗi không
sửa chữa từ bản phát hành này sang bản tiếp theo. Thời gian tải
tăng lên và sự cố tăng lên. Tôi nhớ ngày tôi
tắt sản phẩm trong sự thất vọng và không bao giờ
đã sử dụng nó một lần nữa. Công ty đã ngừng kinh doanh
một thời gian ngắn sau đó.
Hai thập kỷ sau, tôi gặp một trong những nhân viên đầu tiên của công ty đó và hỏi anh ta chuyện gì đã xảy ra. Câu trả lời xác nhận nỗi sợ hãi của tôi. Họ đã vội vàng đưa sản phẩm ra thị trường và đã tạo ra một mớ hỗn độn về mã. Khi họ thêm ngày càng nhiều tính năng, mã ngày càng trở nên tồi tệ hơn cho đến khi họ không thể quản lý được nữa. Đó là mã xấu đã đưa công ty đi xuống.
Bạn đã bao giờ bị cản trở đáng kể bởi mã xấu? Nếu bạn là một lập trình viên có kinh nghiệm thì bạn đã cảm thấy trở ngại này nhiều lần. Thật vậy, chúng tôi có một cái tên cho nó. Chúng tôi gọi nó là lội nước. Chúng tôi lội qua mã xấu. Chúng tôi khẩu hiệu thông qua một mớ hỗn độn
brambles và cạm bẫy tiềm ẩn. Chúng ta đấu tranh để tìm ra con đường của mình, hy vọng vào một số gợi ý, một số manh mối, về những gì đang xảy ra; nhưng tất cả những gì chúng ta thấy ngày càng nhiều mã vô tri.
Tất nhiên bạn đã bị cản trở bởi mã xấu. Vậy thì - tại sao bạn lại viết nó? Bạn có cố gắng đi nhanh không? Bạn có đang vội không? Có lẽ vậy. Có lẽ bạn cảm thấy rằng bạn không có thời gian để làm tốt công việc; rằng sếp của bạn sẽ tức giận với bạn nếu bạn dành thời gian để dọn dẹp mã của mình. Có lẽ bạn chỉ cảm thấy mệt mỏi khi làm việc với chương trình này và
muốn nó kết thúc. Hoặc có thể bạn đã xem xét tồn đọng của những thứ khác mà bạn cần phải hoàn thành và nhận ra rằng bạn cần kết hợp mô-đun này lại với nhau để có thể chuyển sang phần tiếp theo. Tất cả chúng ta đã làm được.
Tất cả chúng tôi đã xem xét mớ hỗn độn mà chúng tôi vừa tạo ra và sau đó đã chọn để nó sang một ngày khác. Tất cả chúng tôi đều cảm thấy nhẹ nhõm khi thấy chương trình lộn xộn của mình hoạt động và quyết định rằng làm việc lộn xộn còn hơn không. Tất cả chúng tôi đều nói rằng chúng tôi sẽ quay lại và dọn dẹp nó sau. Tất nhiên, trong những ngày đó, chúng tôi không biết luật của LeBlanc: Sau này không bao giờ bằng.

## The Total Cost of Owning a Mess 
Nếu bạn đã là một lập trình viên hơn hai hoặc ba năm, bạn có thể đã bị chậm lại đáng kể bởi mã lộn xộn của người khác. Nếu bạn đã là một lập trình viên lâu hơn hai hoặc ba năm, có thể bạn đã bị chậm lại bởi những đoạn mã lộn xộn.
Mức độ chậm lại có thể là đáng kể. Trong khoảng thời gian một hoặc hai năm, các nhóm tiến rất nhanh khi bắt đầu dự án có thể thấy mình đang di chuyển với tốc độ chóng mặt. Mỗi thay đổi mà họ thực hiện đối với mã sẽ phá vỡ hai hoặc ba phần khác của mã. Không
thay đổi là tầm thường. Mọi sự bổ sung hoặc sửa đổi đối với hệ thống đều yêu cầu phải “hiểu rõ” các điểm rối, xoắn và thắt nút để có thể thêm nhiều rối, xoắn và thắt nút hơn.
Theo thời gian, đống rác ngày càng lớn, sâu và cao đến mức họ không thể dọn dẹp được. Không có cách nào cả.
Khi tình trạng lộn xộn hình thành, năng suất của nhóm tiếp tục giảm, tiệm cận với con số không. Khi năng suất giảm, cấp quản lý sẽ làm điều duy nhất mà họ có thể làm được;
họ bổ sung thêm nhân viên vào dự án với hy vọng tăng năng suất. Nhưng nhân viên mới đó không thành thạo trong việc thiết kế hệ thống. Họ không biết sự khác biệt giữa thay đổi phù hợp với ý định thiết kế và thay đổi cản trở ý định thiết kế. Hơn nữa,
họ, và mọi người khác trong nhóm, đang phải chịu áp lực khủng khiếp để tăng năng suất. Vì vậy, tất cả chúng ngày càng tạo ra nhiều mớ hỗn độn hơn, khiến năng suất ngày càng tiến xa về con số không.
(Xem Hình 1-1.)

### The Grand Redesign in the Sky
Cuối cùng cả đội nổi dậy. Họ thông báo cho ban quản lý rằng họ không thể tiếp tục phát triển trong cơ sở mã đáng sợ này. Họ yêu cầu thiết kế lại. Ban lãnh đạo không muốn tiêu tốn nguồn lực vào việc thiết kế lại dự án hoàn toàn mới, nhưng họ không thể phủ nhận rằng hiệu suất là rất khủng khiếp. Cuối cùng, họ tuân theo yêu cầu của các nhà phát triển và cho phép
thiết kế lại lớn trên bầu trời.
Một đội hổ mới được chọn. Mọi người đều muốn tham gia nhóm này vì đây là một dự án về lĩnh vực xanh. Họ bắt đầu lại và tạo ra một thứ gì đó thực sự đẹp đẽ. Nhưng chỉ những người tốt nhất và sáng giá nhất mới được chọn cho đội hổ. Mọi người khác phải tiếp tục duy trì
hệ thống hiện tại.
Bây giờ hai đội đang trong một cuộc đua. Đội hổ phải xây dựng một hệ thống mới có thể làm được mọi thứ mà hệ thống cũ làm. Không chỉ vậy, họ phải theo kịp những thay đổi liên tục được thực hiện đối với hệ thống cũ. Quản lý sẽ không thay thế cũ
hệ thống cho đến khi hệ thống mới có thể làm mọi thứ mà hệ thống cũ làm.
Cuộc đua này có thể diễn ra trong một thời gian rất dài. Tôi đã thấy nó mất 10 năm. Và vào thời điểm hoàn thành, các thành viên ban đầu của đội hổ đã biến mất từ ​​lâu và các thành viên hiện tại đang yêu cầu thiết kế lại hệ thống mới vì nó quá lộn xộn.
Nếu bạn đã trải qua dù chỉ một phần nhỏ của câu chuyện tôi vừa kể, thì bạn đã biết rằng việc dành thời gian để giữ cho mã của bạn sạch sẽ không chỉ là hiệu quả về chi phí; đó là vấn đề sống còn trong nghề nghiệp.

### Attitude
Bạn đã bao giờ lội qua một đống lộn xộn đến mức mất hàng tuần để làm những việc đáng lẽ phải mất hàng giờ? Bạn đã thấy những gì đáng lẽ phải là thay đổi một dòng, được thực hiện thay thế trong hàng trăm mô-đun khác nhau? Những triệu chứng này đều quá phổ biến.
Tại sao điều này xảy ra với mã? Tại sao mã tốt lại nhanh chóng biến thành mã xấu? Chúng tôi có rất nhiều lời giải thích cho nó. Chúng tôi phàn nàn rằng các yêu cầu đã thay đổi theo cách cản trở thiết kế ban đầu. Chúng tôi than phiền vì lịch trình quá chặt chẽ để làm mọi thứ đúng. Chúng ta đổ lỗi cho những người quản lý ngu ngốc và những khách hàng không khoan dung và những kiểu tiếp thị vô dụng và chất khử trùng qua điện thoại. Nhưng lỗi, Dilbert thân mến, không phải ở các vì sao của chúng ta, mà là ở chính chúng ta.
Chúng tôi không chuyên nghiệp. Đây có thể là một viên thuốc đắng để nuốt. Làm thế nào mà lộn xộn này có thể là lỗi của chúng tôi? Còn các yêu cầu thì sao? Còn về lịch trình? Còn những người quản lý ngu ngốc và vô dụng thì sao
các loại tiếp thị? Họ không chịu một số trách nhiệm?
Không. Các nhà quản lý và nhà tiếp thị tìm kiếm chúng tôi để biết thông tin họ cần để đưa ra lời hứa và cam kết; và ngay cả khi họ không nhìn chúng ta, chúng ta cũng không nên ngại nói với họ những gì chúng ta nghĩ. Người dùng tìm đến chúng tôi để xác nhận cách các yêu cầu sẽ phù hợp với hệ thống. Các nhà quản lý dự án tìm đến chúng tôi để giúp đưa ra lịch trình. Chúng tôi đồng hành sâu sắc trong việc lập kế hoạch của dự án và chia sẻ rất nhiều về khả năng ứng phó cho bất kỳ thất bại nào; đặc biệt là nếu những thất bại đó liên quan đến mã xấu! "Nhưng chờ đã!" bạn nói. "Nếu tôi không làm theo những gì người quản lý của mình nói, tôi sẽ bị sa thải." Chắc là không.
Hầu hết các nhà quản lý muốn sự thật, ngay cả khi họ không hành động như vậy. Hầu hết các nhà quản lý muốn có mã tốt, ngay cả khi họ đang ám ảnh về lịch trình. Họ có thể bảo vệ lịch trình và yêu cầu với niềm đam mê; nhưng đó là công việc của họ. Nhiệm vụ của bạn là bảo vệ mã bằng
niềm đam mê.
Để lái xe về nhà, điều gì sẽ xảy ra nếu bạn là một bác sĩ và có một bệnh nhân yêu cầu bạn dừng tất cả việc rửa tay ngớ ngẩn để chuẩn bị cho cuộc phẫu thuật vì mất quá nhiều thời gian? 2 Rõ ràng bệnh nhân là ông chủ; và bác sĩ tuyệt đối nên từ chối
tuân thủ. Tại sao? Bởi vì bác sĩ biết nhiều hơn bệnh nhân về các nguy cơ dễ bị biến chứng và nhiễm trùng. Sẽ là không chuyên nghiệp (đừng bận tâm đến tội phạm) nếu bác sĩ tuân thủ bệnh nhân.
Vì vậy, việc các lập trình viên làm theo ý muốn của những người quản lý không hiểu những rủi ro của việc làm lộn xộn cũng là không chuyên nghiệp

### The Primal Conundrum
Các lập trình viên phải đối mặt với một câu hỏi hóc búa về các giá trị cơ bản. Tất cả các nhà phát triển với hơn một vài năm kinh nghiệm đều biết rằng những mớ hỗn độn trước đây làm chậm họ. Tuy nhiên, tất cả các nhà phát triển đều cảm thấy áp lực phải làm ra những mớ hỗn độn để đáp ứng thời hạn. Tóm lại, họ không mất thời gian để đi nhanh!
Các chuyên gia chân chính biết rằng phần thứ hai của câu hỏi hóc búa là sai. Bạn sẽ không thực hiện đúng thời hạn bằng cách làm cho lộn xộn. Thật vậy, tình trạng lộn xộn sẽ làm bạn chậm lại ngay lập tức, và
sẽ buộc bạn phải bỏ lỡ thời hạn. Cách duy nhất để hoàn thành thời hạn — cách duy nhất để đi nhanh — là luôn giữ cho mã sạch nhất có thể.


### The Art of Clean Code?
Giả sử bạn tin rằng mã lộn xộn là một trở ngại đáng kể. Giả sử rằng bạn chấp nhận rằng cách duy nhất để đạt được tốc độ nhanh là giữ cho mã của bạn sạch sẽ. Sau đó, bạn phải tự hỏi mình: "Làm cách nào để viết mã sạch?" Cố gắng viết mã sạch sẽ không tốt nếu bạn không biết nó là gì
nghĩa là mã phải sạch! Tin xấu là viết mã sạch giống như vẽ một bức tranh. Hầu hết chúng ta đều biết khi nào một bức tranh được vẽ đẹp hay xấu. Nhưng có thể phục hồi

### What Is Clean Code?
Có lẽ có rất nhiều định nghĩa đối với lập trình viên. Vì vậy, tôi đã hỏi một số lập trình viên nổi tiếng và có kinh nghiệm sâu sắc rằng họ nghĩ gì.

#### Bjarne Stroustrup, inventor of C++
#### and author of The C++ Programming
#### Language
Tôi thích mã của mình phải thanh lịch và hiệu quả. Các
logic nên đơn giản để làm cho nó khó
để lỗi ẩn, các phụ thuộc tối thiểu để
bảo trì dễ dàng, xử lý lỗi hoàn thành
theo một chiến lược rõ ràng và theo
hình thức gần với tối ưu để không bị cám dỗ
mọi người làm cho mã lộn xộn với unprinci-
cam kết tối ưu hóa. Mã sạch làm một việc
tốt.
Bjarne sử dụng từ "thanh lịch". Đó là
khá một từ! Từ điển trong MacBook ® của tôi
cung cấp các định nghĩa sau: làm hài lòng
duyên dáng và phong cách về ngoại hình hoặc cách thức; đẹp một cách khéo léo và đơn giản. Lưu ý sự nhấn mạnh của từ “làm hài lòng”. Rõ ràng Bjarne nghĩ rằng mã sạch sẽ dễ đọc. Đọc nó sẽ khiến bạn mỉm cười như một chiếc hộp nhạc được chế tác tốt hoặc thiết kế đẹp
ô tô sẽ.
Bjarne cũng đề cập đến hiệu quả - gấp đôi. Có lẽ điều này không làm chúng ta ngạc nhiên đến từ người phát minh ra C ++; nhưng tôi nghĩ có nhiều thứ hơn là mong muốn tuyệt đối về tốc độ.
Chu kỳ lãng phí là không phù hợp, họ không hài lòng. Và bây giờ hãy lưu ý từ mà Bjarne sử dụng để mô tả hậu quả của sự kém cỏi đó. Anh ấy sử dụng từ "cám dỗ". Có một sâu
sự thật ở đây. Mã xấu sẽ thúc đẩy mớ hỗn độn phát triển! Khi những người khác thay đổi mã xấu, họ có xu hướng làm cho nó tồi tệ hơn.
Thực dụng Dave Thomas và Andy Hunt nói điều này theo một cách khác. Họ đã sử dụng meta-phor của các cửa sổ bị hỏng. 3 Một tòa nhà với các cửa sổ bị vỡ trông như không ai quan tâm
nó. Vậy nên người khác đừng quan tâm nữa. Chúng cho phép nhiều cửa sổ bị hỏng hơn. Cuối cùng họ chủ động phá vỡ chúng. Họ làm bong tróc mặt tiền bằng những bức vẽ bậy và để rác thải thành đống. Một cửa sổ bị hỏng bắt đầu quá trình phân rã.
Bjarne cũng đề cập rằng việc xử lý lỗi phải được hoàn tất. Điều này dẫn đến việc chú ý đến chi tiết. Xử lý lỗi viết tắt chỉ là một cách tạo ra
gammers bóng trên các chi tiết. Rò rỉ bộ nhớ là một, các điều kiện chủng tộc vẫn khác.
Đặt tên không phù hợp nhưng một cách khác. Kết quả là mã sạch thể hiện sự chú ý đến từng chi tiết.
Bjarne kết thúc với khẳng định rằng mã sạch làm tốt một điều. Không phải ngẫu nhiên mà có rất nhiều nguyên tắc thiết kế phần mềm có thể được đúc kết thành lời khuyên đơn giản này. Nhà văn này đến nhà văn khác đã cố gắng truyền đạt suy nghĩ này. Mã lỗi cố gắng làm
quá nhiều, nó có ý định lộn xộn và mục đích không rõ ràng. Mã sạch được tập trung. Mỗi chức năng, mỗi lớp, mỗi mô-đun thể hiện một thái độ duy nhất vẫn hoàn toàn
không bị phân tán và không bị ô nhiễm bởi các chi tiết xung quanh.

#### Grady Booch, author of Object
#### Oriented Analysis and Design with
#### Applications
Mã sạch rất đơn giản và trực tiếp. Mã sạch
đọc như văn xuôi được viết tốt. Mã sạch không bao giờ
che khuất ý định của nhà thiết kế mà thay vào đó là đầy
trừu tượng rõ ràng và đường thẳng
kiểm soát.
Grady đưa ra một số điểm giống như
Bjarne, nhưng anh ấy có quan điểm về khả năng đọc. Tôi
đặc biệt thích quan điểm của anh ấy rằng mã sạch sẽ
đọc như văn xuôi được viết tốt. Nghĩ lại về một
cuốn sách thực sự hay mà bạn đã đọc. Hãy nhớ cách các từ biến mất để được thay thế
bằng hình ảnh! Nó giống như đang xem một bộ phim, phải không? Tốt hơn! Bạn đã nhìn thấy các nhân vật, bạn nghe thấy âm thanh, bạn trải nghiệm những điều kỳ diệu và hài hước.
Đọc mã sạch sẽ không bao giờ giống như đọc Chúa tể của những chiếc nhẫn. Tuy nhiên, phép ẩn dụ lít-ary không phải là một phép ẩn dụ xấu. Giống như một cuốn tiểu thuyết hay, mã sạch sẽ phơi bày rõ ràng mười lỗi trong vấn đề cần giải quyết. Nó sẽ xây dựng những căng thẳng đó lên cao trào và sau đó đưa ra 3. http://www.pragmaticprogrammer.com/booksellers/2004-12.html
www.it-ebooks.infoTổng chi phí sở hữu một tin nhắn
9 người đọc rằng “Aha! Tất nhiên!" khi các vấn đề và căng thẳng được giải quyết trong sự tiết lộ của một giải pháp rõ ràng.
Tôi thấy việc Grady sử dụng cụm từ “trừu tượng rõ ràng” là một oxymoron hấp dẫn!
Xét cho cùng, từ “sắc nét” gần như là một từ đồng nghĩa với “cụ thể”. Từ điển trên MacBook của tôi có định nghĩa sau về "sắc nét": dứt khoát nhanh chóng và thực tế, không chần chừ hoặc chi tiết không cần thiết. Mặc dù có vẻ giống nhau về nghĩa, những từ
mang một thông điệp mạnh mẽ. Mã của chúng tôi phải là vấn đề thực tế chứ không phải suy đoán.
Nó chỉ nên chứa những gì cần thiết. Độc giả của chúng tôi nên nhận thức rằng chúng tôi đã có quyết định.

#### “Big” Dave Thomas, founder
#### of OTI, godfather of the
#### Eclipse strategy
Mã sạch có thể được đọc và được nâng cao bởi
nhà phát triển khác với tác giả ban đầu của nó. Nó có
đơn vị và nghiệm thu. Nó có ý nghĩa
những cái tên. Nó cung cấp một cách thay vì nhiều
cách để làm một việc. Nó có ít depen-
các cơ quan, được xác định rõ ràng, và
cung cấp một API rõ ràng và tối thiểu. Mã phải được
biết chữ vì tùy thuộc vào ngôn ngữ, không phải tất cả
thông tin cần thiết có thể được thể hiện rõ ràng
chỉ trong mã.
Big Dave chia sẻ mong muốn của Grady về khả năng đọc được-
ity, nhưng với một bước ngoặt quan trọng. Dave khẳng định rằng
mã sạch giúp người khác dễ dàng nâng cao mã. Điều này có vẻ hiển nhiên, nhưng nó không thể được nhấn mạnh quá mức. Rốt cuộc, có một sự khác biệt giữa mã dễ đọc và mã dễ thay đổi.
Dave gắn kết sự sạch sẽ với các bài kiểm tra! Mười năm trước, điều này sẽ khiến rất nhiều người nhướng mày. Nhưng kỷ luật Phát triển theo hướng kiểm tra đã có ảnh hưởng sâu sắc đến ngành công nghiệp của chúng tôi và trở thành một trong những kỷ luật cơ bản nhất của chúng tôi. Dave nói đúng. Mã, không có kiểm tra, không sạch. Cho dù nó có trang nhã đến đâu, dù nó có thể đọc được và dễ đọc đến đâu, nếu nó không được kiểm tra, nó sẽ là ô uế.
Dave sử dụng từ tối thiểu hai lần. Rõ ràng anh ta coi trọng mã nhỏ hơn là mã lớn. Thật vậy, đây đã là một nguyên tắc phổ biến trong toàn bộ văn bản phần mềm kể từ khi ra đời. Nhỏ hơn là tốt hơn.
Dave cũng nói rằng mã nên biết chữ. Đây là tài liệu tham khảo mềm về chương trình dành cho người đọc viết của Knuth. 4 Kết quả là mã phải được soạn thảo ở dạng sao cho
nó có thể đọc được bởi con người.


#### Michael Feathers, author of Working
#### Effectively with Legacy Code
Tôi có thể liệt kê tất cả những phẩm chất mà tôi nhận thấy ở
mã sạch, nhưng có một chất lượng bao trùm
dẫn đến tất cả chúng. Luôn làm sạch mã
có vẻ như nó được viết bởi một người quan tâm.
Không có gì rõ ràng mà bạn có thể làm
lam no tôt hơn. Tất cả những điều đó đã được suy nghĩ
về tác giả của mã và nếu bạn cố gắng
tưởng tượng những cải tiến, bạn sẽ được dẫn trở lại
bạn đang ở đâu, ngồi đánh giá cao
mã ai đó để lại cho bạn — mã do ai đó để lại-
một người quan tâm sâu sắc đến nghề thủ công.
Một từ: quan tâm. Đó thực sự là chủ đề của
Cuốn sách này. Có lẽ một phụ đề thích hợp
sẽ là Cách Chăm sóc Mã.
Michael đánh nó vào đầu. Mã sạch là
mã đã được chăm sóc. Ai đó đã dành thời gian để giữ cho nó đơn giản và có trật tự.
Họ đã chú ý thích đáng đến các chi tiết. Họ đã quan tâm.

#### Ron Jeffries, author of Extreme Programming
#### Installed and Extreme Programming
#### Adventures in C#
Ron bắt đầu lập trình sự nghiệp của mình ở Fortran tại Bộ Tư lệnh Không quân Chiến lược và đã viết mã trong hầu hết mọi ngôn ngữ và trên hầu hết mọi
máy móc. Cần cân nhắc kỹ lời nói của anh ta.
Trong những năm gần đây, tôi bắt đầu và gần kết thúc, với Beck’s
quy tắc của mã đơn giản. Theo thứ tự ưu tiên, mã đơn giản:
• Chạy tất cả các bài kiểm tra;
• Không chứa trùng lặp;
• Thể hiện tất cả các ý tưởng thiết kế có trong
hệ thống;
• Giảm thiểu số lượng các thực thể như lớp,
các phương thức, hàm và những thứ tương tự.
Trong số này, tôi chủ yếu tập trung vào sự trùng lặp. Khi cùng một việc được thực hiện lặp đi lặp lại, đó là một dấu hiệu cho thấy trong đầu chúng ta có một ý tưởng không được thể hiện rõ trong mã. Tôi cố gắng tìm ra nó là gì. Sau đó, tôi cố gắng diễn đạt ý tưởng đó rõ ràng hơn.
Tính biểu cảm đối với tôi bao gồm những cái tên có ý nghĩa và tôi có thể sẽ thay đổi tên của mọi thứ nhiều lần trước khi tôi ổn định. Với các công cụ mã hóa hiện đại như Eclipse, việc đổi tên khá rẻ, vì vậy tôi không gặp khó khăn gì khi thay đổi. Biểu cảm đi

ngoài tên, tuy nhiên. Tôi cũng xem xét liệu một đối tượng hoặc phương thức có thực hiện nhiều hơn một việc hay không. Nếu nó là một đối tượng, nó có thể cần được chia thành hai hoặc nhiều đối tượng. Nếu nó là một
, tôi sẽ luôn sử dụng cấu trúc lại Phương thức trích xuất trên nó, dẫn đến một phương thức nói rõ hơn những gì nó hoạt động và một số phương thức con cho biết nó được thực hiện như thế nào.
Sự trùng lặp và biểu cảm khiến tôi phải mất một chặng đường dài để tìm hiểu thứ mà tôi coi là mã sạch, và việc cải thiện mã bẩn chỉ với hai điều này có thể tạo ra sự khác biệt rất lớn. Tuy nhiên, có một việc khác mà tôi biết phải làm, việc này khó hơn một chút
giải thích.
Sau nhiều năm làm công việc này, đối với tôi dường như tất cả các chương trình đều được tạo nên từ những yếu tố rất giống nhau. Một ví dụ là "tìm những thứ trong một bộ sưu tập." Cho dù chúng ta có cơ sở dữ liệu gồm các bản ghi nhân viên, hoặc bản đồ băm gồm các khóa và giá trị, hoặc một mảng các mục của một số
loại, chúng tôi thường thấy mình muốn một món đồ cụ thể từ bộ sưu tập đó. Khi tôi nhận thấy điều đó đang xảy ra, tôi thường sẽ gói phần triển khai cụ thể trong một phương pháp trừu tượng hơn
hoặc lớp học. Điều đó mang lại cho tôi một vài lợi thế thú vị.
Bây giờ tôi có thể triển khai chức năng với một cái gì đó đơn giản, chẳng hạn như bản đồ băm, nhưng vì bây giờ tất cả các tham chiếu đến tìm kiếm đó được bao phủ bởi sự trừu tượng nhỏ của tôi, tôi có thể thay đổi việc triển khai bất kỳ lúc nào tôi muốn. Tôi có thể tiến lên nhanh chóng trong khi vẫn bảo toàn khả năng thay đổi sau này.
Ngoài ra, việc tóm tắt bộ sưu tập thường thu hút sự chú ý của tôi đến những gì “thực sự” đang diễn ra và giúp tôi không đi vào con đường thực hiện hành vi thu thập tùy tiện khi tất cả những gì tôi thực sự cần là một vài cách khá đơn giản để tìm thấy những gì tôi muốn.
Giảm sự trùng lặp, tính biểu cảm cao và sớm xây dựng được những nội dung trừu tượng đơn giản. Đó là điều tạo nên mã sạch cho tôi.
Ở đây, trong một vài đoạn văn ngắn, Ron đã tóm tắt nội dung của cuốn sách này. Không trùng lặp, một điều, biểu cảm, trừu tượng nhỏ. Mọi thứ đều ở đó.


#### Ward Cunningham, inventor of Wiki,
#### inventor of Fit, coinventor of eXtreme
#### Programming. Motive force behind
#### Design Patterns. Smalltalk and OO
#### thought leader. The godfather of all
#### those who care about code.
Bạn biết rằng bạn đang làm việc trên mã sạch khi mỗi
thói quen bạn đọc hóa ra là khá nhiều
Bạn mong đợi. Bạn có thể gọi nó là mã đẹp khi
mã cũng làm cho nó giống như ngôn ngữ
được thực hiện cho vấn đề.
Những câu lệnh như thế này là đặc trưng của Ward.
Bạn đọc nó, gật đầu và sau đó tiếp tục
chủ đề tiếp theo. Nghe có vẻ hợp lý, quá rõ ràng, đến nỗi nó hầu như không được ghi nhận là một cái gì đó sâu sắc. Bạn có thể nghĩ rằng đó là khá nhiều những gì bạn mong đợi. Nhưng chúng ta hãy xem xét kỹ hơn.

“. . . khá nhiều những gì bạn mong đợi. " Lần cuối cùng bạn nhìn thấy một mô-đun giống như những gì bạn mong đợi là khi nào? Có phải nhiều khả năng các mô-đun bạn nhìn sẽ khó hiểu, phức tạp, rối rắm không? Không phải là quy tắc sai hướng? Bạn có từng lo lắng về việc cố gắng nắm bắt và nắm giữ các chuỗi lý luận xuất phát từ toàn bộ hệ thống và đan xen chúng qua mô-đun bạn đang đọc không? Lần cuối cùng bạn là khi nào
đọc qua một số mã và gật đầu theo cách bạn có thể đã gật đầu với tuyên bố của Ward?
Ward hy vọng rằng khi bạn đọc mã sạch, bạn sẽ không ngạc nhiên chút nào. Thật vậy, bạn thậm chí sẽ không tốn nhiều công sức. Bạn sẽ đọc nó, và nó sẽ giống như những gì bạn mong đợi. Nó sẽ rõ ràng, đơn giản và hấp dẫn. Mỗi mô-đun sẽ tạo tiền đề cho
tiếp theo. Mỗi phần cho bạn biết cách viết tiếp theo. Các chương trình sạch sẽ được viết rất hay đến mức bạn thậm chí không nhận ra. Nhà thiết kế làm cho nó trông đơn giản đến kỳ lạ như tất cả các thiết kế đặc biệt.
Còn quan niệm về vẻ đẹp của Ward thì sao? Tất cả chúng tôi đều phản đối thực tế rằng các lan truyền của chúng tôi không được thiết kế cho các vấn đề của chúng tôi. Nhưng tuyên bố của Ward khiến chúng tôi trở lại.
Anh ấy nói rằng mã đẹp làm cho ngôn ngữ giống như nó được tạo ra cho vấn đề! Vì vậy, chúng tôi có trách nhiệm làm cho ngôn ngữ trông đơn giản! Ngôn ngữ cố chấp ở khắp mọi nơi, hãy cẩn thận! Nó không phải là ngôn ngữ làm cho các chương trình có vẻ đơn giản. Đó là lập trình viên làm cho ngôn ngữ có vẻ đơn giản!


## Schools of Thought
Còn tôi (chú Bob) thì sao? Tôi nghĩ gì
mã sạch là? Cuốn sách này sẽ cho bạn biết, một cách gớm ghiếc
chi tiết, những gì tôi và đồng bào của tôi nghĩ về
mã sạch. Chúng tôi sẽ cho bạn biết những gì chúng tôi nghĩ tạo ra
tên biến sạch, hàm sạch, sạch
lớp học, v.v. Chúng tôi sẽ trình bày những ý kiến ​​này như là-
Lutes, và chúng tôi sẽ không xin lỗi vì sự ngoan cố của chúng tôi.
Đối với chúng tôi, tại thời điểm này trong sự nghiệp của chúng tôi, họ đã-
đàn nguyệt. Họ là trường phái suy nghĩ của chúng tôi về sạch sẽ
mã.
Không phải tất cả các võ sĩ đều đồng ý về điều tốt nhất
võ thuật, hoặc kỹ thuật tốt nhất trong một môn võ
nghệ thuật. Thường thì các võ sĩ bậc thầy sẽ hình thành
trường tư tưởng riêng và tập hợp sinh viên để
học hỏi từ họ. Vì vậy, chúng ta thấy Gracie Jiu Jistu,
được thành lập và giảng dạy bởi gia đình Gracie ở Brazil. Chúng ta thấy Hakkoryu Jiu Jistu, được thành lập và giảng dạy bởi Okuyama Ryuho ở Tokyo. Chúng tôi thấy Jeet Kune Do, được thành lập và giảng dạy bởi
Lý Tiểu Long ở Hoa Kỳ.


Học sinh của những cách tiếp cận này đắm mình trong những lời dạy của người sáng lập.
Họ cống hiến hết mình để học những gì mà bậc thầy cụ thể đó dạy, thường là để phù hợp với sự dạy dỗ của bất kỳ bậc thầy nào khác. Sau này, khi học sinh phát triển trong lĩnh vực nghệ thuật của mình, họ có thể trở thành học trò của một bậc thầy khác để có thể mở rộng kiến ​​thức và thực hành.
Một số cuối cùng tiếp tục trau dồi kỹ năng, khám phá các kỹ thuật mới và thành lập trường học của riêng mình.
Không có trường phái khác nhau nào là hoàn toàn đúng. Tuy nhiên, trong một trường học cụ thể, chúng tôi hành động như thể những lời dạy và kỹ thuật là đúng. Rốt cuộc, có một cách đúng đắn để luyện tập Hakkoryu Jiu Jitsu, hoặc Jeet Kune Do. Nhưng sự đúng đắn này trong một trường học không phải là vô hại-
coi thường những lời dạy của một trường khác.
Hãy coi cuốn sách này là một mô tả về Trường học Mã sạch của Cố vấn Đối tượng. Các kỹ thuật và giáo lý bên trong là cách chúng ta thực hành nghệ thuật của mình. Chúng tôi sẵn sàng tuyên bố rằng nếu bạn làm theo những lời dạy này, bạn sẽ được hưởng những lợi ích mà chúng tôi đã được hưởng,
và bạn sẽ học cách viết mã sạch sẽ và chuyên nghiệp. Nhưng đừng sai lầm khi nghĩ rằng bằng cách nào đó chúng ta “đúng” theo bất kỳ nghĩa tuyệt đối nào. Có những trường khác và
những bậc thầy khác có nhiều tuyên bố về tính chuyên nghiệp như chúng tôi. Nó cũng mong bạn học hỏi từ họ.
Thật vậy, nhiều khuyến nghị trong cuốn sách này đang gây tranh cãi. Bạn sẽ không đồng ý với tất cả chúng. Bạn có thể không đồng ý với một số người trong số họ. Tốt rồi.
Chúng tôi không thể yêu cầu thẩm quyền cuối cùng. Mặt khác, những khuyến nghị trong cuốn sách này là những điều mà chúng tôi đã suy nghĩ rất lâu và khó. Chúng tôi đã học được chúng qua nhiều thập kỷ
kinh nghiệm và lặp đi lặp lại thử và sai. Vì vậy, dù bạn đồng ý hay không đồng ý, sẽ thật đáng tiếc nếu bạn không xem và tôn trọng quan điểm của chúng tôi.


## We Are Authors
Trường @author của Javadoc cho chúng ta biết chúng ta là ai. Chúng tôi là tác giả. Và một điều về các tác giả là họ có độc giả. Thật vậy, các tác giả có trách nhiệm giao tiếp tốt với độc giả của họ. Lần tới khi bạn viết một dòng mã, hãy nhớ rằng bạn là tác giả,
viết cho độc giả, những người sẽ đánh giá nỗ lực của bạn.
Bạn có thể hỏi: Thực sự đọc được bao nhiêu mã? Không phải hầu hết mọi nỗ lực đều dành cho việc viết nó?
Bạn đã bao giờ phát lại một phiên chỉnh sửa chưa? Trong những năm 80 và 90, chúng tôi đã có những biên tập viên như Emacs theo dõi mọi thao tác gõ phím. Bạn có thể làm việc trong một giờ và sau đó phát lại toàn bộ phiên chỉnh sửa của mình như một bộ phim tốc độ cao. Khi tôi làm điều này, kết quả thật hấp dẫn.
Phần lớn quá trình phát lại là cuộn và điều hướng đến các mô-đun khác! Bob vào mô-đun.
Anh ta cuộn xuống chức năng cần thay đổi.
Anh dừng lại, cân nhắc các lựa chọn của mình.
Ồ, anh ấy đang cuộn lên đầu mô-đun để kiểm tra việc khởi chạy một biến.
Bây giờ anh ấy cuộn xuống và bắt đầu nhập.

Rất tiếc, anh ấy đang xóa những gì anh ấy đã nhập!
Anh ấy gõ lại.
Anh ấy lại xóa nó đi!
Anh ta gõ một nửa thứ khác nhưng sau đó xóa đi!
Anh ấy cuộn xuống một hàm khác gọi hàm mà anh ấy đang thay đổi để xem nó như thế nào
gọi là.
Anh ta cuộn lại và nhập mã giống như anh ta vừa xóa.
Anh ta dừng lại.
Anh ấy lại xóa mã đó!
Anh ấy bật lên một cửa sổ khác và nhìn vào một lớp con. Chức năng đó có bị ghi đè không?
. . .
Bạn nhận được sự trôi dạt. Thật vậy, tỷ lệ thời gian dành cho việc đọc và viết là hơn 10: 1.
Chúng tôi liên tục đọc mã cũ như một phần của nỗ lực viết mã mới.
Bởi vì tỷ lệ này rất cao, chúng tôi muốn việc đọc mã trở nên dễ dàng, ngay cả khi nó làm cho việc viết khó hơn. Tất nhiên, không có cách nào để viết mã mà không đọc nó, vì vậy việc làm cho mã dễ đọc thực sự giúp bạn viết dễ dàng hơn.
Không có lối thoát khỏi logic này. Bạn không thể viết mã nếu bạn không thể đọc mã làm tròn. Đoạn mã bạn đang cố gắng viết ngày hôm nay sẽ khó hay dễ viết tùy thuộc vào mức độ khó hay dễ đọc của đoạn mã xung quanh. Vì vậy, nếu bạn muốn đi nhanh, nếu bạn muốn hoàn thành nhanh chóng, nếu bạn muốn mã của bạn dễ viết, hãy làm cho nó dễ đọc.


## The Boy Scout Rule
Viết mã tốt thôi là chưa đủ. Mã phải được giữ sạch theo thời gian. Tất cả chúng ta đều đã thấy mã bị thối rữa và xuống cấp theo thời gian. Vì vậy chúng ta phải có vai trò tích cực trong việc ngăn chặn sự suy thoái này.
Hội Nam Hướng đạo Hoa Kỳ có một quy tắc đơn giản mà chúng ta có thể áp dụng cho nghề nghiệp của mình.
Để khu cắm trại sạch hơn bạn đã tìm thấy. 5 Nếu tất cả chúng ta đã kiểm tra mã của mình sạch hơn một chút so với khi chúng ta kiểm tra, thì mã
đơn giản là không thể thối rữa. Việc dọn dẹp không cần phải là một cái gì đó lớn lao. Thay đổi một tên biến cho tốt hơn, chia nhỏ một hàm quá lớn, loại bỏ một chút trùng lặp nhỏ, xóa một câu lệnh if tổng hợp.
Bạn có thể tưởng tượng làm việc trong một dự án mà mã đơn giản trở nên tốt hơn theo thời gian? Bạn có tin rằng bất kỳ lựa chọn nào khác là chuyên nghiệp? Thật vậy, không phải cải tiến liên tục có phải là một phần nội tại của tính chuyên nghiệp không?


## Prequel and Principles
Theo nhiều cách, cuốn sách này là “phần tiền truyện” của cuốn sách tôi viết năm 2002 có tựa đề Phát triển phần mềm Agile: Nguyên tắc, Mẫu và Thực hành (PPP). Cuốn sách về PPP liên quan đến các nguyên tắc của thiết kế hướng đối tượng và nhiều phương pháp được sử dụng bởi các chuyên gia-
các nhà phát triển sional. Nếu bạn chưa đọc PPP, thì bạn có thể thấy rằng nó tiếp tục câu chuyện được kể bởi cuốn sách này. Nếu bạn đã đọc nó, thì bạn sẽ thấy nhiều tình cảm của cuốn sách đó được lặp lại trong cuốn sách này ở cấp độ mã.
Trong cuốn sách này, bạn sẽ tìm thấy các tài liệu tham khảo lẻ tẻ về các nguyên tắc thiết kế khác nhau. Chúng bao gồm Nguyên tắc trách nhiệm duy nhất (SRP), Nguyên tắc đóng mở (OCP) và Nguyên tắc đảo ngược phụ thuộc (DIP) cùng những nguyên tắc khác. Những nguyên tắc này được mô tả trong
chiều sâu trong PPP.


## Conclusion
Sách về nghệ thuật không hứa hẹn biến bạn trở thành nghệ sĩ. Tất cả những gì họ có thể làm là cung cấp cho bạn một số công cụ, kỹ thuật và quy trình suy nghĩ mà các nghệ sĩ khác đã sử dụng. Vì vậy, cuốn sách này cũng không thể hứa hẹn sẽ giúp bạn trở thành một lập trình viên giỏi. Nó không thể hứa sẽ cung cấp cho bạn “mã cảm giác”.
Tất cả những gì nó có thể làm là cho bạn thấy các quy trình suy nghĩ của các lập trình viên giỏi và các thủ thuật, kỹ thuật và công cụ mà họ sử dụng.
Cũng giống như một cuốn sách về nghệ thuật, cuốn sách này sẽ có đầy đủ các chi tiết. Sẽ có rất nhiều mã.
Bạn sẽ thấy mã tốt và bạn sẽ thấy mã xấu. Bạn sẽ thấy mã xấu được chuyển thành mã tốt. Bạn sẽ thấy danh sách các kinh nghiệm học, các nguyên tắc và kỹ thuật. Bạn sẽ thấy ví dụ này đến ví dụ khác. Sau đó, tùy thuộc vào bạn.
Bạn còn nhớ câu chuyện cười cũ về người nghệ sĩ vĩ cầm trong buổi hòa nhạc bị lạc trên đường đến một quán hát không? Anh ta dừng một ông già ở góc đường và hỏi ông ta làm thế nào để đến Carnegie Hall.
Ông lão nhìn người nghệ sĩ vĩ cầm và cây đàn vĩ cầm được kẹp dưới cánh tay, và nói: “Thực tế, con trai. Thực hành!"