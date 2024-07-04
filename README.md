<p align="center">
  <a href="https://www.uit.edu.vn/" title="Trường Đại học Công nghệ Thông tin" style="border: 5;">
    <img src="https://i.imgur.com/WmMnSRt.png" alt="Trường Đại học Công nghệ Thông tin | University of Information Technology">
  </a>
</p>

<!-- Title -->
<h1 align="center"><b>MACHINE LEARNING</b></h1>


## THÔNG TIN NHÓM
<a name="gioithieubanthan"></a>
1. 22521309
  - Họ và Tên: Phạm Huỳnh Nhật Tân
  - Số buổi vắng: 0
  - Số bài tập quá trình: 9
  - Điểm WeCode: 3346

2. 22520240
  - Họ và Tên: Triệu Tấn Đạt
  - Số buổi vắng: 1
  - Số bài tập quá trình: 9
  - Điểm WeCode: 2635

3. 22521610
  - Họ và Tên: Phạm Nguyễn Anh Tuấn
  - Số buổi vắng: 2
  - Số bài tập quá trình: 6
  - Điểm WeCode:3070

# Danh sách thành viên:
| Họ và tên      | MSSV | Lớp     |
| :----:        |    :----:   |          :----: |
| [Phạm Huỳnh Nhật Tân](https://github.com/tanphn?tab=repositories)      | 22521309       | CS114.O21  |
| [Phạm Nguyễn Anh Tuấn](https://github.com/nguoimay1103?tab=repositories)   | 22521610        | CS114.O21     |
| [Triệu Tấn Đạt](https://github.com/nguoimay1103?tab=repositories)   | 22520240       | CS114.O21     |

## GIẢNG VIÊN HƯỚNG DẪN
<a name="giangvien"></a>
* PGS.TS. *Lê Đình Duy* - duydl@uit.edu.vn
* ThS. *Phạm Nguyễn Trường An* - truonganpn@uit.edu.vn
# THÔNG TIN ĐỒ ÁN - THỰC HÀNH
### 1. Trang github của nhóm 

### 2. Đồ án cuối kỳ: MotocycleClassification
- Tổng số lượng ảnh đóng góp: 267 (Honda: 53, Suzuki: 54, Yamaha: 51, VinFast: 42, Others: 67).
  + Phương pháp thu thập ảnh: Hình ảnh được thu thập từ Internet, hội nhóm mua bán xe cũ trên Facebook, trang web của các đại lý bán xe.
  + Cách làm sạch dữ liệu ảnh: Những hình ảnh mờ, kích thước quá nhỏ hoặc quá to, xe chiếm dưới 70% tổng thể bức ảnh sẽ được loại bỏ thủ công.
- Phương pháp rút trích đặc trưng sử dụng: MobileNetV2
  + Trước đó, chúng em sẽ sử dụng model YOLOv5 để phát hiện xe máy cho từng ảnh sau đó sẽ cắt ảnh theo bounding box (trong trường hợp mô hình phát hiện ra nhiều xe máy thì sẽ lấy ảnh có bounding box lớn nhất). Ảnh sau khi được cắt sẽ là đầu vào của mô hình MobileNetV2 để rút trích đặc trưng. Dữ liệu sau khi được rút trích ở: https://drive.google.com/drive/folders/1WIucfV6HysjMAsKIb7r6JbQfM9JjPAyZ
- Thuật toán học được sử dụng: LogisticRegression
- Framework, thư viện sử dụng: os, pandas, numpy, tensorflow,torchvision, pathlib, PIL, torch, sklearn, cv2, random, csv, matplotlib, MobileNetV2,
- Kết quả Accuracy: split1: 72.41, split2: 71.87, split3: 72.02, split4: 73.29, split5: 72.41.

### 3. Danh sách các bài thực hành đã làm - điền thời điểm (ngày, giờ) nộp bài trên Classroom:
- Thống kê dữ liệu (CS114.Tool.DatasetStat.ipynb): 2:40 AM, Jun 08
- Tạo các splits (CS114.Tool.CreateSplit.ipynb): Jun 9
- Hiển thị các ảnh (CS114.Tool.DatasetViz.ipynb): Jun 9
- Ứng dụng Clustering (CS114.Clustering.ipynb): Jun 10
- Đánh giá Model (CS114.Evaluation.ipynb): Jun 14

### 4. Bài tập - Dự đoán điểm IT001
- Mô tả về đặc trưng:
  + attend: Tổng số lượng problem mà user đó đã tham gia
  + attend_rate: Tỉ lệ tham gia của user đó (Tổng số lượng problem tham gia / Tổng số lượng problem có trong từng assignment mà user đó tham gia).
  Ví dụ: user tham gia 10 assignment. Mỗi assignment có 10 problem. Tuy nhiên user đó chỉ tham gia 9 problem trong mỗi assigment. Khi đó attend_rate sẽ có giá trị = 90/100 = 0.9
  + avg_score: Điểm trung bình của user đó. Tổng điểm của từng problem (lấy điểm lớn nhất của từng problem, những problem không tham gia sẽ tính là 0 điểm) / Tổng số lượng problem có trong từng assignment mà user đó tham gia
  các code đã dùng để rút trích đặc trưng, kết quả rút trích lưu trữ quản lý thế nào?
  + avg_submit: Số lần submit trung bình cho từng problem tham gia (Chỉ tính những problem tham gia). Tổng số lần submit của user / Tổng số lượng problem mà user đó đã tham gia (attend)
  + avg_finishtime: Thời gian hoàn thành trung bình cho từng problem (tính bằng giờ). Tổng thời gian của lần submit cuối cùng cho từng problem / Tổng số lượng problem mà user đó đã tham gia (attend)
  + late_rate: tỉ lệ trễ deadline của user đó. Tổng số assignment trễ / Tổng số assignment mà user đó tham gia. Ví dụ một user tham gia 10 assignment và hoàn thành muộn 1 hoặc một vài problem trong 1 assignment nào đó. Khi đó late_rate = 1/10 = 0.1
- Code đã được chúng em chú thích rõ ràng trong file: https://colab.research.google.com/drive/182cbSXcVQSyt2PJ3bkxpVenAOCe0fMmN?usp=sharing
- Thuật toán học, quá trình huấn luyện và thử nghiệm?
  + Chúng em sử dụng thật toán Random Forest Regression đồng thời sử dụng GridSearchCV để tìm ra bộ tham số tốt nhất của mô hình
  + Quá trình huấn luyện được mô tả trong file trên
  + Thử nghiệm: kết quả thu được cho từng bài (Đánh giá theo R^2)
    + Dự đoán điểm TBTL: 19/100
    + Dự đoán điểm thực hành: 27/100
    + Dự đoán điểm quá trình: 11/100
    + Dự đoán điểm cuối kì: 18/100
### 5. Bài tập - Nhận dạng chữ số viết tay
- Mô tả về dữ liệu đóng góp: Dữ liệu gồm 3 ảnh cho mỗi số từ 0 đến 9, được chụp từ chữ viết tay của mỗi sinh viên. Tổng cộng 30 ảnh trên mỗi sinh viên
- Mô tả về đặc trưng và thuật toán học
  + Thuật toán học: chúng em sử dụng mô hình như trong file thầy đã cung cấp.
  Đó là mô hình mạng nơ-ron tích chập (Convolutional Neural Network - CNN) sử dụng thư viện Keras với backend là TensorFlow. Mô hình này thường được sử dụng để nhận dạng các hình ảnh, chẳng hạn như phân loại chữ số viết tay trong bộ dữ liệu MNIST
  + Đặc trưng:
    + Làm mờ ảnh (Gaussian Blur)
    + Chuyển đổi ảnh sang nhị phân (Binary Thresholding): Sử dụng ngưỡng Otsu để chuyển đổi ảnh xám sang nhị phân
    + Chuẩn hóa giá trị pixel: Chuyển đổi giá trị pixel từ 0-255 về khoảng 0-1 để phù hợp với yêu cầu đầu vào của mô hình học sâu.
    + Đảo ngược giá trị pixel: Đảo ngược giá trị pixel để phù hợp với định dạng đầu vào của mô hình.
- Code của bài tập: https://colab.research.google.com/drive/1LoP9T0rgrorK2H2OVkd50TcyDSWkUlhg?usp=sharing

  => Kết quả thu được của chúng em chỉ 518 điểm. Sau đó, chúng em gán nhãn ảnh bằng phương pháp thủ công để thu được số điểm 981 điểm
## MÔ TẢ HỖ TRỢ CỦA CÁC CÔNG CỤ NHƯ CHATGPT, GEMINI, POE

- Chúng em sử dụng ChatGPT để:
  + Tìm hiểu cú pháp, tham số, chức năng của các hàm trong đồ án.
  + Hỗ trợ debug
  + Đưa ra đánh giá để cải thiện mô hình
  + Chọn ra phương pháp trích xuất đặc trưng, thuật toán máy học
  + Gợi ý các đặc trưng cho competition thứ 2
  + Giải thích rõ ràng để giúp hiểu hơn về code

