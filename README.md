[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23573985&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** linh304204@gmail.com  
**Name:** Nguyen Thi Dieu Linh

---

## Mo ta

Bài lab này giới thiệu về **Xây dựng Automated ETL Pipeline** (Extract-Validate-Transform-Load). 

**Những gì được hoàn thành:**
-  **Extract (Trích xuất):** Đọc dữ liệu từ file JSON `raw_data.json` (5 records)
-  **Validate (Kiểm tra):** Lọc dữ liệu không hợp lệ (price ≤ 0, category rỗng) → 2 records bị loại
-  **Transform (Chuyển đổi):** Tính giá giảm 10% (discounted_price), chuẩn hóa category (Title Case), thêm timestamp
-  **Load (Lưu trữ):** Xuất 3 records hợp lệ ra file CSV `processed_data.csv`

**Kết quả:** 3 sản phẩm được xử lý thành công (Laptop, Chair, Monitor)

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
python agent_simulation.py
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

- **Tổng records được xử lý:** 5
- **Records hợp lệ:** 3 ✅
- **Records bị loại:** 2 ❌ (1 có giá âm, 1 có category rỗng)
- **Output file:** `processed_data.csv` (chứa các trường: id, product, price, category, discounted_price, processed_at)
