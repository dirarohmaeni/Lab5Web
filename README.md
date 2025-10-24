### Nama: Dira Rohmaeni
### NIM: 312410465
### Kelas: TI.24.A5


# Langkah - Langkah Pratikum 5
### Buka apklikasi Visual Studio Coden dan buat file lab5_javascript.html sebagai.
```HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Mengenal JavaScript - Validasi Form</title>
  </head>
  <body>
    <h1>Pengenalan JavaScript</h1>
    <h2>Contoh document.write dan console.log</h2>
    <script>
      document.write("Hello World (document.write)<br>");
      console.log("Hello World (console.log)");
    </script>
  </body>
</html>
```

Lalu buka Browser untuk melihat hasilnya
![foto](https://github.com/dirarohmaeni/Lab5Web/blob/04f90fdcd762df0c8824d8bb272698e8eaa128fb/image%20javascript/image%201.png)



### Memunculkan alert & meminta input prompt.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>Mengenal JavaScript - Validasi Form</title>
</head>
<body>
    <h1>Pengenalan JavaScript</h1>
    <h2>Contoh document.write dan console.log</h2>
  <script>
    document.write("Hello World (document.write)<br>");
    console.log("Hello World (console.log)");

    alert("Ini alert contoh");
    let nama = prompt("Siapa nama anda?", "Nama");
    document.write("Hai, " + nama + "<br>");
  </script>
</body>
</html>
```


### Mengganti document.write dengan DOM (innerHTML) agar aman dan merubah alert lewat body onload.
```HTML
   <!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Mengenal JavaScript - Validasi Form</title>
    <script>
      function pesan() {
        alert("Memanggil JavaScript lewat body onload");
      }

      function testAritmatika(val1, val2) {
        document.write("<br>Perkalian: " + val1 * val2 + "<br>");
        document.write("Pembagian: " + val1 / val2 + "<br>");
        document.write("Penjumlahan: " + (val1 + val2) + "<br>");
        document.write("Pengurangan: " + (val1 - val2) + "<br>");
        document.write("Modulus: " + (val1 % val2) + "<br>");
      }
    </script>
  </head>
  <body onload="pesan" ()>
    <h1>Pengenalan JavaScript</h1>
    <h3>Validasi Form Input</h3>
  </body>
</html>
```


### Demonstrasi switch-case dan prompt. Kemudian tambahkan Form cek genap/ganjil dan Validasi dasar.
```html
   <!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Mengenal JavaScript - Validasi Form</title>
    <script>
      function pesan() {
        alert("Memanggil JavaScript lewat body onload");
      }

      function testAritmatika(val1, val2) {
        document.write("<br>Perkalian: " + val1 * val2 + "<br>");
        document.write("Pembagian: " + val1 / val2 + "<br>");
        document.write("Penjumlahan: " + (val1 + val2) + "<br>");
        document.write("Pengurangan: " + (val1 - val2) + "<br>");
        document.write("Modulus: " + (val1 % val2) + "<br>");
      }

      function testSwitch() {
        let val1 = window.prompt("Input nilai (1-5):");
        switch (val1) {
          case "1":
            document.write("Bilangan satu");
            break;
          case "2":
            document.write("Bilangan dua");
            break;
          case "3":
            document.write("Bilangan tiga");
            break;
          case "4":
            document.write("Bilangan empat");
            break;
          case "5":
            document.write("Bilangan lima");
            break;
          default:
            document.write("Bilangan lainnya");
        }
      }

      function validasiForm() {
        let bil = document.kirim.T1.value;

        if (bil === "") {
          alert("Kolom bilangan tidak boleh kosong!");
          document.kirim.T1.focus();
          return false;
        }

        if (isNaN(bil)) {
          alert("Yang dimasukkan harus berupa angka!");
          document.kirim.T1.focus();
          return false;
        }

        if (bil % 2 === 0) document.kirim.T2.value = "Bilangan Genap";
        else document.kirim.T2.value = "Bilangan Ganjil";
      }
    </script>
  </head>
  <body onload="pesan" ()>
    <h1>Pengenalan JavaScript</h1>
    <h3>Validasi Form Input</h3>

    <h2>Cek Bilangan Genap/Ganjil dengan Validasi</h2>
    <form name="kirim" onsubmit="return validasiForm();">
      <p>
        Bilangan:
        <input type="text" name="T1" size="10" />
        <input type="button" value="Cek" onclick="validasiForm()" />
        Hasil:
        <input type="text" name="T2" size="20" readonly />
      </p>
    </form>
  </body>
</html>
```



### Membuat kolom merubah warna halaman.
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Mengenal JavaScript - Validasi Form</title>
    <script>
      function pesan() {
        alert("Memanggil JavaScript lewat body onload");
      }

      function testAritmatika(val1, val2) {
        document.write("<br>Perkalian: " + val1 * val2 + "<br>");
        document.write("Pembagian: " + val1 / val2 + "<br>");
        document.write("Penjumlahan: " + (val1 + val2) + "<br>");
        document.write("Pengurangan: " + (val1 - val2) + "<br>");
        document.write("Modulus: " + (val1 % val2) + "<br>");
      }

      function testSwitch() {
        let val1 = window.prompt("Input nilai (1-5):");
        switch (val1) {
          case "1":
            document.write("Bilangan satu");
            break;
          case "2":
            document.write("Bilangan dua");
            break;
          case "3":
            document.write("Bilangan tiga");
            break;
          case "4":
            document.write("Bilangan empat");
            break;
          case "5":
            document.write("Bilangan lima");
            break;
          default:
            document.write("Bilangan lainnya");
        }
      }

      function validasiForm() {
        let bil = document.kirim.T1.value;

        if (bil === "") {
          alert("Kolom bilangan tidak boleh kosong!");
          document.kirim.T1.focus();
          return false;
        }

        if (isNaN(bil)) {
          alert("Yang dimasukkan harus berupa angka!");
          document.kirim.T1.focus();
          return false;
        }

        if (bil % 2 === 0) document.kirim.T2.value = "Bilangan Genap";
        else document.kirim.T2.value = "Bilangan Ganjil";

        function ubahWarnaLB(warna) {
          document.bgColor = warna;
        }

        function ubahWarnaLD(warna) {
          document.fgColor = warna;
        }
      }
    </script>
  </head>
  <body onload="pesan" ()>
    <h1>Pengenalan JavaScript</h1>
    <h3>Validasi Form Input</h3>

    <h2>Cek Bilangan Genap/Ganjil dengan Validasi</h2>
    <form name="kirim" onsubmit="return validasiForm();">
      <p>
        Bilangan:
        <input type="text" name="T1" size="10" />
        <input type="button" value="Cek" onclick="validasiForm()" />
        Hasil:
        <input type="text" name="T2" size="20" readonly />
      </p>

      <hr />
      <h2>Ubah Warna Halaman</h2>
      <form>
        <input
          type="button"
          value="Latar Belakang Hijau"
          onclick="ubahWarnaLB('green')"
        />
        <input
          type="button"
          value="Latar Belakang Putih"
          onclick="ubahWarnaLB('white')"
        />
        <input
          type="button"
          value="Teks Kuning"
          onclick="ubahWarnaLD('yellow')"
        />
        <input type="button" value="Teks Biru" onclick="ubahWarnaLD('blue')" />
      </form>
      <hr />
    </form>
  </body>
</html>
```


### Checkbox harga dan total otomatis dengan validasi nilai sekaligus membuat kolom Daftar Menu.
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Mengenal JavaScript - Validasi Form</title>

    <script>
      function pesan() {
        alert("Memanggil JavaScript lewat body onload");
      }

      function testAritmatika(val1, val2) {
        document.write("<br>Perkalian: " + val1 * val2 + "<br>");
        document.write("Pembagian: " + val1 / val2 + "<br>");
        document.write("Penjumlahan: " + (val1 + val2) + "<br>");
        document.write("Pengurangan: " + (val1 - val2) + "<br>");
        document.write("Modulus: " + (val1 % val2) + "<br>");
      }

      function testSwitch() {
        let val1 = window.prompt("Input nilai (1-5):");
        switch (val1) {
          case "1":
            document.write("Bilangan satu");
            break;
          case "2":
            document.write("Bilangan dua");
            break;
          case "3":
            document.write("Bilangan tiga");
            break;
          case "4":
            document.write("Bilangan empat");
            break;
          case "5":
            document.write("Bilangan lima");
            break;
          default:
            document.write("Bilangan lainnya");
        }
      }

      function validasiForm() {
        let bil = document.kirim.T1.value;

        if (bil === "") {
          alert("Kolom bilangan tidak boleh kosong!");
          document.kirim.T1.focus();
          return false;
        }

        if (isNaN(bil)) {
          alert("Yang dimasukkan harus berupa angka!");
          document.kirim.T1.focus();
          return false;
        }

        if (bil % 2 === 0) document.kirim.T2.value = "Bilangan Genap";
        else document.kirim.T2.value = "Bilangan Ganjil";
      }

      function ubahWarnaLB(warna) {
        document.bgColor = warna;
      }

      function ubahWarnaLD(warna) {
        document.fgColor = warna;
      }

      function hitung(ele) {
        let total = document.getElementById("total").value;
        total = total ? parseInt(total) : 0;
        let harga = parseInt(ele.value);

        if (ele.checked) total += harga;
        else total -= harga;

        document.getElementById("total").value = total;
      }
    </script>
  </head>

  <body onload="pesan()">
    <h1>Pengenalan JavaScript</h1>
    <h3>Validasi Form Input</h3>

    <h2>Cek Bilangan Genap/Ganjil dengan Validasi</h2>
    <form name="kirim" onsubmit="return validasiForm();">
      <p>
        Bilangan:
        <input type="text" name="T1" size="10" />
        <input type="button" value="Cek" onclick="validasiForm()" />
        Hasil:
        <input type="text" name="T2" size="20" readonly />
      </p>
    </form>

    <hr />
    <h2>Ubah Warna Halaman</h2>
    <form>
      <input
        type="button"
        value="Latar Belakang Hijau"
        onclick="ubahWarnaLB('green')"
      />
      <input
        type="button"
        value="Latar Belakang Putih"
        onclick="ubahWarnaLB('white')"
      />
      <input
        type="button"
        value="Teks Kuning"
        onclick="ubahWarnaLD('yellow')"
      />
      <input type="button" value="Teks Biru" onclick="ubahWarnaLD('blue')" />
    </form>

    <hr />

    <h2>Daftar Menu Makanan</h2>
    <label
      ><input type="checkbox" value="5000" onclick="hitung(this)" /> Ayam Goreng
      Rp. 5.000</label
    ><br />
    <label
      ><input type="checkbox" value="500" onclick="hitung(this)" /> Tempe Goreng
      Rp. 500</label
    ><br />
    <label
      ><input type="checkbox" value="2500" onclick="hitung(this)" /> Telur Dadar
      Rp. 2.500</label
    ><br />
    <strong
      >Total Bayar: Rp. <input id="total" type="text" value="0" readonly
    /></strong>

    <p>
      <small
        >Dimodifikasi terakhir pada:
        <script>
          document.write(document.lastModified);
        </script>
      </small>
    </p>
  </body>
</html>
```

