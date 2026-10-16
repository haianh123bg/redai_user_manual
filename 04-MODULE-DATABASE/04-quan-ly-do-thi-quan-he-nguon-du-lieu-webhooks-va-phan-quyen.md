## Tổng quan các tính năng quản trị nâng cao

Bên cạnh các thao tác bảng tính và dạng xem thông thường, **RedAI Database** cung cấp một hệ thống công cụ quản trị cấp cao toàn diện nhằm phục vụ kiến trúc dữ liệu doanh nghiệp phức tạp, tự động hóa luồng quy trình thời gian thực và bảo mật kiểm soát truy cập nhiều tầng. Tài liệu này tổng hợp hướng dẫn chi tiết cho 5 tính năng quản trị cốt lõi:

1. **Đồ thị quan hệ bảng dữ liệu (`/database/relations`)**: Trực quan hóa toàn bộ lược đồ cơ sở dữ liệu (Entity Relationship Diagram - ERD) dưới dạng đồ thị tương tác, cho phép thiết lập liên kết giữa các bảng trực tiếp bằng thao tác kéo thả.
2. **Tập hợp tùy chọn dùng chung (`/database/option-sets`)**: Quản lý tập trung các bộ danh mục lựa chọn (Option Sets) tái sử dụng cho nhiều trường Select trên nhiều bảng dữ liệu khác nhau.
3. **Nguồn dữ liệu ngoại bộ (`/database/sources`)**: Quản trị các kết nối cơ sở dữ liệu bên ngoài (PostgreSQL, MySQL, API Endpoints) tích hợp trực tiếp vào hệ thống RedAI.
4. **Tự động hóa Webhooks & Scheduled Hooks (`/database/table/:tableId/settings/webhooks`)**: Thiết lập cơ chế bắn dữ liệu thời gian thực sang các hệ thống bên ngoài khi có biến động dữ liệu và lên lịch kích hoạt định kỳ kèm nhật ký thực thi chi tiết.
5. **Phân quyền truy cập và Khóa bảo vệ (`/database/table/:tableId/settings/permissions`)**: Kiểm soát chi tiết quyền đọc/ghi ở cấp độ bảng, cấp độ bản ghi và cấp độ từng trường dữ liệu cho từng vai trò người dùng.

---

## Hướng dẫn chi tiết từng tính năng

### Tính năng 1 — Đồ thị quan hệ bảng dữ liệu (Database Relations ERD)

Đồ thị quan hệ giúp người quản trị có cái nhìn toàn cảnh về cấu trúc liên kết dữ liệu giữa tất cả các bảng trong không gian làm việc.

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Truy cập màn hình Đồ thị quan hệ** | Tại màn hình Danh sách Bảng (`/database`), bấm nút <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> **(Tiện ích nâng cao)** trên thanh công cụ $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:git-fork.svg?color=%23ff3333" width="16" alt="" /> **Đồ thị quan hệ** (hoặc truy cập trực tiếp đường dẫn `/database/relations`). |
| **2. Lọc bảng theo danh mục** | Sử dụng thanh công cụ phía trên để lọc các bảng thuộc một danh mục cụ thể (ví dụ: chỉ hiển thị các bảng thuộc nhóm `Bán Hàng` hoặc `Kho Vận`) nhằm tránh rối mắt khi cơ sở dữ liệu có hàng chục bảng. |
| **3. Khám phá các Node bảng** | Mỗi bảng hiển thị dưới dạng một khối thẻ (Node) bao gồm:<br>• Tên bảng và số lượng bản ghi.<br>• Danh sách các cột chính kèm biểu tượng kiểu dữ liệu.<br>• Cột khóa chính đại diện có biểu tượng ngôi sao <img src="https://api.iconify.design/lucide:star.svg?color=%23ff3333" width="16" alt="" />.<br>• Các đường nối biểu diễn quan hệ (1-1, 1-N, N-N) với mũi tên chỉ rõ hướng liên kết. |
| **4. Tạo liên kết bảng bằng kéo thả** | Nhấp giữ chuột vào điểm nối tròn (Handle) ở cạnh một trường trong bảng A, kéo và thả vào điểm nối của bảng B. Hộp thoại **Cấu hình quan hệ** sẽ xuất hiện ngay lập tức để bạn chọn loại liên kết (Một - Nhiều, Nhiều - Một, Nhiều - Nhiều) và đặt tên cho trường liên kết đảo ngược. |
| **5. Điều hướng khung nhìn sơ đồ** | Sử dụng cụm nút điều khiển ở góc dưới bên trái:<br>• <img src="https://api.iconify.design/lucide:zoom-in.svg?color=%23ff3333" width="16" alt="" /> / <img src="https://api.iconify.design/lucide:zoom-out.svg?color=%23ff3333" width="16" alt="" />: Phóng to hoặc thu nhỏ khung nhìn canvas.<br>• <img src="https://api.iconify.design/lucide:maximize.svg?color=%23ff3333" width="16" alt="" /> **(Vừa khung nhìn)**: Tự động căn chỉnh toàn bộ các bảng nằm trọn trong màn hình.<br>• <img src="https://api.iconify.design/lucide:layout.svg?color=%23ff3333" width="16" alt="" /> **(Tự động sắp xếp - Auto Layout)**: Thuật toán tự động sắp xếp lại vị trí các bảng theo cấu trúc hình cây khoa học, tránh các đường liên kết đè chéo nhau. |

---

### Tính năng 2 — Tập hợp tùy chọn dùng chung (Shared Option Sets)

Khi có các danh mục chuẩn mực được sử dụng lặp lại ở nhiều bảng khác nhau (ví dụ: `Danh sách 63 Tỉnh/Thành`, `Quy mô doanh nghiệp`, `Trạng thái xử lý`), việc tạo Option Sets dùng chung giúp dữ liệu luôn đồng nhất và có thể cập nhật hàng loạt từ một nơi duy nhất.

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Mở màn hình Quản lý Option Sets** | Bấm menu tiện ích nâng cao trên thanh công cụ `/database` $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> **Tập hợp tùy chọn** (đường dẫn `/database/option-sets`). |
| **2. Xem danh sách Option Sets hiện có** | Danh sách hiển thị toàn bộ các bộ tùy chọn trong không gian làm việc kèm: Tên bộ tùy chọn, Mô tả, Số lượng giá trị tùy chọn bên trong và số lượng bảng/cột đang liên kết sử dụng (`{N} usages`). |
| **3. Tạo mới một Option Set** | Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm bộ tùy chọn**:<br>• **Tên bộ tùy chọn \***: Nhập tên (ví dụ: `Mức Độ Ưu Tiên`).<br>• **Mô tả**: Nhập ghi chú về ngữ cảnh áp dụng.<br>• **Danh sách giá trị**: Bấm **+ Thêm giá trị** để điền từng mục (ví dụ: `Thấp`, `Trung Bình`, `Cao`, `Khẩn Cấp`). Nhấp vào ô màu bên cạnh để chọn màu sắc trực quan cho từng mục.<br>• Bấm <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Lưu)** để hoàn tất. |
| **4. Áp dụng vào bảng dữ liệu** | Khi vào màn hình tạo hoặc sửa cột kiểu `SELECT` hoặc `MULTI_SELECT` trong bất kỳ bảng nào, chỉ cần bật tùy chọn **Sử dụng Option Set dùng chung** và chọn bộ tùy chọn vừa tạo. Toàn bộ các giá trị và màu sắc sẽ được kế thừa ngay lập tức. |
| **5. Chỉnh sửa tập trung** | Khi cần bổ sung hoặc đổi màu một giá trị, bạn chỉ cần sửa trong `/database/option-sets`. Mọi bảng đang liên kết với bộ tùy chọn này sẽ tự động cập nhật đồng bộ mà không cần sửa thủ công từng bảng. |

---

### Tính năng 3 — Nguồn dữ liệu ngoại bộ (Database Sources)

Hỗ trợ kết nối cơ sở dữ liệu bên ngoài để quản lý tập trung trên một giao diện RedAI duy nhất.

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Mở trang Nguồn dữ liệu** | Bấm menu tiện ích nâng cao $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> **Nguồn dữ liệu ngoại bộ** (`/database/sources`). |
| **2. Thêm nguồn kết nối mới** | Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm nguồn dữ liệu**:<br>• **Tên nguồn \***: Đặt tên gợi nhớ (ví dụ: `PostgreSQL Server Kế Toán`).<br>• **Loại cơ sở dữ liệu**: Chọn hệ quản trị (PostgreSQL, MySQL, REST API Source).<br>• **Thông số kết nối**: Nhập `Host`, `Port`, `Tên Database`, `Tên người dùng` và `Mật khẩu` (toàn bộ thông tin xác thực được mã hóa AES-256 an toàn). |
| **3. Kiểm tra kết nối (Test Connection)** | Bấm nút <img src="https://api.iconify.design/lucide:check-circle.svg?color=%23ff3333" width="16" alt="" /> **Kiểm tra kết nối**. Hệ thống sẽ thực hiện bắt tay thử nghiệm với máy chủ đích và hiển thị thông báo thành công màu xanh kèm độ trễ phản hồi (latency). |
| **4. Đồng bộ Schema & Bảng** | Sau khi kết nối thành công, hệ thống tự động đọc danh mục bảng từ cơ sở dữ liệu ngoại bộ, cho phép bạn chọn những bảng cần ánh xạ vào giao diện RedAI để truy vấn và phân tích dữ liệu. |

---

### Tính năng 4 — Tự động hóa Webhooks & Scheduled Hooks

Tính năng kết nối tự động giúp RedAI chủ động phát tín hiệu HTTP sang các dịch vụ như CRM, ERP, Telegram, Slack hoặc Zalo mỗi khi có sự biến động dữ liệu trong bảng.

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Mở Cài đặt Webhooks của bảng** | Tại màn hình làm việc của bảng dữ liệu, bấm nút <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **(Cài đặt)** ở góc trên bên phải $\rightarrow$ Chọn tab <img src="https://api.iconify.design/lucide:webhook.svg?color=%23ff3333" width="16" alt="" /> **Webhooks & Tự Động Hóa** (`/database/table/:tableId/settings/webhooks`). |
| **2. Tạo Webhook mới** | Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo Webhook mới**:<br>• **Tên Webhook \***: Đặt tên (ví dụ: `Bắn thông báo đơn hàng mới sang CRM`).<br>• **URL Đích (Endpoint) \***: Nhập địa chỉ webhook nhận dữ liệu (ví dụ: `https://api.doanhnghiep.vn/webhook/order`).<br>• **Phương thức HTTP**: Chọn `POST`, `PUT` hoặc `PATCH`.<br>• **Tiêu đề Headers tùy chỉnh**: Thêm các khóa xác thực cần thiết như `Authorization: Bearer <token>` hoặc `x-api-key: <key>`. |
| **3. Chọn sự kiện kích hoạt (Triggers)** | Tích chọn 1 hoặc nhiều sự kiện muốn hệ thống tự động gửi webhook:<br>• <img src="https://api.iconify.design/lucide:plus-circle.svg?color=%23ff3333" width="16" alt="" /> **Khi tạo mới bản ghi (On Create)**.<br>• <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> **Khi cập nhật bản ghi (On Update)**.<br>• <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **Khi xóa bản ghi (On Delete)**. |
| **4. Thiết lập bộ lọc điều kiện kích hoạt** | Mở mục **Điều kiện kích hoạt**: Thêm các quy tắc lọc chỉ bắn webhook khi thỏa mãn điều kiện nhất định (ví dụ: chỉ gửi khi `[Trạng thái]` chuyển thành `"Đã Thanh Toán"` và `[Tổng tiền]` > 1.000.000). |
| **5. Kiểm thử Webhook ngay tại chỗ (Test Hook)** | Bấm nút <img src="https://api.iconify.design/lucide:play.svg?color=%23ff3333" width="16" alt="" /> **(Kiểm thử Webhook)**. Hệ thống sẽ gửi một gói dữ liệu mẫu (Sample Payload) sang máy chủ đích và hiển thị kết quả phản hồi thực tế: mã trạng thái HTTP (ví dụ: `200 OK`), thời gian thực thi tính bằng mili-giây và nội dung phản hồi từ máy chủ. |
| **6. Theo dõi Nhật ký thực thi (Execution Logs)** | Nhấp vào tab <img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" /> **Nhật ký Webhook** để xem toàn bộ lịch sử các lần kích hoạt tự động với bộ lọc theo trạng thái: Thành công, Thất bại, Đang thử lại. |

---

### Tính năng 5 — Phân quyền truy cập và Khóa bảo vệ bảng dữ liệu

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Mở Cài đặt Phân quyền** | Vào **Cài đặt bảng** $\rightarrow$ Chọn tab <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **Phân quyền** (`/database/table/:tableId/settings/permissions`). |
| **2. Cấu hình quyền theo cấp độ Bảng & Bản ghi** | Thiết lập ma trận quyền cho 4 nhóm vai trò (Admin, Editor, Commenter, Viewer):<br>• **Quản lý cấu trúc (Manage Schema)**: Quyền thêm, sửa, xóa các cột dữ liệu.<br>• **Tạo bản ghi (Create Record)**: Quyền thêm dòng mới vào bảng.<br>• **Chỉnh sửa bản ghi (Update Record)**: Quyền sửa đổi nội dung các ô dữ liệu.<br>• **Xóa bản ghi (Delete Record)**: Quyền xóa dòng dữ liệu khỏi bảng. |
| **3. Phân quyền chi tiết theo từng cột (Field-level Permissions)** | Chuyển sang bảng phân quyền cột: Bạn có thể chọn từng cột nhạy cảm (ví dụ: cột `Giá Vốn`, `Mức Lương`, `Số Điện Thoại`) và thiết lập quyền `Chỉ Đọc (Read-only)` hoặc `Ẩn Hoàn Toàn (Hidden)` đối với các vai trò cấp thấp. |
| **4. Khóa cấu hình Dạng xem (Lock View)** | Khi một Dạng xem đã được tối ưu chuẩn xác bộ lọc và quy tắc sắp xếp, người tạo hoặc Quản trị viên có thể bấm vào menu tab View $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:lock.svg?color=%23ff3333" width="16" alt="" /> **Khóa View**. Khi ở trạng thái khóa, các thành viên khác chỉ có thể xem dữ liệu mà không thể vô tình thay đổi điều kiện lọc hay cấu trúc cột của View. |

---

## Kiểm tra kết quả

1. **Trên sơ đồ ERD**: Các đường liên kết giữa các bảng hiển thị chính xác, kéo thả tạo quan hệ thành công và tự động xuất hiện trường liên kết hai chiều trong bảng tính.
2. **Trên Option Sets**: Khi sửa tên hoặc màu sắc của một mục tùy chọn trong `/database/option-sets`, mở bảng tính chứa cột sử dụng Option Set đó thấy nhãn và màu sắc mới đã được áp dụng ngay lập tức.
3. **Trên Webhooks**: Khi thêm hoặc sửa một dòng dữ liệu thỏa mãn điều kiện lọc, chuyển sang tab Nhật ký Webhook thấy xuất hiện dòng ghi nhận mới với mã trạng thái màu xanh `200 OK`.
4. **Trên Phân quyền**: Đăng nhập bằng tài khoản thành viên có vai trò Viewer/Editor để kiểm chứng các nút thêm cột hoặc sửa ô nhạy cảm đã bị vô hiệu hóa hoặc ẩn đi theo đúng ma trận quyền.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể tự động thực hiện các thao tác quản trị đồ thị quan hệ, cấu hình Option Sets, thiết lập Webhooks tự động hóa và phân quyền bảng, bạn cần đảm bảo Agent đã được trang bị Kỹ năng (Skill) sau:

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Workspace Admin hoặc Workspace Owner |

---

### Bảng ánh xạ từng tính năng kèm Prompt mẫu tương ứng cho AI Agent

Dưới đây là bảng ánh xạ chi tiết các công cụ của AI Agent và câu lệnh thực thi cụ thể cho từng tính năng quản trị:

| Nhóm tính năng | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Tính năng 1: Đồ thị quan hệ bảng dữ liệu** | `relation_listRelations`<br>`relation_createRelation`<br>`relation_deleteRelation` | `Hãy kiểm tra các liên kết hiện có của bảng "tbl_orders" và thiết lập quan hệ Một - Nhiều (1:N) liên kết sang bảng "tbl_order_items" với tên trường liên kết ngược là "Danh Sách Mặt Hàng".` |
| **Tính năng 2: Tập hợp tùy chọn dùng chung** | `optionSet_listOptionSets`<br>`optionSet_createOptionSet`<br>`optionSet_updateOptionSet`<br>`optionSet_deleteOptionSet` | `Hãy tạo một bộ tùy chọn dùng chung mới tên "Trạng Thái Giao Hàng" gồm 4 giá trị: "Chờ lấy hàng" (màu vàng), "Đang giao" (màu xanh dương), "Giao thành công" (màu xanh lá) và "Hủy đơn" (màu đỏ).` |
| **Tính năng 3: Nguồn dữ liệu ngoại bộ** | `source_listSources`<br>`source_createSource`<br>`source_testSourceConnection` | `Hãy kiểm tra tình trạng kết nối của nguồn cơ sở dữ liệu "PostgreSQL Kế Toán" (mã source_acc_01) và báo cáo lại độ trễ phản hồi cùng danh sách các bảng có sẵn.` |
| **Tính năng 4: Tự động hóa Webhooks** | `webhook_listWebhooks`<br>`webhook_createWebhook`<br>`webhook_updateWebhook`<br>`webhook_testWebhook`<br>`webhook_getExecutionLogs` | `Hãy tạo một Webhook tự động cho bảng "tbl_orders" gửi tín hiệu POST đến URL "https://crm.example.com/api/v1/new-order" khi có sự kiện On Create, đính kèm Header Authorization Bearer và kiểm thử gửi gói dữ liệu mẫu ngay lập tức.` |
| **Tính năng 5: Phân quyền & Khóa View** | `permission_getTablePermissions`<br>`permission_updateTablePermissions`<br>`view_lockView` | `Hãy cập nhật phân quyền cho bảng "tbl_salaries": thiết lập vai trò "Editor" chỉ có quyền xem và chỉnh sửa dữ liệu, không có quyền quản lý cấu trúc bảng (manageSchema: false) và khóa Dạng xem "Báo Cáo Lương Thưởng".` |

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Tạo quan hệ bảng trên đồ thị ERD hoặc kéo dây liên kết | Gọi `relation_listRelations` thấy xuất hiện cặp liên kết giữa 2 bảng với đúng quan hệ 1-N. |
| Thêm bộ Option Set mới trong `/database/option-sets` | Gọi `optionSet_listOptionSets` thấy bộ tùy chọn mới kèm danh sách các nhãn và mã màu. |
| Tạo Webhook mới và bấm nút Kiểm thử Webhook | Gọi `webhook_getExecutionLogs` thấy bản ghi nhật ký gửi thử nghiệm với mã HTTP 200. |
| Bấm Khóa View trên tab dạng xem | Gọi `view_getViewDetail` thấy trường thuộc tính `isLocked: true`. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `relation_createRelation` | Mở trang `/database/relations`, thấy đường dây liên kết mới tự động vẽ giữa 2 khối bảng. |
| Agent gọi `optionSet_createOptionSet` | Mở trang `/database/option-sets`, xuất hiện thẻ Option Set mới với đầy đủ nhãn màu. |
| Agent gọi `webhook_createWebhook` | Mở Cài đặt bảng $\rightarrow$ Webhooks, Webhook mới xuất hiện trong danh sách và sẵn sàng kích hoạt. |
| Agent gọi `view_lockView` | Trên tab View xuất hiện biểu tượng ổ khóa <img src="https://api.iconify.design/lucide:lock.svg?color=%23ff3333" width="16" alt="" />, các nút chỉnh sửa cấu hình bị làm mờ. |
