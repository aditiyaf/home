---
layout: post
title:  Cara Push Project Menggunakan Git Ke Repository Github
date:   2021-10-14 11:59:30 +0700
image:  git.jpeg
tags:   [Git, GitHub]
---

Git adalah perangkat  <b>Version Control System</b>  atau { VCS } yang diciptakan oleh Linus Torvalds, yang pada awalnya ditujukan untuk pengembangan kernel Linux. Desain Git terinspirasi oleh BitKeeper dan Monotone.

Git dan GitHub merupakan dua platform yang didirikan oleh satu perusahaan dengan tujuan sama serta fitur yang berbeda. Namun kedua platform ini sangat membantu pekerjaan programmer dalam menyusun kode script secara tim. Seluruh pekerjaan juga dapat dipantau dan dievaluasi dengan mudah karena penggunaan kontrol sistem.

Saat ini, hampir menjadi kewajiban bagi programmer untuk menggunakan kedua platform ini dalam pekerjaannya.

Namun di artikel kali ini saya tidak menjelaskan apa perbedaan dari Git atau Github itu sendiri. Namun saya akan memberikan tutorial tentang <i>bagaimana cara menggunakan git, membuat repository di github, login git, hingga push source code program ke github</i>.

### 1. Membuat akun GitHub

Jika kalian belum memiliki akun Github, kalian bisa mendaftar nya <a rel="dofollow" href="https://github.com/signup?user_email=&source=form-home-signup">disini</a> tapi jika kalian sudah memiliki akun GitHub kalian bisa Skip step ini.

### 2. Menginstall Git

Untuk mendownload Git kalian bisa langsung ke halaman resmi nya <a rel="dofollow" href="https://git-scm.com/downloads">disini</a> jika sudah berhasil mendownload kalian bisa langsung <i>menginstall</i> nya sesuai instruksi yang ada pada saat menginstall.

### 3. Membuat Repository di GitHub

Jika sudah masuk ke akun GitHub kalian, langkah selanjutnya adalah membuat repository baru di akun github kalian.
kalo kalian bingung dimana harus membuat repository baru nya kalian bisa langsung <a href="https://github.com/new">kesini</a>.

![]({{site.baseurl}}/img/newrepo.jpg)#80FF00

kalian hanya perlu memberikan nama repository nya sesuai dengan project yang sedang kalian kerjakan yaa.

### 4. Push Project Dari Git Ke GitHub

Kali ini kalian langsung masuk ke folder project yang ingin kalian push ke GitHub kemudian klik kanan pada folder project nya lalu pilih Git Bash Here.

setelah kalian meng-klik Git Bash Here, setelah itu akan muncul Terminal Git Bash,

masukan perintah berikut ini, jika Terminal Git Bash muncul.

{% highlight js %}
$ git init
{% endhighlight %}
{% highlight js %}
$ git add *
{% endhighlight %}
{% highlight js %}
$ git commit -m "optional text"
{% endhighlight %}

kemudian kita akan melakukan remote ke repository GitHub untuk memindahkan semua file yang ada pada folder Project kalian ke GitHub.

kalian bisa merubah <i>git@github.com:aditiyaf/example.git</i> dengan alamat remote dari repository kalian sendiri

{% highlight js %}
$ git remote add origin git@github.com:aditiyaf/example.git
{% endhighlight %}

lalu 

{% highlight js %}
$ git push -u origin master
{% endhighlight %}

yang terakhir tinggal cek di bagian repository github kalian ya, jika berhasil maka akan ada file project di dalam repository GitHub kalian.