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
Giới thiệu
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
Data analysis tools:
![z5070571748364_9103b436388a5d321a8223eb485d6b5b](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/011864f7-e34a-4e87-a5cc-ccb773c85398)

Biểu đồ histogram về tần suất số lượng sản phẩm trong 1 đơn đặt hàng:
![histogram_order](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/3eb78755-c18f-45f0-bcd4-24ef2a486d33)

Biểu đồ thể số lượng hàng tồn kho theo thời gian:
![tonkhotime](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/8ff0d084-9338-4af2-bcce-cdfbfcef5eb4)

Biểu đồ boxplot thể hiện sự phân phối số lượng hàng tồn kho theo loại sản phẩm
![boxplot](https://github.com/datvu1502/Kho_du_lieu_DW/assets/118582440/a74063c1-2fd7-4cba-a1b6-c6db11cc22b1)


