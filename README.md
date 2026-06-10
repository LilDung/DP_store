# Shopee Income Sales Analyzer

Web app tĩnh để phân tích file báo cáo thu nhập Shopee dạng:

```text
Income.đã phát hành.vn.*.xlsx
```

## Tính năng

- Kéo thả hoặc chọn file Excel trực tiếp trên trình duyệt.
- Đọc sheet `Doanh thu`.
- Tự tìm dòng header có các cột như `Mã giao dịch`, `Đơn hàng / Sản phẩm`, `Mã đơn hàng`, `Tên sản phẩm`.
- Gom dữ liệu theo `Mã đơn hàng`, liên kết dòng tổng `Order` với các dòng sản phẩm `Sku`.
- Không tính dòng sản phẩm rỗng hoặc `-` là sản phẩm.
- Doanh thu đơn lấy từ cột `Tổng tiền đã thanh toán` ở dòng tổng đơn hàng; không lấy doanh thu ở dòng sản phẩm.
- Lưu mô hình dữ liệu tách riêng `orders` và `orderItems` trong trình duyệt.
- Dashboard: tổng doanh thu, tổng đơn, đơn hoàn, tổng sản phẩm bán, tỷ lệ hoàn đơn.
- Biểu đồ: doanh thu theo ngày, doanh thu theo tháng, đơn hoàn theo tháng.
- Thống kê sản phẩm: tên sản phẩm, đã bán, đơn hoàn, doanh thu, giá vốn, lợi nhuận.
- Tìm kiếm, sắp xếp và lọc theo thời gian.
- Thống kê đơn hoàn: mã đơn, ngày đặt, sản phẩm, giá trị hoàn, lý do hoàn nếu file có cột tương ứng.
- Quản lý sản phẩm: gộp nhiều tên sản phẩm về một tên chuẩn.
- Báo cáo lợi nhuận theo sản phẩm và theo tháng.
- Xuất báo cáo Excel và PDF.

## Cách chạy

Mở file `index.html` bằng trình duyệt.

Lưu ý: app dùng SheetJS qua CDN để đọc Excel, vì vậy máy cần có Internet khi mở trang lần đầu.

## Công nghệ

- HTML/CSS/JavaScript thuần.
- SheetJS `xlsx` để đọc file Excel trong trình duyệt.
- Không có backend, dữ liệu không được upload lên server.
