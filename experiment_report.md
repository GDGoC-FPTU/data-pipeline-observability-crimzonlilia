# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** AI20K-0209  
**Name:** Nguyen Thi Dieu Linh  
**Date:** 15/04/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario                          | Agent Response                                                   | Accuracy (1-10) | Notes                                                                |
| --------------------------------- | ---------------------------------------------------------------- | --------------- | -------------------------------------------------------------------- |
| Clean Data (`processed_data.csv`) | Based on my data, the best choice is Laptop at $1200.            | 9               | Du lieu sach, gia tri hop ly, agent dua ra ket qua chinh xac         |
| Garbage Data (`garbage_data.csv`) | Based on my data, the best choice is Nuclear Reactor at $999999. | 2               | Du lieu sai lech, co outlier lon, agent bi dan dat den ket qua vo ly |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

(Viet nhan xet cua ban o day — it nhat 50 tu)

(Hay phan tich cac van de nhu Duplicate IDs, wrong data types, outliers, null values
va giai thich tai sao chung anh huong den ket qua cua Agent.)  

Agent đưa ra kết quả sai khi sử dụng garbage data vì chất lượng dữ liệu đầu vào không được đảm bảo. Trước hết, duplicate IDs có thể khiến agent hiểu nhầm rằng một số mục xuất hiện nhiều lần nên có độ quan trọng cao hơn thực tế. Bên cạnh đó, việc sai kiểu dữ liệu (wrong data types), ví dụ như giá được lưu dưới dạng chuỗi hoặc chứa giá trị không hợp lệ, sẽ làm quá trình xử lý và so sánh bị sai lệch.  
Ngoài ra, sự xuất hiện của outliers như mức giá $999999 của “Nuclear Reactor” khiến agent bị lệch trong quá trình đánh giá, vì hệ thống không có cơ chế kiểm soát giá trị bất thường. Các giá trị null cũng làm thiếu thông tin quan trọng, dẫn đến việc suy luận dựa trên dữ liệu không đầy đủ. Tổng hợp các vấn đề này khiến agent không phân biệt được dữ liệu hợp lệ và dữ liệu sai, từ đó đưa ra quyết định không chính xác.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** (Dong y hay khong? Giai thich ngan gon.) Dong y

(Viet ket luan cua ban o day)

Chất lượng dữ liệu có ảnh hưởng trực tiếp và quyết định đến kết quả của AI agent. Dù prompt được thiết kế tốt đến đâu, nếu dữ liệu đầu vào bị nhiễu, sai lệch hoặc không đầy đủ thì kết quả vẫn sẽ không đáng tin cậy. Vì vậy, đảm bảo dữ liệu sạch và chính xác là yếu tố quan trọng hơn trong các hệ thống AI.