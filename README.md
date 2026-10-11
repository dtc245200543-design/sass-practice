# Thực hành SASS bằng npm và SASS CLI

Ví dụ này dùng SASS cục bộ trong dự án, vì vậy không cần cài đặt toàn cục hoặc chạy terminal với quyền Administrator.

## Yêu cầu

- Node.js và npm. Kiểm tra bằng `node -v` và `npm -v`.
- Nếu chưa có Node.js, tải bộ cài phù hợp tại [nodejs.org](https://nodejs.org/en/download/). npm được cài cùng Node.js.

## Cài đặt và kiểm tra SASS

Mở terminal tại thư mục dự án và chạy:

```sh
npm install
npm run sass:version
```

Lệnh thứ hai hiển thị phiên bản SASS. Với Dart Sass hiện tại, dùng `sass --version` (hoặc `npx sass --version`); tùy chọn viết tắt `sass -v` không được CLI hỗ trợ. Để cài SASS toàn cục thay vì dùng dependency cục bộ, có thể chạy `npm install -g sass`.

## Biên dịch một tệp

```sh
npm run build:single
```

Lệnh biên dịch `styles.scss` thành `styles.css`. Có thể chạy trực tiếp `npx sass styles.scss styles.css`.

## Theo dõi một tệp

```sh
npm run watch:single
```

Giữ lệnh chạy, sau đó sửa và lưu `styles.scss`; SASS sẽ tự cập nhật `styles.css`. Nhấn `Ctrl+C` để dừng.

## Biên dịch và theo dõi nhiều tệp

```sh
npm run build:all
npm run watch:all
```

Các lệnh này chuyển toàn bộ entry point `.scss` trong `scss/` sang `css/`, giữ cấu trúc thư mục. File bắt đầu bằng dấu gạch dưới như `_variables.scss` là partial dùng chung và không tạo CSS riêng.

## Nếu PowerShell chặn lệnh sass

Không cần đặt execution policy thành `Unrestricted`. Dùng `npm.cmd run build:single`, `npm.cmd run watch:single` hoặc `npm.cmd exec sass -- --version` trong PowerShell.

## Nộp bài

Đưa các file nguồn và hướng dẫn này lên repository GitHub hoặc CodePen của bạn, sau đó dán liên kết vào phần nộp bài.
