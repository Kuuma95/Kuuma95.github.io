<!DOCTYPE HTML>
<html>
<head>
---
layout: post
title:  "Logalstorage "
date:   2013-05-22
excerpt: "Ibu Yamada yang bertugas memandu Kuon sedang memeriksa jadwal hari ini ketika tiba-tiba ia menyadari hari ini ada rapat penting."
tag:
- markdown 
- mathjax
- example
- test
- jekyll
comments: true
---
<meta http-equiv="Content-type" content="text/html; charset=utf-8">
<title>Percobaan HTML5 Local Storage</title>
<script type="text/javascript" charset="utf-8" src="jquery.js"></script>
<script type="text/javascript" >
// fungsi simpan(), ketika tombol diklik maka string 
// di dalam input akan tersimpan ke dalam storage browser
function simpan() {		
	var storage = document.getElementById('nama').value;
	localStorage.setItem('Text',storage);
} 
// tampil() akan menampilkan string yang tersimpan
// ke tag div yang ditentukan "hasil"
function tampil() {
	var tampilNama = localStorage.getItem('Text');
	if (tampilNama) {
	x = document.getElementById('tampil');
	x.innerHTML=tampilNama;
	}
}
// fungsi untuk menghapus localstorage browser
function hapus() {
	localStorage.removeItem('Text');
}
</script>
</head>
	<body>
		<input type="text" id="nama" />
		<input type="button" value="Simpan" onclick="simpan()" />
		<input type="button" value="Tampil" onclick="tampil()" />
		<input type="button" value="Hapus" onclick="hapus()" />
		<div id="tampil"></div>
	</body>
</html>
