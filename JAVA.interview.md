## 📚 Flashcards Java Core – Phỏng vấn & Ôn tập

### ✨ Sử dụng cho học tập, phỏng vấn hoặc in ấn

---

### 1. Java là gì?

**Trả lời:**  
Java là một ngôn ngữ lập trình hướng đối tượng (OOP), mạnh mẽ, bảo mật cao, và đặc biệt là **đa nền tảng**. Java được phát triển bởi Sun Microsystems vào năm 1995 (hiện nay do Oracle duy trì).

**Tính năng chính:**

- Đa nền tảng (Write Once, Run Anywhere)
- Quản lý bộ nhớ tự động (Garbage Collection)
- Hỗ trợ lập trình đa luồng (Multithreading)
- Cộng đồng lớn và tài liệu phong phú

**Ví dụ ứng dụng:** Android, web server backend, hệ thống ngân hàng.

---

### 2. JVM là gì?

**Trả lời:**  
JVM (Java Virtual Machine) là một máy ảo để thực thi bytecode Java. Bytecode được sinh ra khi bạn biên dịch mã `.java` thành `.class`, và JVM sẽ đọc – hiểu – chạy nó.

**Chức năng chính:**

- Quản lý bộ nhớ (Heap, Stack)
- Garbage Collection
- Đảm bảo tính bảo mật và nền tảng độc lập

**Ví dụ:** Khi bạn chạy `java HelloWorld`, chính JVM chịu trách nhiệm chạy chương trình này.

---

### 3. JDK và JRE khác nhau thế nào?

**Trả lời:**

- **JDK (Java Development Kit):** Bộ công cụ để lập trình Java, bao gồm compiler, debugger, JRE và các tiện ích.
- **JRE (Java Runtime Environment):** Môi trường để chạy chương trình Java, bao gồm JVM và các thư viện cần thiết.

| Thành phần | Chức năng  | Bao gồm                       |
| ---------- | ---------- | ----------------------------- |
| JDK        | Phát triển | JRE, trình biên dịch, công cụ |
| JRE        | Chạy       | JVM, thư viện runtime         |

---

### 4. Overloading và Overriding khác nhau thế nào?

**Trả lời:**

- **Overloading (nạp chồng):** Cùng tên hàm, khác tham số. Xảy ra trong cùng 1 lớp.
- **Overriding (ghi đè):** Phương thức lớp con ghi đè phương thức của lớp cha. Phải đúng tên, tham số, và có annotation `@Override`.

**Ví dụ Overloading:**

```java
void say(String msg) {}
void say(String msg, int times) {}
```

**Ví dụ Overriding:**

```java
class A { void show() {} }
class B extends A { @Override void show() {} }
```

---

### 5. HashMap và Hashtable khác gì nhau?

**Trả lời:**  
| HashMap | Hashtable |
|----------------|--------------------|
| Không đồng bộ | Đồng bộ (thread-safe) |
| Cho phép `null` key/value | Không cho phép |
| Hiệu năng cao hơn | Chậm hơn trong môi trường nhiều luồng |

**Khuyến nghị:** Dùng `ConcurrentHashMap` thay vì `Hashtable` trong đa luồng.

---

### 6. final, finally, finalize khác nhau như thế nào?

**Trả lời:**

| Từ khóa      | Mục đích                                                                        |
| ------------ | ------------------------------------------------------------------------------- |
| `final`      | Khai báo hằng số, lớp không kế thừa, hàm không override                         |
| `finally`    | Khối mã luôn được thực thi sau try-catch                                        |
| `finalize()` | Hàm được gọi trước khi đối tượng bị xoá bởi GC (ít dùng, không khuyến nghị nữa) |

---

### 7. Checked và Unchecked Exception là gì?

**Trả lời:**

- **Checked Exception:** Bắt buộc phải xử lý (biên dịch sẽ lỗi nếu không try-catch). Ví dụ: `IOException`, `SQLException`
- **Unchecked Exception:** Không bắt buộc xử lý. Ví dụ: `NullPointerException`, `ArrayIndexOutOfBoundsException`

---

### 8. Garbage Collection trong Java là gì?

**Trả lời:**  
Garbage Collection (GC) là quá trình tự động thu hồi bộ nhớ của các đối tượng không còn được tham chiếu.

**Ưu điểm:**

- Tránh rò rỉ bộ nhớ
- Giúp lập trình viên không cần `free()` thủ công như C/C++

**GC hoạt động như thế nào?** JVM quét heap, tìm đối tượng không còn tham chiếu và loại bỏ chúng.

---

### 9. Abstract class và Interface khác nhau thế nào?

**Trả lời:**

| Abstract Class                       | Interface                                                            |
| ------------------------------------ | -------------------------------------------------------------------- |
| Có thể có biến và phương thức thường | Chỉ có hằng số và phương thức abstract (từ Java 8 có default method) |
| Hỗ trợ constructor                   | Không có constructor                                                 |
| Kế thừa 1 class                      | Implement nhiều interface                                            |

---

### 10. Thread là gì?

**Trả lời:**  
Thread là đơn vị thực thi độc lập trong chương trình Java. Java hỗ trợ tạo và chạy nhiều thread để thực hiện song song.

**Ví dụ:**

```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread chạy...");
    }
}
```

---

### 11. Sự khác biệt giữa ArrayList và LinkedList

**Trả lời:**

| ArrayList              | LinkedList                 |
| ---------------------- | -------------------------- |
| Truy cập nhanh (O(1))  | Truy cập chậm (O(n))       |
| Chèn/xoá chậm          | Chèn/xoá nhanh             |
| Sử dụng mảng bên trong | Sử dụng danh sách liên kết |

---

### 12. Sự khác biệt giữa equals() và ==

**Trả lời:**

- `==`: So sánh địa chỉ trong bộ nhớ (tham chiếu)
- `equals()`: So sánh giá trị nội dung của đối tượng (có thể override)

**Ví dụ:**

```java
String a = new String("abc");
String b = new String("abc");
a == b        // false
a.equals(b)   // true
```

---

### 13. static là gì trong Java?

**Trả lời:**  
Từ khóa `static` dùng để khai báo thành viên lớp mà không cần tạo đối tượng.

- Biến `static`: chia sẻ giữa mọi đối tượng
- Phương thức `static`: gọi mà không cần tạo đối tượng
- Khối `static`: khởi tạo một lần duy nhất khi lớp được load

---

### 14. StringBuffer và StringBuilder khác nhau thế nào?

**Trả lời:**

| StringBuffer          | StringBuilder                 |
| --------------------- | ----------------------------- |
| Thread-safe (đồng bộ) | Không thread-safe (nhanh hơn) |
| Chậm hơn              | Nhanh hơn                     |

---

### 15. Tại sao String là immutable?

**Trả lời:**

- Bảo mật (dùng làm key trong HashMap, kết nối DB)
- Thread-safe tự nhiên
- Cache hiệu quả hơn (String Pool)

---

### 16. Serialization là gì?

**Trả lời:**  
Serialization là quá trình chuyển đối tượng thành dạng byte để lưu trữ hoặc truyền qua mạng.

**Từ khóa cần dùng:** `implements Serializable`

---

### 17. Java có hỗ trợ đa kế thừa không?

**Trả lời:**  
Không, Java không hỗ trợ đa kế thừa bằng class để tránh xung đột. Nhưng có thể dùng nhiều interface (đa kế thừa logic).

---

### 18. ClassLoader là gì?

**Trả lời:**  
ClassLoader là thành phần của JVM, dùng để nạp class vào bộ nhớ khi chương trình chạy.

Các loại chính:

- Bootstrap
- Extension
- System ClassLoader

---

### 19. Từ khóa `this` là gì?

**Trả lời:**  
`this` dùng để tham chiếu đến đối tượng hiện tại trong class.

**Dùng trong:**

- Phân biệt biến instance với biến local
- Gọi constructor khác trong cùng class
- Truyền chính nó làm đối số

---

### 20. Từ khóa `super` dùng để làm gì?

**Trả lời:**  
`super` dùng để gọi constructor hoặc phương thức của lớp cha.

**Ví dụ:**

```java
class A {
    void show() { System.out.println("A"); }
}
class B extends A {
    void show() {
        super.show(); // gọi lớp cha
        System.out.println("B");
    }
}
```
