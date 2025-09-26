22658171 - Đặng Hoài Bảo

Đầu tiên mở terminal cd thư mục cookie_session_auth cài: npm install

B1: Chạy câu lệnh node app.js 

B2: MỞ POSTMAN
 - Chạy URL: POST http://localhost:3000/auth/register 
 kèm Body: raw JSON{"username": "hoaibao","password": "12345"} khi send thành công sẽ gửi trả về message "User registered successfully!"
<img width="1919" height="1079" alt="image" src="../cookie_session_auth/public/image/register_1.png" />
<img width="1919" height="1079" alt="image" src="../cookie_session_auth/public/image/register_2.png" />
 
 - Chạy URL: POST http://localhost:3000/auth/login
kèm Body: raw JSON{"username": "hoaibao","password": "12345"} khi send thành công sẽ gửi trả về message "Login successful!"
và tạo ra 1 session_cookie connect.sid và trên MongoDB sẽ tạo ra 1 session 
<img width="1919" height="1079" alt="image" src="../cookie_session_auth/public/image/login_1.png" />
<img width="1919" height="1079" alt="image" src="../cookie_session_auth/public/image/login_2.png" />
<img width="1916" height="1075" alt="image" src="../cookie_session_auth/public/image/login_3.png" />
 
 - Chạy URL: GET http://localhost:3000/auth/profile khi send thành công sẽ gửi trả về thông tin {"_id","username","__v"} thông tin cookie
<img width="1919" height="1079" alt="image" src="../cookie_session_auth/public/image/profile_1.png" />
<img width="1919" height="1079" alt="image" src="../cookie_session_auth/public/image/profile_2.png" />
 
 - Chạy URL: GET http://localhost:3000/auth/profile khi chưa login sẽ gửi trả về message "error": "Unauthorized"
<img width="1919" height="1079" alt="image" src="../cookie_session_auth/public/image/profile_3.png" />
 
 - Chạy URL: GET http://localhost:3000/auth/logout khi send thành công sẽ gửi trả về message "Logout successful!" và trên POSTMAN và MONGODB sẽ xóa cookie_session
<img width="1919" height="1079" alt="image" src="../cookie_session_auth/public/image/logout_1.png" />
<img width="1919" height="1079" alt="image" src="../cookie_session_auth/public/image/logout_2.png" />
<img width="1919" height="1079" alt="image" src="../cookie_session_auth/public/image/logout_3.png" />

