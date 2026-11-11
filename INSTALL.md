# Cài đặt

## 1. MausBot

Mỗi thư mục con bên trong `skills/` là một skill độc lập và có `SKILL.md` ở cấp đầu tiên.

- Architect: cài `shared/engineering-workflow`, `shared/project-context`, `shared/evidence-based-reporting`, cùng 3 skill trong `software-architect/`.
- Senior Developer: cài 3 skill shared và 4 skill trong `senior-developer/`.
- UI/UX Specialist: cài 3 skill shared và 3 skill trong `ui-ux-specialist/`.
- QA & Security Reviewer: cài 3 skill shared và 3 skill trong `qa-security-reviewer/`.

Nếu giao diện nhận GitHub URL:
- Đưa thư mục skill lên một GitHub repository public.
- Chọn URL thư mục chứa `SKILL.md`, hoặc URL trực tiếp tới `SKILL.md` nếu ứng dụng hỗ trợ.
- Không dán URL ZIP vào ô cài skill trừ khi ứng dụng ghi rõ hỗ trợ ZIP.

Nếu ứng dụng chỉ nhận một URL tại một thời điểm, thêm từng skill riêng. Đừng giả định import một skill sẽ tự động import các thư mục sibling.

## 2. Codex / các agent hỗ trợ Agent Skills

Đặt thư mục skill vào một vị trí mà agent runtime đang quét. Với công cụ hỗ trợ thư mục global `~/.agents/skills/`, có thể copy các thư mục skill cần dùng vào đó. Kiểm tra tài liệu đúng phiên bản của ứng dụng trước khi chọn đường dẫn; mỗi host có thể có quy ước riêng.

## 3. Antigravity và MuseAI

Không dùng chung một đường dẫn cài đặt nếu chưa xác minh ứng dụng hỗ trợ. Hãy dùng tính năng Skills/Rules/Knowledge tương ứng của từng ứng dụng. Nếu chỉ có ô nhập nội dung, có thể thêm nội dung `SKILL.md` như chỉ dẫn, nhưng điều đó không đồng nghĩa app đã cài script hoặc tool.

## 4. Kiểm tra skill đã được nạp

Sau khi cài, gửi cho bot:

> Hãy liệt kê các Agent Skills đang khả dụng trong phiên này. Với skill `codebase-audit`, hãy nêu tên, mục đích, 5 bước quy trình chính và một checklist đầu ra. Không được suy đoán skill chưa được nạp. Nếu không đọc được nội dung skill, hãy nói rõ.

Tiếp theo, giao một task nhỏ ở chế độ audit-only và yêu cầu bot chỉ ra:
- Skill nào đã áp dụng.
- File hoặc khu vực đã kiểm tra.
- Bằng chứng cụ thể.
- Điều gì chưa thể xác minh.

## 5. Quy tắc an toàn

- Chỉ cấp quyền đọc/ghi đúng repository cần làm.
- Không cấp quyền production mặc định.
- Không cho phép tự ý chạy lệnh phá huỷ dữ liệu.
- Không đưa API secret, token hoặc private key vào prompt.
- Yêu cầu xác nhận trước khi cài dependency, thay đổi schema, migration, deploy, release hoặc thao tác có tác động bên ngoài.
