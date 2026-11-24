<!doctype html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover" />
  <title>Эволюция драгоценных кристаллов</title>
  <meta name="description" content="2D-игра в жанре слияния кристаллов с реалистичной физикой, 10 уровнями эволюции, бонусами и поддержкой VK Bridge для Игр ВКонтакте." />
  <meta property="og:title" content="Эволюция драгоценных кристаллов" />
  <meta property="og:description" content="Объединяйте драгоценные кристаллы, открывайте 10 уровней эволюции и соберите Радужный алмаз!" />
  <meta property="og:type" content="website" />
  <meta name="twitter:card" content="summary_large_image" />
  <script src="https://unpkg.com/@vkontakte/vk-bridge/dist/browser.min.js"></script>
  <style>
    :root {
      --bg-deep: #060713;
      --bg-mid: #0c1028;
      --surface: rgba(15, 21, 48, 0.78);
      --surface-strong: rgba(13, 18, 42, 0.94);
      --border-subtle: rgba(165, 195, 255, 0.16);
      --border-bright: rgba(165, 195, 255, 0.34);
      --text-main: #f3f6ff;
      --text-muted: #9aa9d6;
      --accent-cyan: #38bdf8;
      --accent-violet: #a855f7;
      --accent-gold: #fbbf24;
      --danger: #ff4d6d;
    }

    * {
      box-sizing: border-box;
      -webkit-tap-highlight-color: transparent;
      user-select: none;
      -webkit-user-select: none;
    }

    html, body {
      margin: 0;
      padding: 0;
      width: 100vw;
      height: 100vh;
      height: 100dvh;
      overflow: hidden;
      background: radial-gradient(circle at 50% 20%, #141a3f 0%, #090b1f 55%, #050610 100%);
      color: var(--text-main);
      font-family: 'Montserrat', 'Rubik', 'Segoe UI', system-ui, -apple-system, sans-serif;
      touch-action: none;
    }

    #app {
      position: relative;
      width: 100vw;
      height: 100vh;
      height: 100dvh;
      overflow: hidden;
    }

    #gameCanvas {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      display: block;
      cursor: crosshair;
      touch-action: none;
    }

    #gameCanvas.hammer-cursor {
      cursor: pointer;
    }

    /* HUD Overlay */
    .hud-layer {
      position: absolute;
      inset: 0;
      pointer-events: none;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      padding: max(10px, env(safe-area-inset-top)) max(14px, env(safe-area-inset-right)) max(12px, env(safe-area-inset-bottom)) max(14px, env(safe-area-inset-left));
      z-index: 10;
    }

    .hud-layer.hidden {
      opacity: 0;
      visibility: hidden;
    }

    .top-bar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
    }

    .score-cluster {
      display: flex;
      align-items: baseline;
      gap: 20px;
      pointer-events: auto;
      background: var(--surface);
      border: 1px solid var(--border-subtle);
      border-radius: 14px;
      padding: 8px 16px;
      box-shadow: 0 8px 24px rgba(0, 0, 0, 0.32);
    }

    .metric {
      display: flex;
      flex-direction: column;
      line-height: 1.15;
    }

    .metric-label {
      font-size: 11px;
      font-weight: 600;
      letter-spacing: 0.04em;
      color: var(--text-muted);
    }

    .metric-value {
      font-size: 22px;
      font-weight: 800;
      font-variant-numeric: tabular-nums;
      color: #ffffff;
      text-shadow: 0 0 14px rgba(56, 189, 248, 0.35);
    }

    .metric-value.best {
      color: var(--accent-gold);
      text-shadow: 0 0 14px rgba(251, 191, 36, 0.3);
    }

    .top-right-cluster {
      display: flex;
      align-items: center;
      gap: 10px;
      pointer-events: auto;
    }

    .next-box,
    .hold-box {
      display: flex;
      align-items: center;
      gap: 10px;
      background: var(--surface);
      border: 1px solid var(--border-subtle);
      border-radius: 14px;
      padding: 6px 12px;
      box-shadow: 0 8px 24px rgba(0, 0, 0, 0.32);
    }

    .hold-box {
      cursor: pointer;
      color: var(--text-main);
      font-family: inherit;
      text-align: left;
      transition: transform 0.15s cubic-bezier(0.16, 1, 0.3, 1), border-color 0.15s ease, background 0.15s ease, opacity 0.15s ease;
    }

    .hold-box:hover {
      border-color: var(--border-bright);
      background: rgba(24, 34, 74, 0.9);
    }

    .hold-box:active {
      transform: scale(0.95);
    }

    .hold-box.used {
      opacity: 0.62;
    }

    .next-info {
      display: flex;
      flex-direction: column;
      line-height: 1.2;
    }

    .next-label {
      font-size: 11px;
      font-weight: 600;
      color: var(--text-muted);
    }

    .next-name {
      font-size: 12px;
      font-weight: 700;
      color: var(--text-main);
      max-width: 96px;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }

    #nextCanvas,
    #holdCanvas {
      width: 40px;
      height: 40px;
      display: block;
    }

    .icon-btn {
      width: 44px;
      height: 44px;
      border-radius: 14px;
      border: 1px solid var(--border-subtle);
      background: var(--surface);
      color: var(--text-main);
      display: inline-flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      transition: transform 0.15s cubic-bezier(0.16, 1, 0.3, 1), border-color 0.15s ease, background 0.15s ease;
      box-shadow: 0 8px 24px rgba(0, 0, 0, 0.32);
      flex-shrink: 0;
    }

    .icon-btn:hover {
      border-color: var(--border-bright);
      background: rgba(24, 34, 74, 0.9);
    }

    .icon-btn:active {
      transform: scale(0.94);
    }

    .icon-btn:focus-visible,
    .hold-box:focus-visible,
    .bonus-btn:focus-visible,
    .primary-btn:focus-visible,
    .secondary-btn:focus-visible {
      outline: 2px solid var(--accent-cyan);
      outline-offset: 2px;
    }

    .icon-btn.muted {
      color: var(--text-muted);
    }

    /* Evolution Scale - Desktop Side Panel & Mobile Compact Strip */
    .evo-desktop {
      position: absolute;
      right: max(18px, env(safe-area-inset-right));
      top: 50%;
      transform: translateY(-50%);
      display: flex;
      flex-direction: column;
      gap: 6px;
      background: var(--surface);
      border: 1px solid var(--border-subtle);
      border-radius: 16px;
      padding: 12px 14px;
      pointer-events: auto;
      box-shadow: 0 12px 32px rgba(0, 0, 0, 0.38);
      max-height: calc(100dvh - 180px);
      overflow: hidden;
    }

    .evo-title {
      font-size: 12px;
      font-weight: 700;
      color: var(--text-muted);
      letter-spacing: 0.03em;
      margin-bottom: 4px;
      text-align: center;
    }

    .evo-list {
      display: flex;
      flex-direction: column;
      gap: 4px;
    }

    .evo-item {
      display: flex;
      align-items: center;
      gap: 8px;
      padding: 2px 4px;
      border-radius: 8px;
      opacity: 0.52;
      transition: opacity 0.2s ease, background 0.2s ease;
    }

    .evo-item.unlocked {
      opacity: 1;
      background: rgba(255, 255, 255, 0.04);
    }

    .evo-item-name {
      font-size: 12px;
      font-weight: 600;
      color: var(--text-main);
      white-space: nowrap;
    }

    .evo-item-lvl {
      font-size: 11px;
      font-weight: 700;
      font-variant-numeric: tabular-nums;
      color: var(--text-muted);
      margin-left: auto;
      padding-left: 8px;
    }

    .evo-mobile {
      display: none;
      align-items: center;
      justify-content: center;
      gap: 4px;
      margin: 4px auto 0;
      background: var(--surface);
      border: 1px solid var(--border-subtle);
      border-radius: 12px;
      padding: 4px 8px;
      pointer-events: auto;
    }

    .evo-mobile-item {
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 0.45;
      transition: opacity 0.2s ease, transform 0.2s ease;
    }

    .evo-mobile-item.unlocked {
      opacity: 1;
    }

    /* Hammer Active Banner */
    .hammer-banner {
      position: absolute;
      top: 76px;
      left: 50%;
      transform: translateX(-50%);
      display: none;
      align-items: center;
      gap: 12px;
      background: rgba(20, 28, 66, 0.95);
      border: 1px solid rgba(56, 189, 248, 0.55);
      border-radius: 12px;
      padding: 8px 14px;
      pointer-events: auto;
      box-shadow: 0 8px 28px rgba(56, 189, 248, 0.28);
      z-index: 20;
      white-space: nowrap;
    }

    .hammer-banner.active {
      display: flex;
    }

    .hammer-banner-text {
      font-size: 13px;
      font-weight: 700;
      color: #e0f2fe;
    }

    .hammer-cancel-btn {
      border: 1px solid rgba(255, 255, 255, 0.22);
      background: rgba(255, 255, 255, 0.08);
      color: #fff;
      font-size: 12px;
      font-weight: 700;
      border-radius: 8px;
      padding: 5px 10px;
      cursor: pointer;
    }

    /* Bottom Bonus Bar */
    .bottom-bar {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 12px;
      width: 100%;
      pointer-events: none;
    }

    .bonus-btn {
      pointer-events: auto;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      min-height: 46px;
      padding: 8px 18px;
      border-radius: 14px;
      border: 1px solid var(--border-subtle);
      background: linear-gradient(180deg, rgba(26, 36, 78, 0.92) 0%, rgba(15, 21, 50, 0.96) 100%);
      color: var(--text-main);
      font-family: inherit;
      font-size: 14px;
      font-weight: 700;
      cursor: pointer;
      box-shadow: 0 8px 24px rgba(0, 0, 0, 0.36);
      transition: transform 0.16s cubic-bezier(0.16, 1, 0.3, 1), border-color 0.16s ease, box-shadow 0.16s ease;
      white-space: nowrap;
      flex-shrink: 0;
    }

    .bonus-btn:hover {
      transform: translateY(-2px);
      border-color: rgba(125, 211, 252, 0.55);
      box-shadow: 0 10px 28px rgba(56, 189, 248, 0.2);
    }

    .bonus-btn:active {
      transform: scale(0.96);
    }

    .bonus-btn.active {
      border-color: var(--accent-cyan);
      background: linear-gradient(180deg, rgba(14, 116, 144, 0.85) 0%, rgba(15, 45, 86, 0.95) 100%);
      box-shadow: 0 0 22px rgba(56, 189, 248, 0.4);
    }

    .bonus-ad-tag {
      display: inline-flex;
      align-items: center;
      gap: 4px;
      font-size: 11px;
      font-weight: 700;
      color: var(--accent-gold);
      padding-left: 6px;
      border-left: 1px solid rgba(255, 255, 255, 0.14);
    }

    /* Toast Message */
    .toast-msg {
      position: absolute;
      bottom: 76px;
      left: 50%;
      transform: translateX(-50%) translateY(8px);
      background: rgba(15, 23, 54, 0.94);
      border: 1px solid var(--border-bright);
      color: var(--text-main);
      font-size: 13px;
      font-weight: 600;
      padding: 8px 16px;
      border-radius: 10px;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.2s ease, transform 0.2s ease;
      z-index: 30;
      white-space: nowrap;
    }

    .toast-msg.visible {
      opacity: 1;
      transform: translateX(-50%) translateY(0);
    }

    /* Modal Screens (Title & Game Over) */
    .modal-backdrop {
      position: absolute;
      inset: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
      background: rgba(5, 7, 19, 0.62);
      z-index: 40;
      opacity: 1;
      transition: opacity 0.22s ease;
    }

    .modal-backdrop.hidden {
      opacity: 0;
      pointer-events: none;
      visibility: hidden;
    }

    .modal-card {
      width: 100%;
      max-width: 430px;
      background: linear-gradient(180deg, rgba(19, 26, 62, 0.96) 0%, rgba(10, 14, 34, 0.98) 100%);
      border: 1px solid var(--border-bright);
      border-radius: 22px;
      padding: 28px 24px;
      text-align: center;
      box-shadow: 0 24px 64px rgba(0, 0, 0, 0.62), inset 0 1px 0 rgba(255, 255, 255, 0.12);
      transform: scale(1);
      transition: transform 0.22s cubic-bezier(0.16, 1, 0.3, 1);
    }

    .modal-backdrop.hidden .modal-card {
      transform: scale(0.94);
    }

    .title-lockup {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;
      margin-bottom: 18px;
    }

    .game-title {
      margin: 0;
      font-size: clamp(24px, 4.2vw, 32px);
      font-weight: 900;
      line-height: 1.15;
      letter-spacing: -0.01em;
      text-wrap: balance;
      background: linear-gradient(135deg, #ffffff 0%, #93c5fd 45%, #e879f9 100%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .subtitle {
      margin: 0;
      font-size: 14px;
      line-height: 1.5;
      color: var(--text-muted);
      max-width: 34ch;
    }

    .rules-strip {
      display: flex;
      flex-direction: column;
      gap: 8px;
      text-align: left;
      margin: 18px 0 22px;
      padding: 14px 16px;
      background: rgba(8, 11, 28, 0.65);
      border: 1px solid var(--border-subtle);
      border-radius: 14px;
      font-size: 13px;
      line-height: 1.45;
      color: #d6e0ff;
    }

    .rule-row {
      display: flex;
      align-items: flex-start;
      gap: 10px;
    }

    .rule-num {
      font-weight: 800;
      color: var(--accent-cyan);
      font-variant-numeric: tabular-nums;
      flex-shrink: 0;
    }

    .primary-btn {
      width: 100%;
      min-height: 50px;
      padding: 12px 24px;
      border-radius: 14px;
      border: none;
      background: linear-gradient(135deg, #0ea5e9 0%, #6366f1 55%, #a855f7 100%);
      color: #ffffff;
      font-family: inherit;
      font-size: 16px;
      font-weight: 800;
      letter-spacing: 0.02em;
      cursor: pointer;
      box-shadow: 0 10px 28px rgba(99, 102, 241, 0.42);
      transition: transform 0.16s cubic-bezier(0.16, 1, 0.3, 1), filter 0.16s ease;
    }

    .primary-btn:hover {
      transform: translateY(-2px);
      filter: brightness(1.08);
    }

    .primary-btn:active {
      transform: scale(0.97);
    }

    .secondary-btn {
      width: 100%;
      min-height: 46px;
      margin-top: 10px;
      padding: 10px 20px;
      border-radius: 14px;
      border: 1px solid rgba(96, 165, 250, 0.42);
      background: linear-gradient(180deg, rgba(30, 58, 138, 0.48) 0%, rgba(15, 23, 54, 0.85) 100%);
      color: #e0f2fe;
      font-family: inherit;
      font-size: 15px;
      font-weight: 700;
      letter-spacing: 0.01em;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 9px;
      cursor: pointer;
      box-shadow: 0 8px 22px rgba(15, 23, 42, 0.42);
      transition: transform 0.16s cubic-bezier(0.16, 1, 0.3, 1), border-color 0.16s ease, background 0.16s ease, box-shadow 0.16s ease;
    }

    .secondary-btn:hover {
      transform: translateY(-2px);
      border-color: rgba(125, 211, 252, 0.72);
      background: linear-gradient(180deg, rgba(37, 99, 235, 0.56) 0%, rgba(17, 29, 68, 0.92) 100%);
      box-shadow: 0 10px 26px rgba(56, 189, 248, 0.22);
    }

    .secondary-btn:active {
      transform: scale(0.97);
    }

    .control-hint {
      margin-top: 14px;
      font-size: 12px;
      color: var(--text-muted);
    }

    .gameover-stats {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
      margin: 18px 0 22px;
    }

    .stat-box {
      background: rgba(8, 11, 28, 0.72);
      border: 1px solid var(--border-subtle);
      border-radius: 14px;
      padding: 12px;
      display: flex;
      flex-direction: column;
      gap: 4px;
    }

    .stat-box-label {
      font-size: 12px;
      font-weight: 600;
      color: var(--text-muted);
    }

    .stat-box-val {
      font-size: 24px;
      font-weight: 900;
      font-variant-numeric: tabular-nums;
      color: #ffffff;
    }

    .stat-box-val.record {
      color: var(--accent-gold);
    }

    .new-record-note {
      font-size: 13px;
      font-weight: 700;
      color: var(--accent-gold);
      margin-bottom: 12px;
      display: none;
    }

    .new-record-note.visible {
      display: block;
    }

    @media (max-width: 960px) {
      .evo-desktop {
        display: none;
      }
      .evo-mobile {
        display: flex;
      }
    }

    @media (max-width: 540px) {
      .score-cluster {
        gap: 10px;
        padding: 6px 10px;
      }
      .metric-value {
        font-size: 17px;
      }
      .next-name {
        display: none;
      }
      .next-box,
      .hold-box {
        padding: 5px 8px;
        gap: 6px;
      }
      #nextCanvas,
      #holdCanvas {
        width: 32px;
        height: 32px;
      }
      .icon-btn {
        width: 38px;
        height: 38px;
      }
      .bonus-btn {
        padding: 8px 13px;
        font-size: 13px;
        gap: 7px;
      }
      .hammer-banner {
        top: 106px;
        max-width: calc(100vw - 24px);
      }
    }
  </style>
</head>
<body>
  <div id="app">
    <canvas id="gameCanvas"></canvas>

    <!-- HUD Layer -->
    <div id="hudLayer" class="hud-layer hidden">
      <div>
        <div class="top-bar">
          <div class="score-cluster">
            <div class="metric">
              <span class="metric-label">Счёт</span>
              <span id="scoreValue" class="metric-value">0</span>
            </div>
            <div class="metric">
              <span class="metric-label">Рекорд</span>
              <span id="bestValue" class="metric-value best">0</span>
            </div>
            <div class="metric" title="Шкатулка собранных Радужных алмазов">
              <span class="metric-label">Алмазы</span>
              <span id="diamondsValue" class="metric-value" style="color: #7dd3fc;">0</span>
            </div>
          </div>

          <div class="top-right-cluster">
            <button id="holdBox" class="hold-box" type="button" aria-label="Резервный кристалл" title="Положить или взять кристалл (клавиша C)">
              <div class="next-info">
                <span class="next-label">Резерв</span>
                <span id="holdCrystalName" class="next-name">Пусто</span>
              </div>
              <canvas id="holdCanvas" width="80" height="80"></canvas>
            </button>
            <div class="next-box" aria-label="Следующий кристалл">
              <div class="next-info">
                <span class="next-label">Следующий</span>
                <span id="nextCrystalName" class="next-name">Осколок</span>
              </div>
              <canvas id="nextCanvas" width="80" height="80"></canvas>
            </div>
            <button id="soundBtn" class="icon-btn" type="button" aria-label="Переключить звук" title="Звук">
              <svg id="soundIconOn" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                <polygon points="11 5 6 9 2 9 2 15 6 15 11 19 11 5"></polygon>
                <path d="M15.54 8.46a5 5 0 0 1 0 7.07"></path>
                <path d="M19.07 4.93a10 10 0 0 1 0 14.14"></path>
              </svg>
              <svg id="soundIconOff" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" style="display:none">
                <polygon points="11 5 6 9 2 9 2 15 6 15 11 19 11 5"></polygon>
                <line x1="23" y1="9" x2="17" y2="15"></line>
                <line x1="17" y1="9" x2="23" y2="15"></line>
              </svg>
            </button>
          </div>
        </div>

        <!-- Mobile Horizontal Evolution Strip -->
        <div id="evoMobile" class="evo-mobile" aria-label="Шкала эволюции кристаллов"></div>
      </div>

      <!-- Desktop Vertical Evolution Scale -->
      <aside class="evo-desktop" aria-label="Шкала эволюции кристаллов">
        <div class="evo-title">Эволюция кристаллов</div>
        <div id="evoDesktop" class="evo-list"></div>
      </aside>

      <!-- Hammer Targeting Prompt -->
      <div id="hammerBanner" class="hammer-banner">
        <span class="hammer-banner-text">Нажмите на кристалл, чтобы разбить</span>
        <button id="hammerCancelBtn" class="hammer-cancel-btn" type="button">Отмена</button>
      </div>

      <!-- Bottom Bonus Controls -->
      <div class="bottom-bar">
        <button id="hammerBtn" class="bonus-btn" type="button">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#38bdf8" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
            <path d="m15 12-8.5 8.5c-.83.83-2.17.83-3 0 0 0 0 0 0 0a2.12 2.12 0 0 1 0-3L12 9"></path>
            <path d="M17.64 15 22 10.64"></path>
            <path d="m20.91 11.7-1.25-1.25c-.6-.6-.93-1.4-.93-2.25v-.86L16.01 4.6a5.56 5.56 0 0 0-3.94-1.64H9l.92.82A6.18 6.18 0 0 1 12 8.4v1.56l2 2h2.47l2.26 1.91"></path>
          </svg>
          <span>Молот</span>
          <span class="bonus-ad-tag">
            <svg width="13" height="13" viewBox="0 0 24 24" fill="currentColor">
              <polygon points="5 3 19 12 5 21 5 3"></polygon>
            </svg>
            Бонус
          </span>
        </button>

        <button id="shakeBtn" class="bonus-btn" type="button">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#c084fc" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M2 12h3"></path>
            <path d="M19 12h3"></path>
            <path d="m4.9 4.9 2.1 2.1"></path>
            <path d="m17 17 2.1 2.1"></path>
            <path d="m4.9 19.1 2.1-2.1"></path>
            <path d="m17 7 2.1-2.1"></path>
            <polygon points="12 5 17 12 12 19 7 12 12 5"></polygon>
          </svg>
          <span>Встряска</span>
          <span class="bonus-ad-tag">
            <svg width="13" height="13" viewBox="0 0 24 24" fill="currentColor">
              <polygon points="5 3 19 12 5 21 5 3"></polygon>
            </svg>
            Бонус
          </span>
        </button>
      </div>
    </div>

    <!-- Toast Notification -->
    <div id="toastMsg" class="toast-msg"></div>

    <!-- Start Title Screen -->
    <div id="startModal" class="modal-backdrop">
      <div class="modal-card">
        <div class="title-lockup">
          <svg width="68" height="68" viewBox="0 0 80 80" fill="none" aria-hidden="true">
            <defs>
              <linearGradient id="logoGrad1" x1="12" y1="8" x2="68" y2="72" gradientUnits="userSpaceOnUse">
                <stop offset="0%" stop-color="#38bdf8" />
                <stop offset="50%" stop-color="#a855f7" />
                <stop offset="100%" stop-color="#f472b6" />
              </linearGradient>
              <linearGradient id="logoGrad2" x1="40" y1="8" x2="40" y2="72" gradientUnits="userSpaceOnUse">
                <stop offset="0%" stop-color="#ffffff" stop-opacity="0.9" />
                <stop offset="100%" stop-color="#38bdf8" stop-opacity="0.2" />
              </linearGradient>
            </defs>
            <polygon points="40,6 68,26 58,68 22,68 12,26" fill="url(#logoGrad1)" stroke="#e0f2fe" stroke-width="2" />
            <polygon points="40,6 54,28 40,68 26,28" fill="url(#logoGrad2)" opacity="0.7" />
            <polyline points="12,26 26,28 54,28 68,26" stroke="#ffffff" stroke-opacity="0.65" stroke-width="1.5" fill="none" />
            <polyline points="22,68 26,28 40,6" stroke="#ffffff" stroke-opacity="0.45" stroke-width="1.2" fill="none" />
            <polyline points="58,68 54,28 40,6" stroke="#ffffff" stroke-opacity="0.45" stroke-width="1.2" fill="none" />
          </svg>
          <h1 class="game-title">Эволюция драгоценных кристаллов</h1>
          <p class="subtitle">Соединяйте одинаковые самоцветы в стакане и откройте путь до Радужного алмаза.</p>
        </div>

        <div class="rules-strip">
          <div class="rule-row">
            <span class="rule-num">1.</span>
            <span>Наводите кристалл сверху и отпускайте, чтобы он упал в стакан.</span>
          </div>
          <div class="rule-row">
            <span class="rule-num">2.</span>
            <span>Столкните два одинаковых кристалла — они сольются в более редкий самоцвет.</span>
          </div>
          <div class="rule-row">
            <span class="rule-num">3.</span>
            <span>Не допускайте переполнения: задержка выше красной линии на 3 секунды ведёт к проигрышу.</span>
          </div>
        </div>

        <button id="playBtn" class="primary-btn" type="button">Играть</button>
        <div class="control-hint">Мышь или палец — сброс · «Резерв» (C) — отложить кристалл · Бонусы внизу</div>
      </div>
    </div>

    <!-- Game Over Screen -->
    <div id="gameOverModal" class="modal-backdrop hidden">
      <div class="modal-card">
        <div class="title-lockup">
          <svg width="56" height="56" viewBox="0 0 64 64" fill="none" aria-hidden="true">
            <polygon points="32,6 54,22 46,54 18,54 10,22" fill="rgba(255,77,109,0.22)" stroke="#ff4d6d" stroke-width="2.2" />
            <line x1="22" y1="24" x2="42" y2="44" stroke="#ff8fa3" stroke-width="2.6" stroke-linecap="round" />
            <line x1="42" y1="24" x2="22" y2="44" stroke="#ff8fa3" stroke-width="2.6" stroke-linecap="round" />
          </svg>
          <h2 class="game-title" style="font-size: 26px;">Стакан переполнен</h2>
          <p class="subtitle">Кристаллы поднялись выше красной черты и удержались там 3 секунды.</p>
        </div>

        <div id="newRecordNote" class="new-record-note">Новый личный рекорд!</div>

        <div class="gameover-stats">
          <div class="stat-box">
            <span class="stat-box-label">Ваш счёт</span>
            <span id="finalScore" class="stat-box-val">0</span>
          </div>
          <div class="stat-box">
            <span class="stat-box-label">Лучший рекорд</span>
            <span id="finalBest" class="stat-box-val record">0</span>
          </div>
        </div>

        <button id="restartBtn" class="primary-btn" type="button">Играть заново</button>
        <button id="shareBtn" class="secondary-btn" type="button">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#38bdf8" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
            <circle cx="18" cy="5" r="3"></circle>
            <circle cx="6" cy="12" r="3"></circle>
            <circle cx="18" cy="19" r="3"></circle>
            <line x1="8.59" y1="13.51" x2="15.42" y2="17.49"></line>
            <line x1="15.41" y1="6.51" x2="8.59" y2="10.49"></line>
          </svg>
          <span>Поделиться рекордом</span>
        </button>
      </div>
    </div>
  </div>

  <script>
    (() => {
      'use strict';

      // =========================================================
      // 1. VK BRIDGE SAFE WRAPPER
      // =========================================================
      let isVKEnv = false;
      let isAdShowing = false;

      function isVKBridgeAvailable() {
        return typeof vkBridge !== 'undefined' && typeof vkBridge.send === 'function';
      }

      function isEmbeddedInVK() {
        if (isVKEnv) return true;
        if (!isVKBridgeAvailable()) return false;
        if (typeof vkBridge.isEmbedded === 'function') {
          try {
            return Boolean(vkBridge.isEmbedded());
          } catch (_) {
            return false;
          }
        }
        return false;
      }

      async function initVKBridge() {
        try {
          if (isVKBridgeAvailable()) {
            const res = await Promise.race([
              vkBridge.send('VKWebAppInit'),
              new Promise((_, reject) => setTimeout(() => reject(new Error('VKWebAppInit timeout')), 1500))
            ]);
            if (!res || res.result !== false) {
              isVKEnv = true;
            }
          }
        } catch (_) {
          isVKEnv = false;
        }
      }

      async function showFullscreenAd(onDone) {
        if (isAdShowing) return;
        if (!isVKBridgeAvailable() || !isEmbeddedInVK()) {
          onDone();
          return;
        }
        isAdShowing = true;
        audio.pauseForAd();
        try {
          await vkBridge.send('VKWebAppShowNativeAds', { ad_format: 'interstitial' });
        } catch (_) {
          // Игнорируем ошибку показа рекламы, чтобы игрок мог продолжить игру
        } finally {
          isAdShowing = false;
          audio.resumeFromAd();
          onDone();
        }
      }

      async function showRewardedAd(onReward) {
        if (isAdShowing) return;
        if (!isVKBridgeAvailable() || !isEmbeddedInVK()) {
          // Режим локального теста без ВКонтакте — выдаём бонус сразу
          onReward();
          return;
        }
        isAdShowing = true;
        audio.pauseForAd();
        try {
          const data = await vkBridge.send('VKWebAppShowNativeAds', { ad_format: 'reward' });
          if (data && data.result === true) {
            onReward();
          } else {
            showToast('Досмотрите рекламу до конца, чтобы получить бонус');
          }
        } catch (_) {
          if (!isVKEnv) {
            onReward();
          } else {
            showToast('Реклама сейчас недоступна');
          }
        } finally {
          isAdShowing = false;
          audio.resumeFromAd();
        }
      }

      // =========================================================
      // 2. WEB AUDIO API PROCEDURAL SYNTHESIZER
      // =========================================================
      class CrystalAudio {
        constructor() {
          this.ctx = null;
          this.muted = false;
          this.adPaused = false;
          this.lastClinkAt = 0;
          try {
            const savedMute = localStorage.getItem('crystal_merge_muted');
            if (savedMute === '1') this.muted = true;
          } catch (_) {}
        }

        ensureContext() {
          if (!this.ctx) {
            const AudioCtx = window.AudioContext || window.webkitAudioContext;
            if (!AudioCtx) return null;
            this.ctx = new AudioCtx();
          }
          if (this.ctx.state === 'suspended' && !this.adPaused && !this.muted) {
            this.ctx.resume().catch(() => {});
          }
          return this.ctx;
        }

        isPlayable() {
          return !this.muted && !this.adPaused && !isAdShowing;
        }

        toggleMute() {
          this.muted = !this.muted;
          try {
            localStorage.setItem('crystal_merge_muted', this.muted ? '1' : '0');
          } catch (_) {}
          if (this.ctx) {
            if (this.muted) {
              this.ctx.suspend().catch(() => {});
            } else if (!this.adPaused) {
              this.ctx.resume().catch(() => {});
            }
          }
          return this.muted;
        }

        pauseForAd() {
          this.adPaused = true;
          if (this.ctx && this.ctx.state === 'running') {
            this.ctx.suspend().catch(() => {});
          }
        }

        resumeFromAd() {
          this.adPaused = false;
          if (this.ctx && !this.muted && this.ctx.state === 'suspended') {
            this.ctx.resume().catch(() => {});
          }
        }

        playDrop() {
          if (!this.isPlayable()) return;
          const ctx = this.ensureContext();
          if (!ctx) return;
          const now = ctx.currentTime;
          const osc = ctx.createOscillator();
          const gain = ctx.createGain();
          osc.type = 'sine';
          osc.frequency.setValueAtTime(520, now);
          osc.frequency.exponentialRampToValueAtTime(240, now + 0.11);
          gain.gain.setValueAtTime(0.08, now);
          gain.gain.exponentialRampToValueAtTime(0.001, now + 0.12);
          osc.connect(gain);
          gain.connect(ctx.destination);
          osc.start(now);
          osc.stop(now + 0.13);
        }

        playClink(intensity) {
          if (!this.isPlayable()) return;
          const nowMs = performance.now();
          if (nowMs - this.lastClinkAt < 55) return;
          this.lastClinkAt = nowMs;

          const ctx = this.ensureContext();
          if (!ctx) return;
          const now = ctx.currentTime;
          const vol = Math.min(0.075, Math.max(0.012, intensity * 0.06));
          const freq = 950 + Math.random() * 550;

          const osc = ctx.createOscillator();
          const gain = ctx.createGain();
          osc.type = 'triangle';
          osc.frequency.setValueAtTime(freq, now);
          osc.frequency.exponentialRampToValueAtTime(freq * 0.88, now + 0.06);
          gain.gain.setValueAtTime(vol, now);
          gain.gain.exponentialRampToValueAtTime(0.0008, now + 0.065);
          osc.connect(gain);
          gain.connect(ctx.destination);
          osc.start(now);
          osc.stop(now + 0.07);
        }

        playMerge(level, combo = 1) {
          if (!this.isPlayable()) return;
          const ctx = this.ensureContext();
          if (!ctx) return;
          const now = ctx.currentTime;

          // Higher crystal level -> brighter, higher pitch crystalline bell
          const scaleSemitones = [0, 2, 4, 7, 9, 12, 14, 16, 19, 24];
          const semi = scaleSemitones[Math.min(level, scaleSemitones.length - 1)] + Math.min(combo - 1, 4);
          const baseFreq = 330 * Math.pow(2, semi / 12);

          // Main crystal tone
          const osc1 = ctx.createOscillator();
          const gain1 = ctx.createGain();
          osc1.type = 'sine';
          osc1.frequency.setValueAtTime(baseFreq, now);
          osc1.frequency.exponentialRampToValueAtTime(baseFreq * 1.015, now + 0.28);
          gain1.gain.setValueAtTime(0.001, now);
          gain1.gain.linearRampToValueAtTime(0.16, now + 0.014);
          gain1.gain.exponentialRampToValueAtTime(0.0008, now + 0.38);
          osc1.connect(gain1);
          gain1.connect(ctx.destination);
          osc1.start(now);
          osc1.stop(now + 0.4);

          // Harmonic shimmer fifth/octave overtone
          const osc2 = ctx.createOscillator();
          const gain2 = ctx.createGain();
          osc2.type = 'triangle';
          osc2.frequency.setValueAtTime(baseFreq * 1.5, now + 0.02);
          gain2.gain.setValueAtTime(0.001, now + 0.02);
          gain2.gain.linearRampToValueAtTime(0.08, now + 0.04);
          gain2.gain.exponentialRampToValueAtTime(0.0008, now + 0.34);
          osc2.connect(gain2);
          gain2.connect(ctx.destination);
          osc2.start(now + 0.02);
          osc2.stop(now + 0.36);
        }

        playHammer() {
          if (!this.isPlayable()) return;
          const ctx = this.ensureContext();
          if (!ctx) return;
          const now = ctx.currentTime;

          // Impact thud
          const osc = ctx.createOscillator();
          const g = ctx.createGain();
          osc.type = 'sawtooth';
          osc.frequency.setValueAtTime(190, now);
          osc.frequency.exponentialRampToValueAtTime(52, now + 0.18);
          g.gain.setValueAtTime(0.16, now);
          g.gain.exponentialRampToValueAtTime(0.001, now + 0.2);
          osc.connect(g);
          g.connect(ctx.destination);
          osc.start(now);
          osc.stop(now + 0.21);

          // High glass shatter sparkles
          for (let i = 0; i < 4; i++) {
            const t = now + i * 0.028;
            const sOsc = ctx.createOscillator();
            const sGain = ctx.createGain();
            sOsc.type = 'triangle';
            sOsc.frequency.setValueAtTime(1400 + i * 420 + Math.random() * 200, t);
            sGain.gain.setValueAtTime(0.07, t);
            sGain.gain.exponentialRampToValueAtTime(0.001, t + 0.12);
            sOsc.connect(sGain);
            sGain.connect(ctx.destination);
            sOsc.start(t);
            sOsc.stop(t + 0.13);
          }
        }

        playShake() {
          if (!this.isPlayable()) return;
          const ctx = this.ensureContext();
          if (!ctx) return;
          const now = ctx.currentTime;
          for (let i = 0; i < 5; i++) {
            const t = now + i * 0.07;
            const osc = ctx.createOscillator();
            const gain = ctx.createGain();
            osc.type = 'sine';
            osc.frequency.setValueAtTime(220 + i * 65, t);
            osc.frequency.exponentialRampToValueAtTime(150 + i * 40, t + 0.09);
            gain.gain.setValueAtTime(0.08, t);
            gain.gain.exponentialRampToValueAtTime(0.001, t + 0.1);
            osc.connect(gain);
            gain.connect(ctx.destination);
            osc.start(t);
            osc.stop(t + 0.11);
          }
        }

        playGameOver() {
          if (!this.isPlayable()) return;
          const ctx = this.ensureContext();
          if (!ctx) return;
          const now = ctx.currentTime;
          const notes = [392, 349.23, 311.13, 261.63];
          notes.forEach((freq, idx) => {
            const t = now + idx * 0.13;
            const osc = ctx.createOscillator();
            const g = ctx.createGain();
            osc.type = 'triangle';
            osc.frequency.setValueAtTime(freq, t);
            g.gain.setValueAtTime(0.11, t);
            g.gain.exponentialRampToValueAtTime(0.001, t + 0.34);
            osc.connect(g);
            g.connect(ctx.destination);
            osc.start(t);
            osc.stop(t + 0.36);
          });
        }
      }

      const audio = new CrystalAudio();

      // =========================================================
      // 3. 10 CRYSTAL EVOLUTION TIERS
      // =========================================================
      const LEVELS = [
        {
          name: 'Звёздный осколок',
          short: 'Осколок',
          r: 16,
          score: 2,
          sides: 4,
          c1: '#e0f2fe',
          c2: '#38bdf8',
          c3: '#0369a1',
          glow: 'rgba(56, 189, 248, 0.72)'
        },
        {
          name: 'Розовый кварц',
          short: 'Кварц',
          r: 21,
          score: 4,
          sides: 5,
          c1: '#fce7f3',
          c2: '#f472b6',
          c3: '#be185d',
          glow: 'rgba(244, 114, 182, 0.72)'
        },
        {
          name: 'Аметист',
          short: 'Аметист',
          r: 27,
          score: 8,
          sides: 6,
          c1: '#f3e8ff',
          c2: '#a855f7',
          c3: '#6b21a8',
          glow: 'rgba(168, 85, 247, 0.75)'
        },
        {
          name: 'Сапфир',
          short: 'Сапфир',
          r: 34,
          score: 16,
          sides: 6,
          c1: '#dbeafe',
          c2: '#3b82f6',
          c3: '#1d4ed8',
          glow: 'rgba(59, 130, 246, 0.75)'
        },
        {
          name: 'Изумруд',
          short: 'Изумруд',
          r: 42,
          score: 32,
          sides: 8,
          c1: '#d1fae5',
          c2: '#10b981',
          c3: '#047857',
          glow: 'rgba(16, 185, 129, 0.75)'
        },
        {
          name: 'Цитрин',
          short: 'Цитрин',
          r: 51,
          score: 64,
          sides: 8,
          c1: '#fef3c7',
          c2: '#f59e0b',
          c3: '#b45309',
          glow: 'rgba(245, 158, 11, 0.78)'
        },
        {
          name: 'Рубин',
          short: 'Рубин',
          r: 61,
          score: 128,
          sides: 10,
          c1: '#fee2e2',
          c2: '#ef4444',
          c3: '#991b1b',
          glow: 'rgba(239, 68, 68, 0.8)'
        },
        {
          name: 'Огненный опал',
          short: 'Опал',
          r: 72,
          score: 256,
          sides: 10,
          c1: '#ffedd5',
          c2: '#fb7185',
          c3: '#ea580c',
          glow: 'rgba(251, 146, 60, 0.85)'
        },
        {
          name: 'Александрит',
          short: 'Александрит',
          r: 84,
          score: 512,
          sides: 12,
          c1: '#ccfbf1',
          c2: '#2dd4bf',
          c3: '#4f46e5',
          glow: 'rgba(45, 212, 191, 0.85)'
        },
        {
          name: 'Радужный алмаз',
          short: 'Алмаз',
          r: 98,
          score: 1024,
          sides: 12,
          c1: '#ffffff',
          c2: '#a5f3fc',
          c3: '#c084fc',
          glow: 'rgba(255, 255, 255, 0.92)',
          rainbow: true
        }
      ];

      // =========================================================
      // 4. RENDERING CRYSTALS (SHARED FOR WORLD, NEXT & SCALE)
      // =========================================================
      function drawCrystal(ctx, x, y, r, level, angle, time, opts = {}) {
        const def = LEVELS[level];
        const scale = opts.scale !== undefined ? opts.scale : 1;
        const alpha = opts.alpha !== undefined ? opts.alpha : 1;
        const dangerGlow = opts.danger || false;
        const targeted = opts.targeted || false;
        const drawR = r * scale;
        if (drawR <= 0.5) return;

        ctx.save();
        ctx.translate(x, y);
        ctx.globalAlpha = alpha;

        // Ambient magical aura glow
        const auraR = drawR * 1.42;
        const auraGrad = ctx.createRadialGradient(0, 0, drawR * 0.25, 0, 0, auraR);
        if (dangerGlow) {
          auraGrad.addColorStop(0, 'rgba(255, 77, 109, 0.65)');
          auraGrad.addColorStop(1, 'rgba(255, 77, 109, 0)');
        } else if (def.rainbow) {
          const hue = (time * 80) % 360;
          auraGrad.addColorStop(0, `hsla(${hue}, 95%, 76%, 0.55)`);
          auraGrad.addColorStop(0.55, `hsla(${(hue + 110) % 360}, 95%, 65%, 0.22)`);
          auraGrad.addColorStop(1, 'rgba(255, 255, 255, 0)');
        } else {
          auraGrad.addColorStop(0, def.glow);
          auraGrad.addColorStop(1, 'rgba(0, 0, 0, 0)');
        }
        ctx.fillStyle = auraGrad;
        ctx.beginPath();
        ctx.arc(0, 0, auraR, 0, Math.PI * 2);
        ctx.fill();

        ctx.rotate(angle);

        // Outer faceted polygon matching collision circle smoothly
        const sides = def.sides;
        const pts = [];
        for (let i = 0; i < sides; i++) {
          const a = (i / sides) * Math.PI * 2 - Math.PI / 2;
          const jitter = i % 2 === 0 ? 1.0 : 0.94;
          pts.push({
            x: Math.cos(a) * drawR * jitter,
            y: Math.sin(a) * drawR * jitter
          });
        }

        // Body gradient
        let bodyGrad;
        if (def.rainbow) {
          const hue = (time * 90) % 360;
          bodyGrad = ctx.createLinearGradient(-drawR, -drawR, drawR, drawR);
          bodyGrad.addColorStop(0, `hsl(${hue}, 95%, 82%)`);
          bodyGrad.addColorStop(0.35, `hsl(${(hue + 70) % 360}, 92%, 72%)`);
          bodyGrad.addColorStop(0.7, `hsl(${(hue + 150) % 360}, 92%, 68%)`);
          bodyGrad.addColorStop(1, `hsl(${(hue + 240) % 360}, 90%, 75%)`);
        } else {
          bodyGrad = ctx.createRadialGradient(-drawR * 0.28, -drawR * 0.3, drawR * 0.08, 0, 0, drawR);
          bodyGrad.addColorStop(0, def.c1);
          bodyGrad.addColorStop(0.5, def.c2);
          bodyGrad.addColorStop(1, def.c3);
        }

        ctx.beginPath();
        ctx.moveTo(pts[0].x, pts[0].y);
        for (let i = 1; i < pts.length; i++) ctx.lineTo(pts[i].x, pts[i].y);
        ctx.closePath();
        ctx.fillStyle = bodyGrad;
        ctx.fill();

        // Crisp luminous rim
        ctx.lineWidth = Math.max(1.2, drawR * 0.055);
        ctx.strokeStyle = dangerGlow
          ? '#ff4d6d'
          : def.rainbow
            ? 'rgba(255, 255, 255, 0.95)'
            : 'rgba(255, 255, 255, 0.72)';
        ctx.stroke();

        // Inner jewel table polygon (faceted depth)
        const innerScale = 0.56;
        const innerPts = pts.map((p) => ({ x: p.x * innerScale, y: p.y * innerScale }));

        // Facet wedges radiating from inner table to outer edge
        for (let i = 0; i < sides; i++) {
          const next = (i + 1) % sides;
          ctx.beginPath();
          ctx.moveTo(pts[i].x, pts[i].y);
          ctx.lineTo(pts[next].x, pts[next].y);
          ctx.lineTo(innerPts[next].x, innerPts[next].y);
          ctx.lineTo(innerPts[i].x, innerPts[i].y);
          ctx.closePath();
          const facetShade = ((i % 3) - 1) * 0.09;
          if (facetShade > 0) {
            ctx.fillStyle = `rgba(255, 255, 255, ${facetShade + 0.08})`;
            ctx.fill();
          } else if (facetShade < 0) {
            ctx.fillStyle = `rgba(5, 8, 28, ${Math.abs(facetShade) + 0.1})`;
            ctx.fill();
          }
          ctx.lineWidth = Math.max(0.7, drawR * 0.022);
          ctx.strokeStyle = 'rgba(255, 255, 255, 0.28)';
          ctx.stroke();
        }

        // Inner glowing core
        ctx.beginPath();
        ctx.moveTo(innerPts[0].x, innerPts[0].y);
        for (let i = 1; i < innerPts.length; i++) ctx.lineTo(innerPts[i].x, innerPts[i].y);
        ctx.closePath();
        const coreGrad = ctx.createRadialGradient(0, 0, 0, 0, 0, drawR * innerScale);
        coreGrad.addColorStop(0, 'rgba(255, 255, 255, 0.78)');
        coreGrad.addColorStop(0.65, def.rainbow ? 'rgba(255,255,255,0.28)' : def.c2);
        coreGrad.addColorStop(1, 'rgba(255, 255, 255, 0.08)');
        ctx.fillStyle = coreGrad;
        ctx.fill();
        ctx.lineWidth = Math.max(0.8, drawR * 0.025);
        ctx.strokeStyle = 'rgba(255, 255, 255, 0.55)';
        ctx.stroke();

        // Specular catchlight (unrotated light direction offset)
        ctx.rotate(-angle);
        ctx.beginPath();
        ctx.ellipse(-drawR * 0.3, -drawR * 0.34, drawR * 0.22, drawR * 0.11, -Math.PI / 4, 0, Math.PI * 2);
        ctx.fillStyle = 'rgba(255, 255, 255, 0.72)';
        ctx.fill();

        // Hammer targeting reticle
        if (targeted) {
          const pulse = 1 + Math.sin(time * 10) * 0.06;
          ctx.strokeStyle = '#38bdf8';
          ctx.lineWidth = 2.4;
          ctx.setLineDash([6, 5]);
          ctx.beginPath();
          ctx.arc(0, 0, (drawR + 6) * pulse, 0, Math.PI * 2);
          ctx.stroke();
          ctx.setLineDash([]);
        }

        ctx.restore();
      }

      // =========================================================
      // 5. DOM REFERENCES & EVOLUTION UI SETUP
      // =========================================================
      const canvas = document.getElementById('gameCanvas');
      const ctx = canvas.getContext('2d');
      const nextCanvas = document.getElementById('nextCanvas');
      const nextCtx = nextCanvas.getContext('2d');
      const holdCanvas = document.getElementById('holdCanvas');
      const holdCtx = holdCanvas.getContext('2d');

      const hudLayer = document.getElementById('hudLayer');
      const scoreEl = document.getElementById('scoreValue');
      const bestEl = document.getElementById('bestValue');
      const diamondsEl = document.getElementById('diamondsValue');
      const nextNameEl = document.getElementById('nextCrystalName');
      const holdBox = document.getElementById('holdBox');
      const holdNameEl = document.getElementById('holdCrystalName');
      const soundBtn = document.getElementById('soundBtn');
      const soundIconOn = document.getElementById('soundIconOn');
      const soundIconOff = document.getElementById('soundIconOff');
      const hammerBtn = document.getElementById('hammerBtn');
      const shakeBtn = document.getElementById('shakeBtn');
      const hammerBanner = document.getElementById('hammerBanner');
      const hammerCancelBtn = document.getElementById('hammerCancelBtn');
      const toastEl = document.getElementById('toastMsg');

      const startModal = document.getElementById('startModal');
      const playBtn = document.getElementById('playBtn');
      const gameOverModal = document.getElementById('gameOverModal');
      const finalScoreEl = document.getElementById('finalScore');
      const finalBestEl = document.getElementById('finalBest');
      const newRecordNote = document.getElementById('newRecordNote');
      const restartBtn = document.getElementById('restartBtn');
      const shareBtn = document.getElementById('shareBtn');

      const evoDesktopEl = document.getElementById('evoDesktop');
      const evoMobileEl = document.getElementById('evoMobile');
      const evoDesktopItems = [];
      const evoMobileItems = [];

      function buildEvolutionUI() {
        LEVELS.forEach((lvl, idx) => {
          // Desktop item
          const row = document.createElement('div');
          row.className = 'evo-item';
          const iconCanvas = document.createElement('canvas');
          iconCanvas.width = 48;
          iconCanvas.height = 48;
          iconCanvas.style.width = '24px';
          iconCanvas.style.height = '24px';
          const iCtx = iconCanvas.getContext('2d');
          drawCrystal(iCtx, 24, 24, 17, idx, 0, 1.2);

          const nameSpan = document.createElement('span');
          nameSpan.className = 'evo-item-name';
          nameSpan.textContent = lvl.name;

          const lvlSpan = document.createElement('span');
          lvlSpan.className = 'evo-item-lvl';
          lvlSpan.textContent = String(idx + 1);

          row.appendChild(iconCanvas);
          row.appendChild(nameSpan);
          row.appendChild(lvlSpan);
          evoDesktopEl.appendChild(row);
          evoDesktopItems.push(row);

          // Mobile compact badge
          const mItem = document.createElement('div');
          mItem.className = 'evo-mobile-item';
          mItem.title = `${idx + 1}. ${lvl.name}`;
          const mCanvas = document.createElement('canvas');
          mCanvas.width = 40;
          mCanvas.height = 40;
          mCanvas.style.width = '22px';
          mCanvas.style.height = '22px';
          const mCtx = mCanvas.getContext('2d');
          drawCrystal(mCtx, 20, 20, 14, idx, 0, 1.2);
          mItem.appendChild(mCanvas);
          evoMobileEl.appendChild(mItem);
          evoMobileItems.push(mItem);
        });
      }

      // =========================================================
      // 6. GAME STATE & WORLD CONSTANTS
      // =========================================================
      const WORLD_W = 400;
      const WORLD_H = 580;
      const DANGER_Y = 108;
      const SPAWN_Y = 34;
      const CORNER_R = 26;
      const GRAVITY = 1360;
      const LOSS_TIME_LIMIT = 3.0;
      const DROP_COOLDOWN = 0.42;

      let gameState = 'TITLE'; // 'TITLE' | 'PLAYING' | 'GAMEOVER'
      let score = 0;
      let bestScore = 0;
      let diamondVault = 0;
      try {
        bestScore = parseInt(localStorage.getItem('crystal_merge_best') || '0', 10) || 0;
        diamondVault = parseInt(localStorage.getItem('crystal_merge_diamonds') || '0', 10) || 0;
      } catch (_) {}

      let crystals = [];
      let particles = [];
      let shockwaves = [];
      let floatingTexts = [];
      let stars = [];
      let nebulaMotes = [];

      let currentLevel = 0;
      let nextLevel = 1;
      let holdLevel = null;
      let canHold = true;
      let aimX = WORLD_W / 2;
      let canDrop = true;
      let dropTimer = 0;
      let dangerTimer = 0;
      let hammerMode = false;
      let hoveredCrystalId = null;
      let shakeTimer = 0;
      let microShake = 0;
      let comboCount = 0;
      let comboTimer = 0;
      let comboGlow = 0;
      let nextId = 1;
      let toastTimeout = null;
      let elapsedTime = 0;

      const unlockedLevels = new Set([0, 1]);

      // Viewport transform cache
      let viewW = window.innerWidth;
      let viewH = window.innerHeight;
      let dpr = Math.min(window.devicePixelRatio || 1, 2);
      let worldScale = 1;
      let worldOffsetX = 0;
      let worldOffsetY = 0;

      function initBackdropParticles() {
        stars = [];
        for (let i = 0; i < 95; i++) {
          stars.push({
            x: Math.random(),
            y: Math.random(),
            size: 0.7 + Math.random() * 1.8,
            phase: Math.random() * Math.PI * 2,
            speed: 0.7 + Math.random() * 1.8
          });
        }
        nebulaMotes = [];
        const moteColors = ['rgba(56, 189, 248, 0.28)', 'rgba(168, 85, 247, 0.25)', 'rgba(244, 114, 182, 0.22)'];
        for (let i = 0; i < 28; i++) {
          nebulaMotes.push({
            x: Math.random(),
            y: Math.random(),
            vx: (Math.random() - 0.5) * 0.015,
            vy: -0.006 - Math.random() * 0.014,
            r: 1.5 + Math.random() * 3.5,
            color: moteColors[i % moteColors.length]
          });
        }
      }

      function computeLayout() {
        viewW = window.innerWidth;
        viewH = window.innerHeight;
        dpr = Math.min(window.devicePixelRatio || 1, 2);
        canvas.width = Math.floor(viewW * dpr);
        canvas.height = Math.floor(viewH * dpr);

        const isNarrow = viewW <= 960;
        const topReserved = isNarrow ? 114 : 82;
        const bottomReserved = 82;
        const sideReserved = isNarrow ? 24 : 260;

        const availW = Math.max(200, viewW - sideReserved);
        const availH = Math.max(180, viewH - topReserved - bottomReserved);

        const totalWorldW = WORLD_W + 24;
        const totalWorldH = WORLD_H + 58; // includes aiming crystal headroom above vessel
        worldScale = Math.min(availW / totalWorldW, availH / totalWorldH);

        worldOffsetX = (viewW - WORLD_W * worldScale) / 2;
        worldOffsetY = topReserved + (availH - WORLD_H * worldScale) / 2 + 26 * worldScale;
      }

      function screenToWorld(clientX, clientY) {
        const rect = canvas.getBoundingClientRect();
        const sx = clientX - rect.left;
        const sy = clientY - rect.top;
        return {
          x: (sx - worldOffsetX) / worldScale,
          y: (sy - worldOffsetY) / worldScale
        };
      }

      // =========================================================
      // 7. HUD & TOAST HELPERS
      // =========================================================
      function updateScoreUI() {
        scoreEl.textContent = String(score);
        bestEl.textContent = String(bestScore);
        diamondsEl.textContent = String(diamondVault);
      }

      function updateNextUI() {
        const def = LEVELS[nextLevel];
        nextNameEl.textContent = def.short;
        nextCtx.clearRect(0, 0, nextCanvas.width, nextCanvas.height);
        drawCrystal(nextCtx, 40, 40, 25, nextLevel, 0, elapsedTime);
      }

      function updateHoldUI() {
        holdCtx.clearRect(0, 0, holdCanvas.width, holdCanvas.height);
        if (holdLevel === null) {
          holdNameEl.textContent = 'Пусто';
          holdCtx.save();
          holdCtx.setLineDash([5, 4]);
          holdCtx.strokeStyle = 'rgba(154, 169, 214, 0.45)';
          holdCtx.lineWidth = 2;
          holdCtx.beginPath();
          holdCtx.arc(40, 40, 22, 0, Math.PI * 2);
          holdCtx.stroke();
          holdCtx.restore();
        } else {
          const def = LEVELS[holdLevel];
          holdNameEl.textContent = def.short;
          drawCrystal(holdCtx, 40, 40, 25, holdLevel, 0, elapsedTime);
        }
        holdBox.classList.toggle('used', !canHold);
      }

      function syncEvolutionUI() {
        LEVELS.forEach((_, idx) => {
          const isUnlocked = unlockedLevels.has(idx);
          evoDesktopItems[idx]?.classList.toggle('unlocked', isUnlocked);
          evoMobileItems[idx]?.classList.toggle('unlocked', isUnlocked);
        });
      }

      function syncSoundUI() {
        soundIconOn.style.display = audio.muted ? 'none' : 'block';
        soundIconOff.style.display = audio.muted ? 'block' : 'none';
        soundBtn.classList.toggle('muted', audio.muted);
      }

      function showToast(msg) {
        toastEl.textContent = msg;
        toastEl.classList.add('visible');
        if (toastTimeout) clearTimeout(toastTimeout);
        toastTimeout = setTimeout(() => {
          toastEl.classList.remove('visible');
        }, 2100);
      }

      function setHammerMode(active) {
        hammerMode = active;
        hoveredCrystalId = null;
        hammerBtn.classList.toggle('active', active);
        hammerBanner.classList.toggle('active', active);
        canvas.classList.toggle('hammer-cursor', active);
      }

      function pickSpawnLevel() {
        // Weighted pick from first 4 levels
        const r = Math.random();
        if (r < 0.38) return 0;
        if (r < 0.68) return 1;
        if (r < 0.88) return 2;
        return 3;
      }

      function resetGame() {
        crystals = [];
        particles = [];
        shockwaves = [];
        floatingTexts = [];
        score = 0;
        dangerTimer = 0;
        shakeTimer = 0;
        microShake = 0;
        comboCount = 0;
        comboTimer = 0;
        comboGlow = 0;
        canDrop = true;
        dropTimer = 0;
        setHammerMode(false);

        unlockedLevels.clear();
        currentLevel = pickSpawnLevel();
        nextLevel = pickSpawnLevel();
        holdLevel = null;
        canHold = true;
        unlockedLevels.add(currentLevel);
        unlockedLevels.add(nextLevel);

        const r = LEVELS[currentLevel].r;
        aimX = Math.max(r + 4, Math.min(WORLD_W - r - 4, WORLD_W / 2));

        updateScoreUI();
        updateNextUI();
        updateHoldUI();
        syncEvolutionUI();
      }

      function startGame() {
        audio.ensureContext();
        resetGame();
        gameState = 'PLAYING';
        startModal.classList.add('hidden');
        gameOverModal.classList.add('hidden');
        hudLayer.classList.remove('hidden');
      }

      function triggerGameOver() {
        if (gameState === 'GAMEOVER') return;
        gameState = 'GAMEOVER';
        setHammerMode(false);
        audio.playGameOver();

        const isNewRecord = score > 0 && score >= bestScore;
        finalScoreEl.textContent = String(score);
        finalBestEl.textContent = String(bestScore);
        newRecordNote.classList.toggle('visible', isNewRecord);
        gameOverModal.classList.remove('hidden');
      }

      // =========================================================
      // 8. PARTICLE & VFX SPAWNERS
      // =========================================================
      function spawnCrystalBurst(x, y, level, count = 22) {
        const def = LEVELS[level];
        for (let i = 0; i < count; i++) {
          const ang = (i / count) * Math.PI * 2 + (Math.random() - 0.5) * 0.45;
          const speed = 90 + Math.random() * (180 + level * 20);
          const color = def.rainbow
            ? `hsl(${Math.floor(Math.random() * 360)}, 95%, 72%)`
            : Math.random() < 0.45 ? def.c1 : def.c2;
          particles.push({
            x,
            y,
            vx: Math.cos(ang) * speed,
            vy: Math.sin(ang) * speed - 40,
            size: 3 + Math.random() * (4.5 + level * 0.4),
            rot: Math.random() * Math.PI * 2,
            vRot: (Math.random() - 0.5) * 12,
            life: 0,
            maxLife: 0.45 + Math.random() * 0.35,
            color
          });
        }
        shockwaves.push({
          x,
          y,
          r: def.r * 0.5,
          maxR: def.r * 2.4 + 28,
          life: 0,
          maxLife: 0.38,
          color: def.rainbow ? '#ffffff' : def.c2
        });
      }

      function addScore(points, x, y, labelSuffix = '') {
        score += points;
        if (score > bestScore) {
          bestScore = score;
          try {
            localStorage.setItem('crystal_merge_best', String(bestScore));
          } catch (_) {}
        }
        updateScoreUI();
        floatingTexts.push({
          x,
          y: y - 10,
          text: `+${points}${labelSuffix}`,
          life: 0,
          maxLife: 0.85,
          color: labelSuffix ? '#fde047' : '#ffffff'
        });
      }

      // =========================================================
      // 9. REALISTIC 2D CIRCLE PHYSICS ENGINE
      // =========================================================
      function stepPhysics(dt) {
        const SUBSTEPS = 8;
        const subDt = dt / SUBSTEPS;

        // Track merges across substeps
        const mergedIds = new Set();
        const mergePairs = [];

        for (let step = 0; step < SUBSTEPS; step++) {
          // 1) Integrate forces
          for (let i = 0; i < crystals.length; i++) {
            const c = crystals[i];
            if (mergedIds.has(c.id)) continue;

            c.vy += GRAVITY * subDt;
            c.vx *= 0.9992;
            c.vy *= 0.9992;
            c.omega *= 0.996;

            c.x += c.vx * subDt;
            c.y += c.vy * subDt;
            c.angle += c.omega * subDt;
          }

          // 2) Circle-Circle collisions
          const n = crystals.length;
          for (let i = 0; i < n; i++) {
            const a = crystals[i];
            if (mergedIds.has(a.id)) continue;

            for (let j = i + 1; j < n; j++) {
              const b = crystals[j];
              if (mergedIds.has(b.id)) continue;

              const dx = b.x - a.x;
              const dy = b.y - a.y;
              const minDist = a.r + b.r;
              const distSq = dx * dx + dy * dy;

              if (distSq < minDist * minDist) {
                // Same level -> queue merge!
                if (a.level === b.level) {
                  mergedIds.add(a.id);
                  mergedIds.add(b.id);
                  mergePairs.push([a, b]);
                  continue;
                }

                const dist = Math.sqrt(distSq) || 0.0001;
                const nx = dx / dist;
                const ny = dy / dist;
                const overlap = minDist - dist;

                const invMassA = 1 / (a.r * a.r);
                const invMassB = 1 / (b.r * b.r);
                const invMassSum = invMassA + invMassB;

                // Positional separation with tiny slop for calm resting stacks
                const slop = 0.02;
                const corr = Math.max(0, overlap - slop) * 0.85 / invMassSum;
                a.x -= nx * corr * invMassA;
                a.y -= ny * corr * invMassA;
                b.x += nx * corr * invMassB;
                b.y += ny * corr * invMassB;

                // Relative velocity along normal
                const rvx = b.vx - a.vx;
                const rvy = b.vy - a.vy;
                const vn = rvx * nx + rvy * ny;

                if (vn < 0) {
                  const restitution = Math.abs(vn) < 38 ? 0.0 : 0.24;
                  const jn = -(1 + restitution) * vn / invMassSum;

                  a.vx -= jn * nx * invMassA;
                  a.vy -= jn * ny * invMassA;
                  b.vx += jn * nx * invMassB;
                  b.vy += jn * ny * invMassB;

                  // Tangential friction & spin transfer
                  const tx = -ny;
                  const ty = nx;
                  const vt = (b.vx - a.vx) * tx + (b.vy - a.vy) * ty - (a.omega * a.r + b.omega * b.r);
                  const invInertiaA = 2 / (a.r * a.r * a.r * a.r); // 1 / (0.5 * m * r^2) where m=r^2
                  const invInertiaB = 2 / (b.r * b.r * b.r * b.r);
                  const effTangMass = invMassSum + (a.r * a.r) * invInertiaA + (b.r * b.r) * invInertiaB;

                  let jt = -vt / effTangMass;
                  const mu = 0.22;
                  const maxJt = jn * mu;
                  if (jt > maxJt) jt = maxJt;
                  if (jt < -maxJt) jt = -maxJt;

                  a.vx -= jt * tx * invMassA;
                  a.vy -= jt * ty * invMassA;
                  b.vx += jt * tx * invMassB;
                  b.vy += jt * ty * invMassB;

                  a.omega -= jt * a.r * invInertiaA;
                  b.omega -= jt * b.r * invInertiaB;

                  if (step === 0 && vn < -130) {
                    audio.playClink(Math.min(1, Math.abs(vn) / 600));
                  }
                }
              }
            }
          }

          // 3) Glass container walls, rounded corners & bottom floor
          for (let i = 0; i < crystals.length; i++) {
            const c = crystals[i];
            if (mergedIds.has(c.id)) continue;
            const r = c.r;

            // Left wall
            if (c.x - r < 0) {
              c.x = r;
              if (c.vx < 0) {
                c.vx = Math.abs(c.vx) < 20 ? 0 : -c.vx * 0.28;
                c.vy *= 0.96;
                c.omega -= (c.vy / r + c.omega) * 0.08;
              }
            }
            // Right wall
            if (c.x + r > WORLD_W) {
              c.x = WORLD_W - r;
              if (c.vx > 0) {
                c.vx = Math.abs(c.vx) < 20 ? 0 : -c.vx * 0.28;
                c.vy *= 0.96;
                c.omega += (c.vy / r - c.omega) * 0.08;
              }
            }
            // Bottom floor
            if (c.y + r > WORLD_H) {
              c.y = WORLD_H - r;
              if (c.vy > 0) {
                if (c.vy > 140 && step === 0) {
                  audio.playClink(Math.min(1, c.vy / 650));
                }
                c.vy = Math.abs(c.vy) < 24 ? 0 : -c.vy * 0.25;
                c.vx *= 0.95;
                c.omega += (c.vx / r - c.omega) * 0.16;
              }
            }

            // Rounded bottom corners so small crystals roll cleanly inward
            if (c.y > WORLD_H - CORNER_R) {
              if (c.x < CORNER_R) {
                const cx = CORNER_R;
                const cy = WORLD_H - CORNER_R;
                const dx = c.x - cx;
                const dy = c.y - cy;
                const dist = Math.hypot(dx, dy);
                const maxD = CORNER_R - r;
                if (maxD > 0 && dist > maxD) {
                  const nx = dx / dist;
                  const ny = dy / dist;
                  c.x = cx + nx * maxD;
                  c.y = cy + ny * maxD;
                  const vn = c.vx * nx + c.vy * ny;
                  if (vn > 0) {
                    c.vx -= 1.2 * vn * nx;
                    c.vy -= 1.2 * vn * ny;
                  }
                }
              } else if (c.x > WORLD_W - CORNER_R) {
                const cx = WORLD_W - CORNER_R;
                const cy = WORLD_H - CORNER_R;
                const dx = c.x - cx;
                const dy = c.y - cy;
                const dist = Math.hypot(dx, dy);
                const maxD = CORNER_R - r;
                if (maxD > 0 && dist > maxD) {
                  const nx = dx / dist;
                  const ny = dy / dist;
                  c.x = cx + nx * maxD;
                  c.y = cy + ny * maxD;
                  const vn = c.vx * nx + c.vy * ny;
                  if (vn > 0) {
                    c.vx -= 1.2 * vn * nx;
                    c.vy -= 1.2 * vn * ny;
                  }
                }
              }
            }
          }
        }

        // 4) Execute queued merges
        if (mergePairs.length > 0) {
          crystals = crystals.filter((c) => !mergedIds.has(c.id));

          for (const [a, b] of mergePairs) {
            if (comboTimer > 0) {
              comboCount = Math.min(8, comboCount + 1);
            } else {
              comboCount = 1;
            }
            comboTimer = 1.5;

            const mx = (a.x + b.x) * 0.5;
            const my = (a.y + b.y) * 0.5;

            if (a.level === LEVELS.length - 1) {
              // Two Rainbow Diamonds -> Prismatic Supernova!
              diamondVault += 2;
              try {
                localStorage.setItem('crystal_merge_diamonds', String(diamondVault));
              } catch (_) {}
              spawnCrystalBurst(mx, my, a.level, 48);
              shockwaves.push({
                x: mx,
                y: my,
                r: 40,
                maxR: 260,
                life: 0,
                maxLife: 0.55,
                color: '#fde047'
              });
              microShake = 8;
              audio.playMerge(9, comboCount + 2);
              addScore(2048 * comboCount, mx, my, ' СВЕРХНОВА!');
              showToast('Сверхнова! +2 алмаза в шкатулку');
            } else {
              const newLvl = a.level + 1;
              const def = LEVELS[newLvl];
              const clampedX = Math.max(def.r + 1, Math.min(WORLD_W - def.r - 1, mx));
              const clampedY = Math.min(WORLD_H - def.r - 1, my);

              crystals.push({
                id: nextId++,
                level: newLvl,
                r: def.r,
                x: clampedX,
                y: clampedY,
                vx: (a.vx + b.vx) * 0.35,
                vy: Math.min(-65, (a.vy + b.vy) * 0.35 - 55),
                angle: (a.angle + b.angle) * 0.5,
                omega: (a.omega + b.omega) * 0.4,
                age: 0.45, // brief grace if newly formed crystal nudges danger line
                popScale: 0.52
              });

              if (newLvl === LEVELS.length - 1) {
                diamondVault += 1;
                try {
                  localStorage.setItem('crystal_merge_diamonds', String(diamondVault));
                } catch (_) {}
                showToast('Радужный алмаз сложен в шкатулку!');
              }

              if (!unlockedLevels.has(newLvl)) {
                unlockedLevels.add(newLvl);
                syncEvolutionUI();
              }

              spawnCrystalBurst(clampedX, clampedY, newLvl, 18 + newLvl * 2);
              if (newLvl >= 5) microShake = Math.max(microShake, 2.5 + (newLvl - 4) * 1.1);
              audio.playMerge(newLvl, comboCount);
              const pts = def.score * comboCount;
              const suffix = comboCount > 1 ? ` x${comboCount}` : '';
              addScore(pts, clampedX, clampedY, suffix);
            }
          }
        }
      }

      // =========================================================
      // 10. AIMING RAYCAST & DROP ACTIONS
      // =========================================================
      function computeAimDropY(x, r) {
        let bestY = WORLD_H - r;
        for (let i = 0; i < crystals.length; i++) {
          const c = crystals[i];
          const sumR = c.r + r;
          const dx = Math.abs(c.x - x);
          if (dx < sumR) {
            const dy = Math.sqrt(sumR * sumR - dx * dx);
            const hitY = c.y - dy;
            if (hitY < bestY && hitY > SPAWN_Y) {
              bestY = hitY;
            }
          }
        }
        return bestY;
      }

      function dropCrystal() {
        if (gameState !== 'PLAYING' || !canDrop || hammerMode) return;
        const def = LEVELS[currentLevel];
        const clampedX = Math.max(def.r + 3, Math.min(WORLD_W - def.r - 3, aimX));

        crystals.push({
          id: nextId++,
          level: currentLevel,
          r: def.r,
          x: clampedX,
          y: SPAWN_Y,
          vx: (Math.random() - 0.5) * 6,
          vy: 45,
          angle: Math.random() * Math.PI * 2,
          omega: (Math.random() - 0.5) * 1.4,
          age: 0,
          popScale: 1
        });

        audio.playDrop();
        canDrop = false;
        canHold = true;
        dropTimer = DROP_COOLDOWN;

        currentLevel = nextLevel;
        nextLevel = pickSpawnLevel();
        unlockedLevels.add(currentLevel);
        unlockedLevels.add(nextLevel);
        updateNextUI();
        updateHoldUI();
        syncEvolutionUI();

        const nextR = LEVELS[currentLevel].r;
        aimX = Math.max(nextR + 3, Math.min(WORLD_W - nextR - 3, aimX));
      }

      function swapHoldCrystal() {
        if (gameState !== 'PLAYING' || !canDrop || hammerMode) return;
        if (!canHold) {
          showToast('Сначала сбросьте текущий кристалл');
          return;
        }
        audio.ensureContext();
        if (holdLevel === null) {
          holdLevel = currentLevel;
          currentLevel = nextLevel;
          nextLevel = pickSpawnLevel();
          unlockedLevels.add(currentLevel);
          unlockedLevels.add(nextLevel);
          updateNextUI();
          syncEvolutionUI();
          showToast(`В резерве: ${LEVELS[holdLevel].short}`);
        } else {
          const tmp = currentLevel;
          currentLevel = holdLevel;
          holdLevel = tmp;
          showToast(`Замена: ${LEVELS[currentLevel].short}`);
        }
        canHold = false;
        updateHoldUI();
        const r = LEVELS[currentLevel].r;
        aimX = Math.max(r + 3, Math.min(WORLD_W - r - 3, aimX));
      }

      function findCrystalAtWorld(wx, wy) {
        for (let i = crystals.length - 1; i >= 0; i--) {
          const c = crystals[i];
          const dx = wx - c.x;
          const dy = wy - c.y;
          if (dx * dx + dy * dy <= (c.r + 8) * (c.r + 8)) {
            return c;
          }
        }
        return null;
      }

      function shatterCrystalWithHammer(target) {
        crystals = crystals.filter((c) => c.id !== target.id);
        spawnCrystalBurst(target.x, target.y, target.level, 30);
        microShake = 6;
        audio.playHammer();
        setHammerMode(false);
        showToast(`Разбит кристалл: ${LEVELS[target.level].short}`);
      }

      function executeShakeBonus() {
        if (crystals.length === 0) {
          showToast('В стакане пока нет кристаллов');
          return;
        }
        shakeTimer = 0.55;
        microShake = 9;
        dangerTimer = Math.max(0, dangerTimer - 0.9);
        audio.playShake();

        for (let i = 0; i < crystals.length; i++) {
          const c = crystals[i];
          c.vy -= 260 + Math.random() * 180;
          c.vx += (Math.random() - 0.5) * 340;
          c.omega += (Math.random() - 0.5) * 10;
        }
      }

      // =========================================================
      // 11. INPUT HANDLING (MOUSE + TOUCH + KEYBOARD)
      // =========================================================
      let isPointerDown = false;
      let activeTouchId = null;

      function updateAimFromClientX(clientX) {
        const w = screenToWorld(clientX, 0);
        const r = LEVELS[currentLevel].r;
        aimX = Math.max(r + 3, Math.min(WORLD_W - r - 3, w.x));
      }

      canvas.addEventListener('pointerdown', (e) => {
        if (gameState !== 'PLAYING') return;
        audio.ensureContext();

        if (hammerMode) {
          const w = screenToWorld(e.clientX, e.clientY);
          const hit = findCrystalAtWorld(w.x, w.y);
          if (hit) {
            shatterCrystalWithHammer(hit);
          } else {
            showToast('Нажмите прямо на кристалл внутри стакана');
          }
          return;
        }

        isPointerDown = true;
        activeTouchId = e.pointerId;
        updateAimFromClientX(e.clientX);
      });

      window.addEventListener('pointermove', (e) => {
        if (gameState !== 'PLAYING') return;
        if (hammerMode) {
          const w = screenToWorld(e.clientX, e.clientY);
          const hit = findCrystalAtWorld(w.x, w.y);
          hoveredCrystalId = hit ? hit.id : null;
          return;
        }
        if (e.pointerType === 'mouse' || (isPointerDown && e.pointerId === activeTouchId)) {
          updateAimFromClientX(e.clientX);
        }
      });

      window.addEventListener('pointerup', (e) => {
        if (gameState !== 'PLAYING') return;
        if (!hammerMode && isPointerDown && e.pointerId === activeTouchId) {
          updateAimFromClientX(e.clientX);
          isPointerDown = false;
          activeTouchId = null;
          dropCrystal();
        }
      });

      window.addEventListener('pointercancel', () => {
        isPointerDown = false;
        activeTouchId = null;
      });

      window.addEventListener('keydown', (e) => {
        if (gameState === 'TITLE' && (e.code === 'Enter' || e.code === 'Space')) {
          e.preventDefault();
          startGame();
        } else if (gameState === 'PLAYING') {
          if (e.code === 'ArrowLeft' || e.code === 'KeyA') {
            const r = LEVELS[currentLevel].r;
            aimX = Math.max(r + 3, aimX - 18);
          } else if (e.code === 'ArrowRight' || e.code === 'KeyD') {
            const r = LEVELS[currentLevel].r;
            aimX = Math.min(WORLD_W - r - 3, aimX + 18);
          } else if (e.code === 'Space' || e.code === 'ArrowDown') {
            e.preventDefault();
            dropCrystal();
          } else if (e.code === 'KeyC' || e.code === 'ShiftLeft' || e.code === 'ShiftRight') {
            e.preventDefault();
            swapHoldCrystal();
          } else if (e.code === 'Escape' && hammerMode) {
            setHammerMode(false);
          }
        }
      });

      // UI Buttons
      playBtn.addEventListener('click', startGame);
      holdBox.addEventListener('click', swapHoldCrystal);

      restartBtn.addEventListener('click', () => {
        showFullscreenAd(() => {
          startGame();
        });
      });

      shareBtn.addEventListener('click', async () => {
        const message = 'Мой рекорд в игре «Эволюция Кристаллов»: ' + score + ' очков! Сможешь побить?';
        if (!isVKBridgeAvailable() || !isEmbeddedInVK()) {
          showToast('Публикация доступна внутри ВКонтакте');
          return;
        }
        try {
          await vkBridge.send('VKWebAppShowWallPostBox', { message });
          showToast('Рекорд опубликован на стене!');
        } catch (_) {
          // Игрок закрыл окно публикации или отменил отправку
        }
      });

      soundBtn.addEventListener('click', () => {
        audio.toggleMute();
        syncSoundUI();
      });

      hammerCancelBtn.addEventListener('click', () => {
        setHammerMode(false);
      });

      hammerBtn.addEventListener('click', () => {
        if (gameState !== 'PLAYING') return;
        if (hammerMode) {
          setHammerMode(false);
          return;
        }
        if (crystals.length === 0) {
          showToast('В стакане пока нет кристаллов');
          return;
        }
        showRewardedAd(() => {
          setHammerMode(true);
        });
      });

      shakeBtn.addEventListener('click', () => {
        if (gameState !== 'PLAYING') return;
        if (crystals.length === 0) {
          showToast('В стакане пока нет кристаллов');
          return;
        }
        setHammerMode(false);
        showRewardedAd(() => {
          executeShakeBonus();
        });
      });

      document.addEventListener('visibilitychange', () => {
        if (document.hidden) {
          audio.pauseForAd();
        } else if (!isAdShowing) {
          audio.resumeFromAd();
        }
      });

      window.addEventListener('resize', computeLayout);

      // =========================================================
      // 12. MAIN GAME LOOP & RENDERING
      // =========================================================
      let lastFrameTime = performance.now();

      function update(dt) {
        elapsedTime += dt;

        // Ambient cosmic dust
        for (let i = 0; i < nebulaMotes.length; i++) {
          const m = nebulaMotes[i];
          m.x += m.vx * dt;
          m.y += m.vy * dt;
          if (m.y < -0.02) m.y = 1.02;
          if (m.x < -0.02) m.x = 1.02;
          if (m.x > 1.02) m.x = -0.02;
        }

        // Particles & Shockwaves
        for (let i = particles.length - 1; i >= 0; i--) {
          const p = particles[i];
          p.life += dt;
          if (p.life >= p.maxLife) {
            particles.splice(i, 1);
            continue;
          }
          p.vy += 420 * dt;
          p.x += p.vx * dt;
          p.y += p.vy * dt;
          p.rot += p.vRot * dt;
        }

        for (let i = shockwaves.length - 1; i >= 0; i--) {
          const s = shockwaves[i];
          s.life += dt;
          if (s.life >= s.maxLife) shockwaves.splice(i, 1);
        }

        for (let i = floatingTexts.length - 1; i >= 0; i--) {
          const f = floatingTexts[i];
          f.life += dt;
          f.y -= 36 * dt;
          if (f.life >= f.maxLife) floatingTexts.splice(i, 1);
        }

        if (gameState !== 'PLAYING') return;

        if (!canDrop) {
          dropTimer -= dt;
          if (dropTimer <= 0) {
            canDrop = true;
          }
        }

        if (comboTimer > 0) {
          comboTimer -= dt;
          if (comboTimer <= 0) comboCount = 0;
        }

        const targetComboGlow = (comboCount >= 2 && comboTimer > 0)
          ? Math.min(1, 0.35 + (comboCount - 2) * 0.16)
          : 0;
        const glowRate = targetComboGlow > comboGlow ? 9.0 : 2.8;
        comboGlow += (targetComboGlow - comboGlow) * Math.min(1, dt * glowRate);

        if (shakeTimer > 0) shakeTimer = Math.max(0, shakeTimer - dt);
        if (microShake > 0) microShake = Math.max(0, microShake - dt * 28);

        // Age & popScale animation
        for (let i = 0; i < crystals.length; i++) {
          const c = crystals[i];
          c.age += dt;
          if (c.popScale < 1) {
            c.popScale = Math.min(1, c.popScale + dt * 4.2);
          }
        }

        stepPhysics(dt);

        // Overflow 3-second check
        let anyInDanger = false;
        for (let i = 0; i < crystals.length; i++) {
          const c = crystals[i];
          c.inDanger = false;
          if (c.age > 1.15 && (c.y - c.r) < DANGER_Y) {
            anyInDanger = true;
            c.inDanger = true;
          }
        }

        if (anyInDanger) {
          dangerTimer += dt;
          if (dangerTimer >= LOSS_TIME_LIMIT) {
            dangerTimer = LOSS_TIME_LIMIT;
            triggerGameOver();
          }
        } else {
          dangerTimer = Math.max(0, dangerTimer - dt * 2.4);
        }
      }

      function renderBackdrop() {
        // Deep cosmic nebula gradient
        const bgGrad = ctx.createRadialGradient(
          viewW * 0.5, viewH * 0.25, 20,
          viewW * 0.5, viewH * 0.5, Math.max(viewW, viewH) * 0.85
        );
        bgGrad.addColorStop(0, '#141b44');
        bgGrad.addColorStop(0.45, '#090d24');
        bgGrad.addColorStop(1, '#040510');
        ctx.fillStyle = bgGrad;
        ctx.fillRect(0, 0, viewW, viewH);

        // Soft glowing nebula clouds
        const n1 = ctx.createRadialGradient(viewW * 0.2, viewH * 0.3, 10, viewW * 0.2, viewH * 0.3, viewW * 0.35);
        n1.addColorStop(0, 'rgba(88, 28, 135, 0.16)');
        n1.addColorStop(1, 'rgba(88, 28, 135, 0)');
        ctx.fillStyle = n1;
        ctx.fillRect(0, 0, viewW, viewH);

        const n2 = ctx.createRadialGradient(viewW * 0.8, viewH * 0.7, 10, viewW * 0.8, viewH * 0.7, viewW * 0.38);
        n2.addColorStop(0, 'rgba(14, 116, 144, 0.14)');
        n2.addColorStop(1, 'rgba(14, 116, 144, 0)');
        ctx.fillStyle = n2;
        ctx.fillRect(0, 0, viewW, viewH);

        // Twinkling starfield
        for (let i = 0; i < stars.length; i++) {
          const s = stars[i];
          const tw = 0.35 + 0.65 * (0.5 + 0.5 * Math.sin(elapsedTime * s.speed + s.phase));
          ctx.fillStyle = `rgba(224, 242, 254, ${tw * 0.75})`;
          ctx.beginPath();
          ctx.arc(s.x * viewW, s.y * viewH, s.size, 0, Math.PI * 2);
          ctx.fill();
        }

        // Drifting luminous stardust motes
        for (let i = 0; i < nebulaMotes.length; i++) {
          const m = nebulaMotes[i];
          ctx.fillStyle = m.color;
          ctx.beginPath();
          ctx.arc(m.x * viewW, m.y * viewH, m.r, 0, Math.PI * 2);
          ctx.fill();
        }
      }

      function renderGlassContainer() {
        const x = 0;
        const y = 62;
        const w = WORLD_W;
        const h = WORLD_H - y;
        const r = CORNER_R;

        // Interior dark glass backdrop
        ctx.save();

        // High-combo exterior & interior aura around the glass vessel
        if (comboGlow > 0.01) {
          const comboHue = comboCount >= 6
            ? (elapsedTime * 160) % 360
            : comboCount >= 4
              ? 42 + Math.sin(elapsedTime * 6) * 14
              : 195 + Math.sin(elapsedTime * 5) * 20;
          const pulseWave = 0.86 + 0.14 * Math.sin(elapsedTime * 9);
          const auraAlpha = comboGlow * pulseWave;

          // Soft radial energy bloom behind glass
          const comboBloom = ctx.createRadialGradient(
            w * 0.5, WORLD_H * 0.62, 40,
            w * 0.5, WORLD_H * 0.55, w * 0.92
          );
          comboBloom.addColorStop(0, `hsla(${comboHue}, 95%, 64%, ${auraAlpha * 0.26})`);
          comboBloom.addColorStop(0.55, `hsla(${(comboHue + 45) % 360}, 92%, 58%, ${auraAlpha * 0.14})`);
          comboBloom.addColorStop(1, 'rgba(0, 0, 0, 0)');
          ctx.fillStyle = comboBloom;
          ctx.fillRect(-70, y - 30, w + 140, h + 90);

          // Glowing outer rim halo
          ctx.save();
          ctx.beginPath();
          ctx.moveTo(x - 6, y);
          ctx.lineTo(x, y + 6);
          ctx.lineTo(x, WORLD_H - r);
          ctx.quadraticCurveTo(x, WORLD_H, x + r, WORLD_H);
          ctx.lineTo(w - r, WORLD_H);
          ctx.quadraticCurveTo(w, WORLD_H, w, WORLD_H - r);
          ctx.lineTo(w, y + 6);
          ctx.lineTo(w + 6, y);
          ctx.lineCap = 'round';
          ctx.shadowColor = `hsla(${comboHue}, 100%, 66%, ${auraAlpha * 0.95})`;
          ctx.shadowBlur = 18 + comboGlow * 22;
          ctx.lineWidth = 6 + comboGlow * 4;
          ctx.strokeStyle = `hsla(${comboHue}, 98%, 70%, ${auraAlpha * 0.55})`;
          ctx.stroke();
          ctx.restore();
        }

        ctx.beginPath();
        ctx.moveTo(x, y);
        ctx.lineTo(x, WORLD_H - r);
        ctx.quadraticCurveTo(x, WORLD_H, x + r, WORLD_H);
        ctx.lineTo(w - r, WORLD_H);
        ctx.quadraticCurveTo(w, WORLD_H, w, WORLD_H - r);
        ctx.lineTo(w, y);
        ctx.closePath();

        const glassFill = ctx.createLinearGradient(0, y, 0, WORLD_H);
        glassFill.addColorStop(0, 'rgba(15, 23, 54, 0.42)');
        glassFill.addColorStop(0.5, 'rgba(11, 16, 40, 0.58)');
        glassFill.addColorStop(1, 'rgba(20, 30, 72, 0.74)');
        ctx.fillStyle = glassFill;
        ctx.fill();

        // Subtle inner edge combo shimmer
        if (comboGlow > 0.01) {
          const comboHue = comboCount >= 6
            ? (elapsedTime * 160) % 360
            : comboCount >= 4
              ? 42
              : 195;
          const innerGlow = ctx.createLinearGradient(0, WORLD_H, 0, y);
          innerGlow.addColorStop(0, `hsla(${comboHue}, 95%, 65%, ${comboGlow * 0.22})`);
          innerGlow.addColorStop(0.45, `hsla(${(comboHue + 35) % 360}, 90%, 60%, ${comboGlow * 0.08})`);
          innerGlow.addColorStop(1, 'rgba(0, 0, 0, 0)');
          ctx.fillStyle = innerGlow;
          ctx.fill();
        }

        // Subtle vertical specular glass streaks inside container
        const streakGrad = ctx.createLinearGradient(12, y, 42, y);
        streakGrad.addColorStop(0, 'rgba(255, 255, 255, 0.08)');
        streakGrad.addColorStop(1, 'rgba(255, 255, 255, 0)');
        ctx.fillStyle = streakGrad;
        ctx.fillRect(10, y + 6, 30, h - r);

        const streakGradR = ctx.createLinearGradient(w - 28, y, w - 8, y);
        streakGradR.addColorStop(0, 'rgba(255, 255, 255, 0)');
        streakGradR.addColorStop(1, 'rgba(186, 230, 253, 0.09)');
        ctx.fillStyle = streakGradR;
        ctx.fillRect(w - 28, y + 6, 20, h - r);

        // Glass outer outline (open top lip -> walls -> rounded base)
        ctx.beginPath();
        ctx.moveTo(x - 6, y);
        ctx.lineTo(x, y + 6);
        ctx.lineTo(x, WORLD_H - r);
        ctx.quadraticCurveTo(x, WORLD_H, x + r, WORLD_H);
        ctx.lineTo(w - r, WORLD_H);
        ctx.quadraticCurveTo(w, WORLD_H, w, WORLD_H - r);
        ctx.lineTo(w, y + 6);
        ctx.lineTo(w + 6, y);

        const rimHue = comboCount >= 6
          ? (elapsedTime * 160) % 360
          : comboCount >= 4
            ? 45
            : 198;
        ctx.lineWidth = 5 + comboGlow * 1.5;
        ctx.strokeStyle = comboGlow > 0.02
          ? `hsla(${rimHue}, 95%, 72%, ${0.52 + comboGlow * 0.45})`
          : 'rgba(147, 197, 253, 0.58)';
        ctx.lineCap = 'round';
        ctx.stroke();

        ctx.lineWidth = 1.8;
        ctx.strokeStyle = comboGlow > 0.02
          ? `rgba(255, 255, 255, ${0.75 + comboGlow * 0.25})`
          : 'rgba(224, 242, 254, 0.85)';
        ctx.stroke();

        // Compact combo streak indicator on glass rim
        if (comboCount >= 2 && comboTimer > 0 && gameState === 'PLAYING') {
          const comboAlpha = Math.min(1, comboTimer * 1.6);
          const badgeHue = comboCount >= 6 ? (elapsedTime * 160) % 360 : comboCount >= 4 ? 45 : 195;
          ctx.save();
          ctx.globalAlpha = comboAlpha;
          ctx.font = '900 15px Montserrat, system-ui, sans-serif';
          ctx.textAlign = 'right';
          ctx.lineWidth = 4;
          ctx.strokeStyle = 'rgba(5, 8, 24, 0.88)';
          const comboText = `КОМБО x${comboCount}`;
          ctx.strokeText(comboText, WORLD_W - 12, y + 24);
          ctx.fillStyle = `hsl(${badgeHue}, 98%, 74%)`;
          ctx.fillText(comboText, WORLD_W - 12, y + 24);
          ctx.restore();
        }

        // Dashed Red Overflow Danger Line
        const dangerRatio = Math.min(1, dangerTimer / LOSS_TIME_LIMIT);
        const pulse = dangerTimer > 0 ? 0.55 + 0.45 * Math.sin(elapsedTime * 14) : 0.65;
        ctx.save();
        ctx.beginPath();
        ctx.setLineDash([10, 8]);
        ctx.moveTo(6, DANGER_Y);
        ctx.lineTo(WORLD_W - 6, DANGER_Y);
        ctx.lineWidth = dangerTimer > 0 ? 2.8 : 2;
        ctx.strokeStyle = `rgba(255, 77, 109, ${pulse})`;
        ctx.stroke();
        ctx.setLineDash([]);
        ctx.restore();

        // Visual 3-second Overflow Timer Bar & Countdown when crystals linger above line
        if (dangerTimer > 0.12 && gameState === 'PLAYING') {
          const remain = Math.max(0, LOSS_TIME_LIMIT - dangerTimer);
          const barW = 140;
          const barH = 8;
          const bx = WORLD_W / 2 - barW / 2;
          const by = DANGER_Y - 26;

          ctx.fillStyle = 'rgba(10, 12, 28, 0.85)';
          ctx.beginPath();
          ctx.roundRect(bx - 10, by - 22, barW + 20, 36, 10);
          ctx.fill();
          ctx.strokeStyle = 'rgba(255, 77, 109, 0.75)';
          ctx.lineWidth = 1.4;
          ctx.stroke();

          ctx.fillStyle = '#ffccd5';
          ctx.font = '800 13px Montserrat, system-ui, sans-serif';
          ctx.textAlign = 'center';
          ctx.fillText(`Переполнение: ${remain.toFixed(1)} с`, WORLD_W / 2, by - 6);

          ctx.fillStyle = 'rgba(255, 255, 255, 0.14)';
          ctx.beginPath();
          ctx.roundRect(bx, by, barW, barH, 4);
          ctx.fill();

          ctx.fillStyle = '#ff4d6d';
          ctx.beginPath();
          ctx.roundRect(bx, by, barW * (1 - dangerRatio), barH, 4);
          ctx.fill();
        }

        ctx.restore();
      }

      function renderAimAndCurrentCrystal() {
        if (gameState !== 'PLAYING' || !canDrop || hammerMode) return;
        const def = LEVELS[currentLevel];
        const x = Math.max(def.r + 3, Math.min(WORLD_W - def.r - 3, aimX));
        const targetY = computeAimDropY(x, def.r);

        // Vertical laser guide line
        const lineGrad = ctx.createLinearGradient(x, SPAWN_Y + def.r, x, targetY);
        lineGrad.addColorStop(0, 'rgba(224, 242, 254, 0.65)');
        lineGrad.addColorStop(1, 'rgba(56, 189, 248, 0.08)');
        ctx.save();
        ctx.beginPath();
        ctx.setLineDash([5, 6]);
        ctx.moveTo(x, SPAWN_Y + def.r);
        ctx.lineTo(x, targetY);
        ctx.lineWidth = 1.8;
        ctx.strokeStyle = lineGrad;
        ctx.stroke();
        ctx.setLineDash([]);

        // Faint ghost landing ring
        ctx.beginPath();
        ctx.arc(x, targetY, def.r, 0, Math.PI * 2);
        ctx.strokeStyle = 'rgba(255, 255, 255, 0.15)';
        ctx.lineWidth = 1.2;
        ctx.stroke();
        ctx.restore();

        // Current crystal waiting at top
        drawCrystal(ctx, x, SPAWN_Y, def.r, currentLevel, Math.sin(elapsedTime * 1.5) * 0.12, elapsedTime);
      }

      function renderParticlesAndPopups() {
        // Shockwave rings
        for (let i = 0; i < shockwaves.length; i++) {
          const s = shockwaves[i];
          const t = s.life / s.maxLife;
          const r = s.r + (s.maxR - s.r) * (1 - Math.pow(1 - t, 3));
          ctx.save();
          ctx.globalAlpha = (1 - t) * 0.7;
          ctx.strokeStyle = s.color;
          ctx.lineWidth = 3 * (1 - t) + 1;
          ctx.beginPath();
          ctx.arc(s.x, s.y, r, 0, Math.PI * 2);
          ctx.stroke();
          ctx.restore();
        }

        // Crystal shard particles
        for (let i = 0; i < particles.length; i++) {
          const p = particles[i];
          const t = p.life / p.maxLife;
          ctx.save();
          ctx.translate(p.x, p.y);
          ctx.rotate(p.rot);
          ctx.globalAlpha = 1 - t;
          ctx.fillStyle = p.color;
          const s = p.size * (1 - t * 0.4);
          ctx.beginPath();
          ctx.moveTo(0, -s);
          ctx.lineTo(s * 0.75, 0);
          ctx.lineTo(0, s);
          ctx.lineTo(-s * 0.75, 0);
          ctx.closePath();
          ctx.fill();
          ctx.restore();
        }

        // Floating score popups
        for (let i = 0; i < floatingTexts.length; i++) {
          const f = floatingTexts[i];
          const t = f.life / f.maxLife;
          ctx.save();
          ctx.globalAlpha = Math.min(1, (1 - t) * 1.4);
          ctx.font = '800 18px Montserrat, system-ui, sans-serif';
          ctx.textAlign = 'center';
          ctx.lineWidth = 4;
          ctx.strokeStyle = 'rgba(5, 8, 24, 0.85)';
          ctx.strokeText(f.text, f.x, f.y);
          ctx.fillStyle = f.color;
          ctx.fillText(f.text, f.x, f.y);
          ctx.restore();
        }
      }

      function render() {
        ctx.save();
        ctx.scale(dpr, dpr);

        renderBackdrop();

        // Compute container shake offset
        let sx = 0;
        let sy = 0;
        if (shakeTimer > 0) {
          const mag = (shakeTimer / 0.55) * 10;
          sx += Math.sin(elapsedTime * 55) * mag;
          sy += Math.cos(elapsedTime * 48) * mag * 0.6;
        }
        if (microShake > 0) {
          sx += (Math.random() - 0.5) * microShake;
          sy += (Math.random() - 0.5) * microShake;
        }

        ctx.translate(worldOffsetX + sx * worldScale, worldOffsetY + sy * worldScale);
        ctx.scale(worldScale, worldScale);

        renderGlassContainer();
        renderAimAndCurrentCrystal();

        // Render all crystals inside container
        for (let i = 0; i < crystals.length; i++) {
          const c = crystals[i];
          drawCrystal(ctx, c.x, c.y, c.r, c.level, c.angle, elapsedTime, {
            scale: c.popScale,
            danger: c.inDanger,
            targeted: hammerMode && hoveredCrystalId === c.id
          });
        }

        renderParticlesAndPopups();

        ctx.restore();
      }

      function loop(now) {
        const rawDt = (now - lastFrameTime) / 1000;
        lastFrameTime = now;
        const dt = Math.min(Math.max(rawDt, 0), 0.05);

        update(dt);
        render();
        requestAnimationFrame(loop);
      }

      // =========================================================
      // 13. BOOTSTRAP
      // =========================================================
      buildEvolutionUI();
      initBackdropParticles();
      computeLayout();
      syncSoundUI();
      updateScoreUI();
      updateNextUI();
      updateHoldUI();
      syncEvolutionUI();
      initVKBridge();
      requestAnimationFrame(loop);
    })();
  </script>
</body>
</html>
