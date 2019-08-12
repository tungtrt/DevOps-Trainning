# Design a Network Topology


## Hierarchical Network Design (Thiết kế mạng phân cấp)
- Các chuyên gia thiết kế mạng đã phát triển mô hình mạng phân cấp để giúp phát triển cấu trúc liên kết (topology) trong từng lớp riêng biệt.
- Mỗi lớp có thể tập trung vào những chức năng đặc biệt, cho phép chọn đúng hệ thống và tính năng cho từng lớp.
- Một cấu trúc liên kết phân cấp điển hình là:
  - ***Lớp mạng trung tâm (Core layer):*** Tốc độ vận chuyển dữ liệu nhanh, độ tin cậy cao, có tính dự phòng, khả năng chịu lỗi.
  - ***Lớp mạng phân bố (Distribution layer):*** Nằm giữa lớp mạng truy cập và trung tâm. Có một số vai trò: giúp giảm tải cho lớp mạng trung tâm, chính sách cơ sở kết nối.
  - ***Lớp mạng truy cập (Access layer):*** Kết nối người dùng với các tài nguyên trên mạng hoặc giao tiếp với lớp mạng phân bố.
### Tại sao lại sử dụng mô hình thiết kế mạng phân cấp?
  - Mô hình phân cấp áp dụng cho cả thiết kế mạng LAN và WAN. 
  - Giữ cho thiết kế đơn giản và dễ hiểu => với chức năng rõ ràng ở từng lớp.
  - Hiệu suất cao => ta có thể dễ dàng thiết kế một hệ thống mạng với tốc độ cao. Bởi mỗi layer thực hiện một chức năng khác nhau => giảm thiểu tắc nghẽn vì xử lý nhiều chức năng ở một vị trí.
  - Có khả năng mở rộng => Việc chia nhỏ thành các lớp với mỗi chức năng khác nhau giúp ta dễ dàng nâng cấp khi có yêu cầu mới.
  - Dễ dàng quản lý => mô hình phân chia rõ ràng
  - Dễ dàng sửa lỗi => khi gặp vấn đề về chính sách (policy) tìm đến lớp mạng phân bố để kiểm tra không cần phải kiểm tra các lớp khác.
#### Flat Versus Hierarchical Topologies.
 - Một cấu trúc liên kết mạng phẳng (flat network topology) là đủ cho những hệ thống mạng nhỏ. 
 - Một thiết kế mạng phẳng (flat network design) không có hệ thống cấp bậc => Mỗi thiết bị kết nối mạng làm cùng một việc => và mạng không chia thành các layers hay modules
 - Dễ dàng thiết kế, áp dụng và dễ dàng bảo trì.
 - Tuy nhiên khả năng mở rộng là không khả thi. Thiếu hệ thống phân cấp làm cho việc sửa lỗi khó khăn hơn. Thay vì tập trung sửa lỗi ở một khu vực ta phải sửa lỗi ở toàn bộ hệ thống mạng.
 #### Flat WAN Topologies.
 - Một mạng diện rộng (WAN) cho một công ty nhỏ có thể bao gồm một vài trang web được kết nối với nhau trong một vòng lặp. 
 - Mỗi trang web có bộ định tuyến WAN kết nối với hai trang web riêng biệt thông qua liên kết point-to-point.
 - Các giao thức định tuyến có thể tập trung nhanh chóng, và giao tiếp với các bất kỳ trang web nào khác có thể khi liên kết bị lỗi (Khi chỉ một địa chỉ liên kết bị lỗi giao tiếp vẫn được phục hồi. Khi nhiều hơn một liên kết bị lỗi thì một vài trang web sẽ bị cô lập)
 - Một cấu trúc liên kết vòng phẳng không nên dùng cho những mạng mà có nhiều trang web. => Một cấu trúc liên kết lặp có nghĩa là có nhiều bước nhảy (hops) giữa các bộ định tuyến trên những phía đối diện của vòng lặp => dẫn đến độ trễ và xác xuất thất bại cao hơn.
 - Nếu phân tích cho thấy các bộ định tuyến (router) trên những phía đối diện của một cấu trúc liên kết vòng lặp (loop topology) trao đổi nhiều lưu lượng nên sử dụng cấu trúc liên kết phân cấp (hierarchical topologies).
#### Flat LAN Topologies.
- Vào đầu và giữa những năm 1990 một thiết kế điển hình của mạng LAN là PC và máy chủ được gắn vào một hoặc nhiều hub trong một cấu trúc liên kết phẳng (flat topology).
- Ngày nay các nhà thiết kế mạng khuyên nên gắn PC và máy chủ vào lớp liên kết dữ liệu (data link layer) bộ chuyển mạch thay vì hubs. Trong trường hợp này, mạng được chia thành các miền băng thông nhỏ việc này sẽ làm hạn chế việc số lượng thiết bị cạnh tranh băng thông bất cứ lúc nào.

#### Mesh Versus Hierarchical-Mesh Topologies.
 - Các nhà thiết kế mạng thường đề xuất cấu trúc liên kết lưới để đáp ứng yêu cầu về tính khả dụng.