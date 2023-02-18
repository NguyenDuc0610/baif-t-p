cau 1
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    System.out.print("Nhap diem trung binh: ");
    double diemTB = scanner.nextDouble();

    if (diemTB < 5.0) {
      System.out.println("Xep loai: Kem");
    } else if (diemTB >= 5.0 && diemTB < 7.0) {
      System.out.println("Xep loai: Trung binh");
    } else if (diemTB >= 7.0 && diemTB < 8.0) {
      System.out.println("Xep loai: Kha");
    } else {
      System.out.println("Xep loai: Gioi");
    }
  }
}

cau 3
import java.util.Scanner;

public class SoNguyenToChu {
    public static void main(String[] args) {
        // Khai báo mảng chứa các chữ số từ 0 đến 9
        String[] chuSo = {"không", "một", "hai", "ba", "bốn", "năm", "sáu", "bảy", "tám", "chín"};

        // Nhập số nguyên n từ người dùng
        Scanner scanner = new Scanner(System.in);
        System.out.print("Nhập số nguyên có 3 chữ số: ");
        int n = scanner.nextInt();

        // Tách các chữ số của n
        int tram = n / 100;
        int chuc = (n % 100) / 10;
        int donVi = n % 10;

        // Tạo chuỗi chữ tương ứng
        String chuoiChu = chuSo[tram] + " trăm ";
        if (chuc == 0 && donVi != 0) {
            chuoiChu += "linh ";
        } else if (chuc == 0 && donVi == 0) {
            chuoiChu = chuSo[tram] + " trăm";
        }
        if (chuc == 1 && donVi != 0) {
            chuoiChu += "mười ";
        } else if (chuc == 1 && donVi == 0) {
            chuoiChu += "mười";
        }
        if (chuc > 1) {
            chuoiChu += chuSo[chuc] + " mươi ";
        }
        if (donVi == 1 && chuc != 1 && chuc != 0) {
            chuoiChu += "mốt";
        }
        if (donVi == 1 && chuc == 0) {
            chuoiChu += chuSo[donVi];
        }
        if (donVi == 2 && chuc != 0) {
            chuoiChu += "hai";
        }
        if (donVi == 2 && chuc == 0) {
            chuoiChu += chuSo[donVi];
        }
        if (donVi == 3 && chuc != 0) {
            chuoiChu += "ba";
        }
        if (donVi == 3 && chuc == 0) {
           
câu 4
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Nhập số nguyên n: ");
        int n = sc.nextInt();
        int giaiThua = 1;
        for (int i = 1; i <= n; i++) {
            giaiThua *= i;
        }
        System.out.println(n + "! = " + giaiThua);
    }
}
câu 5
import java.util.Arrays;
import java.util.Scanner;

public class XoaPhanTuTrongMang {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Nhập mảng a
        System.out.print("Nhập độ dài mảng a: ");
        int n = scanner.nextInt();
        int[] a = new int[n];
        System.out.println("Nhập các phần tử của mảng a:");
        for (int i = 0; i < n; i++) {
            System.out.print("a[" + i + "] = ");
            a[i] = scanner.nextInt();
        }

        // Nhập giá trị x
        System.out.print("Nhập giá trị cần xóa (x) = ");
        int x = scanner.nextInt();

        // Tìm và xóa các phần tử có giá trị x
        int index = 0;
        for (int i = 0; i < a.length; i++) {
            if (a[i] != x) {
                a[index] = a[i];
                index++;
            }
        }
        n = index;

        // Sắp xếp mảng a theo thứ tự tăng dần
        Arrays.sort(a);

        // Xuất mảng a sau khi xóa giá trị x và sắp xếp theo thứ tự tăng dần
        System.out.println("Mảng a sau khi xóa giá trị " + x + " và sắp xếp theo thứ tự tăng dần là:");
        for (int i = 0; i < n; i++) {
            System.out.print(a[i] + " ");
        }
    }
}


