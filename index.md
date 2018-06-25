
## Coding convention

### 4 Principles of Simple Design (4 nguyên lý để có đoạn code đơn giản, dễ đọc, dễ hiểu)

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

### Nguyên tắc comit 

1. Commit luôn là workable code, tức là lấy bất kỳ revision nào cũng phải build và chạy được ứng dụng.

2. Commit nhỏ gọn, nhằm mục đích dễ tự review và người khác review, nếu xây dựng tính năng mới thì nên chia thành nhiều commit nhỏ.

3. Tránh commit chung nhiều task với nhau, khi cần revert rất khó xử lý.

4. Luôn luôn tự review tất cả những thay đổi trước khi commit, tự review sẽ giúp phát hiện những thay đổi không cần thiết, những lỗi logic cơ bản.

5. Viết commit message bao gồm thông tin thay đổi và link task (nếu có)

### Useful shortcuts for Android Studio

[Link 1](https://tech.fleka.me/android-shortcuts-and-tricks-to-boost-up-your-productivity-944548174582)

[Link 2](https://mmbs.github.io/tools/ide/2016/11/07/android-studio-tips-tricks/)

### Kotlin Clean Code

[https://blog.philipphauer.de/clean-code-kotlin/](https://blog.philipphauer.de/clean-code-kotlin/)

Kotlin style

[https://android.github.io/kotlin-guides/style.html](https://android.github.io/kotlin-guides/style.html)

## Tham khảo
- [CodePath android guides](https://github.com/codepath/android_guides/wiki)

- [Android best practices](https://github.com/futurice/android-best-practices)
