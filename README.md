<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portofolio - Vivaldi Iqbal</title>
  
  <!-- Import Font Inter dari Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap" rel="stylesheet">

  <style>
    /* --- CSS Smooth, Elegant & Animated --- */
    
    /* Animasi Latar Belakang Gradien Bergerak */
    @keyframes gradientBG {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    body {
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      /* Gradien yang lebih kaya dengan ukuran lebih besar untuk dianimasikan */
      background: linear-gradient(-45deg, #f5f7fa, #c3cfe2, #e2e8f0, #edf2f7);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
      color: #333333;
      margin: 0;
      padding: 40px 20px;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* Keyframes untuk efek Fade In dari bawah */
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* Animasi melayang ringan untuk elemen tertentu */
    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0px); }
    }

    /* Container Utama */
    .profile-container {
      max-width: 800px;
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(15px);
      -webkit-backdrop-filter: blur(15px);
      border: 1px solid rgba(255, 255, 255, 0.6);
      border-radius: 20px;
      padding: 40px 50px;
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
      transition: transform 0.4s ease, box-shadow 0.4s ease;
      
      /* Memicu animasi fade-in saat pertama kali dimuat */
      animation: fadeInUp 1s ease-out forwards;
    }

    .profile-container:hover {
      box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
    }

    /* Kelas animasi berurutan (Staggered Animation) */
    .animate-item {
      opacity: 0; /* Sembunyikan elemen sebelum animasi berjalan */
      animation: fadeInUp 0.8s ease-out forwards;
    }
    
    .delay-1 { animation-delay: 0.2s; }
    .delay-2 { animation-delay: 0.4s; }
    .delay-3 { animation-delay: 0.6s; }
    .delay-4 { animation-delay: 0.8s; }
    .delay-5 { animation-delay: 1.0s; }

    /* Tipografi */
    .text-center { text-align: center; }

    h1 {
      font-size: 2.5rem;
      color: #1a202c;
      margin-bottom: 5px;
      font-weight: 700;
      letter-spacing: -0.5px;
    }

    /* Animasi gelombang pada emoji tangan */
    .wave {
      display: inline-block;
      animation: wave-animation 2.5s infinite;
      transform-origin: 70% 70%;
    }

    @keyframes wave-animation {
        0% { transform: rotate( 0.0deg) }
       10% { transform: rotate(14.0deg) }
       20% { transform: rotate(-8.0deg) }
       30% { transform: rotate(14.0deg) }
       40% { transform: rotate(-4.0deg) }
       50% { transform: rotate(10.0deg) }
       60% { transform: rotate( 0.0deg) }
      100% { transform: rotate( 0.0deg) }
    }

    h2 {
      font-size: 1.5rem;
      color: #2d3748;
      margin-top: 30px;
      margin-bottom: 15px;
      position: relative;
      display: inline-block;
    }

    /* Garis bawah animasi saat hover pada H2 */
    h2::after {
      content: '';
      position: absolute;
      width: 0;
      height: 3px;
      display: block;
      margin-top: 5px;
      right: 0;
      background: #38B2AC;
      transition: width 0.4s ease;
      -webkit-transition: width 0.4s ease;
    }
    h2:hover::after {
      width: 100%;
      left: 0;
      background: #38B2AC;
    }

    h3 {
      font-size: 1.1rem;
      color: #4a5568;
      font-weight: 400;
      margin-top: 0;
      margin-bottom: 20px;
    }

    h4 {
      font-size: 1.2rem;
      color: #2d3748;
      border-bottom: 2px solid #e2e8f0;
      padding-bottom: 8px;
      display: inline-block;
      margin-bottom: 15px;
      margin-top: 20px;
    }

    p, li {
      line-height: 1.7;
      color: #4a5568;
      font-size: 1rem;
    }

    ul { padding-left: 20px; }
    li {
      margin-bottom: 10px;
      transition: transform 0.2s ease, color 0.2s ease;
    }
    
    /* Efek hover pada list (Tentang Saya) */
    li:hover {
      transform: translateX(5px);
      color: #1a202c;
    }

    hr {
      border: 0;
      height: 1px;
      background: linear-gradient(to right, rgba(0,0,0,0), rgba(0,0,0,0.1), rgba(0,0,0,0));
      margin: 40px 0;
    }

    /* Badges */
    .badge-container {
      display: flex;
      gap: 15px;
      justify-content: center;
      flex-wrap: wrap;
      margin-top: 20px;
      margin-bottom: 10px;
    }

    .badge-container.left { justify-content: flex-start; }

    .badge-container img {
      border-radius: 6px;
      transition: transform 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275), box-shadow 0.3s ease;
      cursor: pointer;
    }

    /* Efek membesar membal (bouncy) pada badge */
    .badge-container img:hover {
      transform: scale(1.15) rotate(-2deg);
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }

    /* Tabel Proyek */
    table {
      width: 100%;
      border-collapse: separate;
      border-spacing: 15px 0;
      margin-top: 10px;
    }

    td {
      background: #ffffff;
      padding: 25px;
      border-radius: 16px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.03);
      vertical-align: top;
      transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      border: 1px solid #edf2f7;
      width: 50%;
      position: relative;
      overflow: hidden;
    }

    /* Efek Hover Kartu Proyek yang Elegan */
    td:hover {
      transform: translateY(-10px) scale(1.02);
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
      border-color: #cbd5e0;
    }

    td h4 {
      margin-top: 0;
      border-bottom: none;
      color: #1a202c;
      font-weight: 700;
      transition: color 0.3s ease;
    }

    td:hover h4 {
      color: #38B2AC; /* Berubah warna saat kartu di-hover */
    }

    /* Gambar GitHub Stats */
    .github-stats {
      transition: transform 0.5s ease;
      animation: float 6s ease-in-out infinite; /* Melayang terus menerus */
    }
    
    .github-stats:hover {
      transform: scale(1.05);
      animation-play-state: paused; /* Berhenti melayang jika di-hover */
    }

    /* Responsif untuk layar kecil (HP) */
    @media (max-width: 600px) {
      table, tr, td {
        display: block;
        width: 100%;
      }
      td {
        margin-bottom: 20px;
        box-sizing: border-box;
      }
    }
  </style>
</head>
<body>

  <div class="profile-container">
    
    <!-- Header Section -->
    <div class="text-center animate-item delay-1">
      <h1>Halo, Saya Vivaldi Iqbal! <span class="wave">👋</span></h1>
      <h3>Seorang Mahasiswa Teknik Informatika & Frontend Developer yang Antusias</h3>
      <p>Saya adalah mahasiswa Teknologi Informasi di Universitas BSI yang memiliki ketertarikan besar dalam membangun antarmuka web yang interaktif dan responsif.</p>
    </div>

    <!-- Kontak & Sosial Media -->
    <div class="badge-container animate-item delay-1">
      <a href="mailto:vivaldiiqbal@gmail.com">
        <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
      </a>
      <a href="https://github.com/vivaldi-iqbalL">
        <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
      </a>
    </div>

    <hr class="animate-item delay-2"/>

    <!-- Tentang Saya -->
    <div class="animate-item delay-2">
      <h2>👨‍💻 Tentang Saya</h2>
      <ul>
        <li>🎓 Saat ini sedang menempuh pendidikan S1 Teknik Informatika (Kelas Karyawan) di <strong>Universitas BSI</strong>.</li>
        <li>💻 Berfokus pada pengembangan aplikasi web, terutama di sisi <strong>Frontend</strong> menggunakan ekosistem modern.</li>
        <li>🚀 Sedang aktif mengembangkan berbagai proyek web, termasuk platform <em>e-commerce</em> dan sistem manajemen layanan.</li>
        <li>⚡ <strong>Fakta Menarik:</strong> Selain <em>coding</em>, saya juga memiliki pengalaman dalam pengaturan jaringan (MikroTik) serta merakit sepeda <em>vintage</em>.</li>
      </ul>
    </div>

    <hr class="animate-item delay-3"/>

    <!-- Keahlian & Teknologi -->
    <div class="animate-item delay-3">
      <h2>🛠️ Keahlian & Teknologi (Tech Stack)</h2>

      <h4>Frontend</h4>
      <div class="badge-container left">
        <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
        <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
        <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
        <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
        <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
      </div>

      <h4>Backend & Database</h4>
      <div class="badge-container left">
        <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
        <img src="https://img.shields.io/badge/Express.js-404D59?style=for-the-badge&logo=express" alt="Express.js" />
        <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP" />
        <img src="https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white" alt="Laravel" />
        <img src="https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" />
        <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
      </div>

      <h4>Tools & Jaringan</h4>
      <div class="badge-container left">
        <img src="https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=apple&logoColor=white" alt="macOS" />
        <img src="https://img.shields.io/badge/VS_Code-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white" alt="VS Code" />
        <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
        <img src="https://img.shields.io/badge/MikroTik-506D85?style=for-the-badge&logo=mikrotik&logoColor=white" alt="MikroTik" />
      </div>
    </div>

    <hr class="animate-item delay-4"/>

    <!-- Proyek Unggulan -->
    <div class="animate-item delay-4">
      <h2>📂 Proyek Unggulan</h2>
      <table>
        <tr>
          <td>
            <h4>🛒 GETRAW FTP</h4>
            <p>Aplikasi web e-commerce <em>full-stack</em> untuk produk <em>streetwear</em>. Dibangun menggunakan <strong>React, Node.js, dan Express</strong> untuk memastikan performa yang cepat dan pengalaman berbelanja yang mulus.</p>
          </td>
          <td>
            <h4>🌐 atto.net</h4>
            <p>Aplikasi web untuk manajemen langganan Wi-Fi perumahan dan permintaan layanan pelanggan. Antarmuka dikembangkan dengan <strong>React dan Tailwind CSS</strong> untuk tampilan yang modern dan responsif.</p>
          </td>
        </tr>
      </table>
    </div>

    <br><br>
    
    <!-- GitHub Stats -->
    <div class="text-center animate-item delay-5">
      <img class="github-stats" src="https://github-readme-stats.vercel.app/api?username=vivaldi-iqbalL&show_icons=true&theme=radium" alt="GitHub Stats" />
    </div>

  </div>

</body>
</html>
