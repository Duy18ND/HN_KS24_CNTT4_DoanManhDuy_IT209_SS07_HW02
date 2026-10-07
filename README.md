# Bài 2: Quản trị Tường lửa UFW cho Cụm Dịch vụ Multi-port

## 1. Quá trình cấu hình
Các lệnh đã được thực thi trên máy chủ để thiết lập chính sách bảo mật:

```bash
# 1. Thiết lập chính sách mặc định (Chặn toàn bộ chiều vào, cho phép chiều ra)
sudo ufw default deny incoming
sudo ufw default allow outgoing

# 2. Mở cổng cho các dịch vụ được phép (SSH, Nginx Web, Spring Boot)
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw allow 8082/tcp

# 3. Kích hoạt tường lửa
sudo ufw enable

<img width="534" height="297" alt="image" src="https://github.com/user-attachments/assets/149811cf-ad6b-4003-8862-a4961e477786" />
