# Install Nexus and push artifactory to Nexus (Linux)
:sparkles::sparkles::sparkles::sparkles::sparkles::sparkles::sparkles::sparkles::sparkles::sparkles::sparkles::sparkles::sparkles::sparkles::sparkles::sparkles:
## Table of content
1. [What is nexus?](#define)
2. [Install](#install)
3. [Run as a service](#service)
<a name="env"></a>
## Chuẩn bị môi trường.
- Cài đặt java
- Đầu tiên add open-jdk repository
```
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
```
- Tiến hành cài đặt 
<a name="define"></a>
## Nexus là gì :question:
- Nexus Repository Manager là công cụ để giúp ta tạo ra các repository để tiện cho việc quản lý các dependencies cho một dự án.
<a name="install"></a>
## Cài đặt :wrench:
- Đầu tiên vào trang [sonatype](https://help.sonatype.com/repomanager3/download) để tải nexus về 
![Download](images/download.png)
- Sau đó giải nén vào một thư mục nào đó >> Vào thư mục đã giải nén >> /home/duong/Downloads/nexus-3.17.0-01/bin >> ./nexus run
![Run](images/nexus_run.png)
- Sau khi chạy xong vào [localhost:8081](http://localhost:8081/) ta thấy giao diện như hình
![Wellcome1](images/wellcome1.png)
- Sau đó ta phải đăng nhập bằng tài khoản admin để có thể tạo các repository trên nexus. Khi lần đầu bấm vào ***sign in*** ở góc phải màn hình sẽ hiện lên một bảng đăng nhập ở đây có ghi thông tin tài khoản admin và nơi chứa mật khẩu. Sau khi đăng nhập thì có thể đổi mật khẩu.
<a name="service"></a>
## Chạy nexus như một service :running_man:
- Tạo một người dùng có đủ quyền để có thể chạy service trong file ***bin/nexus.rc*** ở đây e chọn root:
```run_as_user="root"``` thường thì đầu dòng có dấu # => uncomment nó.
![Download](images/root.png)
- Sau đó symlink từ InstallDir/bin/nexus vào /etc/init.d/nexus: 
  - ```sudo ln -s /home/duong/Downloads/nexus-3.17.0-01/bin/nexus /etc/init.d/nexus```.
- Tạo một file tên nexus.service trong mục etc/systemd/system. Sau đó chèn đoạn script sau:
```[Unit]
Description=nexus service
After=network.target
  
[Service]
Type=forking
LimitNOFILE=65536
ExecStart=/home/duong/Downloads/nexus-3.17.0-01/bin/nexus start
ExecStop=/home/duong/Downloads/nexus-3.17.0-01/bin/nexus stop
User=root
Restart=on-abort
  
[Install]
WantedBy=multi-user.target
```
- Sau khi lưu lại chạy các lệnh: 
```
systemctl daemon-reload
systemctl enable nexus.service
systemctl start nexus.service
```
- Trong đó ***enable***  để service được khởi động cùng hệ thống, ***start*** để chạy service.

Nguồn: [InstallOpenJDK](https://www.geofis.org/en/install/install-on-linux/install-openjdk-8-on-ubuntu-trusty/)
