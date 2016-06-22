---
<html manifest="demo.appcache">
layout: post
title:  "Pelajaran 1: HAJIMEMASHITE "
date:   2016-03-15
excerpt: "Kuon adalah seorang warga negara Vietnam berusia 25 tahun. Ini adalah hari pertama ia bekerja di kantor pusat. Apakah dia bisa mengucapkan salam dengan benar dalam bahasa Jepang?"
tag:
- markdown 
- syntax
- sample
- test
- jekyll

---
<html>
<head>
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
