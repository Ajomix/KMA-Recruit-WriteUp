# Rand0m
- Bài Crypto này gồm 1 file encoder và 1 file có nội dung flag đã bị encrypt

[![](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-31%20181034.png)](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-31%20181034.png)

##### encoder:
[![](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-31%20181122.png)](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-31%20181122.png)

đọc qua các bạn có thể thấy chương trình đã tạo ra 1 dãy byte random theo seed random là giá trị 
của **magicNumber** và đem chuỗi này vào XOR vs từng byte flag để encode flag , vậy mấu chốt ở đây là cần tìm lại key là byte Random mà tác giả đã tạo ra, nếu chúng ta tìm được **magicNumber** thì chúng ta sẽ tìm được ra key random của tác giả tạo ra lúc đó .  Mà tác giả lại để 1 điều kiện rõ ràng ngay trên đầu là magicNumber <=0xFFFFFFFF

[![](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-31%20192226.png)](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-31%20192226.png)

vậy chúng ta đã có 1 giới hạn để có thể tìm được seed của tác giả , mình sẽ sử dụng bruteforce để tìm seed và điều kiện dừng ở đây sẽ là nếu chúng ta decrypt ra được 4 chữ đầu là **"KCSC"** thì mình sẽ dừng lại đây là script mình sử dụng :

[![](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-31%20192631.png)](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-31%20192631.png)

chạy script và flag :

[![](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-31%20192956.png)](https://raw.githubusercontent.com/dungbn123/KMA-Recruit-WriteUp/main/Screenshot%202022-01-31%20192956.png)
