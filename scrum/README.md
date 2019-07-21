# SCRUM :star2:

## Table of contents
<!--ts-->
* [Definenation](#define)
* [Manifesto](#manifesto)
* [Scrum Team](#team)
  * [Scrum master](#team1)
  * [Product Owner](#team2)
  * [Development Team](#team3)
* [Sprint](#sprint)
* [Artifacts](#artifacts)
  * [Produck Backlog](#artifact1)
  * [Sprint Backlog](#artifact2)
  * [Increament](#artifact3)
* [Scrum Events](#event)
  * [Sprint Planning](#event1)
  * [Daily Scrum](#event2)
  * [Sprint Review](#event3)
  * [Retrospective Meeting](#event4)
* [Ứng dụng scrum trong 1 team DEV](#ungdung)
<!--te-->

![SCRUM](/images/sprint.png)

<a name="define"></a>
## Definenation :book:
- Là một phương thức phát triển phần mềm, angile framework (framework ở đây là khung làm việc va nó không hiện hữu không phải là các framework như bootstrap, spring, strut ... có thể cài đặt đc).
- Scrum giúp giải quyết các vấn đề phức tạp, cung cấp các sản phẩm có giá trị cao nhất, chia nhỏ phần mềm thành nhiều phần để phát triển và đơn giản dễ hiểu.
<a name="manifesto"></a>
## Manifesto :scroll:
- Scrum là một phương pháp linh hoạt(agile), vì thế nó tuân thủ theo các nguyên tắc của Agile Manifesto. Có bốn tuyên ngôn như sau:
  - ***Cá nhân và sự tương hỗ quan trọng hơn quy trình và công cụ:*** Đó là sự quan trọng về con người và sự tương hỗ, hỗ trợ nhau giữa các thành viên trong nhóm thể hiện ở trong daily meeting, sự gắn kết và thống nhất giữa các thành viên đóng vai trò quyết định sự thành công hay thất bại của dự án.
  - ***Phần mềm chạy tốt hơn là tài liệu đầy đủ:*** Đó là chỉ viết về những gì mọi người cần để đọc, trong quy trình phát triển phần mềm ta thường thấy phải viết nhiều tài liệu để có thể bắt đầu xây dựng phần mềm. Tuy nhiên điều mà khách hàng quan tâm đó chỉ là phần mềm có chạy tốt hay không, có ổn định hay không.
  - ***Cộng tác với khách hàng hơn là đàm phán hợp đồng:***  Đó là khách hàng thì có nhiều loại khách hàng, mỗi người đều có tính cách và hiểu biết khác nhau vì vậy nên cố gắng hiểu rõ khách hàng cần gì và muốn gì để có thể tư vấn hơn là chỉ chăm chăm tuân theo các điều khoản của hợp đồng.
  - ***Phản hồi với sự thay đổi quan trọng hơn bám theo kế hoạch:*** Trong khi xây dựng phần mềm không phải phần mềm nào cũng đi đúng với hướng thiết kế của nó hay kể cả là thay đổi về nhân sự, deadline, công nghệ vì vậy ta phải thích nghi với mỗi thay đổi đó.
 <a name="team"></a>
## Scrum Team
Scrum team bao gồm:
- Scrum master (SM). 👨‍🏫
- Product Owner (PO). :man:
- Development Team. 👨‍👨‍👦‍👦
<a name="team1"></a>
### Scrum master 👨‍🏫
- Chịu trách nhiệm đảm bảo mọi người hiểu và dùng được Scrum.
- Tối đa hóa giá trị của sản phẩm mà team làm ra.
- Giúp cho những người ngoài team tương tác với nhóm một cách hiệu quả nhất.
- Vừa là boss vừa là phục vụ.
<a name="team2"></a>
### Product Owner :man:
- Là người có tầm nhìn về sản phẩm (hiểu rõ sản phẩm) sau đó cung cấp tầm nhìn đó cho team. Thông thường người đảm nhiệm vai trò này thường là khách hàng, nếu khách hàng không có người đảm nhiệm thì sẽ do vị trí BA(Bussiness Analyst) của công ty hay của đơn vị đảm nhiệm.
- Chịu trách nhiệm về giá trị cao nhất của kết quả sản phẩm nhận đc từ team dev.
- Chịu trách nhiệm quản lý backlog:
   - Mô tả nội dung các mục trong backlog.
   - Thứ tự các mục trong backlog để có thể đạt đc mục đích và hiệu quả công việc.
   - Đảm bảo team dev hiểu rõ các mục trong backlog.
- Nếu muốn thay đổi thứ tự các hạng mục thì phải thuyết phục được PO.
- Team dev không đc phép làm theo lời bất cứ ai khác ngoài PO (EX: PO yêu cầu làm feature A thì lại nghe theo ông SM làm feature B).
<a name="team3"></a>
### Development Team 👨‍👨‍👦‍👦
- Là nhóm dự án thành phần chủ lực để phát triển dự án, nhóm từ 3-6 người để vận hành cho năng suất cao.
- Tập hợp những người có đủ kiến thức và kỹ năng như (frontend, backend, tester, mobile dev, phân tích thiết kế hệ thống...).
- Làm việc với Product Owner xem làm những gì trong sprint này để nâng cao giá trị sản phẩm và báo cáo công việc hàng ngày.
<a name="sprint"></a>
## Sprint :milky_way:
- Có thể hiểu là một chu kỳ làm việc kéo dài từ 1 đến 4 tuần. Sprint còn được gọi là trái tim của agile scrum mỗi sprint này còn tùy thuộc vào lượng công việc đầu vào mà quyết định kéo dài trong bao lâu.
<a name="artifacts"></a>
## Artifacts – Các công cụ :wrench:
<a name="artifact1"></a>
### Produck Backlog
- Đây là danh sách các việc mà team phải làm để hoàn thành sản phẩm.
- Do Product Owner quyết định và nó thường xuyên đc thay đổi để đáp ứng nhu cầu thay đổi khách hàng.
<a name="artifact2"></a>
### Sprint Backlog
- Ở đầu sprint, team sẽ có một cuộc họp (sprint planning meeting) để chọn ra những mục quan trọng trong product backlog để tạo thành sprint backlog.
- Khi có việc mới team dev sẽ đưa vào sprint backlog, các thành viên trong team dev sẽ lựa chọn task và ước lượng thời gian hoàn thành và chịu trách nhiệm sau đó update vào sprint backlog.
<a name="artifact3"></a>
### Increment
- Tập hợp những product backlog đã hoàn thành trong suốt sprint hiện tại và trước đó.
- Đáp ứng điều kiện hoàn thành để ông Product Owner có thể release nó.
<a name="event"></a>
## Scrum Events :stars:
<a name="event1"></a>
### Sprint Planning
- Là một cuộc họp mà bên dev sẽ gặp gỡ ông Product Owner để lên kế hoạch làm việc trong sprint backlog dưới sự tham gia của ông Scrum Master người tạo điều kiện cho cuộc họp.
- Bao gồm phân tích các yêu phải phát triển, và phải thực hiện thế nào trong sprint (Giúp team xác định công việc).
<a name="event2"></a>
### Daily Scrum
- Là cuộc họp hàng ngày của team dev thường kéo dài 15p giúp các thành viên nắm đc tình hình của công việc.
- Trả lời 3 câu hỏi:
  - Hôm qua đã làm đc gì? 
  - Hôm nay ta sẽ làm gì?
  - Đang có những issues gì và vướng mắc gì?
<a name="event3"></a>
### Sprint Review
- Sprint review diễn ra sau khi kết thúc một sprint, xem những gì đã hoàn thành hay là chưa.
- Nhóm scrum và các bên liên quan sẽ trao đổi vs nhau về những gì hoàn thành.
- Thảo luận về các công việc sẽ triển khai trong sprint tiếp theo.
<a name="event4"></a>
### Retrospective Meeting
- Là một cuộc họp mà diễn ra sau Sprint Review.
- Trong cuộc họp này cả team cùng nhìn lại tất cả các yếu tố diễn ra trong sprint vừa qua(con người,công việc...) các điểm gì đã đc và chưa đc và đề xuất nhau cải tiến
<a name="ungdung"></a>
## Ứng dụng scrum trong 1 team DEV
Ví dụ về một vụ DEVOPS-TRAINING:
- Truyện kể về việc a Tùng training devops cho duonghx và chị nhaivt thì anh Tùng có áp dụng scrum vào team tạm gọi là team Training. Ở đây a Tùng sẽ đóng vai trò là PO(Product Owner) bởi anh có tầm nhìn về sản phẩm ở trong trường hợp này sản phẩm ở đây là tầm nhìn về những kiến thức và sẽ cung cấp tầm nhìn đó cho dev team(ở đây là duonghx và chị nhaivt). Khi bắt đầu một sprint thì vào hôm thứ 4, anh Tùng có gọi duonghx và chị nhaivt để tổ chức một buổi họp là Sprint Planning Meeting. Trong cuộc họp này a Tùng đã tạo ra một Product Backlog là những việc team cần phải làm để hoàn thành công việc. Sau khi bàn bạc thì những task để chọn vào sprint backlog(tab to-do trên github) đó là “Scrum agile là gì và ứng dụng trong 1 team dev” và “gitflow trong development”. Sau buổi họp duonghx và chị nhaivt đã bàn và chọn task để làm, sau khi chọn task mỗi người sẽ tự ước lượng khoảng thời gian hoàn thành công việc và phải có trách nhiệm với ước lượng này và sau đó báo về time hoàn thành công việc cho anh Tùng sau đó anh Tùng sẽ dựa vào time này để ước lượng cho khoảng thời gian hoàn thành dự án trong Sprint Review, và mỗi ngày sẽ có một cuộc họp Daily Meeting tầm 15 phút trong team dev để biết tiến độ công việc và để trả lời các câu hỏi về việc hôm qua đã làm những gì? Hôm nay sẽ làm gì ? Đang gặp khó khăn hay issues gì? Ví dụ : hôm qua đã làm task về scrum và hôm nay sẽ tìm hiểu tiếp về scrum và duonghx đang không hiểu scrum là cái gì. Sau khi kết thúc một sprint, ở đây 1 sprint là tầm 1- 4 tuần mà hôm trc em thấy a Tùng bảo 1 tuần thì phải, team dev đã làm xong 1 số chức năng hoàn chỉnh đã sẵn sàng để chuyển giao cho khách hàng. Ở ví dụ này là khi hoàn thành các task đã sẵn sàng chuyển giao cho a Tùng review (Sprint review) anh Tùng sẽ đánh giá các công việc nào đã hoàn thành hay là chưa. Sau đó thảo luận về các công việc sẽ đc triển khai tiếp trong sprint sau. Cuối cùng cả nhóm cùng tham gia Retrospective Meeting để đánh giá những yếu tố đã xảy ra trong sprint vừa qua và cả team đã làm tốt và hoàn thiện đúng thời gian hay không... Sau đó để xuất ra một số cải tiến để tăng hiệu suất làm việc.
