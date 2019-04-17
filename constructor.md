## TechKids - Code Intensive - Hướng dẫn thực hành
### Hàm tạo (constructor)

1. Hiện tại, trong `GameCanvas`, để khởi tạo và sử dụng được 1 đối tượng `PlayerSpell`, cần đến 4 dòng code:

<pre>
      public GameCanvas() {
        ...
        PlayerSpell firstSpell = new PlayerSpell();
        firstSpell.x = 170;
        firstSpell.y = 450;
        firstSpell.loadImage();
        ...
      }
</pre>

hay

<pre>
      void castSpells() {
        ...
        PlayerSpell newSpell = new PlayerSpell();
        newSpell.x = p.x;
        newSpell.y = p.y;
        newSpell.loadImage();
        ...
      }
</pre>

2. Hay nói cách khác, để có thể bắt đầu sử dụng được 1 đối tượng `PlayerSpell`, lập trình viên sử dụng `PlayerSpell` sẽ phải nhớ và làm đủ 4 thao tác này

3. Việc này nghe có vẻ nhẹ nhàng vì hiện giờ trong game mới chỉ tồn tại 1 class có vấn đề như vậy, tuy nhiên với các chương trình Java, số lượng class cần khai báo như vậy có thể nhiều hơn đến hàng trăm, hàng nghìn lần, đồng nghĩa với việc xác suất quên một trong vài thao tác trên, phát sinh các lỗi về logic không đáng có.

4. Trong lập trình hướng đối tượng mà cụ thể là Java, sai sót này được loại bỏ bằng cách viết hàm tạo (constructor) cho `PlayerSpell`, để khi cần khởi tạo đối tượng, người sử dụng class buộc phải cung cấp đầy đủ các thông tin cho đối tượng luôn, nếu không muốn chương trình lỗi không thể chạy được.

5. Mở file `PlayerSpell.java`, bắt đầu thực hiện việc viết hàm tạo cho class này

<pre>
public class PlayerSpell {
    int x;
    int y;
    BufferedImage image;
    ...
    <b>PlayerSpell(int xStart, int yStart) {
      x = xStart;
      y = yStart;
    }</b>
    ...
}
</pre>

Chú ý:
1. `PlayerSpell()` được gọi là hàm tạo (constructor) với dấu hiệu nhận biết là __không có kiểu trả về__ và __có cùng tên với tên của class__
2. Để `PlayerSpell` khởi tạo được, lập trình viên buộc phải cung cấp hai tham số đầu vào là `xStart` và `yStart`, là 2 giá trị ban đầu cho `x` và `y`

6. Quay lại file `GameCanvas.java`, có thể thấy `IntelliJ` đang báo lỗi khởi tạo cho `PlayerSpell` với lý do không cung cấp đủ tham số


![Constructor error 1](images\constructor\constructor_error_1.png)

Và

![Constructor error 1](images\constructor\constructor_error_2.png)

7. Để có thể khởi tạo được `PlayerSpell`, lập trình viên buộc phải thay đổi cách gọi hàm tạo, cung cấp các tham số mà hàm này yêu cầu

<pre>
  public GameCanvas() {
    ...
    <s>PlayerSpell firstSpell = new PlayerSpell()</s>
    <s>firstSpell.x = 170</s>
    <s>firstSpell.y = 450</s>
    <b>PlayerSpell firstSpell = new PlayerSpell(170, 450);</b>
    firstSpell.loadImage();
    ...
  }
</pre>

<pre>
  void castSpells() {
    if (xPressed) {
      <s>PlayerSpell newSpell = new PlayerSpell();</s>
      <s>newSpell.x = p.x</s>
      <s>newSpell.y = p.y</s>
      <b>PlayerSpell newSpell = new PlayerSpell(p.x, p.y);</b>
      newSpell.loadImage();
      ...
</pre>

8. Chạy thử chương trình, nếu các tính năng vẫn hoạt động bình thường, việc khai báo và sử dụng hàm tạo đã hoàn tất

![Result](images\constructor\result.gif)