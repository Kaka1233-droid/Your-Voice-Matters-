<html lang="th">
<head>
  <meta charset="UTF-8" />
  <title>พูดแทนใจ Your Voice Matters – Botnoi Voice</title>

  <!-- Google Fonts: Prompt + Kanit -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Prompt:wght@300;400;500;600;700&family=Kanit:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>

  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            prompt: ['Prompt', 'system-ui', 'sans-serif'],
            kanit: ['Kanit', 'system-ui', 'sans-serif'],
          },
          colors: {
            softpink: '#FDE2FF',
            softpurple: '#E5D4FF',
            softblue: '#E0F2FF',
          },
        }
      }
    }
  </script>

  <style>
    body {
      font-family: 'Prompt', system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }
    .font-kanit {
      font-family: 'Kanit', system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }
  </style>
</head>
<body class="min-h-screen bg-gradient-to-br from-softblue via-softpink to-softpurple flex items-stretch justify-center">

  <div class="w-full max-w-6xl mx-auto p-4 sm:p-6 lg:p-8">
    <!-- กล่องหลัก -->
    <div class="bg-white/80 backdrop-blur-xl shadow-xl rounded-3xl p-4 sm:p-6 lg:p-8 border border-white/60">

      <!-- ส่วนหัว -->
      <header class="flex flex-col md:flex-row items-center md:items-start gap-4 md:gap-6 mb-6">
        <div class="flex-shrink-0">
          <img src="https://kkclassvip.com/wp-content/uploads/2025/05/heart-botnoi-voice.png"
               alt="Botnoi Voice Logo"
               class="w-24 h-auto mx-auto md:mx-0">
        </div>
        <div class="flex-1 text-center md:text-left">
          <h1 class="text-2xl sm:text-3xl lg:text-4xl font-semibold font-kanit text-purple-700 flex items-center justify-center md:justify-start gap-2">
            🗣️ พูดแทนใจ – Botnoi Voice
          </h1>
          <p class="mt-1 text-xs sm:text-sm text-pink-500 font-semibold uppercase tracking-wide">
            Your Voice Matters
          </p>
          <p class="mt-2 text-sm sm:text-base text-gray-600">
            ระบบช่วยสื่อสารสำหรับผู้พิการทางการพูด ใช้ปุ่มข้อความหรือพิมพ์เอง แล้วให้บอทพูดแทนใจคุณ 💜
          </p>
        </div>
      </header>

      <!-- การตั้งค่า Token + เสียง -->
      <section class="mb-6">
        <div class="bg-gradient-to-r from-pink-50 to-purple-50 border border-pink-100 rounded-2xl p-4 sm:p-5 flex flex-col gap-4">
          <div class="flex items-center gap-2 mb-1">
            <span class="inline-flex items-center justify-center w-8 h-8 rounded-full bg-pink-100 text-pink-600 text-lg">🔑</span>
            <h2 class="font-semibold text-gray-800 text-base sm:text-lg">ตั้งค่า Botnoi API Token</h2>
          </div>

          <div class="grid md:grid-cols-[2fr,1fr] gap-4">
            <!-- Token input -->
            <div>
              <label for="tokenInput" class="block text-xs sm:text-sm text-gray-600 mb-1">
                ใส่ Botnoi API Token ของคุณ
              </label>
              <div class="relative">
                <input
                  id="tokenInput"
                  type="password"
                  class="w-full border border-pink-200 rounded-full px-4 py-2 pr-24 text-sm focus:outline-none focus:ring-2 focus:ring-pink-300 focus:border-pink-300 bg-white/80"
                  placeholder="กรอก Token ที่นี่..."
                />
                <button
                  type="button"
                  id="toggleTokenVisibility"
                  class="absolute inset-y-0 right-10 flex items-center text-xs text-purple-500 hover:text-purple-700"
                >
                  👁 แสดง
                </button>
                <button
                  type="button"
                  id="saveTokenBtn"
                  class="absolute inset-y-0 right-0 flex items-center px-3 text-xs font-medium text-white bg-gradient-to-r from-pink-400 to-purple-400 rounded-full hover:from-pink-500 hover:to-purple-500"
                >
                  บันทึก
                </button>
              </div>
              <p class="mt-1 text-[11px] sm:text-xs text-gray-500">
                * Token จะถูกเก็บไว้ในเบราว์เซอร์ของคุณเท่านั้น (localStorage)
              </p>
            </div>

            <!-- เลือกเสียง -->
            <div>
              <label for="speakerSelect" class="block text-xs sm:text-sm text-gray-600 mb-1">
                เลือกเสียงพูด (ไทย/อังกฤษ)
              </label>
              <select
                id="speakerSelect"
                class="w-full border border-purple-200 rounded-full px-4 py-2 text-sm focus:outline-none focus:ring-2 focus:ring-purple-300 focus:border-purple-300 bg-white/80"
              >
                <option value="1">1 – เอวา (th)</option>
                <option value="2">2 – โบ (th)</option>
                <option value="3">3 – คุณงาม (th)</option>
                <option value="4">4 – แม็กซ์ (th)</option>
                <option value="5">5 – อลัน (th)</option>
                <option value="6">6 – ไซเรน (th)</option>
                <option value="7">7 – อลิสา (th)</option>
                <option value="8">8 – เลโอ (th)</option>
                <option value="9">9 – นาเดียร์ (en)</option>
              </select>
              <p class="mt-1 text-[11px] sm:text-xs text-gray-500">
                * เสียง 1–8 ภาษาไทย, เสียง 9 ภาษาอังกฤษ
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- ส่วนหลัก: ปุ่มข้อความ + พื้นที่พิมพ์ -->
      <main class="grid lg:grid-cols-2 gap-6 lg:gap-8">
        <!-- ปุ่มข้อความหมวดหมู่ -->
        <section class="space-y-4">
          <!-- ความต้องการพื้นฐาน -->
          <div class="bg-white/80 rounded-2xl border border-pink-100 p-4 shadow-sm">
            <h3 class="flex items-center gap-2 text-sm sm:text-base font-semibold text-pink-600 mb-3">
              <span class="inline-flex items-center justify-center w-7 h-7 rounded-full bg-pink-100">🍚</span>
              ความต้องการพื้นฐาน
            </h3>
            <div class="grid grid-cols-2 gap-2">
              <button class="quick-btn" data-text="หิวแล้วค่ะ">🍚 หิวแล้วค่ะ</button>
              <button class="quick-btn" data-text="ขอของดื่ม">🥤 ขอของดื่ม</button>
              <button class="quick-btn" data-text="ขอเข้าห้องน้ำ">🚻 ขอเข้าห้องน้ำ</button>
              <button class="quick-btn" data-text="ขอพักหน่อย">🛌 ขอพักหน่อย</button>
              <button class="quick-btn" data-text="หนาวจังเลย">🧊 หนาวจังเลย</button>
              <button class="quick-btn" data-text="ร้อนมากเลยค่ะ">🥵 ร้อนมากเลยค่ะ</button>
            </div>
          </div>

          <!-- ความรู้สึก -->
          <div class="bg-white/80 rounded-2xl border border-purple-100 p-4 shadow-sm">
            <h3 class="flex items-center gap-2 text-sm sm:text-base font-semibold text-purple-600 mb-3">
              <span class="inline-flex items-center justify-center w-7 h-7 rounded-full bg-purple-100">💗</span>
              ความรู้สึก
            </h3>
            <div class="grid grid-cols-2 gap-2">
              <button class="quick-btn" data-text="ดีใจมากเลย">😊 ดีใจมากเลย</button>
              <button class="quick-btn" data-text="รู้สึกเศร้า">😢 รู้สึกเศร้า</button>
              <button class="quick-btn" data-text="โกรธแล้วนะ">😠 โกรธแล้วนะ</button>
              <button class="quick-btn" data-text="กลัวค่ะ">🥺 กลัวค่ะ</button>
              <button class="quick-btn" data-text="รู้สึกไม่สบาย">🤒 รู้สึกไม่สบาย</button>
              <button class="quick-btn" data-text="เครียดจังเลย">🥹 เครียดจังเลย</button>
            </div>
          </div>

          <!-- คำพูดสุภาพ -->
          <div class="bg-white/80 rounded-2xl border border-pink-100 p-4 shadow-sm">
            <h3 class="flex items-center gap-2 text-sm sm:text-base font-semibold text-pink-600 mb-3">
              <span class="inline-flex items-center justify-center w-7 h-7 rounded-full bg-pink-100">🌸</span>
              คำพูดสุภาพ
            </h3>
            <div class="grid grid-cols-2 gap-2">
              <button class="quick-btn" data-text="ขอบคุณค่ะ">🙏 ขอบคุณค่ะ</button>
              <button class="quick-btn" data-text="ขอโทษค่ะ">😔 ขอโทษค่ะ</button>
              <button class="quick-btn" data-text="ขออนุญาตค่ะ">🙋‍♀️ ขออนุญาตค่ะ</button>
              <button class="quick-btn" data-text="ช่วยหน่อยค่ะ">🫶 ช่วยหน่อยค่ะ</button>
              <button class="quick-btn" data-text="สวัสดีค่ะ">👋 สวัสดีค่ะ</button>
              <button class="quick-btn" data-text="ลาก่อนนะคะ">👋 ลาก่อนนะคะ</button>
            </div>
          </div>

          <!-- ฉุกเฉิน -->
          <div class="bg-white/80 rounded-2xl border border-red-100 p-4 shadow-sm">
            <h3 class="flex items-center gap-2 text-sm sm:text-base font-semibold text-red-600 mb-3">
              <span class="inline-flex items-center justify-center w-7 h-7 rounded-full bg-red-100">🚨</span>
              ฉุกเฉิน
            </h3>
            <div class="grid grid-cols-2 gap-2">
              <button class="quick-btn" data-text="ช่วยด้วยค่ะ">🚨 ช่วยด้วยค่ะ</button>
              <button class="quick-btn" data-text="โทรหาญาติให้หน่อย">🏥 โทรหาญาติให้หน่อย</button>
              <button class="quick-btn" data-text="โทรหาคุณหมอ">📞 โทรหาคุณหมอ</button>
              <button class="quick-btn" data-text="รู้สึกเป็นลม">❗ รู้สึกเป็นลม</button>
              <button class="quick-btn" data-text="เจ็บมากเลยค่ะ">💢 เจ็บมากเลยค่ะ</button>
              <button class="quick-btn" data-text="มีอุบัติเหตุเกิดขึ้น">🔴 มีอุบัติเหตุเกิดขึ้น</button>
            </div>
          </div>

          <!-- โรงเรียน/ห้องเรียน -->
          <div class="bg-white/80 rounded-2xl border border-purple-100 p-4 shadow-sm">
            <h3 class="flex items-center gap-2 text-sm sm:text-base font-semibold text-purple-600 mb-3">
              <span class="inline-flex items-center justify-center w-7 h-7 rounded-full bg-purple-100">🏫</span>
              โรงเรียน / ห้องเรียน
            </h3>
            <div class="grid grid-cols-2 gap-2">
              <button class="quick-btn" data-text="ครูคะ หนูไม่เข้าใจ">✋ ครูคะ หนูไม่เข้าใจ</button>
              <button class="quick-btn" data-text="ขอเวลาทำแบบฝึกเพิ่ม">✍️ ขอเวลาทำแบบฝึกเพิ่ม</button>
              <button class="quick-btn" data-text="ขออนุญาตเข้าห้องน้ำ">🙇‍♀️ ขออนุญาตเข้าห้องน้ำ</button>
              <button class="quick-btn" data-text="ช่วยอธิบายอีกครั้ง">🧑‍🏫 ช่วยอธิบายอีกครั้ง</button>
              <button class="quick-btn" data-text="ขอกระดาษทิชชู่">🧻 ขอกระดาษทิชชู่</button>
              <button class="quick-btn" data-text="ขอเจลล้างมือ">🧼 ขอเจลล้างมือ</button>
            </div>
          </div>
        </section>

        <!-- พื้นที่พิมพ์ข้อความ + แสดงเสียง + ประวัติ -->
        <section class="space-y-4">
          <!-- กล่องพิมพ์ข้อความ -->
          <div class="bg-white/80 rounded-2xl border border-purple-100 p-4 shadow-sm">
            <h3 class="flex items-center gap-2 text-sm sm:text-base font-semibold text-purple-700 mb-2">
              <span class="inline-flex items-center justify-center w-7 h-7 rounded-full bg-purple-100">⌨️</span>
              พิมพ์ข้อความที่ต้องการให้พูด
            </h3>
            <textarea
              id="customText"
              rows="4"
              class="w-full border border-purple-200 rounded-2xl px-4 py-3 text-sm focus:outline-none focus:ring-2 focus:ring-purple-300 focus:border-purple-300 bg-white/90"
              placeholder="พิมพ์ข้อความภาษาไทยหรืออังกฤษที่ต้องการให้ระบบพูดแทนใจ..."
            ></textarea>

            <div class="mt-3 flex flex-wrap gap-2 justify-between items-center">
              <button
                id="generateBtn"
                class="inline-flex items-center gap-2 px-4 py-2 rounded-full text-sm font-medium text-white bg-gradient-to-r from-pink-400 to-purple-400 hover:from-pink-500 hover:to-purple-500 shadow-sm"
              >
                <span>🎧 สร้างไฟล์เสียง</span>
              </button>

              <button
                id="speakDirectBtn"
                class="inline-flex items-center gap-2 px-3 py-2 rounded-full text-xs sm:text-sm font-medium text-purple-600 bg-purple-50 hover:bg-purple-100"
              >
                🔊 พูดข้อความนี้ทันที
              </button>
            </div>
          </div>

          <!-- ผลลัพธ์เสียงล่าสุด -->
          <div class="bg-white/90 rounded-2xl border border-pink-100 p-4 shadow-sm">
            <h3 class="flex items-center gap-2 text-sm sm:text-base font-semibold text-pink-700 mb-2">
              <span class="inline-flex items-center justify-center w-7 h-7 rounded-full bg-pink-100">📂</span>
              เสียงที่สร้างล่าสุด
            </h3>
            <div id="latestAudioContainer" class="space-y-2 text-sm text-gray-600">
              <p class="text-xs text-gray-400">ยังไม่มีการสร้างเสียง</p>
            </div>
          </div>

          <!-- ประวัติการสร้างเสียง -->
          <div class="bg-white/90 rounded-2xl border border-purple-100 p-4 shadow-sm max-h-80 overflow-y-auto">
            <div class="flex items-center justify-between mb-2">
              <h3 class="flex items-center gap-2 text-sm sm:text-base font-semibold text-purple-700">
                <span class="inline-flex items-center justify-center w-7 h-7 rounded-full bg-purple-100">🕒</span>
                ประวัติการสร้างเสียง
              </h3>
              <button
                id="clearHistoryBtn"
                class="inline-flex items-center gap-1 px-3 py-1 rounded-full text-xs font-medium text-red-500 bg-red-50 hover:bg-red-100"
              >
                🧹 ล้างประวัติ
              </button>
            </div>
            <div id="historyList" class="space-y-2 text-xs sm:text-sm text-gray-700">
              <p class="text-xs text-gray-400">ยังไม่มีประวัติการสร้างเสียง</p>
            </div>
          </div>
        </section>
      </main>

      <!-- footer -->
      <footer class="mt-6 pt-4 border-t border-white/70 text-center text-[11px] sm:text-xs text-gray-500">
        พัฒนาโดย <span class="font-semibold text-purple-600">ครูขจรวิทย์ แก้วสุขใส</span>
      </footer>
    </div>
  </div>

  <!-- Toast / Popup แจ้งเตือน -->
  <div id="toast"
       class="fixed bottom-4 left-1/2 -translate-x-1/2 z-50 hidden px-4 py-2 rounded-full text-xs sm:text-sm text-white shadow-lg bg-gray-800/90">
  </div>

  <!-- JS ฟังก์ชันหลัก -->
  <script>
    const TOKEN_KEY = 'botnoiToken';
    const HISTORY_KEY = 'botnoiHistory';

    const tokenInput = document.getElementById('tokenInput');
    const toggleTokenVisibility = document.getElementById('toggleTokenVisibility');
    const saveTokenBtn = document.getElementById('saveTokenBtn');
    const speakerSelect = document.getElementById('speakerSelect');
    const customText = document.getElementById('customText');
    const generateBtn = document.getElementById('generateBtn');
    const speakDirectBtn = document.getElementById('speakDirectBtn');
    const latestAudioContainer = document.getElementById('latestAudioContainer');
    const historyList = document.getElementById('historyList');
    const clearHistoryBtn = document.getElementById('clearHistoryBtn');
    const toast = document.getElementById('toast');

    // โหลด Token และ History จาก localStorage
    function loadInitialData() {
      const storedToken = localStorage.getItem(TOKEN_KEY);
      if (storedToken) {
        tokenInput.value = storedToken;
      }
      renderHistory();
    }

    // แสดง Toast
    function showToast(message, type = 'info') {
      const colorMap = {
        info: 'bg-gray-800/90',
        success: 'bg-emerald-500',
        error: 'bg-red-500',
        warning: 'bg-amber-500',
      };
      toast.textContent = message;
      toast.className = 'fixed bottom-4 left-1/2 -translate-x-1/2 z-50 px-4 py-2 rounded-full text-xs sm:text-sm text-white shadow-lg ' + (colorMap[type] || colorMap.info);
      toast.classList.remove('hidden');

      setTimeout(() => {
        toast.classList.add('hidden');
      }, 2500);
    }

    // บันทึก Token
    saveTokenBtn.addEventListener('click', () => {
      const token = tokenInput.value.trim();
      if (!token) {
        showToast('กรุณากรอก Botnoi API Token ก่อนนะคะ', 'warning');
        return;
      }
      localStorage.setItem(TOKEN_KEY, token);
      showToast('บันทึก Token เรียบร้อยค่ะ', 'success');
    });

    // แสดง / ซ่อน Token
    toggleTokenVisibility.addEventListener('click', () => {
      if (tokenInput.type === 'password') {
        tokenInput.type = 'text';
        toggleTokenVisibility.textContent = '🙈 ซ่อน';
      } else {
        tokenInput.type = 'password';
        toggleTokenVisibility.textContent = '👁 แสดง';
      }
    });

    // อ่านประวัติจาก localStorage
    function getHistory() {
      try {
        const raw = localStorage.getItem(HISTORY_KEY);
        if (!raw) return [];
        return JSON.parse(raw) || [];
      } catch (e) {
        console.error('Error parsing history', e);
        return [];
      }
    }

    // บันทึกประวัติใน localStorage
    function saveHistory(history) {
      localStorage.setItem(HISTORY_KEY, JSON.stringify(history));
    }

    // แสดงประวัติ
    function renderHistory() {
      const history = getHistory();
      if (!history.length) {
        historyList.innerHTML = '<p class="text-xs text-gray-400">ยังไม่มีประวัติการสร้างเสียง</p>';
        return;
      }

      historyList.innerHTML = '';
      history.slice().reverse().forEach((item, index) => {
        const div = document.createElement('div');
        div.className = 'border border-purple-100 rounded-xl p-2.5 bg-white/70 flex flex-col gap-1';

        const time = new Date(item.timestamp).toLocaleString('th-TH', {
          dateStyle: 'short',
          timeStyle: 'short'
        });

        div.innerHTML = `
          <div class="flex items-center justify-between gap-2">
            <span class="text-[11px] text-gray-400">#${history.length - index}</span>
            <span class="text-[11px] text-gray-400">${time}</span>
          </div>
          <div class="text-xs text-gray-700 line-clamp-2">
            <strong>ข้อความ:</strong> ${item.text}
          </div>
          <div class="flex items-center justify-between mt-1">
            <span class="text-[11px] text-purple-500">เสียง: ${item.speakerName || item.speaker}</span>
            <div class="flex gap-1">
              <button class="px-2 py-1 rounded-full text-[11px] bg-purple-50 text-purple-600 hover:bg-purple-100 play-history-btn" data-url="${item.audio_url}">
                ▶ เล่น
              </button>
              <a href="${item.audio_url}" download class="px-2 py-1 rounded-full text-[11px] bg-pink-50 text-pink-600 hover:bg-pink-100">
                ⬇ ดาวน์โหลด
              </a>
            </div>
          </div>
        `;
        historyList.appendChild(div);
      });

      // ผูก event ปุ่มเล่นในประวัติ
      const playBtns = historyList.querySelectorAll('.play-history-btn');
      playBtns.forEach(btn => {
        btn.addEventListener('click', () => {
          const url = btn.getAttribute('data-url');
          if (!url) return;
          const audio = new Audio(url);
          audio.play().catch(err => {
            console.error(err);
            showToast('ไม่สามารถเล่นเสียงได้', 'error');
          });
        });
      });
    }

    // เคลียร์ประวัติ
    clearHistoryBtn.addEventListener('click', () => {
      if (!confirm('ต้องการล้างประวัติการสร้างเสียงทั้งหมดหรือไม่?')) return;
      localStorage.removeItem(HISTORY_KEY);
      renderHistory();
      showToast('ล้างประวัติเรียบร้อยแล้ว', 'success');
    });

    // ฟังก์ชันเรียก API Botnoi
    async function callBotnoiAPI(text) {
      const token = localStorage.getItem(TOKEN_KEY) || tokenInput.value.trim();
      if (!token) {
        showToast('กรุณาตั้งค่า Botnoi API Token ก่อนใช้งานค่ะ', 'error');
        throw new Error('No token');
      }

      const speaker = speakerSelect.value || '1';
      const lang = speaker === '9' ? 'en' : 'th';

      const body = {
        text: text,
        speaker: speaker,
        volume: 1,
        speed: 1,
        type_media: "m4a",
        save_file: true,
        language: lang
      };

      const res = await fetch('https://api-voice.botnoi.ai/openapi/v1/generate_audio', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
          'Botnoi-Token': token
        },
        body: JSON.stringify(body)
      });

      if (!res.ok) {
        const msg = `API Error: ${res.status}`;
        showToast(msg, 'error');
        throw new Error(msg);
      }

      const data = await res.json();
      if (!data.audio_url) {
        showToast('ไม่พบ audio_url ในผลลัพธ์', 'error');
        throw new Error('No audio_url in response');
      }

      return { audioUrl: data.audio_url, speaker, language: lang };
    }

    // map speaker code → ชื่อเสียง
    function getSpeakerName(code) {
      const map = {
        '1': 'เอวา (th)',
        '2': 'โบ (th)',
        '3': 'คุณงาม (th)',
        '4': 'แม็กซ์ (th)',
        '5': 'อลัน (th)',
        '6': 'ไซเรน (th)',
        '7': 'อลิสา (th)',
        '8': 'เลโอ (th)',
        '9': 'นาเดียร์ (en)',
      };
      return map[code] || code;
    }

    // อัปเดตส่วนแสดงเสียงล่าสุด
    function updateLatestAudio(text, audioUrl, speakerCode) {
      const speakerName = getSpeakerName(speakerCode);
      latestAudioContainer.innerHTML = `
        <p class="text-xs text-gray-500 mb-1">
          ข้อความล่าสุด: <span class="text-gray-700">${text}</span>
        </p>
        <p class="text-xs text-purple-500 mb-1">เสียง: ${speakerName}</p>
        <audio controls class="w-full mt-1">
          <source src="${audioUrl}" type="audio/mp4" />
          เบราว์เซอร์ของคุณไม่รองรับการเล่นเสียง
        </audio>
        <div class="mt-2 flex justify-end">
          <a href="${audioUrl}" download class="px-3 py-1 rounded-full text-xs bg-pink-50 text-pink-600 hover:bg-pink-100 inline-flex items-center gap-1">
            ⬇ ดาวน์โหลดไฟล์เสียง
          </a>
        </div>
      `;
    }

    // เพิ่มประวัติใหม่
    function addToHistory(text, audioUrl, speakerCode) {
      const history = getHistory();
      history.push({
        text,
        audio_url: audioUrl,
        speaker: speakerCode,
        speakerName: getSpeakerName(speakerCode),
        timestamp: new Date().toISOString(),
      });
      saveHistory(history);
      renderHistory();
    }

    // ปุ่ม "สร้างไฟล์เสียง"
    generateBtn.addEventListener('click', async () => {
      const text = customText.value.trim();
      if (!text) {
        showToast('กรุณาพิมพ์ข้อความก่อนสร้างเสียงนะคะ', 'warning');
        return;
      }
      try {
        showToast('กำลังสร้างไฟล์เสียง...', 'info');
        const { audioUrl, speaker } = await callBotnoiAPI(text);
        updateLatestAudio(text, audioUrl, speaker);
        addToHistory(text, audioUrl, speaker);
        showToast('สร้างไฟล์เสียงสำเร็จแล้วค่ะ', 'success');
      } catch (err) {
        console.error(err);
      }
    });

    // ปุ่ม "พูดข้อความนี้ทันที"
    speakDirectBtn.addEventListener('click', async () => {
      const text = customText.value.trim();
      if (!text) {
        showToast('กรุณาพิมพ์ข้อความก่อนนะคะ', 'warning');
        return;
      }
      try {
        showToast('กำลังสั่งให้พูด...', 'info');
        const { audioUrl, speaker } = await callBotnoiAPI(text);
        const audio = new Audio(audioUrl);
        audio.play();
        updateLatestAudio(text, audioUrl, speaker);
        addToHistory(text, audioUrl, speaker);
        showToast('กำลังพูดข้อความของคุณค่ะ', 'success');
      } catch (err) {
        console.error(err);
      }
    });

    // ฟังก์ชัน speak(text) สำหรับปุ่มข้อความลัด
    async function speak(text) {
      customText.value = text;
      try {
        showToast('กำลังสั่งให้พูด...', 'info');
        const { audioUrl, speaker } = await callBotnoiAPI(text);
        const audio = new Audio(audioUrl);
        audio.play();
        updateLatestAudio(text, audioUrl, speaker);
        addToHistory(text, audioUrl, speaker);
        showToast('กำลังพูดข้อความของคุณค่ะ', 'success');
      } catch (err) {
        console.error(err);
      }
    }

    // ผูก event ให้ปุ่ม quick-btn ทั้งหมด
    function bindQuickButtons() {
      const quickButtons = document.querySelectorAll('.quick-btn');
      quickButtons.forEach(btn => {
        btn.classList.add(
          'inline-flex', 'items-center', 'justify-center',
          'px-3', 'py-2', 'rounded-full',
          'bg-gradient-to-r', 'from-pink-50', 'to-purple-50',
          'hover:from-pink-100', 'hover:to-purple-100',
          'border', 'border-pink-100',
          'text-[11px]', 'sm:text-xs', 'text-gray-700',
          'shadow-sm'
        );
        btn.addEventListener('click', () => {
          const text = btn.getAttribute('data-text') || btn.textContent.trim();
          speak(text);
        });
      });
    }

    // เริ่มต้น
    document.addEventListener('DOMContentLoaded', () => {
      loadInitialData();
      bindQuickButtons();
    });
  </script>
</body>
</html>
# Your-Voice-Matters-
