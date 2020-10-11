# Chapter 03: Say Yes
Bạn có biết rằng tôi đã phát minh ra hộp thư thoại? Đúng rồi. Trên thực tế, có ba trong số
chúng tôi, người đã giữ bằng sáng chế cho hộp thư thoại. Ken Finder, Jerry Fitzpatrick, và tôi. Đó là vào đầu những năm 80, và chúng tôi làm việc cho một công ty tên là Teradyne. Giám đốc điều hành của chúng tôi đã ủy quyền cho chúng tôi nghĩ ra một loại sản phẩm mới và chúng tôi đã phát minh ra
“Lễ tân điện tử”, viết tắt là ER.

Bạn đều biết ER là gì. ER là một trong những cỗ máy khủng khiếp trả lời điện thoại tại các công ty và hỏi bạn tất cả các loại câu hỏi chết người mà bạn
cần trả lời bằng cách nhấn các nút. (“Đối với tiếng Anh, nhấn 1.”)

ER của chúng tôi sẽ trả lời điện thoại cho một công ty và yêu cầu bạn gọi tên của người bạn muốn. Nó sẽ yêu cầu bạn phát âm tên của bạn, và sau đó nó sẽ gọi cho người được đề cập. Nó sẽ thông báo cuộc gọi và hỏi liệu nó nên được chấp nhận. Nếu vậy, nó sẽ kết nối cuộc gọi và ngắt cuộc gọi.

Bạn có thể cho ER biết bạn đang ở đâu. Bạn có thể cung cấp cho nó một số số điện thoại để
thử. Vì vậy, nếu bạn đang ở văn phòng của người khác, ER có thể tìm thấy bạn. Nếu bạn ở
nhà, ER có thể tìm thấy bạn. Nếu bạn ở một thành phố khác, ER có thể tìm thấy bạn.
Và, cuối cùng, nếu ER không thể tìm thấy bạn, nó sẽ có một thông báo. Đó là nơi
hộp thư thoại đến.

Thật kỳ lạ, Teradyne không thể tìm ra cách bán ER. Dự án đã chạy hết ngân sách và được biến thành thứ mà chúng tôi biết cách bán — CDS,
Hệ thống Điều phối Thủ công, để cử thợ sửa điện thoại tới việc làm. Và Teradyne cũng đã đánh rơi bằng sáng chế mà không cho chúng tôi biết. (!) Hiện tại chủ bằng sáng chế đã nộp ba tháng sau khi chúng tôi làm. (!!) 1

Rất lâu sau khi chuyển ER thành CDS, nhưng rất lâu trước khi tôi phát hiện ra rằng
bằng sáng chế đã bị loại bỏ. Tôi đợi CEO của công ty trong một cái cây. Chúng tôi có một cây sồi lớn bên ngoài mặt trước của tòa nhà. Tôi đã leo lên nó và chờ đợi Jaguar của anh ấy để kéo đến. Tôi gặp anh ấy ở cửa và yêu cầu trong vài phút. Anh ta băt buộc.

Tôi nói với anh ấy rằng chúng tôi thực sự cần bắt đầu lại dự án ER. Tôi đã nói với anh ấy rằng tôi đã chắc chắn rằng nó có thể kiếm tiền. Anh ấy làm tôi ngạc nhiên khi nói, "OK Bob, cố gắng lên
kế hoạch. Chỉ cho tôi cách tôi có thể kiếm tiền. Nếu bạn làm và tôi tin điều đó, tôi sẽ bắt đầu
ER một lần nữa. ”

Tôi đã không mong đợi điều đó. Tôi đã mong đợi anh ấy nói, “Bạn nói đúng, Bob. Tôi sẽ
bắt đầu lại dự án đó và tôi sẽ tìm cách kiếm tiền tại 1. Đối với tôi bằng sáng chế không đáng giá chút nào. Tôi đã bán nó cho Teradyne với giá 1 đô la, theo công việc của tôi hợp đồng (và tôi không nhận được đô la).
nó. ” Nhưng không. Anh ấy đặt gánh nặng trở lại cho tôi. Và đó là một gánh nặng cho tôi
trong khoảng. Xét cho cùng, tôi là một gã phần mềm, không phải một gã hám tiền. Tôi muốn làm việc trên Dự án ER, không chịu trách nhiệm về lãi và lỗ. Nhưng tôi không muốn hiển thị
sự mâu thuẫn. Vì vậy, tôi cảm ơn anh ấy và rời văn phòng của anh ấy với những lời sau:
“Cảm ơn Russ. Tôi cam kết . . . Tôi đoán."
Cùng với đó, hãy để tôi giới thiệu bạn với Roy Osherove, người sẽ chỉ cho bạn cách thảm hại đó là tuyên bố.

## A L A N G UAG EbOF C OMMITMENT
Bởi Roy Osherove
Nói. Nghĩa là. Làm
Có ba phần để thực hiện một cam kết.

    1. Bạn nói rằng bạn sẽ làm được.
    2. Ý bạn là nó.
    3. Bạn thực sự làm điều đó.

Nhưng tần suất chúng ta gặp phải những người khác (tất nhiên không phải chính mình!)
không bao giờ đi tất cả các con đường với ba giai đoạn?

    • Bạn hỏi anh chàng IT tại sao mạng quá chậm và anh ta nói “Ừ. Chúng tôi thực sự
    cần có một số bộ định tuyến mới. " Và bạn biết sẽ không có gì xảy ra trong
    danh mục đó.

    • Bạn yêu cầu một thành viên trong nhóm chạy một số kiểm tra thủ công trước khi kiểm tra
    mã nguồn, và anh ấy trả lời, “Chắc chắn rồi. Tôi hy vọng sẽ đạt được nó vào cuối ngày. ”
    Và bằng cách nào đó, bạn cảm thấy rằng ngày mai bạn sẽ cần hỏi xem liệu có thử nghiệm nào thực sự
    diễn ra trước khi nhận phòng.
    • Sếp của bạn đi vào phòng và lầm bầm, "chúng ta phải đi nhanh hơn."

Và bạn biết anh ấy thực sự có nghĩa là BẠN phải tiến nhanh hơn. Anh ấy sẽ không làm
bất cứ thứ gì về nó.

Có rất ít người, khi họ nói điều gì đó, họ có ý nghĩa và sau đó thực sự hoàn thành nó. Có một số người sẽ nói những điều và có nghĩa là chúng, nhưng họ không bao giờ làm được. Và có rất nhiều người hứa hẹn nhiều điều và thậm chí không có ý định làm chúng. Đã bao giờ nghe ai đó nói, "Anh bạn, tôi thực sự cần giảm cân, ”và bạn biết họ sẽ không làm gì với nó? Nó xảy ra mọi lúc.

Tại sao chúng ta cứ có cảm giác kỳ lạ rằng, hầu hết thời gian, mọi người không thực sự cam kết hoàn thành một việc gì đó?

Tệ hơn nữa, thường thì trực giác của chúng ta có thể khiến chúng ta thất vọng. Đôi khi chúng ta muốn tin ai đó thực sự có nghĩa là những gì họ nói khi họ thực sự không nói. Chúng tôi muốn tin rằng một nhà phát triển khi họ nói, nhấn vào góc, rằng họ có thể hoàn thành hai- nhiệm vụ tuần trong một tuần thay vào đó, nhưng chúng ta không nên làm như vậy.

Thay vì tin tưởng vào gan dạ của mình, chúng ta có thể sử dụng một số thủ thuật liên quan đến ngôn ngữ để thử và tìm hiểu xem mọi người có thực sự muốn nói gì không. Và bằng cách thay đổi những gì chúng ta nói, chúng ta có thể tự mình bắt đầu thực hiện các bước 1 và 2 của danh sách trước. Khi nào chúng ta nói rằng chúng tôi sẽ cam kết với một điều gì đó, và chúng tôi cần phải có ý nghĩa đó.

### R ECOG N IZI N G L AC OF C OMMITMENT

Chúng ta nên xem xét ngôn ngữ chúng ta sử dụng khi cam kết thực hiện một điều gì đó, như
dấu hiệu cho biết những điều sắp xảy ra. Trên thực tế, vấn đề nhiều hơn là tìm kiếm
từ cụ thể trong những gì chúng tôi nói. Nếu bạn không thể tìm thấy những từ ma thuật nhỏ đó, rất có thể chúng tôi không cố ý những gì chúng tôi nói, hoặc chúng tôi có thể không tin rằng nó là khả thi.

Dưới đây là một số ví dụ về các từ và cụm từ để tìm kiếm đó là dấu hiệu kể chuyện
of noncommitment:

    • Cần \ nên. "Chúng tôi cần phải hoàn thành việc này." "Tôi cần phải giảm cân." "Người nào
    nên biến điều đó thành hiện thực. ”

    • Hy vọng \ ước muốn. "Tôi hy vọng sẽ hoàn thành việc này vào ngày mai." “Tôi hy vọng chúng ta có thể gặp nhau
    lại một ngày nào đó. " "Tôi ước tôi có thời gian cho việc đó." “Tôi ước gì máy tính này là
    nhanh hơn. ”
    • Hãy. (không theo sau là “Tôi...”) “Đôi khi chúng ta gặp nhau nhé.” "Hãy hoàn thành việc này."

Khi bạn bắt đầu tìm kiếm những từ này, bạn sẽ thấy rằng bạn bắt đầu phát hiện ra chúng
hầu như ở mọi nơi xung quanh bạn, và ngay cả trong những điều bạn nói với người khác.
Bạn sẽ thấy chúng ta có xu hướng rất bận rộn và không chịu trách nhiệm về mọi việc.
Và điều đó không ổn khi bạn hoặc ai đó phụ thuộc vào những lời hứa đó như một phần
của công việc. Tuy nhiên, bạn đã thực hiện bước đầu tiên — bắt đầu nhận ra việc thiếu
cam kết xung quanh bạn và trong bạn.
Chúng tôi đã nghe thấy âm thanh của noncommitment. Làm thế nào để chúng tôi nhận ra thực lời cam kết?


### W H AT D O E S C O M M I T M E N T S O U N D L I K E?
Điểm chung trong các cụm từ của phần trước là chúng cho rằng mọi thứ nằm ngoài tầm tay của “tôi” hoặc họ không chịu trách nhiệm cá nhân.
Trong mỗi trường hợp này, mọi người cư xử như thể họ là nạn nhân của một tình huống thay vì kiểm soát nó.

Sự thật thực sự là cá nhân bạn LUÔN LUÔN có thứ gì đó nằm dưới kiểm soát, vì vậy luôn có điều gì đó bạn có thể hoàn toàn cam kết thực hiện.

Thành phần bí mật để nhận ra cam kết thực sự là tìm kiếm các câu âm thanh như thế này: Tôi sẽ. . . bởi. . . (ví dụ: Tôi sẽ hoàn thành việc này trước Thứ Ba.)

Điều gì quan trọng trong câu này? Bạn đang nói một sự thật về điều gì đó BẠN sẽ làm với thời gian kết thúc rõ ràng. Bạn không nói về bất kỳ ai khác ngoài chính bạn.
Bạn đang nói về một hành động mà bạn sẽ thực hiện. Bạn sẽ không “có thể” lấy nó, hoặc
"Có thể nhận được nó"; bạn sẽ đạt được nó.

Không có (về mặt kỹ thuật) không có cách nào thoát khỏi cam kết bằng lời nói này. Bạn đã nói rằng bạn sẽ làm nó và bây giờ chỉ có thể có một kết quả nhị phân — bạn hoàn thành hoặc không.
Nếu bạn không hoàn thành, mọi người có thể giữ bạn theo lời hứa của mình. Bạn sẽ cảm thấy
tệ về việc không làm điều đó. Bạn sẽ cảm thấy khó xử khi nói với ai đó về việc không có
đã thực hiện nó (nếu ai đó nghe bạn hứa bạn sẽ làm).

Đáng sợ phải không?

Bạn đang chịu hoàn toàn trách nhiệm về điều gì đó, trước mặt ít nhất là khán giả một người. Không chỉ bạn đứng trước gương hay máy tính
màn. Đó là bạn, đối mặt với một con người khác và nói rằng bạn sẽ làm được. Đó là bắt đầu cam kết. Đặt mình vào tình huống buộc bạn phải làm một cái gì đó.

Bạn đã thay đổi ngôn ngữ bạn sử dụng thành ngôn ngữ cam kết và sẽ giúp bạn vượt qua hai giai đoạn tiếp theo: ý nghĩa và theo dõi xuyên qua.

Dưới đây là một số lý do bạn có thể không cố ý hoặc làm theo, với một số giải pháp.

### Nó sẽ không hiệu quả vì tôi dựa vào người X để hoàn thành việc này.
Bạn chỉ có thể cam kết những thứ mà bạn có toàn quyền kiểm soát. Ví dụ, nếu mục tiêu của bạn là hoàn thành một mô-đun cũng phụ thuộc vào một nhóm khác, bạn không thể cam kết hoàn thành mô-đun với sự tích hợp đầy đủ với nhóm khác. Nhưng bạn có thể cam kết các hành động cụ thể sẽ đưa bạn đến mục tiêu của mình. Bạn có thể:

    • Ngồi xuống một giờ với Gary từ nhóm cơ sở hạ tầng để hiểu
    sự phụ thuộc của bạn.
    • Tạo giao diện tóm tắt sự phụ thuộc của mô-đun của bạn với mô-đun khác
    cơ sở hạ tầng của nhóm.
    • Gặp ít nhất ba lần trong tuần này với nhân viên xây dựng để đảm bảo
    các thay đổi hoạt động tốt trong hệ thống xây dựng của công ty.
    • Tạo bản dựng cá nhân của riêng bạn để chạy các bài kiểm tra tích hợp của bạn cho
    mô-đun.

Thấy sự khác biệt?

Nếu mục tiêu cuối cùng phụ thuộc vào người khác, bạn nên cam kết thực hiện các hành động cụ thể
đưa bạn đến gần mục tiêu cuối cùng hơn.


### Nó sẽ không hoạt động vì tôi thực sự không biết liệu nó có thể được thực hiện hay không.
Nếu không thể thực hiện được, bạn vẫn có thể cam kết thực hiện các hành động đưa bạn đến gần hơn
đến mục tiêu. Tìm hiểu xem nó có thể được thực hiện hay không có thể là một trong những hành động để cam kêt!
Thay vì cam kết sửa tất cả 25 lỗi còn lại trước khi phát hành (mà có thể không thực hiện được), bạn có thể cam kết thực hiện những hành động cụ thể này để mang lại cho bạn gần hơn với mục tiêu đó:

    • Vượt qua tất cả 25 lỗi và cố gắng tạo lại chúng.
    • Ngồi xuống với QA, người đã tìm ra từng lỗi để xem bản tóm tắt của lỗi đó.
    • Dành tất cả thời gian bạn có trong tuần này để cố gắng sửa từng lỗi.


### Nó sẽ không hoạt động vì đôi khi tôi không làm được.
Điều đó xảy ra. Điều gì đó bất ngờ có thể xảy ra, và đó là cuộc sống. Nhưng bạn vẫn muốn sống theo mong đợi. Trong trường hợp đó, đã đến lúc thay đổi kỳ vọng,  sớm nhất có thể.

Nếu bạn không thể thực hiện cam kết của mình, điều quan trọng nhất là nâng cao màu đỏ
gắn cờ càng sớm càng tốt cho bất kỳ ai mà bạn đã cam kết.

Bạn càng đưa cờ sớm cho tất cả các bên liên quan, thì càng có nhiều khả năng thời gian để nhóm dừng lại, đánh giá lại các hành động hiện tại đang được thực hiện và quyết định xem
điều gì đó có thể được thực hiện hoặc thay đổi (ví dụ: về mức độ ưu tiên). Bởi
làm điều này, cam kết của bạn vẫn có thể được thực hiện hoặc bạn có thể thay đổi thành
cam kết khác nhau.

Một số ví dụ:

    • Nếu bạn hẹn một buổi trưa tại một quán cà phê ở trung tâm thành phố với đồng nghiệp và bạn
    bị kẹt xe, bạn nghi ngờ mình sẽ có thể theo dõi
    cam kết có mặt đúng giờ. Bạn có thể gọi cho đồng nghiệp của mình ngay khi bạn
    nhận ra bạn có thể đến muộn và cho họ biết. Có lẽ bạn có thể tìm thấy một gần hơn
    nơi gặp gỡ, hoặc có thể hoãn cuộc họp.

    • Nếu bạn đã cam kết giải quyết một lỗi mà bạn nghĩ là có thể giải quyết được và bạn nhận ra
    tại một số điểm, lỗi này ghê tởm hơn nhiều so với suy nghĩ trước đây, bạn
    có thể giương cờ. Sau đó, nhóm có thể quyết định một quá trình hành động để thực hiện
    cam kết đó (ghép nối, tăng đột biến về các giải pháp tiềm năng, động não) hoặc
    thay đổi mức độ ưu tiên và chuyển bạn sang một lỗi khác đơn giản hơn.

Một điểm quan trọng ở đây là: Nếu bạn không nói với ai về tiềm năng vấn đề càng sớm càng tốt, bạn sẽ không cho ai cơ hội để giúp bạn tuân theo cam kết của bạn.


## TÓM LƯỢC
Tạo ra một ngôn ngữ cam kết nghe có vẻ hơi đáng sợ, nhưng nó có thể giúp giải quyết
nhiều vấn đề giao tiếp mà các lập trình viên phải đối mặt ngày nay — ước tính, thời hạn và rủi ro giao tiếp mặt đối mặt. Bạn sẽ được coi là một người nghiêm túc nhà phát triển tuân theo lời của họ và đó là một trong những điều tốt nhất bạn có thể hy vọng trong ngành của chúng tôi.

## L E AR N I N G H OW TO S AY “ Y E S ”

Tôi đã yêu cầu Roy đóng góp bài báo đó vì nó đánh động một hợp âm trong tôi. Tôi có
đã thuyết giảng về việc học cách nói không trong một thời gian. Nhưng nó cũng giống như
quan trọng là học cách nói có.

### T H E O T H E R S I D E OF “T R Y”
Hãy tưởng tượng rằng Peter chịu trách nhiệm về một số sửa đổi đối với xếp hạng động cơ. Anh ấy ước tính riêng rằng những sửa đổi này sẽ mất năm hoặc sáu ngày. Anh ấy cũng nghĩ rằng việc viết tài liệu cho các sửa đổi sẽ mất vài giờ. Vào sáng thứ Hai, người quản lý của anh ấy, Marge, hỏi anh ấy về tình trạng.

    Marge: "Peter, bạn sẽ thực hiện mod công cụ xếp hạng vào thứ Sáu chứ?"

    Peter: "Tôi nghĩ điều đó có thể làm được."
    Marge: "Liệu điều đó có bao gồm tài liệu không?"
    Peter: "Tôi cũng sẽ cố gắng hoàn thành công việc đó."

Có lẽ Marge không thể nghe thấy sự hòa hợp trong các tuyên bố của Peter, nhưng anh ấy chắc chắn
không cam kết nhiều. Marge đang đặt câu hỏi về nhu cầu câu trả lời boolean nhưng câu trả lời boolean của Peter rất mờ.

Lưu ý việc lạm dụng từ try. Trong chương trước, chúng tôi đã sử dụng "nỗ lực thêm"
định nghĩa của thử. Ở đây, Peter đang sử dụng định nghĩa “có thể, có thể không”.
Peter sẽ tốt hơn nếu trả lời như thế này:

    Marge: "Peter, bạn sẽ thực hiện mod công cụ xếp hạng vào thứ Sáu chứ?"
    Peter: "Có thể, nhưng có thể là thứ Hai."
    Marge: "Liệu điều đó có bao gồm tài liệu không?"
    Peter: "Tài liệu sẽ mất vài giờ nữa cho tôi, vì vậy thứ Hai
    là có thể, nhưng có thể muộn nhất là vào thứ Ba. "
Trong trường hợp này, ngôn ngữ của Phi-e-rơ trung thực hơn. Anh ấy đang mô tả của riêng mình
sự không chắc chắn đối với Marge. Marge có thể đối phó với sự không chắc chắn đó. Trên
mặt khác, cô ấy có thể không.


### C HƯỚNG DẪN VỚI DISCIPLINE
    Marge: “Peter, tôi cần có hoặc không rõ ràng. Bạn sẽ có công cụ đánh giá
    đã hoàn thành và được ghi lại vào thứ Sáu? "

Đây là một câu hỏi hoàn toàn công bằng cho Marge. Cô ấy có một lịch trình để duy trì,
và cô ấy cần một câu trả lời nhị phân về thứ Sáu. Phi-e-rơ nên trả lời thế nào?

    Peter: “Trong trường hợp đó, Marge, tôi sẽ phải nói không. Tôi có thể chắc chắn sớm nhất
    rằng tôi sẽ hoàn thành việc sửa đổi và tài liệu là thứ Ba. ”
    Marge: "Bạn đang cam kết với Thứ Ba?"
    Peter: "Vâng, tôi sẽ chuẩn bị tất cả vào thứ Ba."

Nhưng điều gì sẽ xảy ra nếu Marge thực sự cần các sửa đổi và tài liệu được thực hiện bởi
Thứ sáu?
Marge: “Peter, thứ ba mang đến cho tôi một vấn đề thực sự. Willy, nhà văn công nghệ của chúng tôi, sẽ
có sẵn vào thứ Hai. Anh ấy có năm ngày để hoàn thành người dùng
hướng dẫn. Nếu tôi không có tài liệu về công cụ xếp hạng vào sáng Thứ Hai,
anh ấy sẽ không bao giờ hoàn thành sổ tay đúng hạn. Bạn có thể làm tài liệu trước không? ”

    Peter: “Không, mod phải đến trước, bởi vì chúng tôi tạo tài liệu
    từ đầu ra của quá trình chạy thử nghiệm. ”
    Marge: “Chà, không có cách nào bạn có thể hoàn thành các bản mod và
    tài liệu trước sáng thứ Hai? "

Bây giờ Peter có một quyết định để thực hiện. Có một cơ hội tốt là anh ấy sẽ hoàn thành
đánh giá các sửa đổi động cơ vào thứ Sáu và anh ấy thậm chí có thể hoàn thành
tài liệu trước khi anh ấy về nhà vào cuối tuần. Anh ấy có thể làm một vài giờ làm việc trên
Thứ bảy cũng vậy nếu mọi thứ kéo dài hơn anh ấy hy vọng. Vậy anh ta nên nói gì với Marge?

    Peter: “Nhìn Marge, có một cơ hội tốt là tôi có thể hoàn thành mọi việc
    vào sáng thứ Hai nếu tôi dành thêm một vài giờ vào thứ Bảy. ”
    Điều đó có giải quyết được vấn đề của Marge không? Không, nó chỉ đơn giản là thay đổi tỷ lệ cược và đó là
    những gì Peter cần nói với cô ấy.
    Marge: "Vậy tôi có thể tính vào sáng thứ Hai không?"
    Peter: "Có thể, nhưng không chắc chắn."

Điều đó có thể không đủ tốt cho Marge.
Marge: “Nhìn này, Peter, tôi thực sự cần xác định rõ điều này. Có cách nào không bạn
có thể cam kết hoàn thành việc này trước sáng thứ Hai không? ”

Peter có thể bị cám dỗ để vi phạm kỷ luật vào thời điểm này. Anh ấy có thể có được
hoàn thành nhanh hơn nếu anh ấy không viết các bài kiểm tra của mình. Anh ấy có thể hoàn thành công việc nhanh hơn nếu anh ấy không tái cấu trúc. Anh ấy có thể hoàn thành nhanh hơn nếu anh ấy không chạy hết sức
bộ hồi quy.

Đây là nơi các chuyên gia vẽ đường. Trước hết, Peter chỉ sai về những giả thuyết của mình. Anh ta sẽ không hoàn thành nhanh hơn nếu anh ta không viết các bài kiểm tra của mình. Anh ta
sẽ không hoàn thành nhanh hơn nếu anh ta không cấu trúc lại. Anh ấy sẽ không hoàn thành nhanh hơn nếu anh ấy bỏ qua bộ hồi quy đầy đủ. Nhiều năm kinh nghiệm đã dạy chúng tôi rằng phá vỡ
kỷ luật chỉ làm chúng ta chậm lại. 

Nhưng thứ hai, là một chuyên gia, anh ta có trách nhiệm duy trì một số tiêu chuẩn. Mã của anh ta cần được kiểm tra, và cần phải có các bài kiểm tra. Mã của anh ấy cần phải sạch sẽ. Và anh ta phải chắc chắn rằng anh ta không phá vỡ bất cứ điều gì khác trong
hệ thống.

Peter, với tư cách là một chuyên gia, đã cam kết duy trì những tiêu chuẩn. Tất cả các cam kết khác mà anh ta đưa ra phải tuân theo điều đó. Vì thế toàn bộ dòng lý luận này cần phải hủy bỏ.

    Peter: “Không, Marge, tôi thực sự không thể chắc chắn về bất kỳ ngày nào
    trước Thứ Ba. Tôi xin lỗi nếu điều đó làm xáo trộn lịch trình của bạn, nhưng nó là
    chỉ là thực tế mà chúng ta đang phải đối mặt. "
    Marge: “Chết tiệt. Tôi đã thực sự tin tưởng vào việc đưa cái này vào sớm hơn.
    Bạn chắc chắn?"
    Peter: "Tôi chắc chắn rằng có thể muộn nhất là vào Thứ Ba, vâng."
    Marge: “OK, tôi đoán tôi sẽ nói chuyện với Willy để xem liệu anh ấy có thể sắp xếp lại lịch trình của mình hay không.”

Trong trường hợp này, Marge chấp nhận câu trả lời của Peter và bắt đầu tìm kiếm
các tùy chọn. Nhưng điều gì sẽ xảy ra nếu tất cả các lựa chọn của Marge đã hết? Điều gì sẽ xảy ra nếu Peter là hy vọng cuối cùng?

    Marge: "Peter, nhìn này, tôi biết đây là một áp đặt rất lớn, nhưng tôi thực sự cần bạn
    để tìm cách hoàn thành công việc này trước sáng thứ Hai. Nó thực sự
    bạo kích. Bạn không thể làm gì sao? "

Vì vậy, bây giờ Peter bắt đầu nghĩ về việc làm thêm giờ đáng kể, và có lẽ là hầu hết các ngày cuối tuần. Anh ấy cần phải rất trung thực với bản thân về sức chịu đựng và dự trữ của mình. Có thể dễ dàng nói rằng bạn sẽ làm được nhiều việc vào cuối tuần, khó hơn rất nhiều để thực sự tập hợp đủ năng lượng để làm công việc chất lượng cao.


Các chuyên gia biết giới hạn của họ. Họ biết họ có thể làm thêm giờ bao nhiêu áp dụng hiệu quả, và họ biết chi phí sẽ là bao nhiêu.

Trong trường hợp này, Peter cảm thấy khá tự tin rằng có thêm vài giờ trong tuần và một số thời gian vào cuối tuần sẽ là đủ.

    Peter: “Được rồi, Marge, tôi sẽ cho bạn biết điều gì. Tôi sẽ gọi về nhà và dọn dẹp một số
    tăng ca với gia đình tôi. Nếu họ đồng ý với nó, thì tôi sẽ hiểu
    nhiệm vụ hoàn thành vào sáng thứ Hai. Tôi thậm chí sẽ đến vào thứ Hai
    buổi sáng để đảm bảo mọi thứ suôn sẻ với Willy. Nhưng sau đó tôi sẽ về nhà và sẽ không trở lại cho đến thứ Tư. Thỏa thuận?"

Điều này là hoàn toàn công bằng. Peter biết rằng anh ấy có thể nhận được các sửa đổi và tài liệu thực hiện nếu anh ta làm việc ngoài giờ. Anh ấy cũng biết anh ấy sẽ vô dụng cho một vài ngày sau đó.

## PHẦN KẾT LUẬN
Các chuyên gia không bắt buộc phải nói có với mọi thứ được yêu cầu về họ. Tuy nhiên, họ nên làm việc chăm chỉ để tìm ra những cách sáng tạo để biến “có” thành khả thi.
Khi các chuyên gia nói có, họ sử dụng ngôn ngữ cam kết để không nghi ngờ gì về những gì họ đã hứa.