# baitap2
Bài tập 2 của sv: K225480106056 - Hoàng Thị Quyến - Môn Hệ quản trị csdl
BÀI TẬP VỀ NHÀ 02 - MÔN HỆ QUẢN TRỊ CSDL:

DEADLINE: 23H59 NGÀY 25/03/2025

ĐIỀU KIỆN: (ĐÃ LÀM XONG BÀI 1)
1. Đã cài đặt SQL Server 2022 Dev.
2. Đã cài đặt SQL Managerment Studio bản mới nhất.
3. Đã kết nối từ SQL Managerment Studio vào SQL Server.
4. Đã có tài khoản github, biết cách tạo repository(kho lưu trữ) cho phép truy cập public.

BÀI TOÁN:
- Tạo csdl quan hệ với tên QLSV gồm các bảng sau:
  + SinhVien(#masv,hoten,NgaySinh)
  + Lop(#maLop,tenLop)
  + GVCN(#@maLop,#@magv,#HK)
  + LopSV(#@maLop,#@maSV,ChucVu)
  + GiaoVien(#magv,hoten,NgaySinh,@maBM)
  + BoMon(#MaBM,tenBM,@maKhoa)
  + Khoa(#maKhoa,tenKhoa)
  + MonHoc(#mamon,Tenmon,STC)
  + LopHP(#maLopHP,TenLopHP,HK,@maMon,@maGV)
  + DKMH(#@maLopHP,#@maSV,DiemTP,DiemThi,PhanTramThi)

YÊU CẦU:
1. Thực hiện các hành động sau trên giao diện đồ hoạ để tạo cơ sở dữ liệu cho bài toán:
  + Tạo database mới, mô tả các tham số(nếu có) trong quá trình.
  + Tạo các bảng dữ liệu với các trường như mô tả, chọn kiểu dữ liệu phù hợp với thực tế (tự tìm hiểu)
  + Mỗi bảng cần thiết lập PK, FK(s) và CK(s) nếu cần thiết. (chú ý dấu # và @: # là chỉ PK, @ chỉ FK)
2. Chuyển các thao tác đồ hoạ trên thành lệnh SQL tương đương. lưu tất cả các lệnh SQL trong file: Script_DML.sql


HÌNH THỨC LÀM BÀI:
1. Tạo repository mới, tạo file readme.md (có hướng dẫn trên zalo group)
2. Sinh viên thao tác trên máy tính cá nhân, chụp màn hình quá trình làm, chỉ cần chụp active window, thi thoảng chụp full màn hình để thấy sự cá nhân hoá.
3. Hình sau khi chụp paste trực tiếp vào file readme trên github, cần mô tả các phần trên ảnh để tỏ ra là hiểu hết!
4. upload các file liên quan: Script_DML.sql
5. Update link của repository vào cột bài tập 2 trên file excel online của thầy (đã ghim link trên zalo group)

    Bài làm
1. Tạo cơ sở dữ liệu

   
  ![image](https://github.com/user-attachments/assets/16dd854f-84e6-4983-9406-51ed98a6a168)

  

2.Tạo bảng dữ liệu



![image](https://github.com/user-attachments/assets/35c97bce-8e9a-4fc8-87ca-a7df8d55bbc2)



  Ta tạo tương tự và lưu các bảng như hình dưới đây theo đề bài 

  
![image](https://github.com/user-attachments/assets/7696a3be-acd4-4fd3-915a-ecaaff787fb9)




a. Bảng SinhVien(#masv,hoten,NgaySinh)


  ![image](https://github.com/user-attachments/assets/6a3ec1cb-8b12-44ff-bfdb-e553623e92ea)



  
  
b.Lop(#maLop,tenLop)





![image](https://github.com/user-attachments/assets/10befeb4-bb77-4e13-8a0c-998878946ddb)





c.GVCN(#@maLop,#@magv,#HK)




  ![image](https://github.com/user-attachments/assets/4861d758-999a-4d7e-93cd-b3a77435096a)





b.LopSV(#@maLop,#@maSV,ChucVu)





  ![image](https://github.com/user-attachments/assets/08ced5bb-1ea8-4a1f-b0e1-6a15dc793038)






c.GiaoVien(#magv,hoten,NgaySinh,@maBM)





  ![image](https://github.com/user-attachments/assets/958e3ea9-e005-4d8a-95c6-a3f990035ab5)






d.BoMon(#MaBM,tenBM,@maKhoa)






  ![image](https://github.com/user-attachments/assets/01a7c252-88a9-401f-a387-91bdbca6646c)







e.Khoa(#maKhoa,tenKhoa)






  ![image](https://github.com/user-attachments/assets/5382aa31-4afa-46f2-8562-24b2f04a06ce)





f.MonHoc(#mamon,Tenmon,STC)






  ![image](https://github.com/user-attachments/assets/59b0f83e-b884-4911-af25-1995b40f1911)







j.LopHP(#maLopHP,TenLopHP,HK,@maMon,@maGV)





  ![image](https://github.com/user-attachments/assets/8fedbe22-d7c1-4029-955f-f8923f442351)







k.DKMH(#@maLopHP,#@maSV,DiemTP,DiemThi,PhanTramThi)






  ![image](https://github.com/user-attachments/assets/2b0b09da-8e26-4b37-9076-845cb51e9d8e)





Thiết khóa PK, CK, FK cho bảng
Ngay sau khi tạo bảng ta gắn khóa chính






  ![image](https://github.com/user-attachments/assets/538a1669-428e-4614-be5d-ff1ca7a30b0a)






Ta làm tương tự với các bảng còn lại
Thiết lập khóa ngoại






  ![image](https://github.com/user-attachments/assets/f5aa36ae-829d-40a9-b0cf-f42df38e4376)






Làm tương tự với các khóa ngoại còn lại
Thiết lập CK





  ![image](https://github.com/user-attachments/assets/4c06771d-575f-4075-814b-34a692145700)





3. Chuyển thao tác đồ họa thành lệnh SQL





  ![image](https://github.com/user-attachments/assets/32c60088-2eae-4df6-a85a-dbe2197be511)










   
