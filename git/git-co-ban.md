# Git cơ bản
1.	Git config:  git config -- global user.name <username>
git config -- global user.email <email>
git config --global user.password <password>

<gỡ config:  git config –-global unset user.password>

2.	Git init : Tạo thư mục dự án:  git init trong thư mục gốc của dự án
3.	Git clone: copy từ thư mục dự án gốc về: git clone url_thumuc
4.	Git status: kiểm tra trạng thái commit, các thay đổi.
5.	Git add: thêm các mục trong thư mục.
Git add -u (thêm thay đổi những file đã có để commit)
Git add -A(thêm cả file mới để commit)
6.	Git commit: git commit -m “message” – đẩy code lên nhưng không chia sẽ với ai. Có thể kết hợp add nếu có và commit: git commit -a -m “example”
7.	Git push/pull: đẩy code lên remote branch:
git pull remote_name branch_name  and git push remote_name branch_name;
ghi đè: git push remote_name branch_name -f;
8.	Xóa local branch: git branch -D branch/name
9.	Xóa remote branch: git push remote_name branch_nam –delete
10.	Thay đổi url của remote: git remote set-url remote_name url_remote;
11.	Thay đổi tên remote: git remote rename old_name new_name;
12.	Xóa remote: git remote remove remote_name
13.	Git branch: liệt kê các nhánh: git branch hoặc git branch -a
14.	Git checkout: Chuyển sang nhánh(branch) khác: 
git checkout <: branch:>
hoặc ** _ git checkout -b <: branch:> nếu muốn tạo và chuyển sang một nhánh mới.
15.	Git stash: lưu thay đổi nhưng chưa muốn commit
16.	Git merge: Nhóm 2 nhánh lại với nhau
Chuyển tới branch muốn merge rồi  dùng git merge <:branch _muon_merge:>
17.	Git reset: Bỏ commit một tệp trong thư mục git reset HEAD tên_file (dùng để bỏ 1 file ra khỏi lệnh add trước khi commit)
18.	Git remote: kiểm tra remote hiện có: git remote -v; thêm remove: git add remote url_remove;
19.	Git add ten_file; Git add all: thêm các mục vào phần thư mục tổ chức
20.	So sánh thay đổi trước và sau commit: git diff.
21.	Gộp 3 commit gần nhất làm 1: git rebase -I HEAD~3;
Sửa “Pick” thành ‘s’ để gộp, ‘Pick’ thành ‘d’ để xóa commit, Ctrl+O, Enter.
22.	Lịch sử commit (log): git log
	Note:
A.	Khi commit mà chưa có message sẽ có bảng thông báo, để thoát khỏi bảng này: ESC + ‘ : wq’ + Enter.
B.	Lỗi khi push: Could not resolve host:
	git config --global --unset http.proxy 
	git config --global --unset https.proxy
C.	Lỗi 403 khi push
git remote remove origin
git remote add origin url_

git push --set-upstream origin master
D.
Lỗi không đổi checkout được: $ git checkout master
fatal: Unable to create 'C:/Users/Fox/.git/index.lock': File exists.

Another git process seems to be running in this repository, e.g.
an editor opened by 'git commit'. Please make sure all processes
are terminated then try again. If it still fails, a git process
may have crashed in this repository earlier: remove the file manually to continue.
 Cách sửa: Gõ lệnh del .git\index.lock trong commandline




