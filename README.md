# CNTT1-K-N-ng-Promting-v-i-AI-Session03_BTTH6
### 1. Mẫu Prompt theo khung CREATE


[C - Context]
Phòng đào tạo nhận danh sách sinh viên từ nhiều nguồn khác nhau nhưng định dạng họ tên, email và trạng thái học tập chưa đồng nhất. Dữ liệu này cần được làm sạch trước khi đưa lên hệ thống quản lý.

[R - Role & Request]
Đóng vai nhân viên xử lý dữ liệu đào tạo, hãy đọc danh sách sinh viên bên dưới, chuẩn hóa thông tin và chuyển đổi sang định dạng JSON.

[E - Explicit Constraints]
Dữ liệu đầu vào:
Nguyễn Văn An - an.nguyen@gmail.com - đang học
Trần Thị Bình - binhtt@gmail.com - bảo lưu
Lê Hoàng Nam - nam.le@gmail.com - đang học
Phạm Minh Đức - duc.pham@gmail.com - nghỉ học

Quy tắc chuẩn hóa:
- fullName: Họ và tên.
- email: Địa chỉ email.
- status: Chỉ nhận một trong ba giá trị: "đang học", "bảo lưu", "nghỉ học".
- Không tự ý thêm thông tin bên ngoài.
- Giữ nguyên đủ số lượng bản ghi, không làm sót dữ liệu.
- Nếu thông tin nào thiếu hoặc không xác định được thì điền "UNKNOWN".

[A - Action]
1. Tách thông tin từng sinh viên từ dữ liệu đầu vào.
2. Chuẩn hóa trường status theo đúng 3 giá trị quy định.
3. Kiểm tra lại tổng số bản ghi đã xử lý so với bản gốc.
4. Xuất dữ liệu theo đúng cấu trúc JSON yêu cầu.

[T - Target]
Chỉ xuất ra duy nhất JSON thô, không dùng dấu ```json hay khối mã Markdown, không viết thêm lời giải thích bên ngoài.

Cấu trúc bắt buộc:
{
  "students": [
    {
      "fullName": "Nguyễn Văn An",
      "email": "an.nguyen@gmail.com",
      "status": "đang học"
    }
  ],
  "totalRecords": 4
}

[E - Evaluation]
Chuỗi JSON phải đúng cú pháp, không chứa văn bản thừa và số lượng phần tử trong mảng students phải khớp với totalRecords.


### 2. Kết quả đầu ra (Raw JSON)


{

"students": [

{

"fullName": "Nguyễn Văn An",

"email": "an.nguyen@gmail.com",

"status": "đang học"

},

{

"fullName": "Trần Thị Bình",

"email": "binhtt@gmail.com",

"status": "bảo lưu"

},

{

"fullName": "Lê Hoàng Nam",

"email": "nam.le@gmail.com",

"status": "đang học"

},

{

"fullName": "Phạm Minh Đức",

"email": "duc.pham@gmail.com",

"status": "nghỉ học"

}

],
"totalRecords": 4
}
