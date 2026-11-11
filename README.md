# MausBot Curated Skill Stack

Bản phân bổ skill đề xuất cho 4 bot của team:
1. Software Architect
2. Senior Developer
3. UI/UX Specialist
4. QA & Code Reviewer

Đây là gói cấu hình/phân bổ, không phải công cụ tự đăng nhập MausBot để cài đặt. Các skill bên thứ ba cần được import trong giao diện MausBot, sau khi kiểm tra nội dung và quyền.

## Nguyên tắc tuyển chọn
- Chọn theo nhiệm vụ của bot, không chọn chỉ vì install count cao.
- Mỗi bot có 3–4 skill chuyên môn; shared workflow giữ ở Group Instructions.
- Không bật skill đòi hỏi tool chưa có.
- Không để UI/UX tự ý sửa domain logic; QA không tự sửa code khi đang review.
- Không cài skill yêu cầu chạy lệnh ngoài ý muốn, gửi telemetry không rõ ràng hoặc truy cập production.
- Install count là tín hiệu phổ biến, không phải bằng chứng chất lượng/an toàn.

## Ma trận skill
Xem `BOT_SKILL_MATRIX.md`.

## Cài đặt
Xem `MAUSBOT_IMPORT_GUIDE.md`.

## Prompt cấu hình
- `bot-instructions/01-software-architect.md`
- `bot-instructions/02-senior-developer.md`
- `bot-instructions/03-ui-ux-specialist.md`
- `bot-instructions/04-qa-security-reviewer.md`
- `GROUP_INSTRUCTIONS.md`

## Giới hạn đã biết
Skills.sh là directory/CLI ecosystem. `npx skills add` hỗ trợ nhiều coding agents, nhưng không có bằng chứng trong tài liệu đã kiểm tra rằng MausBot được CLI hỗ trợ trực tiếp. Vì vậy gói này hướng dẫn import skill qua Library > Skills của MausBot bằng URL GitHub folder/SKILL.md, rồi xác minh từng bot đã đọc được nội dung.
