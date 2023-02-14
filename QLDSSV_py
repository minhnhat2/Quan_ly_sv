class Student:
    id = 0

    def __init__(self, ten, gioi_tinh, tuoi, diem_toan, diem_van, diem_anh,diem_ly,diem_hoa):
        self.name = ten
        self.gender = gioi_tinh
        self.age = tuoi
        self.diem_toan = diem_toan
        self.diem_van = diem_van
        self.diem_anh = diem_anh
        self.diem_ly = diem_ly
        self.diem_hoa = diem_hoa
        self.subject_gpa = ((self.diem_toan.diem_tbm + self.diem_van.diem_tbm + self.diem_anh.diem_tbm + self.diem_ly.diem_tbm + self.diem_hoa.diem_tbm)) / 5
        if self.subject_gpa >= 8:
            self.hoc_luc = "Xuất Xắc"
        elif self.subject_gpa >= 6.5:
            self.hoc_luc = "Khá"
        elif self.subject_gpa >= 5:
            self.hoc_luc = "Trung Bình"
        else:
            self.hoc_luc = "Yếu"
        self.id = Student.id
        Student.id += 1

class Score:
    def __init__(self,diem_quatrinh, diem_thuchanh, diem_cuoiky):
        self.diem_quatrinh = diem_quatrinh
        self.diem_thuchanh = diem_thuchanh
        self.diem_cuoiky = diem_cuoiky
        self.điểm_tbm = self.diem_quatrinh * 0.2 + self.diem_thuchanh * 0.3 + self.diem_cuoiky * 0.5
        if self.diem_tbm >= 5:
            self.danh_gia = "qua môn"
        else:
            self.danh_gia = "rớt môn"

students = []

def add_student():
    name = input("Nhập tên học sinh: ")
    gender = input("Nhập giới tính: ")
    age = int(input("Nhập tuổi: "))
    diem_toan = Score(
        int(input("Nhập điểm quá trình môn toán: ")),
        int(input("Nhập điểm thực hành môn toán: ")),
        int(input("Nhập điểm cuối kì môn toán: "))
    )
    diem_van = Score(
        int(input("Nhập điểm quá trình môn văn: ")),
        int(input("Nhập điểm thực hành môn văn: ")),
        int(input("Nhập điểm cuối kì môn văn: "))
    )
    diem_anh = Score(
        int(input("Nhập điểm quá trình môn anh: ")),
        int(input("Nhập điểm thực hành môn anh: ")),
        int(input("Nhập điểm cuối kì môn anh: "))
    )
    diem_ly = Score(
        int(input("Nhập điểm quá trình môn lý: ")),
        int(input("Nhập điểm thực hành môn lý: ")),
        int(input("Nhập điểm cuối kì môn lý: "))
    )
    diem_hoa = Score(
        int(input("Nhập điểm quá trình môn hóa: ")),
        int(input("Nhập điểm thực hành môn hóa: ")),
        int(input("Nhập điểm cuối kì môn hóa: "))
    )
    student = Student(ten, gioi_tinh, tuoi, diem_toan, diem_van, diem_anh,diem_ly,diem_hoa)
    students.append(student)
    print("Thêm học sinh thành công")

def update_student():
    id = int(input("Nhập ID học sinh: "))
    for student in students:
        if student.id == id:
            student.ten = input("Nhập tên học sinh mới: ")
            student.gioi_tinh = input("Nhập giới tính học sinh mới: ")
            student.tuoi = int(input("Nhập tuổi học sinh mới: "))
            
            # Update điểm toán
            student.diem_toan.diem_quatrinh = float(input("Nhập điểm quá trình môn toán mới: "))
            student.diem_toan.diem_thuchanh = float(input("Nhập điểm thực hành môn toán mới: "))
            student.diem_toan.diem_cuoiky = float(input("Nhập điểm cuối kỳ môn toán mới: "))
            student.diem_toan.diem_tbm = round((student.diem_toan.diem_quatrinh * 0.2 + student.diem_toan.diem_thuchanh * 0.3 + student.diem_toan.diem_cuoiky * 0.5), 2)
            student.diem_toan.danh_gia = "qua môn" if student.diem_toan.diem_tbm >= 5 else "rớt môn"
            
            # Update điểm văn
            student.diem_van.diem_quatrinh = float(input("Nhập điểm quá trình môn văn mới: "))
            student.diem_van.diem_thuchanh = float(input("Nhập điểm thực hành môn văn mới: "))
            student.diem_van.diem_cuoiky = float(input("Nhập điểm cuối kỳ môn văn mới: "))
            student.diem_van.diem_tbm = round((student.diem_van.diem_quatrinh * 0.2 + student.diem_van.diem_thuchanh * 0.3 + student.diem_van.diem_cuoiky * 0.5), 2)
            student.diem_van.danh_gia = "qua môn" if student.diem_van.diem_tbm >= 5 else "rớt môn"
            
            # Update điểm anh
            student.diem_anh.diem_quatrinh = float(input("Nhập điểm quá trình môn anh mới: "))
            student.diem_anh.diem_thuchanh = float(input("Nhập điểm thực hành môn anh mới: "))
            student.diem_anh.diem_cuoiky = float(input("Nhập điểm cuối kỳ môn anh mới: "))
            student.diem_anh.diem_tbm = round((student.diem_anh.diem_quatrinh * 0.2 + student.diem_anh.diem_thuchanh * 0.3 + student.diem_anh.diem_cuoiky * 0.5), 2)
            student.diem_anh.danh_gia = "qua môn" if student.diem_anh.diem_tbm >= 5 else "rớt môn"
            
            # Update điểm lý
            student.diem_ly.diem_quatrinh = float(input("Nhập điểm quá trình môn lý mới: "))
            student.diem_ly.diem_thuchanh = float(input("Nhập điểm thực hành môn lý mới: "))
            student.diem_ly.diem_cuoiky = float(input("Nhập điểm cuối kỳ môn lý mới: "))
            student.diem_ly.diem_tbm = round((student.diem_ly.diem_quatrinh * 0.2 + student.diem_ly.diem_thuchanh * 0.3 + student.diem_ly.diem_cuoiky * 0.5), 2)
            student.diem_ly.danh_gia = "qua môn" if student.diem_ly.diem_tbm >= 5 else "rớt môn"
            
            # Update điểm hóa
            student.diem_hoa.diem_quatrinh = float(input("Nhập điểm quá trình môn hóa mới: "))
            student.diem_hoa.diem_thuchanh = float(input("Nhập điểm thực hành môn hóa mới: "))
            student.diem_hoa.diem_cuoiky = float(input("Nhập điểm cuối kỳ môn hóa mới: "))
            student.diem_hoa.diem_tbm = round((student.diem_hoa.diem_quatrinh * 0.2 + student.diem_hoa.diem_thuchanh * 0.3 + student.diem_hoa.diem_cuoiky * 0.5), 2)
            student.diem_hoa.danh_gia = "qua môn" if student.diem_hoa.diem_tbm >= 5 else "rớt môn"
            
            # Update subject GPA và học lực
            student.subject_gpa = round((student.diem_toan.diem_tbm + student.diem_van.diem_tbm + student.diem_anh.diem_tbm + student.diem_ly.diem_tbm +student.diem_hoa.diem_tbm) / 5, 2)
            student.hoc_luc = (
                "Xuất Xắc" if student.subject_gpa >= 8 else
                "Khá" if student.subject_gpa >= 6.5 else
                "Trung Bình " if student.subject_gpa >= 5 else
                "Yếu"
            )
            
            print("Thông tin học sinh đã được cập nhập thành công")
            break
    else:
        print("không tìm thấy sinh viên")
            
def delete_student():
    id = int(input("Nhập ID học sinh: "))
    for i, student in enumerate(students):
        if student.id == id:
            del students[i]
            print("Học sinh đã xóa thành công")
            break
    else:
        print("không tìm thấy sinh viên")

def search_student():
    name = input("Nhập tên học sinh: ")
    found = False
    for student in students:
        if name.lower() in student.ten.lower():
            print(f"ID: {student.id}, Tên: {student.ten}, Giới Tính: {student.gioi_tinh}, Tuổi: {student.tuoi}")
            found = True
    if not found:
        print("không tìm thấy sinh viên")

def sort_by_gpa():
    sorted_students = sorted(students, key=lambda s: s.subject_gpa, reverse=True)
    for student in sorted_students:
        print(f"ID: {student.id}, Name: {student.ten}, GPA: {student.subject_gpa}")

def sort_by_name():
    sorted_students = sorted(students, key=lambda s: s.name)
    for student in sorted_students:
        print(f"ID: {student.id}, Name: {student.ten}")

def sort_by_id():
    sorted_students = sorted(students, key=lambda s: s.id)
    for student in sorted_students:
        print(f"ID: {student.id}, Name: {student.ten}")

def display_students():
    for student in students:
        print(f"ID: {student.id}, Name: {student.ten}, GPA: {student.subject_gpa}, Học Lực: {student.hoc_luc}")

while True:
    print("1. Thêm học sinh")
    print("2. Cập nhật thông tin sinh viên theo ID")
    print("3. Xóa sinh viên theo ID")
    print("4. Tìm kiếm sinh viên theo tên")
    print("5. Sắp xếp học sinh theo điểm trung bình")
    print("6. Sắp xếp học sinh theo tên")
    print("7. Sắp xếp sinh viên theo ID")
    print("8. Hiển thị danh sách sinh viên")
    print("9. Exit")
    choice = int(input("Nhập lựa chọn của bạn: "))
    if choice == 1:
        add_student()
    elif choice == 2:
        update_student()
    elif choice == 3:
        delete_student()
    elif choice == 4:
        search_student()
    elif choice == 5:
        sort_by_gpa()
    elif choice == 6:
        sort_by_name()
    elif choice == 7:
        sort_by_id()
    elif choice == 8:
        display_students()
    elif choice == 9:
        break
    else:
        print("lựa chọn không hợp lệ")
