# Churn_prediction

Dự án phân tích và dự đoán khách hàng có khả năng rời bỏ (customer churn) dựa trên bộ dữ liệu thương mại điện tử Olist của Brazil.

Customer churn analysis and prediction using the Brazilian Olist e-commerce dataset, with data preprocessing, feature engineering, and machine learning.

## Cấu trúc thư mục

```text
ChurnProject/
├── archive/                  # Dữ liệu CSV gốc
├── data_preprocessing.ipynb  # Notebook tiền xử lý dữ liệu
├── requirements.txt          # Các thư viện Python
└── .venv/                    # Môi trường Python cục bộ, không commit
```

## Thiết lập môi trường

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

Để mở notebook:

```bash
jupyter lab
```

Trong Jupyter, chọn kernel `Python (ChurnProject)`.

## Dữ liệu

Thư mục `archive/` chứa dữ liệu về:

- khách hàng, đơn hàng và chi tiết sản phẩm trong đơn;
- thanh toán và đánh giá;
- sản phẩm, người bán và địa lý;
- bản dịch tên danh mục sản phẩm.

Khi xây dựng feature theo khách hàng, dùng `customer_unique_id` để nhận diện một khách hàng xuyên suốt nhiều đơn hàng. `customer_id` gắn với từng bản ghi khách hàng trong đơn hàng.

## Hướng phát triển

1. Đọc và kiểm tra chất lượng dữ liệu.
2. Kết hợp các bảng thành dữ liệu cấp khách hàng.
3. Xác định quy tắc churn và mốc thời gian quan sát.
4. Tạo feature về tần suất mua, giá trị đơn hàng, đánh giá và thời gian từ lần mua cuối.
5. Huấn luyện, đánh giá và diễn giải mô hình.

Notebook hiện là điểm bắt đầu cho bước tiền xử lý.
