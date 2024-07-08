### Set Google Cloud Composer


1. สร้าง Composer 3 โดยที่หัวข้อ Environment resources จะตั้งแค่เป็น CUSTOM แล้วจะแก้ไขในหัวข้อ Worker ดังนี้
    - Maximum number of workers: 1
    - CPU: 1
    - Memory: 4
   
![1](https://github.com/woraweetwpsk/end-to-end-project-r2de3/blob/main/images/setup/1_setup_worker.png?raw=true)

2. ติดตั้ง Python Packages โดยติดตั้งที่ PYPI PACKAGES โดยจะทำการเพิ่มดังนี้
    - pymysql
    - sqlalchemy
    - pandas
    - requests

![2](https://github.com/woraweetwpsk/end-to-end-project-r2de3/blob/main/images/setup/2_setup_PYPI.png?raw=true)

3. ตั้งค่า Connections บน Airflow UI โดยตั้งค่าดังนี้
    - Connection Id: mysql_default
    - Connection Type: MySQL
    - Host:
    - Schema: 
    - Login: 
    - Password: 
    - Port:

![3](https://github.com/woraweetwpsk/end-to-end-project-r2de3/blob/main/images/setup/3_setup_connection.png?raw=true)

