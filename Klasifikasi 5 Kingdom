<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BIO-EXPLORER: Portal 3D & AR Klasifikasi Makhluk Hidup</title>
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts (Plus Jakarta Sans) & Font Awesome Icons -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Tailwind Custom Configuration -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        emerald: {
                            50: '#ecfdf5',
                            100: '#d1fae5',
                            200: '#a7f3d0',
                            500: '#10b981',
                            600: '#059669',
                            700: '#047857',
                            800: '#065f46',
                            900: '#064e3b',
                            950: '#022c22',
                        },
                        cream: '#FFFDF7',
                        sand: '#F5F0E6',
                        amber: {
                            400: '#fbbf24',
                            500: '#f59e0b',
                            600: '#d97706',
                        }
                    },
                    fontFamily: {
                        sans: ['"Plus Jakarta Sans"', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        /* Custom Scrollbar untuk Filter Tab di Mobile */
        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(8px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .animate-fade-in {
            animation: fadeIn 0.3s ease-out forwards;
        }
    </style>
</head>
<body class="bg-cream text-slate-800 font-sans antialiased selection:bg-emerald-500 selection:text-white flex flex-col min-h-screen">

    <!-- 1. STICKY NAVBAR -->
    <nav class="sticky top-0 z-40 bg-white/95 backdrop-blur-md border-b border-emerald-100 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <!-- Brand Logo -->
                <a href="#" class="flex items-center gap-2.5 font-extrabold text-xl text-emerald-900 tracking-tight">
                    <span class="w-10 h-10 bg-gradient-to-br from-emerald-600 to-emerald-800 text-white rounded-xl flex items-center justify-center text-lg shadow-md">
                        🧬
                    </span>
                    <div class="leading-none">
                        <span>BIO-<span class="text-amber-500">EXPLORER</span></span>
                        <span class="block text-[10px] font-bold text-slate-500 tracking-wider uppercase mt-0.5">Digital Classification Lab • Klasifikasi 5 Kingdom</span>
                    </div>
                </a>

                <!-- Mini Progress Pill in Navbar -->
                <div class="flex items-center gap-3">
                    <div class="bg-emerald-50 border border-emerald-200 rounded-full px-3.5 py-1.5 flex items-center gap-2 shadow-inner">
                        <i class="fa-solid fa-vr-cardboard text-emerald-600 text-sm"></i>
                        <span id="nav-progress-badge" class="text-xs font-extrabold text-emerald-900">0 / 14 Diamati</span>
                    </div>
                </div>
            </div>
        </div>
    </nav>

    <!-- 2. HERO SECTION & PROGRESS TRACKER -->
    <header class="bg-gradient-to-br from-emerald-900 via-emerald-800 to-emerald-950 text-white relative overflow-hidden">
        <!-- Decorative Elements -->
        <div class="absolute -right-16 -top-16 w-72 h-72 bg-emerald-500/20 rounded-full blur-3xl pointer-events-none"></div>
        <div class="absolute left-10 -bottom-20 w-64 h-64 bg-amber-500/15 rounded-full blur-3xl pointer-events-none"></div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10 md:py-14 relative z-10">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                
                <!-- Left Text & Guide -->
                <div class="lg:col-span-7 space-y-4">
                    <div class="inline-flex items-center gap-2 bg-emerald-950/60 border border-emerald-500/40 px-3.5 py-1.5 rounded-full text-xs font-bold text-amber-400">
                        <i class="fa-solid fa-flask"></i>
                        <span>IPA Kelas VII SMP • Semester 2</span>
                    </div>
                    <div class="space-y-1.5">
                        <h1 class="text-2xl sm:text-4xl lg:text-[40px] font-extrabold leading-tight tracking-tight">
                            BIO-EXPLORER: <span class="text-amber-400">Digital Classification Lab</span>
                        </h1>
                        <p class="text-lg sm:text-2xl font-extrabold text-emerald-200 tracking-wide flex items-center gap-2">
                            <span class="w-2 h-6 bg-amber-400 rounded-full inline-block"></span>
                            <span>Submateri: Klasifikasi 5 Kingdom</span>
                        </p>
                    </div>
                    <p class="text-emerald-100/90 text-sm sm:text-base leading-relaxed max-w-2xl">
                        Jelajahi Keanekaragaman 5 Kingdom Secara Nyata Melalui Augmented Reality (Assemblr Edu). Amati ciri morfologi setiap takson langsung dari perangkatmu!
                    </p>

                    <!-- Panduan Singkat -->
                    <div class="bg-white/10 backdrop-blur-sm border border-white/15 rounded-2xl p-4 text-xs text-emerald-50 space-y-1.5 max-w-2xl">
                        <p class="font-extrabold text-amber-300 flex items-center gap-1.5">
                            <i class="fa-solid fa-circle-info"></i> Panduan Eksplorasi Lab:
                        </p>
                        <p class="leading-relaxed">
                            1. Pilih kategori <strong>5 Kingdom</strong> atau cari nama takson pada kolom pencarian.<br>
                            2. Klik <strong>"Buka AR / 3D Viewer"</strong> untuk memunculkan objek 3D di ruang nyatamu via Assemblr Edu, atau klik <strong>"Pratinjau Modal"</strong> untuk melihat langsung di layar ini.
                        </p>
                    </div>
                </div>

                <!-- Right Card: Exploration Progress Bar -->
                <div class="lg:col-span-5">
                    <div class="bg-white text-slate-800 rounded-3xl p-6 shadow-xl border-2 border-amber-400/50 space-y-4">
                        <div class="flex items-center justify-between">
                            <div>
                                <span class="text-[11px] font-extrabold uppercase tracking-wider text-emerald-600">Status Penjelajahan</span>
                                <h2 class="text-lg font-extrabold text-emerald-950">Progres Pengamatan AR</h2>
                            </div>
                            <div id="rank-icon" class="w-12 h-12 bg-amber-100 text-amber-600 rounded-2xl flex items-center justify-center text-2xl shadow-inner">
                                🧭
                            </div>
                        </div>

                        <!-- Progress Bar -->
                        <div class="space-y-2">
                            <div class="flex justify-between items-end">
                                <span id="progress-text" class="text-sm font-extrabold text-emerald-900">0 dari 14 Spesimen AR Telah Diamati</span>
                                <span id="progress-percentage" class="text-xs font-extrabold text-amber-600 bg-amber-50 px-2.5 py-0.5 rounded-lg border border-amber-200">0%</span>
                            </div>
                            <div class="w-full bg-slate-100 rounded-full h-3.5 p-0.5 border border-slate-200 overflow-hidden">
                                <div id="progress-bar" class="bg-gradient-to-r from-emerald-500 via-emerald-600 to-amber-500 h-full rounded-full transition-all duration-500" style="width: 0%;"></div>
                            </div>
                        </div>

                        <div class="pt-2 border-t border-slate-100 flex items-center justify-between text-xs">
                            <span class="text-slate-500 font-medium">Pangkat Lab: <strong id="explorer-rank" class="text-emerald-800">Junior Observer</strong></span>
                            <button onclick="resetProgress()" class="text-slate-400 hover:text-red-600 font-bold transition-colors flex items-center gap-1" title="Atur ulang catatan pengamatan">
                                <i class="fa-solid fa-rotate-left"></i> Reset
                            </button>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </header>

    <!-- 3. MAIN WORKSPACE: FILTER TABS, SEARCH BAR & SPECIMEN GRID -->
    <main class="flex-grow max-w-7xl mx-auto w-full px-4 sm:px-6 lg:px-8 py-8 space-y-8">

        <!-- Filter & Search Controls -->
        <section class="bg-white p-4 sm:p-5 rounded-3xl border border-emerald-100 shadow-sm space-y-4">
            <div class="flex flex-col md:flex-row md:items-center justify-between gap-4">
                
                <!-- Kingdom Filter Tabs -->
                <div class="flex items-center gap-2 overflow-x-auto no-scrollbar pb-1 md:pb-0" id="kingdom-tabs">
                    <button onclick="setFilter('All')" data-filter="All" class="filter-btn active shrink-0 px-4 py-2.5 rounded-xl text-xs font-extrabold transition-all bg-emerald-600 text-white shadow-md">
                        Semua Kingdom (14)
                    </button>
                    <button onclick="setFilter('Monera')" data-filter="Monera" class="filter-btn shrink-0 px-4 py-2.5 rounded-xl text-xs font-bold transition-all bg-cream hover:bg-emerald-50 text-slate-700 border border-emerald-100">
                        🧫 Kingdom Monera (1)
                    </button>
                    <button onclick="setFilter('Protista')" data-filter="Protista" class="filter-btn shrink-0 px-4 py-2.5 rounded-xl text-xs font-bold transition-all bg-cream hover:bg-emerald-50 text-slate-700 border border-emerald-100">
                        🔬 Kingdom Protista (2)
                    </button>
                    <button onclick="setFilter('Fungi')" data-filter="Fungi" class="filter-btn shrink-0 px-4 py-2.5 rounded-xl text-xs font-bold transition-all bg-cream hover:bg-emerald-50 text-slate-700 border border-emerald-100">
                        🍄 Kingdom Fungi (1)
                    </button>
                    <button onclick="setFilter('Plantae')" data-filter="Plantae" class="filter-btn shrink-0 px-4 py-2.5 rounded-xl text-xs font-bold transition-all bg-cream hover:bg-emerald-50 text-slate-700 border border-emerald-100">
                        🌿 Kingdom Plantae (4)
                    </button>
                    <button onclick="setFilter('Animalia')" data-filter="Animalia" class="filter-btn shrink-0 px-4 py-2.5 rounded-xl text-xs font-bold transition-all bg-cream hover:bg-emerald-50 text-slate-700 border border-emerald-100">
                        🦁 Kingdom Animalia (6)
                    </button>
                </div>

                <!-- Live Search Bar -->
                <div class="relative w-full md:w-72 shrink-0">
                    <i class="fa-solid fa-magnifying-glass absolute left-3.5 top-1/2 -translate-y-1/2 text-slate-400 text-xs"></i>
                    <input type="text" id="searchInput" oninput="handleSearch()" placeholder="Cari takson (misal: Mamalia, Paku)..." 
                           class="w-full pl-9 pr-8 py-2.5 bg-cream border border-emerald-200 rounded-xl text-xs font-medium text-slate-800 focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500 outline-none transition-all">
                    <button id="clearSearchBtn" onclick="clearSearch()" class="hidden absolute right-3 top-1/2 -translate-y-1/2 text-slate-400 hover:text-slate-600 text-xs">
                        <i class="fa-solid fa-xmark"></i>
                    </button>
                </div>

            </div>
        </section>

        <!-- Active Filter Indicator & Counter -->
        <div class="flex items-center justify-between text-xs text-slate-500 px-1">
            <p>Menampilkan <strong id="visible-count" class="text-emerald-900">14</strong> spesimen AR & 3D</p>
            <p class="hidden sm:block"><i class="fa-solid fa-hand-pointer text-amber-500 mr-1"></i> Klik tombol buka AR atau pratinjau untuk menandai selesai</p>
        </div>

        <!-- SPECIMEN CARDS GRID -->
        <section id="specimen-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
            <!-- Kartu Spesimen dirender secara dinamis melalui JavaScript -->
        </section>

        <!-- Empty State (Jika pencarian tidak ditemukan) -->
        <div id="empty-state" class="hidden text-center py-16 bg-white rounded-3xl border border-emerald-100 space-y-3">
            <div class="text-5xl">🔍</div>
            <h3 class="text-lg font-extrabold text-emerald-950">Spesimen Tidak Ditemukan</h3>
            <p class="text-xs text-slate-500 max-w-md mx-auto">Tidak ada spesimen taksonomi yang cocok dengan kata kunci pencarianmu. Coba gunakan kata kunci lain seperti "Protista", "Ikan", atau "Biji".</p>
            <button onclick="clearSearch(); setFilter('All');" class="mt-2 bg-emerald-600 hover:bg-emerald-700 text-white text-xs font-bold px-5 py-2.5 rounded-xl transition-all">
                Tampilkan Semua Spesimen
            </button>
        </div>

    </main>

    <!-- 4. MODAL PRATINJAU IFRAME (PREVIEW MODAL) -->
    <div id="previewModal" class="fixed inset-0 bg-slate-950/75 backdrop-blur-sm z-50 hidden opacity-0 transition-opacity duration-300 flex items-center justify-center p-3 sm:p-6" onclick="closePreviewModal()">
        <div class="bg-white rounded-3xl max-w-4xl w-full overflow-hidden shadow-2xl border border-emerald-200 flex flex-col max-h-[92vh]" onclick="event.stopPropagation()">
            
            <!-- Modal Header -->
            <div class="bg-emerald-900 text-white px-5 py-4 flex items-center justify-between">
                <div class="flex items-center gap-3">
                    <span id="modal-kingdom-badge" class="bg-amber-400 text-emerald-950 text-[10px] font-extrabold uppercase px-2.5 py-1 rounded-lg">Kingdom</span>
                    <h3 id="modal-title" class="font-extrabold text-sm sm:text-base truncate max-w-[200px] sm:max-w-md">Nama Spesimen</h3>
                </div>
                <div class="flex items-center gap-2">
                    <a id="modal-external-btn" href="#" target="_blank" rel="noopener noreferrer" class="bg-emerald-700 hover:bg-emerald-600 text-white text-xs font-bold px-3 py-1.5 rounded-xl flex items-center gap-1.5 transition-colors">
                        <span class="hidden sm:inline">Layar Penuh / AR</span>
                        <i class="fa-solid fa-up-right-from-square"></i>
                    </a>
                    <button onclick="closePreviewModal()" class="w-8 h-8 rounded-xl bg-white/10 hover:bg-white/20 text-white flex items-center justify-center font-bold text-lg transition-colors">
                        &times;
                    </button>
                </div>
            </div>

            <!-- Fallback Notice Banner -->
            <div class="bg-amber-50 border-b border-amber-200 px-5 py-2.5 flex flex-col sm:flex-row sm:items-center justify-between gap-2 text-xs text-amber-900">
                <p class="flex items-center gap-2">
                    <i class="fa-solid fa-triangle-exclamation text-amber-600"></i>
                    <span>Jika pratinjau 3D tidak muncul atau meminta izin kamera AR, silakan buka langsung di tab baru.</span>
                </p>
                <a id="modal-fallback-link" href="#" target="_blank" rel="noopener noreferrer" class="font-extrabold text-emerald-700 hover:text-emerald-800 underline shrink-0">
                    Buka Tautan Assemblr Edu →
                </a>
            </div>

            <!-- Iframe Container -->
            <div class="relative w-full h-[60vh] sm:h-[65vh] bg-slate-100 flex items-center justify-center">
                <div id="iframe-loader" class="absolute inset-0 flex flex-col items-center justify-center text-slate-500 space-y-2 pointer-events-none">
                    <i class="fa-solid fa-spinner fa-spin text-3xl text-emerald-600"></i>
                    <span class="text-xs font-bold">Memuat Ruang 3D Assemblr Edu...</span>
                </div>
                <iframe id="ar-iframe" src="" class="w-full h-full border-0 relative z-10" allow="camera; accelerometer; gyroscope; magnetometer; xr-spatial-tracking; fullscreen" allowfullscreen></iframe>
            </div>

        </div>
    </div>

    <!-- 5. FOOTER -->
    <footer class="bg-emerald-950 text-white border-t border-emerald-900 mt-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10">
            <div class="flex flex-col md:flex-row items-center justify-between gap-6 pb-8 border-b border-emerald-800/80 text-center md:text-left">
                <div class="space-y-1.5">
                    <div class="flex items-center justify-center md:justify-start gap-2 font-extrabold text-lg">
                        <span>🧬</span>
                        <span>BIO-<span class="text-amber-400">EXPLORER</span>: Digital Classification Lab</span>
                    </div>
                    <p class="text-xs text-emerald-200/80">
                        Media Pembelajaran Interaktif IPA Kelas VII SMP Semester 2 — Materi Klasifikasi Makhluk Hidup.
                    </p>
                </div>

                <div class="flex flex-wrap items-center justify-center gap-3">
                    <button onclick="resetProgress()" class="bg-emerald-900 hover:bg-red-900/60 border border-emerald-700 hover:border-red-500/50 text-emerald-100 text-xs font-bold px-4 py-2.5 rounded-xl transition-all flex items-center gap-1.5">
                        <i class="fa-solid fa-trash-can"></i> Reset Progres Belajar
                    </button>
                    <a href="#" class="bg-amber-500 hover:bg-amber-400 text-emerald-950 text-xs font-extrabold px-4 py-2.5 rounded-xl transition-all flex items-center gap-1.5 shadow-md">
                        <span>Kembali ke Atas</span>
                        <i class="fa-solid fa-arrow-up"></i>
                    </a>
                </div>
            </div>

            <div class="pt-6 flex flex-col sm:flex-row items-center justify-between text-xs text-emerald-400/80 gap-3 text-center">
                <p>&copy; 2026 BIO-EXPLORER Digital Lab. Seluruh hak cipta dilindungi.</p>
                <p class="flex items-center gap-1.5">
                    <i class="fa-solid fa-cube text-amber-400"></i>
                    <span>Aset 3D & Augmented Reality didukung oleh <strong>Assemblr Edu AR</strong></span>
                </p>
            </div>
        </div>
    </footer>

    <!-- JAVASCRIPT APPLICATION LOGIC -->
    <script>
        // DATA 14 SPESIMEN AR ASSEMBLR EDU (EXACT LINKS & CATEGORIES)
        const specimensData = [
            {
                id: "monera-1",
                kingdom: "Monera",
                subGroup: "Prokariotik Uniseluler",
                title: "Spesimen Monera (Bakteri & Ganggang Biru)",
                description: "Organisme bersel satu tanpa membran inti sel (prokariotik). Amati struktur sel bakteri dan cyanobacteria secara 3D.",
                url: "https://asblr.com/SGVxgxR",
                icon: "🧫",
                badgeColor: "bg-blue-100 text-blue-800 border-blue-200"
            },
            {
                id: "protista-1",
                kingdom: "Protista",
                subGroup: "Protozoa",
                title: "Protista Mirip Hewan (Protozoa)",
                description: "Organisme eukariotik bersel satu yang dapat bergerak aktif menggunakan silia, flagela, atau kaki semu (pseudopodia).",
                url: "https://asblr.com/kisnri8",
                icon: "🔬",
                badgeColor: "bg-purple-100 text-purple-800 border-purple-200"
            },
            {
                id: "protista-2",
                kingdom: "Protista",
                subGroup: "Alga / Ganggang",
                title: "Protista Mirip Tumbuhan (Alga)",
                description: "Organisme eukariotik berklorofil yang mampu berfotosintesis namun belum memiliki akar, batang, dan daun sejati.",
                url: "https://asblr.com/dGguJWy",
                icon: "🌊",
                badgeColor: "bg-purple-100 text-purple-800 border-purple-200"
            },
            {
                id: "fungi-1",
                kingdom: "Fungi",
                subGroup: "Jamur Makroskopis",
                title: "Spesimen Fungi (Jamur)",
                description: "Organisme eukariotik tidak berklorofil (heterotrof), dinding sel tersusun dari zat kitin, dan berkembang biak dengan spora.",
                url: "https://asblr.com/gHxbdH7",
                icon: "🍄",
                badgeColor: "bg-amber-100 text-amber-800 border-amber-200"
            },
            {
                id: "plantae-1",
                kingdom: "Plantae",
                subGroup: "Tumbuhan Berspora",
                title: "Pteridophyta (Tumbuhan Paku)",
                description: "Tumbuhan berpembuluh sejati (kormofita) yang berkembang biak menggunakan spora yang terletak pada sorus di balik daun.",
                url: "https://asblr.com/gHxbdH7",
                icon: "🌿",
                badgeColor: "bg-emerald-100 text-emerald-800 border-emerald-200"
            },
            {
                id: "plantae-2",
                kingdom: "Plantae",
                subGroup: "Tumbuhan Peralihan",
                title: "Bryophyta (Tumbuhan Lumut)",
                description: "Tumbuhan peralihan antara talus dan kormus, tidak memiliki pembuluh angkut xilem-floem, dan hidup di tempat lembap.",
                url: "https://asblr.com/poLiXDh",
                icon: "🌱",
                badgeColor: "bg-emerald-100 text-emerald-800 border-emerald-200"
            },
            {
                id: "plantae-3",
                kingdom: "Plantae",
                subGroup: "Tumbuhan Berbiji",
                title: "Spermatophyta - Angiospermae (Tumbuhan Biji Tertutup)",
                description: "Tumbuhan berbunga sejati dengan bakal biji yang terlindungi di dalam daun buah (ovarium), terbagi atas monokotil & dikotil.",
                url: "https://asblr.com/lOkv2f",
                icon: "🌺",
                badgeColor: "bg-emerald-100 text-emerald-800 border-emerald-200"
            },
            {
                id: "plantae-4",
                kingdom: "Plantae",
                subGroup: "Tumbuhan Berbiji",
                title: "Spermatophyta - Gimnospermae (Tumbuhan Biji Terbuka)",
                description: "Tumbuhan dengan bakal biji tidak terlindungi daun buah dan memiliki alat reproduksi berbentuk kerucut (strobilus).",
                url: "https://asblr.com/q5om2hE",
                icon: "🌲",
                badgeColor: "bg-emerald-100 text-emerald-800 border-emerald-200"
            },
            {
                id: "animalia-1",
                kingdom: "Animalia",
                subGroup: "Vertebrata",
                title: "[Vertebrata] Pisces (Ikan)",
                description: "Hewan bertulang belakang yang hidup di perairan, bernapas menggunakan insang, bersisik, dan bergerak dengan sirip.",
                url: "https://asblr.com/oWAN",
                icon: "🐟",
                badgeColor: "bg-rose-100 text-rose-800 border-rose-200"
            },
            {
                id: "animalia-2",
                kingdom: "Animalia",
                subGroup: "Vertebrata",
                title: "[Vertebrata] Mamalia",
                description: "Hewan bertulang belakang berdarah panas (homoioterm), tubuh ditutupi rambut, dan memiliki kelenjar susu untuk menyusui.",
                url: "https://asblr.com/qZm9UhA",
                icon: "🐅",
                badgeColor: "bg-rose-100 text-rose-800 border-rose-200"
            },
            {
                id: "animalia-3",
                kingdom: "Animalia",
                subGroup: "Vertebrata",
                title: "[Vertebrata] Amphibia (Amfibi)",
                description: "Hewan bertulang belakang yang hidup di dua alam (air dan darat), berkulit lembap tanpa sisik, dan mengalami metamorfosis.",
                url: "https://asblr.com/b7UUesH",
                icon: "🐸",
                badgeColor: "bg-rose-100 text-rose-800 border-rose-200"
            },
            {
                id: "animalia-4",
                kingdom: "Animalia",
                subGroup: "Invertebrata",
                title: "[Invertebrata] Platyhelminthes (Cacing Pipih)",
                description: "Hewan tidak bertulang belakang bertubuh pipih simetri bilateral, belum memiliki rongga tubuh sejati (aselomata).",
                url: "https://asblr.com/kiDNuEr",
                icon: "🪱",
                badgeColor: "bg-orange-100 text-orange-800 border-orange-200"
            },
            {
                id: "animalia-5",
                kingdom: "Animalia",
                subGroup: "Invertebrata",
                title: "[Invertebrata] Cnidaria (Hewan Berongga)",
                description: "Hewan invertebrata perairan dengan simetri radial dan memiliki sel penyengat (knidosit) pada tentakelnya seperti ubur-ubur.",
                url: "https://asblr.com/oRHjJ44",
                icon: "🪼",
                badgeColor: "bg-orange-100 text-orange-800 border-orange-200"
            },
            {
                id: "animalia-6",
                kingdom: "Animalia",
                subGroup: "Invertebrata",
                title: "[Invertebrata] Mollusca (Hewan Lunak)",
                description: "Hewan tidak bertulang belakang bertubuh lunak dan berlendir, sebagian besar dilindungi cangkang berbahan zat kapur.",
                url: "https://asblr.com/nzts0dQ",
                icon: "🐌",
                badgeColor: "bg-orange-100 text-orange-800 border-orange-200"
            }
        ];

        // STATE MANAGEMENT (Dilengkapi LocalStorage agar progres tersimpan)
        const STORAGE_KEY = 'bio_explorer_observed_ids_v1';
        let observedIds = new Set();
        let activeKingdom = 'All';
        let searchQuery = '';

        // Load saved progress from localStorage safely
        function loadProgress() {
            try {
                const saved = localStorage.getItem(STORAGE_KEY);
                if (saved) {
                    const parsed = JSON.parse(saved);
                    if (Array.isArray(parsed)) {
                        observedIds = new Set(parsed);
                    }
                }
            } catch (e) {
                console.warn("LocalStorage tidak tersedia, menggunakan state sesi sementara.");
            }
        }

        // Save progress to localStorage
        function saveProgress() {
            try {
                localStorage.setItem(STORAGE_KEY, JSON.stringify([...observedIds]));
            } catch (e) {
                // Ignore storage errors in restricted iframes
            }
        }

        // Mark specimen as observed & update UI
        function markAsObserved(id) {
            if (!observedIds.has(id)) {
                observedIds.add(id);
                saveProgress();
                updateProgressUI();
                renderCards();
            }
        }

        // Toggle observed status manually via badge click
        function toggleObserved(id, event) {
            event.stopPropagation();
            if (observedIds.has(id)) {
                observedIds.delete(id);
            } else {
                observedIds.add(id);
            }
            saveProgress();
            updateProgressUI();
            renderCards();
        }

        // Reset all progress
        function resetProgress() {
            observedIds.clear();
            saveProgress();
            updateProgressUI();
            renderCards();
        }

        // Update Progress Bar & Rank Badges
        function updateProgressUI() {
            const total = specimensData.length;
            const count = observedIds.size;
            const percentage = Math.round((count / total) * 100);

            document.getElementById('progress-text').innerText = `${count} dari ${total} Spesimen AR Telah Diamati`;
            document.getElementById('progress-percentage').innerText = `${percentage}%`;
            document.getElementById('progress-bar').style.width = `${percentage}%`;
            document.getElementById('nav-progress-badge').innerText = `${count} / ${total} Diamati`;

            const rankEl = document.getElementById('explorer-rank');
            const rankIconEl = document.getElementById('rank-icon');

            if (count === total) {
                rankEl.innerText = "Master Taxonomist 🏆";
                rankIconEl.innerText = "🏆";
            } else if (count >= 8) {
                rankEl.innerText = "Senior Bio-Explorer ⭐";
                rankIconEl.innerText = "⭐";
            } else if (count >= 3) {
                rankEl.innerText = "Field Researcher 🔬";
                rankIconEl.innerText = "🔬";
            } else {
                rankEl.innerText = "Junior Observer 🧭";
                rankIconEl.innerText = "🧭";
            }
        }

        // Set Kingdom Filter
        function setFilter(kingdom) {
            activeKingdom = kingdom;
            
            // Update tab button styles
            document.querySelectorAll('.filter-btn').forEach(btn => {
                if (btn.getAttribute('data-filter') === kingdom) {
                    btn.className = "filter-btn active shrink-0 px-4 py-2.5 rounded-xl text-xs font-extrabold transition-all bg-emerald-600 text-white shadow-md";
                } else {
                    btn.className = "filter-btn shrink-0 px-4 py-2.5 rounded-xl text-xs font-bold transition-all bg-cream hover:bg-emerald-50 text-slate-700 border border-emerald-100";
                }
            });

            renderCards();
        }

        // Handle Search Input
        function handleSearch() {
            const input = document.getElementById('searchInput');
            const clearBtn = document.getElementById('clearSearchBtn');
            searchQuery = input.value.trim().toLowerCase();

            if (searchQuery.length > 0) {
                clearBtn.classList.remove('hidden');
            } else {
                clearBtn.classList.add('hidden');
            }

            renderCards();
        }

        function clearSearch() {
            const input = document.getElementById('searchInput');
            input.value = '';
            searchQuery = '';
            document.getElementById('clearSearchBtn').classList.add('hidden');
            renderCards();
        }

        // Render Specimen Cards Grid
        function renderCards() {
            const grid = document.getElementById('specimen-grid');
            const emptyState = document.getElementById('empty-state');
            const visibleCountEl = document.getElementById('visible-count');

            const filtered = specimensData.filter(item => {
                const matchKingdom = activeKingdom === 'All' || item.kingdom === activeKingdom;
                const matchSearch = item.title.toLowerCase().includes(searchQuery) ||
                                    item.kingdom.toLowerCase().includes(searchQuery) ||
                                    item.subGroup.toLowerCase().includes(searchQuery) ||
                                    item.description.toLowerCase().includes(searchQuery);
                return matchKingdom && matchSearch;
            });

            visibleCountEl.innerText = filtered.length;

            if (filtered.length === 0) {
                grid.innerHTML = '';
                grid.classList.add('hidden');
                emptyState.classList.remove('hidden');
                return;
            }

            grid.classList.remove('hidden');
            emptyState.classList.add('hidden');

            grid.innerHTML = filtered.map(item => {
                const isObserved = observedIds.has(item.id);
                const cardBorder = isObserved 
                    ? 'border-emerald-500 ring-2 ring-emerald-500/20 bg-emerald-50/20' 
                    : 'border-emerald-100 hover:border-emerald-400 bg-white';
                
                const statusBadge = isObserved
                    ? `<button onclick="toggleObserved('${item.id}', event)" title="Klik untuk ubah status" class="bg-emerald-600 text-white text-[11px] font-extrabold px-3 py-1 rounded-full shadow-sm flex items-center gap-1 transition-transform active:scale-95">
                         <span>Sudah Diamati ✓</span>
                       </button>`
                    : `<button onclick="toggleObserved('${item.id}', event)" title="Tandai sudah diamati" class="bg-slate-100 hover:bg-emerald-100 text-slate-500 hover:text-emerald-800 text-[11px] font-bold px-3 py-1 rounded-full transition-colors">
                         Belum Diamati
                       </button>`;

                return `
                    <article class="rounded-3xl border-2 ${cardBorder} p-6 shadow-sm hover:shadow-xl transition-all duration-300 flex flex-col justify-between animate-fade-in">
                        <div>
                            <!-- Top Row: Kingdom Tag & Observed Status -->
                            <div class="flex items-center justify-between gap-2 mb-4">
                                <span class="text-[11px] font-extrabold px-2.5 py-1 rounded-lg border ${item.badgeColor}">
                                    Kingdom ${item.kingdom}
                                </span>
                                ${statusBadge}
                            </div>

                            <!-- Icon & Title -->
                            <div class="flex items-start gap-3.5 mb-3">
                                <div class="w-12 h-12 rounded-2xl bg-sand border border-amber-200/60 flex items-center justify-center text-2xl shrink-0 shadow-inner">
                                    ${item.icon}
                                </div>
                                <div>
                                    <span class="text-[11px] font-bold text-amber-600 uppercase tracking-wider block">${item.subGroup}</span>
                                    <h3 class="font-extrabold text-base text-emerald-950 leading-snug mt-0.5">${item.title}</h3>
                                </div>
                            </div>

                            <!-- Description -->
                            <p class="text-xs text-slate-600 leading-relaxed mb-6">
                                ${item.description}
                            </p>
                        </div>

                        <!-- Action Buttons -->
                        <div class="space-y-2.5 pt-4 border-t border-slate-100">
                            <a href="${item.url}" target="_blank" rel="noopener noreferrer" onclick="markAsObserved('${item.id}')"
                               class="w-full bg-emerald-600 hover:bg-emerald-700 text-white font-extrabold py-3 px-4 rounded-xl text-xs shadow-md shadow-emerald-600/20 transition-all flex items-center justify-center gap-2 active:scale-95">
                                <i class="fa-solid fa-vr-cardboard text-sm"></i>
                                <span>Buka AR / 3D Viewer</span>
                                <i class="fa-solid fa-arrow-up-right-from-square text-[10px] opacity-80"></i>
                            </a>
                            
                            <button onclick="openPreviewModal('${item.id}')"
                                    class="w-full bg-amber-50 hover:bg-amber-100 text-amber-900 border border-amber-300/80 font-bold py-2.5 px-4 rounded-xl text-xs transition-all flex items-center justify-center gap-2 active:scale-95">
                                <i class="fa-solid fa-eye text-amber-600"></i>
                                <span>Pratinjau Modal</span>
                            </button>
                        </div>
                    </article>
                `;
            }).join('');
        }

        // Modal Iframe Preview Logic
        function openPreviewModal(id) {
            const item = specimensData.find(s => s.id === id);
            if (!item) return;

            // Tandai otomatis telah diamati
            markAsObserved(id);

            const modal = document.getElementById('previewModal');
            const iframe = document.getElementById('ar-iframe');
            
            document.getElementById('modal-kingdom-badge').innerText = `Kingdom ${item.kingdom}`;
            document.getElementById('modal-title').innerText = item.title;
            document.getElementById('modal-external-btn').href = item.url;
            document.getElementById('modal-fallback-link').href = item.url;
            
            iframe.src = item.url;

            modal.classList.remove('hidden');
            setTimeout(() => modal.classList.remove('opacity-0'), 10);
        }

        function closePreviewModal() {
            const modal = document.getElementById('previewModal');
            const iframe = document.getElementById('ar-iframe');
            
            modal.classList.add('opacity-0');
            setTimeout(() => {
                modal.classList.add('hidden');
                iframe.src = ''; // Hentikan proses 3D saat modal ditutup agar hemat memori HP
            }, 300);
        }

        // Tutup modal dengan tombol Escape
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape') {
                const modal = document.getElementById('previewModal');
                if (!modal.classList.contains('hidden')) {
                    closePreviewModal();
                }
            }
        });

        // Initialize App on Load
        window.addEventListener('DOMContentLoaded', () => {
            loadProgress();
            updateProgressUI();
            renderCards();
        });
    </script>
</body>
</html>
