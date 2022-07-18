#### GIT là gì
1. Git giúp ghép code trong 1 dự án
2. Nội dung và các phần của git
- 3 phần:
        Working space   ->   Stage Area   ->   git Local
    + working space: Những thao tác trên máy của mình => ví dụ tạo 1 folder mới thì nó sẽ nằm trên working space
    + stage area: khu vực trạng thái (trung gian)
        - Trạng thái: M - sửa đổi, A - add new (file mới)
    + git local: quản lí code được đưa lên => tạo ra bằng cách dùng git init
        => chứa các commit mới và cũ (lịch sử)


- Flow:
    + git init => tạo ra git local
    + git add . => thêm toàn bộ những thứ mới hoặc thay đổi trong woking place lên stage area
    + git commit -m "" => đưa các file trong stage area sang git local (-m để comment sửa đổi hay thêm mới)
    + git remote add origin http://... : liên kết git local với remote (lần đầu)
    + git push -u origin master (lần đầu, lầu sau chỉ cần git push)

- Quay lại commit cũ: 
    Ví dụ: có 2 commit c1 và c2, ta đang ở c2 => muốn quay lại c1
    + lệnh : git checkout c1 
    + Hành động: Quay lại commit c1 và đồng thời woking space cũng lấy lại các file trong c1


3. Gitlab, github là gì?
- Tất cả những thứ ở trên đều nằm trên máy tính của ta
- Gitlab, github => là kho chứa trên mạng => giúp đẩy các dữ liệu từ git local lên kho chứa trên mạng
- Đẩy code từ git local lên trên remote(kho chứa trên mạng):
    + lệnh: git push origin master
    + tên remote mặc định: "origin"

- git clone: (dùng lần đầu) để tải toàn bộ source code về máy, lưu cả lịch sử của các lần commit trước về máy
- git pull origin master: kéo dữ liệu những phần code mới
- git config credential.helper store: lưu acount git vào máy tính

#### Branch
- branch "master": code chính thống, không code trực tiếp trên master 
- git branch: tạo ra 1 branch nhưng chưa chuyển tới branch đó -> dùng git checkout để chuyển
- git checkout -b "your branch" : tạo mới 1 branch và di chuyển tới branch đó
- git checkout "your branch" : di chuyển tới branch đó
- git merge "tên commit cần merge" : tạo ra 1 commit mới và merge commit cần merge vào commit hiện tại
