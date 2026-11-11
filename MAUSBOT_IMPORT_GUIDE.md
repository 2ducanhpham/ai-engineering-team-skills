# MausBot Import Guide

## Trước khi bắt đầu
- Mở đúng bot: Library → Skills.
- Import từng skill riêng, không import cả repository nếu không muốn nạp tất cả.
- Dùng URL trang skill hoặc URL GitHub folder chứa `SKILL.md` theo đúng format MausBot chấp nhận.
- Nếu GitHub API rate limit, đợi rồi thử lại; không dùng URL sai hoặc URL có dấu chấm thừa.
- Chưa rõ skill được nạp hay chưa thì không giao task có quyền ghi.

## URLs to import

### Bot 1 — Software Architect
1. https://github.com/mattpocock/skills/tree/main/skills/grill-me
2. https://github.com/mattpocock/skills/tree/main/skills/domain-modeling
3. https://github.com/mattpocock/skills/tree/main/skills/codebase-design
4. https://github.com/mattpocock/skills/tree/main/skills/improve-codebase-architecture

### Bot 2 — Senior Developer
1. https://github.com/obra/superpowers/tree/main/skills/test-driven-development
2. https://github.com/obra/superpowers/tree/main/skills/systematic-debugging
3. https://github.com/obra/superpowers/tree/main/skills/executing-plans

### Bot 3 — UI/UX Specialist
1. https://github.com/anthropics/skills/tree/main/skills/frontend-design
2. https://github.com/vercel-labs/agent-skills/tree/main/skills/web-design-guidelines
3. https://github.com/vercel-labs/agent-skills/tree/main/skills/vercel-react-native-skills

### Bot 4 — QA & Security Reviewer
1. https://github.com/obra/superpowers/tree/main/skills/verification-before-completion
2. https://github.com/obra/superpowers/tree/main/skills/requesting-code-review
3. https://github.com/vercel-labs/agent-browser/tree/main/skills/agent-browser

**Nếu URL folder không được MausBot nhận:** mở trang skill trên skills.sh, copy command/repository được hiển thị; hoặc dùng link trực tiếp `SKILL.md` nếu MausBot hỗ trợ. Không giả định folder path ở trên là được mọi phiên bản MausBot chấp nhận; kiểm tra bằng test import.

## Thứ tự cài
1. Architect: grill-me → domain-modeling → codebase-design → improve-codebase-architecture.
2. Developer: TDD → systematic-debugging → executing-plans.
3. UI/UX: frontend-design → web-design-guidelines → vercel-react-native-skills.
4. QA: verification-before-completion → requesting-code-review → agent-browser.

## Xác minh từng skill
Sau mỗi lần Add:
- Kiểm tra skill xuất hiện trong danh sách của bot.
- Mở skill nếu MausBot cho xem nội dung.
- Gửi prompt kiểm tra tương ứng trong `VALIDATION_PROMPTS.md`.
- Nếu bot không đọc được nội dung hoặc chỉ nhắc tên skill, xem như chưa cài thành công.

## Cảnh báo quyền
- Không bật tự động chạy script hoặc lệnh shell từ skill chưa review.
- Không cấp quyền production, secret store hoặc deploy.
- `agent-browser` yêu cầu CLI/browser runtime riêng; import SKILL.md không cài CLI.
- `improve-codebase-architecture` có thể đề xuất RFC/GitHub issue; không cho tạo issue nếu chưa được yêu cầu.
