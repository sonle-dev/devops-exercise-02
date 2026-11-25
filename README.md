# Bài Tập 2: Làm quen CLI Linux - Thao tác file và kiểm tra User/Group

* **Môn học:** Quản trị Hệ thống & Mạng / DevOps
* **Session:** 01
* **Exercise:** 02
* **Học viên:** sonledev

---

## 1. Yêu cầu bài tập
1. Di chuyển vào thư mục home bằng lệnh `cd ~`, tạo một thư mục trống tên là `quickbite-test` bằng lệnh `mkdir`.
2. Tạo một file rỗng tên là `readme.txt` và ghi nội dung cơ bản vào bên trong.
3. Tại thư mục đó, liệt kê chi tiết danh sách file (bao gồm file ẩn) kèm thông tin phân quyền (`ls -la`).
4. Chạy lệnh hiển thị danh sách tất cả các tài khoản người dùng (`users`) đang tồn tại trên hệ thống.
5. Chạy lệnh hiển thị danh sách tất cả các nhóm người dùng (`groups`) đang tồn tại trên hệ thống.

---

## 2. Toàn bộ câu lệnh thực hiện

### 2.1. Thao tác thư mục và file
```bash
# 1. Di chuyển về thư mục Home của user
cd ~

# 2. Tạo thư mục quickbite-test và chuyển vào bên trong
mkdir -p quickbite-test
cd quickbite-test

# 3. Tạo file readme.txt và ghi nội dung
echo "QuickBite Project - System Initialization Test" > readme.txt

# 4. Liệt kê chi tiết file bao gồm cả file ẩn và phân quyền
ls -la
```
* **Kết quả:** Hiển thị file `readme.txt` với quyền hạn mặc định `-rw-r--r--` thuộc sở hữu của user `sonledev`.

### 2.2. Kiểm tra danh sách User và Group hệ thống
```bash
# Hiển thị toàn bộ user trong hệ thống từ file cấu hình /etc/passwd
getent passwd
# Hoặc: cat /etc/passwd

# Hiển thị toàn bộ group trong hệ thống từ file cấu hình /etc/group
getent group
# Hoặc: cat /etc/group
```

---

## 3. Tệp nộp bài
* **Ảnh chụp lệnh `ls -la`:** [homework/session_01/exercise_02/ls_la.png](homework/session_01/exercise_02/ls_la.png)
* **Ảnh chụp danh sách User:** [homework/session_01/exercise_02/users_list.png](homework/session_01/exercise_02/users_list.png)
