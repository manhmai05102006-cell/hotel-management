# 🏨 Hotel Management System

## 1. Giới thiệu dự án

**Hotel Management System** là ứng dụng quản lý khách sạn được xây dựng bằng ngôn ngữ Java, áp dụng các nguyên lý lập trình hướng đối tượng (Object-Oriented Programming – OOP).

Dự án được thực hiện theo nhóm 5 thành viên trong khuôn khổ bài tập lớn môn Lập trình hướng đối tượng. Ứng dụng hướng đến việc hỗ trợ quản lý các hoạt động cơ bản của khách sạn, bao gồm quản lý phòng, khách hàng, nhân viên, đặt phòng, dịch vụ, hóa đơn và thống kê doanh thu.

Mục tiêu của dự án là vận dụng kiến thức Java OOP để giải quyết một bài toán thực tế, rèn luyện kỹ năng thiết kế lớp, tổ chức chương trình theo module, kiểm thử phần mềm và phối hợp phát triển bằng Git/GitHub.

## 2. Mục tiêu dự án

- Xây dựng ứng dụng quản lý khách sạn bằng Java.
- Vận dụng các nguyên lý OOP: đóng gói (Encapsulation), kế thừa (Inheritance), đa hình (Polymorphism) và trừu tượng (Abstraction).
- Thiết kế các lớp có trách nhiệm rõ ràng, hạn chế phụ thuộc không cần thiết giữa các module.
- Tổ chức mã nguồn có cấu trúc, thuận tiện cho việc phát triển, kiểm thử và bảo trì.
- Phối hợp làm việc nhóm thông qua Git và GitHub.
- Hoàn thiện sản phẩm và báo cáo mô tả công nghệ sử dụng, quá trình xây dựng và kết quả đạt được.

## 3. Chức năng của ứng dụng

### 3.1. Quản lý phòng (Room Management)

- Thêm, sửa và xóa thông tin phòng.
- Tìm kiếm phòng theo mã phòng hoặc loại phòng.
- Hiển thị danh sách phòng.
- Quản lý loại phòng: Standard, Deluxe, Suite.
- Quản lý trạng thái phòng: Trống, Đang ở, Bảo trì.
- Kiểm tra trạng thái phòng trước khi thực hiện đặt phòng.

### 3.2. Quản lý khách hàng và nhân viên (Person Management)

- Quản lý thông tin khách hàng.
- Quản lý thông tin nhân viên.
- Thêm, sửa, xóa và tìm kiếm thông tin.
- Xây dựng lớp trừu tượng `Person` làm lớp cơ sở cho `Customer` và `Employee`.
- Áp dụng kế thừa và đóng gói để tái sử dụng các thuộc tính, phương thức chung.

### 3.3. Quản lý đặt phòng (Booking Management)

- Tạo và quản lý thông tin đặt phòng.
- Liên kết đặt phòng với khách hàng và phòng.
- Lưu ngày nhận phòng và ngày trả phòng dự kiến.
- Kiểm tra tình trạng phòng trước khi xác nhận.
- Thực hiện nhận phòng và trả phòng.
- Cập nhật trạng thái phòng theo tình trạng lưu trú.

### 3.4. Quản lý dịch vụ và hóa đơn (Service & Invoice Management)

- Quản lý danh sách dịch vụ của khách sạn.
- Ghi nhận các dịch vụ khách hàng sử dụng.
- Tính tiền phòng theo thời gian lưu trú.
- Tính tiền dịch vụ dựa trên số lượng và đơn giá.
- Tổng hợp chi phí thành hóa đơn.
- Hiển thị hóa đơn thanh toán.

### 3.5. Tích hợp hệ thống và thống kê (Integration & Statistics)

- Xây dựng menu chính để người dùng lựa chọn chức năng.
- Tích hợp các module quản lý phòng, khách hàng, đặt phòng, dịch vụ và hóa đơn.
- Thống kê số lượng phòng theo trạng thái.
- Thống kê lượt đặt phòng và lưu trú.
- Tổng hợp doanh thu từ hóa đơn đã thanh toán.
- Kiểm thử các chức năng và xử lý lỗi đầu vào.

*Lưu ý: Danh sách trên là phạm vi chức năng dự kiến. Nhóm sẽ cập nhật những chức năng thực tế đã hoàn thành trong quá trình phát triển.*

## 4. Công nghệ và công cụ sử dụng

| Công nghệ/Công cụ | Mục đích |
|---|---|
| Java | Ngôn ngữ lập trình chính |
| OOP | Thiết kế lớp, đối tượng và tổ chức nghiệp vụ |
| Java Collections Framework | Quản lý danh sách phòng, khách hàng, đặt phòng và hóa đơn |
| Maven | Quản lý cấu hình, thư viện và biên dịch dự án |
| Git | Theo dõi lịch sử thay đổi mã nguồn |
| GitHub | Lưu trữ mã nguồn và phối hợp làm việc nhóm |
| Visual Studio Code | Môi trường viết, chạy và kiểm thử chương trình |

Các thư viện, framework hoặc công nghệ bổ sung sẽ được cập nhật nếu nhóm thực sự sử dụng trong quá trình triển khai.

## 5. Thiết kế hướng đối tượng

Dự án vận dụng các nguyên lý OOP thông qua việc xây dựng các lớp có nhiệm vụ riêng biệt:

- **Đóng gói (Encapsulation):** sử dụng thuộc tính `private` và các phương thức phù hợp để kiểm soát dữ liệu.
- **Kế thừa (Inheritance):** `Customer` và `Employee` kế thừa từ lớp `Person`.
- **Trừu tượng (Abstraction):** sử dụng lớp trừu tượng `Person` để mô tả những đặc điểm chung của con người trong hệ thống.
- **Đa hình (Polymorphism):** áp dụng khi có nhu cầu xử lý các đối tượng thuộc những lớp khác nhau thông qua kiểu dữ liệu chung.

Các nguyên lý trên sẽ được thể hiện trong mã nguồn tùy theo thiết kế và chức năng thực tế của từng module.

## 6. Cấu trúc dự án

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
- `com.hotel.room`: Các lớp quản lý phòng.
- `com.hotel.person`: Các lớp khách hàng, nhân viên và thông tin cá nhân.
- `com.hotel.booking`: Các lớp xử lý đặt phòng, nhận phòng và trả phòng.
- `com.hotel.invoice`: Các lớp quản lý dịch vụ, hóa đơn và tính chi phí.
- `com.hotel.statistics`: Các chức năng tổng hợp và thống kê.
- `Main.java`: Điểm khởi chạy và điều hướng các chức năng.
- `pom.xml`: File cấu hình dự án Maven.

## 7. Phân công công việc

### TV1 — Quản lý phòng

- Thiết kế lớp `Room`.
- Xây dựng enum `RoomType` và `RoomStatus`.
- Xây dựng lớp `RoomManager`.
- Triển khai chức năng thêm, sửa, xóa, tìm kiếm và hiển thị phòng.
- Kiểm tra tính hợp lệ của thông tin phòng.

**Sản phẩm bàn giao:** Các lớp thuộc package `com.hotel.room` và kết quả kiểm thử module.

### TV2 — Quản lý khách hàng và nhân viên

- Thiết kế lớp trừu tượng `Person`.
- Xây dựng các lớp `Customer` và `Employee`.
- Xây dựng chức năng quản lý khách hàng và nhân viên.
- Áp dụng kế thừa, đóng gói và các nguyên lý OOP phù hợp.

**Sản phẩm bàn giao:** Các lớp thuộc package `com.hotel.person` và kết quả kiểm thử module.

### TV3 — Quản lý đặt phòng

- Thiết kế lớp `Booking`.
- Xây dựng lớp `BookingManager`.
- Triển khai chức năng tạo và quản lý đặt phòng.
- Kiểm tra tình trạng phòng trước khi xác nhận.
- Xử lý nhận phòng, trả phòng và cập nhật trạng thái phòng.
- Phối hợp với TV1 và TV2 để sử dụng dữ liệu phòng và khách hàng.

**Sản phẩm bàn giao:** Các lớp thuộc package `com.hotel.booking` và kết quả kiểm thử module.

### TV4 — Quản lý dịch vụ và hóa đơn

- Thiết kế lớp `Service`.
- Xây dựng các lớp `Invoice` và `InvoiceManager`.
- Quản lý danh sách dịch vụ và ghi nhận dịch vụ đã sử dụng.
- Tính tiền phòng, tiền dịch vụ và tổng chi phí.
- Xây dựng chức năng hiển thị hóa đơn.
- Phối hợp với TV3 để sử dụng thông tin đặt phòng và lưu trú.

**Sản phẩm bàn giao:** Các lớp thuộc package `com.hotel.invoice` và kết quả kiểm thử module.

### TV5 — Tích hợp hệ thống, menu và thống kê

- Xây dựng menu chính trong `Main.java`.
- Tích hợp các module do TV1–TV4 phát triển.
- Xây dựng các chức năng thống kê tổng hợp.
- Kiểm thử hoạt động của toàn bộ chương trình.
- Hỗ trợ xử lý xung đột khi ghép mã nguồn.
- Phối hợp cập nhật README và hoàn thiện báo cáo.

**Sản phẩm bàn giao:** Chương trình hoàn chỉnh có thể chạy thử, các chức năng tích hợp và tài liệu dự án.

## 8. Quy trình xây dựng ứng dụng

Nhóm triển khai dự án theo các bước:

1. **Khảo sát và xác định yêu cầu:** xác định các nghiệp vụ cơ bản của hệ thống quản lý khách sạn.
2. **Phân tích và thiết kế:** xác định các lớp, thuộc tính, phương thức, mối quan hệ kế thừa và cách các module phối hợp.
3. **Khởi tạo dự án:** tạo cấu trúc Java/Maven và repository trên GitHub.
4. **Phát triển từng module:** mỗi thành viên thực hiện phần việc được phân công.
5. **Kiểm thử module:** kiểm tra chức năng và xử lý các trường hợp đầu vào không hợp lệ.
6. **Tích hợp:** ghép các module, kiểm tra sự tương thích giữa các lớp và phương thức.
7. **Kiểm thử toàn hệ thống:** chạy thử các nghiệp vụ từ quản lý phòng đến lập hóa đơn.
8. **Hoàn thiện sản phẩm và báo cáo:** cập nhật chức năng thực tế, kết quả kiểm thử, hình ảnh minh họa và những hạn chế còn tồn tại.

## 9. Quy trình làm việc với GitHub

1. Chủ repository chuẩn bị cấu trúc dự án và đưa phiên bản ban đầu lên GitHub.
2. Các thành viên tải dự án về máy sau khi được cấp quyền truy cập.
3. Mỗi thành viên phát triển module trên nhánh Git riêng.
4. Thường xuyên biên dịch, kiểm thử và commit các thay đổi.
5. Đẩy nhánh lên GitHub và tạo Pull Request.
6. Kiểm tra thay đổi, xử lý xung đột và tích hợp vào nhánh `main`.
7. Chạy thử toàn bộ chương trình sau mỗi đợt tích hợp.
8. Cập nhật tài liệu trước khi hoàn thiện và nộp bài.

### Quy ước làm việc

- Thống nhất tên lớp, phương thức và thuộc tính trước khi tích hợp.
- Không tự ý sửa hoặc xóa code của thành viên khác khi chưa trao đổi.
- Không đưa mật khẩu, token hoặc thông tin bí mật lên GitHub.
- Kiểm tra code trước khi tạo Pull Request.
- Mỗi thành viên chịu trách nhiệm giải thích phần code được giao.

## 10. Hướng dẫn biên dịch và chạy chương trình

### Yêu cầu môi trường

- JDK tương thích với cấu hình trong `pom.xml`.
- Apache Maven.
- Visual Studio Code cùng các extension Java cần thiết.
- Git để quản lý mã nguồn.

### Biên dịch dự án

Mở Terminal tại thư mục chứa `pom.xml` và chạy:

```bash
mvn clean compile
```

Nếu hiển thị `BUILD SUCCESS`, dự án đã biên dịch thành công.

### Chạy chương trình

Sau khi hoàn thiện `Main.java`, có thể chạy trực tiếp trong Visual Studio Code hoặc sử dụng Maven nếu đã cấu hình plugin tương ứng:

```bash
mvn exec:java -Dexec.mainClass="com.hotel.Main"
```

Lệnh Maven trên cần có cấu hình plugin Exec trong `pom.xml`.

## 11. Kiểm thử và đánh giá

Nhóm dự kiến kiểm thử các trường hợp:

- Thêm phòng hợp lệ và xử lý mã phòng trùng.
- Tìm kiếm phòng không tồn tại.
- Không cho nhận phòng đang bảo trì.
- Không cho đặt trùng phòng trong cùng khoảng thời gian.
- Kiểm tra thông tin khách hàng và nhân viên.
- Tính tiền phòng và tiền dịch vụ chính xác.
- Kiểm tra tổng hóa đơn và doanh thu thống kê.
- Xử lý lựa chọn menu không hợp lệ.
- Biên dịch và chạy thử toàn bộ chương trình sau khi tích hợp.

Kết quả kiểm thử sẽ được ghi nhận trong báo cáo dựa trên quá trình chạy chương trình thực tế.

## 12. Kết quả xây dựng

Phần này sẽ được cập nhật sau khi nhóm hoàn thành và kiểm thử ứng dụng, bao gồm:

- Các chức năng đã hoàn thành.
- Kết quả chạy thử và kiểm thử.
- Hình ảnh giao diện hoặc kết quả chạy chương trình.
- Những hạn chế còn tồn tại.
- Hướng cải tiến trong tương lai.

Nhóm không coi các chức năng mới ở mức kế hoạch là chức năng đã hoàn thành nếu chưa được triển khai và kiểm thử.

## 13. Định hướng phát triển

Tùy theo thời gian và yêu cầu môn học, dự án có thể được mở rộng với:

- Giao diện đồ họa bằng Java Swing hoặc JavaFX.
- Lưu trữ dữ liệu bằng MySQL.
- Phân quyền cho nhân viên và quản lý.
- Thống kê doanh thu theo ngày, tháng hoặc năm.
- Xuất hóa đơn và báo cáo ra file.
- Bổ sung kiểm thử tự động và cải thiện xử lý lỗi.

Các tính năng mở rộng chỉ được triển khai khi nhóm thống nhất và các chức năng cốt lõi đã hoạt động ổn định.

---

**Hotel Management System** — Dự án thực hành Java OOP theo nhóm, hướng đến xây dựng một ứng dụng quản lý khách sạn có cấu trúc rõ ràng, dễ kiểm thử và dễ mở rộng.
