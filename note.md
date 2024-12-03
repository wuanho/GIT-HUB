1. Thuật ngữ trong Git:

- Repository (Repo): Là kho lưu trữ, nơi chứa tất cả mã nguồn và lịch sử thay đổi của dự án. Có thể là kho lưu trữ cục bộ (local) hoặc từ xa (remote).

- Branch: Là một nhánh trong kho lưu trữ Git, giúp bạn làm việc song song với các tính năng khác nhau mà không ảnh hưởng đến nhánh chính (thường là master hoặc main). Mỗi nhánh là một bản sao riêng biệt của mã nguồn.

- Conflict: Xảy ra khi có sự mâu thuẫn giữa các thay đổi được thực hiện trên cùng một phần của mã nguồn trong các nhánh khác nhau. Git không thể tự động giải quyết sự mâu thuẫn này và bạn phải chỉnh sửa thủ công.

- Local: Là kho lưu trữ trên máy tính của bạn. Mọi thay đổi trong kho lưu trữ cục bộ phải được "đẩy" (push) lên kho lưu trữ từ xa để đồng bộ với người khác.

- Remote: Là kho lưu trữ Git trên server hoặc dịch vụ như GitHub, GitLab, Bitbucket. Đây là nơi các thay đổi được chia sẻ giữa các lập trình viên.

2. Các lệnh Git:

- git init: Khởi tạo một kho lưu trữ Git mới trong thư mục hiện tại. Kho này sẽ lưu trữ tất cả các thay đổi của mã nguồn.

- git status: Kiểm tra trạng thái của kho lưu trữ, bao gồm các thay đổi đã được stage (chờ commit), các file bị thay đổi, các file chưa được theo dõi (untracked), v.v.

- git add: Thêm các file hoặc thư mục vào "staging area" (khu vực chuẩn bị commit). Ví dụ: git add . để thêm tất cả các thay đổi trong thư mục hiện tại.

- git reset: Hoàn tác thay đổi. Dùng để hủy bỏ commit, đưa lại các file về trạng thái trước commit đó. Thường dùng khi cần điều chỉnh các lỗi trong commit trước đó.

- git commit: Xác nhận các thay đổi đã được thêm vào staging area. Một commit sẽ tạo ra một điểm mốc trong lịch sử của kho lưu trữ.

- git log: Xem lịch sử các commit đã thực hiện. Dùng để theo dõi các thay đổi trong dự án.

- git log --oneline: Hiển thị lịch sử commit dưới dạng ngắn gọn, mỗi commit chỉ hiển thị một dòng.

- git checkout {branch name}: Chuyển sang một nhánh khác trong kho lưu trữ.

- git branch: Liệt kê tất cả các nhánh trong kho lưu trữ. Nhánh hiện tại sẽ được đánh dấu sao.

- git checkout -b {branch name}: Tạo và chuyển sang nhánh mới cùng một lúc.

- git merge {branch name}: Hợp nhất nhánh {branch name} vào nhánh hiện tại. Nếu có xung đột, Git sẽ yêu cầu bạn giải quyết.

- git branch {branch name}: Tạo một nhánh mới có tên {branch name} mà chưa chuyển sang nhánh đó.

- git branch -d {branch name}: Xóa nhánh {branch name} nếu nhánh này đã được hợp nhất vào nhánh chính. Nếu chưa hợp nhất, Git sẽ cảnh báo.

- git push: Đẩy các thay đổi từ kho lưu trữ cục bộ lên kho lưu trữ từ xa (remote). Bạn cần có quyền để thực hiện hành động này.

- git push -u origin {branch name}: Đẩy nhánh {branch name} lên kho lưu trữ từ xa và thiết lập nhánh này làm nhánh "tracking" cho nhánh từ xa, giúp đẩy và kéo (pull) các thay đổi dễ dàng hơn sau này.

- git remote add origin {repo url}: Thêm kho lưu trữ từ xa với tên "origin" và URL kho lưu trữ đó.

- git clone {repo url}: Tạo một bản sao của kho lưu trữ từ xa vào máy cục bộ, tải về tất cả mã nguồn và lịch sử của kho đó.

- git fetch origin: Tải về tất cả các thay đổi từ kho lưu trữ từ xa mà không tự động hợp nhất (merge) vào nhánh cục bộ.

- git checkout -b {branch name} origin/{branch name}: Tạo và chuyển sang nhánh mới từ kho lưu trữ từ xa {branch name}.
