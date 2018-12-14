# Data as s Service 

## Belajar Python 3.7

Python adalah bahasa pemrograman tinggi yang dapat melakukan eksekusi sejumlah intruksi multiguna secara langsung (interpretatif) dengan metode orientasi objek (Object Oriented Programming) serta menggunakan semantik dinamis untuk memberikan tingkat keterbacaan syntax.  

* Installasi : https://conda.io/miniconda.html

Target yang akan diselesaikan pada praktikum ini adalah menampilkan data dari database dalam bentuk json. 
Untuk menyelesaikan tugas ini saya menggunakan :
- Framework	: **Flask** 
	***
	Flask adalah kerangka kerja aplikasi web mikro yang ditulis dalam bahasa pemrograman Python dan berdasarkan Werkzeug toolkit dan template engine Jinja2. Berlisensi BSD. (Wikipedia)
	***
- Database : **MySQL**
	***
	MySQL adalah sebuah perangkat lunak sistem manajemen basis data SQL (bahasa Inggris: database management system) atau DBMS yang multialur, multipengguna, dengan sekitar 6 juta instalasi di seluruh dunia. (Wikipedia)
	***

## Tutorial 
* Install miniconda 
* Setelah terinstall maka akan terbentuk sebuah directori dengan nama miniconda3, selanjutnya buka direktoori tersebut dan masuk ke direktori Scripts dengan perintah 
	~~~
	cd C:\Miniconda3\Scripts\
	~~~
* Masukkan perintah berikut :
	~~~
	pip install virtualenv
	~~~
	Vritualenv adalah tools untuk membuat lingkungan python virtual yang terisolasi. Virtual environment (virtualenv) membuat folder baru di dalam direktori proyek. pada dasarnya, foldernya bernama **venv**, tapi kita bisa menggantinya. Ini menjaga Python dan berkas eksekusi pip di dalam folder virtual environment. Ketika virtual environment diaktifkan, paket-paket yang dipasang setelahnya akan terpasang di dalam folder virtual environment. 
* Untuk memulai menggunakan virtualenv, kita harus menginisialisasi dan mengaktifkannya. Navigasikan ke direktori proyek enjang-belajar dan inisialisasi virutal environment dengan mengetik perintah berikut:
	~~~
	virtualenv enjang-belajar
	~~~
	Perintah di atas akan menyiapkan virtual environment untuk proyek enjang-belajar yang berisi direktori - direktori berikut :
	
	![alt text](https://github.com/EnjangDwiKartini/tct/blob/master/images/virtualenv.PNG "virtualenv")
	
* Selanjutnya mengaktifkan virtualenv dengan perintah :
	~~~
	cd ../Scripts
	activate
	~~~
	Maka akan masuk ke dalam lingkungan virtual dan bisa menginstal modul apapun di sini, tanpa harus menggangu proyek atau aplikasi yang lain.
	
	![alt text](https://github.com/EnjangDwiKartini/tct/blob/master/images/activate.PNG "activate")	

* Langkah berikutnya adalah install framework Flask dengan database mysql dengan perintah berikut :
	~~~
	pip install flask_mysqldb
	~~~
	
	![alt text](https://github.com/EnjangDwiKartini/tct/blob/master/images/install-flask.PNG "Flask")
	
* Setelah terinstall maka perlu membuat database terlebih dahulu yang nantinya akan ditampilkan data yang ada dalam database tersebut dalam bentuk json. Disini saya membuat database dengan nama tct 

	![alt text](https://github.com/EnjangDwiKartini/tct/blob/master/images/create-db.PNG "create db")	
	
	Pada  database tct saya buat sebuah table dengan nama jajanan_pasar dan mengisikan data didalamnya  yang strukturnya seperti berikut :
	
	![alt text](https://github.com/EnjangDwiKartini/tct/blob/master/images/table.PNG "table")		
	
* Selanjutnya buat direktori app dalam direktori proyek enjang-belajar dan buat file dengan nama app.py yang nantinya file ini yang akan dijalankan dimana pada app.py ini berisi script berikut :
	~~~
	from flask import Flask
	from flaskext.mysql import MySQL

	app = Flask(__name__)
	app.config['MYSQL_DATABASE_HOST'] = 'localhost'
	app.config['MYSQL_DATABASE_USER'] = 'root'
	app.config['MYSQL_DATABASE_PASSWORD'] = ''
	app.config['MYSQL_DATABASE_DB'] = 'tct'
	mysql = MySQL(app)

	@app.route('/')
	def index():
		cur = mysql.connect().cursor()
		cur.execute('''SELECT * from jajanan_pasar ''')
		rv = cur.fetchall()
		return str(rv)

	if __name__ == '__main__':
		app.run(debug=True)
	~~~
	
* Jalankan script tersebut dengan perintah berikut :

	![alt text](https://github.com/EnjangDwiKartini/tct/blob/master/images/running.PNG "run")	
	
* Buka http://127.0.0.1:5000/ pada browser, maka akan menampilkan semua data yang ada pada table jajanan_pasar dalam bentuk json seperti berikut :

	![alt text](https://github.com/EnjangDwiKartini/tct/blob/master/images/tampilan-data.PNG "data")


	
	
	





