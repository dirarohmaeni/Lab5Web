### Nama: Dira Rohmaeni
### NIM: 312410465
### Kelas: TI.24.A5


# Langkah - Langkah Pratikum 5
1. Buat file baru dengan nama lab5_javascript.html
2. lalu
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


3. ```HTML
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

4. ```HTML
   <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>Mengenal JavaScript - Validasi Form</title>
    <script>
        function pesan() {
        alert("Memanggil JavaScript lewat body onload");
        }

        function testAritmatika(val1, val2) {
        document.write("<br>Perkalian: " + (val1 * val2) + "<br>");
        document.write("Pembagian: " + (val1 / val2) + "<br>");
        document.write("Penjumlahan: " + (val1 + val2) + "<br>");
        document.write("Pengurangan: " + (val1 - val2) + "<br>");
        document.write("Modulus: " + (val1 % val2) + "<br>");
        }

        function testSwitch() {
        let val1 = window.prompt("Input nilai (1-5):");
        switch (val1) {
        case "1": document.write("Bilangan satu"); break;
        case "2": document.write("Bilangan dua"); break;
        case "3": document.write("Bilangan tiga"); break;
        case "4": document.write("Bilangan empat"); break;
        case "5": document.write("Bilangan lima"); break;
        default: document.write("Bilangan lainnya");
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

        if (bil % 2 === 0)
            document.kirim.T2.value = "Bilangan Genap";
        else
            document.kirim.T2.value = "Bilangan Ganjil";
    }
    </script> 
</head>
<body onload="pesan"()>
    <h1>Pengenalan JavaScript</h1>
    <h3>Validasi Form Input</h3>

    <h2>Cek Bilangan Genap/Ganjil dengan Validasi</h2>
    <form name="kirim" onsubmit="return validasiForm();">
        <p>
            Bilangan:
            <input type="text" name="T1" size="10">
            <input type="button" value="Cek" onclick="validasiForm()">
            Hasil:
            <input type="text" name="T2" size="20" readonly>
        </p>
    </form>
</body>
</html>
```
