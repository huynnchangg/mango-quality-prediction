# Kết quả chạy thử trên dataset đính kèm

Notebook đã được chạy end-to-end trên bản giải nén của `dataverse_files.zip`.

- Tổng file trong cây dữ liệu: 563.
- Sensor files theo từng chặng được đọc: 312 file (bao gồm các logger có dữ liệu theo chặng; file toàn trình `00_All_Recording...` không trộn vào trajectory chính).
- Số Box có trajectory: 31.
- Số dòng sensor sau làm sạch: 20,709.
- Số dòng timestamp lỗi: 0.
- Số dòng mass/weight sau melt: 280.
- Số dòng color sau chuẩn hóa: 414.
- Số Box có thể ghép sensor với quality trong bảng modeling: 5.
- Dataset CSV modeling thử nghiệm: 184 dòng.

**Trạng thái ở môi trường kiểm thử hiện tại:** Parquet chưa được tạo vì môi trường kiểm thử không có `pyarrow`; notebook đã xuất CSV thay thế. Cài `requirements.txt` (bao gồm `pyarrow`) và chạy lại để tạo Parquet.

**Lưu ý khoa học:** số Box overlap là 5, vừa đủ về mặt số lượng để GroupKFold(5) nếu các dòng target hợp lệ vẫn giữ được sau kiểm tra. Các ngưỡng chilling/heat chưa được cấu hình; CNN embedding và RSL chưa được tạo trong preprocessing. Vì vậy không xem CSV demo này là mô hình đã huấn luyện hoặc kết quả dự báo shelf-life.
