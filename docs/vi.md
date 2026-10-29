# Cthangover: Starter Party — nhân vật khởi đầu của người chơi

Mod nhỏ này tạo trạng thái khởi đầu cho một ván mới của Cthangover: Marao trong tổ đội và kỹ năng Kẻ buôn nô lệ trong bộ sưu tập kỹ năng. Bên trong chỉ có mã này; bản thân nhân vật và kỹ năng là dữ liệu của trò chơi gốc và của engine kỹ năng.

## Người chơi mới có gì

Bảng nhân vật ngay lúc đầu của Cthangover — một thành viên tổ đội, Marao, với hai hành động và một ô trống:

![Bảng hành động nhân vật: Đội 1, Marao (mẫu 2, HP 16/16, AP 1, ATK 5, DEF 0) với Tấn công thường và Phòng thủ, ô thứ ba trống.](assets/party.jpg)

Bảng kỹ năng — một kỹ năng, Kẻ buôn nô lệ:

![Bảng kỹ năng: bộ sưu tập có một kỹ năng bị động huyền thoại, Kẻ buôn nô lệ, “+10% tỉ lệ chiêu mộ”, mô tả “Cho phép biến kẻ thù bị đánh bại thành nô lệ với tỉ lệ cơ bản 10%. Việc nuôi nô lệ do bạn lo.”, hiệu ứng bộ sưu tập +10% tỉ lệ chiêu mộ.](assets/skills.jpg)

Kẻ buôn nô lệ chính là thứ cho phép người chơi bắt giữ kẻ địch bị đánh bại (xem Recruiting): thiếu nó thì không kẻ địch nào gia nhập được.

## Khi nào chạy

- Khi các mod của trò chơi đã sẵn sàng, mod thêm nhân vật `Marao` vào tổ đội và trao kỹ năng `slave_master`.
- Mỗi lần bắt đầu **trò chơi mới**, nó làm lại việc đó, vì trò chơi mới trước tiên dọn sạch tổ đội.
- Tải bản lưu sẽ thay tổ đội và kỹ năng bằng những gì đã lưu. Cả hai bước chạy nhiều lần cũng an toàn: Marao không bị thêm hai lần và kỹ năng không bị trao hai lần.

## Muốn đổi phần khởi đầu

- Mod khác có thể thêm nhân vật khởi đầu theo cùng cách: một bộ khởi tạo bằng C# thêm nhân vật của mình vào tổ đội khi các mod sẵn sàng.
- Để bắt đầu không có Marao hay kỹ năng, bỏ mod này khỏi bộ sưu tập của trò chơi và tự dựng tổ đội trong mod của bạn.

## Vấn đề đã biết

- Thẻ Kẻ buôn nô lệ không có hình: ảnh của kỹ năng bị thiếu.
- Thẻ và mô tả hứa “+10% tỉ lệ chiêu mộ”, nhưng không có mã nào đọc thêm chỉ số này; lượt gieo bắt giữ chỉ dùng tỉ lệ của chính kẻ địch.
