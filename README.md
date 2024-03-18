### Program sederhana input data karyawan menggunakan php

kali ini kita akan membuat sebuah porgram sederhana yaitu input data karyawan menggunakan bahasa pemrogramman PHP

> Tools yang dibutuhkan.
- XAMPP
- Visual Studio Code
- Browser (google chrome)

Pertama buat lah folder di dalam htdocs dengan nama **Lab2Web** lalu buat file bernama **index.php**
untuk penamaan folder dan file kalian bebas menamakannya.
Setelah itu buka folder tersebut dengan Visual Studio Code seperti gambar dibawah ini

![image](https://github.com/Rayiden20/lab2web/assets/115732267/ab324abf-4ef3-4aaa-b77f-c7ddaa79086a)

selanjutnya buka file **index.php** lalu ikuti kode seperti gambar dibawah :

![image](https://github.com/Rayiden20/lab2web/assets/115732267/2663826a-a274-4a78-9d55-1fe1977a3902)
> Pembahasan
Pada kode diatas merupakan kode php dalam menangani formulir yang akan diinput,

`
if (isset($_POST['submit'])) {
`
ini pengecekan jika ada  post submit yang dikirim maka lakukan perintah berikut, jika tidak ada dia keluar blok kurang kurawal buka / tutup

Pada bagian berikut dilakukan pengecekan mengenai pekerjaan, jika pekerjaannya sebagai  **Software Engineer** maka gaji nya 23000000 dan seterusnya tergantung pada yang diinputkan nanti didalam formulir

```
$pekerjaan = $_POST["pekerjaan"];
  if ($pekerjaan == "Software Engineer") {
    $gaji = 23000000;
  } else if ($pekerjaan == "Data Analyst") {
    $gaji = 25000000;
  } else if ($pekerjaan == "Design Graphic") {
    $gaji = 19000000;
  } else if ($pekerjaan == "Network Engineer") {
    $gaji = 22000000;
  } else if ($pekerjaan == "QA Engineer") {
    $gaji = 18000000;
  } else if ($pekerjaan == "DevOps Engineer") {
    $gaji = 23500000;
  } else {
    $gaji = 0;
  }
```

Selanjutnya pada bagian blok kode berikut merupakan perhitungan umur berdasarkan tanggal lahir yang diinputkan, kita menggunakan fungsi bawaan php yaitu `DateTime()` yang mana nanti kita dapat mengetahui umur yang akan diinputkan berdasarkan tanggal lahirnya. lalu kita simpan di variabel umur.

```
$tanggal_lahir = new DateTime($_POST['tanggal_lahir']);

  $hari_ini = new DateTime('today');
  $tahun = $tanggal_lahir->diff($hari_ini)->y;
  $bulan = $tanggal_lahir->diff($hari_ini)->m;
  $hari = $tanggal_lahir->diff($hari_ini)->d;

  $umur = $tahun . " tahun " . $bulan . " bulan " . $hari . " hari ";

```

lanjut ke kode berikut :

kode berikut merupakan kerangka html yang akan menampilkan formulir dan data yang diinputkan, pada kode ini kita menambahkan style css agar terlihat menarik.

![image](https://github.com/Rayiden20/lab2web/assets/115732267/4a9ccc20-8bda-48a5-9f7f-03e0290631e7)
![image](https://github.com/Rayiden20/lab2web/assets/115732267/82bf7605-85f3-4f04-80ef-47e79a38fc42)
![image](https://github.com/Rayiden20/lab2web/assets/115732267/57975fd9-3be2-49e4-96a2-c94ca6d489a5)

Selanjutnya tambahkan kode berikut :

pada kode dibawah ini merupakan tag formulir html. sebagai formulir dan hasil dari inputan yang akan diinputkan nanti.

![image](https://github.com/Rayiden20/lab2web/assets/115732267/b725cbb7-4bf0-4ca1-9bc7-f7913afba4ef)
![image](https://github.com/Rayiden20/lab2web/assets/115732267/65499bd2-4b86-4587-93dd-88cf0e2ccc22)

setelah selesai saatnya kita jalankan programnya dengan cara buka xampp control panel lalu start apache, jika sudah buka browser lalu ketikan **`localhost/Lab2Web`**


Berikut hasil program yang akan muncul sebelum diinput dan sesudah diinput :

![image](https://github.com/Rayiden20/lab2web/assets/115732267/de000a03-e4fa-475a-9833-4b8ca4202434)
![image](https://github.com/Rayiden20/lab2web/assets/115732267/d6b89310-3713-467d-b4e0-8cb7ee27189a)

### Selesai, Thank You.













