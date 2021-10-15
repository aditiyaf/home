---
layout: post
title:  Manipulasi Direktori Menggunakan PHP
date:   2021-10-14 13:25:55 +0700
image:  php.png
tags:   [PHP]
---
Direktori adalah lokasi penyimpanan pada file system yang dapat berisi kumpulan file dan direktori.

Ada beberapa fungsi yang dapat digunakan di PHP untuk manipulasi direktori:

> 1. Fungsi <b>mkdir()</b> untuk membuat direktori;
> 2. Fungsi <b>scandir()</b> untuk melihat isi direktori;
> 3. Fungsi <b>rmdir()</b> untuk menghapus direktori;
> 4. Fungsi <b>rename()</b> untuk mengubah nama direktori;

so, mari kita bahas fungsi masing-masing dari perintah diatas.

### 1. Membuat Direktori di PHP

Fungsi yang digunakan untuk membuat direktori di PHP adalah <b>mkdir()</b>. Fungsi ini sama maksudnya dengan perintah mkdir di Linux dan <b>md</b> pada Windows.

Parameter yang diberikan ke fungsi <b>mkdir()</b> berupa string. Parameter ini yang akan menjadi nama direktori.

###### Contoh :
 
 {% highlight js %}
 <?php mkdir("direktori_baru"); ?>
 {% endhighlight %}
 
 Atau kita juga bisa memberikan alamat path, dan atributnya:
 
 {% highlight js %}
 <?php mkdir("./direktori_lama/contoh/dir", 0777, true); ?>
  {% endhighlight %}
  
##### Keterangan :
  
  > Parameter <b>0777</b> adalah hak akses yang kita berikan kepada direktori;
  > Parameter <b>true</b> artinya kita mengizinkan pembuatan direktori secara rekursif.
  
### 2.Melihat isi Direktori di PHP

Fungsi yang digunakan untuk melihat isi direktori adalah <b>scandir()</b>. Fungsi ini akan mengembalikan nilai berupa array yang berisi nama-nama dari isi direktori.

###### Contoh :

 {% highlight js %}
<?php
$dir = scandir("direktori_lawas");
print_r($dir);
?>
 {% endhighlight %}
 
 Maka variabel <b>$dir</b> akan berisi:
 
  {% highlight js %}
Array
(
    [0] => .
    [1] => ..
    [2] => contoh
)
 {% endhighlight %}
 
 Dengan begini, kita bisa memanfaatkan perulangan untuk menampilka semua isi dari direktori.

### 3.Menghapus Direktori di PHP

Menghapus direktori dapat dilakukan dengan fungsi <b>rmdir()</b>. Fungsi ini memiliki parameter berupa string. Parameter tersebut adalah nama direktori yang ingin dihapus.

###### Contoh :

 {% highlight js %}
<?php rmdir("nama_direktori"); ?>
 {% endhighlight %}
 
 Fungsi <b>rmdir()</b> akan menghasilkan error apabila direktorinya tidak ditemukan. Untuk mengatasi ini, kita bisa menggunakan fungsi <b>is_dir()</b> untuk mengecek direktorinya ada atau tidak.
 
###### Contoh :

 {% highlight js %}
<?php
$nama_dir = "direktori_baru";

if( is_dir($nama_dir) ) {
    rmdir($nama_dir); 
} else {
    echo "Direktori tidak ditemukan"; 
}
?>
 {% endhighlight %}
 
### 4.Mengubah Nama Direktori di PHP

Kita dapat merubah nama direktori dengan fungsi <b>rename()</b>. Fungsi ini tidak hanya untuk merubah nama direktori, mengubah nama file juga dapat menggunakan fungsi ini.

Ada dua parameter yang harus diberikan kepada fungsi ini. Pertama, nama file atau direktori yang akan diubah. Kedua, nama barunya.

###### Contoh :

 {% highlight js %}
<?php rename("nama_lama", "“nama_baru"); ?>
 {% endhighlight %}