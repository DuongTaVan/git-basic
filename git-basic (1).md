# GIT là gì. Vai trò của git.
- Git như một kho lưu trữ riêng cho toàn bộ lịch sử thay đổi. 
- Vai trò của git: 
	+ Lưu lại những phiên bản khác nhau của mã nguồn dự án phần mềm. 
	+ Khôi phục lại các mã nguồn từ một phiên bản bất kỳ khác. 
	+ Hỗ trợ so sánh dễ dàng hơn giữa các phiên bản. 
	+ Phát hiện được những vị trí, những phần mà người khác đã chỉnh sửa làm phát sinh lỗi. 
	+ Khôi phục lại những tập tin đã bị mất đi. 
	+ Thử nghiệm và mở rộng các tính năng của dự án một cách dễ dàng mà không làm ảnh hưởng đến các phiên bản chính. 
	+ Hỗ trợ phối hợp thực hiện dự án trong một nhóm mang lại nhiều hiệu quả hơn. 
	+ Git đảm bảo không có xung đột code giữa các lập trình viên trong một nhóm. 
	+ Chỉ cần có clone mã nguồn từ kho chứa hoặc clone một phiên bản thay đổi nào đó từ kho chứa hoặc một nhánh nào đó từ kho chứa là lập trình viên có thể bắt tay vào làm việc mọi lúc mọi nơi.
# Cách tạo 1 repository.
- Cách tạo: Tạo trực tiếp trên git.
# Tạo branch, commit, push.
* Brach: 
- Khái niệm: Nhánh có tác dụng tách riêng được các tính năng của dự án rồi thử nghiệm những tính năng mới dễ dàng hơn.
- Cách tạo một branch: 
 	+ Branch có thể tạo được bằng lệnh branch.
	+ Khi thực hiện lệnh branch mà không chỉ định tham số, thì có thể hiển thị danh sách các branch. Ở đầu có dấu * là branch hiện tại.
* Commit: 
- Khái niệm: Commit là thao tác báo cho hệ thống biết bạn có muốn lưu lại trạng thái hiện hành hay không rồi ghi nhận lại lịch sử các xử lý đã thực hiện như: xóa, cập nhật, thêm các file hoặc thư mục nào đó trên repository.
- Cách tạo một commit: 
	+ Ta sử dụng cú pháp: git commit -m "Ghi chú Commit"
*Push: 
 Lệnh Push thường được sử dụng để đưa nội dung kho lưu trữ cục bộ lên server và nó cũng là cách bạn chuyển giao các commit từ kho lưu trữ cục bộ lên server. 
# Git merge, rebase. Phân biệt rebase và merge.
- Git merge: Tức là gộp hai branch lại với nhau, thao tác này thường dùng để merge branch khác vào branch master trước khi push lên remote repository, hoặc merge hai branch thành một để giải quyết chung một task.
- Git rebase: Git Rebase là một chức năng được dùng khi gắn nhánh đã hoàn thành công việc vào nhánh gốc . Về mặt nội dung thì là việc điều chỉnh nhánh công việc gắn vào với nhánh gốc nên các commit sẽ được đăng kí theo thứ tự gắn vào .
- Phân biệt giữa git rebase và git merge: 
	Nếu so với rebase thì merge là cách có thể tích hợp với master với rất nhiều nhánh trong 1 lần . Tuy nhiên trường hợp tích hợp bằng merge thì những commit của branch sẽ hoàn toàn không được record lại 
# Merge commit.
- Khi code mà thực hiện commit nhiều lần với cùng 1 vấn đề. có thể tận dụng lại commit trước đó. Hoặc thực hiện gộp nhiều commit lại.
# Git tag, release
* Git tag: 
- Tag cho phép ta xác định một cách rõ ràng các phiên bản mã nguồn (code) của dự án.
- Có 2 loại tag là annotated và lightweight:
	+ Lightweight tag được tạo chỉ gồm tên mà không có các tùy chọn -a, -s hoặc -m và không chứa bất kỳ thông tin bổ sung nào.
	+ Annotated tag ngoài tên nó còn có thể lưu trữ dữ liệu bổ sung như Tên tác giả (-s), tin nhắn (-m: message), và ngày dưới dạng các đối tượng đầy đủ trong cơ sở dữ liệu Git.
* Git release:
- Mục đích tạo release là để chia sẻ đóng gói ứng dụng, cùng các ghi chú phát hành và các link tới các file tài liệu ứng dụng cho mọi người trong team, công ty có sửa dụng.
# Git flow.
- git-flow là một tiện ích mở rộng của git, giúp các thao tác trên repository (kho mã nguồn) trở nên dễ dàng và hiệu quả hơn dựa trên mô hình phân nhánh của Vincent Driessen.
- Điểm lợi lớn nhất của Git Flow là giúp việc theo dõi và xử lý các vấn đề nảy sinh do một tính năng, một bản fix rất dễ dàng. Quá trình review sẽ thuận tiện và quan sát được các lỗi nảy sinh trong quá trình deploy.
- Nhược điểm: nếu muốn tăng thời gian triển khai production thì sẽ gặp hạn chế đôi chút về mặt thời gian. Ngoài ra, việc remove các commit không đạt yêu cầu chất lượng cũng khó khăn hơn.
