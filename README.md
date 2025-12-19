## Tổng quan đồ án
Đồ án cuối kì này được thực hiện nhằm mục đích thực hành trọn vẹn quy trình Khoa học Dữ liệu (Data Science Workflow), từ việc tiếp cận nguồn dữ liệu thô đến việc trích xuất các thông tin giá trị (insights).

Sử dụng bộ dữ liệu **Data Science Salaries 2025**, nhóm tập trung phân tích toàn cảnh thị trường lao động ngành dữ liệu trong giai đoạn 2020 - 2025, mục tiêu là đề xây dựng một những câu hỏi thực tế, có giá trị xoay quanh các vấn đề nóng hổi: tác động thực sự của **làn sóng AI (ChatGPT)**, mối tương quan giữa **lương và lạm phát**, cũng như bài toán **so sánh sức mua (PPP)** giữa các quốc gia, và đưa ra kết luận cho các câu hỏi đó.

Kết quả nghiên cứu sẽ cung cấp góc nhìn chiến lược, giúp nhân sự ngành Data định hướng lộ trình học tập và tối đa hóa thu nhập trong 3 năm tới.

---

## Thông tin thành viên
| Họ và Tên | MSSV | Email |
|:---|:---:|:---|
| **Trần Phụng Đình** | 23127527 | tpdinh23@clc.fitus.edu.vn |
| **Nguyễn Đồng Thanh** | 23127538 | ndthanh23@clc.fitus.edu.vn |

---

## Nguồn dữ liệu và mô tả
* **Tên dataset:** Data Science Salaries 2025
* **Link dataset:** [Data Science Salaries 2025 - Kaggle](https://www.kaggle.com/datasets/arnabchaki/data-science-salaries-2025)

### Mô tả chi tiết:
* **Mô tả dữ liệu:** Dataset này tập trung vào mức lương và Xu hướng việc làm trong ngành Khoa học Dữ liệu (Data Science) trên quy mô toàn cầu từ năm 2020-2025.
* **Tác giả/Tổ chức:** Tác giả trên Kaggle là Arnab Chaki. Tuy nhiên, dữ liệu gốc thường được tổng hợp từ nền tảng **aijobs.net** - một trang web chuyên về tuyển dụng và minh bạch mức lương trong ngành AI/Big Data.
* **Thời gian công bố/thu thập:** Dữ liệu bao gồm các bản ghi từ năm 2020 và được cập nhật liên tục, phiên bản mới nhất được cập nhật **11/4/2025**.
* **Giấy phép:** CC0: Public Domain.
> *Chi tiết xem thêm ở file `notebooks/01_data_collection.ipynb`*

---

## Danh sách câu hỏi nghiên cứu
1.  **Câu hỏi 1:** Lương ngành Data tăng là do giá trị thật hay do lạm phát? 
2.  **Câu hỏi 2:** Cơn sốt AI (ChatGPT bùng nổ cuối 2022) tác động thế nào đến cấu trúc lương ngành Data?
3.  **Câu hỏi 3:** So sánh sức mua (PPP): Lương $15k ở Châu Á có 'nghèo' hơn $100k ở Mỹ?
4.  **Câu hỏi 4:** Nên học gì và chọn nước nào để tối đa hóa lương trong 3 năm tới?

---

## Tóm tắt kết quả chính
* **Thị trường:** Dữ liệu bị chi phối mạnh mẽ bởi thị trường **Mỹ (US)** (~84%) và hình thức làm việc **Full-time** (~99%).
* **Lương & Kinh nghiệm:** Có mối quan hệ thuận chiều rõ rệt. Nhóm **Senior (SE)** chiếm đa số và có mức lương ổn định, trong khi nhóm **Executive (EX)** có mức lương (trung vị) vượt trội.
* **Nghề nghiệp:** **Data Scientist, Data Engineer, Data Analyst** là 3 trụ cột chính (chiếm số lượng đông trong khảo sát). Tuy nhiên, các vị trí liên quan đến **AI/Machine Learning** và **Quản lý (Manager)** mới là vị trí đang dẫn đầu về đãi ngộ.
* **Xu hướng lương:** Mức lương trung bình ngành có xu hướng tăng trưởng mạnh qua các năm (2020-2024), nhưng đang có dấu hiệu đi ngang (bão hòa) vào giai đoạn 2024-2025.
* **Làm việc từ xa (Remote Work):** Có một sự bất ngờ thú vị khi mức lương trung vị của nhóm **Remote (100%)** và **On-site (0%)** là **tương đương nhau** (~$140k). Điều này bác bỏ quan điểm cho rằng "làm việc từ xa sẽ bị giảm lương". Tuy nhiên, **Hybrid (50%)** lại có mức lương thấp nhất trong tập dữ liệu này.
* **Tính linh hoạt theo hợp đồng:** Nhân sự **Freelance (FL)** có tỷ lệ làm việc từ xa cao nhất (~62%), trong khi nhân viên **Full-time (FT)** vẫn bị gắn chặt với văn phòng nhiều hơn (75% là On-site).

> *Chi tiết được trình bày trong file `notebooks/02_general_eda.ipynb`*

---

## Cấu trúc thư mục
| Đường dẫn | Nội dung |
|---|---|
| `data/` | Chứa các file CSV: dữ liệu gốc, dữ liệu trung gian sau xử lý, và các file kết quả dự đoán demo. |
| `notebooks/` | Các notebook theo từng bước workflow (01 → 05) để tái lập toàn bộ phân tích/mô hình. |
| `requirements.txt` | Danh sách thư viện Python cần thiết để chạy project. |
| `summary.md` | Báo cáo tổng kết & phản ánh cá nhân (template). |
| `LICENSE` | Giấy phép của repo. |
| `venv/` | Môi trường ảo (nếu có; không bắt buộc). |

Luồng dữ liệu chính (input/output):
- Input EDA: `data/original_data.csv`
- Output EDA (drop duplicates): `data/drop_dup_data.csv`
- Output preprocessing/split:
	- `data/train_hypo_1.csv`, `data/test_hypo_1.csv`
	- `data/train_hypo_2.csv`, `data/test_hypo_2.csv`
- Demo features & dự đoán:
	- `data/demo_X_h1.csv`, `data/demo_X_h2.csv`
	- `data/demo_preds_lr.csv`
	- `data/demo_preds_xgb_baseline.csv`, `data/demo_preds_xgb_tuned.csv`, `data/demo_preds_xgb_compare.csv`

---

## Hướng dẫn chạy
Yêu cầu: Python 3.x và `pip`. Để chạy notebook cần Jupyter (Notebook/Lab).

### 1) Tạo môi trường ảo + cài thư viện
Chạy tại thư mục gốc repo:
- `python -m venv .venv`
- PowerShell: `\.\.venv\Scripts\Activate.ps1`
- CMD: `\.\.venv\Scripts\activate`
- `python -m pip install -r requirements.txt`

### 2) Cài bổ sung nếu thiếu (chỉ khi gặp lỗi)
- Jupyter: `python -m pip install notebook` (hoặc `python -m pip install jupyterlab`)
- XGBoost (do notebook 05 dùng): `python -m pip install xgboost`

### 3) Mở Jupyter đúng thư mục để không lỗi đường dẫn
Do các notebook thường dùng đường dẫn dạng `../data/...`, nên khuyến nghị mở Jupyter từ thư mục `notebooks/`:
- `cd notebooks`
- `jupyter lab` (hoặc `jupyter notebook`)

### 4) Chạy notebooks theo thứ tự khuyến nghị
- `01_data_collection.ipynb`: mô tả nguồn dữ liệu & giấy phép (không bắt buộc để chạy pipeline).
- `02_general_eda.ipynb`: đọc `data/original_data.csv` và xuất `data/drop_dup_data.csv`.
- `03Dinh_data_ques.ipynb` + `03Thanh_data_ques.ipynb`: phân tích/câu hỏi dựa trên `data/drop_dup_data.csv`.
- `04_preprocessing_feature_modeling.ipynb`: tạo feature + chia train/test và lưu các file `train/test_hypo_*.csv` vào `data/`.
- `05_regression_model.ipynb`: train & đánh giá Linear Regression + XGBoost, đồng thời xuất các file demo dự đoán vào `data/`.

Ghi chú: Repo đã có sẵn các file trung gian/kết quả trong `data/`, nên bạn có thể chạy thẳng notebook 05 nếu không cần tái tạo toàn bộ pipeline.

---

## Danh sách thư viện yêu cầu

> *Được liệt kê chi tiết trong `requirements.txt`*


