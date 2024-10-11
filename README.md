import java.util.Scanner;

public class NilaiMahasiswa {
    public static void main(String[] args) {
        // Membuat objek Scanner untuk membaca input dari pengguna
        Scanner scanner = new Scanner(System.in); 


        // Mendeklarasikan variabel untuk menyimpan jumlah mahasiswa, nilai, nilai tertinggi, terendah, jumlah yang lulus, dan batas lulus
        int jumlahMahasiswa, nilai, tertinggi = 0, terendah = 100, lulus;
        final int batasLulus = 60;

        // Meminta pengguna memasukkan jumlah mahasiswa
        System.out.print("Masukkan jumlah mahasiswa: ");
        jumlahMahasiswa = scanner.nextInt();

        // Mengulang proses input nilai untuk setiap mahasiswa
        for (int i = 1; i <= jumlahMahasiswa; i++) {
            // Meminta pengguna memasukkan nilai mahasiswa ke-i
            System.out.print("Masukkan nilai mahasiswa ke-" + i + ": ");
            nilai = scanner.nextInt();

            // Memeriksa apakah nilai yang dimasukkan lebih besar dari nilai tertinggi saat ini
            if (nilai > tertinggi) {
                // Jika ya, maka nilai tertinggi diperbarui
                tertinggi = nilai;
            }

            if (nilai < terendah) {
                terendah = nilai;
            }
            
            if (nilai >= batasLulus) {
                lulus++;
            } else {
                tidakLulus++;
            }

        }
    }
}
