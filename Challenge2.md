# **Challenge2**
- Đề bài gồm 1 file python encoder và 1 file flag đã bị encrypt
- 
[![file](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20191854.png "file")](http://https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20191854.png "file")



- Đọc hàm main chúng ta thấy chương trình chỉ cần một đầu vào là file cần encrypt và chương trình sẽ được encrypt với **key là 0x4b**  :
[![main](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20192139.png "main")](http://https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20192139.png "main")



- Hàm encrypt data: 

[![encr](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20192441.png "encr")](http://https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20192441.png "encr")
- Hàm encrypt này sẽ lấy từng bit của của byte rồi sử dụng phép toán** OR ** để nhét lại bit vào result..... , tóm lại đoạn này chỉ cần sử dụng lại hàm **bR** 1 lần nữa là chúng ta sẽ lấy được dữ liệu ban đầu :V 
Ví dụ :
**bR(0xab)=0xd5
bR(0xd5)=0xab **

- script mình dùng để giải :
[![script](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20194224.png "script")](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-30%20194224.png "script")
FLAG: KCSC{welc9me_t9_my_chall3ng3_easy_byte_reverse}
