## TechKids - Code Intensive - Hướng dẫn thực hành
### Hàm tạo cho Enemy và Player

1. Viết hàm tạo cho class `Enemy`

<pre>

public class Enemy {
  ...
  <b>Enemy(int xStart, int yStart) {
      x = xStart;
      y = yStart;
  }</b>
  ...
}

</pre>

2. Cập nhật lại code trong `GameCanvas.java`

<pre>
  public GameCanvas() {
    ...
    <s>e = new Enemy();</s>
    <b>e = new Enemy(170, 0);</b>
    ...
  }
</pre>

3. Chạy để kiểm tra các chức năng đã thực hiện vẫn còn hoạt động

![Constructor enemy player](images\constructor_enemy_player\constructor_enemy.gif)

4. Viết hàm tạo cho class `Player`

<pre>
public class Player {
    int x;<s> = 170;</s>
    int y;<s> = 500</s>
    BufferedImage image;
    
    Player() {
        x = 170;
        y = 500;
    }
</pre>

Chú ý: Khác với `Enemy`, khi mà các đối tượng của class này có thể xuất hiện trên nhiều điểm khác nhau trên màn hình, nên cần hàm tạo có tham số `xStart`, `yStart` để cho phép người lập trình tạo ra các `Enemy` với tọa độ xuất hiện tùy ý, `Player` chỉ có 1 đối tượng và hiện tại chỉ cần xuất hiện trên đúng 1 điểm của màn hình, nên không cần các tham số đầu vào mà có thể gán thẳng `x`, `y` bên trong hàm tạo

5. Do hàm tạo của Player ở GameCanvas vốn là hàm tạo không tham số từ đầu, nên không cần điều chỉnh gì cả

<pre>
    public GameCanvas() {
      ...
      p = new Player();
      ...
    }
</pre>

6. Chạy để kiểm tra các chức năng đã thực hiện vẫn còn hoạt động