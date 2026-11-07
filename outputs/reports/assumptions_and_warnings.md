# Assumptions and unresolved items

- Chưa cấu hình chilling injury threshold; degree-hours đang để NaN.
- Chưa cấu hình heat stress threshold; degree-hours đang để NaN.
- Timezone của timestamp chưa được xác nhận; đang giữ local-naive datetime.
- T_mangoes được giữ theo tên cột; vị trí logger cần xác minh bằng protocol gốc trước khi gọi là surface/core temperature.
- CNN embedding z in R^16 chưa được tạo; cần huấn luyện 1D-CNN ở modeling stage.
- RSL chưa được tính: cần định nghĩa ngưỡng chất lượng chấp nhận được và mô hình dự báo suy giảm theo thời gian.
