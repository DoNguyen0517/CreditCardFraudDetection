# CreditCardFraudDetection

### Giới thiệu

Kho lưu trữ này chứa mã và tài liệu cho quy trình Xây dựng các mô hình dự báo gian lận tín dụng (Fraud) trong ngân hàng. 
Mục tiêu của dự án này là tìm ra mô hình học máy phù hợp nhất để áp dụng cho dự báo gian lận tín dụng, giúp ngân hàng đưa ra những quyết định cần thiết để đối phó với điều đó.

### Nguồn dữ liệu và tổng quan

Bộ dữ liệu FraudDetection được lấy từ một chia sẻ trên kho dữ liệu Kaggle. 
Đây là tập dữ liệu giao dịch thẻ tín dụng mô phỏng chứa các giao dịch hợp pháp và gian lận từ ngày 1 tháng 1 năm 2019 đến ngày 31 tháng 12 năm 2020. 
Nó bao gồm thẻ tín dụng của 1000 khách hàng thực hiện giao dịch với nhóm 800 người bán.


### Các công cụ được sử dụng

1. **Python**
2. **Pandas** cho **Data Manipulation**, **Cleaning**.
3. **Matplotlib, seaborn** cho **Data Visualization**
4. **Sci-kit learn** cho **Modelling**, **Model Evaluation**

### Quy trình thực hiện

1. **Data Understanding** - Tập dữ liệu đã được kiểm tra kỹ lưỡng để hiểu cấu trúc, các cột và ý nghĩa của chúng.
   Dữ liệu không có từ điển dữ liệu kèm theo. Với sự trợ giúp của các nguồn trực tuyến, tôi đã có thể tạo một nguồn
   giúp tôi hiểu được ý nghĩa của tất cả các cột.
2. **Data Exploration** - Phân tích dữ liệu khám phá (**EDA**) đã được thực hiện để hiểu rõ hơn về dữ liệu, xác định các mẫu và phát hiện ra sự bất thường.
3. **Data Preprocessing**
- Thực hiện bỏ các cột không cần thiết cho quá trình dự báo
- Thực hiện xử lý Outliers với phương pháp **Clipping**
- Thực hiện mã hóa dữ liệu với các biến categorical bằng phương pháp **Dummies**
- Xử lý mất cân bằng đối với biến mục tiêu bằng phương pháp Oversampling, cụ thể là kỹ thuật **SMOTE**
4. **Model Fitting** - Thực hiện xây dựng 2 mô hình dự báo áp dụng cho dự báo phân loại (classification): **Logistic Regression**, **RandomForest**
5. **Model Evaluation** - Thực hiện đánh giá, so sánh 2 mô hình dự báo, tìm ra mô hình tốt nhất bằng việc so sánh thông qua **accuracy score**, **classification report**.
