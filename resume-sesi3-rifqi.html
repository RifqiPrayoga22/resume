<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Deep Dive Dart: Constructor & Enkapsulasi</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root {
  --primary: #0175C2;
  --primary-dark: #005a9e;
  --primary-light: #e3f2fd;
  --dark: #0d1117;
  --bg: #f0f4f8;
  --white: #ffffff;
  --border: #d1dbe6;
  --text: #1a2332;
  --text-muted: #5a6a7e;
  --code-bg: #0d1117;
  --code-text: #e6edf3;
  --green: #22c55e;
  --red: #ef4444;
  --orange: #f77f00;
  --teal: #00b4d8;
  --section-num: #0175C2;
  --tag-bg: #dbeafe;
  --tag-color: #1d4ed8;
}

* { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: 'Plus Jakarta Sans', sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.75;
}

.container {
  max-width: 960px;
  margin: 0 auto;
  padding: 48px 24px;
}

/* ─── HEADER ─────────────────────────────────────────────── */
header {
  background: linear-gradient(135deg, #0175C2 0%, #003d82 60%, #001e4a 100%);
  border-radius: 20px;
  padding: 56px 48px;
  text-align: center;
  margin-bottom: 48px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 24px 60px rgba(1, 117, 194, 0.3);
}

header::before {
  content: '';
  position: absolute;
  top: -80px; right: -80px;
  width: 300px; height: 300px;
  background: rgba(255,255,255,0.04);
  border-radius: 50%;
}

header::after {
  content: '';
  position: absolute;
  bottom: -60px; left: -60px;
  width: 200px; height: 200px;
  background: rgba(0,180,216,0.12);
  border-radius: 50%;
}

header h1 {
  color: #fff;
  font-size: 2rem;
  font-weight: 800;
  letter-spacing: -0.5px;
  margin-bottom: 20px;
  position: relative;
  z-index: 1;
}

.header-badge {
  display: inline-block;
  background: rgba(255,255,255,0.15);
  border: 1px solid rgba(255,255,255,0.25);
  border-radius: 50px;
  padding: 6px 20px;
  font-size: 0.8rem;
  color: #90caf9;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  font-weight: 600;
  margin-bottom: 24px;
  position: relative;
  z-index: 1;
}

.identity-card {
  display: inline-flex;
  gap: 32px;
  background: rgba(255,255,255,0.1);
  border: 1px solid rgba(255,255,255,0.2);
  border-radius: 12px;
  padding: 20px 36px;
  margin-top: 8px;
  position: relative;
  z-index: 1;
}

.identity-item {
  text-align: center;
}

.identity-label {
  font-size: 0.7rem;
  color: #90caf9;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: 600;
  display: block;
  margin-bottom: 4px;
}

.identity-value {
  color: #fff;
  font-size: 0.95rem;
  font-weight: 700;
}

/* ─── TOC ─────────────────────────────────────────────────── */
.toc {
  background: var(--white);
  border-radius: 16px;
  padding: 28px 32px;
  margin-bottom: 40px;
  border: 1px solid var(--border);
  box-shadow: 0 4px 20px rgba(0,0,0,0.05);
}

.toc-title {
  font-size: 0.75rem;
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: 1.5px;
  font-weight: 700;
  margin-bottom: 16px;
  display: flex;
  align-items: center;
  gap: 8px;
}

.toc-title::after {
  content: '';
  flex: 1;
  height: 1px;
  background: var(--border);
}

.toc-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 8px;
}

.toc-item {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 8px 12px;
  border-radius: 8px;
  text-decoration: none;
  color: var(--text);
  font-size: 0.88rem;
  font-weight: 500;
  transition: background 0.2s;
}

.toc-item:hover { background: var(--primary-light); color: var(--primary); }

.toc-num {
  width: 24px; height: 24px;
  background: var(--primary);
  color: #fff;
  border-radius: 6px;
  font-size: 0.72rem;
  font-weight: 700;
  display: flex; align-items: center; justify-content: center;
  flex-shrink: 0;
}

/* ─── SECTION CARDS ───────────────────────────────────────── */
.section {
  background: var(--white);
  border-radius: 16px;
  padding: 40px;
  margin-bottom: 32px;
  border: 1px solid var(--border);
  box-shadow: 0 4px 24px rgba(0,0,0,0.05);
  position: relative;
  overflow: hidden;
}

.section::before {
  content: '';
  position: absolute;
  top: 0; left: 0;
  width: 4px; height: 100%;
  background: var(--primary);
}

.section-header {
  display: flex;
  align-items: flex-start;
  gap: 16px;
  margin-bottom: 20px;
  padding-bottom: 20px;
  border-bottom: 1px solid var(--border);
}

.section-number {
  width: 40px; height: 40px;
  background: linear-gradient(135deg, var(--primary), var(--primary-dark));
  color: #fff;
  border-radius: 10px;
  font-size: 1rem;
  font-weight: 800;
  display: flex; align-items: center; justify-content: center;
  flex-shrink: 0;
  margin-top: 2px;
}

.section-title-wrap h2 {
  color: var(--text);
  font-size: 1.3rem;
  font-weight: 800;
  line-height: 1.3;
}

.section-subtitle {
  font-size: 0.8rem;
  color: var(--text-muted);
  font-weight: 500;
  margin-top: 3px;
}

.section p {
  color: var(--text-muted);
  margin-bottom: 16px;
  font-size: 0.95rem;
  line-height: 1.8;
}

/* ─── INFO BOXES ──────────────────────────────────────────── */
.info-row {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 12px;
  margin: 20px 0;
}

.info-box {
  border-radius: 10px;
  padding: 16px 18px;
  border-left: 4px solid;
}

.info-box.blue  { background: #eff6ff; border-color: var(--primary); }
.info-box.green { background: #f0fdf4; border-color: var(--green); }
.info-box.orange{ background: #fff7ed; border-color: var(--orange); }
.info-box.teal  { background: #ecfeff; border-color: var(--teal); }

.info-box-title {
  font-size: 0.75rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.8px;
  margin-bottom: 4px;
}

.blue  .info-box-title { color: var(--primary); }
.green .info-box-title { color: #16a34a; }
.orange .info-box-title{ color: #c2410c; }
.teal  .info-box-title { color: #0891b2; }

.info-box p {
  font-size: 0.88rem;
  margin: 0;
  color: var(--text);
}

/* ─── COMPARISON TABLE ────────────────────────────────────── */
.compare-table {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
  margin: 20px 0;
}

.compare-col {
  border-radius: 12px;
  padding: 20px;
  border: 2px solid;
}

.compare-col.pub  { background: #f0fdf4; border-color: var(--green); }
.compare-col.priv { background: #fff1f2; border-color: var(--red); }

.compare-col h3 {
  font-size: 1rem;
  font-weight: 800;
  margin-bottom: 12px;
  display: flex;
  align-items: center;
  gap: 8px;
}

.pub h3  { color: #15803d; }
.priv h3 { color: #dc2626; }

.compare-col ul {
  list-style: none;
  padding: 0;
}

.compare-col ul li {
  font-size: 0.88rem;
  color: var(--text);
  padding: 5px 0;
  border-bottom: 1px dashed rgba(0,0,0,0.06);
  display: flex;
  gap: 8px;
}

.compare-col ul li::before { content: '→'; opacity: 0.5; flex-shrink: 0; }

/* ─── BADGE TAGS ──────────────────────────────────────────── */
.tags { display: flex; flex-wrap: wrap; gap: 8px; margin: 12px 0; }

.tag {
  background: var(--tag-bg);
  color: var(--tag-color);
  border-radius: 20px;
  padding: 4px 12px;
  font-size: 0.75rem;
  font-weight: 700;
  letter-spacing: 0.3px;
}

/* ─── HIGHLIGHT NOTE ──────────────────────────────────────── */
.note {
  display: flex;
  gap: 12px;
  background: #fffbeb;
  border: 1px solid #fcd34d;
  border-radius: 10px;
  padding: 14px 18px;
  margin: 16px 0;
  font-size: 0.9rem;
  color: #92400e;
  font-weight: 500;
}

.note-icon { font-size: 1.1rem; flex-shrink: 0; }

/* ─── CODE BLOCKS ─────────────────────────────────────────── */
.code-wrap {
  margin: 20px 0;
  border-radius: 12px;
  overflow: hidden;
  border: 1px solid #30363d;
  box-shadow: 0 8px 30px rgba(0,0,0,0.12);
}

.code-header {
  background: #161b22;
  padding: 10px 18px;
  display: flex;
  align-items: center;
  gap: 8px;
}

.code-dots { display: flex; gap: 6px; }
.dot { width: 12px; height: 12px; border-radius: 50%; }
.dot.r { background: #ef4444; }
.dot.y { background: #f59e0b; }
.dot.g { background: #22c55e; }

.code-lang {
  margin-left: auto;
  font-size: 0.7rem;
  color: #8b949e;
  font-family: 'JetBrains Mono', monospace;
  letter-spacing: 0.5px;
  background: #21262d;
  padding: 2px 10px;
  border-radius: 4px;
}

pre {
  background: var(--code-bg) !important;
  color: var(--code-text) !important;
  padding: 22px 24px !important;
  margin: 0 !important;
  overflow-x: auto;
  font-size: 0.82rem !important;
  line-height: 1.7 !important;
  font-family: 'JetBrains Mono', Consolas, monospace !important;
}

/* Syntax highlights */
.kw { color: #ff7b72; }        /* keywords */
.kw2 { color: #79c0ff; }       /* types/class names */
.fn { color: #d2a8ff; }        /* functions */
.str { color: #a5d6ff; }       /* strings */
.num { color: #f2cc60; }       /* numbers */
.cmt { color: #8b949e; font-style: italic; } /* comments */
.op { color: #ff7b72; }        /* operators */
.var { color: #ffa657; }       /* variables */

/* ─── DARTPAD ─────────────────────────────────────────────── */
.dartpad-section {
  margin-top: 24px;
}

.dartpad-label {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 0.75rem;
  color: var(--text-muted);
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 1px;
  margin-bottom: 10px;
}

.dartpad-label::before {
  content: '';
  width: 8px; height: 8px;
  background: var(--green);
  border-radius: 50%;
  box-shadow: 0 0 0 3px rgba(34,197,94,0.2);
}

.dartpad-wrapper {
  height: 480px;
  border: 2px solid var(--border);
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 20px rgba(0,0,0,0.07);
}

iframe { width: 100%; height: 100%; border: none; }

/* ─── FOOTER ──────────────────────────────────────────────── */
footer {
  text-align: center;
  margin-top: 60px;
  padding-top: 32px;
  border-top: 1px solid var(--border);
  color: var(--text-muted);
  font-size: 0.85rem;
}

/* ─── RESPONSIVE ──────────────────────────────────────────── */
@media (max-width: 640px) {
  .identity-card { flex-direction: column; gap: 16px; padding: 20px; }
  .compare-table { grid-template-columns: 1fr; }
  .section { padding: 24px; }
  header { padding: 36px 24px; }
}
</style>
</head>

<body>
<div class="container">

<!-- ═══════════════ HEADER ═══════════════ -->
<header>
  <div class="header-badge">Dart OOP Series · Sesi 3</div>
  <h1>🚀 Konstruktor dan Enkapsulasi</h1>
  <div class="identity-card">
    <div class="identity-item">
      <span class="identity-label">Nama</span>
      <span class="identity-value">Rifqi Prayoga</span>
    </div>
    <div class="identity-item">
      <span class="identity-label">Kelas</span>
      <span class="identity-value">SI2A</span>
    </div>
    <div class="identity-item">
      <span class="identity-label">NIM</span>
      <span class="identity-value">251410005</span>
    </div>
  </div>
</header>

<!-- ═══════════════ TOC ═══════════════ -->
<nav class="toc">
  <div class="toc-title">Daftar Isi</div>
  <div class="toc-grid">
    <a href="#s1" class="toc-item"><span class="toc-num">1</span> Jenis-jenis Constructor</a>
    <a href="#s2" class="toc-item"><span class="toc-num">2</span> Constant Constructor</a>
    <a href="#s3" class="toc-item"><span class="toc-num">3</span> Initializer List</a>
    <a href="#s4" class="toc-item"><span class="toc-num">4</span> Enkapsulasi</a>
    <a href="#s5" class="toc-item"><span class="toc-num">5</span> Public vs Private</a>
    <a href="#s6" class="toc-item"><span class="toc-num">6</span> Getter</a>
    <a href="#s7" class="toc-item"><span class="toc-num">7</span> Setter</a>
    <a href="#s8" class="toc-item"><span class="toc-num">8</span> Multiple Constructor</a>
    <a href="#s9" class="toc-item"><span class="toc-num">9</span> Sistem Login Sederhana</a>
  </div>
</nav>

<!-- ═══════════════ SECTION 1 ═══════════════ -->
<div class="section" id="s1">
  <div class="section-header">
    <div class="section-number">1</div>
    <div class="section-title-wrap">
      <h2>Jenis-jenis Constructor di Dart</h2>
      <div class="section-subtitle">Theory — Konstruktor</div>
    </div>
  </div>

  <p>Constructor adalah method khusus dalam sebuah class yang digunakan untuk membuat objek. Constructor dipanggil otomatis saat objek dibuat dan berfungsi menginisialisasi nilai awal dari properti class.</p>

  <div class="info-row">
    <div class="info-box blue">
      <div class="info-box-title">Default Constructor</div>
      <p>Dibuat otomatis jika tidak ada constructor lain yang didefinisikan.</p>
    </div>
    <div class="info-box teal">
      <div class="info-box-title">Parameterized Constructor</div>
      <p>Menerima parameter untuk inisialisasi nilai field saat objek dibuat.</p>
    </div>
    <div class="info-box green">
      <div class="info-box-title">Named Constructor</div>
      <p>Constructor dengan nama khusus: <code>Class.namaConstructor()</code></p>
    </div>
    <div class="info-box orange">
      <div class="info-box-title">Redirecting Constructor</div>
      <p>Meneruskan pembuatan objek ke constructor lain dalam class yang sama.</p>
    </div>
  </div>

  <p>Contoh berikut menunjukkan <strong>Default Constructor</strong> dan <strong>Parameterized Constructor</strong> pada class <code>Mahasiswa</code>:</p>

  <div class="code-wrap">
    <div class="code-header">
      <div class="code-dots"><div class="dot r"></div><div class="dot y"></div><div class="dot g"></div></div>
      <div class="code-lang">dart</div>
    </div>
<pre><code><span class="cmt">// ── Default Constructor ──────────────────────────────</span>
<span class="kw">class</span> <span class="kw2">Mahasiswa</span> {
  <span class="kw2">String</span> nama = <span class="str">''</span>;
  <span class="kw2">int</span> umur = <span class="num">0</span>;

  <span class="cmt">// Default constructor</span>
  <span class="fn">Mahasiswa</span>() {
    nama = <span class="str">'Tidak Diketahui'</span>;
    umur = <span class="num">0</span>;
  }

  <span class="kw">void</span> <span class="fn">tampilkan</span>() {
    <span class="fn">print</span>(<span class="str">'Nama: <span class="var">$nama</span> | Umur: <span class="var">$umur</span>'</span>);
  }
}

<span class="cmt">// ── Parameterized Constructor ─────────────────────────</span>
<span class="kw">class</span> <span class="kw2">MahasiswaParam</span> {
  <span class="kw2">String</span> nama;
  <span class="kw2">int</span> umur;

  <span class="cmt">// Parameterized constructor - versi panjang</span>
  <span class="fn">MahasiswaParam</span>(<span class="kw2">String</span> nama, <span class="kw2">int</span> umur) {
    <span class="kw">this</span>.nama = nama;
    <span class="kw">this</span>.umur = umur;
  }

  <span class="cmt">// Shorthand syntax — lebih ringkas!</span>
  <span class="fn">MahasiswaParam</span>.shorthand(<span class="kw">this</span>.nama, <span class="kw">this</span>.umur);

  <span class="kw">void</span> <span class="fn">tampilkan</span>() {
    <span class="fn">print</span>(<span class="str">'Nama: <span class="var">$nama</span> | Umur: <span class="var">$umur</span>'</span>);
  }
}

<span class="kw">void</span> <span class="fn">main</span>() {
  <span class="kw">var</span> m1 = <span class="fn">Mahasiswa</span>();
  m1.<span class="fn">tampilkan</span>(); <span class="cmt">// Nama: Tidak Diketahui | Umur: 0</span>

  <span class="kw">var</span> m2 = <span class="fn">MahasiswaParam</span>(<span class="str">'Rifqi'</span>, <span class="num">21</span>);
  m2.<span class="fn">tampilkan</span>(); <span class="cmt">// Nama: Rifqi | Umur: 21</span>

  <span class="kw">var</span> m3 = MahasiswaParam.<span class="fn">shorthand</span>(<span class="str">'Prayoga'</span>, <span class="num">22</span>);
  m3.<span class="fn">tampilkan</span>(); <span class="cmt">// Nama: Prayoga | Umur: 22</span>
}</code></pre>
  </div>

  <div class="dartpad-section">
    <div class="dartpad-label">Coba Langsung di DartPad</div>
    <div class="dartpad-wrapper">
      <iframe src="https://dartpad.dev/embed-dart.html?id=7629966065b176fa840865cf9dedf583&theme=dark&run=true"></iframe>
    </div>
  </div>
</div>

<!-- ═══════════════ SECTION 2 ═══════════════ -->
<div class="section" id="s2">
  <div class="section-header">
    <div class="section-number">2</div>
    <div class="section-title-wrap">
      <h2>Constant Constructor</h2>
      <div class="section-subtitle">Membuat objek yang tidak dapat diubah (immutable)</div>
    </div>
  </div>

  <p>Constant constructor adalah constructor yang digunakan untuk membuat objek yang bersifat <strong>immutable</strong> — tidak dapat diubah setelah dibuat. Constructor ini ditandai dengan keyword <code>const</code>.</p>

  <div class="info-row">
    <div class="info-box blue">
      <div class="info-box-title">Syarat Utama</div>
      <p>Semua field dalam class harus bertipe <code>final</code> agar nilainya tidak bisa diubah.</p>
    </div>
    <div class="info-box green">
      <div class="info-box-title">Hemat Memori</div>
      <p>Objek dengan nilai yang sama hanya dibuat sekali — objeknya identik di memori.</p>
    </div>
    <div class="info-box teal">
      <div class="info-box-title">Compile-time Constant</div>
      <p>Nilai sudah diketahui saat proses kompilasi, membuat program lebih efisien.</p>
    </div>
  </div>

  <div class="note">
    <span class="note-icon">💡</span>
    <span>Gunakan <code>identical(t1, t2)</code> untuk membuktikan bahwa dua const object dengan nilai sama adalah objek yang <em>benar-benar sama</em> di memori (hasilnya <code>true</code>).</span>
  </div>

  <div class="code-wrap">
    <div class="code-header">
      <div class="code-dots"><div class="dot r"></div><div class="dot y"></div><div class="dot g"></div></div>
      <div class="code-lang">dart</div>
    </div>
<pre><code><span class="kw">class</span> <span class="kw2">TitikKoordinat</span> {
  <span class="kw">final</span> <span class="kw2">double</span> x;
  <span class="kw">final</span> <span class="kw2">double</span> y;

  <span class="cmt">// Constant constructor — keyword 'const'</span>
  <span class="kw">const</span> <span class="fn">TitikKoordinat</span>(<span class="kw">this</span>.x, <span class="kw">this</span>.y);
}

<span class="kw">class</span> <span class="kw2">WarnaRGB</span> {
  <span class="kw">final</span> <span class="kw2">int</span> merah;
  <span class="kw">final</span> <span class="kw2">int</span> hijau;
  <span class="kw">final</span> <span class="kw2">int</span> biru;

  <span class="kw">const</span> <span class="fn">WarnaRGB</span>(<span class="kw">this</span>.merah, <span class="kw">this</span>.hijau, <span class="kw">this</span>.biru);

  <span class="cmt">// Named constant constructor</span>
  <span class="kw">const</span> WarnaRGB.<span class="fn">merahPrimary</span>() : merah = <span class="num">255</span>, hijau = <span class="num">0</span>, biru = <span class="num">0</span>;
  <span class="kw">const</span> WarnaRGB.<span class="fn">hijauPrimary</span>() : merah = <span class="num">0</span>, hijau = <span class="num">255</span>, biru = <span class="num">0</span>;
}

<span class="kw">void</span> <span class="fn">main</span>() {
  <span class="cmt">// Menggunakan const saat membuat objek</span>
  <span class="kw">const</span> t1 = <span class="fn">TitikKoordinat</span>(<span class="num">3.0</span>, <span class="num">4.0</span>);
  <span class="kw">const</span> t2 = <span class="fn">TitikKoordinat</span>(<span class="num">3.0</span>, <span class="num">4.0</span>);

  <span class="fn">print</span>(<span class="fn">identical</span>(t1, t2)); <span class="cmt">// true — objek SAMA karena nilai sama!</span>

  <span class="kw">const</span> merah = WarnaRGB.<span class="fn">merahPrimary</span>();
  <span class="fn">print</span>(merah.merah); <span class="cmt">// 255</span>
  <span class="fn">print</span>(<span class="str">'RGB: <span class="var">${merah.merah}</span>, <span class="var">${merah.hijau}</span>, <span class="var">${merah.biru}</span>'</span>); <span class="cmt">// RGB: 255, 0, 0</span>
}</code></pre>
  </div>

  <div class="dartpad-section">
    <div class="dartpad-label">Coba Langsung di DartPad</div>
    <div class="dartpad-wrapper">
      <iframe src="https://dartpad.dev/embed-dart.html?id=152576be8476be7331e578dd8c531744&theme=dark&run=true"></iframe>
    </div>
  </div>
</div>

<!-- ═══════════════ SECTION 3 ═══════════════ -->
<div class="section" id="s3">
  <div class="section-header">
    <div class="section-number">3</div>
    <div class="section-title-wrap">
      <h2>Constructor dengan Initializer List</h2>
      <div class="section-subtitle">Inisialisasi field sebelum body constructor dijalankan</div>
    </div>
  </div>

  <p>Initializer list adalah fitur constructor yang digunakan untuk menginisialisasi nilai variabel <strong>sebelum body constructor dijalankan</strong>. Ditulis menggunakan tanda titik dua (<code>:</code>) setelah parameter constructor.</p>

  <div class="note">
    <span class="note-icon">⚡</span>
    <span>Initializer list berjalan <strong>SEBELUM</strong> body constructor. Ini satu-satunya cara untuk menginisialisasi field <code>final</code> yang nilainya perlu dihitung dari parameter.</span>
  </div>

  <div class="code-wrap">
    <div class="code-header">
      <div class="code-dots"><div class="dot r"></div><div class="dot y"></div><div class="dot g"></div></div>
      <div class="code-lang">dart</div>
    </div>
<pre><code><span class="kw">class</span> <span class="kw2">Segitiga</span> {
  <span class="kw">final</span> <span class="kw2">double</span> alas;
  <span class="kw">final</span> <span class="kw2">double</span> tinggi;
  <span class="kw">final</span> <span class="kw2">double</span> luas; <span class="cmt">// field dihitung saat inisialisasi</span>

  <span class="cmt">// Initializer List: menghitung luas sebelum body berjalan</span>
  <span class="fn">Segitiga</span>(<span class="kw">this</span>.alas, <span class="kw">this</span>.tinggi)
      : luas = <span class="num">0.5</span> * alas * tinggi {
    <span class="cmt">// Body constructor (opsional)</span>
    <span class="fn">print</span>(<span class="str">'Segitiga dibuat: alas=<span class="var">$alas</span>, tinggi=<span class="var">$tinggi</span>, luas=<span class="var">$luas</span>'</span>);
  }
}

<span class="kw">class</span> <span class="kw2">Lingkaran</span> {
  <span class="kw">final</span> <span class="kw2">double</span> jariJari;
  <span class="kw">final</span> <span class="kw2">double</span> keliling;
  <span class="kw">final</span> <span class="kw2">double</span> luasLingkaran;

  <span class="fn">Lingkaran</span>(<span class="kw">this</span>.jariJari)
      : keliling = <span class="num">2</span> * <span class="num">3.14159</span> * jariJari,
        luasLingkaran = <span class="num">3.14159</span> * jariJari * jariJari;
}

<span class="kw">void</span> <span class="fn">main</span>() {
  <span class="kw">var</span> s = <span class="fn">Segitiga</span>(<span class="num">6.0</span>, <span class="num">4.0</span>);
  <span class="fn">print</span>(s.luas);          <span class="cmt">// 12.0</span>

  <span class="kw">var</span> l = <span class="fn">Lingkaran</span>(<span class="num">7.0</span>);
  <span class="fn">print</span>(l.keliling);      <span class="cmt">// ≈ 43.98</span>
  <span class="fn">print</span>(l.luasLingkaran); <span class="cmt">// ≈ 153.94</span>
}</code></pre>
  </div>

  <div class="dartpad-section">
    <div class="dartpad-label">Coba Langsung di DartPad</div>
    <div class="dartpad-wrapper">
      <iframe src="https://dartpad.dev/embed-dart.html?id=ffa7118db48870df49a7b7db714dcdc5&theme=dark&run=true"></iframe>
    </div>
  </div>
</div>

<!-- ═══════════════ SECTION 4 ═══════════════ -->
<div class="section" id="s4">
  <div class="section-header">
    <div class="section-number">4</div>
    <div class="section-title-wrap">
      <h2>Pengantar Enkapsulasi</h2>
      <div class="section-subtitle">Menyembunyikan detail internal dari dunia luar</div>
    </div>
  </div>

  <p>Enkapsulasi adalah konsep OOP yang menyembunyikan detail implementasi internal sebuah class dan hanya mengekspos bagian yang diperlukan. Tujuannya adalah melindungi data dari perubahan yang tidak sah.</p>

  <div class="info-row">
    <div class="info-box blue">
      <div class="info-box-title">🛡 Keamanan Data</div>
      <p>Data tidak bisa diakses atau diubah sembarangan dari luar class.</p>
    </div>
    <div class="info-box teal">
      <div class="info-box-title">🎛 Kontrol Akses</div>
      <p>Hanya method yang diizinkan (getter/setter) yang bisa mengubah data.</p>
    </div>
    <div class="info-box green">
      <div class="info-box-title">🔧 Fleksibilitas</div>
      <p>Implementasi internal bisa diubah tanpa merusak kode yang menggunakan class tersebut.</p>
    </div>
    <div class="info-box orange">
      <div class="info-box-title">✅ Validasi</div>
      <p>Data dapat divalidasi terlebih dahulu sebelum disimpan melalui setter.</p>
    </div>
  </div>

  <div class="note">
    <span class="note-icon">⚡</span>
    <span>Dart tidak punya keyword <code>private</code> seperti Java/C++. Sebagai gantinya, Dart menggunakan <strong>underscore (_)</strong> di depan nama field/method untuk menandainya sebagai private. Akses dari luar class hanya boleh lewat getter dan setter.</span>
  </div>
</div>

<!-- ═══════════════ SECTION 5 ═══════════════ -->
<div class="section" id="s5">
  <div class="section-header">
    <div class="section-number">5</div>
    <div class="section-title-wrap">
      <h2>Public vs Private di Dart</h2>
      <div class="section-subtitle">Mengontrol akses terhadap data</div>
    </div>
  </div>

  <p>Dart tidak memiliki keyword <code>private</code> atau <code>public</code>. Akses dikontrol menggunakan prefix underscore (<code>_</code>) yang membuat member hanya dapat diakses di dalam file/library yang sama.</p>

  <div class="compare-table">
    <div class="compare-col pub">
      <h3>✅ PUBLIC</h3>
      <ul>
        <li>Tidak ada prefix khusus</li>
        <li>Dapat diakses dari mana saja</li>
        <li>Dari class lain, file lain, library lain</li>
        <li>Contoh: <code>nama</code>, <code>umur</code></li>
        <li>Contoh method: <code>tampilkan()</code></li>
      </ul>
    </div>
    <div class="compare-col priv">
      <h3>🔒 PRIVATE</h3>
      <ul>
        <li>Prefix underscore <code>_</code> sebelum nama</li>
        <li>Hanya bisa diakses dalam file yang sama</li>
        <li>Tidak bisa diakses dari file lain</li>
        <li>Contoh: <code>_nama</code>, <code>_password</code></li>
        <li>Contoh method: <code>_hitungInternal()</code></li>
      </ul>
    </div>
  </div>

  <div class="code-wrap">
    <div class="code-header">
      <div class="code-dots"><div class="dot r"></div><div class="dot y"></div><div class="dot g"></div></div>
      <div class="code-lang">dart</div>
    </div>
<pre><code><span class="kw">class</span> <span class="kw2">Contoh</span> {
  <span class="kw2">String</span> namaPubik = <span class="str">'visible'</span>;   <span class="cmt">// PUBLIC  — bisa diakses dari luar</span>
  <span class="kw2">String</span> _namaPrivate = <span class="str">'hidden'</span>; <span class="cmt">// PRIVATE — prefix _</span>
  <span class="kw2">int</span> _umur = <span class="num">20</span>;                 <span class="cmt">// PRIVATE</span>

  <span class="kw">void</span> <span class="fn">metodePubik</span>() {}           <span class="cmt">// PUBLIC method</span>
  <span class="kw">void</span> <span class="fn">_metodePrivate</span>() {}        <span class="cmt">// PRIVATE method</span>
}

<span class="kw">void</span> <span class="fn">main</span>() {
  <span class="kw">var</span> c = <span class="fn">Contoh</span>();
  <span class="fn">print</span>(c.namaPubik);    <span class="cmt">// ✅ OK — visible</span>
  c.<span class="fn">metodePubik</span>();      <span class="cmt">// ✅ OK</span>
  <span class="cmt">// print(c._namaPrivate); ❌ ERROR jika di file berbeda</span>
  <span class="cmt">// c._metodePrivate();    ❌ ERROR jika di file berbeda</span>
}</code></pre>
  </div>

  <div class="dartpad-section">
    <div class="dartpad-label">Coba Langsung di DartPad</div>
    <div class="dartpad-wrapper">
      <iframe src="https://dartpad.dev/embed-dart.html?id=d41141649bc26a073ed113d4431f5502&theme=dark&run=true"></iframe>
    </div>
  </div>
</div>

<!-- ═══════════════ SECTION 6 ═══════════════ -->
<div class="section" id="s6">
  <div class="section-header">
    <div class="section-number">6</div>
    <div class="section-title-wrap">
      <h2>Getter — Mengakses Data Private</h2>
      <div class="section-subtitle">Mengizinkan pembacaan field private secara terkontrol</div>
    </div>
  </div>

  <p>Getter adalah method khusus yang menggunakan keyword <code>get</code> untuk membaca nilai field private. Getter boleh berisi logika komputasi — tidak hanya mengembalikan field secara langsung.</p>

  <div class="tags">
    <span class="tag">Sintaks: TipeData get namaProperty => _field;</span>
    <span class="tag">Boleh berisi logika</span>
    <span class="tag">Tidak ada parameter</span>
  </div>

  <div class="code-wrap">
    <div class="code-header">
      <div class="code-dots"><div class="dot r"></div><div class="dot y"></div><div class="dot g"></div></div>
      <div class="code-lang">dart</div>
    </div>
<pre><code><span class="kw">class</span> <span class="kw2">Mahasiswa</span> {
  <span class="kw2">String</span> _nama;
  <span class="kw2">int</span> _nim;
  <span class="kw2">double</span> _nilaiAkhir;

  <span class="fn">Mahasiswa</span>(<span class="kw">this</span>._nama, <span class="kw">this</span>._nim, <span class="kw">this</span>._nilaiAkhir);

  <span class="cmt">// Simple getter — mengembalikan nilai field</span>
  <span class="kw2">String</span> <span class="kw">get</span> nama => _nama;
  <span class="kw2">int</span> <span class="kw">get</span> nim => _nim;

  <span class="cmt">// Computed getter — dengan logika</span>
  <span class="kw2">String</span> <span class="kw">get</span> grade {
    <span class="kw">if</span> (_nilaiAkhir >= <span class="num">90</span>) <span class="kw">return</span> <span class="str">'A'</span>;
    <span class="kw">if</span> (_nilaiAkhir >= <span class="num">80</span>) <span class="kw">return</span> <span class="str">'B'</span>;
    <span class="kw">if</span> (_nilaiAkhir >= <span class="num">70</span>) <span class="kw">return</span> <span class="str">'C'</span>;
    <span class="kw">return</span> <span class="str">'D'</span>;
  }

  <span class="kw2">String</span> <span class="kw">get</span> statusKelulusan =>
      _nilaiAkhir >= <span class="num">60</span> ? <span class="str">'LULUS'</span> : <span class="str">'TIDAK LULUS'</span>;

  <span class="cmt">// Getter dengan format khusus</span>
  <span class="kw2">String</span> <span class="kw">get</span> nimFormatted =>
      <span class="str">'NIM: <span class="var">${_nim.toString().padLeft(8, '0')}</span>'</span>;
}

<span class="kw">void</span> <span class="fn">main</span>() {
  <span class="kw">var</span> m = <span class="fn">Mahasiswa</span>(<span class="str">'Rifqi'</span>, <span class="num">251410005</span>, <span class="num">87.5</span>);

  <span class="fn">print</span>(m.nama);            <span class="cmt">// Rifqi</span>
  <span class="fn">print</span>(m.grade);           <span class="cmt">// B</span>
  <span class="fn">print</span>(m.statusKelulusan); <span class="cmt">// LULUS</span>
  <span class="fn">print</span>(m.nimFormatted);    <span class="cmt">// NIM: 51410005</span>
}</code></pre>
  </div>

  <div class="dartpad-section">
    <div class="dartpad-label">Coba Langsung di DartPad</div>
    <div class="dartpad-wrapper">
      <iframe src="https://dartpad.dev/embed-dart.html?id=f0d1674cdbd76664748a499d094277f4&theme=dark&run=true"></iframe>
    </div>
  </div>
</div>

<!-- ═══════════════ SECTION 7 ═══════════════ -->
<div class="section" id="s7">
  <div class="section-header">
    <div class="section-number">7</div>
    <div class="section-title-wrap">
      <h2>Setter — Memodifikasi Data Private</h2>
      <div class="section-subtitle">Mengizinkan perubahan data dengan validasi</div>
    </div>
  </div>

  <p>Setter menggunakan keyword <code>set</code> dan memungkinkan validasi data sebelum disimpan. Setter <strong>tidak memiliki return value</strong>. Gunakan <code>throw Exception()</code> untuk menolak nilai yang tidak valid.</p>

  <div class="tags">
    <span class="tag">Sintaks: set namaProperty(TipeData val) { ... }</span>
    <span class="tag">Tidak ada return value</span>
    <span class="tag">Validasi sebelum simpan</span>
  </div>

  <div class="code-wrap">
    <div class="code-header">
      <div class="code-dots"><div class="dot r"></div><div class="dot y"></div><div class="dot g"></div></div>
      <div class="code-lang">dart</div>
    </div>
<pre><code><span class="kw">class</span> <span class="kw2">User</span> {
  <span class="kw2">String</span> _username;
  <span class="kw2">String</span> _password;
  <span class="kw2">String</span> _email;

  <span class="fn">User</span>(<span class="kw">this</span>._username, <span class="kw">this</span>._password, <span class="kw">this</span>._email);

  <span class="cmt">// Getters</span>
  <span class="kw2">String</span> <span class="kw">get</span> username => _username;
  <span class="kw2">String</span> <span class="kw">get</span> email => _email;

  <span class="cmt">// Setter username — minimal 5 karakter</span>
  <span class="kw">set</span> <span class="fn">username</span>(<span class="kw2">String</span> val) {
    <span class="kw">if</span> (val.length < <span class="num">5</span>) {
      <span class="kw">throw</span> <span class="fn">Exception</span>(<span class="str">'Username minimal 5 karakter!'</span>);
    }
    _username = val;
  }

  <span class="cmt">// Setter password — minimal 8 karakter</span>
  <span class="kw">set</span> <span class="fn">password</span>(<span class="kw2">String</span> val) {
    <span class="kw">if</span> (val.length < <span class="num">8</span>) {
      <span class="kw">throw</span> <span class="fn">Exception</span>(<span class="str">'Password minimal 8 karakter!'</span>);
    }
    _password = val;
  }

  <span class="cmt">// Setter email — harus mengandung '@'</span>
  <span class="kw">set</span> <span class="fn">email</span>(<span class="kw2">String</span> val) {
    <span class="kw">if</span> (!val.<span class="fn">contains</span>(<span class="str">'@'</span>)) {
      <span class="kw">throw</span> <span class="fn">Exception</span>(<span class="str">'Email harus mengandung "@"!'</span>);
    }
    _email = val;
  }
}

<span class="kw">void</span> <span class="fn">main</span>() {
  <span class="kw">var</span> user = <span class="fn">User</span>(<span class="str">'rifqi1'</span>, <span class="str">'password1'</span>, <span class="str">'rifqi@mail.com'</span>);

  user.username = <span class="str">'prayoga'</span>;  <span class="cmt">// ✅ OK</span>
  user.email = <span class="str">'baru@gmail.com'</span>; <span class="cmt">// ✅ OK</span>

  <span class="kw">try</span> {
    user.username = <span class="str">'rif'</span>;    <span class="cmt">// ❌ Exception: min 5 karakter</span>
  } <span class="kw">catch</span> (e) { <span class="fn">print</span>(e); }

  <span class="kw">try</span> {
    user.email = <span class="str">'tidakvalid'</span>; <span class="cmt">// ❌ Exception: tidak ada '@'</span>
  } <span class="kw">catch</span> (e) { <span class="fn">print</span>(e); }
}</code></pre>
  </div>

  <div class="dartpad-section">
    <div class="dartpad-label">Coba Langsung di DartPad</div>
    <div class="dartpad-wrapper">
      <iframe src="https://dartpad.dev/embed-dart.html?id=48f63a4092f9c135ce0290691b08eedd&theme=dark&run=true"></iframe>
    </div>
  </div>
</div>

<!-- ═══════════════ SECTION 8 ═══════════════ -->
<div class="section" id="s8">
  <div class="section-header">
    <div class="section-number">8</div>
    <div class="section-title-wrap">
      <h2>Multiple Constructor (Latihan)</h2>
      <div class="section-subtitle">Named constructor — berbagai cara membuat objek</div>
    </div>
  </div>

  <p>Multiple constructor memungkinkan sebuah class memiliki lebih dari satu constructor. Di Dart, ini dilakukan dengan <strong>named constructor</strong>. Setiap constructor bisa memiliki logika inisialisasi yang berbeda.</p>

  <div class="code-wrap">
    <div class="code-header">
      <div class="code-dots"><div class="dot r"></div><div class="dot y"></div><div class="dot g"></div></div>
      <div class="code-lang">dart</div>
    </div>
<pre><code><span class="kw">class</span> <span class="kw2">Mahasiswa</span> {
  <span class="kw2">String</span> nama;
  <span class="kw2">int</span> nim;
  <span class="kw2">double</span> ipk;

  <span class="cmt">// Constructor default</span>
  <span class="fn">Mahasiswa</span>()
      : nama = <span class="str">'Tidak Diketahui'</span>,
        nim = <span class="num">0</span>,
        ipk = <span class="num">0.0</span>;

  <span class="cmt">// Named constructor — dari Map</span>
  Mahasiswa.<span class="fn">dariMap</span>(<span class="kw2">Map</span>&lt;<span class="kw2">String</span>, <span class="kw">dynamic</span>&gt; data)
      : nama = data[<span class="str">'nama'</span>] ?? <span class="str">'Tidak Diketahui'</span>,
        nim  = data[<span class="str">'nim'</span>]  ?? <span class="num">0</span>,
        ipk  = (data[<span class="str">'ipk'</span>] ?? <span class="num">0.0</span>).<span class="fn">toDouble</span>();

  <span class="cmt">// Named constructor — tanpa nama</span>
  Mahasiswa.<span class="fn">tanpaNama</span>(<span class="kw">this</span>.nim, <span class="kw">this</span>.ipk) : nama = <span class="str">'Anonim'</span>;

  <span class="kw">void</span> <span class="fn">tampilkan</span>() {
    <span class="fn">print</span>(<span class="str">'Nama: <span class="var">$nama</span> | NIM: <span class="var">$nim</span> | IPK: <span class="var">$ipk</span>'</span>);
  }
}

<span class="kw">void</span> <span class="fn">main</span>() {
  <span class="kw">var</span> m1 = <span class="fn">Mahasiswa</span>();
  <span class="kw">var</span> m2 = Mahasiswa.<span class="fn">dariMap</span>({<span class="str">'nama'</span>: <span class="str">'Rifqi'</span>, <span class="str">'nim'</span>: <span class="num">251410005</span>, <span class="str">'ipk'</span>: <span class="num">3.75</span>});
  <span class="kw">var</span> m3 = Mahasiswa.<span class="fn">tanpaNama</span>(<span class="num">67890</span>, <span class="num">3.20</span>);

  m1.<span class="fn">tampilkan</span>(); <span class="cmt">// Nama: Tidak Diketahui | NIM: 0 | IPK: 0.0</span>
  m2.<span class="fn">tampilkan</span>(); <span class="cmt">// Nama: Rifqi | NIM: 251410005 | IPK: 3.75</span>
  m3.<span class="fn">tampilkan</span>(); <span class="cmt">// Nama: Anonim | NIM: 67890 | IPK: 3.2</span>
}</code></pre>
  </div>

  <div class="dartpad-section">
    <div class="dartpad-label">Coba Langsung di DartPad</div>
    <div class="dartpad-wrapper">
      <iframe src="https://dartpad.dev/embed-dart.html?id=5c6689fa64c5ded301dc064430aa0954&theme=dark&run=true"></iframe>
    </div>
  </div>
</div>

<!-- ═══════════════ SECTION 9 ═══════════════ -->
<div class="section" id="s9">
  <div class="section-header">
    <div class="section-number">9</div>
    <div class="section-title-wrap">
      <h2>Sistem Login Sederhana (Studi Kasus)</h2>
      <div class="section-subtitle">Enkapsulasi dalam skenario nyata</div>
    </div>
  </div>

  <p>Contoh kasus berikut menunjukkan bagaimana enkapsulasi diterapkan dalam sistem login. Data sensitif seperti username dan password disimpan sebagai field <strong>private</strong> dan hanya bisa diakses melalui method yang telah ditentukan.</p>

  <div class="code-wrap">
    <div class="code-header">
      <div class="code-dots"><div class="dot r"></div><div class="dot y"></div><div class="dot g"></div></div>
      <div class="code-lang">dart</div>
    </div>
<pre><code><span class="kw">class</span> <span class="kw2">AkunPengguna</span> {
  <span class="kw2">String</span> _username;
  <span class="kw2">String</span> _password;
  <span class="kw2">bool</span> _isLoggedIn = <span class="kw">false</span>;
  <span class="kw2">int</span> _loginAttempts = <span class="num">0</span>;
  <span class="kw">static</span> <span class="kw">const</span> <span class="kw2">int</span> _maxAttempts = <span class="num">3</span>;

  <span class="fn">AkunPengguna</span>(<span class="kw">this</span>._username, <span class="kw">this</span>._password);

  <span class="cmt">// Getters</span>
  <span class="kw2">String</span> <span class="kw">get</span> username => _username;
  <span class="kw2">bool</span> <span class="kw">get</span> isLoggedIn => _isLoggedIn;
  <span class="kw2">bool</span> <span class="kw">get</span> isLocked => _loginAttempts >= _maxAttempts;
  <span class="kw2">String</span> <span class="kw">get</span> status => _isLoggedIn ? <span class="str">'🟢 Online'</span> : <span class="str">'🔴 Offline'</span>;

  <span class="cmt">// Setter password dengan validasi</span>
  <span class="kw">set</span> <span class="fn">password</span>(<span class="kw2">String</span> newPass) {
    <span class="kw">if</span> (newPass.length < <span class="num">8</span>) {
      <span class="kw">throw</span> <span class="fn">Exception</span>(<span class="str">'Password minimal 8 karakter!'</span>);
    }
    _password = newPass;
    <span class="fn">print</span>(<span class="str">'Password berhasil diubah.'</span>);
  }

  <span class="cmt">// Method login</span>
  <span class="kw2">bool</span> <span class="fn">login</span>(<span class="kw2">String</span> user, <span class="kw2">String</span> pass) {
    <span class="kw">if</span> (isLocked) {
      <span class="fn">print</span>(<span class="str">'Akun terkunci! Terlalu banyak percobaan.'</span>);
      <span class="kw">return</span> <span class="kw">false</span>;
    }
    <span class="kw">if</span> (_username == user && _password == pass) {
      _isLoggedIn = <span class="kw">true</span>;
      _loginAttempts = <span class="num">0</span>;
      <span class="fn">print</span>(<span class="str">'Login berhasil! Selamat datang, <span class="var">$_username</span>'</span>);
      <span class="kw">return</span> <span class="kw">true</span>;
    }
    _loginAttempts++;
    <span class="fn">print</span>(<span class="str">'Login gagal! Sisa percobaan: <span class="var">${_maxAttempts - _loginAttempts}</span>'</span>);
    <span class="kw">return</span> <span class="kw">false</span>;
  }

  <span class="kw">void</span> <span class="fn">logout</span>() {
    _isLoggedIn = <span class="kw">false</span>;
    <span class="fn">print</span>(<span class="str">'Logout berhasil. Sampai jumpa, <span class="var">$_username</span>!'</span>);
  }
}

<span class="kw">void</span> <span class="fn">main</span>() {
  <span class="kw">var</span> akun = <span class="fn">AkunPengguna</span>(<span class="str">'rifqi_dev'</span>, <span class="str">'dart1234'</span>);
  <span class="fn">print</span>(akun.status);                      <span class="cmt">// 🔴 Offline</span>

  akun.<span class="fn">login</span>(<span class="str">'rifqi_dev'</span>, <span class="str">'salah'</span>);        <span class="cmt">// Login gagal! (sisa: 2)</span>
  akun.<span class="fn">login</span>(<span class="str">'rifqi_dev'</span>, <span class="str">'dart1234'</span>);    <span class="cmt">// Login berhasil!</span>
  <span class="fn">print</span>(akun.status);                      <span class="cmt">// 🟢 Online</span>

  akun.password = <span class="str">'newpass99'</span>;            <span class="cmt">// Password berhasil diubah</span>
  akun.<span class="fn">logout</span>();                           <span class="cmt">// Logout berhasil</span>
}</code></pre>
  </div>

  <div class="dartpad-section">
    <div class="dartpad-label">Coba Langsung di DartPad</div>
    <div class="dartpad-wrapper">
      <iframe src="https://dartpad.dev/embed-dart.html?id=9875dce55db6c46b440b252c5bcabe8a&theme=dark&run=true"></iframe>
    </div>
  </div>
</div>

<!-- ═══════════════ FOOTER ═══════════════ -->
<footer>
  <p>© 2026 Resume Dart OOP Sesi 3 · <strong>Rifqi Prayoga</strong> · SI2A · 251410005</p>
</footer>

</div>
</body>
</html>
