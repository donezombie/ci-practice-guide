## TechKids - Code Intensive - Hướng dẫn thực hành
### Va chạm và tiêu diệu (Collision and destroy)

1. Va chạm và tiêu diệt là một trong các chức năng bắt buộc phải có của 1 bản demo cho game này, nghĩa là không có chúng, game sẽ không demo chơi được

2. Về cơ bản, bài sẽ được chia làm hai phần:
- Va chạm hay phát hiện va chạm: Cho phép phát hiện va chạm giữa 2 đối tượng quan tâm, cụ thể trong trường hợp này là Enemy và PlayerSpell
- Tiêu diệt: Khi va chạm xảy ra và Enemy mất hết `HP` (Health point), Enemy cần phải bị tiêu diệt, hay nói cách khác là không có mặt

3. Có một vài cách để thực hiện chức năng phát va chạm, ở bài này chỉ đề cập đến cách phù hợp và trực quan nhất để thực hiện, các cách kiểm tra va chạm khác có thể được tìm thấy ở phụ lục

4. Bắt tay vào thực hiện, mở file `GameCanvas.java`

5. Ở trong file `Canvas.java` hiện tại, đang có một đối tượng Enemy - biến `e`, và nhiều hơn một đối tượng `PlayerSpell`, nằm trong list `spells`. Chức năng phát hiện va chạm sẽ được thực hiện với 1 đối tượng Enemy và list spells này, trong tương lai, có thể sẽ có nhiều hơn 1 đối tượng Enemy trong game cần được kiểm tra va chạm với nhiều hơn 1 lá bùa do Player bắn ra, tuy có khác với tình huống hiện tại, nhưng cách làm gần như là tương tự.

6. Việc check va chạm sẽ được liên tục kiểm tra, thế nên sẽ cần đặt trong `gameLoop()`. Đặt hàm `checkCollision()` trong hàm `gameLoop()` và thực hiện khai báo hàm này







