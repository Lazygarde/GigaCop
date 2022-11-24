# Git
## Khái niệm cơ bản
### Git là gì?
`Git` là một hệ thống quản lý phiên bản phân tán (`Distributed Version Control System` - `DVCS`).
### Git hoạt động như thế nào?
* `Git` là một tập hợp các `snapshot` của một hệ thống tập tin.
* Mỗi lần `commit`, Git sẽ "chụp" và tạo ra một snapshot cùng một tham chiếu tới snapshot đó.
* Để hiệu quả, nếu các tệp không thay đổi, Git sẽ không lưu trữ lại file.

<img src="https://user-images.githubusercontent.com/84316258/203686786-e039e80a-1863-4399-921b-26fb5954ec7f.png" width="500" />

## Các lệnh cơ bản

### `git init`
* Lệnh `git init` để khởi tạo một kho chứa `Git` trong thư mục hiện tại.
* Các tệp được theo dõi bởi `Git` sẽ được lưu trong thư mục `.git`.

### `git commit`
* Câu lệnh `git commit` sẽ lưu lại các thay đổi của bạn vào `git`.
* Cấu trúc của câu lệnh: `git commit -m"message"`

### `git push`
* Câu lệnh `git push` sẽ đẩy các thay đổi của bạn lên `git`.
* Cấu trúc của câu lệnh: `git push origin <branch>`
* Trong đó `origin` là tên của `remote` và `<branch>` là tên của `branch` mà bạn muốn đẩy lên.

### `git pull`
* Câu lệnh `git pull` sẽ lấy các thay đổi từ `git` về máy tính của bạn.
* Cấu trúc của câu lệnh: `git pull origin <branch>`
* Trong đó `origin` là tên của `remote` và `<branch>` là tên của `branch` mà bạn muốn lấy về.

### `git remote`
* Lệnh `git remote` được sử dụng để hiển thị danh sách các remote repository.
* Cấu trúc của câu lệnh: `git remote add origin <url>`
* `origin` là tên của remote repository.

### `git merge`
* Lệnh `git merge` được sử dụng để hợp nhất các nhánh khác vào nhánh hiện tại.
* Cấu trúc của câu lệnh: `git merge <branch>`
* `<branch>` là tên của nhánh cần hợp nhất.

### `git branch`
* Lệnh `git branch` được sử dụng để hiển thị danh sách các nhánh.
* Cấu trúc của câu lệnh: `git branch <branch>`
* `<branch>` là tên của nhánh cần tạo.

### `git fetch`
* Lệnh `git fetch` được sử dụng để lấy các thay đổi từ `remote` về `local`.
* Cấu trúc của câu lệnh: `git fetch <remote>`
* `<remote>` là tên của `remote` repository.
