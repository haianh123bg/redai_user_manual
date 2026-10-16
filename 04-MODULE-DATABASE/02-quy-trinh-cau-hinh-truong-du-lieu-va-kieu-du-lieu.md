## Mở khu vực Cấu hình trường dữ liệu và Trình soạn thảo Cột

Trường dữ liệu (Columns / Fields) là các đơn vị cấu trúc nền tảng định hình toàn bộ thông tin được lưu trữ trong mỗi Bảng dữ liệu của **RedAI Database**. Để xem, khởi tạo và tinh chỉnh hệ thống cột, bạn có thể truy cập qua 2 khu vực trực quan trên giao diện:

1. **Thao tác nhanh ngay trên Bảng tính (Grid View - `/database/table/:tableId/view/:viewId`)**:
   - **Thêm cột mới**: Kéo sang cột ngoài cùng bên phải của bảng tính và nhấp vào nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm cột)** nằm trên thanh tiêu đề bảng.
   - **Chỉnh sửa cột hiện có**: Nhấp vào biểu tượng mũi tên <img src="https://api.iconify.design/lucide:chevron-down.svg?color=%23ff3333" width="16" alt="" /> bên cạnh tên bất kỳ cột nào trên thanh tiêu đề $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:edit-2.svg?color=%23ff3333" width="16" alt="" /> **Sửa trường** để mở hộp thoại **Trình chỉnh sửa cột (ColumnEditorModal)**.
2. **Khu vực Cấu hình chuyên sâu danh sách trường (`/database/table/:tableId/settings/fields`)**:
   - Truy cập bằng cách bấm nút <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **(Cài đặt bảng)** ở góc phải trên cùng màn hình bảng dữ liệu $\rightarrow$ Chọn tab <img src="https://api.iconify.design/lucide:columns.svg?color=%23ff3333" width="16" alt="" /> **Trường dữ liệu**.
   - Màn hình hiển thị toàn bộ danh sách các cột trong bảng dưới dạng bảng quản trị, bao gồm: **Tên trường**, **Kiểu dữ liệu**, **Thuộc tính bắt buộc (Required)**, **Khóa chính (Primary/Display)**, **Mô tả** và biểu tượng nắm kéo <img src="https://api.iconify.design/lucide:grip-vertical.svg?color=%23ff3333" width="16" alt="" /> để thay đổi thứ tự các cột.

---

## Các bước thực hiện

### Chọn nhóm kiểu dữ liệu phù hợp với nghiệp vụ

Hệ thống **RedAI Database** hỗ trợ hơn 30 kiểu dữ liệu chuyên sâu được phân nhóm khoa học trên giao diện:

| Nhóm kiểu dữ liệu | Các kiểu dữ liệu cụ thể | Mục đích & Nghiệp vụ phù hợp |
| :--- | :--- | :--- |
| **Văn bản & Đa phương tiện** | Text, Long Text, HTML | Lưu trữ tiêu đề, họ tên, ghi chú dài, mô tả chi tiết bài viết có định dạng phong phú. |
| **Số & Định lượng tài chính** | Number, Currency, Percent, Rating | Quản lý số lượng, đơn giá, doanh số, chiết khấu phần trăm và điểm số đánh giá chất lượng. |
| **Lựa chọn & Trạng thái** | Select, Multi-select, Boolean | Phân loại trạng thái đơn hàng, thẻ tag danh mục, cờ bật/tắt (Đúng/Sai). |
| **Thông tin liên lạc & Vị trí** | Phone, Email, URL, Geo Data, Color | Lưu số điện thoại, hộp thư, liên kết website, tọa độ/địa chỉ bản đồ và mã màu nhận diện. |
| **Thời gian & Lịch trình** | Date, Datetime, Time, Duration, Recurrence | Quản lý ngày tháng, mốc giờ sự kiện, thời lượng cuộc gọi/dự án và chu kỳ lặp lại công việc. |
| **Liên kết bảng & Tính toán tự động** | Auto Number, Relation, Lookup, Rollup, Formula | Tạo mã số tự tăng, kết nối dữ liệu giữa các bảng, lấy giá trị tham chiếu, tính tổng hợp và biểu thức tự động. |
| **Mã hóa, Tương tác & Trí tuệ AI** | QR Code, Barcode, Button, User, Conversation ID, AI | In tem mã vạch/mã QR, tạo nút bấm kích hoạt hành động, gán người phụ trách và xử lý nội dung thông minh với AI. |

---

### Giai đoạn 1 — Khởi tạo và thiết lập thuộc tính cơ bản của trường dữ liệu

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở Trình chỉnh sửa cột** | Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> trên thanh tiêu đề bảng tính (hoặc bấm nút **Thêm trường** tại trang Cài đặt trường). |
| **2. Đặt tên trường và chọn kiểu dữ liệu** | Trong hộp thoại **Trình chỉnh sửa cột**:<br>• **Tên trường \***: Nhập tên rõ nghĩa (ví dụ: `Họ và Tên`, `Tổng Tiền Hợp Đồng`, `Trạng Thái`).<br>• **Kiểu dữ liệu \***: Nhấp vào ô chọn kiểu để mở bảng danh mục hơn 30 kiểu dữ liệu, chọn loại phù hợp. |
| **3. Cấu hình các thuộc tính chung** | Thiết lập các tùy chọn quan trọng:<br>• **Mô tả hướng dẫn**: Nhập gợi ý nhập liệu cho người dùng khi điền biểu mẫu hoặc nhập liệu ô.<br>• **Bắt buộc nhập (Required)**: Bật nút gạt <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> nếu trường này không được phép để trống khi tạo bản ghi mới.<br>• **Giá trị mặc định**: Nhập giá trị tự động gán vào ô khi thêm dòng mới.<br>• **Trường đại diện (Primary/Display Column)**: Bật cờ ngôi sao <img src="https://api.iconify.design/lucide:star.svg?color=%23ff3333" width="16" alt="" /> nếu muốn trường này làm tên đại diện cho bản ghi khi liên kết từ các bảng khác. |
| **4. Lưu và áp dụng** | Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Lưu trường)**. Cột mới sẽ xuất hiện ngay trên giao diện bảng tính. |

---

### Giai đoạn 2 — Cấu hình chuyên sâu theo từng kiểu dữ liệu cụ thể

Mỗi kiểu dữ liệu khi được chọn sẽ hiển thị một bảng điều khiển cấu hình riêng biệt:

#### 1. Nhóm Số và Định lượng tài chính (Number, Currency, Percent, Rating)

- **Số (Number)**:
  - Chọn định dạng hiển thị: `Số nguyên (1.234)` hoặc `Số thập phân (1.234,56)`.
  - Cấu hình số chữ số thập phân sau dấu phẩy (0 đến 6 chữ số).
  - Tùy chọn cho phép nhập số âm hoặc giới hạn giá trị nhỏ nhất (Min) / lớn nhất (Max).
- **Tiền tệ (Currency)**:
  - Chọn ký hiệu tiền tệ: `₫ (VNĐ)`, `$ (USD)`, `€ (EUR)`, `¥ (JPY)` hoặc tùy chỉnh ký hiệu khác.
  - Chọn vị trí hiển thị ký hiệu tiền tệ: Đứng trước số (ví dụ: `$100`) hoặc đứng sau số (ví dụ: `100.000 ₫`).
- **Phần trăm (Percent)**:
  - Hiển thị tự động ký hiệu `%` phía sau giá trị nhập.
- **Đánh giá sao (Rating)**:
  - Chọn số sao tối đa: Từ 1 đến 10 sao (mặc định là 5 sao).
  - Chọn biểu tượng đánh giá: Ngôi sao <img src="https://api.iconify.design/lucide:star.svg?color=%23ff3333" width="16" alt="" />, Trái tim <img src="https://api.iconify.design/lucide:heart.svg?color=%23ff3333" width="16" alt="" /> hoặc Ngón tay thích <img src="https://api.iconify.design/lucide:thumbs-up.svg?color=%23ff3333" width="16" alt="" />.

#### 2. Nhóm Lựa chọn danh mục (Select & Multi-select)

- **Tùy chọn cục bộ (Local Options)**: Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm tùy chọn** để tạo các mục lựa chọn riêng cho bảng. Mỗi mục cho phép đặt tên nhãn và nhấp vào bảng màu để chọn màu thẻ nổi bật.
- **Sử dụng Tập hợp tùy chọn dùng chung (Option Sets)**: Bật tùy chọn **Liên kết Option Set** để chọn một bộ danh mục đã được chuẩn hóa sẵn dùng chung cho toàn hệ thống (ví dụ: `Danh mục Tỉnh/Thành phố`, `Phòng ban`).

#### 3. Số tự động tăng (Auto Number)

- **Tiền tố (Prefix)**: Nhập chuỗi ký tự đứng đầu mã (ví dụ: `HD-`, `KH-`, `NV-`).
- **Số bắt đầu (Start Number)**: Chỉ định số khởi điểm (ví dụ: `1` hoặc `1001`).
- **Số chữ số tối thiểu (Digit Count)**: Định dạng độ dài phần số với các số 0 đệm phía trước (ví dụ: chọn độ dài 5 số sẽ sinh mã `HD-00001`, `HD-00002`).

#### 4. Khóa liên kết bảng khác (Relation)

- **Bảng đích (Target Table) \***: Chọn bảng dữ liệu muốn kết nối trong không gian làm việc.
- **Loại quan hệ (Relationship Type)**:
  - `Một - Nhiều (1:N)`: Một bản ghi ở bảng này liên kết với nhiều bản ghi ở bảng đích (ví dụ: một Khách Hàng có nhiều Đơn Hàng).
  - `Nhiều - Một (N:1)`: Nhiều bản ghi ở bảng này cùng thuộc về một bản ghi ở bảng đích.
  - `Nhiều - Nhiều (N:N)`: Nhiều bản ghi ở bảng này liên kết với nhiều bản ghi ở bảng đích.
  - `Một - Một (1:1)`: Mỗi bản ghi chỉ liên kết duy nhất với một bản ghi tương ứng.
- **Tên trường liên kết ngược (Inverse Field Name)**: Đặt tên cho cột liên kết tự động được sinh ra ở bảng đích để hai bảng liên kết hai chiều hoàn hảo.
- **Điều kiện ràng buộc (Link Conditions)**: Thiết lập bộ lọc chỉ cho phép chọn những bản ghi thỏa mãn điều kiện ở bảng đích.

#### 5. Cột Tra cứu (Lookup) và Tổng hợp (Rollup)

- **Tra cứu (Lookup)**:
  - Chọn cột Relation đã thiết lập trước đó.
  - Chọn cột dữ liệu cần lấy về từ bảng liên kết (ví dụ: từ trường liên kết `Khách Hàng`, lấy về cột `Số Điện Thoại` hoặc `Địa Chỉ`).
- **Tổng hợp (Rollup)**:
  - Chọn cột Relation làm cầu nối.
  - Chọn cột số cần tính toán ở bảng liên kết.
  - Chọn hàm tổng hợp: `Tổng (SUM)`, `Trung bình (AVG)`, `Nhỏ nhất (MIN)`, `Lớn nhất (MAX)`, `Đếm số lượng (COUNT)`, `Đếm giá trị duy nhất (COUNT UNIQUE)`.

#### 6. Công thức tính toán tự động (Formula)

- Trình soạn thảo biểu thức với giao diện tô màu cú pháp trực quan.
- Bảng gợi ý danh sách hàm:
  - Hàm toán học: `SUM()`, `ROUND()`, `ABS()`, `SQRT()`, các phép toán `+`, `-`, `*`, `/`.
  - Hàm chuỗi: `CONCAT()`, `UPPER()`, `LOWER()`, `LEFT()`, `RIGHT()`, `LEN()`.
  - Hàm điều kiện logic: `IF(điều_kiện, giá_trị_nếu_đúng, giá_trị_nếu_sai)`, `AND()`, `OR()`, `NOT()`.
  - Hàm thời gian: `TODAY()`, `NOW()`, `DATE_DIFF()`, `YEAR()`, `MONTH()`.
- Chèn trực tiếp tên các cột khác vào công thức bằng cách gõ ký tự `{` hoặc bấm vào danh sách cột gợi ý.

#### 7. Nút bấm hành động (Button) và Trợ lý AI (AI Assistant)

- **Nút bấm hành động (Button)**:
  - Đặt nhãn nút (ví dụ: `Gửi Hợp Đồng`, `Duyệt Nhanh`, `In Hóa Đơn`).
  - Chọn hành động khi bấm: Gửi Webhook tự động hóa, Mở đường dẫn URL theo dữ liệu bản ghi, hoặc Chuyển trạng thái bản ghi.
- **Trợ lý AI (AI Field)**:
  - Nhập câu lệnh chỉ dẫn (Prompt) cho AI (ví dụ: `Hãy đọc nội dung từ cột {Ghi Chú Phản Hồi} và phân loại cảm xúc thành Tích cực, Tiêu cực hoặc Trung tính`).
  - Chọn mô hình xử lý và thời điểm thực thi (Tự động chạy khi có bản ghi mới hoặc Chạy thủ công khi bấm nút).

---

### Giai đoạn 3 — Sắp xếp, ẩn và quản lý vòng đời trường dữ liệu

| Thao tác | Cách thực hiện |
| :--- | :--- |
| **Thay đổi thứ tự cột** | Nhấp giữ chuột vào tiêu đề cột trên Grid View và kéo thả sang vị trí mong muốn; hoặc vào `/database/table/:tableId/settings/fields`, dùng biểu tượng <img src="https://api.iconify.design/lucide:grip-vertical.svg?color=%23ff3333" width="16" alt="" /> để kéo thả dòng trường lên xuống. |
| **Nhân bản trường (Duplicate Field)** | Nhấp vào menu cột <img src="https://api.iconify.design/lucide:chevron-down.svg?color=%23ff3333" width="16" alt="" /> $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **Nhân bản trường**. Toàn bộ kiểu dữ liệu và cấu hình sẽ được sao chép sang cột mới. |
| **Đặt cột làm Giá trị đại diện** | Nhấp vào menu cột $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:star.svg?color=%23ff3333" width="16" alt="" /> **Đặt làm trường hiển thị chính**. |
| **Xóa cột dữ liệu** | Nhấp vào menu cột $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Xóa trường** $\rightarrow$ Xác nhận trên hộp thoại cảnh báo (lưu ý: thao tác xóa trường sẽ xóa toàn bộ dữ liệu nằm trong cột đó trên tất cả các bản ghi). |

---

## Kiểm tra kết quả

Sau khi cấu hình hệ thống trường dữ liệu, bạn kiểm tra lại tính chính xác qua các tiêu chí:

1. **Hiển thị trên tiêu đề bảng tính**: Tên trường và biểu tượng đại diện cho kiểu dữ liệu tương ứng hiển thị chuẩn xác trên thanh header cột.
2. **Hành vi nhập liệu ô (Inline Cell Editing)**: Khi nhấp đúp vào ô thuộc cột, trình chỉnh sửa hiển thị đúng định dạng (ô chọn ngày với kiểu Date, bảng chọn màu với kiểu Select, khung tải tệp với kiểu Attachment...).
3. **Tính toán tự động**: Với các cột Formula, Lookup và Rollup, dữ liệu tự động cập nhật ngay khi các giá trị nguồn thay đổi mà không cần tải lại trang.
4. **Trường khóa chính**: Cột được đặt làm Display Column luôn hiển thị nổi bật và được dùng làm nhãn khi tìm kiếm hoặc liên kết ở các bảng khác.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể tự động thêm trường, thay đổi kiểu dữ liệu hoặc cấu hình công thức cho bảng, bạn cần đảm bảo Agent đã được trang bị Kỹ năng (Skill) sau:

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Workspace Member, Editor, Admin hoặc Owner |

---

### Bảng ánh xạ giao diện người dùng sang công cụ AI Agent

| Tác vụ trên Giao diện | Tên Tool tương ứng | Ý nghĩa & Tham số chính |
| :--- | :--- | :--- |
| Bấm **Thêm cột** và chọn kiểu dữ liệu | `column_createColumn` | Khởi tạo cột mới trong bảng (`tableId`, `title`, `type`, `description`, `required`, `options`). |
| Xem danh sách cột tại trang cài đặt trường | `column_listColumns` | Lấy toàn bộ danh sách trường và cấu hình chi tiết của bảng (`tableId`). |
| Bấm **Sửa trường** trong menu cột | `column_updateColumn` | Cập nhật tên cột, mô tả hoặc tùy chọn cấu hình (`tableId`, `columnId`, `title`, `options`). |
| Bấm **Xóa trường** trên menu cột | `column_deleteColumn` | Xóa vĩnh viễn trường dữ liệu khỏi bảng (`tableId`, `columnId`). |
| Bấm **Đặt làm trường hiển thị chính** | `column_setPrimaryColumn` | Thiết lập cột làm nhãn đại diện chính cho bản ghi (`tableId`, `columnId`). |
| Kéo thả thay đổi vị trí thứ tự cột | `column_reorderColumns` | Sắp xếp lại danh sách thứ tự hiển thị của các cột (`tableId`, `columnIds`). |
| Cấu hình cột liên kết bảng (Relation) | `relation_createRelation` | Thiết lập khóa quan hệ 1-1, 1-N hoặc N-N giữa hai bảng (`sourceTableId`, `targetTableId`, `type`, `inverseTitle`). |

---

### Khung lệnh (Prompt) mẫu chuẩn 4 phần cho AI Agent

Dưới đây là mẫu câu lệnh hoàn chỉnh để ra lệnh cho AI Agent tự động bổ sung hệ thống cột chuyên sâu cho một bảng dữ liệu:

```text
[MỤC TIÊU]
Thêm 3 trường dữ liệu mới vào bảng "Đơn Đặt Hàng" (mã định danh: `tbl_orders_2026`) gồm: Mã đơn tự tăng, Tổng giá trị tiền tệ và Khóa liên kết với bảng "Khách Hàng".

[DỮ LIỆU ĐẦU VÀO]
- Mã bảng dữ liệu: `tbl_orders_2026`
- Trường 1: Tên "Mã Đơn Hàng", kiểu AUTONUMBER, tiền tố "ORD-", số bắt đầu 10001, độ dài 5 số, đặt làm trường hiển thị chính.
- Trường 2: Tên "Tổng Tiền", kiểu CURRENCY, đơn vị tiền tệ "VNĐ", bắt buộc nhập (required: true).
- Trường 3: Tên "Khách Hàng Mua", kiểu RELATION, liên kết sang bảng "Khách Hàng" (`tbl_customers_2026`), quan hệ Nhiều-Một (N:1), tên trường đảo ngược là "Lịch Sử Đơn Hàng".

[QUY TRÌNH THỰC THI]
1. Gọi tool `column_createColumn` để tạo trường "Mã Đơn Hàng" với kiểu AUTONUMBER và các tùy chọn prefix, startNumber.
2. Gọi tool `column_setPrimaryColumn` để gán trường "Mã Đơn Hàng" làm cột đại diện chính.
3. Gọi tool `column_createColumn` để tạo trường "Tổng Tiền" với kiểu CURRENCY và cờ `required: true`.
4. Gọi tool `relation_createRelation` để tạo quan hệ liên kết bảng với bảng khách hàng.
5. Gọi tool `column_listColumns` để kiểm tra lại toàn bộ danh sách trường sau khi tạo.

[TIÊU CHÍ HOÀN THÀNH]
- 3 trường mới xuất hiện đầy đủ trong cấu trúc bảng `tbl_orders_2026`.
- Bảng đích `tbl_customers_2026` tự động xuất hiện trường liên kết đảo ngược "Lịch Sử Đơn Hàng".
- Báo cáo kết quả chi tiết kèm mã `columnId` của từng trường vừa tạo.
```

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Thêm cột mới hoặc đổi kiểu dữ liệu trong modal | Gọi `column_listColumns` thấy trường mới xuất hiện với đúng `type` và `options`. |
| Đặt cột làm trường đại diện bằng biểu tượng ngôi sao | Gọi `table_getTableDetail` thấy thuộc tính `primaryColumnId` trùng với ID của cột đó. |
| Kéo thả đổi vị trí các cột trên giao diện | Gọi `column_listColumns` thấy mảng các cột trả về theo đúng thứ tự mới. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `column_createColumn` tạo trường mới | Mở Grid View của bảng, cột mới lập tức hiển thị ở vị trí chỉ định với đúng biểu tượng kiểu dữ liệu. |
| Agent gọi `column_deleteColumn` xóa trường | Cột biến mất hoàn toàn khỏi bảng tính và không còn xuất hiện trong danh sách cài đặt trường. |
| Agent gọi `relation_createRelation` tạo liên kết bảng | Mở bảng đích, xuất hiện thêm cột liên kết ngược cho phép chọn các bản ghi từ bảng nguồn. |
