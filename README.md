/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

/**
 *
 * @author Lab Informatika
 */
class quiz_123220161 {
    
class Peserta {
    private String nama;
    private String namaSekolah;
    private double skor;


    public Peserta(String nama, String namaSekolah, double skor) {
        this.nama = nama;
        this.namaSekolah = namaSekolah;
        this.skor = skor;
    }


    public String getNama() {
        return nama;
    }

    public String getNamaSekolah() {
        return namaSekolah;
    }

    public double getSkor() {
        return skor;
    }

    public void setSkor(double skor) {
        this.skor = skor;
    }
}

// Class untuk menangani perlombaan
class Kompetisi {
    private String kategori;


    public Kompetisi(String kategori) {
        this.kategori = kategori;
    }

  
    public String getKategori() {
        return kategori;
    }

    // Method untuk mengecek apakah peserta lolos seleksi
    public boolean isPassed(double skor) {
        return skor >= 85;
    }
}


public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Meminta pengguna memilih kategori perlombaan
        System.out.println("Pilih kategori perlombaan:");
        System.out.println("1. Animasi");
        System.out.println("2. Menulis Surat");
        int pilihKategori = scanner.nextInt();

        // Membuat objek kompetisi
        String category;
        if (pilihKategori == 1) {
            kategori = "Animasi";
        } else {
            kategori = "Menulis Surat";
        }
        Kompetisi kompetisi = new Kompetisi(kategori);

        // Meminta pengguna untuk mengisi informasi peserta
        System.out.println("Masukkan nama peserta:");
        String name = scanner.next();
        System.out.println("Masukkan nama sekolah:");
        String schoolName = scanner.next();
        System.out.println("Masukkan nilai peserta:");
        double score = scanner.nextDouble();

        // Membuat objek Peserta
        Peserta Peserta = new Peserta(nama, namaSekolah, skor);

        // Menampilkan hasil akhir
        System.out.println("Hasil akhir:");
        System.out.println("Nama peserta: " + peserta.getNama());
        System.out.println("Nama sekolah: " + peserta.getNamaSekolah());
        System.out.println("Kategori perlombaan: " + kompetisi.getKategori());
        System.out.println("Nilai peserta: " + peserta.getSkor());
        if (kompetisi.isPassed(peserta.getSkor())) {
            System.out.println("Peserta dinyatakan LOLOS seleksi.");
        } else {
            System.out.println("Peserta TIDAK lolos seleksi.");
        }
    }
}
    
}
