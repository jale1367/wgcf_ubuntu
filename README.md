# wgcf_ubuntu

Steps to get Cloudflare Warp to works on Ubuntu

1 - Setup Wireguard

sudo apt install wireguard

2 - Tải wgcf
Download wgcf tại https://github.com/ViRb3/wgcf/releases

Đôi với AMD64
https://github.com/ViRb3/wgcf/releases/download/v2.2.3/wgcf_2.2.3_linux_amd64

Lưu vào /user/local/bin và set exexute để có thể chạy wgcf

cd /usr/local/bin
sudo wget -o wgcf https://github.com/ViRb3/wgcf/releases/download/v2.2.3/wgcf_2.2.3_linux_amd64
sudo chmod +x wgcf

3 - Cấu hình Warp

sudo -i

cd /etc/wireguard

wgcf register

wgcf generate -p warpplus.conf

exit

4 - Chạy warp

sudo systemctl start wg-quick@warpplus

Lưu ý: Nếu dùng ubuntu minimal thì cần cài thêm resolvconf

sudo apt install resovconf





