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
- Tạo thống kê tóm tắt và trực quan hóa bằng hisplot, lineplot và matrix
- Sử dụng Power BI xây dựng hệ thống chart trực quan hóa dữ liệu.
  
## Data Cleaning
- Kiểm tra null
  - Sử dụng hỗ trợ AI Chatbox tìm year các game chưa có năm phát hành sau đó sử dùng vlookup trong excel
  - Thay thế các cột trống ở NA_Sales, EU_Sales, JP_Sales, Other_Sales và Global_Sales thành giá trị 0
- Chuẩn hóa định dạng dữ liệu ngày tháng và tên cột.
- Loại bỏ các phần trùng lặp

## Exploratory Data Analysis (EDA)
Phân tích cơ bản:
- Sử dụng Descriptive, hisplot và matrix giữa các khu vực
  - <img width="824" alt="Ảnh màn hình 2025-02-17 lúc 12 08 39" src="https://github.com/user-attachments/assets/61c268d4-524e-4951-8702-897608068a04" />
  - <img width="707" alt="Ảnh màn hình 2025-02-17 lúc 12 09 09" src="https://github.com/user-attachments/assets/57448823-d617-40e8-906b-b7c70e6e4ab7" />
  - <img width="854" alt="Ảnh màn hình 2025-02-17 lúc 12 11 01" src="https://github.com/user-attachments/assets/550b60e9-0c1e-46e3-99af-1c9bc3228ecf" />
  -> Tôi rút kết luận như sau:
    - Dựa vào độ lệch chuẩn std cao (1.55 triệu bản) và 50% median = 0.06 triệu bản cho thấy thị trường game rất khắc nhiệt, phần lớn số lượng game được bán ra rất thấp trong đó 75% số có doanh số bán 0.47 triệu bản và 25% game bán được 470.000 triệu bản.
    - NA được xem là thị trường lớn nhất với thị phần chiếm 50% toàn bộ thị trường sau đó là EU với 29% thị phần kế đó là Other 12,9% và JP là 12%.
    - 3 Thị trường NA, EU và JP đều có liên quan ảnh hưởng đến nhau nhưng thị trường JP lại ít ảnh hưởng như 3 thị trường trên, một số game không bán được tại thị trường JP. Ngoài ra JP cũng là thị trường có ít game bán chạy.

Phân tích theo các yếu tố:
- Vì platform có sự update qua các năm nên để chuẩn xác tôi đã tạo thêm cột Manufacturer ghi nhận tên công ty sản xuất platform đó và phân tích bằng công ty sản xuất platform thay cho platform.
  - Tạo data manufacturer và dử dụng vlookup cập nhật vào file data sau đó đọc lại data.
- Gọi và sắp xếp các thể loại game và nhà sản xuất platform theo doanh số bán từ cao đến thấp
  - <img width="865" alt="Ảnh màn hình 2025-02-17 lúc 12 34 56" src="https://github.com/user-attachments/assets/ed3ac235-c2d9-4f42-a2a2-2b61048a4a34" />
  - <img width="830" alt="Ảnh màn hình 2025-02-17 lúc 12 46 25" src="https://github.com/user-attachments/assets/9e941d23-fe5d-460f-b19f-bfc137e85022" />
  -> Rút ra kết luận
    - Nên đầu tư vào platform của Sony, Nintendo và Microsoft. Tránh đầu tư vào game không chạy được trong bộ 3 này vì các platform còn lại có doanh số rất thấp
    - Các thế loại game Action, Sport và Role-Playing có tiềm năng đầu tư lớn
    - Nintendo, EA và Activision là những nhà phát hành đáng chú ý.

Phân tích chi tiết từng thị trường:
  - Kiểm tra doanh số theo thể loại game, nhà phát hành và platform
  - <img width="739" alt="Ảnh màn hình 2025-02-17 lúc 13 28 23" src="https://github.com/user-attachments/assets/0e407ff9-55a0-482e-a38f-e33618241908" />
  - <img width="908" alt="Ảnh màn hình 2025-02-17 lúc 13 31 12" src="https://github.com/user-attachments/assets/b8c646a3-4a72-419c-b948-2d5d683ae8d8" />
  - <img width="879" alt="Ảnh màn hình 2025-02-17 lúc 13 32 12" src="https://github.com/user-attachments/assets/e0d11213-7c51-40d1-8152-4233fd936541" />
  -> Kết luận từng loại thị trường:
    - NA:    Với thị trường bắc mỹ nên tập trung đầu từ vào game thuộc thể loại Action và Sport cho 2 dòng mày của Nintendo và Sony
    - EU:    Với thị trường EU nên tập trung đầu từ vào game thuộc thể loại Action và Sport cho 2 dòng mày của Nintendo và Sony
    - Other: Với thị trường Other nên tập trung đầu từ vào game thuộc thể loại Action và Sport cho 2 dòng mày của Sony và Nintendo. Cần đặc biết chú ý platform thuộc công ty Sony có doanh số rất cao gần như gấp đôi nên khi đầu tư thị trường này nên tập trung vào các game có platform này.
    - JP:Với thị trường Nhật Bản rất khác biết với các thị trường còn lại khi các thế loại game được yêu thích có chung là action và sport nhưng thể loại role-play lại vượt trội rất nhiều, các nhà sản xuất game và platform nội địa vũng vượt trội so với các công ty đến từ nước khác. Cho thấy thị trường này cần nghiên cứu kỹ về tính nội địa trước khi đầu tư. Nếu đầu tư vào thị trường này nên đầu tư game role-play của nhà phát hành và sản xuất flatform Nintendo vì các thông số của công ty này rất vượt trội so với các công ty khác
Kết luận cuối:
  - Thị trường game rất khắc nghiệt vì phần lớn các game đều có doanh số rất thấp nhưng khi thành công thường có doanh số rất cao. Nên khi đầu từ cần chú ý các yếu tố thị trường khi đầu tư như sau:
  - Thị trường NA, EU:
    Thị trường NA và EU đã chiếm tới 76% thị phần toàn ngành game. Đây được xem là 2 thị trường lớn nhất, trong đó thị trường NA chiếm 50% toàn ngành game.
Vì tính chất của 2 thị trường này giống nhau đến 90% theo thể loại game, nhà phát hành và platform nên có thể xem như đầu tư vào 2 thị trường cùng lúc.
Dựa vào bộ data nên đầu từ vào các thể loại game Action, Sport,Shooter thuộc các nhà phát hành Nintendo, EA, Activision và được chơi trên các hệ máy của Sony, Nintendo và Microsoft.
  - Thị trường Others:
    Thị trường này tuy nhỏ hơn 2 thị trường trên nhưng có các thông số về thể loại, nhà phát hành và platform giống với thị trường NA và EU nên về mặt đầu tư có thể đầu tư 3 thị trường NA, EU, Others cùng lúc. Đầu tư các game như đã kết luận ở thị trường NA,EU.
Tuy nhiên thị trường này cũng có tính chất bản địa khác so với 2 thị trường NA, EU nên khi muốn đầu tư tập trung vào thị trường này cần chú ý đến các game được chơi trên platforms của Sony vì chỉ số này vượt trội so với Nintendo và Microsoft.
  - Thị trường JP:
    Đây là một thị trường rất đặc biệt nặng tính bảng địa. Các chỉ số cho thấy các nhà phát hành và công ty sản xuất platform nội địa rất được ưa chuộng. Cần chú ý đến Nintendo vì công ty này phát hành game hay game chơi trên platform của họ có doanh số vượt trội.
Thị trường này cũng thích chơi các thể loại game Action và Shooter như các thị trường khác tuy nhiên thể loại Role-play có doanh số rất vượt trội.
Nên đầu tư game thuộc thể loại role-play thuộc nhà phát hành và chơi trên platform của Nintendo sẽ tăng khả năng thành công cao hơn.
    


 
  

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
