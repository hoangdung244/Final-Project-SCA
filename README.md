# Final-Project-SCA
Bài tập cuối kỳ SCA
# Video games sales analysis and visualization
## Project Overview
Dữ án này được thực hiện trên một bộ dữ liệu doanh số bán game của các thị trường gồm Bắc Mỹ, Châu Âu, Nhật Bản và các thị trường khác. Dữ án được thực hiện nhằm mục đích tìm câu trả lời ban đầu cho việc đầu tư vào thị trường game.
## Purpose and Outcome
Thông qua dự án, tôi sẽ trả lời những câu hỏi chính như:
- Những thể loại game, nhà phát hành và hệ máy của nhà phát hành nào được yêu thích nhất
- Đâu là thị trường lớn nhất, tính chất của các thị trường, nên đầu tư thị trường nào.

## Technologies
- **Power BI**: Để trực quan hóa dữ liệu.
- **Python (Pandas, Matplotlib)**: Để xử lý và phân tích dữ liệu.
- **AI Chatbot**: Hỗ trợ xử lý dữ liệu.

## Data Sources
Dữ liệu được tham khảo từ Kaggle:
- Link Kaggle: https://www.kaggle.com/code/snanilim/video-games-sales-analysis-and-visualization

## Data Overview
- Dữ liệu chứa gần **16.000** game từ những năm 1980 đến 2016
- **10 cột** với các chỉ số liên quan đến thể loại, nhà phát hành, nhà sản xuất và doanh số bán các thị trường

## Analysis
- Tạo thống kê tóm tắt và trực quan hóa bằng hisplot và matrix
- Sử dụng Power BI xây dựng hệ thống chart trực quan hóa dữ liệu.
  
## Data Cleaning
- Kiểm tra null
  - Sử dụng hỗ trợ AI Chatbox tìm year các game chưa có năm phát hành sau đó sử dùng vlookup trong excel
  - Thay thế các cột trống ở NA_Sales, EU_Sales, JP_Sales, Other_Sales và Global_Sales thành giá trị 0 
- Chuẩn hóa định dạng dữ liệu ngày tháng và tên cột.
- Loại bỏ các phần trùng lặp

## Exploratory Data Analysis (EDA)
Phân tích cơ bản
- ** Sử dụng Descriptive, hisplot và matrix giữa các khu vực
- <img width="824" alt="Ảnh màn hình 2025-02-17 lúc 12 08 39" src="https://github.com/user-attachments/assets/61c268d4-524e-4951-8702-897608068a04" />
- <img width="707" alt="Ảnh màn hình 2025-02-17 lúc 12 09 09" src="https://github.com/user-attachments/assets/57448823-d617-40e8-906b-b7c70e6e4ab7" />
- <img width="854" alt="Ảnh màn hình 2025-02-17 lúc 12 11 01" src="https://github.com/user-attachments/assets/550b60e9-0c1e-46e3-99af-1c9bc3228ecf" />
-> Tôi rút kết luận như sau
  - thị trương game rất khắc nhiệt dựa vào độ lệch chuẩn std cao (1.55 triệu bản) và 50% median = 0.06 triệu bản cho thấy thị trường game rất khắc nhiệt, phần lớn số lượng game được bán ra rất thấp trong đó 75% số có doanh số bán 0.47 triệu bản và 25% game bán được 470.000 triệu bản.
  - NA được xem là thị trường lớn với thị phần chiếm 50% toàn bộ thị trường sau đó là EU với 29% thị phần kế đó là Other 12,9 và JP là 12.5.
  - 3 Thị trường NA, EU và JP đều có liên quan ảnh hưởng đến nhau nhưng thị trường JP lại ít ảnh hưởng như 3 thị trường trên, một số game không được tại thị trường JP. Ngoài ra JP cũng là thị trường có ít game bán chạy.


  - Doanh thu bán game các thị trường từ năm 1980 đến 2016
  - 
  - Giá trị trung bình, lớn nhất và nhỏ nhất của số tiền vay.
- **Phân Tích Xu Hướng**:
  - Biểu đồ thể hiện sự thay đổi số lượng khoản vay theo năm.
- **Phân Tích Nhóm Khách Hàng**:
  - Nhóm tuổi khách hàng phổ biến nhất.
  - Tỷ lệ khách hàng có rủi ro tín dụng cao.

## Data Visualization
- **Biểu đồ cột** thể hiện số lượng khoản vay theo từng năm.
- **Biểu đồ tròn** phân tích tỷ lệ nhóm tuổi khách hàng.
- **Biểu đồ hộp (Box plot)** thể hiện phân phối số tiền vay.

## Data Storytelling
- Khách hàng vay từ năm 2014 đến 2018 có xu hướng gia tăng, với phần lớn khoản vay tập trung vào nhóm khách hàng trong độ tuổi từ 25 đến 45.
- Dữ liệu cho thấy rằng khách hàng vay số tiền lớn hơn 100.000 USD có nguy cơ chậm thanh toán cao hơn.

## Outcomes
- Xác định các yếu tố ảnh hưởng đến khả năng thanh toán của khách hàng.
- Nhận diện nhóm khách hàng có nguy cơ tín dụng cao để đưa ra các biện pháp quản lý rủi ro hiệu quả hơn.
- Phân tích xu hướng vay để đưa ra các chính sách phù hợp cho từng nhóm khách hàng.

## Các step thực hiện

## File code python

## Power BI

## Power Point
