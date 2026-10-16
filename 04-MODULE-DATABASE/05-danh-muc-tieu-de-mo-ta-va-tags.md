## Danh mục Tiêu đề, Mô tả và Tags chuẩn hóa — Module Database

Tài liệu này đóng vai trò là danh mục điều hướng trung tâm (Catalog Index) của Phân hệ **04 — Module Database (Bảng dữ liệu động)** trên hệ thống **RedAI**. Bảng tổng hợp siêu dữ liệu dưới đây giúp người dùng, nhà phát triển và đặc biệt là các trợ lý ảo AI Agent nhanh chóng xác định đúng tài liệu nghiệp vụ cần tham chiếu theo từng tình huống cụ thể.

---

## Bảng tổng hợp siêu dữ liệu các tài liệu nghiệp vụ

| Thuộc tính | Chi tiết tài liệu 01 | Chi tiết tài liệu 02 |
| :--- | :--- | :--- |
| **Tên file** | `01-quy-trinh-khoi-tao-bang-du-lieu-va-phan-loai-danh-muc.md` | `02-quy-trinh-cau-hinh-truong-du-lieu-va-kieu-du-lieu.md` |
| **Tiêu đề tài liệu** | Quy trình khởi tạo bảng dữ liệu và phân loại danh mục | Quy trình cấu hình trường dữ liệu và kiểu dữ liệu |
| **Mô tả nghiệp vụ** | Hướng dẫn toàn diện cách tạo bảng dữ liệu mới qua 4 phương án (tạo bảng trống, dùng AI Blueprint kèm xem trước ERD, nhân bản bảng, import Excel/CSV), quản lý danh mục phân loại, vận hành thùng rác lưu trữ 10 ngày và xuất bản bảng thành Tool & MCP cho AI Agent. | Đặc tả chi tiết hơn 30 kiểu dữ liệu trên giao diện (Văn bản, Số, Tiền tệ, Ngày giờ, Select, Checkbox, Relation liên kết bảng, Lookup, Rollup, Formula công thức, Auto Number, Button, AI), cùng các thuộc tính bắt buộc, giá trị mặc định và kiểm tra định dạng. |
| **Agent nên đọc khi** | Cần khởi tạo bảng dữ liệu mới, phân nhóm danh mục, di chuyển bảng giữa các danh mục, khôi phục bảng từ thùng rác hoặc biến bảng thành Tool/MCP Server. | Cần bổ sung cột mới vào bảng, thay đổi kiểu dữ liệu cột, viết công thức tính toán tự động (Formula), cấu hình quan hệ liên kết bảng (Relation) hoặc tổng hợp dữ liệu (Rollup). |
| **Không dùng khi** | Cần chỉnh sửa các dạng xem (Grid, Kanban, Gallery, Calendar, Form) hoặc cấu hình chi tiết kiểu dữ liệu từng cột. | Cần tạo bảng mới, đổi tên bảng, xóa bảng hoặc thiết lập bộ lọc/sắp xếp trên dạng xem. |
| **Thực thể & Quan hệ** | `DatabaseTable`, `TableCategory`, `Workspace`, `CustomTool`, `McpServer`. Bảng thuộc về một Danh mục và Không gian làm việc. | `TableColumn`, `FieldType`, `DatabaseTable`, `RelationLink`, `FormulaExpression`. Mỗi cột thuộc về một Bảng cụ thể. |
| **10 Tags chuẩn hóa** | `database`, `table-create`, `categories`, `import-excel`, `import-csv`, `ai-blueprint`, `duplicate-table`, `trash-recovery`, `custom-tools`, `mcp-server` | `database-fields`, `column-editor`, `field-types`, `relation-field`, `lookup-rollup`, `formula`, `autonumber`, `currency`, `primary-column`, `validation` |

---

| Thuộc tính | Chi tiết tài liệu 03 | Chi tiết tài liệu 04 |
| :--- | :--- | :--- |
| **Tên file** | `03-quy-trinh-thiet-lap-va-tuy-bien-cac-dang-xem-views.md` | `04-quan-ly-do-thi-quan-he-nguon-du-lieu-webhooks-va-phan-quyen.md` |
| **Tiêu đề tài liệu** | Quy trình thiết lập và tùy biến các dạng xem Views | Quản lý đồ thị quan hệ, nguồn dữ liệu, webhooks và phân quyền |
| **Mô tả nghiệp vụ** | Hướng dẫn khởi tạo và vận hành 5 dạng xem cốt lõi (Grid View, Kanban View, Gallery View, Calendar View, Form View), áp dụng bộ công cụ lọc đa điều kiện, sắp xếp, gom nhóm, tô màu dòng tự động và chia sẻ biểu mẫu công khai kèm link rút gọn, mã QR và UTM tracking. | Hướng dẫn các tính năng quản trị cấp cao gồm: sơ đồ thực thể quan hệ tương tác (ReactFlow ERD), quản lý tập hợp tùy chọn dùng chung (Option Sets), kết nối cơ sở dữ liệu ngoại bộ (Sources), tự động hóa Webhooks & Scheduled Hooks và ma trận phân quyền truy cập đa tầng. |
| **Agent nên đọc khi** | Cần chuyển đổi góc nhìn dữ liệu, tạo View mới, thiết lập bộ lọc (Filter), sắp xếp (Sort), gom nhóm (Group by), tô màu dòng, cấu hình biểu mẫu Form công khai hoặc lấy link chia sẻ rút gọn. | Cần quan sát tổng thể kiến trúc ERD giữa các bảng, tạo bộ danh mục dùng chung (Option Sets), tích hợp webhook bắn sự kiện dữ liệu thời gian thực, kiểm tra log webhook hoặc phân quyền bảo mật bảng. |
| **Không dùng khi** | Cần can thiệp cấu trúc cột gốc của bảng hoặc cấu hình Webhook/phân quyền hệ thống. | Cần thao tác nhập liệu ô tính thông thường hoặc thiết kế giao diện Form biểu mẫu thu thập dữ liệu. |
| **Thực thể & Quan hệ** | `TableView`, `ViewType`, `ViewFilter`, `ViewSort`, `ViewGroup`, `RowColorRule`, `SharedLink`. Mỗi View là một cấu hình hiển thị độc lập của Bảng. | `DatabaseRelation`, `OptionSet`, `DataSource`, `TableWebhook`, `WebhookLog`, `TablePermission`. Quản trị liên kết và tự động hóa toàn bảng. |
| **10 Tags chuẩn hóa** | `grid-view`, `kanban-view`, `gallery-view`, `calendar-view`, `form-view`, `view-filters`, `row-color-rules`, `public-form`, `short-links`, `qr-code` | `database-relations`, `erd-diagram`, `option-sets`, `data-sources`, `table-webhooks`, `scheduled-hooks`, `webhook-logs`, `table-permissions`, `field-permissions`, `lock-view` |

---

| Thuộc tính | Chi tiết tài liệu 05 |
| :--- | :--- |
| **Tên file** | `05-danh-muc-tieu-de-mo-ta-va-tags.md` |
| **Tiêu đề tài liệu** | Danh mục Tiêu đề, Mô tả và Tags chuẩn hóa — Module Database |
| **Mô tả nghiệp vụ** | Bảng tổng hợp siêu dữ liệu, bản đồ từ khóa và quy tắc định tuyến thông minh giữa người dùng, hệ thống tài liệu và trợ lý ảo AI Agent cho toàn bộ Phân hệ 04 — Module Database. |
| **Agent nên đọc khi** | Cần định vị nhanh tài liệu phù hợp khi tiếp nhận yêu cầu từ người dùng liên quan đến cơ sở dữ liệu hoặc bảng dữ liệu động. |
| **Không dùng khi** | Đã xác định được chính xác nghiệp vụ cụ thể cần thực hiện trong 4 tài liệu chuyên sâu 01, 02, 03, 04. |
| **Thực thể & Quan hệ** | `DocumentationCatalog`, `ModuleMetadata`, `AIAgentRouting`. |
| **10 Tags chuẩn hóa** | `database-catalog`, `metadata-index`, `agent-routing`, `table-guide`, `schema-guide`, `view-guide`, `relation-guide`, `webhook-guide`, `database-module`, `redai-documentation` |

---

## Bảng định tuyến nhanh theo tình huống thực tế

Dưới đây là bảng tra cứu phản xạ nhanh giúp người dùng và trợ lý ảo AI Agent chọn ngay tài liệu cần thiết:

| Tình huống thực tế phát sinh | Tài liệu cần mở ngay | Công cụ / Đường dẫn trọng tâm |
| :--- | :--- | :--- |
| Muốn tạo bảng dữ liệu mới từ file Excel hoặc nhờ AI gợi ý cấu trúc bảng | `01-quy-trinh-khoi-tao-bang-du-lieu-va-phan-loai-danh-muc.md` | `/database`, `table_createTable`, `import_importData` |
| Cần tạo nhóm danh mục để gom các bảng bán hàng lại gọn gàng | `01-quy-trinh-khoi-tao-bang-du-lieu-va-phan-loai-danh-muc.md` | `category_createCategory`, `table_updateTable` |
| Vô tình xóa nhầm một bảng và muốn lấy lại trong vòng 10 ngày | `01-quy-trinh-khoi-tao-bang-du-lieu-va-phan-loai-danh-muc.md` | Mục Thùng rác, `table_restoreTable` |
| Muốn xuất bản bảng dữ liệu thành API cho AI Agent tự thao tác | `01-quy-trinh-khoi-tao-bang-du-lieu-va-phan-loai-danh-muc.md` | Chuyển hóa thành Tool & MCP, `table_publishAsTool` |
| Muốn thêm cột Tiền tệ, Ngày tháng hoặc Số điện thoại vào bảng | `02-quy-trinh-cau-hinh-truong-du-lieu-va-kieu-du-lieu.md` | `ColumnEditorModal`, `column_createColumn` |
| Cần kết nối bảng Đơn Hàng với bảng Khách Hàng (Relation 1-N) | `02-quy-trinh-cau-hinh-truong-du-lieu-va-kieu-du-lieu.md` | Kiểu dữ liệu Relation, `relation_createRelation` |
| Muốn tính tự động Thành tiền = Số lượng * Đơn giá | `02-quy-trinh-cau-hinh-truong-du-lieu-va-kieu-du-lieu.md` | Kiểu dữ liệu Formula, trình soạn thảo công thức |
| Cần lấy Tổng doanh thu của khách hàng từ bảng Đơn Hàng | `02-quy-trinh-cau-hinh-truong-du-lieu-va-kieu-du-lieu.md` | Kiểu dữ liệu Rollup (hàm SUM) |
| Muốn biến bảng thành quy trình kéo thẻ Kanban theo trạng thái | `03-quy-trinh-thiet-lap-va-tuy-bien-cac-dang-xem-views.md` | `/kanban/:viewId`, `KanbanStackedByMenu` |
| Muốn tạo lịch theo dõi hạn giao hàng theo tuần và tháng | `03-quy-trinh-thiet-lap-va-tuy-bien-cac-dang-xem-views.md` | `/calendar/:viewId`, `CalendarRangeSettings` |
| Cần tạo biểu mẫu gửi khách hàng điền qua mạng xã hội | `03-quy-trinh-thiet-lap-va-tuy-bien-cac-dang-xem-views.md` | `/form/:viewId`, `/s/:code`, `ViewSharedLinksModal` |
| Muốn dòng tự động chuyển màu đỏ khi công việc bị Quá Hạn | `03-quy-trinh-thiet-lap-va-tuy-bien-cac-dang-xem-views.md` | Quy tắc tô màu dòng (Row Color Rules) |
| Muốn xem toàn cảnh sơ đồ quan hệ ERD giữa các bảng trong hệ thống | `04-quan-ly-do-thi-quan-he-nguon-du-lieu-webhooks-va-phan-quyen.md` | `/database/relations` (ReactFlow ERD) |
| Cần tạo một danh sách 63 Tỉnh/Thành phố dùng chung cho 5 bảng | `04-quan-ly-do-thi-quan-he-nguon-du-lieu-webhooks-va-phan-quyen.md` | `/database/option-sets`, `optionSet_createOptionSet` |
| Muốn mỗi khi có đơn hàng mới thì tự động bắn tin nhắn sang Zalo/CRM | `04-quan-ly-do-thi-quan-he-nguon-du-lieu-webhooks-va-phan-quyen.md` | `/settings/webhooks`, `webhook_createWebhook` |
| Cần ẩn cột Giá Vốn đối với nhân viên bán hàng chỉ cho phép Quản lý xem | `04-quan-ly-do-thi-quan-he-nguon-du-lieu-webhooks-va-phan-quyen.md` | `/settings/permissions`, Field-level Permissions |

---

## Danh mục từ khóa tìm kiếm (Keyword Index)

- **Khởi tạo & Nhập liệu**: `tạo bảng`, `bảng trống`, `ask ai blueprint`, `nhân bản bảng`, `duplicate table`, `import excel`, `import csv`, `import json`, `thùng rác`, `khôi phục 10 ngày`, `chuyển hóa tool mcp`.
- **Trường & Cột dữ liệu**: `cột dữ liệu`, `kiểu dữ liệu`, `column editor`, `primary column`, `text`, `number`, `currency`, `percent`, `rating`, `date`, `datetime`, `select`, `multi-select`, `boolean`, `phone`, `email`, `url`, `geo data`, `attachment`, `relation`, `lookup`, `rollup`, `formula`, `autonumber`, `button`, `ai field`.
- **Dạng xem & Trực quan hóa**: `view switcher`, `grid view`, `kanban view`, `gallery view`, `calendar view`, `form view`, `row detail`, `footer summary`, `bộ lọc filter`, `sắp xếp sort`, `gom nhóm group by`, `tô màu dòng row color`, `chiều cao dòng`, `chia sẻ public link`, `short link /s/`, `mã qr`, `utm campaign`.
- **Quản trị nâng cao & Tự động hóa**: `đồ thị quan hệ erd`, `reactflow`, `tập tùy chọn option sets`, `nguồn dữ liệu database sources`, `webhooks`, `scheduled hooks`, `trigger on create/update/delete`, `test webhook`, `webhook logs`, `phân quyền bảng`, `phân quyền cột field-level`, `khóa view lock view`.
