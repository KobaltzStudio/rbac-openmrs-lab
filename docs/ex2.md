## Exercise 2: Study different roles in OpenMRS Demo (1.0 point)

Dựa trên việc nghiên cứu danh sách các vai trò (roles) thực tế hiển thị trong hệ thống OpenMRS Demo (qua trang Quản trị nâng cao), dưới đây là 4 vai trò tiêu biểu sở hữu các tập hợp quyền hạn khác nhau:

1. **Organizational: System Administrator**: vai trò có quyền hạn tối cao, bao gồm tất cả các quyền quản trị về người dùng, vai trò và thiết lập hệ thống. Trong giao diện thực tế, vai trò **Application: Administers System** tương ứng với nhóm quyền này (Privilege Level: High).
2. **Organizational: Doctor**: Vai trò dành cho bác sĩ, sở hữu bộ quyền hạn lâm sàng rộng lớn bao gồm: thêm/sửa/xem hồ sơ bệnh nhân, quản lý các lượt thăm khám (visits) và các phiên khám bệnh (encounters).
3. **Organizational: Nurse**: Vai trò dành cho điều dưỡng, có tập hợp quyền đa dạng để quản lý dữ liệu lâm sàng, nhập chỉ số sinh tồn (vitals), y lệnh xét nghiệm và trích xuất báo cáo.
4. **Organizational: Registration Clerk**: Vai trò dành cho nhân viên tiếp đón, sở hữu các quyền hạn quan trọng về quản lý thông tin hành chính, đăng ký bệnh nhân mới và điều phối lịch hẹn (appointments).

Lưu ý: Các vai trò này thường được thiết lập theo cơ chế thừa hưởng (Inheritance), giúp các vai trò cấp cao tự động sở hữu quyền hạn từ các vai trò cấp thấp hơn.
