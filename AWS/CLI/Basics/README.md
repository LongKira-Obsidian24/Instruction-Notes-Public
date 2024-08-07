# AWS CLI cơ bản

## 1. Các phiên bản AWS CLI

AWS CLI gồm hai phiên bản: 1 và 2 (mới nhất). Hiện tại, phiên bản 2 có một số tính năng không được thêm vào phiên bản 1. Đồng thời, một số câu lệnh được thay đổi trong bản 2 nên không hoàn toàn tương thích với bản 1. Do đó, để chuyển đổi các script từ AWS CLI 1 lên AWS CLI 2, cần viết lại một số lệnh. Hiện tại, bạn có thể xem hướng dẫn [tại đây](https://docs.aws.amazon.com/cli/latest/userguide/cliv2-migration.html) (hướng dẫn tiếng Việt có thể được cung cấp trong tương lai).

Để sử dụng các tính năng mới nhất và nhận được sự hỗ trợ, bài viết khuyến khích độc giả sử dụng AWS CLI 2 nếu không có các yêu cầu đặc biệt.

## 2. Tải và cài đặt AWS CLI
### 2.1 Trên Windows
Tải AWS CLI tại các liên kết sau:

- [AWS CLI 1](https://s3.amazonaws.com/aws-cli/AWSCLI64PY3.msi)
- [AWS CLI 2]([https://awscli.amazonaws.com/AWSCLIV2.msi](https://awscli.amazonaws.com/AWSCLIV2.msi)) _**(Khuyến khích)**_ (Windows | Linux)

Chạy tập tin cài đặt và nhấn _Next_ trong hầu hết các cửa sổ. Riêng tại cửa số _Custom setup_, bạn có thể chọn nơi cài đặt AWS CLI tại _Browse_.

![[Location.jpg]](IMG/Location.jpg)

Sau khi cài đặt xong, bạn nhấn _Finish_ và đã có thể sử dụng AWS CLI. Để đăng nhập vào AWS, chuyển sang phần 3.

## 3. Đăng nhập vào AWS trên AWS

### 3.1. Tạo Access Key
Truy cập vào bảng điều khiển AWS [IAM](console.aws.amazon.com/iam), vào mục _User_ và chọn _Create access key_.

![[AccessKey.jpg]](IMG/AccessKey.jpg)

Chọn mục đích sử dụng là _CLI_

![[AccessKeyStep1.jpg]](IMG/AccessKeyStep1.jpg)

Kéo xuống và đánh dấu tích xác nhận trước khi chuyển sang bước kế tiếp.

![[AccessKeyStep12.jpg]](IMG/AccessKeyStep12.jpg)

Điền thẻ bạn mong muốn:

![[AccessKeyStep2.jpg]](IMG/AccessKeyStep2.jpg)

Lưu khóa về máy dưới dạng CSV.

![[AccessKeyStep3.jpg]](IMG/AccessKeyStep3.jpg)

Trong cửa sổ dòng lệnh, chạy lệnh `aws configure` và điền các thông tin tương ứng

![[CLIconfig.jpg]](IMG/CLIconfig.jpg)