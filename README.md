local_passport_auth_service
# Local Passport Auth Service

Dự án này sử dụng **Passport.js (Local Strategy)** để xác thực người dùng trong Node.js. Bao gồm các chức năng đăng ký, đăng nhập, truy cập profile và đăng xuất.

---

## Cách chạy
```bash
cd local_passport_auth_service
npm install
node app.js   # hoặc node server.js (tuỳ file chính)


Server chạy tại http://localhost:3000

Test bằng Postman
1. Register

Method: POST

URL: http://localhost:3000/register

Body (x-www-form-urlencoded hoặc JSON):

username: admin

password: 12345

2. Login

Method: POST

URL: http://localhost:3000/login

Body (x-www-form-urlencoded hoặc JSON):

username: admin

password: 12345

Server trả về session hoặc token (tùy cấu hình).

3. Profile

Method: GET

URL: http://localhost:3000/profile

Headers / Cookies: gửi kèm session sau khi login

4. Logout

Method: GET

URL: http://localhost:3000/logout

Sau khi logout, truy cập /profile sẽ bị chặn.

5. Database

Mở MongoDB Compass

Database: passportAuth (tuỳ config)

Collection: users

Kiểm tra user admin đã được lưu (password hash).