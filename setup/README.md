### Set Google Cloud Composer

1. สร้าง Composer 3 โดยที่หัวข้อ Environment resources จะตั้งแค่เป็น CUSTOM แล้วจะแก้ไขในหัวข้อ Worker ดังนี้
    - Maximum number of workers: 1
    - CPU: 1
    - Memory: 4
2. ติดตั้ง Python Packages โดยติดตั้งที่ PYPI PACKAGES โดยจะทำการเพิ่มดังนี้
    - pymysql
    - sqlalchemy
    - pandas
    - requests
3. ตั้งค่า Connections บน Airflow UI โดยตั้งค่าดังนี้
    - Connection Id: mysql_default
    - Connection Type: MySQL
    - Host:
    - Schema: 
    - Login: 
    - Password: 
    - Port: 

