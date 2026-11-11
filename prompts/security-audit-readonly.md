# READ-ONLY Mobile App Security Audit

PROJECT:
REPOSITORY:
PLATFORM: iOS / Android / Both
BUILD ARTIFACTS AVAILABLE:
ENVIRONMENT: Local / Staging

## Mission
Đánh giá khả năng trích xuất tài nguyên nhạy cảm, reverse engineering, authentication/authorization, local data protection, network security, logging/telemetry và CI/CD exposure.

## Scope
- APK/IPA packaging, JS bundles/Hermes bytecode, source maps, debug symbols.
- Secrets và configuration: phân biệt public client identifiers với server-side secrets.
- Token lifecycle, storage, refresh, logout, session invalidation.
- API authorization, IDOR/BOLA, privilege escalation, rate limits.
- TLS configuration, certificate validation/pinning nếu có.
- MMKV/AsyncStorage/Keychain/Keystore và dữ liệu nhạy cảm lưu cục bộ.
- Logs, analytics, crash reports và PII exposure.
- CI/CD, signing materials, build artifacts và repository history.

## Safety constraints
- READ-ONLY: không sửa code/config, không rotate key, không thay đổi backend.
- Không tấn công production, không dùng dữ liệu người dùng thật.
- Dynamic testing chỉ trên staging/local có phê duyệt.
- Không in giá trị secret đầy đủ vào báo cáo; chỉ ghi loại, vị trí và fingerprint/đoạn đã che.
- Không kết luận một public key là vulnerability chỉ vì nó xuất hiện trong app; đánh giá quyền và khả năng abuse.

## Required output
Mỗi finding gồm:
- ID, title, severity (Critical/High/Medium/Low/Info)
- Affected component/file/endpoint
- Evidence and reproduction steps
- Impact and realistic attack scenario
- Confidence (High/Medium/Low)
- Recommended remediation
- Whether staging validation is required

Kết luận: PASS / PASS WITH CONDITIONS / FAIL / BLOCKED.
Không tuyên bố an toàn tuyệt đối.
