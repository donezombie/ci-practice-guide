## TechKids - Code Intensive - Hướng dẫn thực hành
### Bài tập: Thêm bùa cho nhân vật

1. Để thực hiện việc tấn công, trước tiên cần thực hiện class mô tả lá bùa cho player

Tạo class `PlayerSpell` với file `PlayerSpell.java`

2. Khi thực hiện bất kỳ class như PlayerSpell, cần trả lời hai câu hỏi chính:

- Class này cung cấp những thao tác nào (methods) cho người dùng?
- Để cung cấp những thao tác trên, class này cần những thống tin (properties) nào để hoạt động?

3. Với `PlayerSpell`, có thể trả lời các câu hỏi trên như sau:

- Các thao tác:
  - Di chuyển tự động (không phụ thuộc vào phím bấm của người dùng)
  - Hiển thị (được vẽ lên) trên màn hình (GameCanvas)
  - Khi chạm vào enemy, cần gây sát thương (damage)
- Các dữ liệu:
  - Để di chuyển tự động, `PlayerSpell` cần có tọa độ `x`, `y` và có thể là một dữ liệu biểu diễn tốc độ, `speed`, được cộng liên tục vào `x` và/hoặc `y`
  - Để hiển thị được, `PlayerSpell` cần có ảnh, `image`
  - Dữ liệu cho va chạm và gây sát thương sẽ được trình bày và thực hiện ở một mục riêng

4. Dựa vào các phân tích trên, thực hiện class `PlayerSpell`, đưa class này vào sử dụng và cho đối tượng sinh ra bởi class này hiển thị và di chuyển tự động 