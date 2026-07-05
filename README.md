# iLearnHTML
A HTML note about some simple HTML description to understand
---
# Kiến thức HTML & CSS Cơ Bản

## PHẦN 1: HTML (Cấu trúc giao diện)

### 1. Cấu trúc một file HTML chuẩn
Các thẻ được sắp xếp theo đúng thứ tự phân cấp từ ngoài vào trong của một trình duyệt:

*   `<!DOCTYPE html>`: Khai báo với trình duyệt đây là file HTML5 để hiển thị cho đẹp và chuẩn.
*   `<html lang="vi">`: Thẻ cha bao bọc toàn bộ trang web, thiết lập ngôn ngữ hiển thị chính là tiếng Việt.
*   `<head>`: Vùng chứa các khai báo cấu hình hệ thống trên tab trình duyệt (người dùng không thấy trực tiếp trên trang).
    *   `<meta charset="UTF-8">`: Cấu hình phông tiếng Việt giúp trang web không bị lỗi font.
    *   `<title></title>`: Tiêu đề hiển thị của trang web trên tab trình duyệt.
    *   `<link rel="stylesheet" href="style.css">`: Nhúng (link) file CSS bên ngoài vào để làm đẹp cho HTML.
*   `<body>`: Nơi chứa toàn bộ nội dung hiển thị của trang web (chữ, hình ảnh, video...).

---

### 2. Các thẻ nội dung cơ bản
*   **Tiêu đề (Headings):** Sử dụng các thẻ từ `<h1>` (to nhất, quan trọng nhất) giảm dần đến `<h6>` (nhỏ nhất).
*   **Đoạn văn:** Thẻ `<p></p>` dùng cho các đoạn văn bản thông thường.
*   **Liên kết (Hyperlink):** Thẻ `<a href="đường_dẫn">Tên hiển thị</a>`.
    *   *Ví dụ:* `<a href="https://www.linux.org/pages/download/">Linux distro</a>`
*   **Hình ảnh:** Thẻ `<img src="đường_dẫn_ảnh" alt="chữ_thay_thế">` (Thẻ đơn, không có thẻ đóng).
    *   *Thuộc tính `alt`:* Hiển thị văn bản thay thế nếu hình ảnh bị lỗi hoặc không load được.
    *   *Ví dụ:* `<img src="https://www.toilet.boncau/cbd.png" alt="Toilet image">`
*   **Danh sách không thứ tự (Unordered List):** Cặp thẻ `<ul>` để bắt đầu danh sách, bên trong **chỉ được chứa** các thẻ con `<li>`.
*   **Thẻ bọc Khối:** Thẻ `<div></div>` đóng vai trò như một cái thùng gom tất cả nội dung liên quan lại thành một khối để dễ quản lý và căn chỉnh CSS.

---

### 3. Biểu mẫu (Form & Input)
*   `<form></form>`: Thẻ dùng để gom các thành phần nhập liệu (`input`, `label`, `button`) lại với nhau để gửi dữ liệu.
*   `<label></label>`: Thẻ ghi chú để người dùng biết ô đó dùng để nhập gì (thường đặt trước `input`).
*   `<br>`: Lệnh xuống dòng (vì mặc định các thẻ `input` sẽ tự động đứng sát nhau trên cùng một hàng).

#### Thuộc tính kết nối Label và Input
Dùng thuộc tính `for` của thẻ `label` bằng với thuộc tính `id` của thẻ `input` để kết nối chúng lại với nhau. Khi người dùng click vào chữ của label, con trỏ chuột sẽ tự động nhảy vào ô input.
*   *Ví dụ:* `<label for="txt">Tên đăng nhập</label> <input id="txt" type="text">`

#### Các kiểu hiển thị của dữ liệu nhập (`type` của `input`)
| Loại Type | Chức năng | Thuộc tính bổ trợ kèm theo |
| :--- | :--- | :--- |
| `type="text"` | Nhập chữ, văn bản bình thường. | `placeholder`: Hiện chữ mờ hướng dẫn trong ô nhập, khi gõ sẽ tự biến mất. |
| `type="password"` | Tự động ẩn các ký tự vừa gõ (biến thành dấu chấm đen). | |
| `type="email"` | Bắt buộc người dùng nhập đúng định dạng email (có đuôi `@...`). | |
| `type="checkbox"` | Tạo ô tick chọn vuông (có thể chọn nhiều ô). | |
| `type="submit"` | Biến input thành một nút bấm để gửi dữ liệu trong form đi. | |

#### Thẻ nút bấm (`<button>`)
*   `type="submit"`: Chức năng gửi dữ liệu trong form đi (giống input submit).
*   `type="button"`: Tạo nút bấm thông thường, thường dùng khi muốn nhúng JavaScript vào để xử lý sự kiện.

---
---

## PHẦN 2: CSS (Định dạng giao diện)

### 1. Cách nhúng & Bộ chọn (Selectors)
*   **Cách nhúng:** Viết các đoạn mã CSS bên trong cặp thẻ `<style></style>` đặt tại phần `<head>` của file HTML (hoặc viết ở file `.css` riêng).
*   **Bộ chọn theo Class:** Ký hiệu bằng dấu chấm `.` (Ví dụ: `.ten-lop {}`).
*   **Bộ chọn theo ID:** Ký hiệu bằng dấu thăng `#` (Ví dụ: `#ten-id {}`).
*   **Gom nhóm nhiều thẻ:** Nếu nhiều thẻ có chung một thuộc tính CSS, viết liên tiếp và cách nhau bằng dấu phẩy `,`.
    *   *Ví dụ:* `h1, p, li, ul { color: red; }`

---

### 2. Thuộc tính Màu sắc & Chữ
*   `color`: Đổi màu chữ.
*   `background-color`: Đổi màu nền.
*   `font-size`: Chỉnh cỡ chữ (Ví dụ: `20px`).
*   `font-weight`: Chỉnh độ đậm nhạt của chữ (Ví dụ: `bold`, `400`, `700`).
*   `text-align`: Căn lề cho chữ (`left` / `right` / `center` / `justify`).

---

### 3. Kích thước & Đường viền
*   `width` / `height`: Chiều rộng / chiều cao của vật thể. Tính bằng đơn vị `px` (cố định) hoặc `%` (tỷ lệ theo màn hình/khối cha).
*   `border`: Tạo đường viền bao quanh khối. 
    *   *Cú pháp gộp nhanh:* `border: [độ dày] [kiểu viền] [màu sắc];` (Ví dụ: `border: 1px solid red;`).

Các kiểu viền (`border-style`) phổ biến:
*   `solid`: Đường kẻ liền (Phổ biến nhất).
*   `dashed`: Kẻ đứt quãng (`---`).
*   `dotted`: Kẻ chấm bi (`......`).
*   `double`: Đường kẻ đôi.
*   `none`: Không có viền (thường dùng để xóa viền mặc định xấu xí của `button` hoặc `input`).

---

### 4. Mô hình hộp (Box Model)
Bố cục của mọi phần tử trên website đều được tính toán từ trong ra ngoài theo thứ tự sau:
1.  **Content (Nội dung):** Phần cốt lõi ở trong cùng chứa chữ hoặc hình ảnh.
2.  **Padding (Khoảng đệm):** Khoảng cách trống từ nội dung bên trong giãn ra đến đường viền.
3.  **Border (Đường viền):** Viền ngoài bao quanh phần padding.
4.  **Margin (Khoảng cách lề):** Khoảng cách trống từ viền của khối này đẩy ra đến viền của khối khác bên ngoài.

> **Mẹo viết nhanh thuộc tính `margin` hoặc `padding` theo chiều kim đồng hồ:**
> Nếu viết 4 thông số liên tiếp: `margin: [Trên] [Phải] [Dưới] [Trái];`

---

### 5. Khả năng hiển thị (Display)
Thuộc tính `display` dùng để quyết định cách một thẻ được dàn trận trên trang web:

*   `display: block` (Khối): Chiếm trọn vẹn 100% chiều ngang màn hình và bắt các thẻ đứng sau nó phải xuống hàng. Chỉnh được kích thước `width` và `height`. (Mặc định của thẻ `div`, `p`, `h1`...).
*   `display: inline` (Hàng): Chiếm vừa khít không gian của nội dung bên trong nó, các thẻ inline khác có thể đứng cạnh nhau trên cùng một hàng. **Không** chỉnh được `width` và `height`. (Mặc định của `<a>`, `<span>`...).
*   `display: inline-block` (Khối trên hàng): Kết hợp cả hai loại trên. Các thẻ có thể xếp hàng ngang cạnh nhau nhưng bạn vẫn thoải mái chỉnh được `width` và `height` cho chúng.
*   `display: none`: Ẩn hoàn toàn khối đó đi khỏi màn hình (biến mất hoàn toàn không để lại dấu vết).

---

### 6. Trạng thái chuột & Hiệu ứng chuyển động

#### Trạng thái chuột (Pseudo-classes)
*   `:hover`: Kích hoạt vùng CSS này khi người dùng di con trỏ chuột vào phần tử (ví dụ: đổi màu nút bấm khi rê chuột qua).
*   `:active`: Kích hoạt vùng CSS này tại đúng khoảnh khắc người dùng ấn giữ chuột xuống.

#### Chỉnh kiểu dáng con trỏ (`cursor`)
Dùng để thay đổi hình dáng con chuột khi rê vào phần tử để người dùng biết có tương tác được không:
*   `pointer`: Biến thành hình bàn tay chỉ ngón trỏ (báo hiệu chỗ này click vào được).
*   `not-allowed`: Biến thành hình vòng tròn đỏ gạch chéo (báo hiệu bị cấm/khóa, không ấn được).
*   `wait`: Biến thành hình vòng tròn xoay xoay / đồng hồ cát (báo hiệu đang tải - loading).
*   `text`: Biến thành hình chữ I (báo hiệu vùng này cho phép bôi đen chọn chữ).
*   `zoom-in` / `zoom-out`: Biến thành hình kính lúp cộng/trừ (thường dùng cho hình ảnh cần phóng to).

#### Biến đổi hình dáng (`transform`)
*   `scale(0.98)`: Thu nhỏ vật thể lại còn 98% kích thước gốc (hay dùng kết hợp với `:active` tạo hiệu ứng nút bị lún xuống khi bấm).
*   `rotate(45deg)`: Xoay vật thể một góc 45 độ.
*   `translateX(20px)`: Dịch chuyển vật thể sang bên phải 20 pixel theo trục ngang.

#### Hiệu ứng mượt mà (`transition`)
Giúp các thay đổi (như hover đổi màu, transform dịch chuyển) diễn ra mượt mà thay vì giật khựng lập tức.
*   *Cú pháp:* `transition: [thuộc tính] [thời gian] [kiểu chuyển động];`
*   *Thuộc tính áp dụng:* Dùng từ khóa `all` để áp dụng cho mọi thay đổi, hoặc chỉ định rõ một thuộc tính cụ thể (ví dụ: `background-color`).
*   *Thời gian:* Tính bằng giây (`0.2s`) hoặc mili-giây (`200ms`).

Các kiểu chuyển động phổ biến:
*   `ease`: Chạy chậm lúc đầu - tăng tốc ở giữa - chậm lại ở cuối (Mặc định).
*   `linear`: Chạy đều một tốc độ từ đầu đến cuối không thay đổi.
*   `ease-in`: Xuất phát chậm - sau đó nhanh dần lên.
*   `ease-out`: Xuất phát nhanh - sau đó chậm dần lại ở cuối.

---

### 7. Flexbox & Các tuyệt chiêu căn giữa bố cục
Flexbox giống như một loại ma thuật giúp dàn hàng và di chuyển các `div` con nằm bên trong một hộp cha.

#### Căn giữa cả một cụm khối con nằm trong hộp Flexbox
Viết các thuộc tính này vào **khối cha**:
```css
.hop-cha {
    display: flex;
    justify-content: center; /* Căn giữa các con theo chiều ngang */
    align-items: center;     /* Căn giữa các con theo chiều dọc */
}
```

#### Các trường hợp căn giữa khác:
*   **Căn giữa dòng chữ văn bản:** Viết `text-align: center;` vào **khối cha** chứa dòng chữ đó.
*   **Căn giữa một khối div độc lập:** Nếu khối div đó đã có kích thước `width` cố định, viết `margin: 0 auto;` vào **chính khối div đó** để nó tự căn đều lề trái phải dạt ra giữa trang.
