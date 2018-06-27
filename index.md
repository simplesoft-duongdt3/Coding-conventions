Topics:
1. [4 Principles of Simple Design (4 nguyên lý để có đoạn code đơn giản, dễ đọc, dễ hiểu)](#anchor_principles_of_simple_design)
2. [Nguyên tắc comit](#anchor_commit_rule)
3. [Tips Clean Code](#anchor_tip_clean_code)
4. [Useful shortcuts for Android Studio](#anchor_android_studio_shortcuts)

## Coding convention

### <a name="anchor_principles_of_simple_design"></a>4 Principles of Simple Design (4 nguyên lý để có đoạn code đơn giản, dễ đọc, dễ hiểu)

1. Keep it Small
  
  Viết hàm nhỏ, làm một việc để dễ review, dễ kiểm soát, giảm lỗi logic.
  
2. Minimize Duplication (Don't Repeat Yourself - DRY)
  
  Hạn chế trùng lặp, nếu phát hiện lặp nên tiến hành refactor thành class chung, hàm chung, biến chung...
  
3. Maximize Clarity
  
  Tên biến, tên hàm, tên lớp phải rõ ràng, chấp nhận tên dài để thể hiện hết ý nghĩa.
  Không có tạo sự bất ngờ khi viết hàm, tránh trường hợp thực thi những việc khác với tên hàm.

4. Runs all tests
  
  Mọi hàm phải được test để đảm bảo không tồn tại hàm không bao giờ được test. (có thể dùng Unit test)

[Ref link](https://www.theguild.nl/4-rules-of-simple-design/)

### <a name="anchor_commit_rule"></a>Nguyên tắc comit 

1. Commit luôn là workable code, tức là lấy bất kỳ revision nào cũng phải build và chạy được ứng dụng.

2. Commit nhỏ gọn, nhằm mục đích dễ tự review và người khác review, nếu xây dựng tính năng mới thì nên chia thành nhiều commit nhỏ.

3. Tránh commit chung nhiều task với nhau, khi cần revert rất khó xử lý.

4. Luôn luôn tự review tất cả những thay đổi trước khi commit, tự review sẽ giúp phát hiện những thay đổi không cần thiết, những lỗi logic cơ bản.

5. Viết commit message bao gồm thông tin thay đổi và link task (nếu có)

### <a name="anchor_tip_clean_code"></a>Tips Clean Code
1. Đặt tên hàm, biến sử dụng từ có nghĩa chung chung, na ná nhau, dễ nhầm lẫn (info, record, detail ...) làm tiền tố/hậu tố

```javascript
//WRONG
val customerInfo: Customer
val customerRecord: Customer

fun getCustomerInfo()
fun getCustomerDetail()
fun getCustomerRecord()
```

```javascript
//CORRECT
val selectedCustomer: Customer

fun getCustomer(): Customer
```
2. Đặt tên biến, hàm không rõ ràng, không thể hiện rõ mục đích sử dụng

```javascript
//WRONG
val days : Int

fun getItems(): List<Item>
```

```javascript
//CORRECT
val daysSinceCreation: Int
val durationInDays: Int

fun getRemovedItems(): List<Item>
```

3. Đặt tên biến, hàm bằng từ lóng, viết tắt (trừ những trường hợp từ viết tắt cực kỳ thông dụng)

```javascript
//WRONG
val modyddmmyy: Date
val uId: Long
```

```javascript
//CORRECT
val daysSinceCreation: Date
val userId: Long
```

4. Đặt tên hàm biến quá rõ ràng, gắn với loại dữ liệu, dài không cần thiết
vd: trường hợp thường gặp nhất là List, ArrayList thường thêm tiền tố List, nếu sau này đổi loại dự liệu thành Array thì tên sẽ không đồng nhất với kiểu dữ liệu, ta nên dùng dạng thêm s, es để biểu diễn số nhiều của biến/hàm.
```javascript
//WRONG
val clientList: List<Client>
```

```javascript
//CORRECT
val clients: List<Client>
val newClients: List<Client>
```

5. Đặt tên hàm biến ngắn, không rõ ràng, khó hiểu
Cố gắng đặt tên hàm và biến rõ ràng nhất có thể, chấp nhận tên dài, để người khác đọc code sẽ giảm bớt thời gian suy nghĩ, tăng tốc độ đọc code và dễ hiểu.

```javascript
//WRONG
fun count(l: List<Customer>)
```

```javascript
//CORRECT
fun countExpiredCustomer(customers: List<Customer>)
```

### <a name="anchor_android_studio_shortcuts"></a>Useful shortcuts for Android Studio

[Link 1](https://tech.fleka.me/android-shortcuts-and-tricks-to-boost-up-your-productivity-944548174582)

[Link 2](https://mmbs.github.io/tools/ide/2016/11/07/android-studio-tips-tricks/)

### Kotlin Clean Code

[https://blog.philipphauer.de/clean-code-kotlin/](https://blog.philipphauer.de/clean-code-kotlin/)

### Kotlin coding style

[https://android.github.io/kotlin-guides/style.html](https://android.github.io/kotlin-guides/style.html)

## Tham khảo
- [CodePath android guides](https://github.com/codepath/android_guides/wiki)

- [Android best practices](https://github.com/futurice/android-best-practices)
