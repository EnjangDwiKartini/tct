# Data as s Service 

### Membuat endpoint yang bisa diakses dengan menggunakan GET

* Author : "Enjang Dwi Kartini"
	~~~
	Development tools		: NodeJS
	Framework			: Express
	Sistem Operasi 		: Windows 10
	Bahasa Pemrograman 		: JavaScript
	Text Editor 			: Notepad++
	Web Browser 			: Mozilla Firefox
	~~~
* Lisensi 
    NodeJS  : https://nodejs.org/en/download/

### Tutorial :
* Pertama pastikan komputer kita telah terinstall NodeJS 
* Siapkan Text Editor yang akan digunakan untuk menuliskan script, disini saya menggunakan Notepad++
* Selanjutnya buat folder baru untuk meletakkan project yang akan kita buat , disini saya membuat folder dengan nama minggu-6
* Buka folder minggu-6 dengan menggunakan cmd, perintahnya adalah sebagai berikut :
	~~~
	cd minggu-6
	~~~
* Selanjutnya masukkan perintah 
	~~~
	npm init
	~~~
	Perintah di atas berfungsi untuk mebuat Node package baru. 
* Kita akan diminta untuk meberikan informasi terkait package yang dibuat seperti berikut :
	~~~
	package name: (tct-6)
	version: (1.0.0)
	description:
	entry point: (index.js)
	test command:
	git repository:
	keywords:
	author: EnjangDK
	~~~
	Dalam hal ini kita bisa mengisikan informasi package yang diinginkan seperti nama package, versi, deskripsi, entry point, dan lainnya. Jika sudah selesai, Node akan membuatkan file package.json di dalam direktori minggu-6 yang berisikan informasi yang diisikan tersebut.
* Selanjutnya kita perlu untuk menginstall Framework yang akan digunakan yaitu Express dengan perintah berikut :
	~~~
	npm install --save express
	~~~
* Jika sudah selesai, kita akan coba untuk membuat program  sederhana  yang akan menampilkan data dalam bentuk json dengan menggunakan Express. Buatlah sebuah file baru dengan nama index.js masukan code di bawah ini.
	~~~
	const express = require('express');
	const app = express(); 

	app.get('/', (req, res) => { 
	  res.jsonp({user : 'Enjang Dwi Kartini'});
	}) 

	app.listen(3000, () => console.log("server berjalan pada http://localhost:3000"))
	~~~
* Untuk menjalankan aplikasi yang kita buat tersebut adalah dengan mengetikkan perintah berikut pada cmd:
	~~~
	node index.js
	~~~
* Untuk mengakses program tersebut dengan cara buka http://localhost:3000 menggunakan web browser. Jika berhasil maka akan menampilkan seperti pada tampilan berikut : 

	![alt text](https://github.com/EnjangDwiKartini/tct/blob/master/images/endpoint.PNG "endpoint")

Pada tahap ini kita sudah berhasil menginstall dan membuat sebuah aplikasi yang menampilkan data dalam bentuk json dengan Express. 