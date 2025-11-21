<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Queen Photography</title>
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&family=Playfair+Display:wght@400;700&family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    :root{
      --dark:#2f3136; /* abu-abu tua */
      --light:#d9dbe0; /* abu-abu muda */
      --muted:#9aa0a6; 
      --accent:#c9b6a6; /* elegan hangat */
      --glass: rgba(255,255,255,0.04);
      --card: rgba(255,255,255,0.03);
    }
    *{box-sizing:border-box}
    body{font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial; margin:0; color:#eee; background: linear-gradient(180deg,var(--dark), #1f2023);}
    header{position:sticky;top:0;backdrop-filter: blur(6px);background: linear-gradient(180deg, rgba(20,20,20,0.55), rgba(20,20,20,0.35));border-bottom:1px solid rgba(255,255,255,0.03);z-index:50}
    .container{max-width:1100px;margin:0 auto;padding:28px}

    /* navbar */
    .nav{display:flex;align-items:center;justify-content:space-between}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:56px;height:56px;border-radius:12px;background:linear-gradient(135deg,var(--accent),var(--light));display:flex;align-items:center;justify-content:center;color:var(--dark);font-weight:800;font-family:Playfair Display}
    nav ul{display:flex;gap:18px;list-style:none;margin:0;padding:0}
    nav a{color:var(--light);text-decoration:none;font-weight:600}
    nav li{position:relative}
    /* submenu */
    .submenu{position:absolute;left:0;top:36px;background:var(--card);padding:8px;border-radius:8px;display:none;min-width:180px}
    nav li:hover .submenu{display:block}
    .submenu a{display:block;padding:6px 10px;color:var(--light);font-weight:500}

    /* hero */
    .hero{padding:56px 0;display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center}
    .hero-left h1{font-family:Playfair Display;font-size:44px;margin:0 0 8px;color:var(--light)}
    .hero-left p{color:var(--muted);font-size:15px;line-height:1.6}
    .cta{margin-top:18px}
    .btn{background:var(--accent);color:var(--dark);padding:12px 18px;border-radius:10px;border:none;font-weight:700;cursor:pointer}

    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:16px;border-radius:12px;border:1px solid rgba(255,255,255,0.03)}

    /* gallery */
    .gallery-filters{display:flex;gap:8px;margin-bottom:12px}
    .filter-btn{padding:8px 12px;border-radius:999px;background:transparent;border:1px solid rgba(255,255,255,0.04);cursor:pointer}
    .gallery-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px}
    .photo{position:relative;border-radius:10px;overflow:hidden}
    .photo img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .35s}
    .photo:hover img{transform:scale(1.05)}

    /* price cards */
    .prices{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:14px}
    .price-card{padding:18px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.03)}
    .price-card h3{margin:0 0 6px;font-family:Playfair Display}
    .price-amount{font-weight:800;margin-top:12px;color:var(--accent);font-size:18px}

    /* contact */
    form{display:grid;gap:10px}
    input, textarea, select{padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:var(--light);outline:none}
    label{font-size:13px;color:var(--muted)}

    footer{padding:28px 0 60px;border-top:1px solid rgba(255,255,255,0.03);margin-top:28px}
    .signature{font-family:Great Vibes;font-size:28px;margin:10px 0}

    /* reviews */
    .reviews{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px}
    .review{padding:12px;border-radius:10px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.03)}
    .review h4{margin:0 0 6px;font-size:15px}
    .review p{margin:0;color:var(--muted);font-size:14px}

    @media (max-width:880px){.hero{grid-template-columns:1fr;}.nav{flex-direction:column;align-items:flex-start}.container{padding:18px}}
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="brand">
        <img src="img/logo2.png" alt="Queen Photography Logo" class="logo" style="display:block; margin:0 auto;">
        <div>
          <div style="font-weight:800">Queen Photography</div>
          <div style="font-size:12px;color:var(--muted)">Save Moment On Your Date</div>
        </div>
      </div>
      <nav>
        <ul>
          <li><a href="#about">Tentang Kami</a></li>
          <li>
            <a href="#samples">Sample Hasil ▾</a>
            <div class="submenu card">
              <a href="#wedding">Wedding</a>
              <a href="#prewedding">Prewedding</a>
              <a href="#engagement">Engagement</a>
              <a href="#graduation">Graduation</a>
              <a href="#lain">Lain-lain</a>
            </div>
          </li>
          <li><a href="#prices">Price List</a></li>
          <li><a href="#contact">Contact Person</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <div class="hero-left">
        <h1>Queen Photography</h1>
        <p>Menangkap setiap detik berharga dengan gaya yang elegan dan modern. Kami mengutamakan kualitas, estetika, dan kepuasan pelanggan sejak 2020.</p>
        <div class="cta"><button class="btn" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Hubungi Sekarang</button></div>
      </div>
      <div class="card">
        <strong>Tentang Kami</strong>
        <p style="margin-top:8px;color:var(--muted);font-size:14px">"Queen Photography adalah penyedia jasa Photography & Videography yang melayani berbagai event seperti Wedding, Prewedding, Graduation, Engagement dan lain lain. kami telah berdedikasi sejak tahun 2020 terpercaya dan mengutamakan kepuasan pelanggan pada setiap jepretan dan setiap detik yang kami ambil. berdomisili di Banyuresmi Kecamatan Cigudeg Kabupaten Bogor, kami melayani berbagai lokasi di Jabodetabek."</p>
      </div>
    </section>

    <!-- SAMPLES -->
    <section id="samples" style="margin-top:18px">
      <div style="display:flex;justify-content:space-between;align-items:end;margin-bottom:8px">
        <h2>Sample Hasil</h2>
        <div class="gallery-filters" aria-hidden>
          <button class="filter-btn" onclick="filterGallery('all')">All</button>
          <button class="filter-btn" onclick="filterGallery('wedding')">Wedding</button>
          <button class="filter-btn" onclick="filterGallery('prewedding')">Prewedding</button>
          <button class="filter-btn" onclick="filterGallery('engagement')">Engagement</button>
          <button class="filter-btn" onclick="filterGallery('graduation')">Graduation</button>
          <button class="filter-btn" onclick="filterGallery('lain')">Lain-lain</button>
        </div>
      </div>

      <div id="gallery" class="gallery-grid">
        <!-- use placeholder images; replace with real samples -->
        
        <!-- Wedding samples -->
        <div class="photo" data-type="wedding"><img src="img/wedding1.jpeg" alt="Wedding sample 1"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 2.jpeg" alt="Wedding sample 2"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 3.jpeg" alt="Wedding sample 3"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 4.jpeg" alt="Wedding sample 4"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 5.jpeg" alt="Wedding sample 5"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 6.jpeg" alt="Wedding sample 6"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 7.jpeg" alt="Wedding sample 7"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 8.jpeg" alt="Wedding sample 8"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 9.jpeg" alt="Wedding sample 9"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 10.jpeg" alt="Wedding sample 10"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 11.jpeg" alt="Wedding sample 11"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 12.jpeg" alt="Wedding sample 12"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 13.jpeg" alt="Wedding sample 13"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 14.jpeg" alt="Wedding sample 14"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 15.jpeg" alt="Wedding sample 15"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 16.jpeg" alt="Wedding sample 16"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 17.jpeg" alt="Wedding sample 17"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 18.jpeg" alt="Wedding sample 18"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 19.jpeg" alt="Wedding sample 19"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 20.jpeg" alt="Wedding sample 20"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 21.jpeg" alt="Wedding sample 21"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 22.jpeg" alt="Wedding sample 22"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 23.jpeg" alt="Wedding sample 23"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 24.jpeg" alt="Wedding sample 24"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 25.jpeg" alt="Wedding sample 25"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 26.jpeg" alt="Wedding sample 26"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 27.jpeg" alt="Wedding sample 27"></div>
        <div class="photo" data-type="wedding"><img src="img/wedding 28.jpeg" alt="Wedding sample 28"></div>


        <!-- Prewedding -->
        <div class="photo" data-type="prewedding"><img src="img/prewed 1.jpeg" alt="Prewedding sample 1"></div>
        <div class="photo" data-type="prewedding"><img src="img/prewed 2.jpeg" alt="Prewedding sample 2"></div>
        <div class="photo" data-type="prewedding"><img src="img/prewed 3.jpeg" alt="Prewedding sample 3"></div>
        <div class="photo" data-type="prewedding"><img src="img/prewed 4.jpeg" alt="Prewedding sample 4"></div>
        <div class="photo" data-type="prewedding"><img src="img/prewed 5.jpeg" alt="Prewedding sample 5"></div>
        <div class="photo" data-type="prewedding"><img src="img/prewed 6.jpeg" alt="Prewedding sample 6"></div>

        <!-- Engagement -->
        <div class="photo" data-type="engagement"><img src="img/engagement 1.jpeg" alt="Engagement sample 1"></div>
        <div class="photo" data-type="engagement"><img src="img/engagement 2.jpeg" alt="Engagement sample 2"></div>
        <div class="photo" data-type="engagement"><img src="img/engagement 3.jpeg" alt="Engagement sample 3"></div>
        <div class="photo" data-type="engagement"><img src="img/engagement 4.jpeg" alt="Engagement sample 4"></div>
        <div class="photo" data-type="engagement"><img src="img/engagement 5.jpeg" alt="Engagement sample 5"></div>
        <div class="photo" data-type="engagement"><img src="img/engagement 6.jpeg" alt="Engagement sample 6"></div>
        <div class="photo" data-type="engagement"><img src="img/engagement 7.jpeg" alt="Engagement sample 7"></div>    
        <div class="photo" data-type="engagement"><img src="img/engagement 8.jpeg" alt="Engagement sample 8"></div> 
        

        <!-- Graduation -->
        <div class="photo" data-type="graduation"><img src="img/graduation 1.jpeg" alt="Graduation sample 1"></div>
        <div class="photo" data-type="graduation"><img src="img/graduation 2.jpeg" alt="Graduation sample 2"></div>
        <div class="photo" data-type="graduation"><img src="img/graduation 3.jpeg" alt="Graduation sample 3"></div>
        <div class="photo" data-type="graduation"><img src="img/graduation 4.jpeg" alt="Graduation sample 4"></div>
        <div class="photo" data-type="graduation"><img src="img/graduation 5.jpeg" alt="Graduation sample 5"></div>
        <div class="photo" data-type="graduation"><img src="img/graduation 6.jpeg" alt="Graduation sample 6"></div>
        <div class="photo" data-type="graduation"><img src="img/graduation 7.jpeg" alt="Graduation sample 7"></div>
        <div class="photo" data-type="graduation"><img src="img/graduation 8.jpeg" alt="Graduation sample 8"></div>
        <div class="photo" data-type="graduation"><img src="img/graduation 9.jpeg" alt="Graduation sample 9"></div>
        <div class="photo" data-type="graduation"><img src="img/graduation 10.jpeg" alt="Graduation sample 10"></div>
        <div class="photo" data-type="graduation"><img src="img/graduation 11.jpeg" alt="Graduation sample 11"></div>

        <!-- Lain-lain -->
        <div class="photo" data-type="lain"><img src="img/lain 1.jpeg" alt="Lain sample 1"></div>
        <div class="photo" data-type="lain"><img src="img/lain 2.jpeg" alt="Lain sample 2"></div>
        <div class="photo" data-type="lain"><img src="img/lain 3.jpeg" alt="Lain sample 3"></div>
        <div class="photo" data-type="lain"><img src="img/lain 4.jpeg" alt="Lain sample 4"></div>

      </div>
    </section>

    <!-- PRICES -->
    <section id="prices" style="margin-top:28px">
      <h2>Price List</h2>
      <div class="prices" style="margin-top:12px">
        <div class="price-card">
          <h3><strong>Silver Package</strong></h3>
          <ul style="color:var(--muted);margin:8px 0;padding-left:18px">
            <li>2 Roll Cetak Photo</li>
            <li>Album Magnetic Photo</li>
            <li>Maksimal File Edit 200 Photo</li>
            <li>Free Transport Area Bogor</li>
            <li>Free Pengantaran Photo Area Bogor</li>
          </ul>
          <div class="price-amount"><strong>IDR 900K</strong></div>
        </div>

        <div class="price-card">
          <h3><strong>Gold Package</strong></h3>
          <ul style="color:var(--muted);margin:8px 0;padding-left:18px">
            <li>Photo Kolase</li>
            <li>Album Photo Kolase 11 Sheet</li>
            <li>Box Album Photo</li>
            <li>Flash Disk</li>
            <li>Maksimal Hasil Edit 500 Photo</li>
            <li>Free Transport Area Bogor</li>
            <li>Free Pengantaran Photo Area Bogor</li>
          </ul>
          <div class="price-amount"><strong>IDR 1,4 Jt</strong></div>
        </div>

        <div class="price-card">
          <h3><strong>Platinum Package</strong></h3>
          <ul style="color:var(--muted);margin:8px 0;padding-left:18px">
            <li>Photo Kolase</li>
            <li>Album Photo Kolase 16 Sheet</li>
            <li>Tas Album Photo</li>
            <li>Flash Disk</li>
            <li>Maksimal Hasil Edit 1000 Photo</li>
            <li>Free Transport Area Bogor</li>
            <li>Free Pengantaran Photo Area Bogor</li>
          </ul>
          <div class="price-amount"><strong>IDR 1,8 Jt</strong></div>
        </div>

        <div class="price-card">
          <h3><strong>Sinematik Video</strong></h3>
          <ul style="color:var(--muted);margin:8px 0;padding-left:18px">
            <li>Hasil Video Utama Maksimal 5 Menit</li>
            <li>Hasil Video Singkat Maksimal 2 Menit</li>
            <li>Free Transport Area Bogor</li>
            <li>File On Google Drive</li>
          </ul>
          <div class="price-amount"><strong>IDR 1 Jt</strong></div>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" style="margin-top:28px">
      <h2>Contact Person</h2>
      <div style="display:grid;grid-template-columns:1fr 420px;gap:18px;margin-top:12px">
        <div class="card">
          <form id="contactForm" onsubmit="openWhatsApp(event)">
            <label for="name">Nama</label>
            <input id="name" name="name" required placeholder="Nama Anda" />

            <label for="phone">Nomor HP (Client)</label>
            <input id="phone" name="phone" placeholder="08xxxxxxxxxx" />

            <label for="location">Lokasi Acara</label>
            <input id="location" name="location" required placeholder="Contoh: Bogor, Gedung Pelaminan" />

            <label for="date">Tanggal Acara</label>
            <input id="date" name="date" type="date" required />

            <label for="package">Pilihan Paket</label>
            <select id="package" name="package">
              <option>Paket Silver - IDR 900K</option>
              <option>Paket Gold - IDR 1,4 Jt</option>
              <option>Paket Platinum - IDR 1,8 Jt</option>
              <option>Video Sinematik - IDR 1 Jt</option>
            </select>

            <label for="notes">Catatan / Pesan</label>
            <textarea id="notes" name="notes" rows="4" placeholder="Tambahkan detail tambahan (opsional)"></textarea>

            <button class="btn" type="submit">Kirim via WhatsApp</button>
          </form>

          <p style="margin-top:10px;color:var(--muted);font-size:13px">Dengan mengirim, Anda akan diarahkan ke WhatsApp kami.</p>
        </div>

        <div class="card">
          <strong>Atau hubungi langsung</strong>
          <p style="color:var(--muted);margin-top:6px">Nomor: <a href="https://wa.me/6285715307661" target="_blank" style="color:var(--accent);text-decoration:none">0857-1530-7661</a></p>

          <strong>Follow Instagram</strong>
          <p style="color:var(--muted);margin-top:6px">Klik: <a href="https://www.instagram.com/mr.queen_photography?igsh=MTlkaDZwYzI1dHExNQ==" target="_blank" style="color:var(--accent);text-decoration:none">mr.queen_photography</a></p>
</a>

          <div style="margin-top:12px">
            <strong>Alamat</strong>
            <p style="color:var(--muted);margin-top:6px">Banyuresmi, Kecamatan Cigudeg, Kabupaten Bogor — melayani Jabodetabek</p>
          </div>
        </div>
      </div>
    </section>

    <!-- FOOTER -->
    <footer>
      <div class="container">
        <div style="text-align:center">
          <div class="signature">Queen Photography</div>
          <div style="font-size:14px;color:var(--muted)">Save Moment On Your Date</div>
        </div>

        <div style="margin-top:20px">
          <h3>Review (23)</h3>
          <div class="reviews" style="margin-top:10px">
            <!-- 23 reviews -->
            <div class="review"><h4>Ayu Putri</h4><p>Layanan ramah, hasil fotonya natural dan sesuai harapan. Terima kasih Queen Photography!</p></div>
            <div class="review"><h4>Rizky H</h4><p>Tim profesional, tepat waktu, hasil editnya rapi. Recommended.</p></div>
            <div class="review"><h4>Siti Marlina</h4><p>Albumnya bagus, warna foto hangat dan elegan. Puas banget.</p></div>
            <div class="review"><h4>Fajar Nugroho</h4><p>Fotografernya sabar dan kreatif. Dokumentasi acara berjalan lancar.</p></div>
            <div class="review"><h4>Intan Sari</h4><p>Pelayanan cepat, komunikasi mudah. Foto dikirim tepat waktu.</p></div>
            <div class="review"><h4>Gilang Pratama</h4><p>Hasil video sinematiknya keren, kualitas audio juga terjaga.</p></div>
            <div class="review"><h4>Dewi Lestari</h4><p>Sangat puas dengan konsep prewedding yang mereka tawarkan.</p></div>
            <div class="review"><h4>Andi Wijaya</h4><p>Harga sebanding dengan kualitas. Timnya ramah dan profesional.</p></div>
            <div class="review"><h4>Nadia Putri</h4><p>Fotografer paham angle yang bagus, hasil fotonya Instagramable!</p></div>
            <div class="review"><h4>Tina Kartika</h4><p>Pengerjaan cepat dan hasil editnya detail. Terima kasih banyak.</p></div>
            <div class="review"><h4>Budi Santoso</h4><p>Rekomendasi untuk yang cari tim fotografi wedding di Bogor.</p></div>
            <div class="review"><h4>Rina Marlina</h4><p>Good service. Mereka fleksibel saat hari H.</p></div>
            <div class="review"><h4>Muhammad Ali</h4><p>Foto graduationnya rapi dan komposisinya kuat. Mantap!</p></div>
            <div class="review"><h4>Putri Amelia</h4><p>Album magneticnya elegan dan kualitas cetak memuaskan.</p></div>
            <div class="review"><h4>Hendra Saputra</h4><p>Timnya disiplin dan hasil yang diberikan sesuai brief.</p></div>
            <div class="review"><h4>Sari Wulandari</h4><p>Engagement shoot-nya natural, kami suka suasananya.</p></div>
            <div class="review"><h4>Rudy Kurniawan</h4><p>Komunikasi mudah, tim tahan banting saat cuaca tidak menentu.</p></div>
            <div class="review"><h4>Lina Farida</h4><p>Kualitas warna dan tone foto sangat konsisten. Good job.</p></div>
            <div class="review"><h4>Anton Prabowo</h4><p>Foto-fotonya bercerita, tim kreatif dan penuh ide bagus.</p></div>
            <div class="review"><h4>Megawati</h4><p>Pelayanan ramah dari awal sampai selesai. Sangat direkomendasikan.</p></div>
            <div class="review"><h4>Yuniarta</h4><p>Video singkatnya pas untuk dibagikan di media sosial, ringkas dan menarik.</p></div>
            <div class="review"><h4>Dian S</h4><p>Proses editingnya teliti, kami puas dengan hasil akhir.</p></div>
            <div class="review"><h4>Arief Budiman</h4><p>Overall sangat menyenangkan bekerja sama dengan Queen Photography.</p></div>

          </div>
        </div>
      </div>
    </footer>
  </main>

  <script>
    // Gallery filter
    function filterGallery(type){
      const photos = document.querySelectorAll('#gallery .photo');
      photos.forEach(p=>{
        if(type==='all' || p.dataset.type===type){
          p.style.display='block'
        } else p.style.display='none'
      })
    }

    // WhatsApp open with form data
    function openWhatsApp(e){
      e.preventDefault();
      const name = encodeURIComponent(document.getElementById('name').value || '-');
      const phone = encodeURIComponent(document.getElementById('phone').value || '-');
      const location = encodeURIComponent(document.getElementById('location').value || '-');
      const date = encodeURIComponent(document.getElementById('date').value || '-');
      const pack = encodeURIComponent(document.getElementById('package').value || '-');
      const notes = encodeURIComponent(document.getElementById('notes').value || '-');

      const message = `Halo Queen Photography!%0A%0ANama: ${name}%0ANomor Client: ${phone}%0ALokasi Acara: ${location}%0ATanggal Acara: ${date}%0APilihan Paket: ${pack}%0Acatatan: ${notes}%0A%0ATerima kasih.`;
      // nomor tujuan dalam format internasional (62 untuk Indonesia)
      const waNumber = '6285715307661';

      const url = `https://wa.me/${waNumber}?text=${message}`;
      window.open(url,'_blank');
    }

    // Lightbox behavior: open image in new tab on click (simple)
    document.querySelectorAll('.photo img').forEach(img=>{
      img.style.cursor='zoom-in'
      img.addEventListener('click',()=> window.open(img.src, '_blank'))
    })
  </script>
</body>
</html>
