# Khái niệm cơ bản
## Git là gì?

`Git` là một hệ thống quản lý phiên bản phân tán (Distributed Version Control System - `DVCS`).

## Git hoạt động như thế nào?

* `Git` là một tập hợp các `snapshot` của một hệ thống tập tin.

* Mỗi lần `commit`, Git sẽ "chụp" và tạo ra một snapshot cùng một tham chiếu tới snapshot đó.

* Để hiệu quả, nếu các tệp không thay đổi, Git sẽ không lưu trữ lại file.

<img src="https://user-images.githubusercontent.com/84316258/203686786-e039e80a-1863-4399-921b-26fb5954ec7f.png" width="500" />

# Phân biệt remote repo và local repo

* `remote repo`: là kho chứa trên mạng, nơi nhiều người làm việc chung, có thể là github, gitlab, bitbucket, ...

* `local repo`: là kho chứa trên máy tính cá nhân, nơi mà mỗi người làm việc độc lập, có thể là git bash, git gui, git desktop, ...

* `origin`: là tên mặc định của remote repo, có thể đổi tên.

<img src="https://user-images.githubusercontent.com/84316258/203879233-ddfc1198-6e2c-474d-9c63-38024ea776ba.png" width="500" />

# Bắt đầu

## Cài đặt Git
Download [git](https://git-scm.com/downloads) và cài đặt.
## Cấu hình Git
* Cấu hình tên người dùng
    ```bash
    git config --global user.name "Tên người dùng"
    ```
* Cấu hình email
    ```bash
    git config --global user.email "Email"
    ```
* Kiểm tra cấu hình
    ```bash
    git config --list
    ```
    <img src="https://user-images.githubusercontent.com/84316258/203887359-a51bf3b0-ffb6-45f7-97b9-ebb2c14c0e85.png" width="500" />

## Tạo kho chứa

* Tạo một thư mục mới
    ```bash
    mkdir tên_thư_mục
    ```

* Chuyển đến thư mục vừa tạo
    ```bash
    cd tên_thư_mục
    ```

* Khởi tạo git
    ```bash
    git init
    ```

* Kiểm tra trạng thái
    ```bash
    git status
    ```
    <img src="https://user-images.githubusercontent.com/84316258/203887837-4909892e-ac9e-4b1e-b013-ff5bb8648f78.png" width="500" />

## Liên kết với remote repo

* Liên kết với remote repo
    ```bash
    git remote add origin đường_dẫn
    ```

* Kiểm tra remote repo
    ```bash
    git remote -v
    ```

    <img src="https://user-images.githubusercontent.com/84316258/203888472-e6e4366e-0b81-44d7-a5c6-d25427e08717.png" width="500" />

## Trạng thái của các file
* `Untracked`: là file chưa được theo dõi bởi Git.

    VD: trong thư mục có 1 file `git.md` chưa được theo dõi bởi Git.
    <img src="https://user-images.githubusercontent.com/84316258/203889061-bd2cbb5e-86ce-4a28-96f5-75bedc751ddc.png" width="500" />
* `Unmodified`: là file đã được theo dõi bởi Git nhưng chưa được chỉnh sửa.
* `Modified`: là file đã được theo dõi bởi Git và đã được chỉnh sửa.
* `Staged`: là file đã được theo dõi bởi Git và đã được chỉnh sửa và đã được chuẩn bị để commit.

<img src="https://user-images.githubusercontent.com/84316258/203888579-defbbd2e-3a45-4c18-bf0a-15ae97c23b17.png" width="500" />

## Thêm file vào kho chứa

* Thêm tất cả các file
    ```bash
    git add .
    ```
* Thêm một file
    ```bash
    git add tên_file
    ```

## Commit
Khi cần lưu lại các thay đổi, ta sẽ `commit`. Sau khi `commit`, các thay đổi sẽ được lưu lại trên local repo.
```bash
git commit -m "message"
```

<img src="https://user-images.githubusercontent.com/84316258/203890207-6e647a34-89b0-4f64-9d2d-339ccb31c44a.png" width="500" />

## Push
Khi cần đẩy các thay đổi lên remote repo, ta sẽ `push`.

```bash
git push -u origin main
```

<img src="https://user-images.githubusercontent.com/84316258/203891761-d708cacd-dea4-4c7f-b0a8-9d128ec34ac1.png" width="500" />

## Pull
Khi cần lấy các thay đổi từ remote repo về local repo, ta sẽ `pull`.

```bash
git pull origin main
```

# Cấu trúc `branch` trong Git
* `master`: là branch mặc định của Git. Nó là branch chính của dự án.
* Thông thường khi làm việc với Git, ta sẽ tạo ra các branch khác để phân chia công việc. Sau khi hoàn thành công việc, ta sẽ merge các branch vào branch `master`. Và một dự án, ngoài branch `master` thường có các branch sau:
    * `develop`: là branch phụ của dự án. Nó được tạo ra từ branch `master` và dùng để phát triển các tính năng mới. Khi tính năng mới đã hoàn thành, ta sẽ merge branch `develop` vào branch `master`.

    * `feature`: là branch phụ của dự án. Nó được tạo ra từ branch `master` và dùng để phát triển các tính năng mới. Khi tính năng mới đã hoàn thành, ta sẽ merge branch `feature` vào branch `master`.

    <img src="https://user-images.githubusercontent.com/84316258/203892730-e2db8d2d-0f97-46f2-8b16-7f4f7ca6b93a.png" width="500" />
* Để tạo branch mới, ta sử dụng lệnh:
    ```bash
    git branch tên_branch
    ```
* Khi cần làm việc với branch, ta sẽ dùng lệnh `checkout` để chuyển sang branch đó.

    ```bash
    git checkout tên_branch
    ```

* Để merge branch `feature` vào branch `master`, ta sẽ dùng lệnh:
    ```bash
    git checkout master
    git merge feature
    ```
* Để xóa branch, ta sẽ dùng lệnh:
    ```bash
    git branch -d tên_branch
    ```
