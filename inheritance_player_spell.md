## TechKids - Code Intensive - Hướng dẫn thực hành
### Áp dụng kế thừa vào `Player` và `PlayerSpell`

1. Mở file Player.java, cho class Player kế thừa (extends) từ GameObject, đồng thời xóa đi những thuộc tính và phương thức mà Player được thừa hưởng từ GameObject

<pre>

public class Player <b>extends GameObject</b> {
  <s>int x = 170;</s>
  <s>int y = 500;</s>
  <s>BufferedImage image;</s>
  ...
  <s>void paint(Graphics g) {</s>
      <s>g.drawImage(image, x, y, null);</s>
  <s>}</s>
  ...
}
</pre>

2. Chạy thử để đảm bảo các chức năng đã thực hiện vẫn hoạt động

3. Mở file PlayerSpell.java, cho class PlayerSpell kế thừa (extends) từ GameObject, đồng thời, giống với Player, xóa đi những thuộc tính và phương thức mà PlayerSpell được thừa hưởng từ GameObject

<pre>

public class PlayerSpell <b>extends GameObject</b> {
  <s>int x;</s>
  <s>int y;</s>
  <s>BufferedImage image;</s>
  ...
  <s>void paint(Graphics g) {</s>
      <s>g.drawImage(image, x, y, null);</s>
  <s>}</s>
  ...
}
</pre>

4. Chạy thử để đảm bảo các chức năng đã thực hiện vẫn hoạt động