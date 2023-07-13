# Proyek Akhir Pemrograman Berbasis Objek 1

Proyek ini adalah contoh sederhana aplikasi pengolahan data Hotel menggunakan Java sebagai tugas akhir dari mata kuliah pemrograman berbasis objek 1.

## Deskripsi

Aplikasi ini menerima input berupa nama tamu, kode dan nama hotel, dan memberikan output berupa informasi detail dari kode tersebut seperti lantai kamar, nomor kamar, dan kelas hotel.

Aplikasi ini mengimplementasikan beberapa konsep penting dalam pemrograman berorientasi objek (OOP) seperti Class, Object, Atribut, Method Constructor, Method Mutator, Method Accessor, Encapsulation, Inheritance, Overloading, Overriding, Seleksi, Perulangan, IO Sederhana, Array, dan Error Handling.

## Penjelasan Kode

Berikut adalah bagian kode yang relevan dengan konsep OOP yang dijelaskan:

1. **Class** adalah template atau blueprint dari object. Pada kode ini, `Hotel`, `HotelDetail`, dan `HotelBeraksi` adalah contoh dari class.

```bash
public class Hotel {
    ...
}

public class HotelDetail extends Hotel {
    ...
}

public class HotelBeraksi {
    ...
}
```

2. **Object** adalah instance dari class. Pada kode ini, `tamu[i] = new HotelDetail(namatamu, kode, namahotel);` adalah contoh pembuatan object.

```bash
tamu[i] = new HotelDetail(namatamu, kode, namahotel);
```

3. **Atribut** adalah variabel yang ada dalam class. Pada kode ini, `namatamu`, `kode` dan `namahotel` adalah contoh atribut.

```bash
String namatamu;
String kode;
String namahotel;
```

4. **Constructor** adalah method yang pertama kali dijalankan pada saat pembuatan object. Pada kode ini, constructor ada di dalam class `Hotel` dan `HotelDetail`.

```bash
public Hotel(String namatamu, String kode. String namahotel) {
    this.namatamu = namatamu;
    this.kode = kode;
    this.namahotel = namahotel;
}

public HotelDetail(String namatamu, String kode, String namahotel) {
    super(namatamu, kode, namahotel);
}
```

5. **Mutator** atau setter digunakan untuk mengubah nilai dari suatu atribut. Pada kode ini, `setNamatamu`,`setKodepesanan` dan `setNamahotel` adalah contoh method mutator.

```bash
public void setNamatamu(String namatamu) {
    this.namatamu = namatamu;
}

public void setKodepesanan(String kode) {
    this.kode = kode;
}
    
public void setNamahotel (String namahotel) {
    this.namahotel = namahotel;
}
```

6. **Accessor** atau getter digunakan untuk mengambil nilai dari suatu atribut. Pada kode ini, `getNamatamu`, `getKodepesanan`, `getLantaiKamar`, `getNomorKamar` dan `getKelas` adalah contoh method accessor.

```bash
public String getNamatamu() {
    return namatamu;
}

public String getKodepesanan() {
    return kode;
}
    
public String getNamahotel() {
    return namahotel;
}
```

7. **Encapsulation** adalah konsep menyembunyikan data dengan membuat atribut menjadi private dan hanya bisa diakses melalui method. Pada kode ini, atribut `namatamu`, `kode` `namahotel` dienkapsulasi dan hanya bisa diakses melalui method getter dan setter.

```bash
private String namatamu;
private String kode;
private String namahotel;

```

8. **Inheritance** adalah konsep di mana sebuah class bisa mewarisi property dan method dari class lain. Pada kode ini, `HotelDetail` mewarisi `Hotel` dengan sintaks `extends`.

```bash
public class HotelDetail extends Hotel {
    ...
}
```

9. **Polymorphism** adalah konsep di mana sebuah nama dapat digunakan untuk merujuk ke beberapa tipe atau bentuk objek berbeda. Ini memungkinkan metode-metode dengan nama yang sama untuk berperilaku berbeda tergantung pada tipe objek yang mereka manipulasi, polymorphism bisa berbentuk Overloading ataupun Overriding. Pada kode ini, method `infoHotel(String)` di `Hotel` merupakan overloading method `infoHotel` dan `infoHotel` di `HotelDetail` merupakan override dari method `infoHotel` di `Hotel`.

```bash
public String infoHotel(String harga){
        return infoHotel() + "\nHarga : "+harga;
}

@Override
public String infoHotel() {
    ...
}
```

10. **Seleksi** adalah statement kontrol yang digunakan untuk membuat keputusan berdasarkan kondisi. Pada kode ini, digunakan seleksi `if else` dalam method `getLantaiKamar` dan seleksi `switch` dalam method `getNomorKamar` dan `getKelas`.

```bash
public String getLantaiKamar(){
     String kodeLantai = getKodepesanan().substring(0, 1);
     //seleksi if
     if(kodeLantai.equals("1")){
         return "Lantai 1";
     } else if (kodeLantai.equals("2")) {
        return "Lantai 2";
     } else if (kodeLantai.equals("3")) {
        return "Lantai 3";
     } else if (kodeLantai.equals("4")) {
        return "Lantai 4";
     } else if (kodeLantai.equals("5")) {
        return "Lantai 5";
     } else {
         return "Lantai tidak ada";
     }
 }

public String getNomorKamar(){
     String kodeKamar = getKodepesanan().substring(1, 3);
     //seleksi switch
     switch(kodeKamar){
         case "01":
             return "01";
         case "02":
             return "02";
         case "03":
             return "03";
         case "04":
             return "04";
         case "05":
             return "05";
         case "06":
             return "06";
         case "07":
             return "07";
         case "08":
             return "08";
         default:
             return "Kamar Tidak Tersedia";
     }
 }
 
 public String getKelas(){
     String kodeKelas = getKodepesanan().substring(3, 6);
     switch(kodeKelas){
         case "001":
             return "Standar";
         case "002":
             return "Deluxe";
         case "003":
             return "Superior";
         case "004":
             return "Eksekutif";
         case "005":
             return "Suite";
         case "006":
             return "Apartemen";
         default:
             return "Fasilitas Tidak Tersedia";
        }
    }
```

11. **Perulangan** adalah statement kontrol yang digunakan untuk menjalankan blok kode berulang kali. Pada kode ini, digunakan loop `for` untuk meminta input dan menampilkan data.

```bash
for(int i=0; i<tamu.length; i++){
    ...
}
```

12. **Input Output Sederhana** digunakan untuk menerima input dari user dan menampilkan output ke user. Pada kode ini, digunakan class `Scanner` untuk menerima input dan method `System.out.println` untuk menampilkan output.

```bash
Scanner scanner = new Scanner(System.in);
System.out.print(" 1. Masukkan Nama Tamu : ");
String namatamu = scanner.nextLine();

System.out.println("Data Tamu Hotel: ");
System.out.println(data.infoHotel());
```

13. **Array** adalah struktur data yang digunakan untuk menyimpan beberapa nilai dalam satu variabel. Pada kode ini, `HotelDetail[] tamu = new HotelDetail[2];` adalah contoh penggunaan array.

```bash
HotelDetail[] tamu = new HotelDetail[2];
```

14. **Error Handling** digunakan untuk menangani error yang mungkin terjadi saat runtime. Pada kode ini, digunakan `try catch` untuk menangani error.

```bash
try {
    // code that might throw an exception
} catch (Exception e) {
    System.out.println("Kesalahan umum: "+e.getMessage());
}
```

## Usulan nilai

| No  | Materi         |  Nilai  |
| :-: | -------------- | :-----: |
|  1  | Class          |    5    |
|  2  | Object         |    5    |
|  3  | Atribut        |    5    |
|  4  | Constructor    |    5    |
|  5  | Mutator        |    5    |
|  6  | Accessor       |    5    |
|  7  | Encapsulation  |    5    |
|  8  | Inheritance    |    5    |
|  9  | Polymorphism   |   10    |
| 10  | Seleksi        |    5    |
| 11  | Perulangan     |    5    |
| 12  | IO Sederhana   |   10    |
| 13  | Array          |   15    |
| 14  | Error Handling |   15    |
|     | **TOTAL**      | **100** |

## Pembuat

Nama: Muhammad Fikri Firzatullah
NPM: 2110010506
