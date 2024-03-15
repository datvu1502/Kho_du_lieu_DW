# KHO DỮ LIỆU VÀ KINH DOANH THÔNG MINH
Trong thời đại số hóa ngày càng phát triển, dữ liệu đã trở thành một tài nguyên
quan trọng, được coi là "dầu mỏ" của thế kỷ XXI. Hiểu và khai thác dữ liệu một cách
thông minh đã trở thành yếu tố quyết định sự thành công của các doanh nghiệp và tổ
chức trong mọi lĩnh vực. Kho dữ liệu, cùng với công nghệ phân tích dữ liệu và trí tuệ nhân
tạo, đóng vai trò quan trọng trong việc tạo ra thông tin hữu ích và hiểu sâu về khách
hàng, thị trường và quy trình kinh doanh.

Báo cáo này sẽ giới thiệu một số khái niệm cơ bản về kho dữ liệu và kinh doanh
thông minh, từ cách xây dựng một kho dữ liệu hiệu quả, quản lý dữ liệu, cho đến quá
trình trích xuất thông tin, phân tích và áp dụng dữ liệu trong kinh doanh.

# Tổng quan về Inventory
Quản lý hàng tồn kho hay quản lý kho hàng là tập hợp các công việc liên quan đến các
công tác tổ chức, quản lý, sắp xếp, bảo quản hàng hóa trong kho lưu trữ. Quản lý hàng
tồn kho đề cập đến quá trình đặt hàng, lưu trữ, sử dụng và bán hàng tồn kho của công ty.
Điều này bao gồm việc quản lý nguyên liệu thô, linh kiện và thành phẩm, cũng như lưu
kho và xử lý các mặt hàng đó. Quản lý hàng tồn kho là một công việc quan trọng trong
phải luôn thực hiện liên tục và xuyên suốt trong quá trình hàng hóa lưu trữ trong kho.
Việc quản lý hàng tồn kho hiệu quả giúp tăng cường an toàn trong bảo quản hàng
hóa, tận dụng tốt cơ sở vật chất, tiết kiệm chi phí đầu tư cũng như tăng doanh thu cho
doanh nghiệp về lâu dài.
# Vai trò của quản lý kho
• Tối ưu hoá chi phí: Quản lý hàng tồn kho hiệu quả giúp giảm thiểu chi phí lưu trữ,
vận chuyển, và xử lý hàng tồn kho.

• Đảm bảo sẵn sàng cung ứng: Quản lý hàng tồn kho đảm bảo rằng tổ chức luôn có
đủ hàng hóa để đáp ứng nhu cầu của khách hàng.

• Tăng hiệu quả tài chính: Quản lý hàng tồn kho hiệu quả giúp tối ưu hóa vòng quay
vốn.


• Theo dõi và đánh giá hiệu suất: Quản lý hàng tồn kho cung cấp thông tin quan
trọng để theo dõi và nhận biết xu hướng tiêu thụ, đánh giá hiệu quả của chiến lược
quản lý hàng tồn kho và thực hiện các điều chỉnh cần thiết.

# Quy trình nghiệp vụ
![diagram](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/24fc5e6e-1bcc-4b31-a77f-70d364aacf4b)

# Tổng quan về bộ dữ liệu
• Tên bộ dữ liệu: AdventureWorks2022

• Nguồn: Microsoft learn

• Kích thước: 200MB

• Dữ liệu gồm 16 bảng, được trích ra từ cơ sở dữ liệu hoàn chỉnh của công ty
AdventureWorks.

Nội dung bộ dữ liệu: Cơ sở dữ liệu quan hệ chứa thông tin về các giao dịch của
công ty AdventureWorks-một công ty hư cấu đa quốc gia chuyên sản xuất và kinh doanh
xe đạp và phụ kiện xe đạp. Thông tin giao dịch liên quan đến nhập hàng, mua hàng từ các
nhà cung cấp, thông tin liên quan đến sản xuất của công ty và các dữ liệu về bán hàng
của công ty.

# Mô hình ERD & OLTP
![OLTP](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/7513f029-f84c-41cb-bd51-5f3a817098b0)

# Khám phá dữ liệu
## Data analysis tools:

![z5070571748364_9103b436388a5d321a8223eb485d6b5b](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/011864f7-e34a-4e87-a5cc-ccb773c85398)
## Biểu đồ scatter thể hiện tương quan giữa ScrappedQty và StockedQty:
![scatter](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/295aebb8-15e2-4a2d-b8e3-0afc723a75c5)

Từ biểu đồ phân tán ta có thể nhận thấy rằng có sự tương quan giữa số lượng đơn
sản phẩm được sản xuất và số lượng sản phẩm bị lỗi (trong các trường hợp xuất hiện sản phẩm lỗi). Điều này cũng rất phù hợp với thực tế khi chúng tả sản xuất
 nhiều thì trường hợp xuất hiện sản phẩm lỗi càng cao
## Biểu đồ histogram về tần suất số lượng sản phẩm trong 1 đơn đặt hàng:
![histogram_order](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/3eb78755-c18f-45f0-bcd4-24ef2a486d33)

Từ biểu đồ ta có thể thấy ràng tần suất số lượng sản phẩm được đặt trong 1 đơn
hàng có hình dáng nửa của hình chung có đỉnh nằm trong khoảng 0-10. Từ đó có
thể đánh giá rằng nó đang tuân theo phân phối chuẩn.

## Biểu đồ histogram về tần suất số lượng hàng tồn kho:
![histogram_quantity](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/423896c0-e2c6-4113-8195-6f5545825763)

Từ biểu đồ ta có thể thấy tần suất số lượng hàng tồn kho có dạng biểu đồ nhiều
đỉnh. Nó là biểu hiện của sự đa dạng và phức tạp trong dữ liệu. Và nó không tuân
theo một luật phân phối nào.

## Biểu đồ cột thể số lượng hàng tồn kho trung bình tại các cơ sở:
![mean_location](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/b5148be7-72b3-4817-9078-861f6539402c)

Từ biểu đồ trên ta có thể thấy rằng số lượng hàng tồn kho giữa các cơ sở phân bố
không đều, và có sự chênh lệch khá lớn giữa cơ sở cao nhất và thấp nhất. Cơ sở có
số lượng hàng tồn kho trung bình là Sheet Metal Racks và cơ sở có lượng hàng tồn
kho thấp nhất là Paint Storage.

## Biểu đồ thể số lượng hàng tồn kho theo thời gian:
![tonkhotime](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/8ff0d084-9338-4af2-bcce-cdfbfcef5eb4)

Biểu đồ trên thể hiện số lượng hàng tồn kho của các loại sản phẩm theo thời gian.

– Đối với loại sản phẩm Accessories và Clothing: số lượng hàng tồn kho có sự
biến động không cao. Có xu hướng tăng từ tháng 5/2011 đến tháng 1/2012.
Giữ mức ổn định từ tháng 1/2012 cho đến tháng 5/2013. Và có xu hướng giảm
từ tháng 5/2013 đến tháng 9/2014.

– Đối với loại sản phẩm Bikes: số lượng hàng tồn kho có sự biến động lớn. Có xu
hướng giảm từ tháng 5/2011 đến tháng 5/2012. Có xu hướng tăng từ tháng
5/2012 đến tháng 5/2013. Có xu hướng giảm từ tháng 5/2013 đến tháng 9/2014.

– Đối với loại sản phẩm Components: số lượng hàng tồn kho có sự biến động lớn.
Có xu hướng tăng mạnh từ tháng 5/2011 đến tháng 5/2012. Và có xu hướng
giảm mạnh từ tháng 5/2012 đến tháng 9/2014.
## Biểu đồ boxplot thể hiện sự phân phối số lượng hàng tồn kho theo loại sản phẩm
![boxplot](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/a74063c1-2fd7-4cba-a1b6-c6db11cc22b1)

Độ cao giữa các hộp có sự chênh lệch thể hiện sự phân bố không đồng đều giữa các
loại sản phẩm tồn kho. Có xuất hiện một vài giá trị ngoại lai trong loại sản phẩm
Accessories.

– Đối với loại sản phẩm Bikes: số lượng hàng tồn kho có sự biến động lớn. Có xu
hướng giảm từ tháng 5/2011 đến tháng 5/2012. Có xu hướng tăng từ tháng
5/2012 đến tháng 5/2013. Có xu hướng giảm từ tháng 5/2013 đến tháng 9/2014.

– Đối với loại sản phẩm Components: số lượng hàng tồn kho có sự biến động lớn.
Có xu hướng tăng mạnh từ tháng 5/2011 đến tháng 5/2012. Và có xu hướng
giảm mạnh từ tháng 5/2012 đến tháng 9/2014.
# Kiến trúc Datawarehouse
Kiến trúc mô hình hệ thống Datawarehouse gồm 4 lớp:

<img width="844" alt="datawarehouse" src="https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/c65fcccb-8a1a-49ec-baaa-6983ee7e1177">

#  Tóm tắt các hoạt động ETL
• Extrasct: 2 file bak AdventureWorks2022.bak và AdventureWorksDW2022.bak sau
khi được download sẽ được mở và lưu trữ trên SQL Server. Sau đó, thực hiện việc
trích xuất dữ liệu cần thiết từ SQL Server vào vùng stagging để xử lý.

• Transform: Gồm các hoạt động được thực hiện trên các công cụ là Power Query,
MySQL, Python như: làm sạch dữ liệu, xử lý dữ liệu null, xóa các trường không cần
thiết, định dạng kiểu dữ liệu, chuẩn hóa dữ liệu, phân loại dữ liệu theo nhóm.

• Load: Tải dữ liệu sau khi đã tiền xử lí vào hệ cơ sở dữ liệu datamart trong MySQL,
quá trình load dữ liệu sẽ được sử dụng bằng Python thông qua mysql-connector.

## Sử dụng công cụ PowerQuery

• Dim Product: Chuẩn hóa lại cột ID trong bảng Product, sau đó nối bảng product
với bảng ProductCategory và ProductSubCategory để lấy các trường dữ liệu cần
thiết, tiếp đến sẽ loại bỏ các trường dữ liệu không cần thiết như ID của bảng
ProductCategory, ProductSubCategory,...Cuối cùng, thay thế các giá trị NULL bằng
dữ liệu có nghĩa cho việc phân tích.

![etl_product](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/d97b3973-e76f-4b5b-a369-f0759ba5f907)

• Dim Vendor: Loại bỏ các trường không quan trọng trong bảng Vendor, giữ lại 3
trường VendorID, Name, CreditRating.

![etl_vendor](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/8bec5f63-3836-4a23-bff3-b99dbe06e2ae)

• Dim Ship Method: Loại bỏ các trường không quan trọng trong bảng ShipMethod,
giữ lại 3 trường ShipMethodID, Name.

![etl_shipmethod](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/4d7b7d31-60d7-4c1b-93f6-c1465e14c8cf)

• Fact Purchasing: Nối bảng PurchaseOrderHeader với bảng PurchaseOrderDetail và
bảng DimProduct đã được xử lý. Sau đó, bỏ đi một số trường dữ liệu không cần
thiết.

![etl_purchase (1)](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/93dd23f8-e729-49f2-86bb-1f79bdf6eaa9)

• Fact Sales: Thực hiện lọc dữ liệu trên bảng TransactionHistory với TransactionType
là S. Sau đó, bỏ đi một số trường dữ liệu không cần thiết.

![etl_sales](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/63e75284-5ceb-4b02-bec5-e9ee5e1e2215)

• Fact Work Order: Thực hiện lọc dữ liệu trên bảng TransactionHistory với Transac-
tionType là S. Sau đó, bỏ đi một số trường dữ liệu không cần thiết.

![etl_workorder](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/35f2ff47-959c-4d48-ba8a-68070afd0901)

##  Sử dụng công cụ Python
• Sinh trường dữ liệu thời gian bắt đầu theo đúng định dạng chuẩn của MySQL

<img width="553" alt="time1" src="https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/77915e29-a812-4b97-a0ef-5555d99b963d">

• Sau đó đổ vào cơ sở dữ liệu MySQL.

<img width="552" alt="time2" src="https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/8e0e9f89-f4e0-4d3e-909c-f1680398afa3">

## Sử dụng công cụ MySQL
• Do dữ liệu thời gian tại vùng staging chưa phải dạng chuẩn của MySQL, nên khi xây
dựng các bảng trong MySQl đều để các trường thời gian dưới dạng VARCHAR(20).
Sau khi dữ liệu, cần đưa về dạng chuẩn, điều này được thực hiện trên MySQL
Workbench bằng công cụ Table.

![time_sql](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/8a949a72-7340-4772-b6b9-ec8d69df8f29)

# Chuyển đổi từ OLTP sang OLAP
Trích xuất các trường dữ liệu trong oltp để tạo dim, fact

![otlpolap1](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/352e5b1d-67c8-4f2f-bf15-b90e994c700c)

![oltpolap2](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/fdee84f6-b7b1-490d-83f9-c21c1703de40)

# Data Model OLAP
## Hệ thống chiều khái niệm
Chiều khái niệm về thời gian

<img width="221" alt="voi_date" src="https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/dd97decb-2a4f-4fbb-82fd-c94111c6bc11">

Chiều khái niệm về sản phẩm

<img width="590" alt="voi_product" src="https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/463462e7-877e-4216-8ca9-f4305f595f8d">

Chiều khái niệm về đơn vị vận chuyển

<img width="95" alt="voi_ship" src="https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/0ffd2611-57a6-4351-8fe0-3793df31b7cb">

Chiều khái niệm về nhà cung cấp
<img width="239" alt="voi_vendor" src="https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/0863ec1c-ef9a-467d-9687-783163909d1b">


## Model Logic
<img width="834" alt="model_logic" src="https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/b02fd36c-98a7-45a8-95af-b079cd8fde1b">

## Model Vật Lý
![dimfact_erd](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/1bd4da5c-d836-4197-9776-547c5f182e97)

Các Fact và Dimension bao gồm:

• Fact-Sales: có chức năng thống kê các chỉ số quan trọng trong quá trình bán hàng.

• Fact-Purchasing: có nhiệm vụ phân tích tình hình nhập hàng.

• Fact-Work Order: phục vụ cho việc báo cáo về khâu sản xuất của công ty.

• Fact-Inventory Balance: chứa thông tin các giao dịch xuất-nhập hàng ngày trong
kho, giúp thực hiện các quyết định liên quan đến phân phối số lượng các sản phẩm
một cách hợp lý.

• Dim-Date: chứa thông tin về thời gian.

• Dim-Product: chứa các thông tin về sản phẩm.

• Dim-Ship Method: chứa các thông tin về các hình thức vận chuyển.

• Dim-Vendor: chứa các thông tin về nhà cung cấp và mức độ tin cậy của nhà cung
cấp đó.

# Xây dựng Dashboard phân tích dữ liệu

1. Trang Quản lý kho hàng gồm các slicer và các chart thể hiện các thông số tổng quát
giúp người sử dụng dashboard có được những thông số theo mục đích phân tích. Các
chart chính trong dash chủ yếu đưa ra các thông tin phân tích liên quan đến tổng
lượng hàng trong kho, lượng hàng nhập, xuất theo thời gian. Số lượng sản phẩm
trong kho theo loại sản phẩm, màu, hàng sản xuất và hàng bán.
![dash1](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/042a8efe-9e9e-4ec5-86de-95c2e5ee62fd)

2. Trang Phân tích đơn nhập hàng chủ yếu phân tích số lượng và giá trị hàng mua theo
các nhà cung cấp, phương thức vận chuyển theo thời gian, thời gian nhập hàng của
từng loại sản phẩm.
![2dash](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/d153d9c6-72ec-4855-bc99-c4e7ef557749)

3. Trang Phân tích sản xuất gồm các slicer, chart và chỉ số thể hiện tình hình tổng
quan về sản lượng và giá trị sản xuất theo thời gian, có thể drilldown từ loại sản
phẩm xuống tên sản phẩm để phân tích cụ thể.
![3dash](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/16e3bad9-41c2-4634-bc2c-1f22a4ca81ea)

4. Trang Phân tích bán hàng chủ yếu phân tích về tổng lượng bán và giá trị theo
loại sản phẩm và theo thời gian. Dùng slicer để tùy ý, tùy chỉnh thông tin hiển thị
dashboard mà người dùng cần.
![4dash](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/df912479-aa86-4ee2-9d5b-4b9743160d48)





