1. Các file mô hình:
- model_config.json: file lưu các siêu tham số.
- model_weight.h5: file lưu các trọng số mô hình.
Mục đích lưu file mô hình thành hai file riêng để tiện cho việc thống kê.
2. Dữ liệu kiểm thử (test set):
- test.pkl: là tập kiểm thử chứa tổng cộng 893 sentences.
- dicts.pkl: là tập bắt buộc cần có để đối chiếu từ (mapping word) trong Word Embedding.
- Lưu ý: result.json là file cấu trúc lưu thông tin
3. Load mô hình và Predict kết quả:
- Chạy cmd: python Predict.py
- File kết quả được lưu trong thư mục Result
4. Thư mục Result gồm:
- model_config.json và model_weight.h5: lưu lại các file thông tin mô hình dùng cho thống kê.
- test.txt: kết quả dự đoán
- result.json: cho biết thông tin độ lỗi đạt được
5. Cấu trúc file test.txt
- Các câu được tách ra thành từng từ riêng biệt và được đặt trong cặp kí hiệu BOS và EOS.
- Với mỗi từ, ta sẽ có 2 nhãn: nhãn thứ nhất là nhãn mô hình dự đoán được và nhãn thứ hai là nhãn đúng.