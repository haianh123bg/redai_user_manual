## Mở khu vực Quản lý Bảng dữ liệu và Phân loại Danh mục

Để quản lý cơ sở dữ liệu động, khởi tạo bảng mới và tổ chức phân loại theo danh mục trên **RedAI Database**, người dùng truy cập từ giao diện làm việc chính theo các bước:

| Bước | Thao tác trên giao diện | Chi tiết hiển thị |
| :--- | :--- | :--- |
| **1. Chọn Không gian làm việc** | Nhấp vào menu chuyển đổi ở góc trên bên trái màn hình. | Chọn đúng **Workspace** và **Base** đang làm việc để quản trị dữ liệu tương ứng. |
| **2. Truy cập phân hệ Database** | Tại màn hình **Trang chủ**, nhấp vào thẻ dịch vụ **Database**. | Thẻ có mô tả *"Hệ thống Low-code Database thế hệ mới tạo và quản lý bảng dữ liệu, tự động hóa quy trình dữ liệu cho AI Agent"*. Thanh điều hướng hiển thị đường dẫn breadcrumb: `Trang chủ > Database`. |

---

### Bố cục không gian làm việc Database

Màn hình làm việc trung tâm được chia làm 2 khu vực chức năng chính:

| Khu vực | Thành phần giao diện | Chức năng chi tiết |
| :--- | :--- | :--- |
| **Thanh bên trái (Danh mục)** | Nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm danh mục mới** | Nằm cạnh tiêu đề `Danh mục`, mở hộp thoại khởi tạo nhóm danh mục phân loại mới. |
| | <img src="https://api.iconify.design/lucide:layout-list.svg?color=%23ff3333" width="16" alt="" /> **Tất cả bảng người dùng tạo** | Mục mặc định ở trên cùng, hiển thị toàn bộ các bảng do người dùng tạo trong cơ sở dữ liệu. |
| | **Danh mục tùy chỉnh** (Biểu tượng thư mục) | Danh sách các nhóm do người dùng tự đặt tên. Rê chuột vào tên danh mục sẽ hiển thị 2 biểu tượng thao tác nhanh: <img src="https://api.iconify.design/lucide:pencil.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa tên danh mục)** và <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Xóa danh mục)**. |
| | <img src="https://api.iconify.design/lucide:folder.svg?color=%23ff3333" width="16" alt="" /> **Chưa có Category** | Tập hợp các bảng dữ liệu chưa được gắn vào bất kỳ nhóm danh mục nào. |
| | <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **Tất cả bảng hệ thống** | Nhóm các bảng dữ liệu hệ thống của Workspace, đi kèm các phân nhóm mặc định: `Email Marketing`, `Zalo`, `Đối tượng`... |
| **Khu vực hiển thị danh sách bảng (Bên phải)** | **Thanh công cụ phía trên (Toolbar)** | • <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **Tìm kiếm**: Tìm nhanh bảng theo tên.<br>• <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo bảng** (Nút màu đỏ): Mở hộp thoại khởi tạo bảng dữ liệu mới.<br>• <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Thùng rác**: Chuyển sang khu vực quản lý bảng đã xóa tạm thời.<br>• <img src="https://api.iconify.design/lucide:rotate-cw.svg?color=%23ff3333" width="16" alt="" /> **Tải lại danh sách bảng**: Làm mới danh sách bảng theo thời gian thực.<br>• <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> **(Tùy chọn khác)**: Menu mở rộng các tiện ích bổ sung. |
| | **Dòng bảng dữ liệu** | Mỗi bảng hiển thị biểu tượng bảng tính và tên bảng. Nhấp vào dòng bảng để mở rộng các Dạng xem (Views) trực thuộc và nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm view...**. |
| | **Menu thao tác trên bảng (<img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" />)** | Rê chuột vào dòng bảng sẽ xuất hiện nút <img src="https://api.iconify.design/lucide:rotate-cw.svg?color=%23ff3333" width="16" alt="" /> **Làm mới**, nút <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> **(Menu chức năng)** và mũi tên <img src="https://api.iconify.design/lucide:chevron-right.svg?color=%23ff3333" width="16" alt="" />. |

---

### Bảng chức năng menu ngữ cảnh của từng bảng dữ liệu

Khi bấm vào biểu tượng <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> trên dòng bảng, một bảng chọn chức năng xuất hiện với tiêu đề là tên bảng (kèm nút sao chép slug định danh):

| Lệnh thao tác | Biểu tượng | Tác vụ thực hiện |
| :--- | :--- | :--- |
| **Đổi tên bảng** | <img src="https://api.iconify.design/lucide:pencil.svg?color=%23ff3333" width="16" alt="" /> | Mở ngăn kéo bên phải để chỉnh sửa lại tên hiển thị của bảng. |
| **Di chuyển sang category** | <img src="https://api.iconify.design/lucide:folder-input.svg?color=%23ff3333" width="16" alt="" /> | Chọn danh mục đích từ danh sách để chuyển nhóm quản lý cho bảng. |
| **Trường** | <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> | Điều hướng sang màn hình quản trị cấu trúc cột: `Trang chủ > Database > Table Fields`. |
| **Quyền bảng** | <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> | Mở ngăn kéo bên phải cấu hình ma trận 9 quyền thao tác cấp độ bảng. |
| **Quyền trường** | <img src="https://api.iconify.design/lucide:shield-alert.svg?color=%23ff3333" width="16" alt="" /> | Mở ngăn kéo bên phải thiết lập quyền xem và sửa chi tiết cho từng cột dữ liệu. |
| **Bảo mật cấp bản ghi** | <img src="https://api.iconify.design/lucide:lock.svg?color=%23ff3333" width="16" alt="" /> | Mở ngăn kéo bên phải thiết lập điều kiện phân quyền Xem, Xuất, Sửa, Xóa theo từng vai trò hoặc người dùng. |
| **Quan hệ** | <img src="https://api.iconify.design/lucide:network.svg?color=%23ff3333" width="16" alt="" /> | Điều hướng sang sơ đồ quan hệ tương tác trực quan: `Trang chủ > Database > Quan hệ`. |
| **Webhooks** | <img src="https://api.iconify.design/lucide:webhook.svg?color=%23ff3333" width="16" alt="" /> | Mở hộp thoại `Tạo Webhook mới 🦉` để kết nối dữ liệu thời gian thực sang Workflow hoặc bên ngoài. |
| **Đồ thị bảng (Graph)** | <img src="https://api.iconify.design/lucide:git-graph.svg?color=%23ff3333" width="16" alt="" /> | Mở khung nhìn đồ thị dữ liệu liên kết riêng của bảng này. |

---

## Các bước thực hiện

### Giai đoạn 1 — Khởi tạo bảng dữ liệu mới

Khi bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo bảng** trên thanh công cụ, hộp thoại **Tạo bảng** xuất hiện với 3 tab chính:

```
[ + Tạo bảng ]          [ ✨ Tạo bằng AI ]          [ Import ]
  ├── Tạo trực tiếp
  └── Tạo từ bảng có sẵn
```

#### Phương án 1 — Tạo trực tiếp (Tạo bảng trống)

| Bước | Thao tác thực hiện | Mô tả chi tiết |
| :--- | :--- | :--- |
| **1. Chọn tab Tạo trực tiếp** | Trong tab **+ Tạo bảng**, chọn nhánh phụ **Tạo trực tiếp**. | Mở biểu mẫu cấu hình cơ bản cho bảng mới. |
| **2. Nhập thông số bảng** | Điền các trường thông tin:<br>• **Tên bảng \***: Nhập tên bảng muốn khởi tạo vào ô `Nhập tên bảng...`.<br>• **Danh mục**: Chọn danh mục quản lý từ danh sách thả xuống (hoặc để mặc định `Không chọn danh mục`).<br>• **Nguồn dữ liệu**: Chọn nguồn cơ sở dữ liệu lưu trữ (mặc định là `Mặc định`). | Cung cấp định danh và vị trí lưu trữ cho bảng. |
| **3. Xác nhận tạo bảng** | Bấm nút xác nhận ở góc dưới hộp thoại. | Bảng mới xuất hiện trong danh sách và sẵn sàng để cấu hình trường dữ liệu. |

---

#### Phương án 2 — Tạo từ bảng có sẵn (Kế thừa cấu trúc hoặc dữ liệu)

| Bước | Thao tác thực hiện | Mô tả chi tiết |
| :--- | :--- | :--- |
| **1. Chọn tab Tạo từ bảng có sẵn** | Trong tab **+ Tạo bảng**, chọn nhánh phụ **Tạo từ bảng có sẵn**. | Mở biểu mẫu sao chép và kế thừa bảng. |
| **2. Cấu hình bảng nguồn** | • **Tên bảng \***: Nhập tên cho bảng mới.<br>• **Bảng nguồn \***: Nhấp vào menu thả xuống `Chọn bảng nguồn` và chọn bảng gốc muốn nhân bản. | Xác định nguồn kế thừa cấu trúc. |
| **3. Tùy chọn sao chép dữ liệu** | Bật công tắc <img src="https://api.iconify.design/lucide:toggle-right.svg?color=%23ff3333" width="16" alt="" /> **Sao chép dữ liệu** nếu muốn giữ lại các bản ghi hiện có (nếu tắt, hệ thống chỉ nhân bản cấu trúc cột trống). | Kích hoạt bộ tùy biến dữ liệu sao chép. |
| **4. Tùy chỉnh trường và bộ lọc (Tùy chọn)** | Khi công tắc Sao chép dữ liệu được bật:<br>• **Tùy chỉnh field sao chép**: Bật công tắc để chọn từng cột cần sao chép qua danh sách hộp kiểm (kèm nút `Bỏ chọn tất cả`).<br>• **Bộ lọc**: Bấm nút `+ Thêm điều kiện lọc` hoặc `+ Thêm nhóm` để thiết lập quy tắc lọc dữ liệu theo điều kiện logic **Và (AND)** / **Hoặc (OR)** (ví dụ: chỉ sao chép các bản ghi có trạng thái Hoàn thành). | Tối ưu phạm vi dữ liệu được kế thừa vào bảng mới. |
| **5. Hoàn tất nhân bản** | Bấm nút xác nhận tạo bảng. | Hệ thống tiến hành tạo bảng mới với đúng cấu trúc và dữ liệu lọc đã chỉ định. |

---

#### Phương án 3 — Tạo bằng AI (AI Blueprint)

| Bước | Thao tác thực hiện | Mô tả chi tiết |
| :--- | :--- | :--- |
| **1. Chọn tab Tạo bằng AI** | Nhấp vào tab **✨ Tạo bằng AI** trên thanh tiêu đề hộp thoại. | Mở khung nhập yêu cầu cho trợ lý thiết kế dữ liệu AI. |
| **2. Nhập mô tả nghiệp vụ** | Nhập yêu cầu nghiệp vụ bằng văn bản tự nhiên (ví dụ: *"Tạo bảng Quản lý Hợp đồng gồm Mã hợp đồng, Khách hàng, Giá trị, Ngày ký, Hạn nghiệm thu và Trạng thái thanh toán"*). | Cung cấp ngữ cảnh nghiệp vụ để AI phân tích cấu trúc cột phù hợp. |
| **3. Phân tích và duyệt Blueprint** | Bấm nút phân tích để AI đề xuất danh sách cột, kiểu dữ liệu tương ứng và xem trước sơ đồ quan hệ. | Người dùng duyệt lại danh sách cột đề xuất, thêm bớt trường tùy ý trước khi bấm xác nhận tạo. |

---

#### Phương án 4 — Import từ tệp ngoại bộ (CSV / Excel / JSON)

| Bước | Thao tác thực hiện | Mô tả chi tiết |
| :--- | :--- | :--- |
| **1. Chọn tab Import** | Nhấp vào tab **Import** (biểu tượng bảng tính màu xanh lá). | Tiêu đề hộp thoại chuyển thành **Tạo bảng từ Excel**. |
| **2. Chọn Danh mục & Nguồn dữ liệu** | Chọn danh mục phân loại và nguồn dữ liệu đích từ các menu thả xuống. | Định vị bảng trước khi tải tệp lên. |
| **3. Chọn loại tệp** | Chọn 1 trong 3 định dạng tại mục **1. Chọn loại tệp**:<br>• **CSV** (*Giá trị phân tách bằng dấu phẩy*).<br>• **Excel (XLSX)** (*Mở bằng Excel*).<br>• **JSON** (*JavaScript Object Notation*). | Xác định quy cách đọc cấu trúc tệp nguồn. |
| **4. Tải tệp lên** | Tại mục **2. Tải tệp lên**, nhấp vào khung `Chọn file để tải lên` hoặc kéo thả tệp vào khung.<br>*(Hệ thống hỗ trợ file `.xlsx`, `.xls`, `.csv`, `.json` với dung lượng tối đa **10MB**)*. | Hệ thống phân tích tệp và hiển thị số sheet cùng số cột dữ liệu có trong tệp. |
| **5. Ánh xạ trường dữ liệu (Nhập dữ liệu)** | Hệ thống chuyển sang màn hình **Nhập dữ liệu** với bảng ánh xạ 3 cột:<br>• **TRƯỜNG HỆ THỐNG TƯƠNG ỨNG**: Danh sách các trường dữ liệu của hệ thống.<br>• **NGUỒN DỮ LIỆU**: Menu thả xuống chọn cột tương ứng từ file đã tải lên (hoặc chọn `— Bỏ qua (Không import) —`).<br>• **CẤU HÌNH GIÁ TRỊ / ÁNH XẠ**: Thiết lập quy tắc chuyển đổi giá trị nếu cần. | Khớp nối chính xác dữ liệu từ file ngoại bộ vào hệ thống bảng RedAI. |
| **6. Xác nhận nhập dữ liệu** | Bấm nút xác nhận để thực thi tiến trình import. | Hệ thống tự động tạo bảng mới và nhập hàng loạt bản ghi theo ánh xạ đã chọn. |

---

### Giai đoạn 2 — Quản lý phân loại danh mục (Categories)

| Bước | Thao tác thực hiện | Mô tả chi tiết |
| :--- | :--- | :--- |
| **1. Tạo danh mục mới** | Tại thanh bên trái, bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> cạnh chữ **Danh mục**. | Nhập tên danh mục mới (ví dụ: `Bán Hàng & CSKH`, `Kế Toán`) và bấm lưu. |
| **2. Gán hoặc di chuyển bảng vào danh mục** | Rê chuột vào dòng bảng cần phân loại → Bấm <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> → Chọn <img src="https://api.iconify.design/lucide:folder-input.svg?color=%23ff3333" width="16" alt="" /> **Di chuyển sang category**. | Chọn danh mục đích từ danh sách để chuyển bảng vào nhóm quản lý tương ứng. |
| **3. Đổi tên danh mục** | Rê chuột vào tên danh mục trên thanh bên trái → Bấm biểu tượng <img src="https://api.iconify.design/lucide:pencil.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa)**. | Nhập tên mới cho danh mục và lưu lại. |
| **4. Xóa danh mục** | Rê chuột vào tên danh mục → Bấm biểu tượng <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Xóa)**. | Xác nhận xóa danh mục. Các bảng bên trong danh mục này sẽ tự động chuyển về mục <img src="https://api.iconify.design/lucide:folder.svg?color=%23ff3333" width="16" alt="" /> **Chưa có Category**, toàn bộ dữ liệu bảng vẫn được bảo toàn nguyên vẹn. |

---

### Giai đoạn 3 — Vận hành Thùng rác và Khôi phục bảng dữ liệu

Hệ thống RedAI Database tích hợp cơ chế bảo vệ xóa mềm tự động để chống thất thoát dữ liệu do thao tác nhầm lẫn:

| Bước | Thao tác thực hiện | Mô tả chi tiết |
| :--- | :--- | :--- |
| **1. Xóa tạm thời bảng dữ liệu** | Rê chuột vào dòng bảng cần xóa → Bấm biểu tượng <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> → Chọn lệnh xóa bảng. | Bảng được gỡ khỏi danh sách hoạt động và chuyển vào lưu trữ tạm thời trong Thùng rác. |
| **2. Truy cập khu vực Thùng rác** | Trên thanh công cụ phía trên bên phải màn hình danh sách bảng, bấm vào biểu tượng <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Thùng rác**. | Màn hình hiển thị danh sách các bảng bị xóa tạm thời kèm khung thông báo vàng:<br>*"Cơ chế lưu trữ thùng rác: Các bảng trong thùng rác có thể được khôi phục bất cứ lúc nào. Sau 10 ngày kể từ khi xóa mềm, hệ thống sẽ tự động xóa vĩnh viễn dữ liệu."* |
| **3. Kiểm tra thông tin lưu trữ** | Quan sát danh sách bảng trong thùng rác. | Mỗi dòng hiển thị: Tên bảng, slug định danh và đồng hồ đếm ngược: `(clock) Còn {N} ngày nữa sẽ xóa vĩnh viễn`. |
| **4. Khôi phục bảng dữ liệu** | Trên dòng bảng cần lấy lại, bấm biểu tượng <img src="https://api.iconify.design/lucide:rotate-ccw.svg?color=%23ff3333" width="16" alt="" /> **Khôi phục**. | Bảng được đưa trở lại danh mục ban đầu với đầy đủ cấu trúc cột, các Dạng xem (Views) và dữ liệu nguyên vẹn. |
| **5. Xóa vĩnh viễn dữ liệu** | Trên dòng bảng muốn hủy bỏ hoàn toàn, bấm biểu tượng <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Xóa vĩnh viễn**. | Hệ thống yêu cầu xác nhận lần cuối trước khi xóa hoàn toàn bảng khỏi cơ sở dữ liệu (thao tác này không thể phục hồi). |
| **6. Thao tác hàng loạt & Quay lại** | • Dùng hộp kiểm `[ ] Chọn tất cả` để khôi phục hoặc xóa vĩnh viễn nhiều bảng cùng lúc.<br>• Bấm biểu tượng mũi tên <img src="https://api.iconify.design/lucide:arrow-left.svg?color=%23ff3333" width="16" alt="" /> trên thanh công cụ Thùng rác để quay lại danh sách bảng hoạt động. | Quản lý vòng đời dữ liệu theo lô nhanh chóng và tiện lợi. |

---

## Kiểm tra kết quả

Sau khi hoàn thành quy trình khởi tạo bảng và sắp xếp danh mục, người dùng kiểm tra lại theo các tiêu chí:

| Hạng mục kiểm tra | Tiêu chí đạt chuẩn |
| :--- | :--- |
| **1. Vị trí hiển thị bảng** | Bảng mới xuất hiện đúng trong danh mục đã chỉ định hoặc trong mục `Chưa có Category`. |
| **2. Cấu trúc trường & Dữ liệu** | Nhấp vào dòng bảng để mở Dạng xem mặc định; kiểm tra tên các cột và số lượng bản ghi hiển thị chính xác theo phương án khởi tạo (bảng trống, bảng nhân bản hoặc import từ file). |
| **3. Tính năng khôi phục** | Thử nghiệm đưa bảng vào Thùng rác và khôi phục lại; bảng hiển thị đúng thời hạn 10 ngày đếm ngược và phục hồi nguyên vẹn khi nhấn nút khôi phục. |
