## End to End Project in Road to Data Engineer 3.0 By DataTH

---
### รายละเอียด Folder
- **cleansing_data_with_pyspark**: เป็นการ transform โดยใช้ Pyspark ในรูปแบบของ Jupyter notebook และ python script
- **dags**: เป็น folder ที่เก็บไฟล์ dag ที่ใช้สำหรับทำ Data Pipeline บน Google Cloud Composer
- **setup**: เป็นการตั้งค่าการใช้งาน Google Cloud Composer สำหรับ Project นี้

---

### Architecture

### Tools
1. Orchestration: Google Cloud Composer
2. Data Lake: Google Cloud Storage
3. Data Warehouse: BigQuery
4. Data Visualization: Looker Studio
5. Language: Python

### DAG Task
1. ดึง Data จาก MySQL
    - ดึง Data จาก MySQL
    - Merge Data จาก 3 Table ที่ดึงมา
    - Save file เป็น Parquet ใน Google Cloud Storage
2. ดึง Data จาก API 
    - ดึง Data จาก API มาอยู่ในรูปแบบของ Pandas DataFrame
    - ลบ Column "id" แล้วเปลี่ยน type ของ Column "date" ให้อยู่ในรูปแบบ date
    - Save file เป็น Parquet ใน Google Cloud Storage
3. Transform ข้อมูลจาก Data 2 แหล่งแล้วนำมารวมกัน
4. Upload จาก Google Cloud Storage ไปยัง BigQuery

### Dashboard

