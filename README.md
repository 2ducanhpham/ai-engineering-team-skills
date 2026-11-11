# AI Engineering Team Skills Pack

Bộ Agent Skills được thiết kế cho team AI đa vai trò: Software Architect, Senior Developer, UI/UX Specialist và QA & Security Reviewer.

## Mục tiêu

- Biến yêu cầu mơ hồ thành kế hoạch có tiêu chí nghiệm thu.
- Khảo sát codebase trước khi thay đổi.
- Chia việc theo vai trò, tránh nhiều agent sửa cùng một vùng code.
- Code có kiểm thử, review độc lập và báo cáo bằng bằng chứng.
- Ưu tiên an toàn: không tự ý deploy, migration, xoá dữ liệu, thay đổi production hoặc lộ secrets.

## Cấu trúc

```text
ai-engineering-team-skills/
├── README.md
├── INSTALL.md
├── TEAM_WORKFLOW.md
├── prompts/
│   ├── team-bootstrap.md
│   ├── task-intake.md
│   └── security-audit-readonly.md
└── skills/
    ├── shared/
    │   ├── engineering-workflow/SKILL.md
    │   ├── project-context/SKILL.md
    │   └── evidence-based-reporting/SKILL.md
    ├── software-architect/
    │   ├── software-architecture/SKILL.md
    │   ├── technical-planning/SKILL.md
    │   └── codebase-audit/SKILL.md
    ├── senior-developer/
    │   ├── implementation/SKILL.md
    │   ├── debugging/SKILL.md
    │   ├── test-driven-development/SKILL.md
    │   └── refactoring/SKILL.md
    ├── ui-ux-specialist/
    │   ├── ui-ux-design/SKILL.md
    │   ├── mobile-ux/SKILL.md
    │   └── accessibility/SKILL.md
    └── qa-security-reviewer/
        ├── code-review/SKILL.md
        ├── testing-strategy/SKILL.md
        └── security-audit/SKILL.md
```

## Thiết kế quan trọng

Skill là hướng dẫn vận hành cho agent, không phải model hay quyền truy cập công cụ. Agent chỉ có thể thực hiện thao tác nếu ứng dụng chủ (MausBot/Codex/Antigravity/MuseAI) cấp công cụ, quyền file và môi trường thực thi tương ứng.

Các skill trong gói là nội dung gốc, được viết để dùng làm nền tảng và cần được điều chỉnh theo stack/quy trình của từng repository. Không có skill nào bảo đảm code luôn đúng; cần chạy test và review thực tế.

## Cách dùng nhanh

1. Giải nén ZIP.
2. Mở `INSTALL.md`.
3. Cài các thư mục skill phù hợp vào từng bot. Nếu nền tảng chỉ nhận một `SKILL.md`, hãy thêm từng skill riêng.
4. Dán `prompts/team-bootstrap.md` vào Group Instructions.
5. Mỗi task phải nêu rõ repository, mục tiêu và phạm vi quyền.
