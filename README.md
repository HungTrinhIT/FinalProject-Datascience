<h1>BÁO CÁO ĐỒ ÁN CUỐI KÌ - KHOA HỌC DỮ LIỆU ỨNG DỤNG</h1>

<h2>1. Thành viên nhóm và phân công</h2>

* Thành viên 
  * Trịnh Vũ Minh Hùng, MSSV: 1712049
  * Nguyễn Văn Khoa, MSSV: 1712072    
* Phân công:
    | Thành viên | Công việc |
    | ----------- | ----------- |
    | Trịnh Vũ Minh Hùng | <ul> <li>Phát biểu bài toán, đặt ra câu hỏi từ đó đặt ra các yêu cầu để thu thập dữ liệu</li><li>Thu thập dữ liệu nhà ở và trung cư từ trang [Chợ tốt](https://nha.chotot.com/)</li><li>Clean data</li><li>Viết báo cáo</li></ul>  |
    | Nguyễn Văn Khoa  | <ul><li>Thu thập dữ liệu từ trang [Chợ tốt](https://nha.chotot.com/)</li><li>Visualize các cột dữ liêụ để xây dựng dataset cho  bước training</li><li>Training với mô hình **Linear Regression** và đưa ra nhận xét</li></ul> |

<h2>2. Tổng quan đồ án</h2>

2.1. **Phát biểu bài toán**

- **Bài toán 1:** Dự đoán giá chung cư khu vực thành phố Hồ Chí Minh với tập dữ liêụ 24949 entries từ trang [Chợ tốt](https://nha.chotot.com/)
- **Bài toán 2:** Đánh giá rating 
  
2.2. **Quá trình thực hiện đồ án** : trải qua 2 giai đoạn vơí hai bài toán khác nhau

  - **Giai đoạn 1**: Ở giai đoạn này, nhóm hướng đến bài toán **dự đoán giá chung cư và nhà ở** của khu vực **thành phố Hồ Chí Minh**. Sau đó, sử dụng phương pháp **parse HTML** để thu thập dữ liệu từ trang [Chợ tốt](https://nha.chotot.com/).
    - Thông tin về dữ liệu thu thập được: ![Dữ liệu về chung cư](./images/chotot_data1.png)<br>
    - Vấn đề: Ở đây dữ liệu thiếu khá nhiều, và sẽ có một số cột không ảnh hưởng đến output giá chung cư nên sẽ phải tiền xử lý, trực quan hoá các cột dữ liệu để tìm ra dữ liệu nào được giữ lại để xây dựng cho quá trình traning ***(tiền xử lý và EDA dữ liệu sẽ được trình bày bên dưới)***

  - **Giai đoạn 2**: Sau khi thực hiện xong đồ án, nhóm thấy sai số của output là khá cao hơn 1 tỷ VNĐ. Lý do, bộ dữ liêụ thu thập được là không tốt ảnh hưởng lớn đến quá trình traning do đó nhóm đã làm thêm 1 bài toán khác đó là




<h2>3. Phân tích chi tiết</h2>

**3.1. Bài toán 1:**
  
  - Dữ liệu sau khi thu thập được bao gồm 24949 dòng: ![Dữ liệu chung cư](./images/chotot_data2.png)
  - Mô tả các biến:
    - **DiaChi:** địa chỉ của chung cư, ở thành phố Hồ Chí Minh
    - **TinhTrangBDS:** là chung cư này đã bàn giao chưa, hay vẫn còn đang trong quá trìnhg xây dựng. 
    - **DienTich:** diện tích thực ở(sử dụng) trên sổ hồng, đơn vị: **triệu/m2**.
    - **PhongNgu:** số lượng phòng ngủ.
    - **TenPhanKhu:** căn hộ đó thuộc block nào trong khu chung cư ấý. Vì 1 khu chung cư có rất nhiều block, các block ở vị trí khác nhau sẽ có giá khác nhau.
    - **SoTang:** căn hộ nằm ở tầng thứ mấy.
    - **PhongTam:** số lượng nhà vệ sinh.
    - **Loại:** chung cư hay nhà ở xã hội.
    - **GiayTo:** giấy tờ pháp lý của căn hộ, có đang tranh chấp hay không, có hợp pháp hay không.
    - **MaCanHo:** mã căn hộ (giống như số nhà).
    - **TinhTrangNoiThat:** căn hộ đã có nội thất hay chưa(sofa, lò vi sóng, máy lạnh,...).
    - **HuongCuaChinh:** hướng cửa chính của căn hộ.
    - **HuongBanCong:** hướng ban công của căn hộ.
    - **DacDiem:** Đặc điểm căn hộ ( căn trong góc, hay căn chính giữa,...).
    - **Gia:** giá bán của căn hộ.








 