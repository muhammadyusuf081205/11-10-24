import java.util.Scanner;

public class PenjualanTiketBioskop {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int jumlahTiket, totalTiket = 0, hargaTiket = 50000;
        double totalPenjualan = 0;

        do {
            System.out.print("Masukkan jumlah tiket yang terjual (0 untuk berhenti): ");
            jumlahTiket = scanner.nextInt();

            if (jumlahTiket < 0) {
                System.out.println("Jumlah tiket tidak boleh negatif. Silakan coba lagi.");
                continue; // Ulangi perulangan jika input negatif
            } else if (jumlahTiket == 0) {
                break; // Keluar dari perulangan jika input 0
            }

            double diskon = 0;
            if (jumlahTiket > 10) {
                diskon = 0.15;
            } else if (jumlahTiket > 4) {
                diskon = 0.1;
            }

            double hargaSetelahDiskon = jumlahTiket * hargaTiket * (1 - diskon);
            totalTiket += jumlahTiket;
            totalPenjualan += hargaSetelahDiskon;

            System.out.println("Total penjualan untuk transaksi ini: Rp" + hargaSetelahDiskon);
        } while (true);

        System.out.println("\nTotal tiket yang terjual: " + totalTiket + " tiket");
        System.out.println("Total penjualan hari ini: Rp" + totalPenjualan);
    }
}




import java.util.Scanner;

public class HitungParkir {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        int pilihanKendaraan, durasiParkir, totalBiaya = 0;

        do {
            System.out.println("Pilih jenis kendaraan:");
            System.out.println("1. Mobil");
            System.out.println("2. Motor");
            System.out.print("Masukkan pilihan (0 untuk keluar): ");
            pilihanKendaraan = input.nextInt();

            if (pilihanKendaraan == 0) {
                break;
            }

            System.out.print("Masukkan durasi parkir (dalam jam): ");
            durasiParkir = input.nextInt();

            if (durasiParkir <= 5) {
                if (pilihanKendaraan == 1) {
                    totalBiaya += durasiParkir * 3000;
                } else if (pilihanKendaraan == 2) {
                    totalBiaya += durasiParkir * 2000;
                } else {
                    System.out.println("Pilihan kendaraan tidak valid.");
                }
            } else {
                totalBiaya += 12500;
            }
        } while (pilihanKendaraan != 0);

        System.out.println("Total biaya parkir: Rp " + totalBiaya);
    }
}
