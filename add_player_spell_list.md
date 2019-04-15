## TechKids - Code Intensive - Hướng dẫn thực hành
### Thêm nhiều bùa cho nhân vật

1. Ở bài trước, một lá bùa - `PlayerSpell` đã được thêm vào `GameCanvas`, ở bài này, nhiều lá bùa sẽ được thêm vào và xuất hiện cùng lúc.

2. Việc cần làm với yêu cầu này, trong khả thi, không phải là khai báo thêm biến kiểu `PlayerSpell` trfwong `GameCanvas`. Lý do không được làm việc này là vì số lượng Spell trong tương lai sẽ xuất hiện nhiều, trên thực tế là mỗi khi người dùng nhấn phím X để bắn, mỗi lần như vậy, không thể tạm dừng chương trình lại, thêm một biến `PlayerSpell`, chạy lại chương trình rồi mời người chơi chơi tiếp được

3. Tất cả các đối tượng `PlayerSpell` cần phải được quản lý bằng 1 biến duy nhất, để mỗi khi một `PlayerSpell` mới cần được sinh ra, chương trình không cần thay đổi gì

4. Việc quản lý tất cả `PlayerSpell` cần một kiểu dữ liệu có thể chứa được các phần tử giống nhau về kiểu, có thể thêm hay xóa các phần tử ở thời điểm chương trình đã chạy (run-time). Kiểu dữ liệu đáp ứng được các yếu tố này, được gọi là `List` (danh sách), trong `Java`, lập trình viên có thể lựa chọn các biến thể khác nhau của `List`: `ArrayList`, `Vector`, `LinkedList`. Các kiểu dữ liệu này, nếu chỉ thao tác với số lượng phần tử vừa phải (dưới 100, 200 phần tử), thì không khác gì nhau về cách thao tác (Có thể đọc thêm về sự khác biệt giữa các kiểu dữ liệu này ở phụ lục). Ở trường hợp này, `ArrayList` sẽ được sử dụng.

5. 