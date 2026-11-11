# Bot Skill Matrix

## 1. Software Architect — 4 chuyên môn
| Skill | Nguồn | Dùng khi |
|---|---|---|
| grill-me | `mattpocock/skills` | Làm rõ yêu cầu, chất vấn giả định, stress-test kiến trúc trước khi code |
| domain-modeling | `mattpocock/skills` | Làm rõ thuật ngữ/domain, edge cases, glossary và quyết định nghiệp vụ |
| codebase-design | `mattpocock/skills` | Dùng chung vocabulary để phân tích module/interface/seam/depth |
| improve-codebase-architecture | `mattpocock/skills` | Audit điểm nghẽn kiến trúc, đề xuất deep-module refactor và testability |

**Lưu ý:** `improve-codebase-architecture` tham chiếu `codebase-design`; cài cả hai. Skill này có Snyk Warn trên listing tại thời điểm nghiên cứu, nên review SKILL.md và scripts trước khi import; không cho phép tự tạo GitHub issues hoặc thay đổi repo nếu chưa được duyệt.

## 2. Senior Developer — 3 chuyên môn
| Skill | Nguồn | Dùng khi |
|---|---|---|
| test-driven-development | `obra/superpowers` | Feature/bug/refactor có thay đổi hành vi; viết test trước và quan sát test fail |
| systematic-debugging | `obra/superpowers` | Bug khó; điều tra nguyên nhân gốc trước khi sửa |
| executing-plans | `obra/superpowers` | Thực thi plan đã được duyệt theo từng task/checkpoint |

Không bật `using-superpowers` mặc định nếu nó xung đột với quy tắc approval/handoff của team. Không ép TDD cho thay đổi chỉ tài liệu hoặc thay đổi không có hành vi chạy được.

## 3. UI/UX Specialist — 3 chuyên môn
| Skill | Nguồn | Dùng khi |
|---|---|---|
| frontend-design | `anthropics/skills` | Định hướng thẩm mỹ, typography, composition, visual identity; tránh UI rập khuôn |
| web-design-guidelines | `vercel-labs/agent-skills` | Audit web UI về hierarchy, responsive, accessibility và interaction |
| vercel-react-native-skills | `vercel-labs/agent-skills` | React Native performance, navigation, lists, animations, safe areas, platform patterns |

**Lưu ý:** `web-design-guidelines` dành cho web UI; không dùng máy móc để đánh giá native mobile. `vercel-react-native-skills` có một số gợi ý thiên Expo/stack nhất định; phải đối chiếu RN hiện tại trước khi áp dụng, không thay thư viện chỉ vì skill đề xuất.

## 4. QA & Security Reviewer — 3 chuyên môn
| Skill | Nguồn | Dùng khi |
|---|---|---|
| verification-before-completion | `obra/superpowers` | Xác nhận test/build/fix bằng output mới, không tuyên bố pass nếu chưa chạy |
| requesting-code-review | `obra/superpowers` | Tạo review độc lập với phạm vi/diff/acceptance criteria rõ ràng |
| agent-browser | `vercel-labs/agent-browser` | Browser E2E/exploratory cho web khi CLI/browser tool đã được cài và cho phép |

**Lưu ý:** `agent-browser` không tự tạo quyền browser cho MausBot. Skill page là discovery stub, hướng dẫn cần tải từ CLI `agent-browser skills get core`; chỉ cài nếu môi trường hỗ trợ CLI. QA vẫn giữ skill `security-audit` riêng trong gói nền; không thay thế audit chuyên biệt bằng browser automation.

## Shared skills
Giữ nguyên shared skills trong ZIP nền:
- engineering-workflow
- project-context
- evidence-based-reporting

Không cần import lại shared skill vào từng bot nếu Group Instructions của MausBot đã áp dụng được chung; nếu mỗi bot có Library riêng, import từng shared skill vào mỗi bot.
