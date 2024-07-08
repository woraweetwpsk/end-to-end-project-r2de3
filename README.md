## End to End Project in Road to Data Engineer 3.0 By DataTH

เป็นโปรเจคใน Workshop ของคอร์ส Road to Data Engineer 3.0 By DataTH ซึ่งเป็น Project End to End ซึ่งใช้ Tool หลักๆอยู่บน Google Cloud Platform 
โดยใน Project จะมีการ Tranform ด้วย Pandas แต่ก็จะมี Workshop ที่ให้ Transform ข้อมูลด้วย Pyspark ด้วยจึงนำมาใส่เพิ่มเติมนอกเหนือจาก Project นี้

---

### รายละเอียด Folder
- **cleansing_data_with_pyspark**: เป็นการ transform โดยใช้ Pyspark ในรูปแบบของ Jupyter notebook และ python script
- **dags**: เป็น folder ที่เก็บไฟล์ dag ที่ใช้สำหรับทำ Data Pipeline บน Google Cloud Composer
- **setup**: เป็นการตั้งค่าการใช้งาน Google Cloud Composer สำหรับ Project นี้

---

### Architecture
![a](https://github.com/woraweetwpsk/end-to-end-project-r2de3/blob/main/images/architecture.png?raw=true)

### Tools
1. Orchestration: Google Cloud Composer
2. Data Lake: Google Cloud Storage
3. Data Warehouse: BigQuery
4. Data Visualization: Looker Studio
5. Language: Python

### DAG Task
![d](https://github.com/woraweetwpsk/end-to-end-project-r2de3/blob/main/images/dag.png?raw=true)

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
![dash1](https://github.com/woraweetwpsk/end-to-end-project-r2de3/blob/main/images/dashboard_!.png?raw=true)
![dash2](https://github.com/woraweetwpsk/end-to-end-project-r2de3/blob/main/images/dashboard_2.png?raw=true)

