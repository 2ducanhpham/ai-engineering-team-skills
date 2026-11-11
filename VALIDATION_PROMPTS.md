# Validation prompts

Chạy từng prompt trực tiếp trong bot tương ứng sau khi import.

## Architect
Bạn đang có những skill nào được nạp? Với `grill-me`, `domain-modeling`, `codebase-design`, `improve-codebase-architecture`, hãy:
1. Xác nhận bạn đọc được nội dung từng skill.
2. Tóm tắt mục đích và quy trình chính của từng skill.
3. Nêu rõ skill nào phụ thuộc skill khác.
4. Nói rõ công cụ nào bạn không có.
Không được suy đoán skill chưa đọc được.

## Senior Developer
Hãy chứng minh bạn đọc được `test-driven-development`, `systematic-debugging`, `executing-plans`.
Đưa ra workflow cho một bug React Native: điều tra nguyên nhân → test tái hiện → fix nhỏ → regression tests → verification.
Chưa được sửa file hoặc chạy lệnh.

## UI/UX Specialist
Hãy chứng minh bạn đọc được `frontend-design`, `web-design-guidelines`, `vercel-react-native-skills`.
Giải thích skill nào dùng cho web, skill nào dùng cho React Native. Đưa ra checklist audit màn hình mobile nhưng chưa sửa code.

## QA & Security Reviewer
Hãy chứng minh bạn đọc được `verification-before-completion`, `requesting-code-review`, `agent-browser`.
Nêu khác biệt giữa skill instructions và browser runtime. Nếu không có agent-browser CLI/browser tool, phải báo BLOCKED cho browser automation; không được giả vờ đã chạy.
