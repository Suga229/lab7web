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
