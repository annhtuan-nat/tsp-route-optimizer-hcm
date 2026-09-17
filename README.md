# TSP Route Optimizer HCM

Ứng dụng tối ưu lộ trình dựa trên thuật toán Travelling Salesman Problem (TSP) tại Thành phố Hồ Chí Minh.

---

## Giới thiệu

**TSP Route Optimizer HCM** là ứng dụng được xây dựng nhằm giải bài toán **Travelling Salesman Problem (TSP)** trong phạm vi **Thành phố Hồ Chí Minh**. Người dùng có thể lựa chọn nhiều địa điểm trực tiếp trên bản đồ, chọn điểm xuất phát và sử dụng các thuật toán TSP để tìm lộ trình tối ưu.

Đây là đồ án môn **Phân tích và Thiết kế Giải thuật** tại Trường Đại học Giao thông Vận tải TP. Hồ Chí Minh (UTH).

---

## Mục tiêu của đề tài

* Xây dựng ứng dụng tối ưu lộ trình giữa nhiều địa điểm.
* So sánh hiệu quả của các thuật toán giải bài toán TSP.
* Hiển thị trực quan kết quả trên bản đồ Thành phố Hồ Chí Minh.
* Hỗ trợ người dùng lựa chọn thuật toán phù hợp với từng bài toán.

---

## Thuật toán được triển khai

Ứng dụng tích hợp ba thuật toán giải bài toán TSP:

| Thuật toán                          | Mô tả                                                    |
| ----------------------------------- | -------------------------------------------------------- |
| **Brute Force (Vét cạn)**           | Duyệt tất cả các lộ trình để tìm nghiệm tối ưu.          |
| **Held-Karp (Dynamic Programming)** | Quy hoạch động kết hợp Bitmask để giảm số lần tính toán. |
| **Nearest Neighbor (Heuristic)**    | Thuật toán tham lam chọn địa điểm gần nhất ở mỗi bước.   |

---

## Công nghệ sử dụng

* **Python 3.12**
* **Tkinter** – Xây dựng giao diện người dùng.
* **OpenStreetMap** – Hiển thị bản đồ.
* **TkinterMapView** – Hiển thị và tương tác với bản đồ.
* **Pillow (PIL)** – Tạo marker và biểu tượng trên bản đồ.
* **Math / Itertools / Time** – Xử lý khoảng cách và thuật toán.

---

## Chức năng chính

* Thêm địa điểm trực tiếp trên bản đồ.
* Xóa địa điểm đã chọn.
* Chọn điểm xuất phát.
* Tạo điểm ngẫu nhiên trong phạm vi TP. Hồ Chí Minh.
* Giải bài toán TSP bằng 3 thuật toán.
* Hiển thị tuyến đường tối ưu trên bản đồ.
* Hiển thị tổng khoảng cách và thời gian thực thi.
* So sánh kết quả của ba thuật toán trên cùng bộ dữ liệu.
* Mô phỏng quá trình di chuyển theo lộ trình.

---

## Cấu trúc thư mục

```text
tsp-route-optimizer-hcm/
│── main.py                 # Khởi chạy chương trình
│── gui.py                  # Giao diện người dùng
│── algorithms.py           # Các thuật toán TSP
│── graph.py                # Xây dựng ma trận khoảng cách
│── city_data.py            # Quản lý dữ liệu địa điểm
│── visualization.py        # Hiển thị bản đồ và tuyến đường
│── requirements.txt        # Danh sách thư viện
│── README.md               # Giới thiệu dự án
```

---

## Hướng dẫn cài đặt

### 1. Clone repository

```bash
git clone https://github.com/annhtuan-nat/tsp-route-optimizer-hcm.git
```

### 2. Di chuyển vào thư mục dự án

```bash
cd tsp-route-optimizer-hcm
```

### 3. Cài đặt thư viện

```bash
pip install -r requirements.txt
```

### 4. Chạy chương trình

```bash
python main.py
```

---

## Hướng dẫn sử dụng

1. Mở ứng dụng.
2. Bật chế độ **Thêm/Xóa điểm**.
3. Chọn các địa điểm trên bản đồ TP. Hồ Chí Minh.
4. Chọn điểm xuất phát.
5. Chọn thuật toán muốn sử dụng.
6. Nhấn **Giải TSP** để tìm lộ trình tối ưu.
7. Quan sát kết quả trên bản đồ hoặc sử dụng **So sánh 3 thuật toán**.

---

## Giao diện ứng dụng

Ứng dụng hiển thị trực tiếp trên bản đồ OpenStreetMap với các chức năng:

* Marker đánh dấu các địa điểm.
* Tuyến đường tối ưu.
* Chi tiết lộ trình.
* Tổng khoảng cách.
* Thời gian thực thi.
* So sánh ba thuật toán.

> Hình ảnh giao diện sẽ được cập nhật trong thư mục `images/`.

---

## Đánh giá thuật toán

| Tiêu chí                  | Brute Force | Held-Karp  | Nearest Neighbor |
| ------------------------- | ----------- | ---------- | ---------------- |
| Độ tối ưu                 | Tối ưu      | Tối ưu     | Gần tối ưu       |
| Thời gian thực thi        | Cao         | Trung bình | Thấp             |
| Phù hợp số lượng địa điểm | Ít          | Trung bình | Nhiều            |

---

## Hướng phát triển

* Tính khoảng cách theo mạng lưới đường giao thông thực tế.
* Tích hợp dữ liệu giao thông thời gian thực.
* Hỗ trợ nhập địa chỉ thay vì chọn điểm trên bản đồ.
* Bổ sung các thuật toán tối ưu khác như Genetic Algorithm và Ant Colony Optimization.
* Phát triển phiên bản Web và Mobile.

---

## Thông tin đề tài

**Tên đề tài:**

> **Xây dựng ứng dụng tối ưu lộ trình dựa trên thuật toán TSP tại Thành phố Hồ Chí Minh**

**Môn học:** Phân tích và Thiết kế Giải thuật

**Trường:** Trường Đại học Giao thông Vận tải Thành phố Hồ Chí Minh (UTH)

---

## Tác giả


Sinh viên Trường Đại học Giao thông Vận tải Thành phố Hồ Chí Minh (UTH).

---

## Giấy phép

Dự án được thực hiện phục vụ mục đích học tập và nghiên cứu trong môn **Phân tích và Thiết kế Giải thuật**.
