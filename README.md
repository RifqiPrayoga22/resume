<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mastering Dart: Sesi 3 - Constructor & Enkapsulasi</title>
    <style>
        :root {
            --primary: #0175C2;
            --dark-blue: #015f9e;
            --bg: #f4f7f9;
            --text: #2c3e50;
        }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background: var(--bg); margin: 0; color: var(--text); line-height: 1.6; }
        .container { max-width: 1100px; margin: 0 auto; padding: 40px 20px; }
        
        /* Header */
        header { background: linear-gradient(135deg, var(--primary), var(--dark-blue)); color: white; padding: 40px; border-radius: 20px; text-align: center; box-shadow: 0 10px 20px rgba(0,0,0,0.1); margin-bottom: 40px; }
        
        /* Section Styling */
        .section-title { color: var(--primary); border-left: 5px solid var(--primary); padding-left: 15px; margin: 40px 0 20px; }
        .card-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
        .card { background: white; padding: 25px; border-radius: 15px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); }
        
        /* Explanation Blocks */
        .desc-box { background: #e3f2fd; border-radius: 10px; padding: 15px; margin-top: 10px; font-size: 0.95em; }
        code { background: #fee; color: #c0392b; padding: 2px 5px; border-radius: 4px; font-weight: bold; }

        /* Login Simulation */
        .login-box { background: white; max-width: 450px; margin: 40px auto; padding: 35px; border-radius: 20px; box-shadow: 0 15px 35px rgba(0,0,0,0.1); border-top: 8px solid var(--primary); }
        .login-box h3 { text-align: center; margin-bottom: 25px; color: var(--primary); }
        input { width: 100%; padding: 12px; margin: 10px 0; border: 2px solid #eee; border-radius: 10px; transition: 0.3s; }
        input:focus { border-color: var(--primary); outline: none; }
        button { width: 100%; padding: 14px; background: var(--primary); color: white; border: none; border-radius: 10px; font-weight: bold; cursor: pointer; transition: 0.3s; }
        button:hover { background: var(--dark-blue); transform: translateY(-2px); }

        /* DartPad Section */
        .dartpad-wrapper { height: 600px; border: 2px solid #ddd; border-radius: 15px; overflow: hidden; margin-top: 20px; }
        iframe { width: 100%; height: 100%; border: none; }
        
        .status-tag { display: inline-block; padding: 5px 12px; border-radius: 20px; font-size: 0.8em; font-weight: bold; margin-bottom: 10px; }
        .tag-theory { background: #e8f5e9; color: #2e7d32; }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>📖 Resume Materi Sesi 3</h1>
        <p>Konstruktor & Enkapsulasi: Fondasi Keamanan dan Inisialisasi Objek di Dart</p>
    </header>

    <h2 class="section-title">1. Teori Konstruktor</h2>
    <div class="card-grid">
        <div class="card">
            <span class="status-tag tag-theory">Konsep Dasar</span>
            <h3>Apa itu Konstruktor?</h3>
            <p>Konstruktor adalah metode khusus yang dipanggil saat pertama kali objek dibuat. Fungsinya untuk menyiapkan data awal objek.</p>
            <div class="desc-box">
                <strong>Default:</strong> Menginisialisasi field secara langsung.<br>
                <strong>Named:</strong> Membuat banyak cara inisialisasi dalam satu class.
            </div>
        </div>
        <div class="card">
            <span class="status-tag tag-theory">Lanjutan</span>
            <h3>Constant & Initializer</h3>
            <p><strong>Constant Constructor:</strong> Membuat objek yang tidak bisa diubah (immutable), sangat efisien untuk memori.</p>
            <p><strong>Initializer List:</strong> Menetapkan nilai variabel <em>sebelum</em> body konstruktor berjalan. Cocok untuk validasi mentah.</p>
        </div>
    </div>

    

    <h2 class="section-title">2. Teori Enkapsulasi</h2>
    <div class="card-grid">
        <div class="card">
            <span class="status-tag tag-theory">Keamanan Data</span>
            <h3>Public vs Private</h3>
            <p>Enkapsulasi membungkus data agar tidak bisa diakses sembarangan dari luar file.</p>
            <div class="desc-box">
                Gunakan <code>_</code> (underscore) di depan nama variabel untuk menjadikannya <strong>Private</strong>.
            </div>
        </div>
        <div class="card">
            <span class="status-tag tag-theory">Akses Kontrol</span>
            <h3>Getter & Setter</h3>
            <p><strong>Getter:</strong> Menyediakan akses baca saja ke variabel private.</p>
            <p><strong>Setter:</strong> Mengubah nilai variabel private dengan tambahan <strong>Logika Validasi</strong> agar data tetap aman.</p>
        </div>
    </div>

    

    <div class="login-box">
        <h3>🔐 Simulasi Sistem Login</h3>
        <p style="text-align:center; font-size: 0.8em; color: #666;">Menguji Enkapsulasi & Validasi Setter</p>
        <input type="text" id="uName" placeholder="Username (Min 5 Karakter)">
        <input type="password" id="uPass" placeholder="Password (Min 8 Karakter)">
        <input type="email" id="uEmail" placeholder="Email (Harus mengandung @)">
        <button onclick="checkData()">Simpan Data</button>
        <p id="feedback" style="text-align:center; font-weight:bold; margin-top:15px;"></p>
    </div>

    <h2 class="section-title">3. Praktek Langsung (Embedded DartPad)</h2>
    <p>Klik tombol <strong>Run</strong> pada editor di bawah untuk mencoba kode latihan yang sudah kita buat.</p>
    <div class="dartpad-wrapper">
        <iframe src="https://dartpad.dev/embed-dart.html?id=cfec6519ab526f16c35a947bcd9608e9&theme=light"></iframe>
    </div>
</div>

<script>
    function checkData() {
        const u = document.getElementById('uName').value;
        const p = document.getElementById('uPass').value;
        const e = document.getElementById('uEmail').value;
        const f = document.getElementById('feedback');

        // Logika Setter Dart yang disimulasikan
        if (u.length < 5) {
            f.innerText = "❌ Gagal: Username minimal 5 karakter!";
            f.style.color = "#d93025";
        } else if (p.length < 8) {
            f.innerText = "❌ Gagal: Password minimal 8 karakter!";
            f.style.color = "#d93025";
        } else if (!e.includes('@')) {
            f.innerText = "❌ Gagal: Email harus mengandung '@'!";
            f.style.color = "#d93025";
        } else {
            f.innerText = "✅ Sukses: Enkapsulasi Berhasil, Data Disimpan!";
            f.style.color = "#1e8e3e";
        }
    }
</script>

</body>
</html>
