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
* Cú pháp:
    ```bash
    git init
    ```

### `git commit`
* Câu lệnh `git commit` sẽ lưu lại các thay đổi của bạn vào `git`.
* Cú pháp:
    ```bash
    git commit -m "message"
    ```
    * `-m` là tùy chọn cho phép bạn nhập một thông điệp mô tả cho commit.
    * `message` là thông điệp mô tả cho commit.

### `git push`
* Câu lệnh `git push` sẽ đẩy các thay đổi của bạn lên `git`.
* Cú pháp:
    ```bash
    git push origin <branch>
    ```
    * `origin` là tên của remote repository.
    * `<branch>` là tên của branch.

### `git pull`
* Câu lệnh `git pull` sẽ lấy các thay đổi từ `git` về máy tính của bạn.
* Cú pháp:
    ```bash
    git pull origin <branch>
    ```
    * `origin` là tên của remote repository.
    * `<branch>` là tên của branch.

### `git remote`
* Lệnh `git remote` được sử dụng để hiển thị danh sách các remote repository.
* Cú pháp:
    ```bash
    git remote
    ```


### `git merge`
* Lệnh `git merge` được sử dụng để hợp nhất các nhánh khác vào nhánh hiện tại.
* Cú pháp:
    ```bash
    git merge <branch>
    ```
    `<branch>` là tên của branch.


### `git branch`
* Lệnh `git branch` được sử dụng để hiển thị danh sách các nhánh.
* Cú pháp:
    ```bash
    git branch
    ```


### `git fetch`
* Lệnh `git fetch` được sử dụng để lấy các thay đổi từ `remote` về `local`.
* Cú pháp:
    ```bash
    git fetch <remote>
    ```
    `<remote>` là tên của remote repository.
