<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Radiant Friends: ผจญภัยดินแดนกัมมันตรังสีสุด Kawaii</title>
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts: Gaegu, Fredoka & Mali for ultra kawaii vibes -->
    <link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@400;600;700&family=Gaegu:wght@400;700&family=Mali:wght@400;600;700&display=swap" rel="stylesheet">
    <!-- JS Confetti for celebration effects -->
    <script src="https://cdn.jsdelivr.net/npm/js-confetti@latest/dist/js-confetti.browser.js"></script>
    <!-- MathJax for nice LaTeX rendering -->
    <script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js" id="MathJax-script" async></script>

    <style>
        body {
            font-family: 'Mali', cursive;
            background: linear-gradient(135deg, #fff0f5 0%, #e6f0fa 50%, #f0fff4 100%);
            color: #4a4a4a;
            user-select: none;
            overflow-x: hidden;
        }
        .font-fredoka { font-family: 'Fredoka', cursive; }
        .font-gaegu { font-family: 'Gaegu', cursive; }

        /* Custom Bounce & Float Animations */
        @keyframes float-gentle {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-8px) rotate(2deg); }
        }
        .animate-float { animation: float-gentle 3s ease-in-out infinite; }

        @keyframes pulse-cute {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        .animate-cute { animation: pulse-cute 2s ease-in-out infinite; }

        /* Soft Pastel Cards & Shadows */
        .kawaii-card {
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(10px);
            border: 4px solid #fecdd3;
            border-radius: 2rem;
            box-shadow: 0 12px 30px -8px rgba(244, 63, 94, 0.15), 0 4px 10px -2px rgba(0, 0, 0, 0.05);
        }

        .btn-kawaii {
            transition: all 0.2s cubic-bezier(0.34, 1.56, 0.64, 1);
            box-shadow: 0 6px 0 #cbd5e1;
        }
        .btn-kawaii:hover {
            transform: translateY(-3px);
            box-shadow: 0 9px 0 #cbd5e1;
        }
        .btn-kawaii:active {
            transform: translateY(3px);
            box-shadow: 0 3px 0 #cbd5e1;
        }

        .btn-pink { background: #fda4af; border: 3px solid #f43f5e; color: #881337; box-shadow: 0 6px 0 #f43f5e; }
        .btn-pink:hover { box-shadow: 0 9px 0 #f43f5e; }
        
        .btn-cyan { background: #a5f3fc; border: 3px solid #06b6d4; color: #164e63; box-shadow: 0 6px 0 #06b6d4; }
        .btn-cyan:hover { box-shadow: 0 9px 0 #06b6d4; }

        .btn-amber { background: #fde047; border: 3px solid #eab308; color: #713f12; box-shadow: 0 6px 0 #eab308; }
        .btn-amber:hover { box-shadow: 0 9px 0 #eab308; }

        .btn-purple { background: #e9d5ff; border: 3px solid #a855f7; color: #581c87; box-shadow: 0 6px 0 #a855f7; }
        .btn-purple:hover { box-shadow: 0 9px 0 #a855f7; }

        /* Print styles for certificate */
        @media print {
            body * { visibility: hidden; }
            #printable-cert, #printable-cert * { visibility: visible; }
            #printable-cert {
                position: absolute; left: 0; top: 0; width: 100%;
                background: white !important;
                border: 12px double #f43f5e !important;
                border-radius: 2rem !important;
                padding: 2rem !important;
            }
            .no-print { display: none !important; }
        }
    </style>
</head>
<body class="min-h-screen flex flex-col justify-between relative overflow-x-hidden">

    <!-- Floating background decorative cute items -->
    <div class="fixed inset-0 pointer-events-none z-0 overflow-hidden opacity-40">
        <div class="absolute top-10 left-10 animate-float text-4xl">🌸</div>
        <div class="absolute top-1/4 right-12 animate-float text-4xl" style="animation-delay: 1s;">✨</div>
        <div class="absolute bottom-20 left-16 animate-float text-4xl" style="animation-delay: 1.5s;">🍰</div>
        <div class="absolute bottom-10 right-20 animate-float text-4xl" style="animation-delay: 0.5s;">🧪</div>
        <div class="absolute top-1/2 left-5 animate-float text-3xl" style="animation-delay: 2s;">⭐</div>
    </div>

    <!-- Header Navigation -->
    <header class="sticky top-0 z-40 bg-white/80 backdrop-blur-md border-b-4 border-rose-200 px-4 py-3 shadow-sm">
        <div class="max-w-6xl mx-auto flex justify-between items-center">
            <!-- Brand Logo -->
            <div class="flex items-center gap-3 cursor-pointer" onclick="showScreen('hub-screen')">
                <div class="w-12 h-12 rounded-2xl bg-rose-100 border-2 border-rose-400 flex items-center justify-center animate-cute text-2xl shadow-sm">
                    ⚛️
                </div>
                <div>
                    <h1 class="font-fredoka text-xl md:text-2xl font-bold text-rose-500 leading-tight flex items-center gap-1">
                        Radiant Friends <span class="text-xs bg-rose-200 text-rose-700 font-semibold px-2 py-0.5 rounded-full">Kawaii Science</span>
                    </h1>
                    <p class="text-[11px] text-gray-500 font-semibold">เกมการเรียนรู้เรื่องกัมมันตภาพรังสีสุดน่ารัก</p>
                </div>
            </div>

            <!-- Top Actions -->
            <div class="flex items-center gap-2 md:gap-3">
                <button onclick="toggleAudio()" id="sound-btn" class="px-3 py-1.5 rounded-2xl bg-amber-100 border-2 border-amber-400 text-amber-800 text-xs font-bold hover:bg-amber-200 transition flex items-center gap-1.5">
                    <span id="sound-icon">🔊</span> <span class="hidden sm:inline">เสียงเปิดอยู่</span>
                </button>
                <button onclick="openCodex()" class="px-3 py-1.5 rounded-2xl bg-purple-100 border-2 border-purple-400 text-purple-800 text-xs font-bold hover:bg-purple-200 transition flex items-center gap-1.5">
                    📖 <span class="hidden sm:inline">คลังความรู้</span>
                </button>
                <button onclick="showCertModal()" class="px-3 py-1.5 rounded-2xl bg-rose-100 border-2 border-rose-400 text-rose-800 text-xs font-bold hover:bg-rose-200 transition flex items-center gap-1.5">
                    🎓 <span class="hidden sm:inline">ใบประกาศ</span>
                </button>
            </div>
        </div>
    </header>

    <!-- Main Container -->
    <main class="flex-grow flex items-center justify-center p-4 relative z-10 my-2">

        <!-- ================= HUB / MENU SCREEN ================= -->
        <div id="hub-screen" class="w-full max-w-5xl kawaii-card p-6 md:p-10 text-center space-y-8 animate-cute">
            
            <!-- Mascot Welcome Header -->
            <div class="space-y-3">
                <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-pink-100 border-2 border-pink-300 text-rose-600 text-xs font-bold">
                    <span>✨ ยินดีต้อนรับสู่ห้องแล็บสุดคาวาอี้ของน้องนิวตรอน! ✨</span>
                </div>
                <h2 class="text-3xl md:text-5xl font-extrabold text-rose-500 font-fredoka leading-tight">
                    เรียนรู้ "กัมมันตภาพรังสี" ผ่านมินิเกมสนุกๆ!
                </h2>
                <p class="text-gray-600 max-w-2xl mx-auto text-xs md:text-sm leading-relaxed">
                    สะสมดาวจากมินิเกมทั้ง 4 ด่านเพื่อทำความรู้จักกับพี่ๆ รังสี ($\alpha, \beta, \gamma$), อิ่มอร่อยกับเค้กครึ่งชีวิต, จับคู่ประโยชน์ไอโซโทป และแต่งตัวป้องกันรังสีกันเลย!
                </p>
            </div>

            <!-- Mini Games Selection Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-5 text-left">
                
                <!-- Game 1 Card -->
                <div onclick="startMiniGame(1)" class="group cursor-pointer bg-rose-50/80 border-3 border-rose-300 hover:border-rose-500 rounded-3xl p-5 hover:bg-rose-100/90 transition-all transform hover:-translate-y-1.5 relative overflow-hidden flex flex-col justify-between">
                    <div class="text-center my-2 text-5xl group-hover:scale-110 transition">🎯</div>
                    <div>
                        <div class="flex justify-between items-center mb-1">
                            <span class="px-2 py-0.5 rounded-full text-[10px] font-bold bg-rose-200 text-rose-800">เกมที่ 1</span>
                            <span id="star-g1" class="text-amber-500 text-xs">⭐⭐⭐</span>
                        </div>
                        <h3 class="font-bold text-rose-600 text-base mb-1 font-fredoka">1. ทายใจรังสี!</h3>
                        <p class="text-gray-500 text-[11px] leading-relaxed">ยิงรังสีน้องแอลฟา เบตา แกมมา ทะลุฉากกำบังให้ถูกชนิด!</p>
                    </div>
                    <button class="mt-4 w-full py-2 rounded-2xl btn-pink text-xs font-bold text-center">เริ่มเล่นเลย! ✨</button>
                </div>

                <!-- Game 2 Card -->
                <div onclick="startMiniGame(2)" class="group cursor-pointer bg-cyan-50/80 border-3 border-cyan-300 hover:border-cyan-500 rounded-3xl p-5 hover:bg-cyan-100/90 transition-all transform hover:-translate-y-1.5 relative overflow-hidden flex flex-col justify-between">
                    <div class="text-center my-2 text-5xl group-hover:scale-110 transition">🐹🍰</div>
                    <div>
                        <div class="flex justify-between items-center mb-1">
                            <span class="px-2 py-0.5 rounded-full text-[10px] font-bold bg-cyan-200 text-cyan-800">เกมที่ 2</span>
                            <span id="star-g2" class="text-amber-500 text-xs">⭐⭐⭐</span>
                        </div>
                        <h3 class="font-bold text-cyan-700 text-base mb-1 font-fredoka">2. บ้านแฮมสเตอร์ครึ่งชีวิต</h3>
                        <p class="text-gray-500 text-[11px] leading-relaxed">แบ่งเค้กกับน้องแฮมสเตอร์ตามเวลารอบครึ่งชีวิตพร้อมโจทย์คำนวณ!</p>
                    </div>
                    <button class="mt-4 w-full py-2 rounded-2xl btn-cyan text-xs font-bold text-center">กินเค้กกัน! 🍰</button>
                </div>

                <!-- Game 3 Card -->
                <div onclick="startMiniGame(3)" class="group cursor-pointer bg-amber-50/80 border-3 border-amber-300 hover:border-amber-500 rounded-3xl p-5 hover:bg-amber-100/90 transition-all transform hover:-translate-y-1.5 relative overflow-hidden flex flex-col justify-between">
                    <div class="text-center my-2 text-5xl group-hover:scale-110 transition">🃏✨</div>
                    <div>
                        <div class="flex justify-between items-center mb-1">
                            <span class="px-2 py-0.5 rounded-full text-[10px] font-bold bg-amber-200 text-amber-800">เกมที่ 3</span>
                            <span id="star-g3" class="text-amber-500 text-xs">⭐⭐⭐</span>
                        </div>
                        <h3 class="font-bold text-amber-700 text-base mb-1 font-fredoka">3. จับคู่ไอโซโทปมหาสนุก</h3>
                        <p class="text-gray-500 text-[11px] leading-relaxed">เปิดการ์ดจับคู่ชื่อสารกัมมันตรังสีกับประโยชน์ใช้สอย!</p>
                    </div>
                    <button class="mt-4 w-full py-2 rounded-2xl btn-amber text-xs font-bold text-center">เปิดการ์ด! 🎴</button>
                </div>

                <!-- Game 4 Card -->
                <div onclick="startMiniGame(4)" class="group cursor-pointer bg-purple-50/80 border-3 border-purple-300 hover:border-purple-500 rounded-3xl p-5 hover:bg-purple-100/90 transition-all transform hover:-translate-y-1.5 relative overflow-hidden flex flex-col justify-between">
                    <div class="text-center my-2 text-5xl group-hover:scale-110 transition">🛡️👗</div>
                    <div>
                        <div class="flex justify-between items-center mb-1">
                            <span class="px-2 py-0.5 rounded-full text-[10px] font-bold bg-purple-200 text-purple-800">เกมที่ 4</span>
                            <span id="star-g4" class="text-amber-500 text-xs">⭐⭐⭐</span>
                        </div>
                        <h3 class="font-bold text-purple-700 text-base mb-1 font-fredoka">4. ชุดเกราะป้องกันรังสี</h3>
                        <p class="text-gray-500 text-[11px] leading-relaxed">แต่งตัว วิ่งหนี และวางฉากกำบังด้วยหลัก เวลา-ระยะทาง-กำบัง!</p>
                    </div>
                    <button class="mt-4 w-full py-2 rounded-2xl btn-purple text-xs font-bold text-center">สวมเกราะ! 🛡️</button>
                </div>

            </div>

            <!-- Total Progress & Certificate Trigger -->
            <div class="pt-4 border-t-2 border-dashed border-rose-200 flex flex-col sm:flex-row justify-between items-center gap-4">
                <div class="text-left">
                    <span class="text-xs font-bold text-gray-500">คะแนนสะสมรวมน่ารักๆ:</span>
                    <div class="text-2xl font-bold text-rose-500 font-fredoka"><span id="total-score-display">0</span> / 1000 แต้ม 🌟</div>
                </div>
                <button onclick="showCertModal()" class="px-8 py-3 bg-gradient-to-r from-rose-400 to-pink-400 text-white rounded-2xl font-bold font-fredoka text-base shadow-lg hover:brightness-105 transition transform active:scale-95 flex items-center gap-2">
                    🎓 พิมพ์ใบประกาศนียบัตรน่ารักส่งครู
                </button>
            </div>
        </div>

        <!-- ================= MINI-GAME 1: RADIATION SHOOTER ================= -->
        <div id="game1-screen" class="hidden w-full max-w-4xl kawaii-card p-6 space-y-5">
            <div class="flex justify-between items-center border-b-2 border-rose-200 pb-3">
                <div class="flex items-center gap-3">
                    <span class="text-3xl">🎯</span>
                    <div>
                        <h3 class="font-bold text-rose-600 text-lg font-fredoka">เกมที่ 1: ทายใจรังสี! (Radiation Match)</h3>
                        <p class="text-xs text-gray-500">เลือกยิงรังสีน้องแอลฟา เบตา แกมมา ให้เหมาะกับสิ่งกีดขวางข้างหน้า</p>
                    </div>
                </div>
                <button onclick="showScreen('hub-screen')" class="px-3 py-1 bg-gray-100 hover:bg-gray-200 rounded-xl text-xs font-bold text-gray-600">
                    ✖️ ออก
                </button>
            </div>

            <!-- Game Board Container -->
            <div class="bg-rose-50/60 border-2 border-rose-200 rounded-3xl p-5 space-y-4">
                <div class="flex justify-between items-center text-xs font-bold">
                    <span class="text-rose-700">ด่านที่ <span id="g1-round">1</span> / 5</span>
                    <span class="text-amber-600">คะแนน: <span id="g1-score">0</span> แต้ม</span>
                </div>

                <!-- Shooter Stage Canvas Box -->
                <div id="g1-stage-box" class="bg-white rounded-2xl p-6 border-2 border-rose-200 text-center space-y-4 min-h-[180px] flex flex-col justify-center items-center relative overflow-hidden">
                    <div id="g1-obstacle-icon" class="text-6xl animate-bounce">📄</div>
                    <h4 id="g1-obstacle-title" class="font-bold text-base text-gray-700">แผ่นกระดาษบางๆ ขวางอยู่!</h4>
                    <p id="g1-question" class="text-xs text-rose-600 font-bold">รังสีชนิดใดที่จะ "ถูกแผ่นกระดาษกั้นไว้ได้สำเร็จ" ไม่สามารถทะลุผ่านไปได้?</p>
                </div>

                <!-- Radiation Bullet Buttons -->
                <div class="grid grid-cols-1 md:grid-cols-3 gap-3">
                    <button onclick="shootRadiation('alpha')" class="p-4 bg-emerald-100 border-2 border-emerald-400 hover:bg-emerald-200 rounded-2xl flex flex-col items-center gap-1 transition">
                        <span class="text-2xl">🟢</span>
                        <span class="font-bold text-emerald-800 text-sm font-fredoka">1. รังสีแอลฟา ($\alpha$)</span>
                        <span class="text-[10px] text-emerald-600">มวลมาก ประจุ +2</span>
                    </button>
                    <button onclick="shootRadiation('beta')" class="p-4 bg-cyan-100 border-2 border-cyan-400 hover:bg-cyan-200 rounded-2xl flex flex-col items-center gap-1 transition">
                        <span class="text-2xl">🔵</span>
                        <span class="font-bold text-cyan-800 text-sm font-fredoka">2. รังสีเบตา ($\beta$)</span>
                        <span class="text-[10px] text-cyan-600">อิเล็กตรอน ประจุ -1</span>
                    </button>
                    <button onclick="shootRadiation('gamma')" class="p-4 bg-purple-100 border-2 border-purple-400 hover:bg-purple-200 rounded-2xl flex flex-col items-center gap-1 transition">
                        <span class="text-2xl">🟣</span>
                        <span class="font-bold text-purple-800 text-sm font-fredoka">3. รังสีแกมมา ($\gamma$)</span>
                        <span class="text-[10px] text-purple-600">คลื่นแม่เหล็กไฟฟ้า ไม่มีประจุ</span>
                    </button>
                </div>

                <!-- Feedback Popup Banner -->
                <div id="g1-feedback" class="hidden p-3 rounded-2xl text-center text-xs font-bold leading-relaxed"></div>
            </div>
        </div>

        <!-- ================= MINI-GAME 2: HAMSTER HALF-LIFE ================= -->
        <div id="game2-screen" class="hidden w-full max-w-4xl kawaii-card p-6 space-y-5">
            <div class="flex justify-between items-center border-b-2 border-cyan-200 pb-3">
                <div class="flex items-center gap-3">
                    <span class="text-3xl">🐹🍰</span>
                    <div>
                        <h3 class="font-bold text-cyan-600 text-lg font-fredoka">เกมที่ 2: บ้านแฮมสเตอร์ครึ่งชีวิต (Half-Life Lab)</h3>
                        <p class="text-xs text-gray-500">เรียนรู้การสลายตัวของสารที่ลดลงทีละครึ่งเหมือนเค้กแสนอร่อย!</p>
                    </div>
                </div>
                <button onclick="showScreen('hub-screen')" class="px-3 py-1 bg-gray-100 hover:bg-gray-200 rounded-xl text-xs font-bold text-gray-600">
                    ✖️ ออก
                </button>
            </div>

            <!-- Interactive Cake Half-Life Demo -->
            <div class="bg-cyan-50/80 border-2 border-cyan-200 rounded-3xl p-4 md:p-5 space-y-4">
                <div class="flex justify-between items-center text-xs font-bold text-cyan-800">
                    <span>🍰 สิมูเลเตอร์ลองทานเค้กรังสี: ปริมาณสารที่เหลือ $N(t) = N_0(1/2)^n$</span>
                    <span>รอบครึ่งชีวิต ($n$): <strong id="g2-n-display" class="text-rose-500 text-sm font-fredoka">0</strong></span>
                </div>

                <!-- Cake Slices Grid Visual -->
                <div class="bg-white p-4 rounded-2xl border-2 border-cyan-100 text-center space-y-3">
                    <div id="cake-grid" class="flex flex-wrap justify-center gap-2 max-h-32 overflow-y-auto p-2">
                        <!-- 16 cake icons dynamically generated -->
                    </div>
                    <div class="flex justify-between items-center text-xs font-bold text-gray-600 px-4">
                        <span>เริ่มต้น: <strong id="cake-start-val" class="text-cyan-600">100% (16 ชิ้น)</strong></span>
                        <span>เหลือปัจจุบัน: <strong id="cake-rem-val" class="text-rose-500">100% (16 ชิ้น)</strong></span>
                    </div>
                    <input type="range" id="cake-slider" min="0" max="4" step="1" value="0" oninput="updateCakeSim(this.value)" class="w-full accent-cyan-400 cursor-pointer">
                </div>

                <!-- Quiz Challenge Box -->
                <div class="bg-white p-4 rounded-2xl border-2 border-cyan-200 space-y-3">
                    <div class="flex justify-between items-center text-xs">
                        <span class="font-bold text-cyan-700 font-fredoka">โจทย์ท้าทายความคิด (ข้อ <span id="g2-q-num">1</span> / 3)</span>
                        <span class="text-amber-600 font-bold">คะแนน: <span id="g2-score">0</span> แต้ม</span>
                    </div>
                    <p id="g2-q-text" class="text-xs md:text-sm text-gray-700 font-semibold leading-relaxed">
                        กำลังโหลดโจทย์คำนวณ...
                    </p>
                    <div id="g2-options" class="grid grid-cols-1 md:grid-cols-2 gap-2">
                        <!-- Dynamic options buttons -->
                    </div>
                    <div id="g2-exp" class="hidden p-3 bg-cyan-100 text-cyan-800 rounded-xl text-xs font-semibold leading-relaxed"></div>
                </div>
            </div>
        </div>

        <!-- ================= MINI-GAME 3: ISOTOPE MATCHING ================= -->
        <div id="game3-screen" class="hidden w-full max-w-4xl kawaii-card p-6 space-y-5">
            <div class="flex justify-between items-center border-b-2 border-amber-200 pb-3">
                <div class="flex items-center gap-3">
                    <span class="text-3xl">🃏✨</span>
                    <div>
                        <h3 class="font-bold text-amber-600 text-lg font-fredoka">เกมที่ 3: จับคู่ไอโซโทปมหาสนุก (Isotope Matching)</h3>
                        <p class="text-xs text-gray-500">คลิกการ์ดไอโซโทปรังสีฝั่งซ้าย และคลิกประโยชน์ที่สอดคล้องกันฝั่งขวา!</p>
                    </div>
                </div>
                <button onclick="showScreen('hub-screen')" class="px-3 py-1 bg-gray-100 hover:bg-gray-200 rounded-xl text-xs font-bold text-gray-600">
                    ✖️ ออก
                </button>
            </div>

            <div class="bg-amber-50/70 border-2 border-amber-200 rounded-3xl p-4 md:p-6 space-y-4">
                <div class="flex justify-between items-center text-xs font-bold">
                    <span class="text-amber-800">จับคู่ให้ครบทั้ง 4 คู่เพื่อผ่านด่าน!</span>
                    <span class="text-amber-600">คะแนน: <span id="g3-score">0</span> แต้ม</span>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <!-- Left: Isotopes -->
                    <div id="g3-isotopes-list" class="space-y-2"></div>
                    <!-- Right: Uses -->
                    <div id="g3-uses-list" class="space-y-2"></div>
                </div>
            </div>
        </div>

        <!-- ================= MINI-GAME 4: SAFETY SHIELD MASTER ================= -->
        <div id="game4-screen" class="hidden w-full max-w-4xl kawaii-card p-6 space-y-5">
            <div class="flex justify-between items-center border-b-2 border-purple-200 pb-3">
                <div class="flex items-center gap-3">
                    <span class="text-3xl">🛡️👗</span>
                    <div>
                        <h3 class="font-bold text-purple-600 text-lg font-fredoka">เกมที่ 4: ชุดเกราะป้องกันรังสี (Safety Shield Master)</h3>
                        <p class="text-xs text-gray-500">ปรับใช้หลักการ 3 ประการ: เวลา (Time), ระยะทาง (Distance) และฉากกำบัง (Shielding)!</p>
                    </div>
                </div>
                <button onclick="showScreen('hub-screen')" class="px-3 py-1 bg-gray-100 hover:bg-gray-200 rounded-xl text-xs font-bold text-gray-600">
                    ✖️ ออก
                </button>
            </div>

            <!-- Interactive Defense Lab -->
            <div class="bg-purple-50/70 border-2 border-purple-200 rounded-3xl p-5 space-y-5">
                <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                    
                    <!-- Control 1: Time -->
                    <div class="bg-white p-4 rounded-2xl border-2 border-purple-200 space-y-2 text-center">
                        <span class="text-2xl">⏱️</span>
                        <h4 class="font-bold text-purple-800 text-xs font-fredoka">1. เวลาปฏิบัติงาน ($t$)</h4>
                        <p class="text-[10px] text-gray-500">ยิ่งสั้น ยิ่งปลอดภัย!</p>
                        <input type="range" id="g4-time" min="5" max="60" value="30" oninput="updateG4Dose()" class="w-full accent-purple-400">
                        <div class="text-xs font-bold text-purple-600"><span id="g4-time-val">30</span> นาที</div>
                    </div>

                    <!-- Control 2: Distance -->
                    <div class="bg-white p-4 rounded-2xl border-2 border-purple-200 space-y-2 text-center">
                        <span class="text-2xl">📏</span>
                        <h4 class="font-bold text-purple-800 text-xs font-fredoka">2. ระยะห่าง ($d$)</h4>
                        <p class="text-[10px] text-gray-500">ยิ่งไกล ปริมาณรังสีลดลงกำลังสอง!</p>
                        <input type="range" id="g4-dist" min="1" max="10" value="2" oninput="updateG4Dose()" class="w-full accent-purple-400">
                        <div class="text-xs font-bold text-purple-600"><span id="g4-dist-val">2</span> เมตร</div>
                    </div>

                    <!-- Control 3: Shielding -->
                    <div class="bg-white p-4 rounded-2xl border-2 border-purple-200 space-y-2 text-center">
                        <span class="text-2xl">🛡️</span>
                        <h4 class="font-bold text-purple-800 text-xs font-fredoka">3. ฉากกำบังรังสี ($S$)</h4>
                        <p class="text-[10px] text-gray-500">เลือกชุดเกราะป้องกันให้เหมาะสม</p>
                        <select id="g4-shield" onchange="updateG4Dose()" class="w-full bg-purple-50 border border-purple-300 rounded-xl p-2 text-xs font-bold text-purple-800 focus:outline-none">
                            <option value="none">ไม่มีฉากกำบัง (ตัวคูณ 1.0)</option>
                            <option value="cloth">ชุดแล็บมาตรฐาน (ตัวคูณ 0.8)</option>
                            <option value="lead">เสื้อกั๊กตะกั่วหนา (ตัวคูณ 0.2)</option>
                            <option value="concrete">กำแพงคอนกรีตตะกั่ว (ตัวคูณ 0.05)</option>
                        </select>
                    </div>

                </div>

                <!-- Dose Meter Screen -->
                <div class="bg-white p-5 rounded-2xl border-2 border-purple-200 text-center space-y-3">
                    <div class="text-xs text-gray-500 font-semibold">ปริมาณรังสีสะสมที่ได้รับ:</div>
                    <div id="g4-dose-num" class="text-4xl font-extrabold text-rose-500 font-fredoka">45.0 mSv</div>
                    <div class="w-full bg-gray-100 h-4 rounded-full overflow-hidden border border-gray-200">
                        <div id="g4-dose-bar" class="h-full bg-rose-400 transition-all duration-300" style="width: 75%;"></div>
                    </div>
                    <p id="g4-status" class="text-xs font-bold text-rose-500">⚠️ อันตราย! ปริมาณรังสีสูงเกินมาตรฐาน 10 mSv</p>

                    <button onclick="submitG4Mission()" class="mt-2 px-8 py-3 btn-purple rounded-2xl text-xs font-bold">
                        💖 ยืนยันแผนการป้องกันรังสีสุดปลอดภัย
                    </button>
                </div>
            </div>
        </div>

    </main>

    <!-- ================= CODEX KNOWLEDGE MODAL ================= -->
    <div id="codex-modal" class="hidden fixed inset-0 bg-black/50 backdrop-blur-sm z-50 flex items-center justify-center p-4">
        <div class="bg-white border-4 border-purple-300 rounded-3xl max-w-3xl w-full max-h-[85vh] flex flex-col shadow-2xl overflow-hidden">
            <div class="flex justify-between items-center p-4 bg-purple-100 border-b-2 border-purple-200">
                <h3 class="font-bold text-purple-800 text-base font-fredoka flex items-center gap-2">
                    📖 คลังความรู้น่ารักประจำห้องแล็บ (Kawaii Science Guide)
                </h3>
                <button onclick="closeCodex()" class="text-gray-400 hover:text-gray-600 text-lg">✖️</button>
            </div>

            <div class="p-6 overflow-y-auto space-y-5 text-xs text-gray-700 leading-relaxed">
                <div class="space-y-2 border-b border-purple-100 pb-3">
                    <h4 class="font-bold text-rose-600 text-sm font-fredoka">1. ชนิดของรังสีหลัก 3 พี่น้อง</h4>
                    <ul class="list-disc pl-5 space-y-1">
                        <li><strong>รังสีแอลฟา ($\alpha$):</strong> นิวเคลียสฮีเลียม ($^{4}_{2}\text{He}$) มีประจุบวก +2 มวลมาก อำนาจทะลุทะลวงต่ำสุด (กระดาษ 1 แผ่นก็กั้นได้)</li>
                        <li><strong>รังสีเบตา ($\beta$):</strong> อิเล็กตรอนความเร็วสูง ($^{0}_{-1}\text{e}$) ประจุลบ -1 อำนาจทะลุทะลวงปานกลาง (แผ่นอลูมิเนียมกั้นได้)</li>
                        <li><strong>รังสีแกมมา ($\gamma$):</strong> คลื่นแม่เหล็กไฟฟ้าพลังงานสูง ไม่มีประจุ อำนาจทะลุทะลวงสูงมาก (ต้องใช้ตะกั่วหนา/คอนกรีต)</li>
                    </ul>
                </div>

                <div class="space-y-2 border-b border-purple-100 pb-3">
                    <h4 class="font-bold text-cyan-600 text-sm font-fredoka">2. ความหมายของครึ่งชีวิต (Half-Life, $T_{1/2}$)</h4>
                    <p>คือ ระยะเวลาที่สารกัมมันตรังสีสลายตัวจนเหลือเพียง <strong>ครึ่งหนึ่ง (50%)</strong> ของปริมาณเดิม ณ จุดเริ่มต้น</p>
                    <p class="bg-cyan-50 p-2 rounded-xl text-cyan-800 font-bold">สูตรคำนวณ: $N(t) = N_0 \left(\frac{1}{2}\right)^n$  โดยที่ $n = \frac{t}{T_{1/2}}$</p>
                </div>

                <div class="space-y-2">
                    <h4 class="font-bold text-amber-600 text-sm font-fredoka">3. ประโยชน์ & หลักการป้องกันรังสี 3 ประการ</h4>
                    <p>• <strong>ประโยชน์:</strong> Cobalt-60 (รักษามะเร็ง), Iodine-131 (ต่อมไทรอยด์), Carbon-14 (หาอายุวัตถุโบราณ), Phosphorus-32 (ปุ๋ยการเกษตร)</p>
                    <p>• <strong>การป้องกันอันตราย:</strong> ลด<u>เวลา</u> ($t$) + เพิ่ม<u>ระยะทาง</u> ($d$) + เสริม<u>ฉากกำบัง</u> ($S$)</p>
                </div>
            </div>
        </div>
    </div>

    <!-- ================= KAWAII CERTIFICATE MODAL ================= -->
    <div id="cert-modal" class="hidden fixed inset-0 bg-black/60 backdrop-blur-sm z-50 flex items-center justify-center p-4 overflow-y-auto">
        <div class="bg-white border-4 border-rose-300 rounded-3xl max-w-xl w-full p-6 text-center space-y-4 shadow-2xl relative">
            
            <!-- Certificate View Area -->
            <div id="printable-cert" class="border-4 border-dashed border-rose-300 p-6 rounded-2xl bg-rose-50/40 space-y-4 text-left">
                <div class="text-center space-y-1 border-b-2 border-rose-200 pb-3">
                    <div class="text-2xl font-bold text-rose-500 font-fredoka">🌸 ใบประกาศนียบัตรยอดเยี่ยม 🌸</div>
                    <p class="text-[10px] text-gray-500 font-bold uppercase tracking-widest">Kawaii Science Learning Certificate</p>
                </div>

                <div class="space-y-3">
                    <div>
                        <label class="block text-xs font-bold text-gray-600 mb-1">ชื่อ-นามสกุล นักเรียน:</label>
                        <input type="text" id="student-name" placeholder="ระบุชื่อ-นามสกุล..." class="w-full bg-white border-b-2 border-rose-400 font-bold text-rose-600 px-2 py-1 text-sm focus:outline-none rounded-t">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-gray-600 mb-1">ชั้น / เลขที่ / โรงเรียน:</label>
                        <input type="text" id="student-class" placeholder="เช่น ม.5/1 เลขที่ 12..." class="w-full bg-white border-b-2 border-rose-400 font-bold text-rose-600 px-2 py-1 text-sm focus:outline-none rounded-t">
                    </div>
                </div>

                <!-- Scores Breakdown -->
                <div class="bg-white p-3 rounded-xl border border-rose-200 space-y-1">
                    <div class="text-xs font-bold text-gray-600">ผลการเรียนรู้จากมินิเกมกัมมันตภาพรังสี:</div>
                    <div class="grid grid-cols-2 gap-2 text-[11px] font-semibold text-gray-700">
                        <span>🎯 1. ทายใจรังสี: <strong id="cert-g1-val" class="text-rose-500">0</strong> แต้ม</span>
                        <span>🐹 2. ครึ่งชีวิต: <strong id="cert-g2-val" class="text-cyan-600">0</strong> แต้ม</span>
                        <span>🃏 3. จับคู่ไอโซโทป: <strong id="cert-g3-val" class="text-amber-600">0</strong> แต้ม</span>
                        <span>🛡️ 4. ป้องกันรังสี: <strong id="cert-g4-val" class="text-purple-600">0</strong> แต้ม</span>
                    </div>
                    <div class="pt-2 border-t border-dashed border-gray-200 flex justify-between items-center text-xs font-bold">
                        <span>คะแนนรวมทั้งหมด:</span>
                        <span class="text-lg text-rose-500 font-fredoka"><span id="cert-total-val">0</span> / 1000 แต้ม 🌟</span>
                    </div>
                </div>

                <div class="text-center text-xs text-gray-500 font-semibold pt-1">
                    ผ่านการทดสอบองค์ความรู้เรื่องสมบัติ ครึ่งชีวิต ประโยชน์ และการป้องกันรังสีเรียบร้อยแล้ว ✨
                </div>
            </div>

            <!-- Modal Action Buttons -->
            <div class="flex justify-center gap-3 no-print">
                <button onclick="printCert()" class="px-6 py-2.5 btn-pink rounded-2xl text-xs font-bold flex items-center gap-1.5">
                    🖨️ พิมพ์ / บันทึก PDF ส่งครู
                </button>
                <button onclick="closeCertModal()" class="px-4 py-2.5 bg-gray-200 hover:bg-gray-300 text-gray-700 rounded-2xl text-xs font-bold">
                    ปิด
                </button>
            </div>
        </div>
    </div>

    <!-- JavaScript Application Core -->
    <script>
        // Sound & Audio FX Generator
        let audioEnabled = true;
        const AudioCtx = window.AudioContext || window.webkitAudioContext;
        let audioCtx = null;
        const jsConfetti = new JSConfetti();

        function playSound(type) {
            if (!audioEnabled) return;
            try {
                if (!audioCtx) audioCtx = new AudioCtx();
                const now = audioCtx.currentTime;
                const osc = audioCtx.createOscillator();
                const gain = audioCtx.createGain();
                osc.connect(gain);
                gain.connect(audioCtx.destination);

                if (type === 'pop') {
                    osc.frequency.setValueAtTime(600, now);
                    osc.frequency.exponentialRampToValueAtTime(200, now + 0.08);
                    gain.gain.setValueAtTime(0.1, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.08);
                    osc.start(now);
                    osc.stop(now + 0.08);
                } else if (type === 'success') {
                    osc.frequency.setValueAtTime(523.25, now);
                    osc.frequency.setValueAtTime(659.25, now + 0.08);
                    osc.frequency.setValueAtTime(783.99, now + 0.16);
                    gain.gain.setValueAtTime(0.12, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.3);
                    osc.start(now);
                    osc.stop(now + 0.3);
                } else if (type === 'wrong') {
                    osc.frequency.setValueAtTime(200, now);
                    osc.frequency.setValueAtTime(140, now + 0.1);
                    gain.gain.setValueAtTime(0.1, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.25);
                    osc.start(now);
                    osc.stop(now + 0.25);
                }
            } catch(e){}
        }

        function toggleAudio() {
            audioEnabled = !audioEnabled;
            document.getElementById('sound-icon').innerText = audioEnabled ? "🔊" : "🔇";
            document.getElementById('sound-btn').querySelector('span:last-child').innerText = audioEnabled ? "เสียงเปิดอยู่" : "ปิดเสียงแล้ว";
        }

        // Global Scores
        let scores = { 1: 0, 2: 0, 3: 0, 4: 0 };

        function updateTotals() {
            const total = scores[1] + scores[2] + scores[3] + scores[4];
            document.getElementById('total-score-display').innerText = total;
            
            ['g1', 'g2', 'g3', 'g4'].forEach((id, idx) => {
                const sc = scores[idx + 1];
                const starEl = document.getElementById(`star-${id}`);
                if (sc >= 200) starEl.innerText = "⭐⭐⭐";
                else if (sc >= 100) starEl.innerText = "⭐⭐";
                else if (sc > 0) starEl.innerText = "⭐";
                else starEl.innerText = "🔒";
            });
        }

        function showScreen(screenId) {
            playSound('pop');
            ['hub-screen', 'game1-screen', 'game2-screen', 'game3-screen', 'game4-screen'].forEach(id => {
                document.getElementById(id).classList.add('hidden');
            });
            document.getElementById(screenId).classList.remove('hidden');
            updateTotals();
        }

        function openCodex() { playSound('pop'); document.getElementById('codex-modal').classList.remove('hidden'); }
        function closeCodex() { playSound('pop'); document.getElementById('codex-modal').classList.add('hidden'); }

        function startMiniGame(num) {
            playSound('pop');
            if (num === 1) initGame1();
            if (num === 2) initGame2();
            if (num === 3) initGame3();
            if (num === 4) initGame4();
            showScreen(`game${num}-screen`);
        }

        /* ================= GAME 1 LOGIC ================= */
        const g1Questions = [
            {
                icon: "📄", title: "แผ่นกระดาษบางๆ ขวางอยู่!",
                q: "รังสีชนิดใดที่จะ 'ถูกแผ่นกระดาษกั้นไว้ได้สำเร็จ' ไม่สามารถทะลุผ่านไปได้?",
                ans: "alpha", reason: "ถูกต้องจ้า! รังสีแอลฟามีมวลมาก อำนาจทะลุทะลวงต่ำ ถูกกระดาษกั้นได้สบายเลย ✨"
            },
            {
                icon: "🪙", title: "แผ่นอลูมิเนียมหนา 5 มม. ขวางอยู่!",
                q: "รังสีชนิดใดที่จะถูกหยุดไว้ด้วย 'แผ่นอลูมิเนียม' (ในขณะที่แกมมาทะลุผ่านไปได้)?",
                ans: "beta", reason: "เก่งมาก! รังสีเบตาโดนแผ่นอลูมิเนียมกั้นไว้ได้พอดีเลยจ้า 🔵"
            },
            {
                icon: "🧱", title: "บล็อกตะกั่วหนาขวางอยู่!",
                q: "รังสีแกมมา ($\gamma$) พลังงานสูง ต้องใช้วัสดุใดในการหยุดยั้งรังสี?",
                ans: "gamma", reason: "ถูกต้อง! รังสีแกมมาทะลุทะลวงสูงมาก ต้องใช้ตะกั่วหนาหรือคอนกรีตบังเท่านั้น 🟣"
            },
            {
                icon: "⚡", title: "สนามไฟฟ้าขั้วบวก (+) อยู่ด้านบน!",
                q: "รังสีเบตา (ประจุลบ -1) เมื่อพุ่งผ่านสนามไฟฟ้านี้จะเบี่ยงเบนไปทางไหน?",
                ans: "beta", reason: "ถูกต้อง! รังสีเบตามีประจุลบ จึงโดนขั้วบวกดูดเบี่ยงเบนขึ้นด้านบนจ้า ⚡"
            },
            {
                icon: "✨", title: "เคลื่อนที่ผ่านสนามไฟฟ้าเป็นเส้นตรง!",
                q: "รังสีชนิดใดไม่มีประจุไฟฟ้า จึงไม่เบี่ยงเบนในสนามไฟฟ้าเลย?",
                ans: "gamma", reason: "ถูกต้อง! รังสีแกมมาเป็นคลื่นแม่เหล็กไฟฟ้า ไม่มีประจุไฟฟ้า จึงเคลื่อนตรงไปจ้า! 🌟"
            }
        ];
        let g1Idx = 0;

        function initGame1() {
            g1Idx = 0;
            scores[1] = 0;
            document.getElementById('g1-score').innerText = scores[1];
            loadG1Question();
        }

        function loadG1Question() {
            const q = g1Questions[g1Idx];
            document.getElementById('g1-round').innerText = g1Idx + 1;
            document.getElementById('g1-obstacle-icon').innerText = q.icon;
            document.getElementById('g1-obstacle-title').innerText = q.title;
            document.getElementById('g1-question').innerText = q.q;
            document.getElementById('g1-feedback').className = "hidden";
            if (window.MathJax) MathJax.typesetPromise();
        }

        function shootRadiation(type) {
            const q = g1Questions[g1Idx];
            const fb = document.getElementById('g1-feedback');
            fb.classList.remove('hidden');

            if (type === q.ans) {
                playSound('success');
                scores[1] += 50;
                document.getElementById('g1-score').innerText = scores[1];
                fb.className = "p-3 rounded-2xl text-center text-xs font-bold bg-emerald-100 text-emerald-800 border-2 border-emerald-300";
                fb.innerText = "✨ " + q.reason;
            } else {
                playSound('wrong');
                fb.className = "p-3 rounded-2xl text-center text-xs font-bold bg-rose-100 text-rose-800 border-2 border-rose-300";
                fb.innerText = "❌ ยังไม่ถูกต้องน้า ลองทบทวนชนิดประจุและอำนาจทะลุทะลวงอีกครั้งจ้า!";
            }

            setTimeout(() => {
                g1Idx++;
                if (g1Idx < g1Questions.length) loadG1Question();
                else {
                    jsConfetti.addConfetti();
                    alert(`🎉 ผ่านด่านที่ 1 แล้ว! ได้รับ ${scores[1]} แต้ม`);
                    showScreen('hub-screen');
                }
            }, 2000);
        }

        /* ================= GAME 2 LOGIC ================= */
        const g2Questions = [
            {
                q: "เริ่มต้นน้องแฮมสเตอร์มีเค้กรังสี 80 กรัม มีครึ่งชีวิต 5 วัน เมื่อเวลาผ่านไป 15 วัน จะเหลือเค้กกี่กรัม?",
                opts: ["40 กรัม", "20 กรัม", "10 กรัม", "5 กรัม"],
                ans: 2, exp: "เวลารวม 15 วัน / ครึ่งชีวิต 5 วัน = 3 รอบ <br>80g ➔ 40g (รอบ1) ➔ 20g (รอบ2) ➔ 10g (รอบ3) เหลือ 10 กรัมจ้า!"
            },
            {
                q: "ถ้าเริ่มต้นมีเค้ก 100% สลายตัวผ่านไปกี่ครึ่งชีวิต จึงจะเหลือเค้กเพียง 12.5%?",
                opts: ["2 รอบ", "3 รอบ", "4 รอบ", "5 รอบ"],
                ans: 1, exp: "100% ➔ 50% (รอบ1) ➔ 25% (รอบ2) ➔ 12.5% (รอบ3) ตอบ 3 รอบครึ่งชีวิตจ้า!"
            },
            {
                q: "สารกัมมันตรังสีชนิดหนึ่งสลายตัวจาก 100 กรัม เหลือ 25 กรัม ในเวลา 10 วัน สารนี้มีครึ่งชีวิตกี่วัน?",
                opts: ["2.5 วัน", "5 วัน", "10 วัน", "20 วัน"],
                ans: 1, exp: "100g ➔ 50g ➔ 25g (สลายตัว 2 รอบ) <br>ครึ่งชีวิต = 10 วัน / 2 รอบ = 5 วันจ้า!"
            }
        ];
        let g2Idx = 0;

        function initGame2() {
            g2Idx = 0;
            scores[2] = 0;
            document.getElementById('g2-score').innerText = scores[2];
            initCakeGrid();
            loadG2Question();
        }

        function initCakeGrid() {
            const grid = document.getElementById('cake-grid');
            grid.innerHTML = '';
            for (let i = 0; i < 16; i++) {
                const cake = document.createElement('span');
                cake.id = `cake-item-${i}`;
                cake.className = "text-xl transition-all duration-300";
                cake.innerText = "🍰";
                grid.appendChild(cake);
            }
            document.getElementById('cake-slider').value = 0;
            updateCakeSim(0);
        }

        function updateCakeSim(n) {
            document.getElementById('g2-n-display').innerText = n;
            const remCount = Math.round(16 * Math.pow(0.5, n));
            const remPercent = Math.pow(0.5, n) * 100;

            for (let i = 0; i < 16; i++) {
                const el = document.getElementById(`cake-item-${i}`);
                if (el) {
                    if (i < remCount) {
                        el.style.opacity = "1";
                        el.style.transform = "scale(1)";
                    } else {
                        el.style.opacity = "0.15";
                        el.style.transform = "scale(0.7)";
                    }
                }
            }

            document.getElementById('cake-rem-val').innerText = `${remPercent.toFixed(1)}% (${remCount} ชิ้น)`;
        }

        function loadG2Question() {
            const q = g2Questions[g2Idx];
            document.getElementById('g2-q-num').innerText = g2Idx + 1;
            document.getElementById('g2-q-text').innerText = q.q;
            document.getElementById('g2-exp').classList.add('hidden');

            const optsBox = document.getElementById('g2-options');
            optsBox.innerHTML = '';

            q.opts.forEach((opt, idx) => {
                const btn = document.createElement('button');
                btn.className = "p-2.5 bg-cyan-100 hover:bg-cyan-200 border-2 border-cyan-300 rounded-2xl text-xs font-bold text-cyan-900 transition text-left";
                btn.innerText = `${idx + 1}. ${opt}`;
                btn.onclick = () => answerG2(idx);
                optsBox.appendChild(btn);
            });
        }

        function answerG2(selected) {
            const q = g2Questions[g2Idx];
            const exp = document.getElementById('g2-exp');
            exp.innerHTML = "💡 <strong>วิธีคิด:</strong> " + q.exp;
            exp.classList.remove('hidden');

            if (selected === q.ans) {
                playSound('success');
                scores[2] += 80;
                document.getElementById('g2-score').innerText = scores[2];
            } else {
                playSound('wrong');
            }

            setTimeout(() => {
                g2Idx++;
                if (g2Idx < g2Questions.length) loadG2Question();
                else {
                    jsConfetti.addConfetti();
                    alert(`🎉 ผ่านด่านที่ 2 แล้ว! ได้รับ ${scores[2]} แต้ม`);
                    showScreen('hub-screen');
                }
            }, 2500);
        }

        /* ================= GAME 3 LOGIC ================= */
        const g3Data = [
            { id: 'co60', name: 'Cobalt-60 (Co-60)', use: '🩺 ฉายรังสีรักษาโรคมะเร็ง & ถนอมอาหาร' },
            { id: 'i131', name: 'Iodine-131 (I-131)', use: '🦋 ตรวจและรักษาความผิดปกติของต่อมไทรอยด์' },
            { id: 'c14', name: 'Carbon-14 (C-14)', use: '🏺 ตรวจหาอายุวัตถุโบราณและฟอสซิล' },
            { id: 'p32', name: 'Phosphorus-32 (P-32)', use: '🌱 ศึกษาการดูดซึมปุ๋ยของรากพืชในการเกษตร' }
        ];
        let selectedIso3 = null;

        function initGame3() {
            scores[3] = 0;
            document.getElementById('g3-score').innerText = scores[3];
            renderG3Cards();
        }

        function renderG3Cards() {
            const isoList = document.getElementById('g3-isotopes-list');
            const useList = document.getElementById('g3-uses-list');
            isoList.innerHTML = '';
            useList.innerHTML = '';

            g3Data.forEach(item => {
                const btn = document.createElement('button');
                btn.id = `g3-iso-${item.id}`;
                btn.className = "w-full p-3 bg-white border-2 border-amber-300 rounded-2xl text-xs font-bold text-amber-900 text-left hover:bg-amber-100 transition";
                btn.innerText = "⚛️ " + item.name;
                btn.onclick = () => selectG3Iso(item.id);
                isoList.appendChild(btn);
            });

            const shuffled = [...g3Data].sort(() => Math.random() - 0.5);
            shuffled.forEach(item => {
                const btn = document.createElement('button');
                btn.className = "w-full p-3 bg-white border-2 border-amber-300 rounded-2xl text-xs font-semibold text-gray-700 text-left hover:bg-amber-100 transition";
                btn.innerText = item.use;
                btn.onclick = () => matchG3Use(item.id);
                useList.appendChild(btn);
            });
        }

        function selectG3Iso(id) {
            playSound('pop');
            selectedIso3 = id;
            g3Data.forEach(item => {
                const el = document.getElementById(`g3-iso-${item.id}`);
                if (el) {
                    if (item.id === id) el.className = "w-full p-3 bg-amber-200 border-3 border-amber-500 rounded-2xl text-xs font-bold text-amber-950 text-left";
                    else el.className = "w-full p-3 bg-white border-2 border-amber-300 rounded-2xl text-xs font-bold text-amber-900 text-left";
                }
            });
        }

        function matchG3Use(useId) {
            if (!selectedIso3) {
                alert("คลิกเลือกฝั่งการ์ดไอโซโทปด้านซ้ายก่อนน้า ✨");
                return;
            }

            if (selectedIso3 === useId) {
                playSound('success');
                scores[3] += 60;
                document.getElementById('g3-score').innerText = scores[3];
                const card = document.getElementById(`g3-iso-${selectedIso3}`);
                card.classList.add('opacity-30', 'pointer-events-none');
                selectedIso3 = null;

                if (scores[3] >= 240) {
                    jsConfetti.addConfetti();
                    setTimeout(() => {
                        alert(`🎉 จับคู่ครบถ้วน! ได้รับ ${scores[3]} แต้ม`);
                        showScreen('hub-screen');
                    }, 500);
                }
            } else {
                playSound('wrong');
                alert("❌ คู่นี้ยังไม่ถูกต้องน้า ลองดูประโยช์ใหม่อีกครั้งจ้า");
            }
        }

        /* ================= GAME 4 LOGIC ================= */
        function initGame4() {
            scores[4] = 0;
            updateG4Dose();
        }

        function updateG4Dose() {
            const time = parseInt(document.getElementById('g4-time').value);
            const dist = parseInt(document.getElementById('g4-dist').value);
            const shield = document.getElementById('g4-shield').value;

            document.getElementById('g4-time-val').innerText = time;
            document.getElementById('g4-dist-val').innerText = dist;

            let sFactor = 1.0;
            if (shield === 'cloth') sFactor = 0.8;
            if (shield === 'lead') sFactor = 0.2;
            if (shield === 'concrete') sFactor = 0.05;

            const dose = ((10 * time) / (dist * dist)) * sFactor;
            const doseEl = document.getElementById('g4-dose-num');
            const bar = document.getElementById('g4-dose-bar');
            const status = document.getElementById('g4-status');

            doseEl.innerText = dose.toFixed(1) + " mSv";

            if (dose <= 10) {
                doseEl.className = "text-4xl font-extrabold text-emerald-500 font-fredoka";
                bar.className = "h-full bg-emerald-400 transition-all duration-300";
                bar.style.width = `${Math.min(100, (dose/10)*100)}%`;
                status.className = "text-xs font-bold text-emerald-600";
                status.innerText = "💖 ปลอดภัยมากๆ! ปริมาณรังสีสะสมไม่เกินเกณฑ์มาตรฐาน 10 mSv";
            } else {
                doseEl.className = "text-4xl font-extrabold text-rose-500 font-fredoka";
                bar.className = "h-full bg-rose-400 transition-all duration-300";
                bar.style.width = `${Math.min(100, (dose/40)*100)}%`;
                status.className = "text-xs font-bold text-rose-500";
                status.innerText = "⚠️ อันตราย! ปริมาณรังสีสูงเกินมาตรฐาน 10 mSv";
            }
        }

        function submitG4Mission() {
            const doseText = document.getElementById('g4-dose-num').innerText;
            const dose = parseFloat(doseText);

            if (dose <= 10) {
                playSound('success');
                scores[4] = 250;
                jsConfetti.addConfetti();
                alert("💖 ยินดีด้วย! คุณวางแผนระบบป้องกันรังสีได้ปลอดภัยสุดๆ!");
                showScreen('hub-screen');
            } else {
                playSound('wrong');
                alert("⚠️ ปริมาณรังสียังสูงเกินไป ลองลดเวลา เพิ่มระยะทาง หรือเปลี่ยนฉากกำบังให้หนาขึ้นน้า");
            }
        }

        /* ================= CERTIFICATE MODAL LOGIC ================= */
        function showCertModal() {
            playSound('pop');
            document.getElementById('cert-g1-val').innerText = scores[1];
            document.getElementById('cert-g2-val').innerText = scores[2];
            document.getElementById('cert-g3-val').innerText = scores[3];
            document.getElementById('cert-g4-val').innerText = scores[4];

            const total = scores[1] + scores[2] + scores[3] + scores[4];
            document.getElementById('cert-total-val').innerText = total;

            document.getElementById('cert-modal').classList.remove('hidden');
        }

        function closeCertModal() {
            playSound('pop');
            document.getElementById('cert-modal').classList.add('hidden');
        }

        function printCert() {
            window.print();
        }

        // Initialize Application
        window.onload = function() {
            showScreen('hub-screen');
        };
    </script>
</body>
</html>
