
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">

  :root {
    --green: #3B6D11;
    --green-light: #EAF3DE;
    --green-mid: #639922;
    --pink: #D4537E;
    --pink-light: #FBEAF0;
    --pink-mid: #ED93B1;
    --cream: #FDFAF5;
    --dark: #2C2A22;
    --muted: #888780;
    --border: rgba(0,0,0,0.1);
    --white: #ffffff;
    --shadow: 0 4px 24px rgba(0,0,0,0.08);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--dark);
    min-height: 100vh;
  }

  /* HERO */
  .hero {
    background: linear-gradient(135deg, #3B6D11 0%, #639922 40%, #D4537E 100%);
    padding: 0;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 320px; height: 320px;
    border-radius: 50%;
    background: rgba(255,255,255,0.07);
  }
  .hero::after {
    content: '';
    position: absolute;
    bottom: -60px; left: -60px;
    width: 240px; height: 240px;
    border-radius: 50%;
    background: rgba(255,255,255,0.05);
  }
  .nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 2rem;
    position: relative; z-index: 2;
  }
  .logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.8rem;
    font-weight: 700;
    color: white;
    letter-spacing: 2px;
  }
  .logo span {
    display: block;
    font-size: 0.65rem;
    font-family: 'DM Sans', sans-serif;
    font-weight: 300;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: rgba(255,255,255,0.8);
    margin-top: -4px;
  }
  .nav-badge {
    background: rgba(255,255,255,0.15);
    border: 1px solid rgba(255,255,255,0.3);
    color: white;
    padding: 6px 16px;
    border-radius: 50px;
    font-size: 0.78rem;
    font-weight: 500;
    backdrop-filter: blur(8px);
  }
  .hero-body {
    padding: 2rem 2rem 3.5rem;
    position: relative; z-index: 2;
  }
  .hero-body h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 5vw, 3.2rem);
    font-weight: 700;
    color: white;
    line-height: 1.15;
    margin-bottom: 1rem;
    max-width: 600px;
  }
  .hero-body h1 em {
    font-style: italic;
    color: rgba(255,255,255,0.85);
  }
  .hero-body p {
    color: rgba(255,255,255,0.85);
    font-size: 0.95rem;
    line-height: 1.7;
    max-width: 520px;
    margin-bottom: 1.5rem;
  }
  .badges-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }
  .badge {
    background: rgba(255,255,255,0.18);
    border: 1px solid rgba(255,255,255,0.3);
    color: white;
    padding: 5px 14px;
    border-radius: 50px;
    font-size: 0.78rem;
    font-weight: 400;
    display: flex;
    align-items: center;
    gap: 5px;
    backdrop-filter: blur(4px);
  }
  .badge-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: #C0DD97;
    flex-shrink: 0;
  }

  /* PROMO STRIP */
  .promo-strip {
    background: var(--pink);
    color: white;
    padding: 10px 2rem;
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    justify-content: center;
    align-items: center;
    font-size: 0.82rem;
    font-weight: 500;
  }
  .promo-strip span {
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .promo-strip strong { font-weight: 600; }

  /* MAIN CONTENT */
  .main { max-width: 900px; margin: 0 auto; padding: 2rem 1.5rem; }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    font-weight: 600;
    color: var(--dark);
    margin-bottom: 0.3rem;
  }
  .section-sub {
    font-size: 0.85rem;
    color: var(--muted);
    margin-bottom: 1.5rem;
  }

  /* PRODUCTS */
  .products-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    gap: 1rem;
    margin-bottom: 2.5rem;
  }
  .product-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 16px;
    overflow: hidden;
    transition: transform 0.2s, box-shadow 0.2s;
    cursor: pointer;
    position: relative;
  }
  .product-card:hover { transform: translateY(-3px); box-shadow: var(--shadow); }
  .product-card.selected {
    border: 2px solid var(--green-mid);
    box-shadow: 0 0 0 3px rgba(99,153,34,0.15);
  }
  .product-thumb {
    height: 130px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 3.5rem;
    position: relative;
  }
  .product-thumb.green-bg { background: linear-gradient(135deg, #EAF3DE, #C0DD97); }
  .product-thumb.pink-bg  { background: linear-gradient(135deg, #FBEAF0, #F4C0D1); }
  .check-badge {
    position: absolute;
    top: 8px; right: 8px;
    width: 26px; height: 26px;
    border-radius: 50%;
    background: var(--green-mid);
    display: none;
    align-items: center;
    justify-content: center;
    color: white;
    font-size: 13px;
  }
  .product-card.selected .check-badge { display: flex; }
  .product-info { padding: 12px 14px 14px; }
  .product-name {
    font-family: 'Playfair Display', serif;
    font-size: 1rem;
    font-weight: 600;
    color: var(--dark);
    margin-bottom: 2px;
  }
  .product-desc {
    font-size: 0.75rem;
    color: var(--muted);
    margin-bottom: 8px;
    line-height: 1.5;
  }
  .product-price-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .product-price {
    font-size: 1rem;
    font-weight: 600;
    color: var(--green);
  }
  .product-unit { font-size: 0.72rem; color: var(--muted); }

  /* QTY */
  .qty-control {
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .qty-btn {
    width: 26px; height: 26px;
    border-radius: 50%;
    border: 1px solid var(--border);
    background: var(--cream);
    color: var(--dark);
    cursor: pointer;
    font-size: 1rem;
    display: flex; align-items: center; justify-content: center;
    transition: background 0.15s;
  }
  .qty-btn:hover { background: var(--green-light); }
  .qty-num {
    font-size: 0.9rem;
    font-weight: 600;
    min-width: 20px;
    text-align: center;
    color: var(--dark);
  }

  /* ORDER FORM */
  .order-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 1.5rem;
    margin-bottom: 1.5rem;
  }
  .order-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 600;
    margin-bottom: 1rem;
    color: var(--dark);
  }

  label {
    display: block;
    font-size: 0.8rem;
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 5px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }
  input[type="text"], select {
    width: 100%;
    padding: 10px 14px;
    border: 1px solid var(--border);
    border-radius: 10px;
    font-family: 'DM Sans', sans-serif;
    font-size: 0.9rem;
    color: var(--dark);
    background: var(--cream);
    outline: none;
    transition: border 0.2s;
    margin-bottom: 14px;
    -webkit-appearance: none;
  }
  input[type="text"]:focus, select:focus { border-color: var(--green-mid); background: white; }

  /* PAYMENT METHODS */
  .pay-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 8px;
    margin-bottom: 14px;
  }
  .pay-option {
    border: 1.5px solid var(--border);
    border-radius: 10px;
    padding: 10px 12px;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 8px;
    transition: all 0.2s;
    background: var(--cream);
  }
  .pay-option:hover { border-color: var(--green-mid); background: var(--green-light); }
  .pay-option.selected { border-color: var(--green-mid); background: var(--green-light); }
  .pay-option .pay-icon { font-size: 1.2rem; }
  .pay-option .pay-label { font-size: 0.82rem; font-weight: 500; color: var(--dark); }
  .pay-option.selected .pay-label { color: var(--green); }

  /* PROMO RADIO */
  .promo-opts { display: flex; flex-direction: column; gap: 8px; margin-bottom: 14px; }
  .promo-opt {
    border: 1.5px solid var(--border);
    border-radius: 10px;
    padding: 10px 14px;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 10px;
    background: var(--cream);
    transition: all 0.2s;
  }
  .promo-opt:hover { border-color: var(--pink); background: var(--pink-light); }
  .promo-opt.selected { border-color: var(--pink); background: var(--pink-light); }
  .promo-radio {
    width: 16px; height: 16px;
    border-radius: 50%;
    border: 2px solid var(--border);
    background: white;
    flex-shrink: 0;
    display: flex; align-items: center; justify-content: center;
  }
  .promo-opt.selected .promo-radio { border-color: var(--pink); }
  .promo-dot {
    width: 8px; height: 8px;
    border-radius: 50%;
    background: var(--pink);
    display: none;
  }
  .promo-opt.selected .promo-dot { display: block; }
  .promo-text { font-size: 0.82rem; font-weight: 500; color: var(--dark); flex: 1; }
  .promo-tag {
    font-size: 0.72rem;
    font-weight: 600;
    padding: 2px 8px;
    border-radius: 50px;
    background: var(--pink-light);
    color: var(--pink);
  }

  /* SUMMARY */
  .summary-box {
    background: var(--cream);
    border-radius: 12px;
    padding: 14px;
    margin-top: 12px;
  }
  .summary-row {
    display: flex;
    justify-content: space-between;
    font-size: 0.85rem;
    padding: 4px 0;
    color: var(--muted);
  }
  .summary-row.total {
    font-size: 1rem;
    font-weight: 600;
    color: var(--dark);
    border-top: 1px solid var(--border);
    margin-top: 6px;
    padding-top: 8px;
  }
  .discount-row { color: var(--pink) !important; }

  /* WA BUTTON */
  .wa-btn {
    width: 100%;
    padding: 14px;
    border-radius: 14px;
    border: none;
    background: linear-gradient(135deg, #25D366, #128C7E);
    color: white;
    font-family: 'DM Sans', sans-serif;
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    margin-top: 1rem;
    transition: opacity 0.2s, transform 0.1s;
    letter-spacing: 0.2px;
  }
  .wa-btn:hover { opacity: 0.92; transform: scale(0.99); }
  .wa-btn:active { transform: scale(0.97); }
  .wa-btn:disabled { opacity: 0.5; cursor: not-allowed; transform: none; }
  .wa-icon { font-size: 1.2rem; }

  /* EMPTY STATE */
  .empty-state {
    text-align: center;
    padding: 2rem;
    color: var(--muted);
    font-size: 0.85rem;
  }

  /* FOOTER */
  .footer {
    text-align: center;
    padding: 2rem;
    font-size: 0.78rem;
    color: var(--muted);
    border-top: 1px solid var(--border);
    margin-top: 1rem;
  }

  @media (max-width: 500px) {
    .products-grid { grid-template-columns: 1fr 1fr; }
    .pay-grid { grid-template-columns: 1fr 1fr; }
    .hero-body h1 { font-size: 1.8rem; }
  }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <nav class="nav">
    <div class="logo">SUMORA <span>Dimsum Flora</span></div>
    <div class="nav-badge">🌿 Natural & Fresh</div>
  </nav>
  <div class="hero-body">
    <h1>Dimsum Sehat,<br><em>Cantik & Instagramable</em></h1>
    <p>Perpaduan ayam, tahu, dan wortel dengan kulit dua warna dari ekstrak buah naga & bayam. Tanpa pewarna buatan — lezat, sehat, dan estetik.</p>
    <div class="badges-row">
      <div class="badge"><div class="badge-dot"></div>Tanpa Pewarna Buatan</div>
      <div class="badge"><div class="badge-dot"></div>Kulit Buatan Sendiri</div>
      <div class="badge"><div class="badge-dot"></div>Bergizi Tinggi</div>
      <div class="badge"><div class="badge-dot"></div>Instagramable</div>
    </div>
  </div>
</div>

<!-- PROMO STRIP -->
<div class="promo-strip">
  <span>🎓 <strong>Diskon 5%</strong> untuk Mahasiswa</span>
  <span>🛒 <strong>Diskon 10%</strong> untuk pembelian &gt;15 pcs</span>
</div>

<!-- MAIN -->
<div class="main">

  <!-- PRODUK -->
  <div class="section-title">Menu Produk</div>
  <div class="section-sub">Pilih produk yang kamu inginkan</div>

  <div class="products-grid" id="productsGrid">
    <!-- diisi JS -->
  </div>

  <!-- FORM -->
  <div class="order-card">
    <h3>Detail Pesanan</h3>

    <label for="custName">Nama Pemesan</label>
    <input type="text" id="custName" placeholder="Masukkan nama kamu..." />

    <label for="custPhone">Nomor HP / WhatsApp</label>
    <input type="text" id="custPhone" placeholder="Contoh: 08123456789" />

    <label for="custAddress">Alamat Lengkap</label>
    <input type="text" id="custAddress" placeholder="Jalan, No. Rumah, Kelurahan, Kecamatan, Kota..." style="margin-bottom:0" />
    <div style="font-size:0.75rem;color:var(--muted);margin-bottom:14px;margin-top:4px;">Isi jika pesan antar, kosongkan jika ambil langsung</div>

    <label>Jenis Pengambilan</label>
    <div class="pay-grid" style="margin-bottom:14px" id="pickupGrid">
      <div class="pay-option" data-pickup="Ambil Langsung" onclick="selectPickup(this)">
        <span class="pay-icon">🏠</span>
        <span class="pay-label">Ambil Langsung</span>
      </div>
      <div class="pay-option" data-pickup="Antar ke Alamat" onclick="selectPickup(this)">
        <span class="pay-icon">🛵</span>
        <span class="pay-label">Antar ke Alamat</span>
      </div>
    </div>

    <label>Metode Pembayaran</label>
    <div class="pay-grid" id="payGrid">
      <div class="pay-option" data-pay="Tunai" onclick="selectPay(this)">
        <span class="pay-icon">💵</span>
        <span class="pay-label">Tunai</span>
      </div>
      <div class="pay-option" data-pay="QRIS" onclick="selectPay(this)">
        <span class="pay-icon">📱</span>
        <span class="pay-label">QRIS</span>
      </div>
      <div class="pay-option" data-pay="E-Wallet" onclick="selectPay(this)">
        <span class="pay-icon">👜</span>
        <span class="pay-label">E-Wallet</span>
      </div>
      <div class="pay-option" data-pay="Transfer Bank" onclick="selectPay(this)">
        <span class="pay-icon">🏦</span>
        <span class="pay-label">Transfer Bank</span>
      </div>
    </div>

    <label>Promo (Opsional)</label>
    <div class="promo-opts" id="promoOpts">
      <div class="promo-opt" data-promo="none" data-disc="0" onclick="selectPromo(this)">
        <div class="promo-radio"><div class="promo-dot"></div></div>
        <div class="promo-text">Tidak ada promo</div>
      </div>
      <div class="promo-opt" data-promo="mahasiswa" data-disc="5" onclick="selectPromo(this)">
        <div class="promo-radio"><div class="promo-dot"></div></div>
        <div class="promo-text">Diskon Mahasiswa</div>
        <div class="promo-tag">5%</div>
      </div>
      <div class="promo-opt" data-promo="bulk" data-disc="10" id="promoOpt10" onclick="selectPromo(this)">
        <div class="promo-radio"><div class="promo-dot"></div></div>
        <div class="promo-text">Pembelian &gt;15 pcs</div>
        <div class="promo-tag">10%</div>
      </div>
    </div>

    <!-- SUMMARY -->
    <div class="summary-box" id="summaryBox">
      <div class="empty-state" id="emptyState">Belum ada produk dipilih</div>
      <div id="summaryItems"></div>
    </div>

    <button class="wa-btn" id="waBtn" onclick="sendToWA()" disabled>
      <span class="wa-icon">💬</span> Pesan via WhatsApp
    </button>
  </div>
</div>

<div class="footer">
  &copy; 2025 SUMORA — Dimsum Flora &nbsp;·&nbsp; Dibuat dengan 💚 untuk generasi modern
</div>

<script>
const PRODUCTS = [
  {
    id: 1,
    name: "Sumora Original",
    desc: "Kulit hijau bayam, isian ayam + wortel",
    price: 18000,
    unit: "/6 pcs",
    pcs: 6,
    bg: "green-bg",
    emoji: "🥟"
  },
  {
    id: 2,
    name: "Sumora Merah",
    desc: "Kulit merah buah naga, isian tahu + wortel",
    price: 18000,
    unit: "/6 pcs",
    pcs: 6,
    bg: "pink-bg",
    emoji: "🌸"
  },
  {
    id: 3,
    name: "Sumora Duo",
    desc: "Mix kulit hijau & merah, isian lengkap",
    price: 35000,
    unit: "/12 pcs",
    pcs: 12,
    bg: "green-bg",
    emoji: "🎋"
  },
  {
    id: 4,
    name: "Sumora Party Box",
    desc: "Box spesial 20 pcs, cocok untuk acara",
    price: 55000,
    unit: "/20 pcs",
    pcs: 20,
    bg: "pink-bg",
    emoji: "🎁"
  }
];

const cart = {};
let selectedPay = '';
let selectedPickup = '';
let selectedPromo = { promo: 'none', disc: 0 };
const WA_NUMBER = '6281234567890'; // Ganti dengan nomor WhatsApp bisnis

function formatRupiah(n) {
  return 'Rp ' + n.toLocaleString('id-ID');
}

function renderProducts() {
  const grid = document.getElementById('productsGrid');
  grid.innerHTML = PRODUCTS.map(p => `
    <div class="product-card" id="card-${p.id}" onclick="toggleProduct(${p.id})">
      <div class="product-thumb ${p.bg}">
        <span style="font-size:3rem">${p.emoji}</span>
        <div class="check-badge">✓</div>
      </div>
      <div class="product-info">
        <div class="product-name">${p.name}</div>
        <div class="product-desc">${p.desc}</div>
        <div class="product-price-row">
          <div>
            <div class="product-price">${formatRupiah(p.price)}</div>
            <div class="product-unit">${p.unit}</div>
          </div>
          <div class="qty-control" id="qty-${p.id}" style="display:none" onclick="event.stopPropagation()">
            <button class="qty-btn" onclick="changeQty(${p.id}, -1)">−</button>
            <span class="qty-num" id="qnum-${p.id}">1</span>
            <button class="qty-btn" onclick="changeQty(${p.id}, 1)">+</button>
          </div>
        </div>
      </div>
    </div>
  `).join('');
}

function toggleProduct(id) {
  if (cart[id]) {
    delete cart[id];
    document.getElementById('card-' + id).classList.remove('selected');
    document.getElementById('qty-' + id).style.display = 'none';
  } else {
    cart[id] = 1;
    document.getElementById('card-' + id).classList.add('selected');
    document.getElementById('qty-' + id).style.display = 'flex';
    document.getElementById('qnum-' + id).textContent = 1;
  }
  updateSummary();
}

function changeQty(id, delta) {
  if (!cart[id]) return;
  cart[id] = Math.max(1, (cart[id] || 1) + delta);
  document.getElementById('qnum-' + id).textContent = cart[id];
  updateSummary();
}

function getTotalPcs() {
  let total = 0;
  for (const id in cart) {
    const p = PRODUCTS.find(x => x.id == id);
    total += p.pcs * cart[id];
  }
  return total;
}

function updateSummary() {
  const items = Object.keys(cart);
  const emptyEl = document.getElementById('emptyState');
  const sumItems = document.getElementById('summaryItems');
  const totalPcs = getTotalPcs();

  // Auto-suggest 10% promo
  const promo10El = document.getElementById('promoOpt10');
  if (totalPcs >= 16) {
    promo10El.style.opacity = '1';
    promo10El.style.pointerEvents = 'auto';
  } else {
    promo10El.style.opacity = '0.45';
    if (selectedPromo.promo === 'bulk') {
      selectedPromo = { promo: 'none', disc: 0 };
      document.querySelectorAll('.promo-opt').forEach(o => {
        if (o.dataset.promo === 'none') o.classList.add('selected');
        else o.classList.remove('selected');
      });
    }
  }

  if (items.length === 0) {
    emptyEl.style.display = 'block';
    sumItems.innerHTML = '';
    document.getElementById('waBtn').disabled = true;
    return;
  }

  emptyEl.style.display = 'none';

  let subtotal = 0;
  let rows = '';
  items.forEach(id => {
    const p = PRODUCTS.find(x => x.id == id);
    const qty = cart[id];
    const sub = p.price * qty;
    subtotal += sub;
    rows += `<div class="summary-row"><span>${p.name} × ${qty}</span><span>${formatRupiah(sub)}</span></div>`;
  });

  rows += `<div class="summary-row"><span style="color:var(--muted);font-size:0.78rem">Total pcs: ${totalPcs}</span></div>`;

  const disc = selectedPromo.disc;
  const discAmt = Math.round(subtotal * disc / 100);
  const total = subtotal - discAmt;

  if (disc > 0) {
    rows += `<div class="summary-row discount-row"><span>Diskon ${disc}%</span><span>− ${formatRupiah(discAmt)}</span></div>`;
  }
  rows += `<div class="summary-row total"><span>Total</span><span>${formatRupiah(total)}</span></div>`;

  sumItems.innerHTML = rows;

  const nameOk = document.getElementById('custName').value.trim().length > 0;
  const payOk = selectedPay !== '';
  const pickupOk = selectedPickup !== '';
  document.getElementById('waBtn').disabled = !(nameOk && payOk && pickupOk);
}

function selectPickup(el) {
  document.querySelectorAll('#pickupGrid .pay-option').forEach(o => o.classList.remove('selected'));
  el.classList.add('selected');
  selectedPickup = el.dataset.pickup;
  updateSummary();
}

function selectPay(el) {
  document.querySelectorAll('.pay-option').forEach(o => o.classList.remove('selected'));
  el.classList.add('selected');
  selectedPay = el.dataset.pay;
  updateSummary();
}

function selectPromo(el) {
  const id = el.dataset.promo;
  const disc = parseInt(el.dataset.disc);
  if (id === 'bulk' && getTotalPcs() < 16) return;
  document.querySelectorAll('.promo-opt').forEach(o => o.classList.remove('selected'));
  el.classList.add('selected');
  selectedPromo = { promo: id, disc };
  updateSummary();
}

function sendToWA() {
  const name = document.getElementById('custName').value.trim();
  const phone = document.getElementById('custPhone').value.trim();
  const address = document.getElementById('custAddress').value.trim();
  if (!name) { alert('Mohon isi nama pemesan terlebih dahulu.'); return; }
  if (!selectedPickup) { alert('Mohon pilih jenis pengambilan.'); return; }
  if (!selectedPay) { alert('Mohon pilih metode pembayaran.'); return; }

  const items = Object.keys(cart);
  if (items.length === 0) { alert('Pilih setidaknya satu produk.'); return; }

  let subtotal = 0;
  let orderLines = '';
  items.forEach(id => {
    const p = PRODUCTS.find(x => x.id == id);
    const qty = cart[id];
    const sub = p.price * qty;
    subtotal += sub;
    orderLines += `• ${p.name} × ${qty} porsi (${p.pcs * qty} pcs) = ${formatRupiah(sub)}\n`;
  });

  const totalPcs = getTotalPcs();
  const disc = selectedPromo.disc;
  const discAmt = Math.round(subtotal * disc / 100);
  const total = subtotal - discAmt;
  let promoLine = '';
  if (disc > 0) promoLine = `Promo: Diskon ${disc}% (−${formatRupiah(discAmt)})\n`;

  const phoneLine = phone ? `*No. HP:* ${phone}\n` : '';
  const addressLine = (selectedPickup === 'Antar ke Alamat' && address) ? `*Alamat:* ${address}\n` : (selectedPickup === 'Antar ke Alamat' ? `*Alamat:* (belum diisi)\n` : '');

  const msg =
`Halo Sumora! Saya ingin memesan dimsum 🌿

*Nama:* ${name}
${phoneLine}*Pengambilan:* ${selectedPickup}
${addressLine}
*Pesanan:*
${orderLines.trim()}
*Total pcs:* ${totalPcs}
${promoLine}*Total Bayar:* ${formatRupiah(total)}
*Pembayaran:* ${selectedPay}

Mohon konfirmasi ketersediaan dan pengirimannya ya. Terima kasih! 🙏`;

  const waUrl = `https://wa.me/${WA_NUMBER}?text=${encodeURIComponent(msg)}`;
  window.open(waUrl, '_blank');
}

document.getElementById('custName').addEventListener('input', updateSummary);
document.getElementById('custPhone').addEventListener('input', updateSummary);
document.getElementById('custAddress').addEventListener('input', updateSummary);

// Init
renderProducts();
document.querySelector('.promo-opt[data-promo="none"]').classList.add('selected');
document.getElementById('promoOpt10').style.opacity = '0.45';
</script>
</body>
