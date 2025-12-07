/shopee-express
   ├── index.html<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Shopee Express - Home</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<nav>
    <div class="logo">Shopee Express</div>
    <ul>
        <li><a href="index.html">Beranda</a></li>
        <li><a href="layanan.html">Layanan</a></li>
        <li><a href="cek-resi.html">Cek Resi</a></li>
    </ul>
</nav>

<div class="container">
    <h2>Selamat Datang di Shopee Express</h2>
    <p>Layanan pengiriman cepat, aman, dan terpercaya.</p><br>

    <a href="cek-resi.html">
        <button>Cek Resi Sekarang</button>
    </a>
</div>

<footer>
    © 2025 Shopee Express (Versi Tiruan)
</footer>

</body>
</html>

   ├── layanan.html<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Layanan - Shopee Express</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<nav>
    <div class="logo">Shopee Express</div>
    <ul>
        <li><a href="index.html">Beranda</a></li>
        <li><a href="layanan.html">Layanan</a></li>
        <li><a href="cek-resi.html">Cek Resi</a></li>
    </ul>
</nav>

<div class="container">
    <h2>Layanan Pengiriman</h2><br>

    <ul>
        <li>Shopee Express Standard</li>
        <li>Shopee Express Hemat</li>
        <li>Shopee Express Same Day</li>
        <li>Shopee Express Instant</li>
    </ul>
</div>

<footer>
    © 2025 Shopee Express (Versi Tiruan)
</footer>

</body>
</html>

   ├── cek-resi.htmlfunction cekResi() {
    let resi = document.getElementById("resiInput").value;
    let hasil = document.getElementById("hasilResi");

    if (resi === "") {
        hasil.style.display = "block";
        hasil.innerHTML = "<strong>Masukkan nomor resi terlebih dahulu.</strong>";
        return;
    }

    hasil.style.display = "block";
    hasil.innerHTML = `
        <h3>Hasil Pelacakan</h3>
        <p><strong>Nomor Resi:</strong> ${resi}</p>
        <p><strong>Status:</strong> Paket sedang dalam perjalanan</p>
        <p><strong>Lokasi Terakhir:</strong> Gudang Transit Jakarta</p>
        <p><strong>Estimasi Sampai:</strong> 2 - 3 hari</p>
    `;
}

   ├── style.css /* RESET */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* BODY */
body {
    font-family: Arial, sans-serif;
    background: #f5f5f5;
}

/* NAVBAR */
nav {
    width: 100%;
    background: #ff5722;
    padding: 15px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

nav .logo {
    color: white;
    font-size: 22px;
    font-weight: bold;
}

nav ul {
    list-style: none;
    display: flex;
    gap: 20px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    font-size: 16px;
}

nav ul li a:hover {
    text-decoration: underline;
}

/* CONTAINER */
.container {
    width: 90%;
    max-width: 900px;
    margin: 50px auto;
    background: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

/* BUTTON */
button {
    padding: 12px;
    width: 100%;
    background: #ff5722;
    border: none;
    color: white;
    font-size: 18px;
    border-radius: 8px;
    cursor: pointer;
}

button:hover {
    background: #e64a19;
}

/* INPUT */
input {
    width: 100%;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 8px;
    margin: 10px 0;
    font-size: 16px;
}

/* FOOTER */
footer {
    text-align: center;
    padding: 20px;
    margin-top: 40px;
    background: #ff5722;
    color: white;
}

   └── script.js<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Cek Resi - Shopee Express</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<nav>
    <div class="logo">Shopee Express</div>
    <ul>
        <li><a href="index.html">Beranda</a></li>
        <li><a href="layanan.html">Layanan</a></li>
        <li><a href="cek-resi.html">Cek Resi</a></li>
    </ul>
</nav>

<div class="container">
    <h2>Cek Resi Pengiriman</h2>
    <input type="text" id="resiInput" placeholder="Masukkan nomor resi">
    <button onclick="cekResi()">Cek Resi</button>

    <div id="hasilResi" style="display:none; margin-top:20px; background:#fff3e0; padding:15px; border-radius:8px;"></div>
</div>

<footer>
    © 2025 Shopee Express (Versi Tiruan)
</footer>

<script src="script.js"></script>
</body>
</html>

