# 🏡 USA Real Estate Price Prediction & Data Analysis
โครงการวิเคราะห์และทำนายราคาอสังหาริมทรัพย์ในสหรัฐอเมริกาด้วยเทคนิคการเรียนรู้ของเครื่อง (Machine Learning) และพีชคณิตเชิงเส้น (Linear Algebra)

---

## 📌 1. รายละเอียดโครงการ (Project Overview)
โครงการนี้จัดทำขึ้นโดยเป็นส่วนหนึ่งของรายวิชา **201 คณิตศาสตร์สำหรับวิทยาการข้อมูล (Mathematics for Data Science)** ประจำภาคการศึกษา 1/2568  

* **วัตถุประสงค์:** เพื่อศึกษาคุณลักษณะและปัจจัยที่มีผลต่อราคาอสังหาริมทรัพย์ เช่น จำนวนห้องนอน จำนวนห้องน้ำ พื้นที่ที่ดิน และพื้นที่ใช้สอย พร้อมทั้งพัฒนาและประเมินประสิทธิภาพของโมเดลเชิงสถิติและการเรียนรู้ของเครื่องสำหรับทำนายราคาขาย (`price`)
* **ชุดข้อมูล (Dataset):** USA Real Estate Dataset (`realtor-data.zip.csv`) จาก Kaggle / Realtor.com

---

## 👥 2. สมาชิกในกลุ่ม (Group Members)
1. **นายอิศม์เดช บุญจรัส** (รหัสนักศึกษา: 68114540753)
2. **นายไชยวัฒน์ ทำดี** (รหัสนักศึกษา: 68114540155)

---

## 🛠️ 3. โครงสร้างการวิเคราะห์และโมเดล (Workflow & Methodology)

### 3.1 Exploratory Data Analysis (EDA) & Data Preprocessing
* สำรวจการกระจายตัวของราคาอสังหาริมทรัพย์ (Target Variable Distribution)
* วิเคราะห์ค่าทางสถิติเบื้องต้น (`.describe()`) และจัดการค่าผิดปกติ (Outliers)
* สร้าง Correlation Heatmap เพื่อประเมินความสัมพันธ์ระหว่างปัจจัยต่างๆ

### 3.2 Linear Algebra Analysis (CLO1)
* ประยุกต์ใช้เทคนิค **PCA (Principal Component Analysis)** ในการลดมิติของข้อมูล (Dimensionality Reduction) โดยคำนวณผ่าน Covariance Matrix และ Eigendecomposition
* วิเคราะห์ความแปรปรวนสะสมด้วย Scree Plot เพื่อคัดเลือกองค์ประกอบหลัก (Principal Components) ที่เหมาะสม

### 3.3 Statistical Learning & Model Evaluation (CLO2 - CLO4)
* **Statistical Learning Analysis:** วิเคราะห์โครงสร้างข้อมูลเพื่อเลือกโมเดลประเภท Regression และศึกษา Bias-Variance Tradeoff ผ่าน Model Complexity
* **Model Building:** เปรียบเทียบประสิทธิภาพระหว่าง **Simple Linear Regression** (ใช้ปัจจัยเดี่ยวที่มีความสัมพันธ์สูงสุด) และ **Multiple Linear / Regularized Regression** (ใช้ปัจจัยทั้งหมด)
* **Model Selection:** ประเมินและเปรียบเทียบโมเดลด้วย **5-Fold Cross-Validation** เพื่อลดการ Overfitting และคัดเลือกโมเดลที่มีค่า Root Mean Squared Error (RMSE) ต่ำที่สุด

---

## 📁 4. โครงสร้างไฟล์ใน Repository (Repository Structure)
```text
├── .gitignore                    # ไฟล์กำหนดรายการที่ไม่บันทึกขึ้น Git
├── README.md                     # เอกสารอธิบายรายละเอียดโครงการ
├── realtor-data.zip.csv          # ชุดข้อมูลอสังหาริมทรัพย์ (USA Real Estate Dataset)
└── lab15_project_template.ipynb  # Jupyter Notebook สรุปโค้ดและการวิเคราะห์ทั้งหมด
