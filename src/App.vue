<template>
  <header>
    <h1>電力看得見，碳排降得下</h1>
  </header>

  <div class="tab-container">
    <div class="tabs">
      <button class="tab-button" :class="{ active: activeTab === 'home' }" @click="changeTab('home')">首頁</button>
      <button class="tab-button" :class="{ active: activeTab === 'intro' }" @click="changeTab('intro')">基礎介紹</button>
      <button class="tab-button" :class="{ active: activeTab === 'material' }" @click="changeTab('material')">教材介紹</button>
      <button class="tab-button" :class="{ active: activeTab === 'simulation' }" @click="changeTab('simulation')">互動模擬</button>
      <button class="tab-button" :class="{ active: activeTab === 'dashboard' }" @click="changeTab('dashboard')">能源戰情室</button>
    </div>

    <div v-if="activeTab === 'home'" class="tab-content-vue">
      <div class="home-hero">
        <div>
          <h2 style="font-size: 2.8rem; margin-bottom: 0.8rem; border:none; color: white;">智慧能源管理與培訓</h2>
          <p style="font-size: 1.3rem; opacity: 0.95;">數據連結行動，透過 VR 實驗室預見減碳成果</p>
        </div>
      </div>
      
      <div class="grid-2">
        <div class="info-card">
          <h3 style="color:var(--accent-blue);"><i class="fas fa-link"></i> 數據與人的橋樑</h3>
          <p>我們發現智慧電表雖然擁有強大的數據基礎，但缺乏一個與使用者對話的橋樑。透過本系統，複雜的電力參數將轉化為直觀的視覺反饋。</p>
        </div>
        <div class="info-card" style="background: #f1f5f9;">
          <h3 style="color:var(--secondary-color);"><i class="fas fa-shield-alt"></i> 數位轉型標配</h3>
          <p>應對國際供應鏈稽核，自動化能耗監控不再是選項，而是企業維持國際競爭力的「標配」。</p>
        </div>
      </div>

      <div style="margin-top: 4rem;">
        <h2 style="text-align:center;"><i class="fas fa-lightbulb"></i> 安裝智慧電表，您可以知道什麼？</h2>
        <div class="grid-2" style="margin-top: 2rem;">
          <div class="flip-card">
            <div class="flip-card-inner">
              <div class="flip-card-front">
                <h4>看見隱形消耗</h4>
                <p>傳統電表要等一個月後的帳單，智慧電表讓您即時看到「現在」用了多少電，精準抓出待機電力浪費。</p>
              </div>
              <div class="flip-card-back">
                <h4 style="color: var(--accent-blue); margin-top: 0;"><i class="fas fa-search-dollar"></i> 實際案例</h4>
                <p>發現辦公區印表機與飲水機在下班後依然消耗大量待機電力，透過加裝定時斷電，每月可輕鬆節省數千元無效電費。</p>
              </div>
            </div>
          </div>
          <div class="flip-card">
            <div class="flip-card-inner">
              <div class="flip-card-front">
                <h4>掌握尖離峰成本</h4>
                <p>精準計算工廠尖峰與離峰時段的電力費用，協助管理者將高耗電排程轉移至離峰時段，有效降低整體營運成本。</p>
              </div>
              <div class="flip-card-back">
                <h4 style="color: var(--accent-blue); margin-top: 0;"><i class="fas fa-chart-line"></i> 實際案例</h4>
                <p>將高耗能的烘烤爐排程移至半夜的離峰時段運作，避開尖峰高昂費率，工廠單月電費支出成功降低了 20% 以上。</p>
              </div>
            </div>
          </div>
          <div class="flip-card">
            <div class="flip-card-inner">
              <div class="flip-card-front">
                <h4>智慧設備連動控制</h4>
                <p>具備強大的擴充整合能力，可與冷氣空調、溫度計、環境檢測器等設備連動，實現自動化的能源與環境管理。</p>
              </div>
              <div class="flip-card-back">
                <h4 style="color: var(--accent-blue); margin-top: 0;"><i class="fas fa-robot"></i> 實際案例</h4>
                <p>當環境感測器偵測到溫度超過 28 度且有人員在場時，系統自動啟動冷氣並鎖定於適當溫度，達到節能與舒適雙贏。</p>
              </div>
            </div>
          </div>
          <div class="flip-card">
            <div class="flip-card-inner">
              <div class="flip-card-front">
                <h4>碳足跡「精準折算」</h4>
                <p>直接乘以當年「電力排碳係數」，算出每一小時、每一天產生了多少碳排放。</p>
              </div>
              <div class="flip-card-back">
                <h4 style="color: var(--accent-blue); margin-top: 0;"><i class="fas fa-leaf"></i> 實際案例</h4>
                <p>月底一鍵產出報表，系統自動將本月耗電量換算為約 4.95 噸碳排放 (CO2e)，可直接作為企業 ESG 綠色報告數據。</p>
              </div>
            </div>
          </div>
          <div class="flip-card">
            <div class="flip-card-inner">
              <div class="flip-card-front">
                <h4>多迴路細節監控</h4>
                <p>單獨知道冷氣、照明、電腦設備各別用了多少電，而非只有總表的模糊數字。</p>
              </div>
              <div class="flip-card-back">
                <h4 style="color: var(--accent-blue); margin-top: 0;"><i class="fas fa-sitemap"></i> 實際案例</h4>
                <p>打破「總電費很貴但不知哪裡貴」的盲點，精確揪出「廠房 B 的舊型空調系統」佔了總用電 40%，以進行針對性汰換。</p>
              </div>
            </div>
          </div>
          <div class="flip-card">
            <div class="flip-card-inner">
              <div class="flip-card-front">
                <h4>專業級電力參數面板</h4>
                <div class="param-grid">
                  <div class="param-tag"><span>電壓/電流</span>V / A</div>
                  <div class="param-tag"><span>有效/無效功率</span>kW / kVAR</div>
                  <div class="param-tag"><span>視在功率/因數</span>kVA / PF</div>
                  <div class="param-tag"><span>系統頻率</span>Hz</div>
                </div>
              </div>
              <div class="flip-card-back">
                <h4 style="color: var(--accent-blue); margin-top: 0;"><i class="fas fa-bolt"></i> 實際案例</h4>
                <p>監控功率因數 (PF)。若 PF 低於標準時系統自動發出預警通知，提醒工程師檢修，避免因此被加收無效電力費用。</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div v-if="activeTab === 'intro'" class="tab-content-vue">
      <div class="sub-nav">
        <button class="sub-btn" :class="{ active: activeSubTab === 'carbon' }" @click="changeSubTab('carbon')">🍀 什麼是碳盤查？</button>
        <button class="sub-btn" :class="{ active: activeSubTab === 'meter' }" @click="changeSubTab('meter')">📟 智慧電表介紹</button>
      </div>

      <div v-if="activeSubTab === 'carbon'" class="sub-content-vue">
        <h2>企業綠色轉型的第一關：碳盤查</h2>
        <p>碳盤查是指企業針對營運活動產生的溫室氣體（GHG）進行清查與計算。通常依照 ISO 14064-1 分為：</p>
        <div class="grid-3" style="margin-top: 1.5rem;">
          <div class="info-card" style="border-top: 6px solid #3b82f6;"><b>範疇一：直接排放</b><br><small>工廠煙囪、公司配車、冷媒洩漏。</small></div>
          <div class="info-card" style="border-top: 6px solid #10b981;"><b>範疇二：能源間接</b><br><small>外購電力、蒸汽 or 熱能。</small></div>
          <div class="info-card" style="border-top: 6px solid #f59e0b;"><b>範疇三：其他間接</b><br><small>供應商排碳、通勤、運輸。</small></div>
        </div>

        <div style="margin-top: 2rem; background: #f8fafc; padding: 1.5rem; border-radius: 12px; border-left: 5px solid var(--accent-blue);">
          <h3 style="margin-top: 0; color: var(--primary-dark);"><i class="fas fa-list-ul"></i> 常見的碳排放來源例子</h3>
          <p style="margin-bottom: 0.5rem;">在進入實際計算之前，讓我們先看看生活中與企業裡有哪些常見的碳排行為：</p>
          <ul style="line-height: 1.8; margin-bottom: 0; color: var(--secondary-color);">
            <li><strong>電力消耗：</strong> 辦公室的冷氣、照明，工廠的生產機台運作（屬於範疇二）。</li>
            <li><strong>燃油燃燒：</strong> 公司業務車燃燒汽油、發電機燃燒柴油（屬於範疇一）。</li>
            <li><strong>製程與逸散：</strong> 冷氣冷媒外洩、化學工業或水泥業製程中直接釋放的溫室氣體（屬於範疇一）。</li>
            <li><strong>供應鏈與員工活動：</strong> 員工每天搭車通勤、上下游物流運送、商務出差搭飛機（屬於範疇三）。</li>
          </ul>
        </div>

        <div class="vue-calculator-box">
          <h3>📟 企業實時碳足跡折算器（體驗 Vue 的威力）</h3>
          <p style="color: #64748b; font-size: 0.95rem;">試著輸入預估用電量，系統將根據你網頁設定的 <strong style="color:var(--success)">0.495</strong> 電力排碳係數自動折算：</p>
          <div style="margin: 1.5rem 0;">
            <label style="font-weight: bold; display: block; margin-bottom: 0.5rem;">輸入當月用電度數 (kWh)：</label>
            <input type="number" v-model.number="userKwh" placeholder="請輸入電度數，例如 10000" class="calc-input" />
          </div>
          <div class="calc-result-grid" v-if="userKwh > 0">
            <div class="res-card">
              <span>折算碳排放量</span>
              <strong>{{ computedCarbonKg }} 公斤 CO₂e</strong>
              <small>約 {{ computedCarbonTon }} 公噸</small>
            </div>
            <div class="res-card" style="border-left-color: #3b82f6;">
              <span>相當於地球吸收量</span>
              <strong>約幫地球種植了 {{ computedTrees }} 棵大樹</strong>
              <small>（以每棵樹年吸碳 12kg 計算）</small>
            </div>
          </div>
        </div>

        <h3 style="margin-top:2.5rem;">🛠️ 執行流程</h3>
        <div class="process-step"><div class="step-num">1</div><div><b>邊界設定：</b>決定清查整間公司 or 特定廠區。</div></div>
        <div class="process-step"><div class="step-num">2</div><div><b>排放源鑑別：</b>找出所有排碳設備。</div></div>
        <div class="process-step"><div class="step-num">3</div><div><b>蒐集計算：</b>活動數據 × 係數 = 碳排放量。</div></div>
        <div class="process-step"><div class="step-num">4</div><div><b>外部查證：</b>委託公正第三方機構（如 SGS）核發證書。</div></div>
        <div style="background: #fff5f5; border-left: 5px solid var(--danger); padding: 1.5rem; border-radius: 8px; margin-top: 1rem;">
          <b>不做會發生什麼事？</b> 訂單流失（供應鏈踢除）、高額罰款、標籤為不環保企業。
        </div>
      </div>

      <div v-if="activeSubTab === 'meter'" class="sub-content-vue">
        <div style="text-align: center; margin-bottom: 3rem;">
          <h2 style="border:none;">從數據收集到可視化：硬體運作流程</h2>
          <p style="max-width: 800px; margin: 0.5rem auto 0; color: var(--secondary-color);">
            一套完整的智慧能源監控系統，是由多個關鍵硬體依序組合而成。以下將依據資料的流動順序，為您解析各個元件所扮演的角色：
          </p>
        </div>
        <div class="grid-2" style="align-items: center;">
          <div class="image-box">
            <img src="https://yulun7030.github.io/0610/p3.jpg" alt="智慧監控系統硬體元件" style="border-radius: 12px;">
          </div>
          <div>
            <div class="process-step">
              <div class="step-num">1</div>
              <div><b>電力數據量測 (三相/單相電表)</b><br>依據用電設備的規模，安裝對應的 SDT 三相或 SDM 單相電子式電表。它們是數據收集的起點，精準量測原始電力數據。</div>
            </div>
            <div class="process-step">
              <div class="step-num">2</div>
              <div><b>數據集中與遠傳 (通訊伺服器)</b><br>電表量測到的數據，會傳輸至 HF2211 這類的「通訊中繼站」，透過 WiFi 或有線網路穩定地傳送到後端系統。</div>
            </div>
            <div class="process-step">
              <div class="step-num">3</div>
              <div><b>數據整合與可視化 (HMI/雲端平台)</b><br>在 HMI 管理面板或雲端平台上，數據被整合並以圖表化呈現，讓管理者能一目了然地看到機台的即時用電、產量與花費。</div>
            </div>
            <div class="process-step" style="background: #f1f5f9;">
              <div class="step-num" style="background: var(--secondary-color);"><i class="fas fa-thermometer-half"></i></div>
              <div><b>(選配) 環境因子監控</b><br>可整合環境監測面板，同步監控配電箱的溫度、濕度等，提早發現因環境過熱可能導致的電力風險。</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div v-if="activeTab === 'material'" class="tab-content-vue">
      <div class="motivation-expanded">
        <h2 style="color: var(--primary-dark); border:none;"><i class="fas fa-lightbulb"></i> 開發動機：跨越數據的「最後一哩路」</h2>
        <p>智慧電表雖然擁有強大的數據基礎，但往往缺乏與使用者對話的橋樑。對於管理者而言，電表數據僅僅是冷冰冰的數字；對於技術人員而言，實體安裝具備高壓電風險。</p>
        <p>藉由 <b>VR 模擬系統</b>，我們創造了一個「虛擬實驗室」。使用者能嘗試不同的用電情境（如：更換節能電器、調整負載），達成<b>「先模擬、後行動」</b>的減碳策略。這不僅是培訓，更是決策的視覺化工具。</p>
      </div>
      <h3 style="text-align:center; font-size: 1.8rem; margin-bottom: 2rem;">核心教學目標</h3>
      <div class="grid-3">
        <div class="info-card" style="text-align: center;">
          <i class="fas fa-map-marked-alt" style="font-size: 2.5rem; color: var(--accent-blue); margin-bottom: 1.2rem;"></i>
          <h4>1. 環境理解與設定</h4>
          <div style="text-align: left;">
            <div class="objective-item"><i class="fas fa-check"></i> 識別電表正確安裝位置</div>
            <div class="objective-item"><i class="fas fa-check"></i> 掌握單/三相接線邏輯</div>
            <div class="objective-item"><i class="fas fa-check"></i> 熟悉通訊參數與後台配置</div>
          </div>
        </div>
        <div class="info-card" style="text-align: center;">
          <i class="fas fa-tools" style="font-size: 2.5rem; color: var(--accent-blue); margin-bottom: 1.2rem;"></i>
          <h4>2. 獨立作業能力</h4>
          <div style="text-align: left;">
            <div class="objective-item"><i class="fas fa-check"></i> 獨立完成 CT 比流器掛載</div>
            <div class="objective-item"><i class="fas fa-check"></i> 正確操作斷路器與配線</div>
            <div class="objective-item"><i class="fas fa-check"></i> 完成數據傳輸檢測</div>
          </div>
        </div>
        <div class="info-card" style="text-align: center;">
          <i class="fas fa-chart-line" style="font-size: 2.5rem; color: var(--accent-blue); margin-bottom: 1.2rem;"></i>
          <h4>3. 數據解讀分析</h4>
          <div style="text-align: left;">
            <div class="objective-item"><i class="fas fa-check"></i> 解釋 V, A, kW, PF 意義</div>
            <div class="objective-item"><i class="fas fa-check"></i> 判讀波形並找出異常</div>
            <div class="objective-item"><i class="fas fa-check"></i> 轉化數據為減碳建議</div>
          </div>
        </div>
      </div>
    </div>

    <div v-if="activeTab === 'simulation'" class="tab-content-vue">
      <h2 style="text-align: center;">VR 虛擬安裝實驗室</h2>
      <div style="background: #e0f2fe; border-left: 6px solid #0284c7; padding: 1.8rem; border-radius: 8px; margin-bottom: 2rem;">
        <h3 style="margin-top: 0; color: #0369a1;"><i class="fas fa-bullhorn"></i> 任務開場白：尋找隱藏的智慧電表</h3>
        <p style="margin-bottom: 0.8rem; font-size: 1.1rem;">這是一家已經全面導入「智慧電表」的現代化公司。您的任務是：</p>
        <ul style="margin-bottom: 1.5rem; color: #0f172a; font-size: 1.05rem; line-height: 2;">
          <li><strong>任務一：</strong>請在下方的 360 度環景畫面中，拖曳視角並找出所有的互動圖示 (Icon) 位置。</li>
          <li><strong>任務二：</strong>請找出「智慧電表」到底安裝在哪裡？當您按下智慧電表圖示時，將會解鎖一道隨堂測驗！</li>
        </ul>
      </div>

      <div style="position: relative; width: 100%; height: 650px; border-radius: 20px; overflow: hidden; border: 1px solid #e2e8f0;">
        <button @click="openQuizHandler" class="sub-btn active pulse-btn" style="position: absolute; bottom: 30px; right: 30px; z-index: 10; font-size: 1.1rem; padding: 0.8rem 1.8rem; border-radius: 50px; box-shadow: 0 5px 15px rgba(0,0,0,0.4);">
          <i class="fas fa-play-circle"></i> 進入隨堂測驗
        </button>
        <iframe src="https://tour.panoee.net/6a0d1b8bc24fa576842dc893?v=updated" width="100%" height="100%" frameborder="0" allow="xr-spatial-tracking; gyroscope; accelerometer; fullscreen; autoplay;"></iframe>
      </div>
    </div>

    <div v-if="activeTab === 'dashboard'" class="tab-content-vue">
      <div class="energy-dashboard" style="margin-top: 0;">
        <h3 style="margin-top: 0;">⚡ 台灣即時能源發電監測戰情室</h3>
        <p class="update-tag">數據更新時間：{{ updateTime }}</p>

        <!-- 模塊 2: 動態跑馬燈：即時能耗警報 -->
        <div class="alert-ticker">
          <h4 style="margin-top: 0; margin-bottom: 8px; color: #e11d48;"><i class="fas fa-bell"></i> 廠區即時預警跑馬燈</h4>
          <transition-group name="list" tag="div" style="position: relative;">
            <div v-for="alert in alerts" :key="alert.id" class="alert-item">
              {{ alert.type }} {{ alert.time }} {{ alert.msg }}
            </div>
          </transition-group>
        </div>

        <div class="grid-2" style="align-items: center; margin-top: 1.5rem;">
          <div id="power-pie-chart" style="width: 100%; height: 350px;"></div>

          <div class="energy-analysis-card">
            <h4>💡 今日電網碳足跡評估</h4>
            <p class="status-text">{{ greenEnergyStatus }}</p>
            
            <div class="data-row">
              <span>🍀 再生綠能比例：</span>
              <strong>{{ powerData.green }} %</strong>
            </div>
            <div class="data-row">
              <span>🔥 火力發電比例：</span>
              <strong>{{ (powerData.coal + powerData.gas).toFixed(1) }} %</strong>
            </div>
            <small style="color: #94a3b8; display:block; margin-top: 1rem;">
              *註：本看板實時讀取台灣電力公司發電數據。當再生能源發電比例越高，企業使用範疇二的能源間接排放「實際碳強度」就越低。
            </small>
          </div>
        </div>

        <!-- 模塊 1: 歷史能耗趨勢圖 -->
        <div style="background: #f8fafc; padding: 1.5rem; border-radius: 12px; border: 1px solid #e2e8f0; margin-top: 1.5rem;">
          <div id="power-line-chart" style="width: 100%; height: 350px;"></div>
        </div>

        <!-- 模塊 3: 環境因子監測 -->
        <div class="grid-2" style="margin-top: 1.5rem; gap: 1.5rem;">
          <div style="background: #f8fafc; padding: 1.5rem; border-radius: 12px; border: 1px solid #e2e8f0; text-align: center;">
            <h4 style="margin-top:0; color: var(--secondary-color);"><i class="fas fa-temperature-high"></i> 戶外環境溫度 (新北淡水)</h4>
            <div id="temp-gauge" style="width: 100%; height: 250px;"></div>
          </div>
          <div style="background: #f8fafc; padding: 1.5rem; border-radius: 12px; border: 1px solid #e2e8f0; text-align: center;">
            <h4 style="margin-top:0; color: var(--secondary-color);"><i class="fas fa-tint"></i> 配電箱預估濕度</h4>
            <div id="hum-gauge" style="width: 100%; height: 250px;"></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="modal-overlay" :class="{ show: showQuizModal }">
    <div class="modal-content">
      <button class="close-btn" @click="showQuizModal = false">&times;</button>
      <h3 style="color: var(--accent-blue); margin-top: 0; font-size: 1.5rem;"><i class="fas fa-question-circle"></i> 隨堂測驗解鎖！</h3>
      
      <div v-if="currentQuestion === 1">
        <p class="quiz-title">1/4. 對於小型企業而言，導入「智慧電表 Slim 系列」最核心的商業價值與應用方向是什麼？</p>
        <div class="quiz-options">
          <button class="quiz-btn" :class="getBtnClass(1, 'A')" :disabled="quizAnswered[1]" @click="submitAnswer(1, 'A', false)">A. 單純為了符合法規，避免被政府開罰</button>
          <button class="quiz-btn" :class="getBtnClass(1, 'B')" :disabled="quizAnswered[1]" @click="submitAnswer(1, 'B', true)">B. 為能源管理、設備監控與節能決策提供可靠的數據基礎</button>
          <button class="quiz-btn" :class="getBtnClass(1, 'C')" :disabled="quizAnswered[1]" @click="submitAnswer(1, 'C', false)">C. 完全取代廠房內的所有人工巡檢</button>
        </div>
        <div class="quiz-feedback" v-html="quizFeedback[1]"></div>
        <button v-if="quizAnswered[1]" class="sub-btn" style="margin-top: 1rem; width:100%;" @click="currentQuestion = 2">下一題 <i class="fas fa-arrow-right"></i></button>
      </div>

      <div v-if="currentQuestion === 2">
        <p class="quiz-title">2/4. 當公司主管計畫評估工廠內部「大型機台」的能源消耗，並透過大數據分析來優化能源使用、降低營運成本時，應該搭配「智慧製造數據採集網關」的哪一個系統應用場景？</p>
        <div class="quiz-options">
          <button class="quiz-btn" :class="getBtnClass(2, 'A')" :disabled="quizAnswered[2]" @click="submitAnswer(2, 'A', false)">A. CRM 客戶關係管理系統</button>
          <button class="quiz-btn" :class="getBtnClass(2, 'B')" :disabled="quizAnswered[2]" @click="submitAnswer(2, 'B', false)">B. HRM 人力資源管理系統</button>
          <button class="quiz-btn" :class="getBtnClass(2, 'C')" :disabled="quizAnswered[2]" @click="submitAnswer(2, 'C', true)">C. EMS 能源管理系統</button>
        </div>
        <div class="quiz-feedback" v-html="quizFeedback[2]"></div>
        <button v-if="quizAnswered[2]" class="sub-btn" style="margin-top: 1rem; width:100%;" @click="currentQuestion = 3">下一題 <i class="fas fa-arrow-right"></i></button>
      </div>

      <div v-if="currentQuestion === 3">
        <p class="quiz-title">3/4. 若小型企業廠區內有大電流（如 100A 或 200A）的三相用電設備需要進行電力監測，主管在採購智慧電表時應注意什麼規格配置？</p>
        <div class="quiz-options">
          <button class="quiz-btn" :class="getBtnClass(3, 'A')" :disabled="quizAnswered[3]" @click="submitAnswer(3, 'A', false)">A. 選擇單相智慧電表即可</button>
          <button class="quiz-btn" :class="getBtnClass(3, 'B')" :disabled="quizAnswered[3]" @click="submitAnswer(3, 'B', true)">B. 選擇三相智慧電表，並透過電壓互感器雙比來支援 100A 及 200A 的電流檢測</button>
          <button class="quiz-btn" :class="getBtnClass(3, 'C')" :disabled="quizAnswered[3]" @click="submitAnswer(3, 'C', false)">C. 選擇不需連接任何互感器的直接式智慧電表</button>
        </div>
        <div class="quiz-feedback" v-html="quizFeedback[3]"></div>
        <button v-if="quizAnswered[3]" class="sub-btn" style="margin-top: 1rem; width:100%;" @click="currentQuestion = 4">下一題 <i class="fas fa-arrow-right"></i></button>
      </div>

      <div v-if="currentQuestion === 4">
        <p class="quiz-title">4/4. 小型企業在安裝智慧電表時，往往擔心施工繁複、佔用過多空間。根據產品規格，這款智慧電表採用何種安裝方式，有利於節省工廠配電箱的空間與安裝時間？</p>
        <div class="quiz-options">
          <button class="quiz-btn" :class="getBtnClass(4, 'A')" :disabled="quizAnswered[4]" @click="submitAnswer(4, 'A', false)">A. 壁掛式安裝</button>
          <button class="quiz-btn" :class="getBtnClass(4, 'B')" :disabled="quizAnswered[4]" @click="submitAnswer(4, 'B', false)">B. 鎖螺絲固定安裝</button>
          <button class="quiz-btn" :class="getBtnClass(4, 'C')" :disabled="quizAnswered[4]" @click="submitAnswer(4, 'C', true)">C. DIN導軌安裝</button>
        </div>
        <div class="quiz-feedback" v-html="quizFeedback[4]"></div>
        <button v-if="quizAnswered[4]" class="sub-btn" style="margin-top: 1rem; width:100%;" @click="currentQuestion = 5">查看結果 <i class="fas fa-arrow-right"></i></button>
      </div>

      <div v-if="currentQuestion === 5" style="text-align: center; padding: 2rem 0 1rem 0;">
        <i class="fas fa-award" style="font-size: 5rem; color: #f59e0b; margin-bottom: 1.5rem;"></i>
        <h3 style="font-size: 1.8rem; color: var(--primary-dark); margin-top: 0; margin-bottom: 1rem;">恭喜過關！</h3>
        <p style="font-size: 1.1rem; color: var(--secondary-color); margin-bottom: 2rem; line-height: 1.8;">
          您已成功完成全部 4 道隨堂測驗！<br>
          相信您對智慧電表的應用與價值已經有更深刻的認識了。
        </p>
        <button class="sub-btn active" style="width:100%; font-size: 1.1rem; padding: 1rem;" @click="showQuizModal = false">完成並關閉 <i class="fas fa-check"></i></button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted, computed, nextTick } from 'vue'
import * as echarts from 'echarts'

// --- 狀態管理與路由控制 ---
const activeTab = ref('home')        
const activeSubTab = ref('carbon')    
const showQuizModal = ref(false)     
const currentQuestion = ref(1)       

// --- 碳排計算機變數 ---
const userKwh = ref(0)
const carbonCoefficient = 0.495      

const computedCarbonKg = computed(() => {
  if (!userKwh.value || userKwh.value < 0) return 0
  return parseFloat((userKwh.value * carbonCoefficient).toFixed(2))
})
const computedCarbonTon = computed(() => {
  return (computedCarbonKg.value / 1000).toFixed(2)
})
const computedTrees = computed(() => {
  if (computedCarbonKg.value === 0) return 0
  return Math.round(computedCarbonKg.value / 12)
})

// --- 隨堂測驗專用狀態群 ---
const quizAnswered = ref({ 1: false, 2: false, 3: false, 4: false })
const quizSelected = ref({ 1: '', 2: '', 3: '', 4: '' })
const quizFeedback = ref({ 1: '', 2: '', 3: '', 4: '' })
const correctAnswers = { 1: 'B', 2: 'C', 3: 'B', 4: 'C' }

function openQuizHandler() {
  showQuizModal.value = true
  currentQuestion.value = 1
  quizAnswered.value = { 1: false, 2: false, 3: false, 4: false }
  quizSelected.value = { 1: '', 2: '', 3: '', 4: '' }
  quizFeedback.value = { 1: '', 2: '', 3: '', 4: '' }
}

function submitAnswer(qNum, option, isCorrect) {
  quizAnswered.value[qNum] = true
  quizSelected.value[qNum] = option
  if (isCorrect) {
    quizFeedback.value[qNum] = '<span style="color: #10b981;"><i class="fas fa-check-circle"></i> 答對了！</span>'
  } else {
    quizFeedback.value[qNum] = '<span style="color: #e53e3e;"><i class="fas fa-times-circle"></i> 答錯囉！</span>'
  }
}

function getBtnClass(qNum, option) {
  if (!quizAnswered.value[qNum]) return ''
  const correctOpt = correctAnswers[qNum]
  if (option === correctOpt) return 'correct'
  if (quizSelected.value[qNum] === option && option !== correctOpt) return 'wrong'
  return ''
}

// --- 💡 能源 API 串接與 ECharts 圓餅圖邏輯 ---
const powerData = ref({
  coal: 40.0,       
  gas: 35.0,        
  nuclear: 8.0,     
  green: 12.0,      
  others: 5.0
})
const updateTime = ref('連線中...')
const isLoading = ref(true)

// 跑馬燈警報變數
const alerts = ref([
  { id: Date.now(), time: '09:30', msg: '功率因數 (PF) 降至 0.85，低於台電標準，請檢修。', type: '🚨' },
  { id: Date.now()-1000, time: '10:15', msg: '廠房 B 空調異常耗電，已自動發送預警簡訊。', type: '⚠️' }
])
let alertTimer = null

// 控制換頁並安全加載圖表
const changeTab = (tabName) => {
  activeTab.value = tabName
  if (tabName === 'dashboard') {
    nextTick(() => {
      initChart()
      initLineChart()
      fetchEnvironmentData()
    })
  }
}

const changeSubTab = (subTabName) => {
  activeSubTab.value = subTabName
}

const greenEnergyStatus = computed(() => {
  if (powerData.value.green >= 15) return '🟢 今日綠能發電充足，電網實際排碳強度較低！'
  return '🟡 今日火力發電比例偏高，請密切監控企業用電能耗！'
})

onMounted(async () => {
  await fetchPowerData()
  initChart()

  // 啟動跑馬燈定時器
  alertTimer = setInterval(() => {
    const now = new Date()
    const time = `${now.getHours().toString().padStart(2, '0')}:${now.getMinutes().toString().padStart(2, '0')}`
    const msgList = [
      '冷卻水塔馬達電流過載，請檢查。',
      '空調系統待機耗能超過基準值。',
      '偵測到電壓異常波動，已記錄至系統日誌。',
      '產線 C 設備即將超過契約容量！'
    ]
    const randomMsg = msgList[Math.floor(Math.random() * msgList.length)]
    const type = Math.random() > 0.5 ? '🚨' : '⚠️'
    
    alerts.value.unshift({ id: Date.now(), time, msg: randomMsg, type })
    // 保持最多顯示 3 筆
    if (alerts.value.length > 3) alerts.value.pop()
  }, 8000)
})

onUnmounted(() => {
  if (alertTimer) clearInterval(alertTimer)
})

async function fetchPowerData() {
  try {
    isLoading.value = true
    const res = await fetch('https://api.allorigins.win/get?url=' + encodeURIComponent('https://www.taipower.com.tw/d006/load_program/content/load-page/generation_to_pdf.json'))
    if (!res.ok) throw new Error('CORS proxy response error')
    
    const wrapper = await res.json()
    const rawData = JSON.parse(wrapper.contents)
    
    const coalPower = parseFloat(rawData.coal || 38)
    const gasPower = parseFloat(rawData.lng || 36)
    const nuclearPower = parseFloat(rawData.nuclear || 7)
    const greenPower = parseFloat(rawData.solar || 0) + parseFloat(rawData.wind || 0) + parseFloat(rawData.hydro || 11)
    
    const total = coalPower + gasPower + nuclearPower + greenPower
    
    if (total > 0) {
      powerData.value.coal = parseFloat(((coalPower / total) * 100).toFixed(1))
      powerData.value.gas = parseFloat(((gasPower / total) * 100).toFixed(1))
      powerData.value.nuclear = parseFloat(((nuclearPower / total) * 100).toFixed(1))
      powerData.value.green = parseFloat(((greenPower / total) * 100).toFixed(1))
      powerData.value.others = parseFloat((100 - (powerData.value.coal + powerData.value.gas + powerData.value.nuclear + powerData.value.green)).toFixed(1))
    }
    
    const now = new Date()
    updateTime.value = `${now.toLocaleDateString()} ${now.toLocaleTimeString()} (台電實時數據)`
  } catch (error) {
    console.warn('⚠️ 台電連線被攔截，已切換至安全本地模擬數據：', error)
    powerData.value = { coal: 41.5, gas: 36.2, nuclear: 6.8, green: 11.5, others: 4.0 }
    const now = new Date()
    updateTime.value = `${now.toLocaleDateString()} ${now.toLocaleTimeString()} (系統自動安全備用數據)`
  } finally {
    isLoading.value = false
  }
}

async function fetchEnvironmentData() {
  try {
    // 串接 Open-Meteo 開放天氣 API (新北淡水區經緯度)
    const res = await fetch('https://api.open-meteo.com/v1/forecast?latitude=25.17&longitude=121.44&current=temperature_2m,relative_humidity_2m')
    if (!res.ok) throw new Error('Weather API error')
    const data = await res.json()
    const t = data.current.temperature_2m
    const h = data.current.relative_humidity_2m
    initGaugeCharts(t, h)
  } catch (error) {
    console.warn('氣象 API 連線失敗，使用模擬數據', error)
    initGaugeCharts(28.5, 65)
  }
}

function initChart() {
  const chartDom = document.getElementById('power-pie-chart')
  if (!chartDom) return
  
  const existingChart = echarts.getInstanceByDom(chartDom)
  if (existingChart) {
    existingChart.dispose()
  }

  const myChart = echarts.init(chartDom)
  const option = {
    title: { text: '台灣即時發電結構比例', left: 'center', textStyle: { fontSize: 16 } },
    tooltip: { trigger: 'item', formatter: '{b} : {c}%' },
    legend: { bottom: '0%', icon: 'circle', itemWidth: 10, itemHeight: 10 },
    series: [
      {
        name: '發電來源',
        type: 'pie',
        radius: ['40%', '65%'],
        avoidLabelOverlap: false,
        itemStyle: { borderRadius: 8, borderColor: '#fff', borderWidth: 2 },
        label: { show: false },
        data: [
          { value: powerData.value.coal, name: '燃煤發電', itemStyle: { color: '#64748b' } },
          { value: powerData.value.gas, name: '天然氣', itemStyle: { color: '#3b82f6' } },
          { value: powerData.value.nuclear, name: '核能發電', itemStyle: { color: '#f59e0b' } },
          { value: powerData.value.green, name: '再生綠能', itemStyle: { color: '#10b981' } },
          { value: powerData.value.others, name: '其他發電', itemStyle: { color: '#cbd5e1' } }
        ]
      }
    ]
  }
  myChart.setOption(option)
}

function initLineChart() {
  const chartDom = document.getElementById('power-line-chart')
  if (!chartDom) return
  const myChart = echarts.getInstanceByDom(chartDom) || echarts.init(chartDom)

  const option = {
    title: { text: '🔌 今日 24 小時用電負載曲線', left: 'center', textStyle: { fontSize: 16, color: '#334155' } },
    tooltip: { trigger: 'axis', formatter: '{b} <br/>耗電量: <b>{c} kW</b>' },
    xAxis: { 
      type: 'category', 
      boundaryGap: false, 
      data: ['00:00','02:00','04:00','06:00','08:00','10:00','12:00','14:00','16:00','18:00','20:00','22:00','24:00'] 
    },
    yAxis: { type: 'value', name: 'kW', splitLine: { lineStyle: { type: 'dashed' } } },
    visualMap: {
      show: false,
      dimension: 0,
      pieces: [
        { lte: 4, color: '#10b981' }, // 00-08 離峰
        { gt: 4, lte: 11, color: '#ef4444' }, // 08-22 尖峰
        { gt: 11, color: '#10b981' } // 22-24 離峰
      ]
    },
    series: [
      {
        name: '耗電量',
        type: 'line',
        smooth: true,
        symbolSize: 8,
        areaStyle: {
          color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [
            { offset: 0, color: 'rgba(59, 130, 246, 0.4)' },
            { offset: 1, color: 'rgba(59, 130, 246, 0.05)' }
          ])
        },
        data: [120, 100, 110, 150, 300, 550, 600, 580, 620, 480, 350, 180, 130],
        markArea: {
          itemStyle: { color: 'rgba(239, 68, 68, 0.08)' },
          data: [ [ { name: '尖峰時段 (費率高)', xAxis: '08:00' }, { xAxis: '22:00' } ] ]
        }
      }
    ]
  }
  myChart.setOption(option)
}

function initGaugeCharts(temp, hum) {
  const tempDom = document.getElementById('temp-gauge')
  const humDom = document.getElementById('hum-gauge')
  if (!tempDom || !humDom) return
  
  const tChart = echarts.getInstanceByDom(tempDom) || echarts.init(tempDom)
  const hChart = echarts.getInstanceByDom(humDom) || echarts.init(humDom)

  const commonGaugeOpt = {
    type: 'gauge', center: ['50%', '60%'], radius: '100%',
    pointer: { itemStyle: { color: 'inherit' } },
    axisTick: { distance: -20, length: 8, lineStyle: { color: '#fff', width: 2 } },
    splitLine: { distance: -30, length: 30, lineStyle: { color: '#fff', width: 4 } },
    axisLabel: { color: 'inherit', distance: 40, fontSize: 12 },
    detail: { valueAnimation: true, formatter: '{value}', fontSize: 24, offsetCenter: [0, '40%'] }
  };

  tChart.setOption({ series: [{ ...commonGaugeOpt, min: 0, max: 50,
    axisLine: { lineStyle: { width: 15, color: [[0.4, '#3b82f6'], [0.7, '#10b981'], [1, '#ef4444']] } },
    detail: { ...commonGaugeOpt.detail, formatter: '{value} ℃' },
    data: [{ value: temp, name: '溫度' }]
  }] })

  hChart.setOption({ series: [{ ...commonGaugeOpt, min: 0, max: 100,
    axisLine: { lineStyle: { width: 15, color: [[0.3, '#10b981'], [0.7, '#3b82f6'], [1, '#6366f1']] } },
    detail: { ...commonGaugeOpt.detail, formatter: '{value} %' },
    data: [{ value: hum, name: '濕度' }]
  }] })
}
</script>

<style>
:root {
  --primary-dark: #0f172a;
  --primary-color: #1e293b;
  --secondary-color: #334155; 
  --background-gray: #cbd5e0;
  --text-color: #1e293b;
  --accent-blue: #1d4ed8;
  --white: #ffffff;
  --danger: #e53e3e;
  --success: #10b981;
  --card-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.2);
}

body {
  font-family: 'Segoe UI', 'Microsoft JhengHei', sans-serif;
  background-color: var(--background-gray);
  color: var(--text-color);
  margin: 0; padding: 0; line-height: 1.8;
}

header {
  background: linear-gradient(135deg, var(--primary-dark) 0%, var(--primary-color) 100%);
  color: white; padding: 2.5rem 0; text-align: center;
  box-shadow: 0 4px 15px rgba(0,0,0,0.3);
  position: relative; overflow: hidden;
}
header::after {
  content: ''; position: absolute; top: 0; left: 0; width: 100%; height: 100%;
  background-image: radial-gradient(circle, rgba(255,255,255,0.05) 1px, transparent 1px);
  background-size: 25px 20px;
}

.tab-container {
  max-width: 1300px; margin: 2rem auto; background: var(--white);
  border-radius: 20px; box-shadow: var(--card-shadow);
  overflow: hidden; min-height: 850px; border: 1px solid rgba(0,0,0,0.1);
}

.tabs { display: flex; background-color: #f1f5f9; border-bottom: 2px solid #e2e8f0; }
.tab-button {
  flex: 1; padding: 1.5rem 1rem; border: none; background: none;
  font-size: 1.15rem; font-weight: 700; color: #64748b; cursor: pointer; transition: 0.3s;
}
.tab-button:hover { background-color: #e2e8f0; color: var(--accent-blue); }
.tab-button.active { background-color: var(--white); color: var(--accent-blue); position: relative; }
.tab-button.active::after { content: ''; position: absolute; top: 0; left: 0; width: 100%; height: 6px; background-color: var(--accent-blue); }

.tab-content-vue { padding: 3rem; animation: fadeIn 0.6s ease; }

.sub-nav { display: flex; gap: 1.2rem; margin-bottom: 2.5rem; justify-content: center; border-bottom: 1px solid #f1f5f9; padding-bottom: 1.5rem; }
.sub-btn {
  padding: 0.7rem 1.8rem; border-radius: 50px; border: 2px solid #cbd5e1; 
  background: white; font-weight: 700; cursor: pointer; transition: 0.3s; color: #475569;
}
.sub-btn:hover { border-color: var(--accent-blue); color: var(--accent-blue); }
.sub-btn.active { background: var(--accent-blue); color: white; border-color: var(--accent-blue); box-shadow: 0 4px 10px rgba(37, 99, 235, 0.3); }

.grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 2.5rem; }
.grid-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 1.5rem; }
.info-card { 
  padding: 2rem; border-radius: 16px; background: var(--white); border: 1px solid #e2e8f0; 
  box-shadow: 0 4px 6px rgba(0,0,0,0.02); transition: 0.3s;
}
.info-card:hover { transform: translateY(-5px); box-shadow: 0 15px 30px rgba(0,0,0,0.08); }

.flip-card { background-color: transparent; width: 100%; height: 280px; perspective: 1000px; }
.flip-card-inner { position: relative; width: 100%; height: 100%; transition: transform 0.6s; transform-style: preserve-3d; }
.flip-card:hover .flip-card-inner { transform: rotateY(180deg); }
.flip-card-front, .flip-card-back {
  position: absolute; width: 100%; height: 100%; backface-visibility: hidden; border-radius: 16px; 
  padding: 1.8rem; box-sizing: border-box; border: 1px solid #e2e8f0; background: var(--white);
  box-shadow: 0 4px 6px rgba(0,0,0,0.02);
}
.flip-card-back {
  transform: rotateY(180deg); background: #f8fafc; border-bottom: 4px solid var(--accent-blue);
  display: flex; flex-direction: column; justify-content: center;
}
.flip-card-front h4 { margin-top: 0; font-size: 1.15rem; color: var(--primary-dark); }

.home-hero {
  height: 380px; border-radius: 18px; display: flex; align-items: center; justify-content: center;
  background: linear-gradient(rgba(15, 23, 42, 0.75), rgba(15, 23, 42, 0.75)), url('https://yulun7030.github.io/0610/p1.jpg') no-repeat center center;
  background-size: cover; color: white; text-align: center; margin-bottom: 3rem;
}

.param-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(130px, 1fr)); gap: 12px; margin-top: 1.5rem; }
.param-tag { 
  background: var(--primary-dark); color: #38bdf8; padding: 15px 10px; border-radius: 10px; text-align: center; font-size: 0.95rem; font-weight: 700;
}
.param-tag span { color: #94a3b8; font-size: 0.7rem; display: block; margin-bottom: 4px; }

.image-box { width: 100%; max-width: 500px; margin: 0 auto; border-radius: 15px; overflow: hidden; box-shadow: 0 10px 20px rgba(0,0,0,0.1); border: 1px solid #e2e8f0; }
.image-box img { width: 100%; display: block; }

.process-step { display: flex; align-items: flex-start; gap: 1.2rem; margin-bottom: 1.2rem; background: #f8fafc; padding: 1.5rem; border-radius: 12px; border: 1px solid #e2e8f0; }
.step-num { background: var(--primary-color); color: white; width: 32px; height: 32px; border-radius: 50%; display: flex; align-items: center; justify-content: center; flex-shrink: 0; font-weight: bold; }

.motivation-expanded { background: #f8fafc; border-left: 10px solid var(--primary-color); padding: 2.5rem; border-radius: 0 16px 16px 0; margin-bottom: 3rem; }
.objective-item { background: #fff; padding: 1rem; border-radius: 8px; border: 1px solid #edf2f7; margin-bottom: 0.8rem; display: flex; align-items: center; gap: 12px; font-size: 0.95rem; }
.objective-item i { color: var(--accent-blue); }

.faq-container { width: 100%; }
.faq-container details { background: #fff; border: 1px solid #e2e8f0; border-radius: 12px; margin-bottom: 1.2rem; transition: 0.3s; box-shadow: 0 4px 6px rgba(0,0,0,0.02); }
.faq-container details:hover { border-color: var(--accent-blue); box-shadow: 0 10px 20px rgba(0,0,0,0.05); }
.faq-container summary {
  padding: 1.5rem; font-size: 1.15rem; font-weight: 700; cursor: pointer; color: var(--primary-color);
  list-style: none; position: relative; border-radius: 12px; transition: 0.2s ease;
}
.faq-container summary::after { content: '+'; position: absolute; right: 20px; font-size: 1.5rem; color: var(--accent-blue); top: 50%; transform: translateY(-50%); }
.faq-container details[open] summary::after { content: '−'; }
.faq-container details[open] summary {
  border-bottom-left-radius: 0; border-bottom-right-radius: 0; border-bottom: 1px solid #e2e8f0;
  border-left: 6px solid var(--accent-blue); padding-left: calc(1.5rem - 6px);
}
.faq-container p {
  background: #f8fafc; padding: 1.5rem; margin: 0; font-size: 1rem; line-height: 1.8;
  border-bottom-left-radius: 12px; border-bottom-right-radius: 12px;
}

@keyframes fadeIn { from { opacity: 0; transform: translateY(15px); } to { opacity: 1; transform: translateY(0); } }
@keyframes heartbeat {
  0% { transform: scale(1); }
  15% { transform: scale(1.08); }
  30% { transform: scale(1); }
  45% { transform: scale(1.08); }
  60%, 100% { transform: scale(1); }
}
.pulse-btn { animation: heartbeat 2s infinite ease-in-out; }

@media (max-width: 1024px) { .grid-2, .grid-3 { grid-template-columns: 1fr !important; } }

.modal-overlay {
  position: fixed; top: 0; left: 0; width: 100%; height: 100%;
  background: rgba(15, 23, 42, 0.75); display: none; 
  justify-content: center; align-items: center; z-index: 9999;
  opacity: 0; transition: opacity 0.3s ease; backdrop-filter: blur(4px);
}
.modal-overlay.show { display: flex; opacity: 1; }
.modal-content {
  background: white; padding: 2.5rem; border-radius: 16px; width: 90%; max-width: 550px;
  position: relative; box-shadow: 0 20px 40px rgba(0,0,0,0.3);
  transform: translateY(-20px); transition: transform 0.3s ease;
}
.modal-overlay.show .modal-content { transform: translateY(0); }
.close-btn { position: absolute; top: 15px; right: 20px; font-size: 1.8rem; background: none; border: none; cursor: pointer; color: #64748b; transition: 0.2s; }
.close-btn:hover { color: var(--danger); transform: scale(1.1); }
.quiz-btn { display: block; width: 100%; text-align: left; padding: 1.2rem; margin-bottom: 1rem; border: 2px solid #e2e8f0; border-radius: 8px; background: #f8fafc; font-size: 1rem; font-weight: 500; cursor: pointer; transition: 0.2s; color: var(--text-color); }
.quiz-btn:hover:not(:disabled) { border-color: var(--accent-blue); background: #eff6ff; box-shadow: 0 4px 6px rgba(37, 99, 235, 0.1); }
.quiz-btn.correct { background: #d1fae5; border-color: var(--success); color: #065f46; font-weight: bold; }
.quiz-btn.wrong { background: #fee2e2; border-color: var(--danger); color: #991b1b; }
.quiz-feedback { margin-top: 1.5rem; font-weight: bold; text-align: center; font-size: 1.1rem; min-height: 28px; }

.vue-calculator-box {
  background: #f0fdf4; border: 2px dashed #10b981; border-radius: 16px;
  padding: 2rem; margin-top: 3rem; box-shadow: 0 4px 6px rgba(0,0,0,0.02);
}
.calc-input {
  width: 100%; padding: 0.8rem 1.2rem; font-size: 1.1rem; border-radius: 8px;
  border: 1px solid #cbd5e1; box-sizing: border-box;
}
.calc-result-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; margin-top: 1.5rem; }
.res-card {
  background: white; padding: 1.2rem; border-radius: 10px; border-left: 5px solid #10b981;
  box-shadow: 0 2px 4px rgba(0,0,0,0.05); display: flex; flex-direction: column;
}
.res-card span { font-size: 0.85rem; color: #64748b; font-weight: bold; }
.res-card strong { font-size: 1.4rem; color: #0f172a; margin: 0.3rem 0; }
.res-card small { font-size: 0.8rem; color: #94a3b8; }

.energy-dashboard {
  background: #ffffff;
  border: 1px solid #e2e8f0;
  border-radius: 16px;
  padding: 2.5rem;
  margin-top: 3rem;
  box-shadow: 0 4px 20px rgba(0,0,0,0.05);
}
.update-tag {
  font-size: 0.9rem;
  color: #64748b;
  background: #f1f5f9;
  display: inline-block;
  padding: 4px 12px;
  border-radius: 6px;
  margin: 0;
}
.energy-analysis-card {
  background: #f8fafc;
  padding: 1.8rem;
  border-radius: 12px;
  border-left: 6px solid var(--accent-blue);
}
.status-text {
  font-weight: bold;
  font-size: 1.1rem;
  margin-bottom: 1.5rem;
}
.data-row {
  display: flex;
  justify-content: space-between;
  padding: 8px 0;
  border-bottom: 1px dashed #e2e8f0;
}
.data-row strong {
  color: var(--primary-dark);
  font-size: 1.1rem;
}

.alert-ticker { margin-top: 1rem; background: #fff1f2; border: 1px solid #fecdd3; border-radius: 8px; padding: 1rem; overflow: hidden; }
.alert-item { color: #be123c; font-weight: 500; padding: 6px 0; border-bottom: 1px dashed #fecdd3; display: flex; gap: 8px; }
.alert-item:last-child { border-bottom: none; }
.list-enter-active, .list-leave-active { transition: all 0.5s ease; }
.list-enter-from { opacity: 0; transform: translateX(-30px); }
.list-leave-to { opacity: 0; transform: translateX(30px); }
</style>