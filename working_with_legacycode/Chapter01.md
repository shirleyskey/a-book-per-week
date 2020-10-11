# Chapter01: Changing Software
Thay đổi mã là rất tốt. Đó là những gì chúng tôi làm để kiếm sống. Nhưng có những cách
thay đổi mã khiến cuộc sống trở nên khó khăn và có nhiều cách khiến nó
dễ dàng hơn. Trong ngành, chúng tôi chưa nói nhiều về điều đó. Gần nhất chúng ta có
gotten là tài liệu về tái cấu trúc. Tôi nghĩ chúng ta có thể mở rộng cuộc thảo luận
và nói về cách đối phó với mã trong những tình huống khó khăn nhất. Làm
rằng, chúng ta phải tìm hiểu sâu hơn về cơ chế thay đổi.

### Four Reasons to Change Software
Vì mục tiêu đơn giản, hãy cùng xem xét bốn lý do chính để thay đổi phần mềm.
1. Thêm một tính năng
2. Sửa lỗi
3. Cải tiến thiết kế
4. Tối ưu hóa việc sử dụng tài nguyên

##### Adding Features and Fixing Bugs
Thêm một tính năng có vẻ như là kiểu thay đổi dễ thực hiện nhất.
Phần mềm hoạt động theo một cách và người dùng nói rằng hệ thống cần thực hiện một số-
điều khác nữa.
Giả sử rằng chúng tôi đang làm việc trên một ứng dụng dựa trên web và một người quản lý
cho chúng tôi biết rằng cô ấy muốn logo công ty được chuyển từ phía bên trái của trang sang
phía bên phải. Chúng tôi nói chuyện với cô ấy về điều đó và phát hiện ra nó không đơn giản như vậy. Bà ấy
muốn di chuyển logo, nhưng cô ấy cũng muốn có những thay đổi khác. Cô ấy muốn làm nó
hoạt hình cho bản phát hành tiếp theo. Đây là sửa lỗi hay thêm một tính năng mới? Nó
tùy thuộc vào quan điểm của bạn. Từ quan điểm của khách hàng, cô ấy
chắc chắn yêu cầu chúng tôi khắc phục sự cố. Có lẽ cô ấy đã xem trang web và tham dự một
gặp gỡ những người trong bộ phận của cô ấy và họ quyết định thay đổi logo
vị trí và yêu cầu thêm một chút chức năng. Theo quan điểm của nhà phát triển
xem, thay đổi có thể được coi là một tính năng hoàn toàn mới. “Nếu họ chỉ
ngừng thay đổi ý định của họ, chúng tôi sẽ hoàn thành ngay bây giờ. " Nhưng trong một số tổ chức-
việc di chuyển logo chỉ được coi là một bản sửa lỗi, bất kể thực tế là nhóm
sẽ phải làm rất nhiều việc mới.
Thật hấp dẫn để nói rằng tất cả những điều này chỉ là chủ quan. Bạn xem nó như một bản sửa lỗi,
và tôi coi đó là một tính năng và đó là kết thúc của nó. Đáng buồn thay, trong nhiều cơ quan-
zation, sửa lỗi và tính năng phải được theo dõi và tính toán riêng
vì hợp đồng hoặc sáng kiến ​​chất lượng. Ở cấp độ con người, chúng ta có thể quay trở lại
và liên tục về việc liệu chúng tôi đang thêm tính năng hay sửa lỗi, nhưng nó
tất cả chỉ là thay đổi mã và các tạo tác khác. Thật không may, cuộc nói chuyện này về lỗi-
sửa chữa và bổ sung tính năng mặt nạ thứ quan trọng hơn nhiều đối với chúng tôi
về mặt kỹ thuật: thay đổi hành vi. Có một sự khác biệt lớn giữa việc thêm mới
hành vi và thay đổi hành vi cũ.
Hành vi là điều quan trọng nhất của phần mềm. Nó là những gì người dùng phụ thuộc vào.
Người dùng thích điều đó khi chúng tôi thêm hành vi (miễn là họ thực sự muốn), nhưng nếu chúng tôi
thay đổi hoặc loại bỏ hành vi mà họ phụ thuộc vào (giới thiệu lỗi), họ ngừng tin tưởng chúng tôi.
Trong ví dụ về logo của công ty, chúng ta có đang thêm hành vi không? Đúng. Sau
thay đổi, hệ thống sẽ hiển thị logo ở bên phải của trang. Chúng ta có ...
ting loại bỏ bất kỳ hành vi? Có, sẽ không có biểu trưng ở phía bên trái.
Hãy xem xét một trường hợp khó hơn. Giả sử rằng một khách hàng muốn thêm biểu trưng vào
bên phải của một trang, nhưng không có trang nào ở bên trái để bắt đầu. Đúng,
chúng tôi đang thêm hành vi, nhưng chúng tôi có xóa bất kỳ hành vi nào không? Có bất cứ thứ gì được hiển thị
nơi mà logo sắp được hiển thị?
Chúng ta đang thay đổi hành vi, thêm nó hay cả hai?
Nó chỉ ra rằng, đối với chúng tôi, chúng tôi có thể rút ra một sự khác biệt hữu ích hơn cho chúng tôi là
lập trình viên. Nếu chúng ta phải sửa đổi mã (và loại HTML được tính là mã),
chúng ta có thể thay đổi hành vi. Nếu chúng tôi chỉ thêm mã và gọi nó, chúng tôi đang
thường thêm hành vi. Hãy xem một ví dụ khác. Đây là một phương pháp trên một
Lớp Java:
CDPlayer lớp công cộng
{
public void addTrackListing (Theo dõi bản nhạc) {
...
}
...
}
Lớp có một phương thức cho phép chúng tôi thêm danh sách theo dõi. Hãy thêm
một phương pháp khác cho phép chúng tôi thay thế danh sách theo dõi.

CDPlayer lớp công cộng
{
public void addTrackListing (Theo dõi bản nhạc) {
...
}
5
Bốn lý do
thay đổi
Phần mềm
public void ReplaceTrackLists (String name, Track track) {
...
}
...
}
Khi chúng tôi thêm phương thức đó, chúng tôi đã thêm hành vi mới vào ứng dụng của mình hay
thay đổi nó? Câu trả lời là: không. Thêm một phương pháp không thay đổi hành vi
trừ khi phương thức được gọi bằng cách nào đó.
Hãy thực hiện một thay đổi mã khác. Hãy đặt một nút mới trên giao diện người dùng
cho đầu đĩa CD. Nút cho phép người dùng thay thế danh sách bản nhạc. Với động thái đó,
chúng tôi đang thêm hành vi mà chúng tôi đã chỉ định trong phương thức ReplaceTrackListing, nhưng chúng tôi
cũng thay đổi hành vi một cách tinh vi. Giao diện người dùng sẽ hiển thị khác với nhưng-
tấn. Rất có thể, giao diện người dùng sẽ mất khoảng một micro giây để hiển thị. Nó
dường như gần như không thể thêm hành vi mà không thay đổi nó ở một mức độ nào đó.

##### Improving Design
Cải tiến thiết kế là một dạng thay đổi phần mềm khác. Khi chúng ta muốn
thay đổi cấu trúc của phần mềm để làm cho nó dễ bảo trì hơn, nói chung chúng tôi muốn
cũng giữ nguyên hành vi của nó. Khi chúng ta bỏ hành vi trong quá trình đó, chúng ta thường
gọi đó là một lỗi. Một trong những lý do chính khiến nhiều lập trình viên không thử
để cải thiện thiết kế thường là vì nó tương đối dễ dàng để mất hành vi hoặc tạo
hành vi xấu trong quá trình thực hiện.
Hành động cải tiến thiết kế mà không thay đổi hành vi của nó được gọi là refactor-
ing. Ý tưởng đằng sau việc tái cấu trúc là chúng ta có thể làm cho phần mềm được bảo trì tốt hơn-
có thể mà không thay đổi hành vi nếu chúng tôi viết thử nghiệm để đảm bảo rằng
hành vi không thay đổi và thực hiện các bước nhỏ để xác minh rằng tất cả các
thuế. Mọi người đã làm sạch mã trong hệ thống trong nhiều năm, nhưng chỉ trong
một vài năm đã bắt đầu tái cấu trúc. Tái cấu trúc khác với dọn dẹp chung ở
rằng chúng tôi không chỉ làm những việc có rủi ro thấp như định dạng lại mã nguồn hoặc
những thứ xâm lấn và rủi ro chẳng hạn như viết lại các đoạn của nó. Thay vào đó, chúng tôi đang làm
một loạt các sửa đổi cấu trúc nhỏ, được hỗ trợ bởi các bài kiểm tra để tạo mã
dễ thay đổi hơn. Điều quan trọng của việc tái cấu trúc theo quan điểm thay đổi là
rằng sẽ không có bất kỳ thay đổi chức năng nào khi bạn cấu trúc lại
(mặc dù hành vi có thể thay đổi phần nào do cấu trúc thay đổi
bạn thực hiện có thể thay đổi hiệu suất, tốt hơn hoặc tệ hơn).

##### Optimization
Tối ưu hóa giống như tái cấu trúc, nhưng khi chúng tôi làm điều đó, chúng tôi có một mục tiêu khác.
Với cả tái cấu trúc và tối ưu hóa, chúng tôi nói, "Chúng tôi sẽ giữ chức năng-
sự đồng minh giống hệt nhau khi chúng tôi thực hiện thay đổi, nhưng chúng tôi sẽ thay đổi
thứ gì khác." Trong cấu trúc lại, "cái gì đó khác" là cấu trúc chương trình; chúng tôi
muốn bảo trì dễ dàng hơn. Trong tối ưu hóa, "cái gì đó khác" là
một số tài nguyên được chương trình sử dụng, thường là thời gian hoặc bộ nhớ.

##### Putting It All Together
Có vẻ lạ khi cấu trúc lại và tối ưu hóa giống nhau.
Chúng có vẻ gần gũi với nhau hơn nhiều so với việc bổ sung các tính năng hoặc sửa lỗi. Nhung la
điều này thực sự đúng? Điểm chung giữa tái cấu trúc và tối ưu hóa-
tion là chúng tôi giữ chức năng bất biến trong khi chúng tôi để một thứ khác thay đổi.
Nói chung, ba điều khác nhau có thể thay đổi khi chúng ta làm việc trong một hệ thống:
cấu trúc, chức năng và sử dụng tài nguyên.
Hãy xem những gì thường thay đổi và những gì vẫn giữ nguyên
khi chúng tôi thực hiện bốn loại thay đổi khác nhau (vâng, thường thì cả ba loại thay đổi, nhưng
hãy xem những gì là điển hình):

Bề ngoài, cấu trúc lại và tối ưu hóa trông rất giống nhau. Họ nắm giữ
chức năng bất biến. Nhưng điều gì sẽ xảy ra khi chúng ta tính đến chức năng mới-
ity riêng? Khi chúng tôi thêm một tính năng, chúng tôi thường thêm chức năng mới,
nhưng không thay đổi chức năng hiện có.
Thêm tính năng, tái cấu trúc và tối ưu hóa, tất cả đều giữ chức năng hiện có
bất biến. Trên thực tế, nếu chúng tôi xem xét kỹ lưỡng việc sửa lỗi, vâng, nó sẽ thay đổi chức năng,
nhưng những thay đổi thường rất nhỏ so với số lượng func-
màu sắc không bị thay đổi.
Việc bổ sung tính năng và sửa lỗi rất giống với việc tái cấu trúc và tối ưu hóa-
sự. Trong cả bốn trường hợp, chúng tôi muốn thay đổi một số chức năng, một số hành vi,
nhưng chúng tôi muốn bảo tồn nhiều hơn nữa (xem Hình 1.1).
Đó là một cái nhìn tốt đẹp về những gì sẽ xảy ra khi chúng tôi thực hiện các thay đổi,
nhưng thực tế nó có ý nghĩa gì đối với chúng ta? Về mặt tích cực, nó dường như cho chúng ta biết
những gì chúng ta phải tập trung vào. Chúng tôi phải đảm bảo rằng số lượng nhỏ
những thứ mà chúng tôi thay đổi được thay đổi một cách chính xác. Về mặt tiêu cực, tốt, rằng
không phải là điều duy nhất chúng tôi phải tập trung vào. Chúng ta phải tìm ra cách
bảo toàn phần còn lại của hành vi. Thật không may, việc bảo quản nó liên quan đến nhiều hơn
hơn là chỉ để lại mã một mình. Chúng ta phải biết rằng hành vi không
thay đổi, và điều đó có thể khó khăn. Số lượng hành vi mà chúng ta phải
phục vụ thường rất lớn, nhưng đó không phải là vấn đề lớn. Vấn đề lớn là chúng tôi
thường không biết hành vi đó có bao nhiêu rủi ro khi chúng tôi thực hiện
những thay đổi. Nếu chúng tôi biết, chúng tôi có thể tập trung vào hành vi đó và không quan tâm đến
phần còn lại. Hiểu biết là điều quan trọng mà chúng ta cần thực hiện thay đổi một cách an toàn.
Duy trì hành vi hiện có là một trong những thách thức lớn nhất trong phát triển phần mềm.
Ngay cả khi chúng tôi đang thay đổi các tính năng chính, chúng tôi thường có những khu vực rất lớn
hành vi mà chúng ta phải giữ gìn.

### Risky Change
Hành vi bảo tồn là một thách thức lớn. Khi nào chúng ta cần thay đổi và
bảo tồn hành vi, nó có thể liên quan đến rủi ro đáng kể.
Để giảm thiểu rủi ro, chúng ta phải đặt ra ba câu hỏi:
1. Chúng tôi phải thực hiện những thay đổi nào?
2. Làm thế nào chúng ta biết rằng chúng ta đã làm đúng?
3. Làm thế nào chúng ta biết rằng chúng ta không bị hỏng bất cứ thứ gì?
Bạn có thể chi trả bao nhiêu tiền thay đổi nếu những thay đổi có rủi ro?
Hầu hết các nhóm mà tôi đã làm việc cùng đã cố gắng quản lý rủi ro một cách rất thận trọng-
cách vative. Họ giảm thiểu số lượng thay đổi mà họ thực hiện đối với mã
căn cứ. Đôi khi đây là chính sách của nhóm: ��œNếu nó không bị hỏng, đừng sửa nó. " Tại khác
thời gian, nó không phải là bất cứ điều gì mà bất cứ ai nói rõ. Các nhà phát triển chỉ rất cau-
khó chịu khi họ thay đổi. "Gì? Tạo một phương pháp khác cho điều đó? Không,
Tôi sẽ chỉ đặt các dòng mã ngay tại đây trong phương thức, nơi tôi có thể thấy chúng và
phần còn lại của mã. Nó ít phải chỉnh sửa hơn và an toàn hơn ”.
Thật hấp dẫn khi nghĩ rằng chúng ta có thể giảm thiểu các sự cố phần mềm bằng cách tránh
nhưng, thật không may, nó luôn bắt kịp chúng ta. Khi chúng ta tránh tạo
các lớp và phương thức mới, những lớp hiện có phát triển lớn hơn và khó hơn
đứng. Khi bạn thực hiện các thay đổi trong bất kỳ hệ thống lớn nào, bạn có thể thực hiện
ít thời gian để làm quen với lĩnh vực bạn đang làm việc. Sự khác biệt
giữa hệ thống tốt và hệ thống xấu là ở những hệ thống tốt, bạn cảm thấy khá
bình tĩnh sau khi bạn hoàn thành việc học đó và bạn tự tin vào sự thay đổi của mình
sắp thực hiện. Trong mã có cấu trúc kém, chuyển từ việc tìm ra mọi thứ
để thực hiện các thay đổi giống như nhảy khỏi vách đá để tránh hổ. Bạn do dự và
do dự. “Tôi đã sẵn sàng làm chưa? Chà, tôi đoán là tôi phải làm vậy. ”
Tránh thay đổi gây ra những hậu quả xấu khác. Khi mọi người không làm
thay đổi thường xuyên họ bị gỉ ở nó. Chia nhỏ một lớp lớn thành nhiều mảnh có thể
công việc khá liên quan trừ khi bạn làm nó một vài lần một tuần. Khi bạn làm, nó
trở thành thông lệ. Bạn giỏi hơn trong việc tìm ra những gì có thể phá vỡ và những gì không thể,
và nó dễ thực hiện hơn nhiều.
Hệ quả cuối cùng của việc tránh thay đổi là sợ hãi. Thật không may, nhiều đội
sống với nỗi sợ hãi về sự thay đổi đáng kinh ngạc và nó trở nên tồi tệ hơn mỗi ngày. Thường thì họ không
nhận thức được mức độ sợ hãi của họ cho đến khi họ học được các kỹ thuật tốt hơn và
nỗi sợ hãi bắt đầu biến mất.
Chúng ta đã nói về việc tránh thay đổi là một điều xấu, nhưng chúng ta
thay thế? Một thay thế là chỉ cần cố gắng nhiều hơn. Có lẽ chúng ta có thể thuê thêm peo-
cầu xin để mọi người có đủ thời gian ngồi phân tích, xem xét kỹ lưỡng tất cả
của mã và thực hiện các thay đổi theo cách “đúng đắn”. Chắc chắn phải mất nhiều thời gian và xem xét kỹ lưỡng hơn
sẽ giúp thay đổi an toàn hơn. Hay nó sẽ? Sau tất cả những sự soi mói đó, liệu có ai biết được
rằng họ đã hiểu đúng không?



