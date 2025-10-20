# 33-HoangThiTam-
# 33_HoangThanhTam.py

# Danh sách để lưu thông tin các sinh viên.
# Mỗi sinh viên là một dictionary.
student_list = []

def add_student(name, year_of_birth, address):
    """
    YÊU CẦU 1:
    - Tạo dictionary lưu thông tin sinh viên.
    - Thêm dictionary vào danh sách student_list.
    - In ra thông báo "Da them sinh vien <ten> thanh cong."
    """
    student = {
        "name": name,
        "year_of_birth": year_of_birth,
        "address": address
    }
    student_list.append(student)
    print(f"Da them sinh vien {name} thanh cong.")

def print_student_list():
    """
    YÊU CẦU 2:
    - In tiêu đề danh sách.
    - Nếu trống => in "Danh sach trong."
    - Nếu không, duyệt và in mỗi sinh viên theo định dạng:
      " - Ten: [Họ tên], Nam sinh: [Năm sinh], Dia chi: [Địa chỉ]"
    """
    print("--- DANH SACH SINH VIEN ---")
    if not student_list:
        print("Danh sach trong.")
    else:
        for sv in student_list:
            print(f" - Ten: {sv['name']}, Nam sinh: {sv['year_of_birth']}, Dia chi: {sv['address']}")

def search_student(search_name):
    """
    YÊU CẦU 3:
    - In tiêu đề kết quả tìm kiếm.
    - Tìm tất cả sinh viên có tên chứa search_name (không phân biệt hoa thường).
    - In thông tin của các sinh viên tìm thấy (theo định dạng như trên).
    - Nếu không tìm thấy, in "Khong tim thay sinh vien nao."
    """
    print("--- KET QUA TIM KIEM ---")
    found = False
    for sv in student_list:
        if search_name.lower() in sv["name"].lower():
            print(f" - Ten: {sv['name']}, Nam sinh: {sv['year_of_birth']}, Dia chi: {sv['address']}")
            found = True
    if not found:
        print("Khong tim thay sinh vien nao.")

# --- Phần thực thi chính để kiểm tra ---
if __name__ == "__main__":
    print("--- CHUONG TRINH QUAN LY SINH VIEN ---")
    
    # Yêu cầu 1: Thêm sinh viên
    print("\n1. Them sinh vien:")
    add_student("Nguyen Van An", 2003, "Da Nang")
    add_student("Tran Thi Binh", 2002, "Quang Nam")
    add_student("Le Van Hung", 2003, "Hue")

    # Yêu cầu 2: In danh sách
    print("\n2. In danh sach sinh vien:")
    print_student_list()

    # Yêu cầu 3: Tìm kiếm
    print("\n3. Tim kiem sinh vien theo ten 'an':")
    search_student("an")
    
    print("\nTim kiem sinh vien theo ten 'Dung':")
    search_student("Dung")
student_list = []

def add_student(name, year_of_birth, address):
    student = {
        "name": name,
        "year_of_birth": year_of_birth,
        "address": address
    }
    student_list.append(student)
    print(f"Da them sinh vien {name} thanh cong.")
