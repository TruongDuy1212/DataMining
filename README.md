# DataMining
🔄 Thứ tự thực thi & Cách chạy lại (Reproduction Guide)
Dự án được thiết kế theo dạng các module độc lập. Tuy nhiên, để bám sát theo luồng logic của báo cáo, khuyến nghị thực thi theo trình tự sau:

Bước 1: Khởi tạo dự án
Clone kho chứa này về máy tính cá nhân của bạn:
git clone [https://github.com/](https://github.com/)[username-cua-ban]/[ten-repo].git
cd [ten-repo]

**Bước 2: Chạy các mô hình Phân lớp (Classification)**

Mở file bai2-phan-lop.ipynb bằng Jupyter Notebook hoặc VS Code.

Chọn Run All (hoặc chạy tuần tự từng ô cell).

Kết quả đầu ra: Các bảng Classification Report (Precision, Recall, F1-Score) cho bộ D1, D2, D3.

**Bước 3: Chạy mô hình Khai phá luật (Association Rules)**

Mở file bai3-luat-ket-hop.ipynb.

Chọn Run All.

Lưu ý: Mã nguồn đã được cấu hình ngưỡng Support siêu nhỏ (0.001 cho D3) để giải quyết vấn đề phân tán dữ liệu thưa thớt. Thuật toán sẽ tự động in ra Top 3 luật kết hợp mạnh nhất.

**Bước 4: Chạy mô hình Phân cụm (Clustering)**

Mở file bai4-phan-cum.ipynb.
Chọn Run All.
Kết quả đầu ra: Biểu đồ Elbow (Khuỷu tay) chứng minh số cụm $k=3$, bảng đánh giá chỉ số Silhouette/DBI, và các bảng Profiling khắc họa chân dung khách hàng cho từng tập dữ liệu.

⚠️ Xử lý sự cố (Troubleshooting):
Nếu gặp lỗi _IncompleteInputError hoặc hệ thống bị treo bộ nhớ (RAM) khi chạy file, hãy bấm nút Clear Outputs để làm sạch bộ nhớ đệm, sau đó chọn Restart Kernel and Run All Cells để môi trường tính toán lại từ đầu.**
