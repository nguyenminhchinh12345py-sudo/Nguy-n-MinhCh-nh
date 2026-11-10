# Hệ thống đặt lịch tư vấn tâm lý và pháp lý cho sinh viên

> **Trạng thái tài liệu:** Bản khởi thảo yêu cầu và thiết kế.  
> **Lưu ý:** Issue dự án có đính kèm `Tai_lieu_du_an_chia_the_ghi_chu.docx` và `PRD_Dat_lich_tu_van_tam_ly_va_phap_ly.docx`, nhưng nội dung tệp chưa được đọc trong phiên này. Vì vậy, nội dung dưới đây được xây dựng từ tên dự án và cần được đối chiếu, cập nhật theo hai tài liệu gốc trước khi xem là yêu cầu đã chốt.

## 1. Tổng quan

Hệ thống giúp sinh viên tìm kiếm dịch vụ tư vấn tâm lý hoặc pháp lý, xem thông tin chuyên viên, chọn khung giờ phù hợp và quản lý lịch hẹn. Hệ thống cũng hỗ trợ chuyên viên quản lý lịch làm việc và hỗ trợ người quản trị vận hành dịch vụ.

### Mục tiêu

- Giúp sinh viên đặt, xem, đổi hoặc hủy lịch thuận tiện.
- Hạn chế trùng lịch và giúp chuyên viên quản lý lịch hẹn tập trung.
- Bảo vệ thông tin cá nhân và thông tin nhạy cảm của người sử dụng.
- Cung cấp quy trình rõ ràng để sinh viên biết trạng thái lịch hẹn và cách nhận hỗ trợ.

### Nguyên tắc thiết kế

1. **Riêng tư trước tiên:** chỉ thu thập dữ liệu cần thiết, giới hạn người được xem.
2. **Tôn trọng và không phán xét:** ngôn từ thân thiện, dễ hiểu, phù hợp với sinh viên.
3. **Minh bạch:** hiển thị rõ loại tư vấn, thời lượng, hình thức, quy định đổi/hủy và trạng thái lịch.
4. **An toàn:** hệ thống đặt lịch không thay thế dịch vụ cấp cứu, chẩn đoán y khoa hoặc tư vấn pháp lý chính thức.
5. **Dễ tiếp cận:** giao diện hoạt động tốt trên điện thoại và hỗ trợ người dùng có nhu cầu tiếp cận khác nhau.

## 2. Phạm vi dự kiến

### Trong phạm vi

- Đăng ký, đăng nhập và quản lý hồ sơ cơ bản.
- Xem danh mục tư vấn tâm lý và pháp lý.
- Xem hồ sơ chuyên viên và các khung giờ còn trống.
- Tạo, xem, đổi hoặc hủy lịch theo chính sách được cấu hình.
- Nhận thông báo về việc đặt lịch và thay đổi trạng thái.
- Chuyên viên quản lý giờ làm việc và lịch hẹn.
- Quản trị viên quản lý người dùng, dịch vụ, chuyên viên và báo cáo vận hành ở mức phù hợp.

### Ngoài phạm vi (cần xác nhận)

- Chẩn đoán, điều trị hoặc đưa ra kết luận tự động về tình trạng tâm lý.
- Hệ thống tự động đưa ra lời khuyên pháp lý có tính ràng buộc.
- Thanh toán trực tuyến, tích hợp hồ sơ bệnh án hoặc hồ sơ pháp lý bên ngoài.
- Ghi âm hoặc ghi hình buổi tư vấn.

> Các mục trên chỉ được đưa vào phạm vi khi có yêu cầu, đánh giá rủi ro và quy trình bảo vệ dữ liệu phù hợp.

## 3. Đối tượng sử dụng và quyền hạn

| Vai trò | Nhu cầu chính | Quyền dự kiến |
|---|---|---|
| Sinh viên | Tìm và đặt lịch tư vấn | Quản lý hồ sơ và lịch của chính mình; xem thông tin dịch vụ công khai |
| Chuyên viên | Quản lý lịch làm việc và buổi tư vấn | Quản lý khung giờ, xem lịch được phân công và cập nhật trạng thái cần thiết |
| Quản trị viên | Vận hành hệ thống | Quản lý tài khoản, dịch vụ, chuyên viên và cấu hình; quyền truy cập dữ liệu nhạy cảm cần bị giới hạn và ghi nhật ký |

## 4. Quy trình chính

### Đặt lịch của sinh viên

1. Sinh viên đăng nhập hoặc tạo tài khoản.
2. Chọn loại tư vấn: tâm lý hoặc pháp lý.
3. Xem thông tin dịch vụ, chuyên viên, hình thức tư vấn và thời lượng.
4. Chọn ngày, giờ còn trống và cung cấp thông tin tối thiểu cần thiết cho buổi hẹn.
5. Xác nhận yêu cầu đặt lịch.
6. Hệ thống kiểm tra khung giờ lần cuối để tránh đặt trùng.
7. Hệ thống tạo lịch và thông báo kết quả cùng trạng thái hiện tại.
8. Sinh viên có thể xem, đổi hoặc hủy lịch theo chính sách.

### Xử lý lịch của chuyên viên

1. Chuyên viên thiết lập hoặc cập nhật giờ làm việc.
2. Hệ thống hiển thị lịch được phân công.
3. Chuyên viên cập nhật trạng thái buổi hẹn theo quy trình vận hành.
4. Nếu cần thay đổi lịch, hệ thống thông báo cho sinh viên và lưu lại lịch sử thay đổi.

## 5. Yêu cầu chức năng dự kiến

- **FR-01 – Tài khoản:** đăng ký, đăng nhập, đăng xuất và khôi phục quyền truy cập.
- **FR-02 – Hồ sơ:** người dùng xem và cập nhật thông tin cá nhân được phép chỉnh sửa.
- **FR-03 – Danh mục dịch vụ:** hiển thị loại tư vấn, mô tả, hình thức, thời lượng và điều kiện tham gia.
- **FR-04 – Tìm chuyên viên:** lọc theo loại tư vấn, lịch trống hoặc tiêu chí công khai đã được duyệt.
- **FR-05 – Đặt lịch:** chỉ cho phép đặt khung giờ còn trống; xác nhận rõ thông tin trước khi gửi.
- **FR-06 – Quản lý lịch:** xem chi tiết, đổi hoặc hủy lịch theo quy định.
- **FR-07 – Quản lý lịch làm việc:** chuyên viên tạo và cập nhật khung giờ khả dụng.
- **FR-08 – Trạng thái lịch:** hỗ trợ các trạng thái như `cho_xac_nhan`, `da_xac_nhan`, `da_huy`, `hoan_thanh` hoặc `vang_mat` (cần thống nhất nghiệp vụ).
- **FR-09 – Thông báo:** gửi thông báo khi có yêu cầu đặt lịch hoặc thay đổi lịch; không đưa nội dung nhạy cảm vào thông báo không bảo mật.
- **FR-10 – Quản trị:** quản lý dịch vụ, tài khoản, chuyên viên và cấu hình quyền.
- **FR-11 – Nhật ký:** ghi lại thao tác quan trọng liên quan đến lịch và quyền truy cập dữ liệu.

## 6. Yêu cầu phi chức năng

- **Bảo mật:** xác thực an toàn, phân quyền theo vai trò, mã hóa kết nối và bảo vệ dữ liệu lưu trữ phù hợp.
- **Riêng tư:** không thu thập thông tin về vấn đề tư vấn nếu không thực sự cần; có thông báo mục đích sử dụng và thời hạn lưu trữ.
- **Toàn vẹn lịch:** hai yêu cầu đặt cùng một khung giờ không được đồng thời thành công.
- **Tính sẵn sàng:** thông báo rõ khi hệ thống lỗi; không tạo lịch nửa chừng khi thao tác thất bại.
- **Khả năng sử dụng:** giao diện tiếng Việt rõ ràng, hoạt động trên màn hình nhỏ và có trạng thái lỗi dễ hiểu.
- **Khả năng bảo trì:** tách biệt giao diện, nghiệp vụ và lưu trữ dữ liệu; có kiểm thử tự động cho các luồng chính.
- **Khả năng truy vết:** ghi nhật ký sự kiện quản trị và thay đổi lịch, tránh ghi nội dung tư vấn nhạy cảm vào log.

## 7. Dữ liệu cốt lõi (đề xuất)

Các bảng/đối tượng dưới đây là gợi ý ban đầu, cần điều chỉnh theo PRD và công nghệ được chọn.

### `NguoiDung`

- `id`: mã định danh.
- `ho_ten`: tên hiển thị.
- `email`: email đăng nhập hoặc liên hệ.
- `vai_tro`: `sinh_vien`, `chuyen_vien`, `quan_tri_vien`.
- `trang_thai`: trạng thái tài khoản.
- `created_at`, `updated_at`: thời điểm tạo/cập nhật.

### `ChuyenVien`

- `id`, `nguoi_dung_id`.
- `loai_tu_van`: tâm lý, pháp lý hoặc loại được phê duyệt.
- `gioi_thieu`: nội dung giới thiệu công khai đã được duyệt.
- `trang_thai_xac_minh`: trạng thái xác minh thông tin chuyên môn.

### `KhungGio`

- `id`, `chuyen_vien_id`.
- `bat_dau_luc`, `ket_thuc_luc`.
- `hinh_thuc`: trực tiếp hoặc trực tuyến (nếu được hỗ trợ).
- `trang_thai`: còn trống, đã đặt, không khả dụng.

### `LichHen`

- `id`, `sinh_vien_id`, `chuyen_vien_id`, `khung_gio_id`.
- `loai_tu_van`, `hinh_thuc`.
- `trang_thai`, `ly_do_huy` (nếu cần và được phép lưu).
- `created_at`, `updated_at`.

> Không nên lưu nội dung trao đổi trong buổi tư vấn vào bản ghi lịch hẹn. Nếu nghiệp vụ bắt buộc lưu dữ liệu nhạy cảm, cần có đánh giá pháp lý, chính sách đồng ý, thời hạn lưu trữ, phân quyền chặt chẽ và biện pháp bảo vệ riêng.

## 8. Quy tắc nghiệp vụ quan trọng

- Khung giờ phải có thời điểm bắt đầu trước thời điểm kết thúc.
- Không cho phép đặt một khung giờ đã được giữ hoặc đã có lịch hợp lệ.
- Việc kiểm tra và giữ khung giờ phải được thực hiện nguyên tử ở phía máy chủ/cơ sở dữ liệu, không chỉ dựa vào giao diện.
- Chỉ người sở hữu lịch hoặc nhân sự có quyền phù hợp mới được xem/thay đổi lịch.
- Quy tắc đặt trước, đổi lịch, hủy lịch, thời gian đệm và xác nhận của chuyên viên cần được cấu hình và thống nhất với PRD.
- Múi giờ cần được xác định thống nhất; lưu thời gian theo chuẩn phù hợp và hiển thị theo múi giờ người dùng/cơ sở.
- Trạng thái lịch chỉ chuyển theo các bước hợp lệ, ví dụ không thể chuyển lịch đã hủy thành đã hoàn thành nếu không có thao tác được phân quyền.

## 9. Mẫu mã minh họa

Đoạn mã dưới đây là **mã giả JavaScript** để minh họa quy tắc kiểm tra lịch. Đây chưa phải mã triển khai và cần được điều chỉnh theo framework, cơ sở dữ liệu và quy tắc thực tế.

```js
// Mã giả: tạo lịch hẹn an toàn, tránh đặt trùng khung giờ.
async function datLichHen(yeuCau, nguoiDungHienTai) {
  if (!nguoiDungHienTai || nguoiDungHienTai.vaiTro !== "sinh_vien") {
    throw new Error("Bạn cần đăng nhập bằng tài khoản sinh viên.");
  }

  if (!yeuCau.chuyenVienId || !yeuCau.khungGioId || !yeuCau.loaiTuVan) {
    throw new Error("Vui lòng chọn chuyên viên, khung giờ và loại tư vấn.");
  }

  // Trong ứng dụng thật, kiểm tra và tạo lịch phải nằm trong một transaction.
  return coSoDuLieu.transaction(async (giaoDich) => {
    const khungGio = await giaoDich.khoaVaTimKhungGio(yeuCau.khungGioId);

    if (!khungGio || khungGio.trangThai !== "con_trong") {
      throw new Error("Khung giờ này không còn khả dụng. Vui lòng chọn giờ khác.");
    }

    const lichHen = await giaoDich.taoLichHen({
      sinhVienId: nguoiDungHienTai.id,
      chuyenVienId: yeuCau.chuyenVienId,
      khungGioId: khungGio.id,
      loaiTuVan: yeuCau.loaiTuVan,
      trangThai: "cho_xac_nhan",
    });

    await giaoDich.capNhatTrangThaiKhungGio(khungGio.id, "da_dat");
    return lichHen;
  });
}
```

### Ví dụ phản hồi API

```json
{
  "thong_bao": "Yêu cầu đặt lịch đã được ghi nhận.",
  "lich_hen": {
    "ma_lich": "LH-000123",
    "trang_thai": "cho_xac_nhan",
    "bat_dau_luc": "2026-11-12T09:00:00+07:00"
  }
}
```

Tên trường và trạng thái trong ví dụ chỉ mang tính minh họa; API thực tế cần thống nhất quy ước đặt tên.

## 10. API dự kiến

| Phương thức | Đường dẫn | Mục đích |
|---|---|---|
| `GET` | `/api/dich-vu` | Xem danh mục dịch vụ |
| `GET` | `/api/chuyen-vien` | Tìm chuyên viên theo tiêu chí công khai |
| `GET` | `/api/khung-gio?chuyen_vien_id=...&ngay=...` | Xem giờ còn trống |
| `POST` | `/api/lich-hen` | Tạo yêu cầu đặt lịch |
| `GET` | `/api/lich-hen/cua-toi` | Xem lịch của người dùng đang đăng nhập |
| `PATCH` | `/api/lich-hen/{id}` | Đổi trạng thái hoặc cập nhật lịch theo quyền |
| `DELETE` | `/api/lich-hen/{id}` | Hủy lịch nếu chính sách cho phép |

Mọi API cần xác thực, kiểm tra quyền truy cập trên máy chủ, xác thực dữ liệu đầu vào và trả lỗi không làm lộ thông tin nhạy cảm.

## 11. Bảo mật, riêng tư và an toàn người dùng

- Chỉ yêu cầu dữ liệu tối thiểu để điều phối lịch.
- Không đưa loại vấn đề tư vấn, nội dung riêng tư hoặc thông tin nhạy cảm vào tiêu đề email, thông báo màn hình khóa hoặc URL.
- Áp dụng phân quyền tối thiểu; chuyên viên chỉ xem thông tin cần thiết cho lịch được phân công.
- Bảo vệ phiên đăng nhập, mật khẩu và dữ liệu truyền nhận; không lưu mật khẩu dạng văn bản thuần.
- Giới hạn truy cập quản trị và ghi nhật ký truy cập/thay đổi quan trọng.
- Có quy trình xử lý yêu cầu xóa, chỉnh sửa hoặc xuất dữ liệu theo chính sách và quy định áp dụng.
- Hiển thị chính sách quyền riêng tư, mục đích xử lý dữ liệu và thông tin liên hệ hỗ trợ.
- Nêu rõ dịch vụ đặt lịch không phải kênh cấp cứu. Nếu người dùng đang gặp nguy hiểm tức thời, hướng dẫn họ liên hệ dịch vụ khẩn cấp tại địa phương hoặc người hỗ trợ đáng tin cậy.
- Không hiển thị đánh giá công khai hoặc hồ sơ có thể tiết lộ việc một sinh viên đã sử dụng dịch vụ nhạy cảm.

## 12. Kiểm thử cần có

- Sinh viên đặt được khung giờ còn trống.
- Hai yêu cầu đồng thời cho cùng khung giờ: chỉ một yêu cầu thành công.
- Không cho đặt khung giờ trong quá khứ hoặc khung giờ không thuộc chuyên viên đã chọn.
- Người dùng không thể xem hoặc sửa lịch của người khác.
- Đổi/hủy lịch tuân thủ chính sách và cập nhật trạng thái nhất quán.
- Chuyên viên chỉ xem được lịch được phân công.
- Kiểm tra dữ liệu đầu vào, lỗi mạng và lỗi cơ sở dữ liệu không tạo lịch trùng hoặc lịch không hoàn chỉnh.
- Thông báo không chứa dữ liệu nhạy cảm.
- Kiểm tra giao diện trên điện thoại, bàn phím và trình đọc màn hình ở các luồng chính.

## 13. Gợi ý cấu trúc thư mục

Cấu trúc cuối cùng phụ thuộc vào công nghệ được nhóm chọn. Ví dụ:

```text
.
├── docs/
│   ├── HE_THONG_DAT_LICH_TU_VAN.md
│   ├── API.md
│   └── QUYEN_RIENG_TU.md
├── frontend/
├── backend/
├── database/
├── tests/
├── .env.example
└── README.md
```

Không đưa mật khẩu, khóa API hoặc dữ liệu thật của sinh viên vào Git. Chỉ đưa biến mẫu không chứa bí mật vào `.env.example`.

## 14. Kế hoạch triển khai gợi ý

1. Đọc và chốt yêu cầu từ PRD cùng tài liệu ghi chú.
2. Xác định quy tắc đặt/đổi/hủy lịch, vai trò và dữ liệu cần thu thập.
3. Vẽ luồng người dùng, wireframe và mô hình dữ liệu.
4. Xây dựng đăng nhập, phân quyền và danh mục dịch vụ.
5. Xây dựng lịch khả dụng và quy trình đặt lịch có chống trùng.
6. Bổ sung quản lý lịch, thông báo và giao diện quản trị.
7. Kiểm thử quyền riêng tư, bảo mật, khả năng tiếp cận và các tình huống đồng thời.
8. Triển khai thử nghiệm với dữ liệu giả; chỉ dùng dữ liệu thật sau khi có phê duyệt và quy trình bảo vệ phù hợp.

## 15. Câu hỏi cần xác nhận từ tài liệu PRD

- Ai được sử dụng hệ thống và có cần xác minh email/tư cách sinh viên không?
- Lịch được xác nhận tự động hay cần chuyên viên duyệt?
- Hỗ trợ tư vấn trực tiếp, trực tuyến hay cả hai?
- Thời lượng buổi hẹn, thời gian đặt trước và quy tắc đổi/hủy là gì?
- Sinh viên có được chọn chuyên viên không? Có cần phân công tự động không?
- Có cần thanh toán, nhắc lịch qua email/SMS hay tích hợp lịch cá nhân không?
- Dữ liệu nào được lưu, ai được xem và lưu trong bao lâu?
- Quy trình hỗ trợ khẩn cấp và đầu mối liên hệ của trường là gì?
- Công nghệ, môi trường triển khai và tiêu chí nghiệm thu đã được chọn chưa?

## 16. Tài liệu nguồn

- [Issue dự án: Hệ thống đặt lịch tư vấn tâm lý và pháp lý cho sinh viên](https://github.com/nguyenminhchinh12345py-sudo/Nguy-n-MinhCh-nh/issues/1)
- [Tài liệu dự án chia theo ghi chú (DOCX)](https://github.com/user-attachments/files/34620025/Tai_lieu_du_an_chia_the_ghi_chu.docx)
- [PRD đặt lịch tư vấn tâm lý và pháp lý (DOCX)](https://github.com/user-attachments/files/34620030/PRD_Dat_lich_tu_van_tam_ly_va_phap_ly.docx)

---

**Việc cần làm tiếp theo:** đối chiếu tài liệu này với nội dung hai tệp DOCX, thay các phần “dự kiến/cần xác nhận” bằng yêu cầu đã thống nhất và cập nhật công nghệ thực tế của dự án.
