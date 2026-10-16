## Mở khu vực Danh sách Bảng dữ liệu và Phân loại Danh mục

Để bắt đầu quản lý dữ liệu động, khởi tạo bảng mới, phân nhóm danh mục và quản lý vòng đời dữ liệu trên **RedAI Database**, bạn truy cập vào đường dẫn sau trên thanh điều hướng bên trái của hệ thống **RedAI**:

1. **Danh sách Bảng dữ liệu (`/database`)**: Không gian quản trị trung tâm của toàn bộ các bảng dữ liệu (Dynamic Tables) trong Không gian làm việc (Workspace) hiện tại. Màn hình được chia làm 2 khu vực chính:
   - **Thanh bên trái (Bảng phân loại danh mục - Categories Sidebar)**:
     - <img src="https://api.iconify.design/lucide:layout-grid.svg?color=%23ff3333" width="16" alt="" /> **Tất cả bảng**: Xem toàn bộ các bảng dữ liệu đang có trong không gian làm việc.
     - <img src="https://api.iconify.design/lucide:folder.svg?color=%23ff3333" width="16" alt="" /> **Chưa phân loại**: Gom các bảng dữ liệu chưa được gán vào bất kỳ danh mục tùy chỉnh nào.
     - **Danh mục tùy chỉnh (Collection Categories)**: Danh sách các nhóm bảng do người dùng tự định nghĩa (ví dụ: `Bán hàng`, `Nhân sự`, `Kho vận`, `Chăm sóc khách hàng`). Mỗi danh mục đi kèm nút thao tác <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> **(Thao tác)** để đổi tên hoặc xóa nhóm.
     - Nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm danh mục mới**: Khởi tạo một nhóm danh mục mới để tổ chức bảng khoa học.
     - <img src="https://api.iconify.design/lucide:cpu.svg?color=%23ff3333" width="16" alt="" /> **Bảng hệ thống**: Khu vực dành cho các bảng dữ liệu cấu hình lõi của hệ thống RedAI.
     - <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Thùng rác**: Nơi lưu trữ các bảng dữ liệu đã bị xóa tạm thời với cơ chế đếm ngược lưu trữ an toàn trong vòng **10 ngày** trước khi tự động dọn dẹp vĩnh viễn.
   - **Khu vực hiển thị danh sách bảng (Main Content Area)**:
     - **Thanh công cụ phía trên (Toolbar)**:
       - Ô tìm kiếm <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm kiếm bảng dữ liệu...)**.
       - Nút thả xuống <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo Bảng Mới**: Mở menu 4 phương án tạo bảng (Tạo bảng trống, Hỏi AI Dynamic Table Blueprint, Nhân bản bảng, Import dữ liệu).
       - Nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Làm mới)**: Tải lại toàn bộ dữ liệu danh sách bảng.
       - Nút tiện ích mở rộng <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> **(Tiện ích nâng cao)**:
         - <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> **Tập hợp tùy chọn (Option Sets)**: Chuyển sang trang quản lý các bộ giá trị lựa chọn dùng chung (`/database/option-sets`).
         - <img src="https://api.iconify.design/lucide:git-fork.svg?color=%23ff3333" width="16" alt="" /> **Đồ thị quan hệ (Relations ERD)**: Chuyển sang trang sơ đồ trực quan quan hệ giữa các bảng (`/database/relations`).
         - <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> **Nguồn dữ liệu ngoại bộ (Sources)**: Quản lý các kết nối cơ sở dữ liệu bên ngoài (`/database/sources`).
         - <img src="https://api.iconify.design/lucide:hard-drive.svg?color=%23ff3333" width="16" alt="" /> **Dung lượng lưu trữ (Storage Usage)**: Mở hộp thoại kiểm tra số lượng bản ghi, dung lượng tệp đính kèm và tổng dung lượng bảng.
         - <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **Trung tâm tiện ích (Utilities Center)**: Mở bộ công cụ quét bản ghi trùng lặp, tạo dữ liệu giả lập (Mock Data), in nhãn QR Code và trích xuất dữ liệu tự động.
2. **Thao tác trên từng thẻ bảng dữ liệu**: Mỗi bảng hiển thị tên bảng, mô tả, số lượng bản ghi, số lượng trường và menu chức năng <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" />:
   - <img src="https://api.iconify.design/lucide:edit-2.svg?color=%23ff3333" width="16" alt="" /> **Đổi tên & Mô tả bảng**: Cập nhật thông tin nhận diện bảng.
   - <img src="https://api.iconify.design/lucide:folder-input.svg?color=%23ff3333" width="16" alt="" /> **Di chuyển danh mục**: Đổi nhóm danh mục quản lý cho bảng.
   - <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **Nhân bản bảng**: Sao chép cấu trúc hoặc dữ liệu bảng sang bảng mới.
   - <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **Tải tài liệu API (OpenAPI JSON)**: Tải tệp đặc tả kỹ thuật REST API của riêng bảng này.
   - <img src="https://api.iconify.design/lucide:folder-sync.svg?color=%23ff3333" width="16" alt="" /> **Chuyển hóa thành Tool & MCP**: Xuất bản tự động toàn bộ API CRUD của bảng thành bộ công cụ tùy chỉnh (Custom Tools) và máy chủ MCP để AI Agent gọi trực tiếp.
   - <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Xóa bảng (Chuyển vào thùng rác)**: Đưa bảng vào danh sách lưu trữ tạm thời trong 10 ngày.

---

## Các bước thực hiện

### Chọn phương án khởi tạo bảng dữ liệu phù hợp

| Phương án khởi tạo | Khi nào nên sử dụng | Kết quả nhận được |
| :--- | :--- | :--- |
| **Phương án 1 — Tạo bảng trống** | Khi bạn đã có sẵn thiết kế cấu trúc trường hoặc muốn tự tay thêm từng cột theo quy chuẩn riêng. | Một bảng mới được khởi tạo ngay với cột định danh mặc định, sẵn sàng để cấu hình trường. |
| **Phương án 2 — Hỏi AI Dynamic Table Blueprint** | Khi bạn có ý tưởng nghiệp vụ nhưng chưa rõ cần những trường dữ liệu nào, quan hệ ra sao. | Trợ lý AI tự động gợi ý toàn bộ cấu trúc bảng, các cột phù hợp và hiển thị sơ đồ quan hệ ERD trực quan để bạn duyệt trước khi tạo. |
| **Phương án 3 — Nhân bản bảng dữ liệu** | Khi bạn muốn tạo bảng mới có cấu trúc tương tự bảng hiện có, hoặc cần bản sao lưu dữ liệu để thử nghiệm. | Tạo ra một bảng mới kế thừa toàn bộ danh sách trường dữ liệu, có tùy chọn sao chép cả dữ liệu bản ghi và bộ lọc. |
| **Phương án 4 — Import từ tệp dữ liệu ngoại bộ** | Khi bạn đã có sẵn dữ liệu từ file Excel (`.xlsx`), file văn bản (`.csv`) hoặc tệp cấu trúc (`.json`). | Tự động đọc tiêu đề cột, suy đoán kiểu dữ liệu thông minh và nhập hàng loạt bản ghi vào bảng mới. |

---

### Giai đoạn 1 — Khởi tạo bảng dữ liệu mới

#### Phương án 1 — Tạo bảng trống

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở menu Tạo Bảng Mới** | Tại màn hình **Danh sách Bảng** (`/database`), bấm vào nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo Bảng Mới** trên thanh công cụ và chọn **Tạo bảng trống**. |
| **2. Nhập thông tin bảng** | Trong hộp thoại khởi tạo:<br>• **Tên bảng \***: Nhập tên bảng dữ liệu (ví dụ: `Khách Hàng Tiềm Năng`, `Đơn Đặt Hàng`).<br>• **Mô tả**: Nhập mục đích sử dụng và ý nghĩa nghiệp vụ của bảng.<br>• **Danh mục**: Chọn nhóm danh mục muốn phân loại (hoặc để mặc định `Chưa phân loại`). |
| **3. Chọn loại View mặc định** | Chọn kiểu hiển thị đầu tiên cho bảng (mặc định là <img src="https://api.iconify.design/lucide:table.svg?color=%23ff3333" width="16" alt="" /> **Grid View**). Bạn có thể đặt lại **Tên View** ban đầu. |
| **4. Xác nhận tạo** | Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo bảng)**. Hệ thống sẽ mở ngay không gian làm việc của bảng mới tạo. |

#### Phương án 2 — Hỏi AI Dynamic Table Blueprint (Kèm xem trước sơ đồ ERD)

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở công cụ Tạo bảng bằng AI** | Bấm vào nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo Bảng Mới** và chọn dòng <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **Hỏi AI Dynamic Table Blueprint**. |
| **2. Nhập mô tả nghiệp vụ mong muốn** | Nhập yêu cầu nghiệp vụ vào khung thoại (ví dụ: `Hãy thiết kế bảng Quản lý Hợp đồng Bán lẻ gồm mã hợp đồng, khách hàng liên kết, ngày ký, tổng giá trị, trạng thái thanh toán và tệp đính kèm scan`). |
| **3. Phân tích và xem trước sơ đồ ERD** | Bấm nút <img src="https://api.iconify.design/lucide:send.svg?color=%23ff3333" width="16" alt="" /> **(Phân tích)**. AI sẽ tạo ra bản thiết kế chi tiết bao gồm:<br>• Danh sách các cột đề xuất kèm kiểu dữ liệu tương ứng (Text, Currency, Date, Attachment, Select...).<br>• Khung xem trước sơ đồ quan hệ <img src="https://api.iconify.design/lucide:git-fork.svg?color=%23ff3333" width="16" alt="" /> **AiBlueprintErdPreview** trực quan mô phỏng liên kết với các bảng hiện có. |
| **4. Điều chỉnh và áp dụng** | Bạn có thể chọn bỏ bớt hoặc thêm các cột theo ý muốn, sau đó bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Khởi tạo theo Blueprint)** để hoàn tất. |

#### Phương án 3 — Nhân bản bảng dữ liệu (Duplicate Table)

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở menu nhân bản** | Trên thẻ bảng muốn nhân bản (hoặc trong menu thả xuống Tạo Bảng Mới), chọn <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **Nhân bản bảng**. |
| **2. Cấu hình thông số nhân bản** | Trong hộp thoại nhân bản:<br>• **Tên bảng mới \***: Nhập tên cho bảng nhân bản (mặc định thêm tiền tố `Bản sao của...`).<br>• **Sao chép dữ liệu bản ghi**: Bật nút gạt nếu muốn giữ lại toàn bộ dữ liệu hiện có (nếu tắt, chỉ nhân bản bộ khung cấu trúc cột).<br>• **Sao chép bộ lọc & Dạng xem (Views)**: Bật nút gạt để kế thừa toàn bộ các View Grid, Kanban, Gallery, Calendar đã thiết lập. |
| **3. Hoàn tất nhân bản** | Bấm nút <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Bắt đầu nhân bản)**. |

#### Phương án 4 — Import từ tệp dữ liệu ngoại bộ (CSV / Excel / JSON)

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở hộp thoại Import** | Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo Bảng Mới** $\rightarrow$ chọn <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> **Import dữ liệu**. |
| **2. Tải lên tệp nguồn** | Kéo thả tệp dữ liệu vào khung tải lên (hỗ trợ định dạng `.csv`, `.xlsx`, `.json` với dung lượng tối đa 20MB). |
| **3. Xem trước và ánh xạ kiểu dữ liệu cột** | Hệ thống tự động trích xuất các cột từ dòng tiêu đề đầu tiên. Tại bảng ánh xạ:<br>• Kiểm tra **Tên cột**.<br>• Chọn lại **Kiểu dữ liệu** phù hợp nếu hệ thống nhận diện chưa đúng ý (ví dụ: chuyển đổi giữa Text, Number, Date, Phone, Email).<br>• Tích chọn cột làm **Khóa chính đại diện (Display Column)**. |
| **4. Thực thi nhập dữ liệu** | Bấm nút <img src="https://api.iconify.design/lucide:arrow-right.svg?color=%23ff3333" width="16" alt="" /> **(Bắt đầu Import)**. Tiến trình sẽ hiển thị thanh phần trăm và tự động điều hướng sang bảng mới sau khi nhập dữ liệu thành công. |

---

### Giai đoạn 2 — Quản lý phân loại danh mục (Categories)

Để nhóm các bảng dữ liệu theo từng phòng ban, dự án hoặc quy trình:

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Tạo danh mục mới** | Tại thanh bên trái của màn hình Danh sách Bảng, bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm danh mục mới** $\rightarrow$ Nhập tên nhóm (ví dụ: `Kinh Doanh`) $\rightarrow$ Bấm nút lưu. |
| **2. Gán bảng vào danh mục** | Bấm vào menu <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> trên thẻ bảng $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:folder-input.svg?color=%23ff3333" width="16" alt="" /> **Di chuyển danh mục** $\rightarrow$ Chọn danh mục đích từ danh sách thả xuống $\rightarrow$ Bấm **Xác nhận**. |
| **3. Sửa hoặc xóa danh mục** | Rê chuột vào tên danh mục trên thanh bên trái $\rightarrow$ Bấm biểu tượng <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" />:<br>• **Đổi tên danh mục**: Sửa lại tên hiển thị.<br>• **Xóa danh mục**: Xóa nhóm phân loại (lưu ý: các bảng thuộc nhóm này sẽ tự động chuyển về trạng thái <img src="https://api.iconify.design/lucide:folder.svg?color=%23ff3333" width="16" alt="" /> **Chưa phân loại**, dữ liệu bên trong bảng không bị ảnh hưởng). |

---

### Giai đoạn 3 — Vận hành Thùng rác và Khôi phục dữ liệu

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Xóa tạm thời bảng dữ liệu** | Trên thẻ bảng cần xóa, bấm biểu tượng <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Xóa bảng**. Bảng sẽ biến mất khỏi danh sách hoạt động và được đưa vào Thùng rác. |
| **2. Truy cập Thùng rác** | Tại thanh bên trái, nhấp vào mục <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Thùng rác**. Tại đây hiển thị danh sách các bảng bị xóa kèm thông tin:<br>• Tên bảng gốc.<br>• Thời gian xóa.<br>• **Hạn lưu trữ còn lại**: Đếm ngược số ngày còn lại (trong tổng hạn định 10 ngày). |
| **3. Khôi phục hoặc xóa vĩnh viễn** | Tại mỗi dòng bảng trong Thùng rác:<br>• Bấm nút <img src="https://api.iconify.design/lucide:rotate-ccw.svg?color=%23ff3333" width="16" alt="" /> **(Khôi phục)**: Đưa bảng trở lại danh mục ban đầu với đầy đủ cấu hình cột và dữ liệu nguyên vẹn.<br>• Bấm nút <img src="https://api.iconify.design/lucide:x-circle.svg?color=%23ff3333" width="16" alt="" /> **(Xóa vĩnh viễn)**: Hủy bỏ hoàn toàn bảng dữ liệu khỏi hệ thống ngay lập tức (không thể phục hồi). |

---

### Giai đoạn 4 — Xuất bản bảng thành Tool & MCP cho AI Agent

Tính năng độc quyền của RedAI cho phép biến bất kỳ bảng dữ liệu động nào thành một bộ công cụ lập trình để AI Agent tự động đọc/ghi:

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở menu chuyển hóa** | Trên thẻ bảng dữ liệu, bấm vào biểu tượng <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:folder-sync.svg?color=%23ff3333" width="16" alt="" /> **Chuyển hóa thành Tool & MCP**. |
| **2. Cấu hình đặc tả xuất bản** | Trong hộp thoại xuất bản:<br>• **Tên nhóm Project Schema**: Đặt tên đại diện cho nhóm công cụ (mặc định lấy theo tên bảng).<br>• **Các quyền thao tác cấp phép**: Tích chọn các API muốn sinh ra gồm: `Xem danh sách bản ghi (List/Query)`, `Xem chi tiết bản ghi (Get)`, `Thêm bản ghi mới (Create)`, `Cập nhật bản ghi (Update)`, `Xóa bản ghi (Delete)`.<br>• **Đăng ký MCP Server**: Bật tùy chọn nếu muốn tự động đăng ký endpoint này vào hệ thống máy chủ MCP của Không gian làm việc. |
| **3. Hoàn tất xuất bản** | Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Xác nhận xuất bản)**. Sau khi hoàn tất, AI Agent có thể gọi trực tiếp các công cụ này trong hội thoại mà không cần lập trình thủ công. |

---

## Kiểm tra kết quả

Sau khi hoàn tất quy trình khởi tạo và tổ chức danh mục, bạn kiểm tra lại theo các tiêu chí:

1. **Hiển thị trên Danh sách Bảng**: Tên bảng mới xuất hiện đúng vị trí trong danh mục đã gán, hiển thị đúng số lượng cột ban đầu và trạng thái hoạt động.
2. **Cấu trúc trường và View**: Mở bảng dữ liệu, thanh tiêu đề hiển thị đúng tên bảng và Tab View mặc định đầu tiên hoạt động ổn định.
3. **Thùng rác**: Khi thực hiện xóa thử một bảng, bảng lập tức chuyển vào mục Thùng rác kèm thời gian đếm ngược chính xác, và khi bấm Khôi phục bảng trở lại nguyên vẹn vị trí cũ.
4. **Tool & MCP**: Nếu có xuất bản công cụ, kiểm tra trong mô-đun Tích hợp hoặc màn hình Quản lý Custom Tools thấy xuất hiện nhóm API tương ứng với bảng.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể tự động thực hiện các thao tác khởi tạo bảng, cấu hình danh mục và quản lý dữ liệu, bạn cần đảm bảo Agent đã được trang bị Kỹ năng (Skill) sau:

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
| Bấm **Tạo Bảng Mới** $\rightarrow$ Tạo bảng trống | `table_createTable` | Khởi tạo bảng dữ liệu mới trong workspace (`name`, `description`, `categoryId`, `viewType`). |
| Xem danh sách bảng trên màn hình `/database` | `table_listTables` | Lấy danh sách toàn bộ các bảng trong workspace (`workspaceId`, `categoryId`, `includeSystem`). |
| Nhấp đúp đổi tên bảng hoặc cập nhật mô tả | `table_updateTable` | Chỉnh sửa thuộc tính bảng (`tableId`, `name`, `description`, `categoryId`). |
| Chuyển bảng vào **Thùng rác** | `table_deleteTable` | Xóa mềm bảng dữ liệu, đưa vào vùng lưu trữ 10 ngày (`tableId`). |
| Bấm **Khôi phục** bảng trong Thùng rác | `table_restoreTable` | Phục hồi bảng dữ liệu từ thùng rác về danh mục hoạt động (`tableId`). |
| Bấm **Thêm danh mục mới** trên thanh bên | `category_createCategory` | Tạo nhóm danh mục phân loại mới (`name`, `description`, `order`). |
| Đổi tên hoặc sắp xếp nhóm danh mục | `category_updateCategory` | Cập nhật tên và thứ tự hiển thị danh mục (`categoryId`, `name`, `order`). |
| Bấm **Xóa danh mục** | `category_deleteCategory` | Xóa nhóm danh mục (`categoryId`, `reassignToUncategorized: true`). |
| Bấm **Import dữ liệu** từ file CSV/Excel | `import_importData` | Nhập dữ liệu tự động theo lô vào bảng (`tableId`, `fileUrl`, `mappings`). |
| Bấm **Chuyển hóa thành Tool & MCP** | `table_publishAsTool` | Đăng ký tự động API CRUD của bảng thành Custom Tools và MCP Server (`tableId`, `operations`). |

---

### Khung lệnh (Prompt) mẫu chuẩn 4 phần cho AI Agent

Dưới đây là mẫu câu lệnh hoàn chỉnh để ra lệnh cho AI Agent tự động khởi tạo danh mục và bảng dữ liệu nghiệp vụ:

```text
[MỤC TIÊU]
Khởi tạo một danh mục bảng mới có tên "Quản Trị Bán Hàng" và tạo bên trong một bảng dữ liệu động mới mang tên "Khách Hàng Doanh Nghiệp" trên RedAI Database.

[DỮ LIỆU ĐẦU VÀO]
- Tên danh mục mới: "Quản Trị Bán Hàng"
- Tên bảng dữ liệu: "Khách Hàng Doanh Nghiệp"
- Mô tả bảng: "Bảng lưu trữ thông tin đối tác B2B, người liên hệ đại diện, mã số thuế và doanh thu ước tính."
- Cấu hình View mặc định: Dạng Grid View với tên "Tất cả khách hàng B2B".

[QUY TRÌNH THỰC THI]
1. Gọi tool `category_createCategory` để tạo danh mục "Quản Trị Bán Hàng" và lưu lại `categoryId` vừa tạo.
2. Gọi tool `table_createTable` với tham số `name: "Khách Hàng Doanh Nghiệp"`, `categoryId` tương ứng và đặt view mặc định là GRID.
3. Kiểm tra thông tin phản hồi để xác nhận `tableId` và `viewId` đã được cấp phát thành công.

[TIÊU CHÍ HOÀN THÀNH]
- Danh mục "Quản Trị Bán Hàng" xuất hiện trên thanh bên trái danh sách bảng.
- Bảng "Khách Hàng Doanh Nghiệp" được khởi tạo thành công bên trong danh mục đó.
- Trả về mã định danh `tableId` và đường dẫn truy cập trực tiếp trên giao diện để người dùng vào sử dụng ngay.
```

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Tạo bảng mới hoặc đổi tên bảng trên giao diện | Gọi `table_listTables` thấy xuất hiện bảng mới với đúng tên và mô tả đã đặt. |
| Thêm danh mục mới và chuyển bảng vào danh mục | Gọi `category_listCategories` và `table_getTableDetail` thấy `categoryId` trùng khớp. |
| Bấm xóa bảng đưa vào thùng rác | Gọi `table_listTables` không còn thấy bảng ở trạng thái hoạt động; gọi `trash_listDeletedTables` thấy bảng kèm hạn 10 ngày. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `table_createTable` tạo bảng mới | Tải lại trang `/database`, thẻ bảng mới lập tức xuất hiện trong danh mục tương ứng. |
| Agent gọi `category_createCategory` tạo danh mục | Thanh bên trái xuất hiện thêm tên nhóm danh mục mới trong danh sách. |
| Agent gọi `table_restoreTable` phục hồi bảng | Truy cập `/database`, bảng được phục hồi hoàn chỉnh dữ liệu và không còn nằm trong mục Thùng rác. |
