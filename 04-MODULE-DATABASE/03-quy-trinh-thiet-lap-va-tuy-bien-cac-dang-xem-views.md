## Mở thanh điều khiển View Header và Chuyển đổi Dạng xem

Trong **RedAI Database**, Dạng xem (Views) cho phép bạn quan sát, phân tích và tương tác với cùng một nguồn dữ liệu theo nhiều góc nhìn trực quan khác nhau: từ bảng tính truyền thống, bảng thẻ quy trình, thư viện ảnh, lịch biểu thời gian cho đến biểu mẫu thu thập dữ liệu công khai. Mỗi bảng dữ liệu có thể chứa không giới hạn các dạng xem được lưu trữ cấu hình độc lập.

Để mở thanh điều khiển View và chuyển đổi các góc nhìn, bạn truy cập vào đường dẫn của bảng tương ứng:

1. **Thanh tiêu đề dạng xem (View Header & Tabs)**: Nằm ngay dưới thanh tiêu đề chính của bảng dữ liệu, hiển thị danh sách các tab View hiện có cùng các nút điều khiển:
   - Các tab Dạng xem hiện có: Nhấp vào từng tab để chuyển đổi không gian làm việc tương ứng:
     - <img src="https://api.iconify.design/lucide:table.svg?color=%23ff3333" width="16" alt="" /> **Grid View** (`/database/table/:tableId/view/:viewId`): Bảng tính dữ liệu chi tiết dạng hàng và cột.
     - <img src="https://api.iconify.design/lucide:kanban.svg?color=%23ff3333" width="16" alt="" /> **Kanban View** (`/database/table/:tableId/kanban/:viewId`): Bảng quản lý thẻ công việc theo các cột trạng thái quy trình.
     - <img src="https://api.iconify.design/lucide:layout-grid.svg?color=%23ff3333" width="16" alt="" /> **Gallery View** (`/database/table/:tableId/gallery/:viewId`): Thư viện thẻ trực quan nổi bật hình ảnh và thông tin tóm tắt.
     - <img src="https://api.iconify.design/lucide:calendar.svg?color=%23ff3333" width="16" alt="" /> **Calendar View** (`/database/table/:tableId/calendar/:viewId`): Lịch biểu trực quan theo tháng, tuần, ngày dựa trên các mốc thời gian.
     - <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **Form View** (`/database/table/:tableId/form/:viewId`): Biểu mẫu nhập liệu trực quan có thể chia sẻ công khai qua liên kết hoặc mã QR.
   - Nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm View mới)**: Mở hộp thoại **Tạo Dạng xem mới (CreateViewModal)** để bổ sung thêm một góc nhìn mới cho bảng.
   - Menu ngữ cảnh trên từng tab View (<img src="https://api.iconify.design/lucide:chevron-down.svg?color=%23ff3333" width="16" alt="" />): Cho phép đổi tên View, nhân bản View, khóa cấu hình View (chống chỉnh sửa bộ lọc/cột ngoài ý muốn) hoặc xóa View khỏi bảng.
2. **Thanh công cụ tác vụ đa năng (View Toolbar)**: Bố trí ngay dưới tab View, cung cấp bộ công cụ mạnh mẽ:
   - <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **Tìm kiếm bản ghi**: Nhập từ khóa để tìm kiếm nhanh trên tất cả các trường hoặc lọc theo một trường chỉ định.
   - <img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" /> **Lọc (Filter)**: Tạo bộ lọc đa điều kiện kết hợp toán tử AND/OR hoặc nhờ AI sinh bộ lọc tự động.
   - <img src="https://api.iconify.design/lucide:arrow-up-down.svg?color=%23ff3333" width="16" alt="" /> **Sắp xếp (Sort)**: Sắp xếp dữ liệu đa tầng theo thứ tự tăng dần hoặc giảm dần.
   - <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **Gom nhóm (Group by)**: Gom nhóm các dòng theo giá trị của cột chỉ định.
   - <img src="https://api.iconify.design/lucide:eye-off.svg?color=%23ff3333" width="16" alt="" /> **Ẩn/Hiện trường (Fields)**: Tùy chỉnh danh sách các cột hiển thị riêng cho View này.
   - <img src="https://api.iconify.design/lucide:palette.svg?color=%23ff3333" width="16" alt="" /> **Tô màu dòng (Row Color Rules)**: Đặt màu nền nổi bật cho các bản ghi thỏa mãn điều kiện.
   - <img src="https://api.iconify.design/lucide:rows.svg?color=%23ff3333" width="16" alt="" /> **Chiều cao dòng (Row Height)**: Chọn kích thước dòng hiển thị (Nhỏ, Trung bình, Lớn, Rất lớn).
   - <img src="https://api.iconify.design/lucide:share-2.svg?color=%23ff3333" width="16" alt="" /> **Chia sẻ View**: Quản lý liên kết công khai, tạo link rút gọn và mã QR.

---

## Các bước thực hiện

### Chọn dạng xem phù hợp với bài toán nghiệp vụ

| Dạng xem (View Type) | Khi nào nên sử dụng | Tính năng nổi bật |
| :--- | :--- | :--- |
| **Grid View (Bảng tính)** | Cần quản lý, đối soát dữ liệu hàng loạt, nhập liệu trực tiếp vào ô như Excel. | Chỉnh sửa trực tiếp ô (Inline Edit), xem chi tiết dòng (`RowDetailModal`), tính toán thống kê chân trang (Footer Summary). |
| **Kanban View (Bảng thẻ)** | Quản lý quy trình làm việc nhiều bước (ví dụ: Tiếp nhận $\rightarrow$ Đang xử lý $\rightarrow$ Hoàn thành). | Kéo thả thẻ mượt mà giữa các cột phân nhóm, cấu hình trường hiển thị trên thẻ, gắn ảnh bìa trực quan. |
| **Gallery View (Thư viện ảnh)** | Quản lý sản phẩm thương mại, danh mục nhân sự, tài sản hoặc portfolio có hình ảnh. | Thẻ trực quan với ảnh bìa nổi bật (chế độ Cover hoặc Fit), tùy chỉnh trường hiển thị dưới thẻ. |
| **Calendar View (Lịch biểu)** | Lên lịch sự kiện, theo dõi hạn chót (Deadline), kế hoạch dự án, lịch bàn giao hợp đồng. | Chuyển đổi linh hoạt chế độ Năm/Tháng/Tuần/Ngày, điều hướng dải ngày, kéo thả dời lịch sự kiện. |
| **Form View (Biểu mẫu công khai)** | Thu thập phản hồi khách hàng, đăng ký tư vấn, khảo sát dịch vụ mà không cần cấp quyền tài khoản. | Thiết kế biểu mẫu tùy biến logo/ảnh bìa, kéo thả câu hỏi, chia sẻ liên kết rút gọn, gắn mã UTM theo dõi nguồn. |

---

### Giai đoạn 1 — Khởi tạo Dạng xem mới

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở hộp thoại Tạo View** | Nhấp vào nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> trên thanh tab View để mở cửa sổ **Cấu hình View (CreateViewModal)**. |
| **2. Chọn loại View và đặt tên** | • Chọn 1 trong 5 loại View: **Grid**, **Kanban**, **Gallery**, **Calendar** hoặc **Form**.<br>• **Tên View \***: Đặt tên gợi nhớ (ví dụ: `Đơn Hàng Chờ Xử Lý`, `Lịch Giao Hàng Tuần Này`).<br>• **Mô tả**: Nhập ghi chú về mục đích lọc hoặc phân loại của View này. |
| **3. Cấu hình quyền truy cập View** | Chọn chế độ quản trị View:<br>• **Cộng tác (Collaborative)**: Mọi thành viên có quyền sửa cấu hình View.<br>• **Khóa (Locked)**: Chỉ người tạo và Quản trị viên mới được sửa bộ lọc và sắp xếp. |
| **4. Xác nhận khởi tạo** | Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo View)**. Giao diện sẽ tự động chuyển sang tab View mới. |

---

### Giai đoạn 2 — Thiết lập và tùy biến chi tiết từng Dạng xem

#### 1. Dạng xem Bảng tính (Grid View)

- **Chỉnh sửa trực tiếp trên ô (Inline Cell Editing)**:
  - Nhấp đúp chuột vào bất kỳ ô nào để nhập liệu ngay lập tức. Dùng phím `Enter` để lưu và xuống dòng dưới, phím `Tab` để chuyển sang ô bên phải, phím `Escape` để hủy.
  - Hỗ trợ các trình biên tập thông minh tương ứng với từng kiểu dữ liệu: bảng chọn ngày cho kiểu Date, danh sách thả xuống có màu cho Select, trình tải tệp cho Attachment, cửa sổ chọn quan hệ cho Relation.
- **Xem và sửa chi tiết bản ghi (Row Detail Modal)**:
  - Nhấp vào biểu tượng mở rộng <img src="https://api.iconify.design/lucide:maximize-2.svg?color=%23ff3333" width="16" alt="" /> ở đầu mỗi dòng bản ghi.
  - Cửa sổ hiển thị toàn bộ các trường của bản ghi dạng biểu mẫu dọc, cho phép nhập liệu thoải mái các văn bản dài, xem tệp đính kèm kích thước lớn và duyệt qua lại giữa các dòng bằng 2 nút <img src="https://api.iconify.design/lucide:chevron-left.svg?color=%23ff3333" width="16" alt="" /> **Trước** và <img src="https://api.iconify.design/lucide:chevron-right.svg?color=%23ff3333" width="16" alt="" /> **Sau**.
- **Thanh tổng hợp chân trang (Footer Summary Bar)**:
  - Dưới chân mỗi cột số, ngày tháng hoặc danh mục, nhấp vào ô tổng hợp để chọn hàm thống kê mong muốn:
    - Nhóm đếm: `Số lượng (Count)`, `Trống (Empty)`, `Có dữ liệu (Filled)`, `Duy nhất (Unique)`.
    - Nhóm tính toán: `Tổng (Sum)`, `Trung bình (Average)`, `Nhỏ nhất (Min)`, `Lớn nhất (Max)`, `Trung vị (Median)`, `Độ lệch chuẩn (Standard Deviation)`.
    - Nhóm tỷ lệ: `Phần trăm có dữ liệu`, `Phần trăm duy nhất`, `Phần trăm đã chọn`.

#### 2. Dạng xem Bảng thẻ quy trình (Kanban View)

- **Cấu hình trường phân nhóm Stacks (`KanbanStackedByMenu`)**:
  - Nhấp vào nút <img src="https://api.iconify.design/lucide:columns.svg?color=%23ff3333" width="16" alt="" /> **Gom thẻ theo** trên thanh công cụ.
  - Chọn trường dữ liệu làm tiêu chí tạo các cột trạng thái (hỗ trợ các trường kiểu: `SELECT`, `MULTI_SELECT`, `USER`, `BOOLEAN`).
  - Chọn trường ảnh bìa thẻ: Chọn trường `ATTACHMENT` hoặc `URL` (tùy chọn) để hiển thị hình ảnh minh họa trên đầu mỗi thẻ.
- **Kéo thả và quản lý thẻ**:
  - Kéo thả thẻ từ cột này sang cột khác để tự động cập nhật giá trị trường phân nhóm (ví dụ: kéo từ cột `Chờ Duyệt` sang `Đã Duyệt`).
  - Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm thẻ mới** ở cuối mỗi cột để tạo nhanh bản ghi mới thuộc đúng trạng thái của cột đó.
- **Tùy biến hiển thị trường trên thẻ (`KanbanToolbarFieldMenu`)**:
  - Bấm nút <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **Tùy chỉnh thẻ** trên thanh công cụ. Bật/tắt các công tắc để quyết định những trường thông tin nào (ngày giao, số tiền, người phụ trách...) được lộ ra ngoài mặt thẻ.

#### 3. Dạng xem Thư viện thẻ trực quan (Gallery View)

- **Cấu hình ảnh bìa và hiển thị thẻ (`GalleryToolbarCardMenu`)**:
  - Nhấp vào nút <img src="https://api.iconify.design/lucide:image.svg?color=%23ff3333" width="16" alt="" /> **Ảnh bìa** trên thanh công cụ.
  - Chọn cột ảnh bìa tại mục **Ảnh bìa** (chọn trường `ATTACHMENT` chứa ảnh sản phẩm/chân dung).
  - Chọn chế độ khớp ảnh tại mục **Hiển thị ảnh**:
    - `Lấp đầy khung (Cover)`: Ảnh phóng to vừa khít tỷ lệ khung thẻ.
    - `Vừa khung (Fit/Contain)`: Giữ nguyên tỷ lệ gốc của bức ảnh, không bị cắt viền.
- **Chọn các trường hiển thị dưới thẻ (`GalleryToolbarFieldMenu`)**:
  - Bấm nút <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **Trường hiển thị** $\rightarrow$ Tích chọn các thông tin muốn làm nổi bật (ví dụ: Tên sản phẩm, Giá bán, Tồn kho).

#### 4. Dạng xem Lịch biểu thời gian (Calendar View)

- **Cấu hình dải ngày sự kiện (`CalendarRangeSettings`)**:
  - Nhấp vào nút <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **Cấu hình** trên thanh công cụ.
  - Chọn **Trường ngày bắt đầu \***: Bắt buộc chọn một trường kiểu `DATE` hoặc `DATETIME`.
  - Chọn **Trường ngày kết thúc (Tùy chọn)**: Dành cho các sự kiện kéo dài nhiều ngày (nếu để trống, sự kiện hiển thị dưới dạng một điểm mốc trong ngày).
  - Chọn **Trường ảnh bìa**: Gắn hình ảnh đại diện cho ô sự kiện trên lịch.
- **Chuyển đổi chế độ xem và điều hướng**:
  - Chuyển đổi linh hoạt giữa 4 chế độ qua các nút bấm: <img src="https://api.iconify.design/lucide:calendar.svg?color=%23ff3333" width="16" alt="" /> **Năm (Year)**, **Tháng (Month)**, **Tuần (Week)**, **Ngày (Day)**.
  - Bấm <img src="https://api.iconify.design/lucide:chevron-left.svg?color=%23ff3333" width="16" alt="" /> **Trước** / <img src="https://api.iconify.design/lucide:chevron-right.svg?color=%23ff3333" width="16" alt="" /> **Sau** để đổi mốc thời gian, hoặc bấm **Hôm nay** để quay về ngày hiện tại ngay lập tức.
  - Kéo thả sự kiện sang một ô ngày khác để tự động dời mốc ngày trong cơ sở dữ liệu.

#### 5. Dạng xem Biểu mẫu thu thập dữ liệu (Form View)

- **Tùy biến nhận diện thương hiệu cho Form**:
  - Nhấp vào tiêu đề để sửa **Tên biểu mẫu** và **Mô tả hướng dẫn**.
  - Tải lên **Ảnh bìa biểu mẫu (Cover)** và **Ảnh Logo thương hiệu** để tăng độ uy tín chuyên nghiệp.
- **Sắp xếp câu hỏi và thuộc tính trường**:
  - Kéo thả các khối câu hỏi để sắp xếp lại thứ tự từ trên xuống dưới.
  - Tại từng câu hỏi, bạn có thể:
    - Bật/tắt công tắc <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **Bắt buộc**: Bắt buộc người gửi phải điền câu hỏi này.
    - Bật/tắt công tắc <img src="https://api.iconify.design/lucide:eye-off.svg?color=%23ff3333" width="16" alt="" /> **Ẩn trường**: Ẩn trường khỏi biểu mẫu công khai nhưng vẫn gán sẵn giá trị mặc định ngầm định.
- **Cấu hình phản hồi sau khi hoàn tất**:
  - Nhập **Thông báo cảm ơn** xuất hiện sau khi người dùng bấm nút gửi form.
  - Nhập **Đường dẫn chuyển hướng (Redirect URL)** nếu muốn trình duyệt tự động chuyển sang trang cảm ơn hoặc website của bạn sau khi gửi dữ liệu.
  - Bật tùy chọn **Cho phép gửi phản hồi khác** nếu người dùng có nhu cầu gửi nhiều lần.

---

### Giai đoạn 3 — Sử dụng bộ công cụ Lọc, Sắp xếp và Tô màu dữ liệu

| Công cụ | Cách thức thiết lập |
| :--- | :--- |
| **Bộ lọc (Filter)** | Bấm nút <img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" /> **Lọc** trên thanh công cụ:<br>• Bấm **+ Thêm điều kiện**: Chọn `Cột` $\rightarrow$ Chọn `Toán tử` (bằng, chứa, bắt đầu bằng, rỗng...) $\rightarrow$ Nhập `Giá trị`.<br>• Kết hợp nhiều điều kiện bằng logic **VÀ (AND)** hoặc **HOẶC (OR)**.<br>• **Tạo bộ lọc bằng AI**: Nhấp vào biểu tượng <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> và gõ yêu cầu tự nhiên (ví dụ: `Lọc đơn hàng hoàn thành trong tuần này có giá trị trên 5 triệu`), AI sẽ tự động sinh quy tắc lọc chính xác. |
| **Sắp xếp (Sort)** | Bấm nút <img src="https://api.iconify.design/lucide:arrow-up-down.svg?color=%23ff3333" width="16" alt="" /> **Sắp xếp**:<br>• Bấm **+ Thêm quy tắc sắp xếp**: Chọn cột và chiều sắp xếp (Tăng dần `A $\rightarrow$ Z`, `0 $\rightarrow$ 9` hoặc Giảm dần `Z $\rightarrow$ A`, `9 $\rightarrow$ 0`).<br>• Có thể thêm nhiều tầng sắp xếp ưu tiên từ trên xuống dưới. |
| **Gom nhóm (Group by)** | Bấm nút <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **Gom nhóm**:<br>• Chọn cột muốn gom nhóm (ví dụ: `Phòng Ban` hoặc `Trạng Thái`). Toàn bộ bảng tính sẽ được chia thành các nhóm có thanh tiêu đề riêng, hiển thị số lượng bản ghi và cho phép thu gọn/mở rộng từng nhóm. |
| **Tô màu dòng (Row Color Rules)** | Bấm nút <img src="https://api.iconify.design/lucide:palette.svg?color=%23ff3333" width="16" alt="" /> **Màu sắc** $\rightarrow$ Thêm quy tắc màu:<br>• Thiết lập điều kiện (ví dụ: `Nếu [Trạng thái] = "Quá Hạn"`).<br>• Chọn màu nền tương ứng (ví dụ: màu đỏ cảnh báo). Toàn bộ dòng thỏa mãn điều kiện sẽ được tự động đổi màu nổi bật. |

---

### Giai đoạn 4 — Chia sẻ View và Biểu mẫu công khai

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở hộp thoại Chia sẻ** | Bấm nút <img src="https://api.iconify.design/lucide:share-2.svg?color=%23ff3333" width="16" alt="" /> **(Chia sẻ View)** trên thanh công cụ phía trên. |
| **2. Bật quyền chia sẻ công khai** | Bật nút gạt **Kích hoạt liên kết công khai**. Hệ thống sẽ cấp phát một mã UUID an toàn không thể đoán trước (`/form/:sharedViewUuid`). |
| **3. Sử dụng Link rút gọn & Mã QR** | • **Liên kết rút gọn**: Sao chép đường dẫn dạng ngắn gọn (`/s/:code`) cực kỳ tiện lợi để gửi qua tin nhắn SMS, Zalo hoặc mạng xã hội.<br>• **Mã QR Code**: Bấm nút <img src="https://api.iconify.design/lucide:qr-code.svg?color=%23ff3333" width="16" alt="" /> **Tải mã QR** để in ấn lên tờ rơi, bàn ăn hoặc bảng thông báo. |
| **4. Gắn tham số chiến dịch tiếp thị (UTM Presets)** | Mở mục **Cấu hình UTM Campaign**:<br>• Điền các tham số: `utm_source` (ví dụ: `facebook`), `utm_medium` (`cpc`), `utm_campaign` (`khuyen_mai_tet`).<br>• Liên kết tạo ra sẽ tự động đính kèm các tham số này, giúp theo dõi chính xác nguồn dẫn dữ liệu khi người dùng điền biểu mẫu. |
| **5. Xem mã cURL tích hợp ngoài** | Bấm vào nút <img src="https://api.iconify.design/lucide:code.svg?color=%23ff3333" width="16" alt="" /> **(Xem API cURL)** để lấy đoạn mã HTTP POST mẫu tích hợp form trực tiếp từ mã nguồn website ngoài vào bảng dữ liệu RedAI. |

---

## Kiểm tra kết quả

Sau khi thiết lập các Dạng xem và bộ công cụ hiển thị, bạn kiểm tra lại:

1. **Chuyển đổi mượt mà**: Nhấp lần lượt qua các tab View, dữ liệu hiển thị tức thì theo đúng cấu trúc của từng loại (Grid hiển thị dạng lưới bảng tính, Kanban hiển thị các cột trạng thái, Gallery hiển thị thẻ có ảnh bìa).
2. **Bộ lọc & Sắp xếp**: Dữ liệu chỉ hiển thị các bản ghi khớp với điều kiện lọc đã chọn; khi sửa hoặc thêm bản ghi mới, các quy tắc sắp xếp và tô màu dòng lập tức có hiệu lực tự động.
3. **Liên kết chia sẻ & Biểu mẫu**: Sao chép liên kết rút gọn `/s/:code`, mở thử trên cửa sổ trình duyệt ẩn danh (không đăng nhập) để kiểm chứng biểu mẫu hiển thị đầy đủ tiêu đề, logo và cho phép gửi dữ liệu thành công vào bảng.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể tự động tạo các dạng xem, cấu hình bộ lọc nâng cao và trích xuất đường dẫn chia sẻ, bạn cần đảm bảo Agent đã được trang bị Kỹ năng (Skill) sau:

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
| Bấm **+ Thêm View mới** trên thanh tab | `view_createView` | Khởi tạo dạng xem mới (`tableId`, `title`, `type`: GRID/KANBAN/GALLERY/CALENDAR/FORM). |
| Xem danh sách các View của một bảng | `view_listViews` | Lấy danh sách toàn bộ các View và cấu hình của bảng (`tableId`). |
| Chỉnh sửa bộ lọc, sắp xếp, ẩn hiện cột của View | `view_updateView` | Cập nhật cấu hình hiển thị của View (`tableId`, `viewId`, `filters`, `sorts`, `hiddenColumns`). |
| Đổi tên View hoặc khóa cấu hình View | `view_updateView` | Thay đổi tên hiển thị hoặc bật cờ `isLocked: true` (`tableId`, `viewId`, `title`, `isLocked`). |
| Bấm **Xóa View** trên menu ngữ cảnh | `view_deleteView` | Xóa một View khỏi bảng (`tableId`, `viewId`). |
| Bấm **Nhân bản View** | `view_duplicateView` | Nhân bản toàn bộ cấu hình của một View sang View mới (`tableId`, `viewId`). |
| Bật **Chia sẻ View** và lấy link rút gọn | `view_createSharedLink` | Kích hoạt liên kết công khai hoặc rút gọn cho View (`tableId`, `viewId`, `allowSubmit`). |

---

### Khung lệnh (Prompt) mẫu chuẩn 4 phần cho AI Agent

Dưới đây là mẫu câu lệnh hoàn chỉnh để ra lệnh cho AI Agent tự động khởi tạo và cấu hình chuyên sâu một Dạng xem Kanban cho bảng dữ liệu:

```text
[MỤC TIÊU]
Khởi tạo một Dạng xem Kanban mới mang tên "Tiến Độ Đơn Hàng" cho bảng `tbl_orders_2026`, phân nhóm theo cột "Trạng Thái" và chỉ lọc các đơn hàng phát sinh trong tháng hiện tại.

[DỮ LIỆU ĐẦU VÀO]
- Mã bảng dữ liệu: `tbl_orders_2026`
- Loại Dạng xem: KANBAN
- Tên View mới: "Tiến Độ Đơn Hàng"
- Trường phân nhóm Stacks: Cột "Trạng Thái" (`col_status_id`)
- Trường ảnh bìa Cover: Cột "Ảnh Sản Phẩm" (`col_product_img_id`)
- Bộ lọc áp dụng: Điều kiện `[Ngày Tạo] >= "2026-10-01"` kết hợp logic AND với `[Xóa Tạm Thời] = false`

[QUY TRÌNH THỰC THI]
1. Gọi tool `view_createView` với `type: "KANBAN"` và `title: "Tiến Độ Đơn Hàng"`.
2. Lấy `viewId` vừa nhận được, gọi tool `view_updateView` để cấu hình trường gom nhóm `groupFieldId: "col_status_id"`, `coverImageFieldId: "col_product_img_id"`.
3. Bổ sung cấu trúc bộ lọc `filters` vào cùng lệnh `view_updateView` để giới hạn các đơn hàng trong tháng.
4. Kiểm tra cấu hình trả về để xác nhận View đã lưu trữ đầy đủ.

[TIÊU CHÍ HOÀN THÀNH]
- Tab View Kanban "Tiến Độ Đơn Hàng" xuất hiện trên giao diện bảng `tbl_orders_2026`.
- Bảng hiển thị các cột trạng thái tương ứng với các giá trị của cột "Trạng Thái".
- Trả về mã `viewId` và liên kết truy cập trực tiếp đến Dạng xem này.
```

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Tạo View mới hoặc đổi bộ lọc/sắp xếp trên thanh công cụ | Gọi `view_getViewDetail` thấy mảng `filters` và `sorts` lưu đúng cấu hình vừa chọn. |
| Bật liên kết chia sẻ công khai và lấy short link | Gọi `view_getViewDetail` thấy trường `sharedLink` và mã `shortCode` hoạt động. |
| Kéo thẻ Kanban sang cột mới trên giao diện | Gọi `record_getRecordDetail` thấy giá trị của trường trạng thái đã được cập nhật tương ứng. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `view_createView` tạo View mới | Tải lại trang, thanh tab View xuất hiện thêm tab mới với biểu tượng tương ứng với loại View. |
| Agent gọi `view_updateView` cấu hình bộ lọc | Mở View trên trình duyệt, dữ liệu lập tức được lọc và nút Lọc hiển thị số điều kiện đang áp dụng. |
| Agent gọi `view_createSharedLink` tạo link công khai | Mở hộp thoại Chia sẻ View trên giao diện, thấy công tắc công khai đang bật kèm URL và mã QR. |
