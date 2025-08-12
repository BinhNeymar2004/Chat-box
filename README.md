ỨNG DỤNG CHAT BOT

1. Giới thiệu
Bài làm tập trung vào việc phát triển một ứng dụng chatbot thông minh, sử dụng API Gemini từ Google AI Studio. Mục tiêu là tạo ra một giao diện web cho phép người dùng nhập câu hỏi hoặc tin nhắn và nhận phản hồi tự động từ mô hình ngôn ngữ Gemini. Ứng dụng này được thiết kế để hỗ trợ giao tiếp cơ bản, cung cấp thông tin và thử nghiệm khả năng của mô hình AI trong xử lý ngôn ngữ tự nhiên. Dự án được thực hiện vào ngày 12/08/2025, hướng đến tính đơn giản và hiệu quả trong trải nghiệm người dùng.
Sử dụng công nghệ, thuật toán, ngôn ngữ lập trình gì
Ngôn ngữ lập trình:
HTML, JavaScript (sử dụng React qua CDN) để xây dựng giao diện và logic client-side.
2. Công nghệ
- React: Quản lý trạng thái giao diện (tin nhắn, input, loading) và render động.
- Tailwind CSS: Cung cấp styling linh hoạt, đáp ứng trên nhiều thiết bị với giao diện hiện đại.
- Fetch API: Sử dụng để gọi API Gemini từ client-side.
3. Thuật toán và mô hình:
- Sử dụng mô hình ngôn ngữ Gemini (cụ thể là gemini-1.5-flash) từ Google, dựa trên các thuật toán transformer để xử lý ngôn ngữ tự nhiên.
- Không triển khai thuật toán tự tạo mà tận dụng API có sẵn để sinh văn bản.
4. Môi trường:
- Chạy trực tiếp trên trình duyệt, không yêu cầu server phức tạp (có thể dùng python -m http.server để test local).
Một số giao diện cơ bản
5. Giao diện chính:
<img width="1859" height="907" alt="image" src="https://github.com/user-attachments/assets/3031a356-0127-455e-a571-543c81e26f95" />

Tiêu đề: "Gemini Chatbot" hiển thị ở đầu trang, sử dụng font lớn và màu xám đậm.
Khu vực chat: Một vùng cuộn tự động (height 96px) với tin nhắn người dùng (màu xanh, nằm bên phải) và tin nhắn bot (màu xám, nằm bên trái), mỗi tin nhắn có bo góc và giới hạn chiều rộng tối đa.
Ô nhập liệu: Một ô input linh hoạt (flex-1) với placeholder "Nhập tin nhắn..." và nút "Gửi" màu xanh lá, chuyển sang xanh đậm khi hover.
Trạng thái loading: Nút "Gửi" thay đổi thành "Đang xử lý..." khi API được gọi.
