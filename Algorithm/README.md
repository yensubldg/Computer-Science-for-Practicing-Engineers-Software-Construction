# Algorithm (Thuật toán)

### Định nghĩa

- Tập câu lệnh (hay chỉ thị) xác định, có thứ tự nhằm giải bài toán đặt ra.

### Các tính chất của thuật toán

| Tính chất     | Nội dung                                                                                                                                              |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Tính đúng     | Thuật toán phải giải được bài toán đặt ra                                                                                                             |
| Tính dừng     | Thuật toán phải dừng sau một số `hữu hạn` các bước                                                                                                    |
| Tính xác định | Các bước của thuật toán phải rõ ràng, xác định. Với một giá trị đầu vào, nếu thực hiện đúng theo các bước của thuật toán thì ta có duy nhất 1 đầu ra. |
| Tính phổ quát | Khi xây dựng thuật toán phải giải cho 1 lớp các bài toán (ví dụ giải phương trình bậc 2 có thể giải cho bất kỳ phương trình bậc 2 nào)                |

### Đánh giá thuật toán

- Một bài toán (problem) có thể có nhiều cách giải khác nhau. Để so sánh giữa các cách giải ta thường dựa vào độ phức tạp của thuật toán.

# Algorithm Complexity (Độ phức tạp của Thuật toán)

- Độ phức tạp theo không gian: Số ô nhớ cần thiết để thuật toán có thể thực hiện được.
- Độ phức tạp theo thời gian: Thời gian thực hiện xong các lệnh và trả về kết quả kể từ lúc nhận dữ liệu vào.

Thông thường khi nói đến độ phức tạp của thuật toán ta chỉ nói đến độ phức tạp theo thời gian.

Ký hiệu độ phức tạp là `T(n)` với n là kích thước dữ liệu.

Nếu kích thước dữ liệu càng lớn thì thời gian thực hiện thuật toán để trả về kết quả càng lớn `(Không tỉ lệ thuận)`.

### Các nguyên lý xác định độ phức tạp

#### Nguyên lý cộng

Nếu công việc `A` được chia làm hai công việc con rời nhau `A1` và `A2` , trong đó công việc `A1` có độ phức tạp `f1(n)`, công việc `A2` có độ phức tạp `f2(n)` thì độ phức tạp của công việc `A` là `f1(n) + f2(n)`.

Dùng ký pháp O (BigO) `(1)`

```
T(n) = O(f1(n) + f2(n)) = O(max(f1(n), f2(n)))
```

Ví dụ: Sắp xếp mảng n phần tử theo thuật toán sắp xếp nổi bọt rồi in ra.

- Sắp xếp: O(n^2)
- In ra: O(n)

Độ phức tạp của thuật toán là

```
T(n) = O(n^2) + O(n) = O(max(n^2, n)) = O(n^2)
```

#### Nguyên lý nhân

Nếu công việc `A` có `f1(n)` lần gọi hàm `X`, trong đó hàm `X` có độ phức tạp là `g(n)` thì độ phức tạp của công việc `A` là `f1(n) * g(n)`

```
T(n) = O(f1(n) * g(n))
```

### So sánh hai thuật toán

Khi so sánh hai thuật toán thì ta bỏ qua các yếu tố như sau:

- Ngôn ngữ lập trình (Programming Language): C, C++, Java, Python, ...
- Yếu tố phần cứng (Hardware) : CPU, RAM, HDD, SSD, ...
- Kỹ thuật cài đặt thuật toán (Setup): Cài đặt thuật toán trên máy tính, cài đặt thuật toán trên máy chủ, ...
- Vào ra dữ liệu (Input/Output): In ra màn hình, ghi file, ...
- Hệ điều hành (Operating System): Windows, Linux, MacOS, ...

# Ký hiệu

(1) `BigO`: Độ phức tạp thời gian `BigO` (Big O notation) thể hiện sự thay đổi của độ phức tạp thời gian phụ thuộc vào sự thay đổi của dữ liệu đầu vào.
