# [Thực Hành] Hướng dẫn cài đặt SASS bằng npm & SASS CLI

Bài thực hành kiểm tra môi trường Node.js/npm, cài đặt và sử dụng Dart Sass CLI để biên dịch mã nguồn SCSS sang CSS theo giáo trình CodeGym.

---

## 1. Kiểm tra môi trường Node.js & npm
Kiểm tra phiên bản Node.js:
```bash
node -v
# Kết quả: v26.7.0
```

Kiểm tra phiên bản npm:
```bash
npm -v
# Kết quả: 11.19.0
```

---

## 2. Cài đặt SASS CLI
Cài đặt SASS ở chế độ toàn cục (global):
```bash
npm install -g sass
```
Hoặc sử dụng thông qua `npx`:
```bash
npx sass --version
# Kết quả: 1.105.1 compiled with dart2js
```

---

## 3. Chuyển đổi tệp SCSS sang CSS bằng SASS CLI
Biên dịch file đơn lẻ:
```bash
sass styles.scss styles.css
```

---

## 4. Kích hoạt chế độ theo dõi (Watch Mode)
Tự động biên dịch khi có bất kỳ thay đổi nào trong file SCSS:
```bash
sass styles.scss styles.css --watch
```

---

## 5. Biên dịch nhiều tệp SCSS cùng lúc qua thư mục
Chuyển đổi toàn bộ thư mục `scss/` sang thư mục đầu ra `css/`:
```bash
sass scss/:css/
```
Chế độ watch cho toàn bộ thư mục:
```bash
sass scss/:css/ --watch
```

---

## 6. Cấu trúc thư mục dự án
```
thuc-hanh-cai-dat-sass-npm-cli/
├── index.html        # Trang giao diện HTML áp dụng CSS đã biên dịch
├── styles.scss       # File SCSS chính
├── styles.css        # File CSS được SASS biên dịch tự động
├── styles.css.map    # Source map hỗ trợ debug
├── package.json      # npm scripts điều khiển SASS
├── README.md         # Hướng dẫn chi tiết
├── scss/             # Thư mục mã nguồn SCSS
│   ├── _variables.scss
│   ├── _mixins.scss
│   └── main.scss
└── css/              # Thư mục CSS sau khi biên dịch từ scss/
    ├── main.css
    └── main.css.map
```
