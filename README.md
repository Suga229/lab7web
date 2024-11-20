<h1> 1. menjalankan web server dari menu xampp control</h1>

![image](https://github.com/user-attachments/assets/4261d9a3-f448-4aa8-ad20-d6c682ad6ec2)

<h1>2. Buat folde lab7_php_dasar pada root directory server (c:/xampp/htdocs)</h1>

![image](https://github.com/user-attachments/assets/ef9e6baf-3988-4b4e-99c0-c71e8902052c)

<h3>kemudian untuk mengakses directory tersebut pada web server dengan mengakses url</h3>

![image](https://github.com/user-attachments/assets/cbd8f04e-4db9-4c17-b7da-80965d692ff9)

<h1>3. php dasar</h1>
<h4>buat file baru dengan nama php_dasar.php pada directory tersebut</h4>

    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>PHP Dasar</title>
    </head>
    <body>
      <h1>Belajar PHP Dasar</h1>
        <?php
        echo "Hello World";
        ?>
    </body>
    </html>
Kemudian untuk mengakses hasilnya melalui URL: http://localhost/lab7_php_dasar/php_dasar.php

![image](https://github.com/user-attachments/assets/9d8f6112-dac6-4693-a36b-080e66c37e88)

<h1>4. variable php</h1>
Menambahkan variable pada program.
     
    <?php
    $nim = "0411500400";
    $nama = 'Abdullah';
    echo "NIM : " . $nim . "<br>";
    echo "Nama : $nama";
    ?>

![image](https://github.com/user-attachments/assets/7d5e2adc-e696-4a91-a357-3ab9d2081146)

<h1>5. Predefine Variable $_GET</h1>

    <?php
    echo 'Selamat Datang ' . $_GET['nama'];
    ?>

untuk mengaksesnya gunakan url:
http://localhost/lab7_php_dasar/latihan2.php?nama=agus

![image](https://github.com/user-attachments/assets/73ddb6d4-f167-4fb8-9433-3af56d3013ec)

<h1> membuat form input</h1>
    
    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>PHP Dasar</title>
    </head>
    <body>
      <h2>Form Input</h2>
      <form method="post">
      <label>Nama: </label>
      <input type="text" name="nama">
      <input type="submit" value="Kirim">
    </form>
    <?php
    echo 'Selamat Datang ' . $_POST['nama'];
    ?>
    </body>
    </html>

  ![image](https://github.com/user-attachments/assets/2c86ad68-d49d-44d2-94ea-d64d8e451cbc)

<h1>operator</h1>

    <?php
    $gaji = 1000000;
    $pajak = 0.1;
    $thp = $gaji - ($gaji*$pajak);
    echo "Gaji sebelum pajak = Rp. $gaji <br>";
    echo "Gaji yang dibawa pulang = Rp. $thp";
    ?>

![image](https://github.com/user-attachments/assets/c96135c7-0f1b-4c31-93a3-284f7fcafece)

<h1>kondisi if</h1>

    <?php
    $nama_hari = date("l");
    if ($nama_hari == "Sunday") {
    echo "Minggu";
    } elseif ($nama_hari == "Monday") {
    echo "Senin";
    } else {
    echo "Selasa";
    }
    ?>


![image](https://github.com/user-attachments/assets/d553d393-6a84-40a1-989e-2c6fb7be52de)


<h1>kondisi switch</h1>

      <?php
      $nama_hari = date("l");
      switch ($nama_hari) {
      case "Sunday":
      echo "Minggu";
      break;
      case "Monday":
      echo "Senin";
      break;
      case "Tuesday":
          echo "Selasa";
          break;
          default:
          echo "Sabtu";
          ?>


![image](https://github.com/user-attachments/assets/302c52b7-5dbb-480e-824a-f603a5b75298)

<h1>perulangan for</h1>

    <?php
    echo "Perulangan 1 sampai 10 <br />";
    for ($i=1; $i<=10; $i++) {
    echo "Perulangan ke: " . $i . '<br />';
    }
    echo "Perulangan Menurun dari 10 ke 1 <br />";
    for ($i=10; $i>=1; $i--) {
    echo "Perulangan ke: " . $i . '<br />';
    }
    ?>


![image](https://github.com/user-attachments/assets/17eb7453-ffe5-4b5c-952c-406a64dd3e06)

<h2>perulangan while</h2>

    <?php
    echo "Perulangan 1 sampai 10 <br />";
    $i=1;
    while ($i<=10) {
    echo "Perulangan ke: " . $i . '<br />';
    $i++;
    }
    ?>


![image](https://github.com/user-attachments/assets/a6492ae5-18c1-492c-99c0-ae747b90d0a1)

<h1>perulangan dowhile</h1>

    <?php
    echo "Perulangan 1 sampai 10 <br />";
    $i=1;
    do {
    echo "Perulangan ke: " . $i . '<br />';
    $i++;
    } while ($i<=10);
    ?>


![image](https://github.com/user-attachments/assets/181b7f6d-9e23-40f2-a895-17669bc42977)

<h1>pertanyaan dan tugas</h1>

Pertanyaan dan Tugas Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang berbeda-beda sesuai pilihan pekerjaan.

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Form Input</title>
    </head>
    <body>
        <h2>Form Input</h2>
        <form method="post">
            <label>Nama: </label><input type="text" name="nama"><br>
            <label>Tanggal Lahir: </label><input type="date" name="tanggal_lahir"><br>
            <label>Pekerjaan: </label>
            <select name="pekerjaan">
                <option value="front">front end</option>
                <option value="back">back end</option>
                <option value="uiux">ui ux</option>
            </select><br>
            <input type="submit" value="Kirim">
        </form>
    
        <?php
        if ($_SERVER['REQUEST_METHOD'] == 'POST') {
            $nama = $_POST['nama'];
            $tanggal_lahir = $_POST['tanggal_lahir'];
            $pekerjaan = $_POST['pekerjaan'];
    
            
            $tanggal_lahir = new DateTime($tanggal_lahir);
            $sekarang = new DateTime();
            $umur = $sekarang->diff($tanggal_lahir)->y;
    
            
            $gaji = 0;
            if ($pekerjaan == "front") {
                $gaji = 8000000;
            } elseif ($pekerjaan == "back") {
                $gaji = 6000000;
            } elseif ($pekerjaan == "uiux") {
                $gaji = 10000000;
            }
    
            
            echo "<h3>Hasil Input</h3>";
            echo "Nama: $nama<br>";
            echo "Tanggal Lahir: " . $tanggal_lahir->format('d-m-Y') . "<br>";
            echo "Umur: $umur tahun<br>";
            echo "Pekerjaan: " . ucfirst($pekerjaan) . "<br>";
            echo "Gaji: Rp. " . number_format($gaji, 0, ',', '.') . "<br>";
        }
        ?>
    </body>
    </html>

![image](https://github.com/user-attachments/assets/d2a79a67-6363-4adc-89a6-7c1c5cbac246)
