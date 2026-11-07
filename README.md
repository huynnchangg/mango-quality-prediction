# Mango Quality Prediction — Data → ML Pipeline

Nghiên cứu: **Dự đoán sự suy giảm chất lượng và thời hạn sử dụng còn lại của xoài từ lịch sử phơi nhiễm trong chuỗi cung ứng lạnh**.

## Quick start

1. Clone repository.
2. Tạo môi trường Python 3.10+.
3. Cài dependencies: `pip install -r requirements.txt`.
4. Giải nén dataset gốc vào `data/raw/` sao cho `data/raw/0_README.txt` tồn tại.
5. Mở `notebooks/mango_data_ml_pipeline_stage_1_10.ipynb`, chạy từ đầu đến cuối.
6. Xem kết quả trong `outputs/`.

Có thể đặt đường dẫn dữ liệu khác bằng biến môi trường `MANGO_DATA_RAW`.

## Pipeline

Stage 1 Inventory → Stage 2 Data understanding → Stage 3 Cleaning → Stage 4 Trajectory → Stage 5 Matching → Stage 6 Features → Stage 7 Targets → Stage 8 Leakage prevention → Stage 9 EDA → Stage 10 Freeze.

## Data governance

Không commit dataset gốc, thông tin cá nhân hoặc file lớn lên repository công khai nếu chưa kiểm tra giấy phép. Giữ nguyên cấu trúc dataset gốc trong `data/raw/`.

## Important scientific notes

- `T_mangoes` is retained as the source variable name; physical placement must be confirmed from the dataset protocol before interpreting it as fruit surface/core temperature.
- Sensor logger serial IDs are not fabricated. `sensor_file_id` is a logical file identifier only.
- Timestamps have no explicit timezone in the supplied text files; they remain naive local timestamps.
- Chilling/heat thresholds are configurable and unset by default.
- CNN embeddings and Remaining Shelf Life (RSL) are not fabricated in this preprocessing notebook; they require a validated model and quality acceptance threshold.

## Outputs

Generated tables, figures, reports and processed datasets are written to `outputs/`. See the final notebook section for the full list.
