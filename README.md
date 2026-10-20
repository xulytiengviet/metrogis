# MetroGIS Việt Nam

WebGIS hai thành phố **TP. Hồ Chí Minh** và **Hà Nội** với giao diện đỏ – vàng, bộ chọn tuyến/ga, tìm ga, hiển thị hành trình cùng mô phỏng **Agent-Based Modeling (ABM)**.

## Chạy
Ứng dụng tĩnh: mở `index.html` qua HTTP server hoặc xuất bản bằng GitHub Pages (Settings → Pages → Deploy from branch → main → /(root)). Leaflet và các ô nền OpenStreetMap cần kết nối Internet.

## Tính năng
- Chọn thành phố và tuyến metro, duyệt nhà ga, tìm kiếm, popup tọa độ, vẽ đường đi trên cùng tuyến.
- ABM: tác tử đoàn tàu hai chiều, tốc độ, headway, hàng chờ ga, hành khách lên tàu; chạy/tạm dừng/từng bước/đặt lại.
- “Khám phá Metro” là chuyên mục riêng gồm 6 chuyên đề kỹ thuật, vận hành và TOD.
- Giao diện responsive; 100% tiếng Việt.

## Chất lượng dữ liệu và phạm vi
**Cảnh báo:** Tọa độ và đoạn nối giữa các ga trong `index.html` là dữ liệu minh họa được biên soạn độc lập, **không phải hình học đường sắt đã khảo sát**. Chỉ hiển thị các đoạn tuyến được chọn trong bản mẫu; chưa tích hợp bộ `network.json` của trang tham khảo, chưa kiểm chứng tính đầy đủ và tiến độ mới nhất. Không có realtime GTFS, không có lịch tàu, giá vé hay số lượng hành khách thật. Phần ABM hoàn toàn giả định và không dùng để điều hành giao thông.

Tài liệu tham chiếu của website Metro Việt Nam: https://metro.jamesthang.com/data/metro/SOURCES.md . Cần kiểm tra điều khoản dữ liệu trước khi tái sử dụng. Không sao chép mã hoặc tài sản của website đó.

Bản đồ: © OpenStreetMap contributors, https://www.openstreetmap.org/copyright. Leaflet: BSD-2-Clause.

## Hướng phát triển
Tách mạng lưới thành GeoJSON/GTFS, xác minh tọa độ nhà ga, trạng thái từng đoạn với nguồn vận hành chính thức, xây dựng chuyển tuyến qua thuật toán đường đi ngắn nhất, GTFS-RT nếu có quyền truy cập; ABM theo điều kiện thực nghiệm, seed xác định và xuất CSV.

© 2026 MetroGIS demonstration.