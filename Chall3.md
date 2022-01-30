# Chall3
- Đề bài cho 1 file python và 1 file ảnh PNG 

[![](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20203221.png)](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20203221.png)

- file này là file **.pyc** nên mình dùng tool để decompile ra file **.py** ,
**TOOL**: https://github.com/rocky/python-uncompyle6/

- Sau decompile ta có file .py như sau :
**main:**
[![](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20204622.png)](http://https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20204622.png)

**LSB**:
[![](https://github.com/dungbn123/KMA-Recruit-WriteUp/blob/main/Screenshot%202022-01-30%20204805.png?raw=true)](http://https://github.com/dungbn123/KMA-Recruit-WriteUp/blob/main/Screenshot%202022-01-30%20204805.png?raw=true)

Bài này nhận hai đầu vào là Message muốn giấu và giấu vào file nào , 
đọc hàm **lsb** thì ta thấy nó chuyển hết Message Flag thành binary rồi **lấy từng bit giấu vào 24 pixel đầu của ảnh **, vậy nên công việc cần làm là đọc file encrypt và nhặt lại từng bit đã bị giấu vào file , script mình dùng để giải : 

[![](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20205545.png)](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20205545.png)

**flag :KCSC{congra!are_u_happy_now??}**
