# 🏨 Hotel Management System

## 1. Giới thiệu dự án

**Hotel Management System** là dự án xây dựng chương trình quản lý khách sạn bằng ngôn ngữ Java, áp dụng các nguyên lý lập trình hướng đối tượng (Object-Oriented Programming – OOP).

Dự án được thực hiện theo hình thức làm việc nhóm gồm 5 thành viên. Hệ thống hướng đến việc hỗ trợ quản lý các hoạt động cơ bản của khách sạn, bao gồm quản lý phòng, khách hàng, nhân viên, đặt phòng, dịch vụ, hóa đơn và thống kê doanh thu.

Mục tiêu của dự án là vận dụng kiến thức Java OOP vào một bài toán thực tế, rèn luyện kỹ năng thiết kế chương trình, phân chia module, làm việc nhóm và sử dụng Git/GitHub để quản lý mã nguồn.

## 2. Mục tiêu dự án

- Xây dựng chương trình quản lý khách sạn có cấu trúc rõ ràng, dễ sử dụng và dễ mở rộng.
- Áp dụng các nguyên lý OOP: đóng gói (Encapsulation), kế thừa (Inheritance), đa hình (Polymorphism) và trừu tượng (Abstraction).
- Phân chia chương trình thành các module độc lập, có thể phát triển và kiểm thử riêng.
- Quản lý mã nguồn và phối hợp làm việc nhóm thông qua Git và GitHub.
- Tích hợp các module thành một hệ thống thống nhất, đảm bảo các chức năng hoạt động chính xác.

## 3. Chức năng chính

### 3.1. Quản lý phòng (Room Management)

- Thêm phòng mới vào hệ thống.
- Cập nhật thông tin phòng.
- Xóa phòng khi đáp ứng các điều kiện nghiệp vụ.
- Tìm kiếm phòng theo mã phòng.
- Hiển thị danh sách phòng.
- Quản lý loại phòng: Standard, Deluxe, Suite.
- Quản lý trạng thái phòng: Trống, Đang ở, Bảo trì.
- Kiểm tra tình trạng phòng trước khi nhận khách.

### 3.2. Quản lý khách hàng và nhân viên (Person Management)

- Quản lý thông tin khách hàng.
- Quản lý thông tin nhân viên.
- Thêm, cập nhật, tìm kiếm và hiển thị thông tin.
- Xây dựng lớp `Person` làm lớp cơ sở cho `Customer` và `Employee`.
- Tái sử dụng các thuộc tính và phương thức chung thông qua kế thừa.

### 3.3. Quản lý đặt phòng và lưu trú (Booking Management)

- Tạo và quản lý thông tin đặt phòng.
- Gắn thông tin đặt phòng với khách hàng và phòng tương ứng.
- Lưu ngày nhận phòng và ngày trả phòng dự kiến.
- Kiểm tra khả năng đáp ứng phòng trước khi xác nhận đặt phòng.
- Thực hiện thủ tục nhận phòng và trả phòng.
- Cập nhật trạng thái phòng theo tình trạng lưu trú thực tế.
- Ngăn chặn việc đặt hoặc sử dụng trùng phòng trong cùng khoảng thời gian.

### 3.4. Quản lý dịch vụ và hóa đơn (Service & Invoice Management)

- Quản lý danh sách dịch vụ của khách sạn.
- Thêm, cập nhật và tìm kiếm dịch vụ.
- Ghi nhận các dịch vụ khách hàng đã sử dụng.
- Tính chi phí phòng dựa trên thời gian lưu trú và quy định tính giá.
- Tính chi phí dịch vụ dựa trên số lượng và đơn giá.
- Tổng hợp chi phí phòng và dịch vụ thành hóa đơn.
- Hiển thị hoặc in hóa đơn thanh toán.

### 3.5. Tích hợp hệ thống và thống kê (Integration & Statistics)

- Xây dựng menu chính để người dùng lựa chọn chức năng.
- Kết nối các module phòng, khách hàng, đặt phòng, dịch vụ và hóa đơn.
- Kiểm tra tính nhất quán của dữ liệu giữa các module.
- Thống kê số lượng phòng theo trạng thái.
- Thống kê số lượt đặt phòng và lưu trú.
- Tổng hợp doanh thu từ các hóa đơn đã thanh toán.
- Kiểm thử toàn bộ chương trình và hoàn thiện sản phẩm.

*Lưu ý: Các chức năng trên là phạm vi dự kiến. Những chức năng thực tế được hoàn thành sẽ được cập nhật trong quá trình phát triển.*

## 4. Công nghệ sử dụng

| Công nghệ | Mục đích |
|---|---|
| Java | Ngôn ngữ lập trình chính |
| OOP | Thiết kế lớp, đối tượng và tổ chức nghiệp vụ |
| Maven | Quản lý cấu hình và biên dịch dự án |
| Git | Theo dõi lịch sử thay đổi mã nguồn |
| GitHub | Lưu trữ mã nguồn và phối hợp làm việc nhóm |
| Visual Studio Code | Môi trường viết và kiểm thử code |

## 5. Cấu trúc dự án

```text
hotel-management/
├── pom.xml
├── README.md
└── src/
    ├── main/
    │   └── java/
    │       └── com/
    │           └── hotel/
    │               ├── Main.java
    │               ├── room/
    │               ├── person/
    │               ├── booking/
    │               ├── invoice/
    │               └── statistics/
    └── test/
        └── java/
```

### Mô tả các package

- `com.hotel`: Package gốc của ứng dụng.
- `com.hotel.room`: Các lớp và chức năng quản lý phòng.
- `com.hotel.person`: Các lớp khách hàng, nhân viên và quản lý thông tin cá nhân.
- `com.hotel.booking`: Các lớp xử lý đặt phòng, nhận phòng và trả phòng.
- `com.hotel.invoice`: Các lớp quản lý dịch vụ, hóa đơn và tính chi phí.
- `com.hotel.statistics`: Các chức năng tổng hợp và thống kê.
- `Main.java`: Điểm khởi chạy và điều hướng các chức năng của chương trình.
- `pom.xml`: File cấu hình dự án Maven.

## 6. Phân công công việc

Dự án được chia thành 5 phần để các thành viên có thể phát triển và kiểm thử từng module trước khi tích hợp.

### TV1 — Quản lý phòng (Room Module)

**Phạm vi công việc:**
- Thiết kế lớp `Room`.
- Xây dựng enum `RoomType` và `RoomStatus`.
- Xây dựng lớp `RoomManager`.
- Triển khai các chức năng thêm, sửa, xóa, tìm kiếm và hiển thị phòng.
- Kiểm tra tính hợp lệ của thông tin phòng và trạng thái phòng.

**Sản phẩm bàn giao:** Các lớp thuộc package `com.hotel.room` và kết quả kiểm thử module.

### TV2 — Quản lý khách hàng và nhân viên (Person Module)

**Phạm vi công việc:**
- Thiết kế lớp trừu tượng `Person`.
- Xây dựng các lớp `Customer` và `Employee`.
- Triển khai chức năng quản lý thông tin khách hàng và nhân viên.
- Áp dụng kế thừa, đóng gói và các nguyên lý OOP phù hợp.

**Sản phẩm bàn giao:** Các lớp thuộc package `com.hotel.person` và kết quả kiểm thử module.

### TV3 — Quản lý đặt phòng (Booking Module)

**Phạm vi công việc:**
- Thiết kế lớp `Booking`.
- Xây dựng lớp `BookingManager`.
- Triển khai chức năng tạo và quản lý đặt phòng.
- Kiểm tra khả năng đáp ứng của phòng.
- Xử lý nhận phòng, trả phòng và cập nhật trạng thái lưu trú.
- Phối hợp với TV1 và TV2 để sử dụng thông tin phòng và khách hàng.

**Sản phẩm bàn giao:** Các lớp thuộc package `com.hotel.booking` và kết quả kiểm thử module.

### TV4 — Quản lý dịch vụ và hóa đơn (Service & Invoice Module)

**Phạm vi công việc:**
- Thiết kế lớp `Service`.
- Xây dựng các lớp `Invoice` và `InvoiceManager`.
- Quản lý danh sách dịch vụ và ghi nhận dịch vụ đã sử dụng.
- Tính tiền phòng, tiền dịch vụ và tổng chi phí.
- Xây dựng chức năng hiển thị hoặc in hóa đơn.
- Phối hợp với TV3 để lấy thông tin lưu trú phục vụ tính tiền.

**Sản phẩm bàn giao:** Các lớp thuộc package `com.hotel.invoice` và kết quả kiểm thử module.

### TV5 — Tích hợp hệ thống, giao diện và thống kê (Integration & Statistics)

**Phạm vi công việc:**
- Thiết kế menu chính trong `Main.java`.
- Tích hợp các module do TV1–TV4 phát triển.
- Xây dựng các chức năng thống kê tổng hợp.
- Kiểm thử hoạt động của toàn hệ thống.
- Hỗ trợ giải quyết xung đột khi ghép mã nguồn.
- Quản lý tiến độ, cập nhật README và phối hợp hoàn thiện báo cáo.

**Sản phẩm bàn giao:** Chương trình hoàn chỉnh có thể chạy thử, các chức năng tích hợp và tài liệu dự án.

## 7. Quy trình làm việc nhóm

Nhóm sử dụng Git và GitHub để quản lý mã nguồn theo quy trình sau:

1. Chủ repository chuẩn bị cấu trúc dự án và đưa phiên bản ban đầu lên GitHub.
2. Các thành viên tải project về máy sau khi được cấp quyền truy cập.
3. Mỗi thành viên phát triển module được phân công trên nhánh Git riêng.
4. Thường xuyên kiểm tra, biên dịch và kiểm thử code trong quá trình làm việc.
5. Commit các thay đổi với nội dung mô tả rõ ràng.
6. Đẩy nhánh lên GitHub và tạo Pull Request để đề nghị ghép code vào nhánh `main`.
7. Kiểm tra, xử lý xung đột và chạy thử sau khi tích hợp.
8. Cập nhật tài liệu và hoàn thiện sản phẩm trước khi nộp.

### Quy ước làm việc

- Không tự ý sửa hoặc xóa code của thành viên khác khi chưa trao đổi.
- Thống nhất tên lớp, phương thức, thuộc tính và quy tắc nghiệp vụ trước khi tích hợp.
- Không đưa mật khẩu, token hoặc dữ liệu bí mật lên repository.
- Chỉ ghép code sau khi đã kiểm tra các thay đổi và biên dịch thành công.
- Mỗi thành viên chịu trách nhiệm giải thích và bảo trì phần code được giao.

## 8. Hướng dẫn chạy chương trình

### Yêu cầu môi trường

- Đã cài đặt JDK tương thích với cấu hình trong `pom.xml`.
- Đã cài đặt Apache Maven.
- Đã tải project về máy hoặc clone repository từ GitHub.
- Có môi trường phát triển Java, chẳng hạn Visual Studio Code.

### Biên dịch dự án

Mở Terminal tại thư mục chứa `pom.xml`, sau đó chạy:

```bash
mvn clean compile
```

Nếu Maven hiển thị `BUILD SUCCESS`, quá trình biên dịch đã hoàn thành.

### Chạy chương trình

Sau khi lớp `Main.java` được hoàn thiện, có thể chạy theo một trong các cách phù hợp với cấu hình dự án:

```bash
mvn exec:java -Dexec.mainClass="com.hotel.Main"
```

Lệnh trên cần cấu hình plugin Maven Exec trong `pom.xml`. Nếu chưa cấu hình plugin, có thể chạy `Main.java` trực tiếp trong Visual Studio Code hoặc dùng lệnh Java phù hợp với cấu trúc biên dịch.

## 9. Kiểm thử và đánh giá

Nhóm dự kiến kiểm thử các trường hợp sau:

- Thêm phòng hợp lệ và xử lý mã phòng trùng.
- Tìm kiếm phòng không tồn tại.
- Không cho nhận phòng đang bảo trì.
- Không cho đặt trùng phòng trong cùng khoảng thời gian.
- Kiểm tra thông tin khách hàng và nhân viên.
- Tính tiền phòng và tiền dịch vụ chính xác.
- Kiểm tra tổng hóa đơn và doanh thu thống kê.
- Xử lý lựa chọn menu không hợp lệ.
- Biên dịch và chạy thử toàn bộ chương trình sau khi tích hợp.

## 10. Trạng thái dự án

**Trạng thái hiện tại:** Đang trong quá trình phát triển.

Các module đang được chuẩn bị theo kế hoạch phân công. Chức năng thực tế, kết quả kiểm thử và các thay đổi về phạm vi dự án sẽ được cập nhật trong quá trình triển khai.

## 11. Định hướng phát triển

Tùy theo yêu cầu môn học và thời gian thực hiện, dự án có thể được mở rộng với:

- Giao diện đồ họa bằng Java Swing hoặc JavaFX.
- Lưu trữ dữ liệu bằng MySQL hoặc cơ sở dữ liệu khác.
- Phân quyền sử dụng cho nhân viên và quản lý.
- Báo cáo doanh thu theo ngày, tháng hoặc năm.
- Xuất hóa đơn và báo cáo ra file.
- Nâng cao khả năng kiểm thử tự động và xử lý lỗi.

Các tính năng mở rộng chỉ được triển khai khi nhóm thống nhất và các chức năng cốt lõi đã hoạt động ổn định.

---

**Hotel Management System** — Dự án thực hành Java OOP theo nhóm, hướng đến việc xây dựng một chương trình quản lý khách sạn có cấu trúc rõ ràng, dễ kiểm thử và dễ mở rộng.
