<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Deep Dive Dart: Constructor & Enkapsulasi</title>

<style>
:root{
--primary:#0175C2;
--dark:#202124;
--bg:#f8f9fa;
--code-bg:#282c34;
--accent:#e3f2fd;
--border:#e0e0e0;
}

body{
font-family:'Segoe UI',Tahoma,sans-serif;
background:var(--bg);
margin:0;
color:#333;
line-height:1.8;
}

.container{
max-width:1000px;
margin:auto;
padding:40px 20px;
}

header{
background:linear-gradient(135deg,var(--primary),#005a9e);
color:white;
padding:50px 20px;
border-radius:15px;
text-align:center;
margin-bottom:40px;
box-shadow:0 4px 20px rgba(0,0,0,0.1);
}

.section{
background:white;
padding:35px;
border-radius:12px;
margin-bottom:30px;
box-shadow:0 4px 6px rgba(0,0,0,0.05);
border-top:5px solid var(--primary);
}

h2{
color:var(--primary);
margin-top:0;
font-size:1.8rem;
border-bottom:2px solid var(--accent);
padding-bottom:10px;
}

h3{
color:var(--dark);
margin-top:30px;
font-size:1.3rem;
background:var(--accent);
padding:5px 15px;
border-radius:5px;
}

pre{
background:var(--code-bg);
color:#abb2bf;
padding:20px;
border-radius:10px;
overflow-x:auto;
font-size:14px;
line-height:1.5;
border:1px solid #3e4451;
}

.dartpad-wrapper{
height:700px;
border:2px solid var(--border);
border-radius:12px;
overflow:hidden;
margin-top:30px;
}

iframe{
width:100%;
height:100%;
border:none;
}

.footer{
text-align:center;
margin-top:50px;
color:#777;
font-size:0.9rem;
}
</style>
</head>

<body>

<div class="container">

<header>
<h1>🚀 Mastering Dart: Sesi 3</h1>
<p>Konstruktor dan Enkapsulasi dalam Pemrograman Dart</p>
</header>
<header>
        <p><b>Nama :</b> Rifqi Prayoga</p>
        <p><b>NIM :</b> 251410005</p>
        <p><b>Kelas :</b> SI2A</p>
</header>


<div class="section">
<h2>📘 Tujuan Pembelajaran</h2>

<p>
Pada sesi ini peserta mempelajari konsep penting dalam pemrograman berorientasi objek
(Object Oriented Programming) yaitu <b>Constructor</b> dan <b>Enkapsulasi</b>.
Kedua konsep ini sangat penting karena hampir seluruh aplikasi modern yang dibuat
menggunakan bahasa pemrograman berbasis objek selalu memanfaatkan kedua konsep tersebut.
Dengan memahami constructor, seorang programmer dapat membuat objek dengan kondisi
awal yang benar. Sedangkan dengan memahami enkapsulasi, programmer dapat melindungi
data di dalam class agar tidak diakses secara sembarangan oleh bagian program lain.
</p>

<p>
Setelah menyelesaikan sesi ini peserta diharapkan mampu memahami berbagai jenis
constructor dalam Dart, memahami bagaimana mekanisme initializer list bekerja,
serta mampu mengimplementasikan enkapsulasi menggunakan variabel private,
getter, dan setter untuk menjaga integritas data dalam sebuah program.
</p>

</div>



<div class="section">

<h2>📖 1. Theory </h2>

<h3>1.1 Jenis-jenis Constructor di Dart</h3>

<p>
Constructor adalah sebuah method khusus dalam sebuah class yang secara otomatis
dipanggil ketika objek dari class tersebut dibuat. Fungsi utama dari constructor
adalah untuk menginisialisasi nilai awal dari properti yang dimiliki oleh objek.
Dengan adanya constructor, programmer dapat memastikan bahwa setiap objek yang
dibuat memiliki data awal yang valid.
</p>

<p>
Dalam bahasa pemrograman Dart terdapat beberapa jenis constructor yang dapat
digunakan untuk membuat objek dengan berbagai cara. Constructor paling dasar
disebut dengan <b>default constructor</b> atau <b>generative constructor</b>.
Constructor ini biasanya digunakan untuk mengisi nilai properti class langsung
melalui parameter constructor.
</p>

<pre><code>
class Mahasiswa{

String nama;
int umur;

Mahasiswa(this.nama,this.umur);

}
</code></pre>

<p>
Ketika objek dibuat menggunakan constructor tersebut, maka nilai parameter
yang diberikan akan langsung dimasukkan ke dalam properti class.
</p>



<h3>1.2 Constant Constructor</h3>

<p>
Constant constructor digunakan ketika kita ingin membuat objek yang bersifat
konstan atau tidak dapat diubah setelah objek tersebut dibuat. Dalam Dart,
constant constructor ditandai dengan penggunaan keyword <b>const</b>.
Penggunaan constant constructor sangat bermanfaat ketika kita ingin membuat
objek yang tidak berubah selama program berjalan, misalnya pada objek
koordinat, konfigurasi sistem, atau data statis lainnya.
</p>

<p>
Agar sebuah class dapat menggunakan constant constructor, semua field
di dalam class tersebut harus bertipe <b>final</b>. Hal ini dilakukan agar
nilai dari field tersebut tidak dapat dimodifikasi setelah objek dibuat.
</p>

<pre><code>
class Point{

final int x;
final int y;

const Point(this.x,this.y);

}
</code></pre>



<h3>1.3 Constructor dengan Initializer List</h3>

<p>
Initializer list merupakan fitur dalam Dart yang digunakan untuk
menginisialisasi nilai properti sebelum constructor utama dijalankan.
Initializer list ditandai dengan penggunaan tanda titik dua (:)
setelah deklarasi constructor.
</p>

<p>
Initializer list sering digunakan ketika kita ingin melakukan
transformasi data atau validasi sebelum nilai tersebut disimpan
ke dalam properti class.
</p>

<pre><code>
class User{

final String username;

User(String name)
: username = name.toLowerCase();

}
</code></pre>



<h3>1.4 Pengantar Enkapsulasi</h3>

<p>
Enkapsulasi merupakan salah satu prinsip utama dalam pemrograman
berorientasi objek. Konsep ini digunakan untuk menyembunyikan data
internal suatu objek agar tidak dapat diakses secara langsung oleh
kode di luar class tersebut.
</p>

<p>
Dengan menggunakan enkapsulasi, programmer dapat memastikan bahwa
data yang disimpan dalam sebuah objek hanya dapat diakses melalui
mekanisme tertentu yang telah ditentukan oleh class tersebut.
Hal ini membantu menjaga keamanan data serta mencegah terjadinya
kesalahan manipulasi data dari luar class.
</p>



<h3>1.5 Public vs Private di Dart</h3>

<p>
Dalam Dart, konsep public dan private tidak menggunakan keyword
seperti pada beberapa bahasa pemrograman lain. Sebagai gantinya,
Dart menggunakan tanda underscore (_) di awal nama variabel
untuk menandakan bahwa variabel tersebut bersifat private.
</p>

<p>
Variabel private hanya dapat diakses di dalam file yang sama
(library yang sama) sehingga membantu menjaga keamanan data.
</p>

<pre><code>
class User{

String username;
String _password;

}
</code></pre>



<h3>1.6 Getter – Mengakses Data Private</h3>

<p>
Getter adalah method khusus yang digunakan untuk membaca nilai
dari variabel private. Dengan menggunakan getter, kita tetap
dapat mengakses data private tanpa harus membuka akses langsung
ke variabel tersebut.
</p>

<pre><code>
class User{

String _username="rifqi";

String get username{

return _username;

}

}
</code></pre>



<h3>1.7 Setter – Memodifikasi Data Private</h3>

<p>
Setter digunakan untuk mengubah nilai variabel private dengan
menambahkan proses validasi terlebih dahulu. Dengan setter,
program dapat memastikan bahwa data yang dimasukkan oleh user
memenuhi aturan tertentu sebelum disimpan dalam variabel.
</p>

<pre><code>
class User{

String _password="";

set password(String value){

if(value.length>=8){

_password=value;

}

}

}
</code></pre>

</div>



<div class="section">

<h2>💻 2. Practice</h2>

<p>
Pada bagian praktik ini peserta diminta mencoba berbagai contoh
implementasi constructor dan enkapsulasi secara langsung dalam
program Dart.
</p>

<pre><code>
class Mahasiswa{

String nama;
int umur;

Mahasiswa(this.nama,this.umur);

Mahasiswa.tanpaNama(){

nama="Tanpa Nama";
umur=0;

}

}
</code></pre>

</div>



<div class="section">

<h2>🧠 3. Latihan </h2>

<p>
Latihan ini bertujuan untuk melatih pemahaman peserta mengenai
pembuatan multiple constructor dan penerapan enkapsulasi lengkap.
</p>

<pre><code>
class Mahasiswa{

String nama;
String nim;

Mahasiswa(this.nama,this.nim);

Mahasiswa.dariMap(Map data)
: nama=data["nama"],
nim=data["nim"];

Mahasiswa.tanpaNama(){

nama="Tanpa Nama";
nim="0000";

}

}
</code></pre>

</div>



<div class="section">

<h2>📊 4. Contoh Kasus</h2>

<p>
Contoh kasus berikut memperlihatkan bagaimana konsep getter
dan setter digunakan dalam sistem login sederhana.
</p>

<pre><code>
class Login{

String _username="admin";
String _password="12345678";

bool login(String user,String pass){

return user==_username && pass==_password;

}

}
</code></pre>

</div>



<div class="section">

<h2>💻 Implementasi Interaktif (DartPad)</h2>

<div class="dartpad-wrapper">
<iframe src="https://dartpad.dev/embed-dart.html?id=cfec6519ab526f16c35a947bcd9608e9&theme=dark"></iframe>
</div>

</div>


<div class="footer">
<p>© 2026 Modul Belajar Dart Sesi 3 - Rifqi Prayoga</p>
</div>

</div>

</body>
</html>
