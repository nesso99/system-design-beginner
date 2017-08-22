## Nguồn tham khảo dịch: Clean Code - Robert C.Martin

## Các định nghĩa code sạch (clean code)
* Bjarne Stroustrup: Tôi thích code của tôi phải thanh lịch và hiệu quả. Logic phải mạch lạc để khó có lỗi ẩn trong nó, các dependency nhỏ nhẹ và dễ bảo trì, xử lý lỗi hoàn chỉnh theo chiến lược khớp nối (articulated strategy), và hiệu năng gần đạt mức tối ưu để người khác không làm rối code với các việc tối ưu hóa vô kỷ luật. Làm code sạch là làm một điều tốt.

* Grady Booch: Code sạch là đơn giản và trực tiếp (direct). Làm code đọc dễ hiểu như văn viết. Code không bao giờ che dấu ý định của người thiết kế mà xa hơn là các trừu tượng rõ ràng và các luồng điều khiển mạch lạc.

## Đặt tên ngữ nghĩa (Meaningful Names)

**Phần này đã có bản dịch trên [http://tapchilaptrinh.vn](http://tapchilaptrinh.vn/2014/01/07/ma-sach-ten-co-y-nghia/) nhưng mình vẫn viết ngắn gọn theo ý của mình, kiểu như note lại**

### Đặt tên sao cho người đọc biết nó dùng để làm gì
Có thể mất thời gian để bạn đặt tên nhưng nó sẽ tiết kiệm rất nhiều thời gian của bạn sau này. Hãy cho người đọc code biết vì sao nó tồn tại

Bạn thích đọc đoạn code nào hơn?

```java
public List<int[]> getThem() {
    List<int[]> list1 = new ArrayList<int[]>();
    for (int[] x : theList)
    if (x[0] == 4)
    list1.add(x);
    return list1;
}
```

```java
public List<Cell> getFlaggedCells() {
    List<Cell> flaggedCells = new ArrayList<Cell>();
    for (Cell cell : gameBoard)
    if (cell.isFlagged())
    flaggedCells.add(cell);
    return flaggedCells;
}
```

### Tránh sử dụng các đoạn code gây nhầm lẫn, dư thừa
### Tạo sự khác biệt có ý nghĩa
### Sử dụng các tên có thể phát âm được
### Sử dụng các tên có thể tìm kiếm được
### Tránh dùng các kiểu mã hóa
#### Hungarian Notation
#### Thành phần tiền tố
#### Giao diện và cài đặt của nó

## Hàm (Functions)

### Nhỏ thôi!
### Do One Thing
### One level of abtraction per Function
### Switch statements
### Use Descriptive Names
### Function Arguments
### Have No Side Effects
### Command QUery Separation
### Prefer Exceptions to Returning Error code
### don't repeat yourself
### Structured Programming
### How do you write function like this
### Conclusion


