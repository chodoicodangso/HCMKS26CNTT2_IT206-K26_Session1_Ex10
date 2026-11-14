Phần 1: Lập Bảng Tính Chi Phí Chi Tiết (Cho 50.000 tin nhắn)  
Công thức tính Token thực tế (có nhân hệ số BPE Tiếng Việt \= 2.5):  
Tổng Input Token \= 50.000 tin x 200 từ x 2.5 \= 25.000.000 tokens  
Tổng Output Token \= 50.000 tin x 100 từ x 2.5 \= 12.500.000 tokens  
Bảng tính toán chi phí thực tế theo API GPT-4o  
Chi phí Input: (25.000.000 / 1.000.000) x 2.50 \= 62.50  
Chi phí Output: (12.500.000 / 1.000.000) x 10.00 \= 125.00  
Tổng chi phí USD: 62.50 \+ \$125.00 \= 187.50  
Quy đổi ra VNĐ (Tỷ giá 25.000): 187.50 x 25.000 \= 4.687.500 VNĐ  
Chỉ ra lỗi tính thiếu của phòng Marketing:  
Marketing tính nhầm số lượng token theo kiểu tiếng Anh (1 từ \= 1 token), ra kết quả 37.5 USD (\~937.500 VNĐ)  
Bỏ qua hệ số BPE Tiếng Việt và định dùng tài khoản cá nhân (\$20/tháng), dẫn đến việc tính thiếu ngân sách thực tế gấp 5 lần (thiếu gần 3.75 triệu VNĐ) và gây rủi ro lớn về bảo mật PII  
Phần 2: Thiết Kế Hạ Tầng Enterprise API Gateway  
Lý do bắt buộc chuyển sang Enterprise API (Azure OpenAI / Private LLM):  
Chính sách Zero Data Retention: Nhà cung cấp cam kết không lưu trữ dữ liệu hội thoại hay thông tin cá nhân (PII) của khách hàng để train AI  
Tuân thủ bảo mật doanh nghiệp: Tránh dùng tài khoản cá nhân gây rò rỉ dữ liệu, đồng thời tích hợp sẵn các lớp mã hóa và phân quyền  
Kiểm soát vận hành: Dễ dàng quản lý hạn mức sử dụng và lọc tự động các từ khóa nhạy cảm trước khi gửi lên hệ thống.  