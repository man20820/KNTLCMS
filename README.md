
KNTLCMS Content Management System . CMS untuk ketik url/nama di facebook<br>
Contohnya adalah seperti masukan namasitus.com/namakamu nanti akan muncul sesuatu<br>
KNTLCMS ini berlisensi opensource dan boleh dipakai gratis asalkan jangan hilangkan watermark / atribut KNTLCMS dan dilarang distribusi KNTLCMS untuk mendapatkan uang

<h2>Syarat WebServer</h2>
- PHP 7.0 keatas (belum dites di php 5.6 kebawah tapi ini CMS di debug memakai PHP 7.1)
- VPS (pake hosting bisa tapi tidak maksimal dan tidak direkomendasi)
- MySQL
- nginx (pake apache bisa tapi tidak maksimal . lebih baik murtad ke nginx)


<h2>Cara Install</h2>
1. Clone seluruh repository KNTLCMS 
2. chmod file config.php menjadi 766
3. pergi ke namasitus.com/install
4. lakukan instalasi . pastikan detail database mysql benar
5. KNTLCMS sukses terinstall
<b>
WARNING! setelah melakukan install . instalasi KNTLCMS anda hanya bia dipakai memakai namasitus.com/nama?namakamu bukan namasitus.com/namakamu . untuk fix masalah ini silahkan ikuti cara selanjutnya</b>

<h2>Cara Agar bisa namasitus.com/namakamu</h2>
<b>WARNING! Hanya untuk VPS saja . dan hanya untuk webserver nginx saja . jika memakai apache mohon murtad ke nginx untuk mengaktifkan fitur ini . tidak work untuk hosting</b><br>
1. Buka Config Situs . biasanya ada di /etc/nginx/sites-enabled/namasitus.conf<br>
2. cari bagian location / { dan ganti menjadi seperti berikut <br>

>  location / {<br>
>   index index.php ;<br>
>   try_files $uri $uri/ /index.php?nama=$uri;<br>
>  }<br>

3. Save file dan restart nginx menggunakan command "systemctl nginx restart"<br>

<h2>Demo / Contoh Karya hasil KNTLCMS</h2>
<a href src="http://setomulyadi.ml">setomulyadi.ml | Quotes Kak Seto</a>
