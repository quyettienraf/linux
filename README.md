# linux
##1. Thay đổi kích thước Swap Space trên ubuntu
- Swap hay còn được gọi là RAM ảo được sử dụng để hỗ trợ lưu trữ dữ liệu khi bộ nhớ vật lý (RAM) đã đầy. Vậy nếu bạn đã có swapfile rồi nhưng dung lượng nó nhỏ quá. Thế là bạn muốn thay đổi thì hãy làm theo các bước sau nhé.

- Dùng lần lượt 6 lệnh sau:
```bash
sudo swapoff /swapfile
sudo fallocate -l 8G /swapfile
ls -lh /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
sudo echo ‘/swapfile none swap sw 0 0’ | sudo tee -a /etc/fstab
```
### Giải thích ý nghĩa các lệnh đã dùng ở trên:
- Tắt/ngưng sử dụng swapfile hiện tại
- Cấp dung lượng 8G cho swapfile (số này bạn thay đổi theo nhu cầu sử dụng nhé)
- Kiểm tra dung lượng file swap vừa tạo và chắc chắn đã có quyền đọc và ghi cho file nhé! (Permission is -rw——-)
- Đánh dấu file vừa tạo là swap file. Nếu không chạy lệnh này hệ thống sẽ sử dụng dung lượng file cũ.
- Bật lại việc sử dụng swapfile
- Thiết lập tự kích hoạt swapfile mỗi khi khởi động lại hệ thống.
Để kiểm tra Swapfile có được kích hoạt chưa hãy dùng lệnh sau: free -h

Hy vọng hữu ích với bạn!
