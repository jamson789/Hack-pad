
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>💀 HACKER'S DEN · Encrypted</title>
    <style>
        /* ============================================================
           BASE - HACKER THEME
        ============================================================ */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        @import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap');

        body {
            min-height: 100vh;
            background: #0a0a0a;
            font-family: 'Share Tech Mono', 'Courier New', monospace;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            overflow-x: hidden;
            position: relative;
        }

        /* ============================================================
           FOG / MIST BACKGROUND
        ============================================================ */
        .fog-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            overflow: hidden;
            background: #0a0a0a;
        }

        .fog-layer {
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: 
                radial-gradient(ellipse at 20% 30%, rgba(0, 255, 65, 0.06) 0%, transparent 50%),
                radial-gradient(ellipse at 80% 70%, rgba(0, 255, 65, 0.04) 0%, transparent 50%),
                radial-gradient(ellipse at 50% 50%, rgba(0, 255, 65, 0.03) 0%, transparent 60%);
            animation: fogMove1 25s ease-in-out infinite alternate;
        }

        .fog-layer:nth-child(2) {
            background: 
                radial-gradient(ellipse at 30% 60%, rgba(0, 200, 50, 0.04) 0%, transparent 40%),
                radial-gradient(ellipse at 70% 30%, rgba(0, 255, 65, 0.03) 0%, transparent 40%);
            animation: fogMove2 30s ease-in-out infinite alternate;
            opacity: 0.6;
        }

        .fog-layer:nth-child(3) {
            background: 
                radial-gradient(ellipse at 60% 80%, rgba(0, 255, 100, 0.03) 0%, transparent 30%);
            animation: fogMove3 20s ease-in-out infinite alternate;
            opacity: 0.4;
        }

        @keyframes fogMove1 {
            0% { transform: translate(0, 0) scale(1); }
            100% { transform: translate(5%, 3%) scale(1.1); }
        }

        @keyframes fogMove2 {
            0% { transform: translate(0, 0) scale(1); }
            100% { transform: translate(-4%, 5%) scale(1.15); }
        }

        @keyframes fogMove3 {
            0% { transform: translate(0, 0) scale(1); }
            100% { transform: translate(3%, -4%) scale(1.05); }
        }

        /* ============================================================
           HACKER BACKGROUND IMAGE (SVG matrix style)
        ============================================================ */
        .hacker-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            pointer-events: none;
            opacity: 0.04;
            background-image: 
                url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Ctext x='10' y='30' font-family='Courier' font-size='14' fill='%2300ff41' opacity='0.3'%3E01001010 01101000 01100001 01100011 01101011%3C/text%3E%3Ctext x='10' y='60' font-family='Courier' font-size='12' fill='%2300ff41' opacity='0.2'%3E01100101 01110010 00100000 01101101 01101111%3C/text%3E%3Ctext x='10' y='85' font-family='Courier' font-size='10' fill='%2300ff41' opacity='0.15'%3E01100100 01100101 00100000 01101000 01100001%3C/text%3E%3Ctext x='10' y='105' font-family='Courier' font-size='12' fill='%2300ff41' opacity='0.2'%3E01100011 01101011 01100101 01110010 01110011%3C/text%3E%3Ctext x='200' y='45' font-family='Courier' font-size='10' fill='%2300ff41' opacity='0.1'%3E01110011 01100101 01100011 01110101 01110010%3C/text%3E%3Ctext x='200' y='65' font-family='Courier' font-size='12' fill='%2300ff41' opacity='0.15'%3E01100101 00100000 01110100 01101000 01100101%3C/text%3E%3Ctext x='200' y='85' font-family='Courier' font-size='10' fill='%2300ff41' opacity='0.1'%3E00100000 01110111 01101111 01110010 01101100%3C/text%3E%3Ctext x='200' y='105' font-family='Courier' font-size='12' fill='%2300ff41' opacity='0.12'%3E01100100 00100000 01101000 01100001 01100011%3C/text%3E%3Ctext x='300' y='80' font-family='Courier' font-size='14' fill='%2300ff41' opacity='0.08'%3E01101011 00100000 01100101 01110010%3C/text%3E%3C/svg%3E");
            background-size: 400px 400px;
            background-repeat: repeat;
            animation: bgScroll 60s linear infinite;
        }

        @keyframes bgScroll {
            0% { transform: translate(0, 0); }
            100% { transform: translate(400px, 400px); }
        }

        /* ============================================================
           HACKER AVATAR / IMAGE in header
        ============================================================ */
        .hacker-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            border: 1px solid rgba(0, 255, 65, 0.15);
            background: rgba(0, 0, 0, 0.4);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            color: #00ff41;
            text-shadow: 0 0 30px rgba(0, 255, 65, 0.2);
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Ccircle cx='50' cy='40' r='22' fill='none' stroke='%2300ff41' stroke-width='1.5' opacity='0.3'/%3E%3Ccircle cx='50' cy='55' r='30' fill='none' stroke='%2300ff41' stroke-width='1.5' opacity='0.2'/%3E%3Ccircle cx='50' cy='45' r='4' fill='%2300ff41' opacity='0.3'/%3E%3Ccircle cx='50' cy='65' r='6' fill='%2300ff41' opacity='0.15'/%3E%3Cpath d='M35 75 L65 75' stroke='%2300ff41' stroke-width='1.5' opacity='0.15'/%3E%3C/svg%3E");
            background-size: cover;
            background-position: center;
        }

        /* ============================================================
           MATRIX RAIN (visible)
        ============================================================ */
        .matrix-rain {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
            opacity: 0.06;
            font-family: 'Share Tech Mono', monospace;
            font-size: 16px;
            color: #00ff41;
            overflow: hidden;
            line-height: 1.4;
            text-shadow: 0 0 10px rgba(0, 255, 65, 0.1);
        }

        /* ============================================================
           MAIN TERMINAL CARD
        ============================================================ */
        .terminal {
            position: relative;
            z-index: 1;
            width: 100%;
            max-width: 980px;
            background: rgba(8, 8, 8, 0.92);
            border: 1px solid rgba(0, 255, 65, 0.12);
            border-radius: 16px;
            padding: 0;
            box-shadow: 
                0 0 80px rgba(0, 255, 65, 0.04),
                0 0 200px rgba(0, 255, 65, 0.02),
                inset 0 0 100px rgba(0, 255, 65, 0.02);
            backdrop-filter: blur(10px);
            overflow: hidden;
        }

        .terminal::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                repeating-linear-gradient(0deg, 
                    transparent,
                    transparent 2px,
                    rgba(0, 255, 65, 0.003) 2px,
                    rgba(0, 255, 65, 0.003) 4px
                );
            pointer-events: none;
            z-index: 0;
        }

        /* ============================================================
           TERMINAL HEADER
        ============================================================ */
        .terminal-header {
            background: rgba(0, 255, 65, 0.03);
            padding: 10px 24px;
            border-bottom: 1px solid rgba(0, 255, 65, 0.06);
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 10px;
            position: relative;
            z-index: 1;
        }

        .terminal-dots {
            display: flex;
            gap: 8px;
            align-items: center;
        }

        .dot-terminal {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            display: inline-block;
        }

        .dot-terminal.red { background: #ff1744; box-shadow: 0 0 10px rgba(255, 23, 68, 0.2); }
        .dot-terminal.yellow { background: #ffea00; box-shadow: 0 0 10px rgba(255, 234, 0, 0.2); }
        .dot-terminal.green { background: #00ff41; box-shadow: 0 0 15px rgba(0, 255, 65, 0.3); }

        .terminal-title {
            color: rgba(0, 255, 65, 0.4);
            font-size: 0.7rem;
            letter-spacing: 3px;
            text-transform: uppercase;
            font-weight: 400;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .terminal-title .blink {
            animation: blinkTerm 1s step-end infinite;
            color: #00ff41;
        }

        @keyframes blinkTerm {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }

        .terminal-status {
            color: rgba(0, 255, 65, 0.2);
            font-size: 0.6rem;
            letter-spacing: 1px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* ============================================================
           TERMINAL BODY
        ============================================================ */
        .terminal-body {
            padding: 24px 28px 20px;
            position: relative;
            z-index: 1;
        }

        /* ============================================================
           OUTPUT / DISPLAY AREA with Hacker Image
        ============================================================ */
        .display-area {
            background: rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(0, 255, 65, 0.04);
            border-radius: 8px;
            padding: 16px 20px;
            min-height: 130px;
            margin-bottom: 20px;
            font-size: 0.85rem;
            color: rgba(0, 255, 65, 0.5);
            line-height: 1.8;
            position: relative;
            font-family: 'Share Tech Mono', monospace;
            overflow: hidden;
        }

        /* Hacker image inside display area */
        .display-area::before {
            content: '';
            position: absolute;
            right: 10px;
            bottom: 10px;
            width: 80px;
            height: 80px;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 200 200'%3E%3Ccircle cx='100' cy='80' r='45' fill='none' stroke='%2300ff41' stroke-width='2' opacity='0.08'/%3E%3Ccircle cx='100' cy='80' r='30' fill='none' stroke='%2300ff41' stroke-width='1.5' opacity='0.06'/%3E%3Ccircle cx='100' cy='80' r='15' fill='%2300ff41' opacity='0.04'/%3E%3Cpath d='M60 110 L140 110' stroke='%2300ff41' stroke-width='2' opacity='0.06'/%3E%3Cpath d='M60 120 L140 120' stroke='%2300ff41' stroke-width='1.5' opacity='0.04'/%3E%3Ccircle cx='85' cy='75' r='4' fill='%2300ff41' opacity='0.06'/%3E%3Ccircle cx='115' cy='75' r='4' fill='%2300ff41' opacity='0.06'/%3E%3Cpath d='M90 90 Q100 100 110 90' stroke='%2300ff41' stroke-width='1.5' fill='none' opacity='0.06'/%3E%3Ctext x='20' y='160' font-family='Courier' font-size='10' fill='%2300ff41' opacity='0.04'%3E%3C/%3E%3Ctext x='20' y='175' font-family='Courier' font-size='8' fill='%2300ff41' opacity='0.03'%3Ehacker%3C/text%3E%3C/svg%3E");
            background-size: contain;
            background-repeat: no-repeat;
            opacity: 0.5;
            pointer-events: none;
        }

        .display-area .prompt {
            color: rgba(0, 255, 65, 0.3);
            position: relative;
            z-index: 1;
        }

        .display-area .prompt .cursor-line {
            display: inline-block;
            width: 8px;
            height: 1em;
            background: rgba(0, 255, 65, 0.15);
            animation: cursorBlinkHack 0.8s step-end infinite;
            vertical-align: text-bottom;
        }

        .display-area .hacker-text {
            color: #00ff41;
            text-shadow: 0 0 20px rgba(0, 255, 65, 0.05);
        }

        @keyframes cursorBlinkHack {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }

        /* ============================================================
           LOCK STATUS - HACKER STYLE
        ============================================================ */
        .lock-status {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 12px;
            padding: 10px 16px;
            background: rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(0, 255, 65, 0.03);
            border-radius: 8px;
            margin-bottom: 16px;
        }

        .lock-status .lock-icon {
            font-size: 1.2rem;
            color: rgba(0, 255, 65, 0.2);
        }

        .lock-status .lock-text {
            color: rgba(0, 255, 65, 0.2);
            font-size: 0.75rem;
            letter-spacing: 1px;
        }

        .lock-status .lock-text .highlight {
            color: #00ff41;
            text-shadow: 0 0 20px rgba(0, 255, 65, 0.1);
        }

        .lock-status .status-badge {
            padding: 2px 14px;
            border-radius: 4px;
            border: 1px solid rgba(0, 255, 65, 0.03);
            font-size: 0.6rem;
            color: rgba(0, 255, 65, 0.15);
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        .status-badge.active {
            border-color: rgba(0, 255, 65, 0.08);
            color: #00ff41;
            text-shadow: 0 0 20px rgba(0, 255, 65, 0.05);
        }

        /* ============================================================
           INPUT SECTION
        ============================================================ */
        .input-section {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-bottom: 16px;
        }

        .input-row-hack {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .input-row-hack input,
        .input-row-hack textarea {
            flex: 1;
            padding: 12px 16px;
            background: rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(0, 255, 65, 0.04);
            border-radius: 6px;
            color: rgba(0, 255, 65, 0.5);
            font-family: 'Share Tech Mono', monospace;
            font-size: 0.85rem;
            outline: none;
            transition: all 0.3s ease;
            min-width: 140px;
        }

        .input-row-hack input:focus,
        .input-row-hack textarea:focus {
            border-color: rgba(0, 255, 65, 0.08);
            background: rgba(0, 0, 0, 0.6);
            color: #00ff41;
            box-shadow: 0 0 30px rgba(0, 255, 65, 0.02);
        }

        .input-row-hack textarea {
            min-height: 100px;
            resize: vertical;
            font-family: 'Share Tech Mono', monospace;
        }

        .input-row-hack input::placeholder,
        .input-row-hack textarea::placeholder {
            color: rgba(0, 255, 65, 0.06);
        }

        /* ============================================================
           BUTTONS - HACKER STYLE (solid green)
        ============================================================ */
        .btn-hack {
            padding: 10px 24px;
            background: rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(0, 255, 65, 0.04);
            border-radius: 6px;
            color: rgba(0, 255, 65, 0.2);
            font-family: 'Share Tech Mono', monospace;
            font-size: 0.7rem;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            white-space: nowrap;
            position: relative;
            overflow: hidden;
        }

        .btn-hack::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(0, 255, 65, 0.03) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .btn-hack:hover::after {
            opacity: 1;
        }

        .btn-hack:hover {
            background: rgba(0, 255, 65, 0.02);
            border-color: rgba(0, 255, 65, 0.06);
            color: #00ff41;
            box-shadow: 0 0 30px rgba(0, 255, 65, 0.02);
        }

        .btn-hack:active {
            transform: scale(0.95);
        }

        .btn-hack.danger {
            border-color: rgba(255, 23, 68, 0.03);
            color: rgba(255, 23, 68, 0.15);
        }

        .btn-hack.danger:hover {
            border-color: rgba(255, 23, 68, 0.06);
            color: #ff1744;
            box-shadow: 0 0 30px rgba(255, 23, 68, 0.02);
            background: rgba(255, 23, 68, 0.02);
        }

        .btn-hack.success {
            border-color: rgba(0, 255, 65, 0.06);
            color: #00ff41;
            text-shadow: 0 0 20px rgba(0, 255, 65, 0.05);
        }

        .btn-hack.success:hover {
            border-color: rgba(0, 255, 65, 0.10);
            color: #33ff77;
            box-shadow: 0 0 40px rgba(0, 255, 65, 0.04);
            background: rgba(0, 255, 65, 0.02);
        }

        .btn-group-hack {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 4px;
        }

        /* ============================================================
           NOTES LIST - TERMINAL STYLE
        ============================================================ */
        #notesContainer {
            margin-top: 20px;
            max-height: 400px;
            overflow-y: auto;
        }

        .note-entry {
            padding: 10px 14px;
            border-left: 2px solid rgba(0, 255, 65, 0.03);
            border-bottom: 1px solid rgba(0, 255, 65, 0.02);
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 10px;
            transition: all 0.3s ease;
            background: rgba(0, 0, 0, 0.1);
            margin-bottom: 2px;
        }

        .note-entry:hover {
            background: rgba(0, 255, 65, 0.01);
            border-left-color: rgba(0, 255, 65, 0.06);
        }

        .note-entry .note-content {
            flex: 1;
            color: rgba(0, 255, 65, 0.4);
            font-size: 0.8rem;
            font-family: 'Share Tech Mono', monospace;
            word-break: break-word;
            line-height: 1.6;
        }

        .note-entry .note-content .highlight-note {
            color: #00ff41;
            text-shadow: 0 0 20px rgba(0, 255, 65, 0.03);
        }

        .note-entry .note-meta {
            color: rgba(0, 255, 65, 0.06);
            font-size: 0.55rem;
            letter-spacing: 0.5px;
        }

        .note-entry .note-actions {
            display: flex;
            gap: 2px;
        }

        .note-entry .note-actions button {
            background: none;
            border: none;
            color: rgba(0, 255, 65, 0.06);
            cursor: pointer;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 0.8rem;
            transition: all 0.3s ease;
            font-family: 'Share Tech Mono', monospace;
        }

        .note-entry .note-actions button:hover {
            background: rgba(0, 255, 65, 0.02);
            color: #00ff41;
        }

        .note-entry .note-actions .copy-hack:hover {
            color: #33ff77;
        }

        .empty-terminal {
            text-align: center;
            color: rgba(0, 255, 65, 0.04);
            padding: 40px 20px;
            font-size: 0.8rem;
            letter-spacing: 2px;
            font-style: italic;
        }

        /* ============================================================
           TOAST - HACKER STYLE
        ============================================================ */
        .toast-hack {
            position: fixed;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%) translateY(120px);
            background: rgba(0, 0, 0, 0.95);
            border: 1px solid rgba(0, 255, 65, 0.04);
            padding: 10px 28px;
            border-radius: 6px;
            color: rgba(0, 255, 65, 0.2);
            font-family: 'Share Tech Mono', monospace;
            font-size: 0.7rem;
            letter-spacing: 1px;
            z-index: 999;
            opacity: 0;
            transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            pointer-events: none;
            backdrop-filter: blur(10px);
            text-shadow: 0 0 20px rgba(0, 255, 65, 0.02);
        }

        .toast-hack.show {
            opacity: 1;
            transform: translateX(-50%) translateY(0);
            color: #00ff41;
            border-color: rgba(0, 255, 65, 0.06);
        }

        /* ============================================================
           SCROLL
        ============================================================ */
        #notesContainer::-webkit-scrollbar {
            width: 3px;
        }
        #notesContainer::-webkit-scrollbar-track {
            background: rgba(0, 0, 0, 0.2);
        }
        #notesContainer::-webkit-scrollbar-thumb {
            background: rgba(0, 255, 65, 0.04);
            border-radius: 10px;
        }

        /* ============================================================
           RESPONSIVE
        ============================================================ */
        @media (max-width: 640px) {
            .terminal-body {
                padding: 16px 14px 14px;
            }
            .terminal-header {
                padding: 8px 14px;
            }
            .terminal-title {
                font-size: 0.5rem;
                letter-spacing: 1px;
            }
            .btn-hack {
                padding: 8px 14px;
                font-size: 0.6rem;
                flex: 1;
            }
            .display-area {
                font-size: 0.7rem;
                padding: 12px 14px;
                min-height: 90px;
            }
            .display-area::before {
                width: 50px;
                height: 50px;
                right: 5px;
                bottom: 5px;
            }
            .input-row-hack input,
            .input-row-hack textarea {
                font-size: 0.75rem;
                padding: 10px 12px;
            }
            .lock-status {
                flex-direction: column;
                align-items: stretch;
                text-align: center;
            }
            .toast-hack {
                font-size: 0.6rem;
                padding: 8px 18px;
                width: 92%;
            }
            .hacker-avatar {
                width: 30px;
                height: 30px;
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>

<!-- ===== FOG / MIST ===== -->
<div class="fog-container">
    <div class="fog-layer"></div>
    <div class="fog-layer"></div>
    <div class="fog-layer"></div>
</div>

<!-- ===== HACKER BG IMAGE ===== -->
<div class="hacker-bg"></div>

<!-- ===== MATRIX RAIN ===== -->
<div class="matrix-rain" id="matrixRain"></div>

<!-- ===== MAIN TERMINAL ===== -->
<div class="terminal">

    <!-- TERMINAL HEADER -->
    <div class="terminal-header">
        <div class="terminal-dots">
            <span class="dot-terminal red"></span>
            <span class="dot-terminal yellow"></span>
            <span class="dot-terminal green"></span>
        </div>
        <div class="terminal-title">
            <span class="blink">⬤</span> 
            <span>ROOT@HACKER-DEN</span>
            <span style="color:rgba(0,255,65,0.1);">~</span>
            <span style="color:rgba(0,255,65,0.05);">$</span>
        </div>
        <div class="terminal-status">
            <div class="hacker-avatar"></div>
            <span>ENCRYPTED</span>
        </div>
    </div>

    <!-- TERMINAL BODY -->
    <div class="terminal-body">

        <!-- DISPLAY AREA -->
        <div class="display-area" id="displayArea">
            <span class="prompt">
                <span id="displayText">> system ready · enter passphrase to unlock</span>
                <span class="cursor-line"></span>
            </span>
        </div>

        <!-- LOCK STATUS -->
        <div class="lock-status">
            <div class="lock-icon" id="lockIcon">🔒</div>
            <div class="lock-text" id="lockText">
                STATUS: <span class="highlight" id="lockStatusText">LOCKED</span>
            </div>
            <div class="status-badge" id="statusBadge">⛔ OFFLINE</div>
        </div>

        <!-- PASSPHRASE INPUT -->
        <div class="input-section">
            <div class="input-row-hack">
                <input type="password" id="passphraseInput" placeholder="> enter passphrase..." />
                <button class="btn-hack success" id="unlockBtn">[ UNLOCK ]</button>
                <button class="btn-hack danger" id="lockBtn">[ LOCK ]</button>
            </div>
        </div>

        <!-- NOTE INPUT -->
        <div class="input-section">
            <div class="input-row-hack">
                <textarea id="noteInput" placeholder="> write your secret note... (ctrl+enter to save)"></textarea>
            </div>
            <div class="btn-group-hack">
                <button class="btn-hack success" id="saveNoteBtn">[ SAVE ]</button>
                <button class="btn-hack danger" id="clearAllBtn">[ DELETE ALL ]</button>
            </div>
        </div>

        <!-- NOTES LIST -->
        <div id="notesContainer">
            <div class="empty-terminal">> no notes found</div>
        </div>

    </div>
</div>

<!-- ===== TOAST ===== -->
<div class="toast-hack" id="toast">> action completed</div>

<script>
    (function() {
        "use strict";

        // ============================================================
        // MATRIX RAIN (more visible)
        // ============================================================
        (function matrixRain() {
            const el = document.getElementById('matrixRain');
            const chars = '0123456789ABCDEF';
            let rows = 50;
            let cols = Math.floor(window.innerWidth / 18);
            let grid = [];

            for (let i = 0; i < cols; i++) {
                grid.push(Math.floor(Math.random() * rows));
            }

            function draw() {
                let output = '';
                for (let y = 0; y < rows; y++) {
                    for (let x = 0; x < cols; x++) {
                        if (grid[x] === y) {
                            output += chars[Math.floor(Math.random() * chars.length)];
                        } else {
                            output += ' ';
                        }
                    }
                    output += '\n';
                }
                el.textContent = output;

                for (let i = 0; i < cols; i++) {
                    if (Math.random() > 0.97) {
                        grid[i] = 0;
                    } else {
                        grid[i] = (grid[i] + 1) % rows;
                    }
                }
            }

            setInterval(draw, 120);
            draw();
        })();

        // ============================================================
        // DOM REFS
        // ============================================================
        const passInput = document.getElementById('passphraseInput');
        const unlockBtn = document.getElementById('unlockBtn');
        const lockBtn = document.getElementById('lockBtn');
        const noteInput = document.getElementById('noteInput');
        const saveBtn = document.getElementById('saveNoteBtn');
        const clearAllBtn = document.getElementById('clearAllBtn');
        const notesContainer = document.getElementById('notesContainer');
        const lockIcon = document.getElementById('lockIcon');
        const lockStatusText = document.getElementById('lockStatusText');
        const statusBadge = document.getElementById('statusBadge');
        const displayText = document.getElementById('displayText');
        const toast = document.getElementById('toast');

        // ============================================================
        // STATE
        // ============================================================
        let currentPassphrase = '';
        let isUnlocked = false;
        let notes = [];

        // ============================================================
        // TOAST
        // ============================================================
        let toastTimeout = null;

        function showToast(message = '> action completed') {
            toast.textContent = message;
            toast.classList.add('show');
            clearTimeout(toastTimeout);
            toastTimeout = setTimeout(() => {
                toast.classList.remove('show');
            }, 2000);
        }

        // ============================================================
        // UI UPDATE
        // ============================================================
        function updateUI() {
            if (isUnlocked && currentPassphrase.length > 0) {
                lockIcon.textContent = '🔓';
                lockStatusText.textContent = 'UNLOCKED';
                lockStatusText.style.color = '#00ff41';
                statusBadge.textContent = '● ONLINE';
                statusBadge.className = 'status-badge active';
                displayText.innerHTML = '> system ready · <span class="hacker-text">' + notes.length + '</span> notes found';
            } else {
                lockIcon.textContent = '🔒';
                lockStatusText.textContent = 'LOCKED';
                lockStatusText.style.color = '';
                statusBadge.textContent = '⛔ OFFLINE';
                statusBadge.className = 'status-badge';
                displayText.textContent = '> system locked · enter passphrase to unlock';
            }
            renderNotes();
        }

        // ============================================================
        // ENCRYPTION
        // ============================================================
        async function getKeyFromPassphrase(pass) {
            const enc = new TextEncoder();
            const keyMaterial = await crypto.subtle.importKey(
                'raw',
                enc.encode(pass),
                'PBKDF2',
                false,
                ['deriveKey']
            );
            return crypto.subtle.deriveKey(
                {
                    name: 'PBKDF2',
                    salt: enc.encode('hacker-den-salt-2026'),
                    iterations: 250000,
                    hash: 'SHA-256'
                },
                keyMaterial,
                { name: 'AES-GCM', length: 256 },
                false,
                ['encrypt', 'decrypt']
            );
        }

        async function encryptText(text, passphrase) {
            if (!passphrase) throw new Error('Passphrase missing');
            const key = await getKeyFromPassphrase(passphrase);
            const enc = new TextEncoder();
            const data = enc.encode(text);
            const iv = crypto.getRandomValues(new Uint8Array(12));
            const encrypted = await crypto.subtle.encrypt({ name: 'AES-GCM', iv }, key, data);
            const combined = new Uint8Array(iv.length + encrypted.byteLength);
            combined.set(iv, 0);
            combined.set(new Uint8Array(encrypted), iv.length);
            return btoa(String.fromCharCode(...combined));
        }

        async function decryptText(encoded, passphrase) {
            if (!passphrase) throw new Error('Passphrase missing');
            const key = await getKeyFromPassphrase(passphrase);
            const combined = Uint8Array.from(atob(encoded), c => c.charCodeAt(0));
            const iv = combined.slice(0, 12);
            const data = combined.slice(12);
            const decrypted = await crypto.subtle.decrypt({ name: 'AES-GCM', iv }, key, data);
            return new TextDecoder().decode(decrypted);
        }

        // ============================================================
        // STORAGE
        // ============================================================
        function loadNotes() {
            try {
                const raw = localStorage.getItem('hacker_den_notes');
                notes = raw ? JSON.parse(raw) : [];
            } catch (_) {
                notes = [];
            }
        }

        function saveNotes() {
            localStorage.setItem('hacker_den_notes', JSON.stringify(notes));
        }

        // ============================================================
        // RENDER
        // ============================================================
        async function renderNotes() {
            if (!isUnlocked || !currentPassphrase) {
                if (notes.length === 0) {
                    notesContainer.innerHTML = `<div class="empty-terminal">> locked · unlock to view</div>`;
                } else {
                    let html = '';
                    for (let i = 0; i < notes.length; i++) {
                        html += `
                            <div class="note-entry">
                                <div class="note-content">🔐 [encrypted]</div>
                                <div class="note-meta">#${i+1}</div>
                                <div class="note-actions">
                                    <button class="copy-hack" data-index="${i}">📋</button>
                                    <button class="delete-hack" data-index="${i}">✕</button>
                                </div>
                            </div>
                        `;
                    }
                    notesContainer.innerHTML = html;
                }
                attachEvents();
                return;
            }

            if (notes.length === 0) {
                notesContainer.innerHTML = `<div class="empty-terminal">> no notes found · create one</div>`;
                return;
            }

            let html = '';
            for (let i = 0; i < notes.length; i++) {
                let decrypted = '❌ decryption failed';
                try {
                    decrypted = await decryptText(notes[i], currentPassphrase);
                } catch (_) {
                    decrypted = '⚠️ wrong passphrase or corrupted';
                }
                html += `
                    <div class="note-entry">
                        <div class="note-content"><span class="highlight-note">${escapeHtml(decrypted)}</span></div>
                        <div class="note-meta">#${i+1}</div>
                        <div class="note-actions">
                            <button class="copy-hack" data-content="${escapeHtml(decrypted)}">📋</button>
                            <button class="delete-hack" data-index="${i}">✕</button>
                        </div>
                    </div>
                `;
            }
            notesContainer.innerHTML = html;
            attachEvents();
        }

        function escapeHtml(text) {
            const d = document.createElement('div');
            d.textContent = text;
            return d.innerHTML;
        }

        // ============================================================
        // EVENTS
        // ============================================================
        function attachEvents() {
            document.querySelectorAll('.copy-hack').forEach(btn => {
                btn.addEventListener('click', function(e) {
                    e.stopPropagation();
                    let content = this.dataset.content;
                    if (!content) {
                        const idx = parseInt(this.dataset.index, 10);
                        if (!isNaN(idx) && notes[idx]) {
                            content = notes[idx];
                        } else {
                            content = 'no content';
                        }
                    }
                    if (content) {
                        navigator.clipboard.writeText(content).then(() => {
                            showToast('> copied to clipboard');
                        }).catch(() => {
                            const textarea = document.createElement('textarea');
                            textarea.value = content;
                            document.body.appendChild(textarea);
                            textarea.select();
                            document.execCommand('copy');
                            document.body.removeChild(textarea);
                            showToast('> copied');
                        });
                    }
                });
            });

            document.querySelectorAll('.delete-hack').forEach(btn => {
                btn.addEventListener('click', function() {
                    const idx = parseInt(this.dataset.index, 10);
                    if (isUnlocked && currentPassphrase) deleteNote(idx);
                    else showToast('> ⛔ unlock first');
                });
            });
        }

        // ============================================================
        // CRUD
        // ============================================================
        async function addNote(plainText) {
            if (!isUnlocked || !currentPassphrase) {
                showToast('> ⛔ unlock first');
                return false;
            }
            if (!plainText.trim()) {
                showToast('> ⚠️ write something');
                return false;
            }
            try {
                const encrypted = await encryptText(plainText.trim(), currentPassphrase);
                notes.push(encrypted);
                saveNotes();
                noteInput.value = '';
                await renderNotes();
                updateUI();
                showToast('> ✅ note saved');
                return true;
            } catch (e) {
                showToast('> ❌ error: ' + e.message);
                return false;
            }
        }

        async function deleteNote(index) {
            if (!isUnlocked || !currentPassphrase) {
                showToast('> ⛔ unlock first');
                return;
            }
            if (index >= 0 && index < notes.length) {
                notes.splice(index, 1);
                saveNotes();
                await renderNotes();
                updateUI();
                showToast('> 🗑️ note deleted');
            }
        }

        async function clearAllNotes() {
            if (!isUnlocked || !currentPassphrase) {
                showToast('> ⛔ unlock first');
                return;
            }
            if (notes.length === 0) return;
            if (confirm('⚠️ delete ALL notes permanently?')) {
                notes = [];
                saveNotes();
                await renderNotes();
                updateUI();
                showToast('> 🗑️ all notes deleted');
            }
        }

        // ============================================================
        // LOCK / UNLOCK
        // ============================================================
        async function unlock(passphrase) {
            if (!passphrase || passphrase.trim().length < 4) {
                showToast('> ⚠️ passphrase must be 4+ chars');
                return false;
            }
            if (notes.length > 0) {
                try {
                    await decryptText(notes[0], passphrase.trim());
                } catch (_) {
                    showToast('> ❌ wrong passphrase');
                    return false;
                }
            }
            currentPassphrase = passphrase.trim();
            isUnlocked = true;
            passInput.value = '';
            updateUI();
            await renderNotes();
            showToast('> 🔓 unlocked');
            return true;
        }

        function lock() {
            isUnlocked = false;
            currentPassphrase = '';
            passInput.value = '';
            updateUI();
            renderNotes();
            showToast('> 🔒 locked');
        }

        // ============================================================
        // INIT
        // ============================================================
        function init() {
            loadNotes();
            isUnlocked = false;
            currentPassphrase = '';
            updateUI();
            renderNotes();

            unlockBtn.addEventListener('click', async () => await unlock(passInput.value));
            lockBtn.addEventListener('click', lock);
            saveBtn.addEventListener('click', async () => await addNote(noteInput.value));
            clearAllBtn.addEventListener('click', async () => await clearAllNotes());

            passInput.addEventListener('keydown', async (e) => {
                if (e.key === 'Enter') {
                    e.preventDefault();
                    await unlock(passInput.value);
                }
            });

            noteInput.addEventListener('keydown', async (e) => {
                if (e.key === 'Enter' && e.ctrlKey) {
                    e.preventDefault();
                    await addNote(noteInput.value);
                }
            });
        }

        init();
    })();
</script>
</body>
</html>
