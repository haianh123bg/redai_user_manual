## Mở khu vực Quản trị Dạng xem (Views)

Dạng xem (Views) trong **RedAI Database** cho phép người dùng quan sát, lọc và tương tác với cùng một cơ sở dữ liệu dưới nhiều góc độ khác nhau (bảng tính, bảng thẻ Kanban, thư viện ảnh, lịch biểu và biểu mẫu công khai). Mỗi bảng dữ liệu hỗ trợ không giới hạn số lượng dạng xem với các cấu hình bộ lọc và quyền hạn độc lập.

| Phương thức truy cập | Thao tác trên giao diện | Chi tiết hiển thị |
| :--- | :--- | :--- |
| **1. Mở rộng danh sách View từ Bảng** | Tại danh sách bảng (`Trang chủ > Database`), nhấp chuột vào dòng bảng cần xem. | Dòng bảng mở rộng ra danh sách các Dạng xem trực thuộc kèm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm view...**. |
| **2. Chuyển đổi giữa các Dạng xem** | Nhấp vào tên một Dạng xem trong danh sách con của bảng. | Hệ thống điều hướng vào màn hình làm việc tương ứng:<br>• **Grid View**: `Trang chủ > Database > View Details`<br>• **Kanban View**: `Trang chủ > Database > Kanban View`<br>• **Form View**: `Trang chủ > Database > Form View`<br>• **Calendar View**: `Trang chủ > Database > Calendar View` |

---

### Bảng chức năng menu tác vụ trên từng Dạng xem (<img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" />)

Khi rê chuột vào một dòng View và bấm menu ba chấm <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> (hoặc mở menu tiện ích trên thanh công cụ của View Details), một bảng chọn chức năng xuất hiện:

| Lệnh thao tác | Biểu tượng | Phạm vi & Chức năng chi tiết |
| :--- | :--- | :--- |
| **Đổi tên view** | <img src="https://api.iconify.design/lucide:pencil.svg?color=%23ff3333" width="16" alt="" /> | Đổi tên hiển thị nhận diện cho Dạng xem. |
| **Nhân bản View** | <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> | Tạo bản sao mới kế thừa toàn bộ cấu hình hiển thị, bộ lọc và quy tắc sắp xếp. |
| **Nhập dữ liệu** | <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> | Tải tệp Excel/CSV lên để nhập thêm các bản ghi mới vào view này. |
| **Xuất dữ liệu** | <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> | Xuất toàn bộ bản ghi đang hiển thị theo bộ lọc hiện tại ra tệp bảng tính. |
| **Trung Tâm Tiện Ích** | <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> | Mở ngăn kéo bộ công cụ nâng cao: in tem nhãn QR, làm sạch dữ liệu, sinh dữ liệu mẫu... |
| **Gộp dữ liệu** | <img src="https://api.iconify.design/lucide:git-merge.svg?color=%23ff3333" width="16" alt="" /> | Hợp nhất dữ liệu từ bảng hoặc nguồn dữ liệu khác vào view hiện tại. |
| **Cập nhật theo điều kiện** | <img src="https://api.iconify.design/lucide:edit-3.svg?color=%23ff3333" width="16" alt="" /> | Cập nhật hàng loạt giá trị cho các bản ghi thỏa mãn điều kiện chỉ định. |
| **Quyền bảng** | <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> | Mở ngăn kéo quản trị 9 phạm vi phân quyền bảng. |
| **Quyền trường** | <img src="https://api.iconify.design/lucide:shield-alert.svg?color=%23ff3333" width="16" alt="" /> | Mở ngăn kéo phân quyền xem và sửa chi tiết cho từng cột dữ liệu. |
| **Bảo mật cấp bản ghi** | <img src="https://api.iconify.design/lucide:lock.svg?color=%23ff3333" width="16" alt="" /> | Phân quyền Xem, Xuất, Sửa, Xóa bản ghi theo vai trò hoặc bộ lọc điều kiện. |
| **Shared view** | <img src="https://api.iconify.design/lucide:share-2.svg?color=%23ff3333" width="16" alt="" /> | Mở ngăn kéo cấu hình liên kết chia sẻ công khai kèm mật mã bảo vệ. |
| **Xóa view** | <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> | Xóa dạng xem này khỏi bảng (lưu ý: mỗi bảng phải giữ lại tối thiểu 1 view cuối cùng). |

---

## Các bước thực hiện

### Giai đoạn 1 — Khởi tạo Dạng xem mới (Cấu hình View)

| Bước | Thao tác thực hiện | Mô tả chi tiết |
| :--- | :--- | :--- |
| **1. Mở ngăn kéo Cấu hình View** | Tại danh sách mở rộng của bảng, nhấp vào nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm view...**. | Ngăn kéo **Cấu hình View** xuất hiện từ cạnh phải màn hình. |
| **2. Chọn loại View** | Tại mục **Loại View**, nhấp vào liên kết đỏ **Thay đổi** để chọn 1 trong 5 loại hiển thị:<br>• **Grid**: Bảng tính lưới hàng và cột truyền thống.<br>• **Kanban**: Bảng thẻ quy trình theo trạng thái.<br>• **Form**: Biểu mẫu thu thập dữ liệu.<br>• **Calendar**: Lịch biểu mốc thời gian.<br>• **Gallery**: Thư viện thẻ hình ảnh trực quan. | Xác định mô hình trực quan hóa dữ liệu phù hợp với nhu cầu. |
| **3. Đặt tên và mô tả View** | • **Tên View**: Nhập tên gợi nhớ vào ô `Ví dụ: Tất cả khách hàng...`.<br>• Công tắc **Thêm mô tả**: Bật công tắc để nhập văn bản ghi chú về tiêu chí lọc của View này. | Giúp các thành viên trong nhóm hiểu rõ mục đích của View. |
| **4. Cấu hình quyền quản trị View** | Chọn 1 trong 3 chế độ tại mục **Quyền cấu hình view**:<br>• **Cộng tác** (*Mặc định*): Editor, Admin và Owner đều có thể chỉnh sửa cấu hình view.<br>• **Đã khóa**: Chỉ người tạo view, Admin và Owner mới có quyền thay đổi bộ lọc, sắp xếp và cột.<br>• **Cá nhân**: Chỉ bạn, Admin và Owner mới nhìn thấy và thay đổi cấu hình view này. | Bảo vệ cấu hình hiển thị chuẩn mực của doanh nghiệp tránh bị sửa ngoài ý muốn. |
| **5. Xác nhận khởi tạo** | Bấm nút xác nhận ở chân ngăn kéo. | View mới lập tức được tạo và hiển thị trong danh sách dạng xem của bảng. |

---

### Giai đoạn 2 — Vận hành và tùy biến chi tiết từng Dạng xem

#### 1. Dạng xem Bảng tính lưới (Grid View)

Màn hình `Trang chủ > Database > View Details` cung cấp thanh công cụ mạnh mẽ phía trên bảng dữ liệu:

| Công cụ Toolbar | Biểu tượng | Chức năng thao tác |
| :--- | :--- | :--- |
| **Thêm bản ghi** | <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> | Nút màu đỏ ở đầu bảng (hoặc dòng dấu cộng ở chân bảng) để thêm dòng mới vào bảng tính. |
| **Hoàn tác & Làm lại** | <img src="https://api.iconify.design/lucide:undo.svg?color=%23ff3333" width="16" alt="" /> / <img src="https://api.iconify.design/lucide:redo.svg?color=%23ff3333" width="16" alt="" /> | Hủy bỏ hoặc khôi phục thao tác sửa dữ liệu ô vừa thực hiện. |
| **Ẩn/Hiện trường** | <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> | Kèm huy hiệu đỏ hiển thị số cột (ví dụ: `25`). Bấm để bật/tắt hiển thị từng cột riêng cho View này. |
| **Bộ lọc (Filter)** | <img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" /> | Thiết lập các điều kiện lọc dữ liệu kết hợp toán tử logic **Và (AND)** / **Hoặc (OR)**. |
| **Sắp xếp (Sort)** | <img src="https://api.iconify.design/lucide:arrow-up-down.svg?color=%23ff3333" width="16" alt="" /> | Sắp xếp thứ tự bản ghi tăng dần (A → Z, 0 → 9) hoặc giảm dần theo một hoặc nhiều cột. |
| **Gom nhóm (Group by)** | <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> | Gom các dòng bản ghi thành các nhóm có thanh tiêu đề riêng theo giá trị của cột chỉ định. |
| **Chiều cao dòng (Row Height)** | <img src="https://api.iconify.design/lucide:rows.svg?color=%23ff3333" width="16" alt="" /> | Kèm huy hiệu trạng thái `1`. Cho phép chọn mức hiển thị dòng: Thấp, Trung bình, Cao, Rất cao. |
| **Xóa bản ghi đã chọn** | <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> | Xóa nhanh các bản ghi đang được tích chọn qua hộp kiểm đầu dòng. |
| **Tìm kiếm** | <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> | Tìm nhanh từ khóa xuất hiện trên mọi ô tính của view. |
| **Làm mới & Toàn màn hình** | <img src="https://api.iconify.design/lucide:rotate-cw.svg?color=%23ff3333" width="16" alt="" /> / <img src="https://api.iconify.design/lucide:maximize-2.svg?color=%23ff3333" width="16" alt="" /> | Tải lại dữ liệu và mở rộng bảng tính trọn vẹn màn hình trình duyệt. |

##### Thao tác Chi tiết dòng bản ghi (Row Detail Modal)
Nhấp đúp chuột vào bất kỳ dòng nào hoặc bấm nút mở rộng để mở hộp thoại **Chi tiết dòng #{N}**:
- **Cột bên trái**: Hiển thị toàn bộ các trường của bản ghi dạng biểu mẫu dọc, dễ dàng nhập liệu các văn bản dài.
- **Cột bên phải**: Gồm 2 tab quan trọng:
  - Tab **Bình luận**: Gửi nhận xét và trao đổi nội bộ về bản ghi này.
  - Tab **Lịch sử thay đổi**: Ghi nhận chi tiết nhân sự thực hiện cập nhật và mốc thời gian (ví dụ: *"Bùi Mạnh Phi đã cập nhật bản ghi - 3 ngày trước"*).
- **Cụm nút góc dưới bên trái**: Nút sao chép bản ghi <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" />, nút xem cấu trúc JSON `< / >`, và nút xóa bản ghi <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" />.

---

#### 2. Dạng xem Bảng thẻ quy trình (Kanban View)

Giao diện `Trang chủ > Database > Kanban View` tổ chức các bản ghi thành các thẻ công việc di chuyển qua các cột trạng thái (Stacks):

| Thành phần | Đặc điểm & Thao tác |
| :--- | :--- |
| **Cột trạng thái (Stacks)** | Bao gồm cột mặc định `(Chưa phân loại)`, các cột theo giá trị trường lựa chọn và nút `+ New stack` ở bên phải để thêm cột trạng thái mới. |
| **Menu trên tiêu đề cột (<img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" />)** | Bấm biểu tượng ba chấm trên đầu mỗi cột để chọn: `+ New record` (Thêm bản ghi mới vào cột này), `< Collapse stack` (Thu gọn cột), `Collapse all` (Thu gọn mọi cột), `Expand all` (Mở rộng mọi cột), `Delete stack` (Xóa cột). |
| **Kéo thả thẻ** | Kéo thẻ từ cột này sang cột khác để tự động cập nhật giá trị trường trạng thái tương ứng. |
| **Chân cột trạng thái** | Hiển thị nút `+ Thêm thẻ` và huy hiệu đếm tổng số thẻ có trong cột (ví dụ: `5 thẻ`, `1 thẻ`). |

---

#### 3. Dạng xem Biểu mẫu thu thập dữ liệu (Form View)

Giao diện `Trang chủ > Database > Form View` dùng để thiết kế và chia sẻ biểu mẫu nhập liệu công khai:

| Khu vực | Thành phần giao diện | Chi tiết thiết lập |
| :--- | :--- | :--- |
| **Khung xem trước biểu mẫu (Ở giữa)** | Ảnh bìa (Banner) | Hiển thị hình ảnh nhận diện thương hiệu đầu trang form. |
| | Tiêu đề & Các câu hỏi | Tiêu đề lớn của form và các khối nhập liệu tương ứng với từng cột dữ liệu trong bảng. |
| **Panel cấu hình bên phải** | **Tab Cài đặt** | • **Tiêu đề lớn**: Nhập tên biểu mẫu (ví dụ: `Form đặt lịch khám Hoàng Anh PHCN`).<br>• **Ảnh Banner (URL)**: Dán link ảnh banner thương hiệu (để trống nếu dùng ảnh mặc định).<br>• **Mô tả / Phụ đề**: Nhập hướng dẫn điền form cho khách hàng.<br>• **Thông điệp gửi thành công**: Lời cảm ơn xuất hiện sau khi người dùng gửi form. |
| | **Tab Trường dữ liệu** | • Kéo thả biểu tượng tay cầm để sắp xếp lại thứ tự xuất hiện các câu hỏi từ trên xuống dưới.<br>• Nhấp vào từng trường để đặt: **Nhãn tùy chỉnh**, **Placeholder (Gợi ý)**, **Văn bản trợ giúp** và công tắc **Bắt buộc nhập**. |
| **Thanh công cụ Form** | Nút <img src="https://api.iconify.design/lucide:share-2.svg?color=%23ff3333" width="16" alt="" /> **Chia sẻ** | Mở liên kết công khai hoặc tải mã QR để người ngoài điền biểu mẫu mà không cần tài khoản đăng nhập. |

---

#### 4. Dạng xem Lịch biểu thời gian (Calendar View)

Giao diện `Trang chủ > Database > Calendar View` trực quan hóa các bản ghi theo mốc ngày:

| Thành phần | Đặc điểm & Thao tác |
| :--- | :--- |
| **Cụm điều hướng thời gian** | • Nút **Hôm nay**: Quay nhanh về ngày hiện tại.<br>• Nút mũi tên `<` và `>`: Di chuyển qua lại giữa các tháng hoặc tuần.<br>• Hiển thị mốc tháng năm đang xem (ví dụ: `Tháng 10, 2026`). |
| **Bộ chuyển đổi dải xem (Scope)** | Chuyển đổi linh hoạt qua 4 nút bấm: **Năm** | **Tháng** (*Mặc định*) | **Tuần** | **Ngày**. |
| **Thanh công cụ Lịch** | Gồm nút Lọc (<img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" />), Ẩn/Hiện trường (<img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" />), Làm mới (<img src="https://api.iconify.design/lucide:rotate-cw.svg?color=%23ff3333" width="16" alt="" />), Cài đặt trường ngày bắt đầu/kết thúc (<img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" />) và Toàn màn hình. |

---

## Kiểm tra kết quả

Sau khi hoàn thiện thiết lập các Dạng xem, người dùng kiểm tra lại:

| Hạng mục kiểm tra | Tiêu chí đạt chuẩn |
| :--- | :--- |
| **1. Khả năng chuyển đổi View** | Bấm chuyển đổi giữa các tab View, dữ liệu phản hồi mượt mà theo đúng đặc trưng trực quan của từng dạng (lưới, cột thẻ, biểu mẫu, lịch biểu). |
| **2. Hiệu lực bộ lọc & Gom nhóm** | Bản ghi tự động được gom nhóm chính xác theo trường chỉ định và chỉ hiển thị các dữ liệu thỏa mãn điều kiện lọc. |
| **3. Nhật ký sửa đổi (Row Detail)** | Khi có thay đổi dữ liệu trong ô tính, kiểm tra tab Lịch sử thay đổi trong cửa sổ Chi tiết dòng thấy ghi nhận đúng tên nhân sự và thời điểm cập nhật. |
