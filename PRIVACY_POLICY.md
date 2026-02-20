# Chính Sách Quyền Riêng Tư — Lịch Âm Vạn Niên AI

Hiệu lực: 21/02/2026

TL;DR: Ứng dụng thu một số thông tin cần thiết để cung cấp chức năng (đăng nhập, lưu lịch sử, xử lý mua hàng, AI chat) và sử dụng dịch vụ bên thứ ba (Supabase, Cloudflare Workers, Google Play, dịch vụ AI). Bạn có quyền truy xuất, chỉnh sửa, xóa dữ liệu cá nhân; chúng tôi bảo vệ dữ liệu bằng biện pháp kỹ thuật và quy trình phù hợp.

---

## 1. Phạm vi áp dụng
Chính sách này áp dụng cho người dùng ứng dụng "Lịch Âm Vạn Niên AI" (mobile + web) do nhóm phát triển quản lý.

## 2. Dữ liệu chúng tôi thu
- **Dữ liệu tài khoản:** email, tên (khi bạn đăng ký/đăng nhập qua Supabase).
- **Dữ liệu thiết bị:** ID thiết bị sinh tự động (device_id) để theo dõi giao dịch khách, thông tin nền tảng, phiên bản app. Không thu danh bạ, ảnh, micrô nếu bạn không cấp quyền.
- **Dữ liệu giao dịch:** mua token, SKU, thời gian mua, trạng thái giao dịch, cấp xu (credit), log lỗi liên quan IAP.
- **Dữ liệu sử dụng / telemetry:** hành vi sử dụng, lỗi để cải thiện trải nghiệm.
- **Nội dung hội thoại AI:** nội dung bạn gửi tới dịch vụ AI (ví dụ Gemini) để sinh phản hồi.
- **Dữ liệu lưu cục bộ:** localStorage/IndexedDB dùng để lưu thiết lập, cache, danh sách giao dịch đã xử lý.

## 3. Mục đích sử dụng
- Xác thực & quản lý hồ sơ người dùng.
- Xử lý IAP: xác minh, ghi nhật ký và cấp credits/VIP.
- Cung cấp dịch vụ AI (gửi yêu cầu tới nhà cung cấp AI để trả lời người dùng).
- Phân tích, cải tiến sản phẩm và chẩn đoán sự cố.
- Hỗ trợ và thông báo (nếu bật push notification).

## 4. Chia sẻ dữ liệu
- Chia sẻ với nhà cung cấp dịch vụ cần thiết: Supabase (DB, auth), Cloudflare Workers (API), Google Play (thanh toán), nhà cung cấp AI (Gemini). Chỉ chia sẻ dữ liệu cần thiết cho chức năng tương ứng.
- Tiết lộ theo yêu cầu pháp lý khi cần.
- Không bán dữ liệu người dùng cho bên thứ ba.

## 5. Bảo mật
- Bí mật, keys và JSON service account được lưu trong Cloudflare Secrets; mọi kết nối tới bên thứ ba đều qua HTTPS.
- Hạn chế truy cập nội bộ: chỉ nhân viên vận hành cần thiết mới có quyền truy cập.
- Thực hành quay vòng key định kỳ và không commit file JSON vào repo.

## 6. Thời hạn lưu trữ
- Dữ liệu giao dịch và logs: lưu để phục vụ kiểm toán/hỗ trợ (mặc định: tối thiểu 1 năm, có thể theo quy định pháp luật).
- Dữ liệu tài khoản: giữ đến khi người dùng yêu cầu xóa.
- Dữ liệu telemetry: giữ dạng raw trong thời gian ngắn (ví dụ 90 ngày), tổng hợp/ẩn danh có thể lưu lâu hơn.

## 7. Quyền người dùng
Bạn có quyền:
- **Truy cập:** yêu cầu bản sao dữ liệu cá nhân.
- **Chỉnh sửa:** cập nhật thông tin hồ sơ.
- **Xóa:** yêu cầu xóa tài khoản và dữ liệu liên quan (lưu ý các bản ghi audit có thể được giữ ở dạng ẩn danh nếu bắt buộc).
- **Rút consent / Hạn chế xử lý:** tắt tính năng phân tích hoặc marketing (nếu có).

Để gửi yêu cầu: email đến `support@example.com` (thay bằng email hỗ trợ thực tế) gồm tiêu đề và mô tả.

## 8. Trẻ em
Ứng dụng không dành cho trẻ em dưới 13 tuổi (hoặc theo luật địa phương). Nếu dữ liệu của trẻ em bị thu thập, liên hệ support để xử lý.

## 9. Dịch vụ bên thứ ba
- Supabase: https://supabase.com
- Google Play / Android Publisher API: https://developers.google.com/android-publisher
- Cloudflare Workers: https://workers.cloudflare.com
- Gemini (dịch vụ AI): theo chính sách nhà cung cấp; tránh gửi PII nhạy cảm khi sử dụng AI.

## 10. Thay đổi chính sách
Mọi thay đổi quan trọng sẽ được thông báo qua email hoặc thông báo trong ứng dụng. Phiên bản hiện tại có ngày hiệu lực ở đầu trang.

## 11. Thông tin liên hệ
- Email hỗ trợ: `support@example.com` (thay bằng email thực tế).

---

# Privacy Policy — Lich Am Van Nien AI (English)

Effective date: 21/02/2026

TL;DR: The app collects minimal data required to deliver features (authentication, purchase handling, AI chat) and uses third-party providers (Supabase, Cloudflare Workers, Google Play, AI providers). You can access, correct, and request deletion of personal data. We secure data with appropriate technical and organizational measures.

## Scope
This policy applies to users of the "Lich Am Van Nien AI" mobile and web application.

## Data Collected
- **Account data:** email, display name (via Supabase).
- **Device data:** generated device_id for guest purchases, OS, app version.
- **Purchase data:** purchase token, SKU, timestamps, status, credits, error logs.
- **Usage / telemetry:** feature usage and errors.
- **AI chat content:** user inputs sent to AI provider.
- **Local storage:** settings and processed transaction markers.

## Purpose
- Authentication and user profiles.
- IAP processing and auditing.
- Providing AI responses via third-party AI services.
- Product analytics and debugging.
- Notifications and support.

## Sharing
- Shared only with necessary service providers (Supabase, Cloudflare, Google Play, AI provider).
- Legal disclosures when required.
- No sale of personal data.

## Security
- Secrets stored in Cloudflare Secrets; connections use HTTPS.
- Access limited to necessary personnel.
- Rotate keys periodically; do not store JSON keys in git.

## Retention
- Purchase logs and audit: retained as necessary (default minimum 1 year).
- Account data: retained until account deletion request.
- Telemetry: raw logs short-term (e.g., 90 days); aggregated data may be kept longer.

## User Rights
- Access, correction, deletion (subject to legal/audit retention).
- Opt-out of tracking/analytics where applicable.
- Requests: email `lttrungbk@yahoo.com` with subject and details.

## Children
- Not directed to children under 13 (or per local law). If data of a child is collected, contact support to remove it.

## Third parties
See supplier docs: Supabase, Google Play, Cloudflare, AI provider.

## Contact
lttrungbk@yahoo.com
