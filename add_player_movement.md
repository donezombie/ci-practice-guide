## TechKids - Code Intensive - Hướng dẫn thực hành
### Thêm di chuyển cho nhân vật

1. Mở file `GameCanvas.java`

2. Thực hiện bắt sự kiện phím bấm của người chơi bằng cách gọi hàm `addKeyListener()`

3. Hàm này sẽ yêu cầu một tham số, có kiểu là `KeyListener`

4. Cung cấp tham só này cho hàm `addKeyListener()` bằng cách khởi tạo một KeyListener làm tham số đầu vào

5. `KeyListener`, cũng giống như `WindowListener`, được sinh ra để giúp người lập trình thêm vào các thao tác xử lý sự kiện của mình, sau đó được gắn vào nơi sẽ xảy ra sự kiện là `GameCanvas` thông qua hàm `addKeyListener()`

6. Khi được `IntelliJ` gợi ý điền nốt, chọn vào `new KeyListener()` rồi nhấn `ENTER` để `IntellIJ` hoàn thành toàn bộ khai báo của tham số này

7. Trong các hàm được cung cấp, có `onKeyDown()` và `onKeyUp()` sẽ được quan tâm

8. Thực hiện log (in ra cửa sổ run) trong hai hàm này với nội chính là tên hàm

9. Chạy chương trình

10. Thực hiện nhấn các phím, đặc biệt là các phím sẽ được sử dụng là các phím mũi tên lên &uarr;, xuống &darr;, trái &larr;, phải &rarr;

11. Sau khi nhấn thử vài phím, có các quan sát như sau:
* Khi một phím được nhấn xuống, `onKeyDown()` sẽ được gọi
* Khi nhả phím đó ra (không nhấn nữa), `onKeyUp()` sẽ được gọi
* Với một lần thử, tính từ lúc nhấn phím cho đến lúc nhả phím, có thể `onKeyDown()` được gọi nhiều lần nhưn `onKeyUp()` chỉ được gọi một lần duy nhất

12. 