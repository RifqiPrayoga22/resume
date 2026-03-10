
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deep Dive Dart: Constructor & Enkapsulasi</title>
    <style>
        :root {
            --primary: #0175C2;
            --dark: #202124;
            --bg: #f8f9fa;
            --code-bg: #282c34;
            --accent: #e3f2fd;
            --border: #e0e0e0;
        }
        body { font-family: 'Segoe UI', Tahoma, sans-serif; background: var(--bg); margin: 0; color: #333; line-height: 1.8; }
        .container { max-width: 1000px; margin: auto; padding: 40px 20px; }
        
        header { background: linear-gradient(135deg, var(--primary), #005a9e); color: white; padding: 50px 20px; border-radius: 15px; text-align: center; margin-bottom: 40px; box-shadow: 0 4px 20px rgba(0,0,0,0.1); }
        
        .section { background: white; padding: 35px; border-radius: 12px; margin-bottom: 30px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); border-top: 5px solid var(--primary); }
        h2 { color: var(--primary); margin-top: 0; font-size: 1.8rem; border-bottom: 2px solid var(--accent); padding-bottom: 10px; }
        h3 { color: var(--dark); margin-top: 30px; font-size: 1.3rem; background: var(--accent); padding: 5px 15px; border-radius: 5px; }

        .theory-content { margin: 20px 0; }
        .important-note { background: #fff9c4; border-left: 5px solid #fbc02d; padding: 15px; margin: 20px 0; font-style: italic; }
        
        pre { background: var(--code-bg); color: #abb2bf; padding: 20px; border-radius: 10px; overflow-x: auto; font-size: 14px; line-height: 1.5; border: 1px solid #3e4451; }
        code { font-family: 'Fira Code', 'Consolas', monospace; }
        .keyword { color: #c678dd; }
        .class-name { color: #e5c07b; }
        .string { color: #98c379; }
        .comment { color: #5c6370; font-style: italic; }

        .dartpad-wrapper { height: 700px; border: 2px solid var(--border); border-radius: 12px; overflow: hidden; margin-top: 30px; background: white; }
        iframe { width: 100%; height: 100%; border: none; }
        
        .footer { text-align: center; margin-top: 50px; color: #777; font-size: 0.9rem; }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>🚀 Mastering Dart: Sesi 3</h1>
        <p>Bedah Tuntas Mekanisme Objek: Konstruktor & Arsitektur Enkapsulasi</p>
    </header>

    <div class="section">
        <h2>🏗️ 1. Konstruktor (Constructor) Secara Mendalam</h2>
        <div class="theory-content">
            <p>Dalam paradigma Pemrograman Berorientasi Objek (OOP), <strong>Konstruktor</strong> bukan sekadar fungsi biasa. Ia adalah gerbang siklus hidup objek (object lifecycle). Saat kita memanggil <code>new Class()</code>, sistem melakukan alokasi memori, dan konstruktorlah yang bertugas mengisi memori tersebut dengan data yang valid.</p>
            
            

            <h3>A. Generative & Named Constructor</h3>
            <p>Dart memberikan fleksibilitas unik dibandingkan bahasa lain. Jika di Java kita melakukan <em>overloading</em>, di Dart kita menggunakan <strong>Named Constructor</strong>. Hal ini membuat kode lebih terbaca. Misalnya, daripada menebak apa isi parameter konstruktor, kita bisa menggunakan <code>User.fromJSON(data)</code> yang langsung menjelaskan sumber datanya.</p>

            <h3>B. Initializer List (Titik Dua ':')</h3>
            <p>Seringkali kita perlu memvalidasi atau memodifikasi data <strong>sebelum</strong> objek benar-benar tercipta. Di sinilah <em>Initializer List</em> berperan. Ia berjalan sebelum body <code>{}</code> dijalankan. Ini adalah satu-satunya tempat di mana kita bisa menginisialisasi variabel <code>final</code> yang tidak langsung diberi nilai di parameter.</p>

            <div class="important-note">
                <strong>Tips Ahli:</strong> Gunakan Initializer List untuk melakukan sanitasi data mentah dari API sebelum dimasukkan ke dalam properti kelas.
            </div>

            <pre><code><span class="keyword">class</span> <span class="class-name">Mahasiswa</span> {
  <span class="keyword">final</span> String nama;
  <span class="keyword">final</span> int umur;

  <span class="comment">// 1. Generative Constructor: Cara paling ringkas</span>
  Mahasiswa(this.nama, this.umur);

  <span class="comment">// 2. Named Constructor: Memberikan konteks pembuatan objek</span>
  <span class="comment">// 3. Initializer List: Digunakan setelah tanda ':'</span>
  Mahasiswa.dariMap(Map data) 
      : nama = data[<span class="string">'nama'</span>] ?? <span class="string">'Tanpa Nama'</span>,
        umur = data[<span class="string">'umur'</span>] ?? 0 {
    print(<span class="string">"Objek Mahasiswa berhasil dibuat dari Map!"</span>);
  }

  <span class="comment">// 4. Constant Constructor: Objek bersifat immutable (tidak bisa diubah)</span>
  <span class="keyword">const</span> Mahasiswa.tetap(this.nama, this.umur);
}</code></pre>
        </div>
    </div>

    <div class="section">
        <h2>🛡️ 2. Enkapsulasi: Keamanan & Abstraksi Data</h2>
        <div class="theory-content">
            <p><strong>Enkapsulasi</strong> adalah mekanisme penyembunyian status internal suatu objek. Bayangkan sebuah mobil; Anda cukup menginjak pedal gas (interface) tanpa perlu tahu bagaimana sistem pembakaran bekerja di dalam mesin (internal logic). Itulah esensi enkapsulasi.</p>

            

            <h3>A. Library-Level Privacy</h3>
            <p>Berbeda dengan bahasa lain yang menggunakan kata kunci <code>private</code>, Dart menggunakan tanda garis bawah (underscore) <code>_</code>. Namun perlu diingat: variabel <code>_nama</code> hanya benar-benar tersembunyi jika diakses dari <strong>luar file library</strong> tersebut. Ini menjaga integritas data agar tidak diubah secara sengaja maupun tidak sengaja.</p>

            <h3>B. Kekuatan Getter dan Setter</h3>
            <p>Mengapa tidak langsung membuat variabel public saja? Karena dengan <strong>Setter</strong>, kita memiliki kendali penuh. Kita bisa menambahkan filter, logika keamanan, atau bahkan mencatat (log) setiap kali ada perubahan data. <strong>Getter</strong> memungkinkan kita mengembalikan data dalam format yang berbeda tanpa mengubah data aslinya.</p>

            <pre><code><span class="keyword">class</span> <span class="class-name">SistemKeamanan</span> {
  String _kodeRahasia = <span class="string">""</span>;

  <span class="comment">// Setter: Bertindak sebagai firewall</span>
  <span class="keyword">set</span> updateKode(String kodeBaru) {
    <span class="keyword">if</span> (kodeBaru.length > 10) {
      _kodeRahasia = kodeBaru;
      print(<span class="string">"Status: Kode berhasil diperbarui."</span>);
    } <span class="keyword">else</span> {
      print(<span class="string">"Peringatan: Kode baru terlalu lemah!"</span>);
    }
  }

  <span class="comment">// Getter: Memberikan akses baca</span>
  String <span class="keyword">get</span> statusKode => _kodeRahasia.isNotEmpty ? <span class="string">"Aktif"</span> : <span class="string">"Kosong"</span>;
}</code></pre>
        </div>
    </div>

    <div class="section">
        <h2>💻 3. Praktik Implementasi (Live DartPad)</h2>
        <p>Berikut adalah integrasi seluruh materi di atas dalam sebuah kode utuh. Perhatikan bagaimana <strong>Setter</strong> menolak input yang tidak valid pada bagian konsol.</p>
        <div class="dartpad-wrapper">
            <iframe src="https://dartpad.dev/embed-dart.html?id=cfec6519ab526f16c35a947bcd9608e9&theme=dark"></iframe>
        </div>
    </div>

    <div class="footer">
        <p>&copy; 2026 Modul Belajar Dart Sesi 3 - Rifqi Prayoga </p>
    </div>
</div>

</body>
</html>
