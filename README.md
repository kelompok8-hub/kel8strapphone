
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Strapphone - Kelompok 8 (12 H)</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Font Awesome untuk Ikon -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts: Quicksand untuk tampilan ceria dan modern -->
    <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;500;600;700&display=swap" rel="stylesheet">

    <!-- Konfigurasi Tailwind Kustom -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Quicksand', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            light: '#ffe4e6', // rose-100 (Backgrounds)
                            DEFAULT: '#fb7185', // rose-400 (Rough Red Pastel vibe)
                            dark: '#e11d48', // rose-600 (Hover states)
                            accent: '#fda4af', // rose-300
                        }
                    }
                }
            }
        }
    </script>

    <style>
        body {
            background-color: #fff1f2; /* Rose 50 */
            scroll-behavior: smooth;
        }
        .glass-effect {
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px -5px rgba(251, 113, 133, 0.4);
        }
        /* Animasi Keranjang */
        @keyframes bounce-short {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-5px); }
        }
        .animate-bounce-short {
            animation: bounce-short 0.5s ease-in-out;
        }
    </style>
</head>
<body class="text-gray-700">

    <!-- Navbar -->
    <nav class="fixed w-full z-50 glass-effect shadow-sm">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-brand-dark flex items-center gap-2">
                <i class="fa-solid fa-mobile-screen-button"></i>
                strapphone
            </a>
            
            <div class="flex items-center gap-6">
                <div class="hidden md:flex gap-6 font-semibold text-gray-600">
                    <a href="#home" class="hover:text-brand transition">Beranda</a>
                    <a href="#about" class="hover:text-brand transition">Tentang Kami</a>
                    <a href="#products" class="hover:text-brand transition">Produk</a>
                    <!-- Link Testimoni dihapus -->
                </div>

                <!-- Tombol Keranjang -->
                <button onclick="toggleCart()" class="relative text-brand-dark hover:text-brand transition">
                    <i class="fa-solid fa-cart-shopping text-2xl"></i>
                    <span id="cart-count" class="absolute -top-2 -right-2 bg-brand text-white text-xs font-bold rounded-full h-5 w-5 flex items-center justify-center hidden">0</span>
                </button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="pt-28 pb-20 px-4">
        <div class="container mx-auto flex flex-col-reverse md:flex-row items-center gap-10">
            <!-- Teks Hero -->
            <div class="flex-1 text-center md:text-left">
                <span class="inline-block bg-brand-light text-brand-dark px-3 py-1 rounded-full text-sm font-bold mb-4">
                    ✨ Aksesoris Kekinian & Murah
                </span>
                <h1 class="text-5xl md:text-6xl font-bold text-gray-800 mb-2 leading-tight">
                    Tampil Kece dengan <span class="text-brand">Strapphone</span>
                </h1>
                
                <!-- Identitas Kelompok -->
                <div class="bg-white/50 p-4 rounded-xl border border-brand-accent mb-6 inline-block w-full md:w-auto">
                    <h2 class="text-xl font-bold text-brand-dark">12 H — Kelompok 8</h2>
                    <ul class="text-sm mt-2 text-gray-600 space-y-1 text-left mx-auto max-w-md">
                        <li><i class="fa-solid fa-bullhorn text-brand w-6"></i> Kiramil Bararah <span class="text-xs bg-brand text-white px-2 py-0.5 rounded ml-1">Marketing</span></li>
                        <li><i class="fa-solid fa-truck-fast text-brand w-6"></i> Muhammad Bagus <span class="text-xs bg-blue-400 text-white px-2 py-0.5 rounded ml-1">Delivery</span></li>
                        <li><i class="fa-solid fa-wallet text-brand w-6"></i> Rusty Meliala Tanjung <span class="text-xs bg-green-500 text-white px-2 py-0.5 rounded ml-1">Keuangan</span></li>
                    </ul>
                </div>

                <p class="text-lg text-gray-600 mb-8 max-w-lg mx-auto md:mx-0">
                    Bikin HP kamu makin cantik dan aman dengan koleksi strapphone handmade kami. Harga pelajar, kualitas sultan! Mulai dari <strong>Rp 15.000</strong>.
                </p>
                <a href="#products" class="inline-block bg-brand hover:bg-brand-dark text-white font-bold py-3 px-8 rounded-full shadow-lg transition transform hover:scale-105">
                    Belanja Sekarang <i class="fa-solid fa-arrow-right ml-2"></i>
                </a>
            </div>

            <!-- Gambar Hero -->
            <div class="flex-1 relative">
                <div class="absolute top-0 right-0 w-72 h-72 bg-brand-accent rounded-full mix-blend-multiply filter blur-2xl opacity-70 animate-blob"></div>
                <div class="absolute bottom-0 left-0 w-72 h-72 bg-purple-200 rounded-full mix-blend-multiply filter blur-2xl opacity-70 animate-blob animation-delay-2000"></div>
                <img src="https://www.static-src.com/wcsstore/Indraprastha/images/catalog/full/catalog-image/106/MTA-166294924/no_brand_marle_phone_strap_luxury_bear_big_pearl_crystal_tali_gantungan_hp_premium_strap_phonestrap_handphone_aesthetic_resin_uv_beruang_mutiara_full02_c81d5fb8.jpg" alt="Strapphone Aesthetic" class="relative rounded-3xl shadow-2xl border-4 border-white w-full object-cover h-[400px] md:h-[500px]">
            </div>
        </div>
    </section>

    <!-- Tentang Kami -->
    <section id="about" class="py-16 bg-white">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-3xl font-bold text-gray-800 mb-4">Tentang <span class="text-brand">Kami</span></h2>
            <div class="w-16 h-1 bg-brand mx-auto mb-8 rounded"></div>
            <p class="text-gray-600 max-w-2xl mx-auto leading-relaxed">
                Kami adalah <strong>Kelompok 8 dari kelas 12 H</strong> yang berdedikasi untuk menghadirkan aksesoris handphone yang trendy dan terjangkau. Strapphone kami dibuat dengan penuh cinta (handmade) menggunakan manik-manik berkualitas tinggi. Kami percaya bahwa gaya tidak harus mahal! Cocok banget buat kamu yang suka OOTD dan ingin HP-nya terlihat lebih <em>stand out</em>.
            </p>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-10">
                <div class="p-6 bg-rose-50 rounded-xl">
                    <i class="fa-solid fa-gem text-4xl text-brand mb-4"></i>
                    <h3 class="font-bold text-lg">Kualitas Premium</h3>
                    <p class="text-sm text-gray-500">Bahan manik kuat dan tali tidak mudah putus.</p>
                </div>
                <div class="p-6 bg-rose-50 rounded-xl">
                    <i class="fa-solid fa-money-bill-wave text-4xl text-brand mb-4"></i>
                    <h3 class="font-bold text-lg">Harga Pelajar</h3>
                    <p class="text-sm text-gray-500">Mulai Rp 15.000, pas di kantong anak sekolah!</p>
                </div>
                <div class="p-6 bg-rose-50 rounded-xl">
                    <i class="fa-solid fa-bolt text-4xl text-brand mb-4"></i>
                    <h3 class="font-bold text-lg">Pengiriman Cepat</h3>
                    <p class="text-sm text-gray-500">Ditangani langsung oleh tim delivery kami.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Daftar Layanan / Produk -->
    <section id="products" class="py-16 px-4 bg-brand-light/30">
        <div class="container mx-auto">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-gray-800">Koleksi <span class="text-brand">Strapphone</span></h2>
                <p class="text-gray-500 mt-2">Pilih desain favoritmu dan masukkan ke keranjang!</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-5xl mx-auto">
                <!-- Produk 1 -->
                <div class="product-card bg-white rounded-2xl shadow-md overflow-hidden transition-all duration-300">
                    <div class="h-64 overflow-hidden relative">
                        <img src="https://down-id.img.susercontent.com/file/id-11134207-7r98z-lvla3ycux49q71" alt="Pastel Dreams" class="w-full h-full object-cover">
                        <span class="absolute top-3 right-3 bg-brand text-white text-xs font-bold px-2 py-1 rounded">Best Seller</span>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="text-xl font-bold text-gray-800">Pastel Dreams</h3>
                            <span class="text-brand font-bold text-lg">Rp 15.000</span>
                        </div>
                        <p class="text-gray-500 text-sm mb-4">Perpaduan warna pastel lembut yang bikin harimu makin cerah. Cocok untuk semua warna HP.</p>
                        <button onclick="addToCart(1, 'Pastel Dreams', 15000)" class="w-full bg-white border-2 border-brand text-brand font-bold py-2 rounded-xl hover:bg-brand hover:text-white transition flex justify-center items-center gap-2">
                            <i class="fa-solid fa-cart-plus"></i> Tambah ke Keranjang
                        </button>
                    </div>
                </div>

                <!-- Produk 2 -->
                <div class="product-card bg-white rounded-2xl shadow-md overflow-hidden transition-all duration-300">
                    <div class="h-64 overflow-hidden relative">
                        <img src="https://img.lazcdn.com/g/ff/kf/S15864469d303487987cb5c3093d432a0Z.jpg_960x960q80.jpg_.webp" alt="Crystal Elegance" class="w-full h-full object-cover">
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="text-xl font-bold text-gray-800">Crystal Elegance</h3>
                            <span class="text-brand font-bold text-lg">Rp 15.000</span>
                        </div>
                        <p class="text-gray-500 text-sm mb-4">Manik kristal bening yang berkilau saat terkena cahaya. Memberikan kesan mewah dan elegan.</p>
                        <button onclick="addToCart(2, 'Crystal Elegance', 15000)" class="w-full bg-white border-2 border-brand text-brand font-bold py-2 rounded-xl hover:bg-brand hover:text-white transition flex justify-center items-center gap-2">
                            <i class="fa-solid fa-cart-plus"></i> Tambah ke Keranjang
                        </button>
                    </div>
                </div>

                <!-- Produk 3 -->
                <div class="product-card bg-white rounded-2xl shadow-md overflow-hidden transition-all duration-300">
                    <div class="h-64 overflow-hidden relative">
                        <img src="https://down-id.img.susercontent.com/file/id-11134207-7rbk9-m7g11pivjweu57_tn.webp" alt="Custom Name" class="w-full h-full object-cover">
                        <span class="absolute top-3 left-3 bg-blue-400 text-white text-xs font-bold px-2 py-1 rounded">Pre-Order</span>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="text-xl font-bold text-gray-800">Custom Name</h3>
                            <span class="text-brand font-bold text-lg">Rp 15.000</span>
                        </div>
                        <p class="text-gray-500 text-sm mb-4">Bisa request nama kamu sendiri! Maksimal 8 huruf. Pilihan warna manik bebas request.</p>
                        <button onclick="addToCart(3, 'Custom Name Strap', 15000)" class="w-full bg-white border-2 border-brand text-brand font-bold py-2 rounded-xl hover:bg-brand hover:text-white transition flex justify-center items-center gap-2">
                            <i class="fa-solid fa-cart-plus"></i> Tambah ke Keranjang
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Formulir Pemesanan & Checkout -->
    <section id="order" class="py-16 bg-brand-light/20">
        <div class="container mx-auto px-4 max-w-4xl">
            <div class="bg-white rounded-3xl shadow-xl overflow-hidden flex flex-col md:flex-row">
                <!-- Sisi Ringkasan Pesanan (Dinamis) -->
                <div class="w-full md:w-1/2 p-8 bg-brand-light">
                    <h3 class="text-2xl font-bold text-brand-dark mb-6">Keranjang Belanja <i class="fa-solid fa-basket-shopping"></i></h3>
                    
                    <div id="cart-items-container" class="space-y-4 mb-6 max-h-60 overflow-y-auto">
                        <p class="text-gray-500 italic">Keranjang masih kosong, ayo pilih produk di atas!</p>
                    </div>

                    <div class="border-t border-brand/20 pt-4">
                        <div class="flex justify-between font-bold text-xl text-gray-800">
                            <span>Total:</span>
                            <span id="cart-total">Rp 0</span>
                        </div>
                    </div>
                </div>

                <!-- Sisi Form Data Diri -->
                <div class="w-full md:w-1/2 p-8">
                    <h3 class="text-2xl font-bold text-gray-800 mb-2">Data Pemesan</h3>
                    <p class="text-sm text-gray-500 mb-6">Isi data lengkap untuk pengiriman.</p>

                    <form onsubmit="handleOrder(event)" class="space-y-4">
                        <div>
                            <label class="block text-sm font-bold text-gray-700 mb-1">Nama Lengkap</label>
                            <input type="text" id="customerName" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-brand focus:ring-1 focus:ring-brand">
                        </div>
                        
                        <div>
                            <label class="block text-sm font-bold text-gray-700 mb-1">Alamat Lengkap</label>
                            <textarea id="customerAddress" required rows="3" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-brand focus:ring-1 focus:ring-brand"></textarea>
                        </div>

                        <div>
                            <label class="block text-sm font-bold text-gray-700 mb-1">Nomor WhatsApp</label>
                            <input type="tel" id="customerPhone" required placeholder="08..." class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-brand focus:ring-1 focus:ring-brand">
                        </div>

                        <div>
                            <label class="block text-sm font-bold text-gray-700 mb-1">Metode Pembayaran</label>
                            <select id="paymentMethod" onchange="togglePaymentInfo()" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-brand">
                                <option value="manual">Transfer Manual / Chat</option>
                                <option value="dana">DANA (Otomatis)</option>
                                <option value="qris">QRIS (Scan)</option>
                            </select>
                        </div>

                        <!-- Info Pembayaran Dinamis -->
                        <div id="payment-info-dana" class="hidden bg-blue-50 p-3 rounded-lg border border-blue-200 text-sm">
                            <p class="font-bold text-blue-600 mb-2">Bayar via DANA:</p>
                            <a href="https://link.dana.id/minta?full_url=https://qr.dana.id/v1/281012012025052927934766" target="_blank" class="block text-center bg-blue-500 text-white py-2 rounded-lg hover:bg-blue-600 transition">
                                <i class="fa-solid fa-wallet"></i> Klik untuk Bayar DANA
                            </a>
                        </div>
                        
                        <div id="payment-info-qris" class="hidden bg-gray-50 p-3 rounded-lg border border-gray-200 text-sm text-center">
                            <p class="font-bold text-gray-700 mb-2">Scan QRIS:</p>
                            <!-- Placeholder QRIS -->
                            <div class="bg-white p-2 inline-block border rounded">
                                <i class="fa-solid fa-qrcode text-6xl text-gray-800"></i>
                                <p class="text-xs mt-1">Scan saat COD / Chat</p>
                            </div>
                        </div>

                        <button type="submit" class="w-full bg-brand hover:bg-brand-dark text-white font-bold py-3 rounded-xl shadow-lg transition mt-4">
                            <i class="fa-brands fa-whatsapp"></i> Pesan Sekarang
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-10">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-2xl font-bold mb-2">strapphone</h2>
            <p class="text-gray-400 mb-6">Kelompok 8 - 12 H</p>
            <div class="flex justify-center gap-4 mb-6">
                <a href="#" class="w-10 h-10 rounded-full bg-gray-700 flex items-center justify-center hover:bg-brand transition"><i class="fa-brands fa-instagram"></i></a>
                <a href="#" class="w-10 h-10 rounded-full bg-gray-700 flex items-center justify-center hover:bg-brand transition"><i class="fa-brands fa-tiktok"></i></a>
                <a href="https://wa.me/62881012765828" class="w-10 h-10 rounded-full bg-gray-700 flex items-center justify-center hover:bg-brand transition"><i class="fa-brands fa-whatsapp"></i></a>
            </div>
            <p class="text-sm text-gray-500">&copy; 2024 Strapphone Kelompok 8. All rights reserved.</p>
        </div>
    </footer>

    <!-- Floating WhatsApp Button -->
    <a href="https://wa.me/62881012765828" target="_blank" class="fixed bottom-6 right-6 bg-green-500 text-white w-14 h-14 rounded-full shadow-2xl flex items-center justify-center text-3xl hover:bg-green-600 transition hover:-translate-y-1 z-50 animate-bounce-short">
        <i class="fa-brands fa-whatsapp"></i>
    </a>

    <!-- JavaScript Logic -->
    <script>
        // State Keranjang
        let cart = [];

        // Format Rupiah
        const formatRupiah = (number) => {
            return new Intl.NumberFormat('id-ID', {
                style: 'currency',
                currency: 'IDR',
                minimumFractionDigits: 0
            }).format(number);
        };

        // Fungsi Tambah ke Keranjang
        function addToCart(id, name, price) 
