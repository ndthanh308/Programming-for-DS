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




# Báo cáo Tổng kết & Phản ánh Cá nhân (Individual Reflections)

---

## Thành viên 1: Trần Phụng Đình

### 1. Khó khăn & Thử thách 
**1. Rào cản về kiến thức nghiệp vụ (Domain knowledge)**  
Để có thể đi trả lời cho câu hỏi "Lương tăng do giá trị thật hay do lạm phát", em cần phải dành thời gian phân biệt rõ ràng giữa "Lương danh nghĩa" (Nominal Salary - con số trên hợp đồng) và "Lương thực tế" (Real Salary - sức mua sau lạm phát). Tìm hiều các nguồn ữ liệu CPI (Consumer Price Index) đáng tin cậy, khớp nối được với mốc thời gian (2022-2025) và phạm vi địa lý của dữ liệu lương.

**2. Sự mơ hồ trong phân loại gom nhóm Job Title"**  
Ở câu hỏi "Cơn sốt AI (ChatGPT bùng nổ cuối 2022) tác động thế nào đến cấu trúc lương ngành Data?", dữ liệu thô chứa hàng trăm `Job title` khác nhau (ví dụ: Principal Data Scientist vs AI Scientist). Ranh giới giữa một người làm Data Science thuần túy và một người làm AI/ML thường không rõ ràng, dẫn đến rủi ro phân loại sai. Giải pháp: các từ khóa đặc thù như "LLM", "Neural", "Deep Learning" được xét trước để tách nhóm AI, sau đó mới đến các từ khóa Data truyền thống.
    

### 2. Bài học & Phát triển 
**1. Bạn đã học được những gì?**
* **Ngữ cảnh, mối liên hệ theo thời gian có thể dùng để khai thác rất nhiều thông tin ý nghĩa.** Một con số Data Science đứng một mình không nói lên gì nhiều. Mức lương $160,000 năm 2025 không giống với $160,000 năm 2022. Việc kết hợp dữ liệu nội bộ (lương) với dữ liệu vĩ mô bên ngoài (CPI/Lạm phát) là bước ngoặt để tạo ra một phân tích có chiều sâu.

* **Kết hợp dữ liệu dataset với dữ liệu bên ngoài (external data) như CPI để tạo ra một phân tích toàn diện.** Việc chỉ nhìn vào con số lương tăng trưởng hàng năm là chưa đủ, cần phải liên hệ với các kiến thức nghiệp vụ, đặt nó vào bối cảnh sức mua thực tế để đánh giá đúng bản chất vấn đề.

**2. Điều gì làm bạn bất ngờ nhất?**
* **Bước tiền xử lí dữ liệu (Data Prprocessing) quyết định rất nhiều đến kết luận cuối cùng.** Khi lấy lương trung bình chung, nhóm ngành Data truyền thống có vẻ thấp bất thường. Tuy nhiên, khi nhìn sâu vào dữ liệu, vẽ biểu đồ phân phối Experience, em nhận thấy rằng nhóm Data có tỷ lệ nhân sự mức Junior/Entry-level cao hơn, kéo mức lương trung bình xuống thấp một cách không công bằng, nếu đem đi so với nhóm ngành AI/ML có nhiều Senior hơn. Nếu ở bước tiền xử lí mà em không cẩn thận xử lí dữ liệu thì kết quá phân tích và kết luận có thể sai lệch đi rất nhiều.

**3. Dự án này đã định hình cách hiểu của bạn về Data Science như thế nào?**
Dự án này giúp em nhận ra rằng cốt lõi của Data Science không chỉ là viết code hay vẽ biểu đồ, mà là **tư duy phản biện (Critical Thinking)**. Thay vì chấp nhận ngay kết quả "Lương tăng", em đã phải liên tục đặt ra các câu hỏi mở rộng vấn đề: "Tăng so với cái gì?", "Mức tăng này có bù được lạm phát không?", "Liệu có yếu tố ẩn nào (như remote work, lay-off) đang tác động không?". Chính việc không ngừng đặt câu hỏi "Tại sao?" và "Còn gì nữa không?" mới giúp tôi tìm ra insight giá trị nhất: Người lao động có thể đang "nghèo đi" ngay cả khi được tăng lương.

---

## Thành viên 2: Nguyễn Đồng Thanh

### 1. Khó khăn & Thử thách 

**1. Những trở ngại cụ thể đã gặp phải là gì?**
Đây là lần thứ hai em thực hiện khám phá và phân tích một dữ liệu ở trên Kaggle, nên cũng có phần quen và có chút kinh nghiệm về các bước thực hiện. Khó khăn duy nhất ở đây là thời gian hạn hẹp, lại có nhiều cách code cần phải học, nên em chỉ kịp đọc rồi áp dụng, không có thời gian đào sâu thêm để tối ưu code hay hiểu rõ về các hàm.

Ngoài ra tập dữ liệu này cũng khá “ảo” và em cảm thấy chưa thực sự đủ để ứng dụng gì nhiều, chủ yếu để học và phân tích. Nếu đem đi xây model thì dựa trên tập dữ liệu này kết quả cho ra cũng khá tệ.

Hai câu hỏi em tự đặt ra và hi vọng trả lời được cũng khá phức tạp, vì dữ liệu không có đủ cho các nước đang phát triển. Cuối cùng em phải đổi câu hỏi, đồng thời lọc lại dữ liệu (chỉ lấy 2024–2025) để trả lời cho phù hợp với thực tế.

**2. Bạn đã vượt qua chúng như thế nào?**
Em chấp nhận làm theo hướng “đủ chạy, đủ trả lời” trong thời gian cho phép: đọc tài liệu nhanh, áp dụng lại vào notebook, rồi kiểm tra kết quả bằng trực quan hoá để xem có hợp lý không. Với phần dữ liệu bị lệch (thiếu nước đang phát triển), em xử lý bằng cách điều chỉnh phạm vi phân tích, đổi câu hỏi cho sát dữ liệu và chủ động filter lại giai đoạn 2024–2025.

**3. Điều gì là thử thách lớn nhất và tại sao?**
Thử thách lớn nhất với em vẫn là thời gian. Vì bị gấp nên em không có cơ hội đào sâu: vừa để hiểu rõ bản chất các hàm/thư viện, vừa để tối ưu code và thử thêm nhiều hướng phân tích khác.
    

### 2. Bài học & Phát triển 

**1. Bạn đã học được những gì?**
Em học được rất nhiều. Kiến thức về quy trình Khoa học dữ liệu của em được củng cố thêm vì được thực hành lại từ đầu: đọc dữ liệu, làm sạch, EDA, trực quan hoá và trình bày kết quả. Cách làm cũng bài bản hơn so với lần đầu, vì em biết chia bước rõ ràng và kiểm tra lại bằng biểu đồ thay vì chỉ nhìn số.

Ngoài ra em cũng có cơ hội tìm hiểu thêm về một số thư viện học máy.

**2. Điều gì làm bạn bất ngờ nhất?**
Em bất ngờ vì dữ liệu nhìn thì “to” nhưng khi đi vào các câu hỏi cụ thể (đặc biệt liên quan so sánh theo quốc gia/nước đang phát triển) lại không đủ để kết luận chắc. Việc thiếu dữ liệu khiến mình phải quay lại điều chỉnh câu hỏi và giới hạn phạm vi phân tích, chứ không thể “cố” trả lời theo ý muốn ban đầu.

**3. Dự án này đã định hình cách hiểu của bạn về Data Science như thế nào?**
Dự án này làm em hiểu rõ hơn là Data Science không phải cứ có dữ liệu là làm được mọi thứ. Quan trọng là đặt câu hỏi phù hợp với dữ liệu mình có, biết giới hạn kết luận, và sẵn sàng đổi hướng khi dữ liệu không hỗ trợ.

Nếu có thời gian, em sẽ đào sâu và tìm hiểu kỹ hơn về các thư viện Data Science trong Python. Riêng trong đồ án này, em cũng muốn nghĩ thêm và thử nghiệm thêm các giả thuyết khác để cải thiện chất lượng phân tích và kết quả.



