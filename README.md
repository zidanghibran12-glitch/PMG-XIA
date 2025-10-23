
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" lang="id">
<head>
  <meta charset="UTF-8" />
  <meta content="width=device-width, initial-scale=1.0" name="viewport" />
  <title>Toplezz</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      background-color: #f8c77d;
      color: #444;
    }

    header {
      background: linear-gradient(90deg, #f08b18ce, #ffc08dde);
      color: rgb(255, 255, 255);
      padding: 2rem 1rem;
      text-align: center;
      border-bottom-left-radius: 20px;
      border-bottom-right-radius: 20px;
    }

    header h1 {
      margin: 0;
      font-size: 2rem;
      animation: float 3s ease-in-out infinite;
    }

    header p {
      margin-top: 5px;
      font-size: 1.1rem;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-5px); }
    }

    nav {
      background: linear-gradient(90deg, #f08b18d7, #ffc08dde);
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 10px;
      padding: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    nav a {
      color: #e9a91e;
      text-decoration: none;
      font-weight: 600;
      background: white;
      padding: 8px 15px;
      border-radius: 25px;
      transition: 0.3s;
    }

    nav a:hover {
      background: #f39658;
      color: white;
    }

    .section {
      display: none;
      padding: 2rem 1rem;
      text-align: center;
    }

    .active {
      display: block;
    }

    /* Dashboard */
    .dashboard-box {
      background: white;
      border-radius: 20px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      padding: 2rem;
      max-width: 700px;
      margin: 2rem auto;
    }

    .dashboard-box h2 {
      color: #e96f1e;
      font-size: 1.8rem;
    }

    .dashboard-box p {
      font-size: 1.1rem;
      margin: 10px 0;
      animation: float 3s ease-in-out infinite;
    }

    .features {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 15px;
      margin-top: 1.5rem;
    }

    .feature {
      background: #fff6f0;
      border-radius: 15px;
      width: 160px;
      padding: 1rem;
      transition: 0.3s;
      box-shadow: 0 3px 8px rgba(0,0,0,0.1);
    }

    .feature:hover {
      transform: translateY(-5px);
      background: #ff9a47;
    }

    .start-btn {
      background: #e95e1e;
      color: white;
      border: none;
      padding: 12px 25px;
      border-radius: 25px;
      cursor: pointer;
      font-weight: bold;
      transition: 0.3s;
      margin-top: 15px;
    }

    .start-btn:hover {
      background: #c25618;
      transform: scale(1.05);
    }

    /* Menu */
    .menu-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      margin-top: 2rem;
    }

    .card {
      background: white;
      border-radius: 15px;
      width: 220px;
      padding: 1rem;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .card img {
      width: 100%;
      border-radius: 10px;
      animation: float 3s ease-in-out infinite;
    }

    .price {
      color: #e96f1e;
      font-weight: bold;

    }

    .card button {
      background: #e78f5c;
      color: rgb(255, 255, 255);
      border: none;
      padding: 8px 15px;
      border-radius: 20px;
      cursor: pointer;
      font-weight: 600;
      margin-top: 10px;
      transition: 0.3s;
  
    }

    .card button:hover {
      background: #ff986f;
    }

    /* Form */
    form {
      display: flex;
      flex-direction: column;
      max-width: 400px;
      margin: 2rem auto;
      background: white;
      padding: 2rem;
      border-radius: 20px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }

    form label {
      margin-bottom: 5px;
      text-align: left;
      color: #e9691e;
      font-weight: 600;
    }

    form input, form select, form textarea {
      padding: 10px;
      margin-bottom: 15px;
      border-radius: 10px;
      border: 1px solid #fa9256;
      font-size: 1rem;
    }

    form button {
      background: #e9691e;
      color: white;
      border: none;
      padding: 10px;
      border-radius: 20px;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
    }

    form button:hover {
      background: #c26518;
    }

    /* Struk */
    .receipt {
      background: white;
      border-radius: 15px;
      padding: 1.5rem;
      margin: 1rem auto;
      max-width: 500px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      text-align: left;
    }

    .receipt h3 {
      color: #e9691e;
      border-bottom: 1px dashed #ca8a5f;
      padding-bottom: 5px;
    }

    footer {
      text-align: center;
      background: linear-gradient(90deg, #df9d53, #e29f52);
      color: white;
      padding: 1rem;
      margin-top: 40px;
      border-top-left-radius: 20px;
      border-top-right-radius: 20px;
      font-size: 0.9rem;
    }
  </style>
</head>

<body>
  <header>
    <h1>Toplezz</h1>
    <p>Tempat buat cari Toples</p>
  </header>

  <nav>
    <a href="#" onclick="showSection('dashboard')">Dashboard</a>
    <a href="#" onclick="showSection('menu')">Menu</a>
    <a href="#" onclick="showSection('orderForm')">Order</a>
    <a href="#" onclick="showSection('orders')">Pesanan</a>
  </nav>

  <!-- Dashboard -->
  <div id="dashboard" class="section active">
    <div class="dashboard-box">
      <h2>Selamat Datang di Toplezz</h2>
      <p>Udah nentuin mau pesen berapa?</p>
      <div class="features">
        <div class="feature"><p>Lihat daftar menu</p></div>
        <div class="feature"><p>Pilih toplesmu</p></div>
        <div class="feature"><p>Isi form pemesanan</p></div>
        <div class="feature"><p>Lihat struk & pesanan</p></div>
      </div>
      <button class="start-btn" onclick="showSection('menu')">Pesan Sekarang</button>
    </div>
  </div>

  <!-- Menu -->
  <div id="menu" class="section">
    <h2>Daftar Menu Toples</h2>
    <div class="menu-container">

      <div class="card">
        <img src="images/Toples Polosan.PNG" alt="Toples">
        <h3>Toples</h3>
        <p class="price">Rp5.000</p>
        <button onclick="selectMenu('Toples',5000)">Order</button>
      </div>

      <div class="card">
        <img src="images/Toples Celengan.PNG" alt="Celengan">
        <h3>Celengan</h3>
        <p class="price">Rp12.000</p>
        <button onclick="selectMenu('Celengan',12000)">Order</button>
      </div>

      <div class="card">
        <img src="images/Toples Tanaman.PNG" alt="Tanaman">
        <h3>Pot Tanaman</h3>
        <p class="price">Rp10.000</p>
        <button onclick="selectMenu('Pot Tanaman',10000)">Order</button>
      </div>
      </div>
      </div>

  <!-- Order Form -->
  <div id="orderForm" class="section">
    <h2>Form Pemesanan</h2>
    <form id="formPesanan" onsubmit="prosesPesanan(event)">
      <label>Nama Pemesan:</label>
      <input type="text" id="nama" placeholder="Masukkan nama Anda" required>

      <label>Menu Pilihan:</label>
      <input type="text" id="menuDipilih" readonly required>

      <label>Jumlah:</label>
      <input type="number" id="jumlah" min="1" required>

      <label>Catatan Tambahan:</label>
      <textarea id="catatan" rows="3" placeholder="Contoh: tanpa topping kacang"></textarea>

      <button type="submit">Kirim Pesanan</button>
    </form>
  </div>

  <!-- Pesanan / Struk -->
  <div id="orders" class="section">
    <h2>Struk Pemesanan</h2>
    <div class="receipt" id="receipt" style="display:none;"></div>
    <button class="start-btn" onclick="window.print()" id="printBtn" style="display:none;">Cetak Struk</button>
  </div>

  <footer>
    <p>© 2025 Toplezz — Cari Toples disini aja!</p>
  </footer>

  <script>
    function showSection(sectionId) {
      document.querySelectorAll('.section').forEach(sec => sec.classList.remove('active'));
      document.getElementById(sectionId).classList.add('active');
    }

    let selectedMenu = '';
    let selectedPrice = 0;

    function selectMenu(menu, harga) {
      selectedMenu = menu;
      selectedPrice = harga;
      document.getElementById('menuDipilih').value = menu;
      showSection('orderForm');
    }

    function prosesPesanan(event) {
      event.preventDefault();

      const nama = document.getElementById('nama').value;
      const menu = selectedMenu || document.getElementById('menuDipilih').value;
      const jumlah = parseInt(document.getElementById('jumlah').value);
      const catatan = document.getElementById('catatan').value || '-';
      const total = selectedPrice * jumlah;

      const receiptHTML = `
        <h3>Rincian Pesanan</h3>
        <p><strong>Nama:</strong> ${nama}</p>
        <p><strong>Menu:</strong> ${menu}</p>
        <p><strong>Jumlah:</strong> ${jumlah}</p>
        <p><strong>Catatan:</strong> ${catatan}</p>
        <hr>
        <h3>Total: Rp ${total.toLocaleString('id-ID')}</h3>
      `;

      document.getElementById('receipt').innerHTML = receiptHTML;
      document.getElementById('receipt').style.display = 'block';
      document.getElementById('printBtn').style.display = 'inline-block';
      showSection('orders');
    }
  </script>
</body>
</html>
