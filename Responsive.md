# 1 Agustus 2022 - 5 Agustus 2022

## Responsive
Responsive web design adalah tampilan website yang bisa menyesuaikan dengan device pengguna. Website yang responsif yaitu website yang mampu menyesuaikan layout saat tampil di berbagai jenis device dengan ukuran layar berbeda.
Responsive Design dikembangkan melalui kode-kode CSS.

<b>Mengatur Viewport</b>

Untuk membuat situs web responsif, tambahkan tag <meta> seperti contoh dibawah ini:

>meta name="viewport" content="width=device-width, initial-scale=1.0"

<b>Responsive Images</b>

Responsive images adalah gambar yang diskalakan dengan baik agar sesuai dengan ukuran browser apapun.

Jika lebar CSS disetel ke 100%, gambar akan responsif dan skala naik turun, contohnya:

>img src="img_girl.jpg" style="width:100%;"

Jika properti max-width diatur ke 100%, gambar akan diperkecil jika perlu, tetapi tidak pernah memperbesar lebih besar dari ukuran aslinya, contohnya:

>img src="img_girl.jpg" style="max-width:100%;height:auto;"

<b>Menampilkan Gambar Berbeda Tergantung pada Lebar Browser</b>

Elemen HTML <picture> memungkinkan kita untuk menentukan gambar yang berbeda untuk ukuran jendela browser yang berbeda, contohnya:

<picture>
  <source srcset="img_smallflower.jpg" media="(max-width: 600px)">
  <source srcset="img_flowers.jpg" media="(max-width: 1500px)">
  <source srcset="flowers.jpg">
  <img src="img_smallflower.jpg" alt="Flowers">
</picture>

<b>Responsive Ukuran Teks</b>

Ukuran teks dapat diatur dengan satuan "vw", yang berarti "lebar viewport". Dengan begitu ukuran teks akan mengikuti ukuran jendela browser, contohnya:

><h1 style="font-size:10vw">Hello World</h1>

>Viewport adalah ukuran jendela browser. 1vw = 1% dari lebar viewport. Jika viewport lebarnya 50cm, 1vw adalah 0,5cm.

<b>Media Queries</b>

Dengan media queries, kita dapat menentukan gaya yang sama sekali berbeda untuk ukuran browser yang berbeda.
contohnya :

@media(min-width:992px) {
       .selector { 
             width:970px; 
        }
} 

@media(max-width:768px) {
        .selector { 
              width:750px;
        }
}

<b>Bootstrap</b>

Kerangka kerja CSS populer lainnya adalah Bootstrap. Bootstrap menggunakan HTML, CSS dan jQuery untuk membuat halaman web yang responsif.

<!DOCTYPE html>
<html lang="en">
<head>
<title>Bootstrap Example</title>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>
</head>
<body>

<div class="container">
  <div class="jumbotron">
    <h1>this is Bootstrap</h1>
  </div>
  <div class="row">
    <div class="col-sm-4">
      ...
    </div>
    <div class="col-sm-4">
      ...
    </div>
    <div class="col-sm-4">
    ...
    </div>
  </div>
</div>

</body>
</html>