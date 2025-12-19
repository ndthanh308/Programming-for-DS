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

