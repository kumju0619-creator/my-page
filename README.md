<!DOCTYPE html>
<html lang="ko"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🐾 고양이 천국 - 안녕하세요 금주찡 입니다 🐾</title>
    <!-- 귀여운 한글 폰트 (주아체 & 고운돋움) 로드 -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="">
    <link href="https://fonts.googleapis.com/css2?family=Gowun+Dodum&amp;family=Jua&amp;display=swap" rel="stylesheet">
    
    <style>
        /* 기본 변수 및 리셋 설정 */
        :root {
            --bg-cream: #FFFDF0;
            --card-white: #FFFFFF;
            --yellow-main: #FFB703;
            --yellow-dark: #E08E00;
            --yellow-light: #FFF3B0;
            --yellow-soft: #FFF8D6;
            --amber-accent: #FB8500;
            --brown-text: #5C4728;
            --shadow-soft: 0 8px 20px rgba(230, 168, 23, 0.2);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            font-family: 'Gowun Dodum', sans-serif;
            background-color: var(--bg-cream);
            /* 포근한 노랑 계열 도트 패턴 배경 */
            background-image: radial-gradient(#FFE169 2.5px, transparent 2.5px), radial-gradient(#FFF3B0 2.5px, var(--bg-cream) 2.5px);
            background-size: 40px 40px;
            background-position: 0 0, 20px 20px;
            color: var(--brown-text);
            line-height: 1.6;
            overflow-x: hidden;
            padding-bottom: 60px;
        }

        h1, h2, h3, .font-jua {
            font-family: 'Jua', sans-serif;
            font-weight: normal;
        }

        /* 레이아웃 컨테이너 */
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px 16px;
            display: flex;
            flex-direction: column;
            gap: 28px;
        }

        /* 공통 섹션 카드 스타일 */
        .section-box {
            background: var(--card-white);
            border-radius: 28px;
            padding: 28px 22px;
            box-shadow: var(--shadow-soft);
            border: 3px solid var(--yellow-light);
            position: relative;
            transition: transform 0.2s ease;
        }

        .section-title {
            font-size: 1.6rem;
            color: var(--yellow-dark);
            text-align: center;
            margin-bottom: 18px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        /* 1. 헤더 & 통통 튀는 별명 애니메이션 */
        header.hero {
            text-align: center;
            padding: 36px 20px;
            background: linear-gradient(135deg, #FFF9DB 0%, #FFE885 100%);
            border-radius: 32px;
            border: 4px dashed var(--yellow-main);
            box-shadow: var(--shadow-soft);
            position: relative;
            overflow: hidden;
        }

        .cat-ears-deco {
            font-size: 2.5rem;
            margin-bottom: 8px;
            animation: floatCat 3s ease-in-out infinite;
        }

        @keyframes floatCat {
            0%, 100% { transform: translateY(0px) rotate(-3deg); }
            50% { transform: translateY(-6px) rotate(3deg); }
        }

        .bouncing-title {
            font-family: 'Jua', sans-serif;
            font-size: clamp(1.8rem, 6vw, 2.8rem);
            color: var(--yellow-dark);
            text-shadow: 2px 2px 0px #FFFFFF, 4px 4px 0px rgba(255, 183, 3, 0.35);
            display: inline-block;
            margin: 10px 0;
            word-break: keep-all;
        }

        .bouncing-title span {
            display: inline-block;
            animation: bounceChar 1.4s infinite ease-in-out;
        }

        @keyframes bounceChar {
            0%, 100% { transform: translateY(0) scale(1); }
            40% { transform: translateY(-14px) scale(1.1); color: var(--amber-accent); }
            70% { transform: translateY(2px) scale(0.95); }
        }

        .hero-subtitle {
            font-size: 1.1rem;
            color: var(--brown-text);
            background: rgba(255, 255, 255, 0.85);
            display: inline-block;
            padding: 6px 18px;
            border-radius: 20px;
            margin-top: 8px;
        }

        /* 2. 방문자 환영 인사 칸 */
        .welcome-form {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
            align-items: center;
        }

        .welcome-input {
            flex: 1;
            min-width: 200px;
            max-width: 300px;
            padding: 12px 18px;
            border: 2px solid var(--yellow-main);
            border-radius: 20px;
            font-family: 'Gowun Dodum', sans-serif;
            font-size: 1rem;
            outline: none;
            color: var(--brown-text);
            background: #FFFDF7;
        }

        .welcome-input:focus {
            box-shadow: 0 0 0 4px var(--yellow-light);
        }

        .btn-cute {
            font-family: 'Jua', sans-serif;
            font-size: 1.1rem;
            padding: 12px 22px;
            border: none;
            border-radius: 20px;
            background: var(--yellow-main);
            color: #4A3511;
            cursor: pointer;
            box-shadow: 0 4px 0 var(--yellow-dark);
            transition: all 0.15s ease;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
        }

        .btn-cute:hover {
            background: #FFC629;
            transform: translateY(-2px);
        }

        .btn-cute:active {
            transform: translateY(3px);
            box-shadow: 0 1px 0 var(--yellow-dark);
        }

        .welcome-message {
            margin-top: 16px;
            text-align: center;
            font-size: 1.15rem;
            font-weight: bold;
            color: var(--yellow-dark);
            min-height: 28px;
            background: var(--yellow-light);
            padding: 12px;
            border-radius: 16px;
            display: none;
            animation: popIn 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        @keyframes popIn {
            0% { transform: scale(0.8); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }

        /* 3. 좋아하는 것 3가지 (뒤집히는 플립 카드) */
        .flip-hint {
            text-align: center;
            font-size: 0.95rem;
            color: #8C734B;
            margin-top: -10px;
            margin-bottom: 16px;
        }

        .cards-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 16px;
        }

        @media (max-width: 650px) {
            .cards-grid {
                grid-template-columns: 1fr;
            }
        }

        .flip-card {
            background-color: transparent;
            height: 230px;
            perspective: 1000px;
            cursor: pointer;
        }

        .flip-card-inner {
            position: relative;
            width: 100%;
            height: 100%;
            text-align: center;
            transition: transform 0.6s cubic-bezier(0.4, 0.2, 0.2, 1);
            transform-style: preserve-3d;
        }

        .flip-card.flipped .flip-card-inner {
            transform: rotateY(180deg);
        }

        .flip-card-front, .flip-card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
            border-radius: 22px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 18px;
            box-shadow: 0 6px 14px rgba(230, 168, 23, 0.12);
        }

        .flip-card-front {
            background: linear-gradient(180deg, #FFFFFF 0%, #FFF9DB 100%);
            border: 3px solid #FFE169;
        }

        .flip-card-front .emoji {
            font-size: 3.6rem;
            margin-bottom: 10px;
            transition: transform 0.3s ease;
        }

        .flip-card:hover .flip-card-front .emoji {
            transform: scale(1.15) rotate(6deg);
        }

        .flip-card-front h3 {
            font-size: 1.5rem;
            color: var(--yellow-dark);
        }

        .flip-card-front .tap-badge {
            margin-top: 10px;
            font-size: 0.8rem;
            background: var(--yellow-main);
            color: #4A3511;
            font-weight: bold;
            padding: 3px 10px;
            border-radius: 12px;
        }

        .flip-card-back {
            background: linear-gradient(135deg, #FFD166 0%, #F4A261 100%);
            color: #3D2B10;
            transform: rotateY(180deg);
            border: 3px solid #FFF3B0;
        }

        .flip-card-back h4 {
            font-family: 'Jua', sans-serif;
            font-size: 1.25rem;
            margin-bottom: 8px;
            background: rgba(255, 255, 255, 0.55);
            padding: 4px 12px;
            border-radius: 12px;
        }

        .flip-card-back p {
            font-size: 0.98rem;
            line-height: 1.5;
            word-break: keep-all;
            font-weight: 600;
        }

        /* 4. OX 퀴즈 섹션 */
        .quiz-question {
            font-family: 'Jua', sans-serif;
            font-size: 1.45rem;
            text-align: center;
            background: var(--yellow-soft);
            padding: 18px;
            border-radius: 20px;
            margin-bottom: 18px;
            color: var(--brown-text);
            border: 2px dashed var(--yellow-main);
        }

        .ox-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .btn-ox {
            width: 110px;
            height: 90px;
            font-family: 'Jua', sans-serif;
            font-size: 2.6rem;
            border: none;
            border-radius: 24px;
            cursor: pointer;
            transition: transform 0.2s, box-shadow 0.2s;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .btn-ox span {
            font-size: 0.85rem;
            margin-top: -4px;
        }

        .btn-o {
            background: #FFE169;
            color: #4A3511;
            box-shadow: 0 6px 0 #E08E00;
        }

        .btn-x {
            background: #F4A261;
            color: #4A2508;
            box-shadow: 0 6px 0 #C86D25;
        }

        .btn-ox:active {
            transform: translateY(4px);
            box-shadow: 0 2px 0 rgba(0,0,0,0.2);
        }

        .quiz-feedback {
            margin-top: 18px;
            text-align: center;
            padding: 16px;
            border-radius: 18px;
            font-size: 1.15rem;
            font-weight: bold;
            display: none;
        }

        .quiz-correct {
            background: #FFF9DB;
            color: #7A5200;
            border: 2px solid #FFB703;
            animation: popIn 0.4s ease;
        }

        .quiz-wrong {
            background: #FFEDD8;
            color: #8C3B00;
            border: 2px solid #F4A261;
            animation: shakeSad 0.5s ease;
        }

        @keyframes shakeSad {
            0%, 100% { transform: translateX(0); }
            20%, 60% { transform: translateX(-8px); }
            40%, 80% { transform: translateX(8px); }
        }

        /* 5. 오늘의 고양이 운세 */
        .fortune-box {
            text-align: center;
        }

        .fortune-result {
            margin-top: 18px;
            min-height: 90px;
            background: #FFFDF2;
            border: 2px solid #FFD166;
            border-radius: 20px;
            padding: 18px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            font-size: 1.1rem;
            color: var(--brown-text);
            word-break: keep-all;
        }

        .fortune-badge {
            font-family: 'Jua', sans-serif;
            background: #FFD166;
            color: #4A3511;
            padding: 4px 14px;
            border-radius: 14px;
            font-size: 1rem;
            margin-bottom: 8px;
        }

        /* 6. 10초 미니게임 (금주찡에게 츄르 주기) */
        .game-area {
            text-align: center;
            background: #FFFDF5;
            border-radius: 22px;
            padding: 20px;
            border: 2px solid #FFF3B0;
        }

        .game-stats {
            display: flex;
            justify-content: space-around;
            margin-bottom: 16px;
            font-family: 'Jua', sans-serif;
            font-size: 1.3rem;
        }

        .stat-pill {
            background: white;
            padding: 8px 18px;
            border-radius: 16px;
            box-shadow: 0 3px 8px rgba(230, 168, 23, 0.1);
            border: 2px solid var(--yellow-light);
        }

        .btn-clicker {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 6px solid #FFF3B0;
            background: linear-gradient(145deg, #FFD166, #FFB703);
            color: #4A3511;
            font-family: 'Jua', sans-serif;
            font-size: 1.3rem;
            cursor: pointer;
            box-shadow: 0 8px 0 #D98200, 0 12px 20px rgba(255, 183, 3, 0.4);
            transition: transform 0.08s;
            display: inline-flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            user-select: none;
            margin: 10px 0;
        }

        .btn-clicker:active {
            transform: translateY(6px) scale(0.95);
            box-shadow: 0 2px 0 #D98200;
        }

        .btn-clicker .paw-icon {
            font-size: 2.8rem;
            margin-bottom: 4px;
        }

        .game-result-msg {
            margin-top: 14px;
            font-size: 1.1rem;
            font-weight: bold;
            color: var(--yellow-dark);
            min-height: 28px;
        }

        /* 마우스 반짝이 & 축하 파티클 */
        .sparkle {
            position: fixed;
            pointer-events: none;
            z-index: 9999;
            font-size: 16px;
            animation: sparkleFade 0.8s forwards ease-out;
            user-select: none;
        }

        @keyframes sparkleFade {
            0% {
                opacity: 1;
                transform: translate(-50%, -50%) scale(0.5) rotate(0deg);
            }
            50% {
                opacity: 1;
                transform: translate(-50%, -90%) scale(1.2) rotate(180deg);
            }
            100% {
                opacity: 0;
                transform: translate(-50%, -130%) scale(0.3) rotate(360deg);
            }
        }

        .confetti-particle {
            position: fixed;
            pointer-events: none;
            z-index: 9998;
            font-size: 24px;
            animation: confettiFall 2.2s forwards ease-out;
        }

        @keyframes confettiFall {
            0% {
                opacity: 1;
                transform: translate(0, 0) scale(0.5) rotate(0deg);
            }
            100% {
                opacity: 0;
                transform: translate(var(--tx), var(--ty)) scale(1.3) rotate(720deg);
            }
        }

        footer {
            text-align: center;
            margin-top: 30px;
            font-size: 0.9rem;
            color: #9E8556;
        }
    </style>
<style data-studio="css">
:root{--st-accent:#e2557a}
.st-nav{position:sticky;top:0;z-index:50;width:100%;box-sizing:border-box;background:#fff;background:rgba(255,255,255,.93);backdrop-filter:blur(6px);border-bottom:1px solid rgba(0,0,0,.08)}
.st-nav-in{display:flex;gap:6px;justify-content:center;flex-wrap:wrap;padding:10px 12px;max-width:960px;margin:0 auto}
.st-nav-a{display:inline-block;padding:8px 14px;border-radius:999px;text-decoration:none;color:#333;font-weight:700;font-size:15px;line-height:1.2}
.st-nav-a:hover{background:rgba(0,0,0,.06)}
.st-nav-a.is-on{background:var(--st-accent);color:#fff}
.st-sec{box-sizing:border-box;width:100%;max-width:960px;margin:24px auto;padding:20px}
.st-h{font-size:1.6rem;font-weight:800;line-height:1.3;margin:0 0 12px}
.st-p{font-size:1rem;line-height:1.75;margin:0 0 12px}
.st-btn{display:inline-block;padding:12px 22px;border-radius:12px;background:var(--st-accent);color:#fff!important;text-decoration:none;font-weight:700;font-size:1rem;line-height:1.2;border:0;cursor:pointer;margin:4px}
.st-btn:hover{filter:brightness(1.08)}
.st-img{margin:16px auto;text-align:center}
.st-img img{display:inline-block;width:100%;max-width:100%;height:auto;border-radius:12px}
.st-hero{text-align:center;padding:48px 20px;border-radius:20px;background:#f6f6f6;background:color-mix(in srgb,var(--st-accent) 12%,#fff)}
.st-hero .st-h{font-size:2rem}
.st-cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:14px}
.st-card{background:#fff;border:1px solid rgba(0,0,0,.08);border-radius:16px;padding:18px;box-shadow:0 2px 10px rgba(0,0,0,.05);text-align:left}
.st-ico{font-size:2rem;line-height:1;margin:0 0 8px}
.st-card .st-h{font-size:1.15rem;margin:0 0 6px}
.st-card .st-p{margin:0;font-size:.95rem}
.st-split{display:grid;grid-template-columns:minmax(0,1fr) minmax(0,1.4fr);gap:20px;align-items:center}
@media(max-width:600px){.st-split{grid-template-columns:1fr}}
.st-split img{display:block;width:100%;height:auto;border-radius:16px}
.st-list{margin:0;padding-left:1.3em;line-height:1.9}
.st-hr{border:0;border-top:2px dashed rgba(0,0,0,.15);margin:28px auto;max-width:960px}
.st-foot{text-align:center;font-size:.875rem;opacity:.7;padding:24px 12px}
.st-tab-bar{display:flex;gap:4px;flex-wrap:wrap;border-bottom:2px solid rgba(0,0,0,.08);margin-bottom:14px}
.st-tab{border:0;background:none;padding:10px 14px;font:inherit;font-weight:700;color:inherit;opacity:.6;cursor:pointer;border-bottom:3px solid transparent;margin-bottom:-2px}
.st-tab.is-on{opacity:1;color:var(--st-accent);border-bottom-color:var(--st-accent)}
.st-acc{border:1px solid rgba(0,0,0,.1);border-radius:12px;margin:8px 0;background:#fff;overflow:hidden;text-align:left}
.st-acc summary{cursor:pointer;padding:14px 44px 14px 16px;font-weight:700;list-style:none;position:relative}
.st-acc summary::-webkit-details-marker{display:none}
.st-acc summary::after{content:"+";position:absolute;right:16px;top:50%;transform:translateY(-50%);font-size:1.3em;color:var(--st-accent)}
.st-acc[open] summary::after{content:"\2212"}
.st-acc>.st-p{padding:0 16px 14px;margin:0}
.st-pop{margin:12px 0;text-align:center}
.st-modal{border:0;border-radius:18px;padding:24px;width:min(480px,90vw);box-shadow:0 20px 60px rgba(0,0,0,.3);text-align:left;color:#222}
.st-modal::backdrop{background:rgba(0,0,0,.45)}
.st-slider{position:relative}
.st-slides{display:flex;overflow-x:auto;scroll-snap-type:x mandatory;scrollbar-width:none;border-radius:16px}
.st-slides::-webkit-scrollbar{display:none}
.st-slide{flex:0 0 100%;scroll-snap-align:start;margin:0}
.st-slide img{display:block;width:100%;height:auto;aspect-ratio:16/10;object-fit:cover;border-radius:16px}
.st-slide figcaption{text-align:center;padding:8px;font-size:.95rem}
.st-prev,.st-next{position:absolute;top:calc(50% - 40px);width:44px;height:44px;border-radius:50%;border:0;background:rgba(255,255,255,.92);box-shadow:0 2px 8px rgba(0,0,0,.2);font-size:24px;line-height:1;cursor:pointer;color:#333}
.st-prev{left:10px}.st-next{right:10px}
.st-dots{display:flex;justify-content:center;gap:8px;margin-top:4px}
.st-dots button{width:10px;height:10px;border-radius:50%;border:0;background:rgba(0,0,0,.2);padding:0;cursor:pointer}
.st-dots button.is-on{background:var(--st-accent)}
.st-quiz{text-align:center}
.st-q{font-size:1.25rem;font-weight:800;margin:0 0 14px}
.st-opts{display:grid;gap:8px;max-width:420px;margin:0 auto}
.st-opt{padding:12px 16px;border-radius:12px;border:2px solid rgba(0,0,0,.12);background:#fff;font:inherit;font-weight:700;cursor:pointer;color:#222}
.st-opt.is-ok{border-color:#2f9e5b;background:#e9f7ef}.st-opt.is-no{border-color:#d9475a;background:#fdecee}
.st-qr{min-height:1.6em;font-weight:700;margin:12px 0 0}
.st-ci{display:flex;gap:10px;align-items:center;padding:10px 12px;border:1px solid rgba(0,0,0,.08);border-radius:10px;margin:6px 0;background:#fff;cursor:pointer;text-align:left;color:#222}
.st-ci input{width:20px;height:20px;flex:none;accent-color:var(--st-accent)}
.st-bar{height:10px;border-radius:99px;background:rgba(0,0,0,.08);overflow:hidden;margin-top:12px}
.st-bar i{display:block;height:100%;width:0;background:var(--st-accent);transition:width .3s}
.st-cnt{font-size:.9rem;opacity:.75;margin:6px 0 0}
.st-dday,.st-timer{text-align:center;border-radius:20px;background:#f6f6f6;background:color-mix(in srgb,var(--st-accent) 10%,#fff)}
.st-dlabel,.st-tlabel{margin:0;font-weight:700;opacity:.8}
.st-dnum,.st-tnum{margin:4px 0 8px;font-size:3rem;font-weight:900;color:var(--st-accent);font-variant-numeric:tabular-nums;line-height:1.2}
.st-tnum.is-done{animation:stblink 1s 3}@keyframes stblink{50%{opacity:.2}}
.st-embed iframe{display:block;width:100%;aspect-ratio:16/9;height:auto;border:0;border-radius:14px}
.st-embed[data-kind=map] iframe{aspect-ratio:4/3}
.st-cols{display:grid;gap:16px}
.st-c2{grid-template-columns:repeat(2,minmax(0,1fr))}.st-c3{grid-template-columns:repeat(3,minmax(0,1fr))}
@media(max-width:600px){.st-c2,.st-c3{grid-template-columns:1fr}}
.st-col{min-width:0}
.st-swipe{display:flex;gap:12px;overflow-x:auto;scroll-snap-type:x mandatory;padding:4px 4px 14px;-webkit-overflow-scrolling:touch}
.st-swipe>*{flex:0 0 min(72%,240px);box-sizing:border-box;scroll-snap-align:start}
.st-nav-i{margin-right:5px}
@media(max-width:600px){.st-nav-tab{position:fixed;top:auto;bottom:0;left:0;border-bottom:0;border-top:1px solid rgba(0,0,0,.1);padding-bottom:env(safe-area-inset-bottom)}.st-nav-tab .st-nav-in{flex-wrap:nowrap;justify-content:space-around;gap:0;padding:4px}.st-nav-tab .st-nav-a{flex:1 1 0;min-width:0;display:flex;flex-direction:column;align-items:center;gap:2px;padding:6px 2px;font-size:12px;border-radius:12px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}.st-nav-tab .st-nav-a.is-on{background:none;color:var(--st-accent)}.st-nav-tab .st-nav-i{margin:0;font-size:22px;line-height:1.1}}
.st-g-point{--st-g:linear-gradient(135deg,rgba(255,255,255,0),rgba(255,255,255,.45)),linear-gradient(var(--st-accent),var(--st-accent));--st-gi:#fff}.st-g-sunset{--st-g:linear-gradient(135deg,#f43f5e,#f97316);--st-gi:#fff}.st-g-ocean{--st-g:linear-gradient(135deg,#2563eb,#06b6d4);--st-gi:#fff}.st-g-grape{--st-g:linear-gradient(135deg,#7c3aed,#ec4899);--st-gi:#fff}.st-g-forest{--st-g:linear-gradient(135deg,#047857,#34d399);--st-gi:#fff}.st-g-night{--st-g:linear-gradient(135deg,#0f172a,#475569);--st-gi:#fff}.st-g-peach{--st-g:linear-gradient(135deg,#ffe4e6,#fef3c7);--st-gi:#222}.st-g-mint{--st-g:linear-gradient(135deg,#d1fae5,#dbeafe);--st-gi:#222}.st-g-lav{--st-g:linear-gradient(135deg,#ede9fe,#fce7f3);--st-gi:#222}
html body [class*="st-g-"]{background-image:var(--st-g);color:var(--st-gi)}
html body .st-gtx{color:transparent;-webkit-background-clip:text;background-clip:text;-webkit-text-fill-color:transparent}
.st-hv-lift,.st-hv-grow,.st-hv-glow,.st-hv-press{transition:translate .2s,scale .2s,box-shadow .2s}
@media(hover:hover){.st-hv-lift:hover{translate:0 -6px;box-shadow:0 14px 28px rgba(0,0,0,.18)}.st-hv-grow:hover{scale:1.04}.st-hv-glow:hover{box-shadow:0 8px 24px rgba(0,0,0,.25);box-shadow:0 0 0 3px color-mix(in srgb,var(--st-accent) 35%,transparent),0 8px 24px color-mix(in srgb,var(--st-accent) 45%,transparent)}}
.st-hv-press:active{scale:.95}
html.st-js [data-st-in]{opacity:0;transition:opacity .6s ease,transform .6s ease,translate .2s,scale .2s,box-shadow .2s}
html.st-js [data-st-in="up"]{transform:translateY(26px)}html.st-js [data-st-in="zoom"]{transform:scale(.9)}html.st-js [data-st-in="left"]{transform:translateX(-30px)}
html.st-js [data-st-in].is-in{opacity:1;transform:none}
html.st-editing [data-st-in]{opacity:1!important;transform:none!important}
.st-editing .st-swipe{flex-wrap:wrap;overflow:visible}
html.st-dark{filter:invert(1) hue-rotate(180deg);background:#fff}
html.st-dark img,html.st-dark video,html.st-dark iframe,html.st-dark canvas{filter:invert(1) hue-rotate(180deg)}
.st-editing .st-tab-panel{display:block!important;outline:2px dashed rgba(0,0,0,.18);outline-offset:4px;margin:12px 0}
.st-editing .st-slides{flex-wrap:wrap;gap:10px;overflow:visible}
.st-editing .st-prev,.st-editing .st-next{display:none}
.st-editing dialog.st-modal{display:block;position:static;margin:12px auto;outline:2px dashed rgba(0,0,0,.25)}
.st-editing .st-embed iframe{pointer-events:none}
</style></head>
<body>

    <a class="st-btn" href="rmawn.html">자세히 보기</a><a class="st-btn" href="mango.html">자세히 보기</a><div class="container">
        <!-- 1. 히어로 섹션: 통통 튀는 별명 -->
        <header class="hero">
            <div class="cat-ears-deco">🐱🐾😻🐾🐱</div>
            <h1 class="bouncing-title" id="bouncingTitle" aria-label="안녕하세요 금주찡 입니다">
                <!-- 자바스크립트로 글자별 통통 튀는 span 생성 -->
            </h1>
            <br>
            <p class="hero-subtitle">✨ 말랑말랑 젤리와 낮잠이 가득한 고양이 천국에 오신 걸 환영해요! ✨</p>
        </header>

        <!-- 2. 방문자 환영 인사 칸 -->
        <section class="section-box">
            <h2 class="section-title">💌 방명록 인사 남기기</h2>
            <div class="welcome-form">
                <input type="text" id="visitorName" class="welcome-input" placeholder="이름이나 별명을 적어주세요!" maxlength="15">
                <button type="button" id="greetBtn" class="btn-cute">인사하기 🐾</button>
            </div>
            <div id="welcomeOutput" class="welcome-message"></div>
        </section>

        <!-- 3. 좋아하는 것 3가지 (플립 카드) -->
        <section class="section-box">
            <h2 class="section-title">💖 금주찡이 좋아하는 것 3가지</h2>
            <p class="flip-hint">👇 카드를 톡! 눌러서 뒤집어 보세요 👇</p>
            <div class="cards-grid">
                <!-- 카드 1: 고양이 -->
                <div class="flip-card" onclick="this.classList.toggle('flipped')">
                    <div class="flip-card-inner">
                        <div class="flip-card-front">
                            <div class="emoji">🐈</div>
                            <h3>고양이</h3>
                            <span class="tap-badge">눌러서 이유 보기 ↻</span>
                        </div>
                        <div class="flip-card-back">
                            <h4>🐱 고양이 최고!</h4>
                            <p>지구 정복을 위해 내려온 말랑한 솜뭉치들! 핑크 젤리 발바닥 한 번만 만지면 그날 피로가 싹 녹아내리는 마법의 생명체이기 때문이에요.</p>
                        </div>
                    </div>
                </div>

                <!-- 카드 2: 밥 -->
                <div class="flip-card" onclick="this.classList.toggle('flipped')">
                    <div class="flip-card-inner">
                        <div class="flip-card-front">
                            <div class="emoji">🍚</div>
                            <h3>밥</h3>
                            <span class="tap-badge">눌러서 이유 보기 ↻</span>
                        </div>
                        <div class="flip-card-back">
                            <h4>🍱 맛있는 밥!</h4>
                            <p>세상에서 가장 기분 좋은 소리는 바로 밥솥 취사 완료 멜로디! 맛있는 한 끼를 먹을 때면 꼬리가 프로펠러처럼 빙글빙글 돌아갈 만큼 행복해져요.</p>
                        </div>
                    </div>
                </div>

                <!-- 카드 3: 침대 -->
                <div class="flip-card" onclick="this.classList.toggle('flipped')">
                    <div class="flip-card-inner">
                        <div class="flip-card-front">
                            <div class="emoji">🛏️</div>
                            <h3>침대</h3>
                            <span class="tap-badge">눌러서 이유 보기 ↻</span>
                        </div>
                        <div class="flip-card-back">
                            <h4>🛌 포근한 침대!</h4>
                            <p>이불 밖은 위험해! 한 번 누우면 강력한 중력이 발생해서 절대 빠져나올 수 없는 마성의 블랙홀이자, 세상에서 가장 안전한 나만의 아지트랍니다.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 4. OX 퀴즈 섹션 -->
        <section class="section-box">
            <h2 class="section-title">⭕❌ 금주찡 탐구 OX 퀴즈</h2>
            <div class="quiz-question">
                Q. "나는 집을 제일 좋아한다"
            </div>
            <div class="ox-buttons">
                <button type="button" class="btn-ox btn-o" onclick="checkQuiz(true)">
                    O
                    <span>그렇다냥!</span>
                </button>
                <button type="button" class="btn-ox btn-x" onclick="checkQuiz(false)">
                    X
                    <span>아니다냥!</span>
                </button>
            </div>
            <div id="quizFeedback" class="quiz-feedback"></div>
        </section>

        <!-- 5. 오늘의 고양이 운세 -->
        <section class="section-box fortune-box">
            <h2 class="section-title">🔮 오늘의 냥냥 운세 뽑기</h2>
            <p style="margin-bottom: 14px; font-size: 0.95rem;">고양이 신령님이 오늘의 행운을 점쳐드려요!</p>
            <button type="button" id="fortuneBtn" class="btn-cute">🐾 오늘의 운세 뽑기 🐾</button>
            <div id="fortuneResult" class="fortune-result">
                <span>버튼을 눌러 오늘의 운세를 확인해 보세요!</span>
            </div>
        </section>

        <!-- 6. 10초 미니게임 -->
        <section class="section-box">
            <h2 class="section-title">⏱️ 10초 냥젤리 꾹꾹이 게임</h2>
            <p style="text-align: center; margin-bottom: 14px; font-size: 0.95rem;">
                10초 동안 가운데 발바닥 버튼을 최대한 많이 눌러주세요!
            </p>
            <div class="game-area">
                <div class="game-stats">
                    <div class="stat-pill">⏳ 남은 시간: <span id="timeLeft" style="color: #E08E00;">10.0</span>초</div>
                    <div class="stat-pill">🐾 누른 횟수: <span id="clickCount" style="color: #FB8500;">0</span>번</div>
                </div>

                <button type="button" id="clickerBtn" class="btn-clicker">
                    <span class="paw-icon">🐾</span>
                    <span id="clickerLabel">눌러서 시작!</span>
                </button>

                <div id="gameResultMsg" class="game-result-msg">준비되셨나요? 버튼을 누르면 바로 시작돼요!</div>
                <button type="button" id="resetGameBtn" class="btn-cute" style="display: none; margin: 12px auto 0; background: #E9C46A; box-shadow: 0 4px 0 #B58E38;">
                    다시 도전하기 🔄
                </button>
            </div>
        </section>

        <footer>
            🐾 Made with Cat Love for 금주찡 🐾
        </footer>
    </div>
<!-- ▼ 방명록·OX 투표 (4차시) ▼ --><sb-widget id="sb-web" style="display:block;width:100%;max-width:640px;margin:32px auto;flex:1 1 100%;grid-column:1/-1;align-self:stretch;box-sizing:border-box"></sb-widget>
<script>
(function () {
  var C = {"id":"sb-web","url":"https://script.google.com/macros/s/AKfycbyrO9an04qkque_7L2lDnapM1X2nNI7SK-xui4Dx7YMWQ9tIW9LYQMeSGduGIUJnPc/exec","q":"나는 집을 좋아한다","title":"방명록","sel":"","pos":"after"};
  var host = document.getElementById(C.id);
  if (!host || host.sbReady) return;
  host.sbReady = true;
  var PREVIEW = !!window.__SB_PREVIEW;

  function place() {
    if (!C.sel) return;
    var t = null;
    try { t = document.querySelector(C.sel); } catch (e) {}
    if (!t || t === host || t.contains(host) || !t.parentNode) return;
    if (C.pos === 'before') { if (t.previousElementSibling !== host) t.parentNode.insertBefore(host, t); }
    else if (t.nextElementSibling !== host) t.parentNode.insertBefore(host, t.nextSibling);
  }

  function rgb(s) { var m = (s || '').match(/[\d.]+/g); return m ? m.map(Number) : null; }
  function lum(c) { return (0.299 * c[0] + 0.587 * c[1] + 0.114 * c[2]) / 255; }
  function pageBg() {
    var el = host.parentElement;
    while (el) { var c = rgb(getComputedStyle(el).backgroundColor); if (c && (c.length < 4 || c[3] > 0.5)) return c; el = el.parentElement; }
    return [255, 255, 255];
  }
  function accent() {
    var els = document.querySelectorAll('button, .btn, a, h1, h2');
    for (var i = 0; i < els.length && i < 60; i++) {
      if (host.contains(els[i])) continue;
      var cs = getComputedStyle(els[i]);
      var list = [cs.backgroundColor, cs.color];
      for (var j = 0; j < 2; j++) {
        var c = rgb(list[j]);
        if (!c || (c.length > 3 && c[3] < 0.5)) continue;
        var mx = Math.max(c[0], c[1], c[2]), mn = Math.min(c[0], c[1], c[2]);
        if (mx - mn > 60 && lum(c) > 0.2 && lum(c) < 0.8) return 'rgb(' + c[0] + ',' + c[1] + ',' + c[2] + ')';
      }
    }
    return '#E5486F';
  }

  var root = host.attachShadow ? host.attachShadow({ mode: 'open' }) : host;
  root.innerHTML = '<' + 'style>' +
    '.wrap{display:flex;flex-direction:column;gap:16px}' +
    '.card{box-sizing:border-box;font-family:inherit;font-size:16px;line-height:1.6;text-align:left;border-radius:16px;padding:20px;background:rgba(255,255,255,.94);color:#222;border:1px solid rgba(0,0,0,.1);box-shadow:0 4px 18px rgba(0,0,0,.08)}' +
    '.dark .card{background:rgba(20,20,28,.9);color:#f3f3f6;border-color:rgba(255,255,255,.18)}' +
    '.card *{box-sizing:border-box;font-family:inherit}' +
    'h3{margin:0 0 12px;font-size:20px;line-height:1.35;color:inherit}' +
    '.row{display:flex;gap:8px;flex-wrap:wrap}' +
    'input,textarea{flex:1 1 140px;min-width:0;font-size:16px;padding:10px 12px;border-radius:10px;border:1px solid #ccc;background:#fff;color:inherit}' +
    '.dark input,.dark textarea{border-color:rgba(255,255,255,.3);background:rgba(255,255,255,.08)}' +
    'textarea{flex-basis:100%;resize:vertical;min-height:70px}' +
    'button{font-size:16px;font-weight:700;border:0;border-radius:10px;padding:10px 18px;cursor:pointer;background:var(--a,#E5486F);color:#fff}' +
    'button:disabled{opacity:.45;cursor:default}' +
    '.msg{margin:8px 0 0;font-size:14px;min-height:1em;opacity:.85}' +
    '.list{list-style:none;margin:14px 0 0;padding:0;display:flex;flex-direction:column;gap:8px;max-height:340px;overflow:auto}' +
    '.list li{padding:10px 12px;border-radius:10px;background:rgba(0,0,0,.04);word-break:break-all}.dark .list li{background:rgba(255,255,255,.07)}' +
    '.list b{margin-right:6px}.list small{opacity:.6;font-size:12px}.list p{margin:2px 0 0;white-space:pre-wrap}' +
    '.top{display:flex;justify-content:space-between;align-items:center;gap:8px;margin-top:12px;font-size:14px;opacity:.85}' +
    '.top .re{background:transparent;color:inherit;border:1px solid currentColor;padding:4px 10px;font-size:13px;font-weight:400;opacity:.8}' +
    '.live{display:inline-flex;align-items:center;gap:6px}.live:before{content:"";width:8px;height:8px;border-radius:50%;background:#1BA672;box-shadow:0 0 0 0 rgba(27,166,114,.6);animation:pulse 1.6s infinite}' +
    '@keyframes pulse{70%{box-shadow:0 0 0 7px rgba(27,166,114,0)}100%{box-shadow:0 0 0 0 rgba(27,166,114,0)}}' +
    '.ox{display:flex;gap:10px}.ox button{flex:1;font-size:28px;padding:10px 0;box-shadow:inset 0 -4px 0 rgba(0,0,0,.18)}' +
    '.ox .o{background:linear-gradient(#ff7fa3,#e5486f)}.ox .x{background:linear-gradient(#7d9bff,#4a6cf7)}' +
    '.mine{outline:3px solid #222;outline-offset:2px}.dark .mine{outline-color:#fff}' +
    '.legend{display:flex;justify-content:space-between;font-size:15px;font-weight:700;margin-top:14px}' +
    '.legend .lo{color:#e5486f}.legend .lx{color:#4a6cf7}' +
    '.tube{position:relative;margin-top:6px;height:64px}' +
    '.tube canvas{display:block;width:100%;height:64px}' +
    '.tilt{margin:8px 0 0;font-weight:700;text-align:center;min-height:1.6em}' +
    '</' + 'style><div class="wrap"><div class="card oxc"></div><div class="card gbc"></div></div>';
  var wrap = root.querySelector('.wrap');
  function theme() {
    try { wrap.classList.toggle('dark', lum(pageBg()) < 0.4); wrap.style.setProperty('--a', accent()); } catch (e) {}
  }

  function flagKey(k) { return 'sb-done:' + k + ':' + C.url; }
  var mem = {};
  function getFlag(k) { if (PREVIEW) return mem[k]; try { return localStorage.getItem(flagKey(k)); } catch (e) { return mem[k]; } }
  function setFlag(k, v) { mem[k] = v; if (PREVIEW) return; try { localStorage.setItem(flagKey(k), v); } catch (e) {} }

  function el(tag, cls, text) { var e = document.createElement(tag); if (cls) e.className = cls; if (text != null) e.textContent = text; return e; }
  function time(v) {
    var d = new Date(v); if (isNaN(d)) return '';
    function p(n) { return (n < 10 ? '0' : '') + n; }
    return (d.getMonth() + 1) + '월 ' + d.getDate() + '일 ' + p(d.getHours()) + ':' + p(d.getMinutes());
  }
  function norm(list) {
    if (!Array.isArray(list)) throw new Error('bad');
    return list.map(function (r) { var o = {}; for (var k in r) o[String(k).trim()] = r[k]; return o; });
  }
  var demo = { O: 6, X: 3, '방명록': [{ '시간': new Date().toISOString(), '닉네임': '예시 방문자', '내용': '미리보기용 예시 글이에요. 실제 페이지에서는 방문자가 남긴 글이 보여요.' }] };
  function api(q) { return C.url + (C.url.indexOf('?') < 0 ? '?' : '&') + q; }
  function load(sheet) {
    if (PREVIEW) return Promise.resolve(demo[sheet].slice());
    return fetch(api('sheet=' + encodeURIComponent(sheet))).then(function (r) { return r.json(); }).then(norm);
  }
  function loadCount() {
    if (PREVIEW) return Promise.resolve({ O: demo.O, X: demo.X });
    return fetch(api('count=OX')).then(function (r) { return r.json(); }).then(function (c) {
      if (!c || typeof c.O !== 'number') throw new Error('bad'); return c;
    });
  }
  // 저장 요청: 서버가 바쁘면 잠시 기다렸다가 최대 3번까지 다시 보내기
  function send(data, tries) {
    if (PREVIEW) return Promise.reject(new Error('preview'));
    tries = tries || 0;
    return fetch(C.url, { method: 'POST', body: JSON.stringify(data) }).then(function (r) { return r.text(); }).then(function (t) {
      if (t.indexOf('"ok"') < 0) throw new Error('busy'); return t;
    }).catch(function (e) {
      if (tries >= 3) throw e;
      return new Promise(function (ok) { setTimeout(ok, 1500 * (tries + 1) + Math.random() * 1500); }).then(function () { return send(data, tries + 1); });
    });
  }
  // 주기적으로 다시 불러오기: 실패하면 간격을 늘리고, 탭이 안 보이면 쉬기
  function poll(fn, base) {
    var fails = 0;
    function next() { setTimeout(tick, base * Math.min(5, 1 + fails) + Math.random() * 2000); }
    function tick() {
      if (document.hidden) { next(); return; }
      Promise.resolve(fn()).then(function (ok) { fails = ok === false ? fails + 1 : 0; next(); }, function () { fails++; next(); });
    }
    next();
  }
  function slow(m) { setTimeout(function () { if (m.textContent === '저장 중…') m.textContent = '저장 중… 지금 참여하는 사람이 많아서 조금 걸려요. 창을 닫지 말고 기다려 주세요.'; }, 4000); }
  function failText(e) {
    return e && e.message === 'preview' ? '미리보기에서는 저장되지 않아요. GitHub에 올린 뒤 시험해요.' : '서버와 연결하지 못했어요. 잠시 뒤 다시 눌러 보세요.';
  }

  function placeAndTheme() { place(); theme(); }
  if (document.readyState === 'loading') document.addEventListener('DOMContentLoaded', placeAndTheme); else placeAndTheme();
  window.addEventListener('load', function () { placeAndTheme(); setTimeout(placeAndTheme, 500); });

  buildOX(root.querySelector('.oxc'));
  buildGB(root.querySelector('.gbc'));

  // ---------- OX 투표: 액체 게이지 ----------
  function buildOX(card) {
    card.appendChild(el('h3', '', 'Q. ' + (C.q || '')));
    var box = el('div', 'ox'); var bo = el('button', 'o', 'O'); var bx = el('button', 'x', 'X');
    box.appendChild(bo); box.appendChild(bx);
    var msg = el('p', 'msg');
    var lg = el('div', 'legend'); var lo = el('span', 'lo', 'O 0명'); var lx = el('span', 'lx', 'X 0명'); lg.appendChild(lo); lg.appendChild(lx);
    var tube = el('div', 'tube'); var cv = el('canvas'); tube.appendChild(cv);
    var tilt = el('p', 'tilt');
    var top = el('div', 'top'); var count = el('span', 'live', '불러오는 중…'); var re = el('button', 're', '↻ 새로고침');
    top.appendChild(count); top.appendChild(re);
    [box, msg, lg, tube, tilt, top].forEach(function (x) { card.appendChild(x); });

    var o = 0, x = 0, target = 0.5, pos = 0.5, vel = 0, t0 = 0, running = false, seen = true;
    var bubbles = [];
    for (var i = 0; i < 14; i++) bubbles.push({ s: i % 2, x: Math.random(), y: Math.random(), r: 1 + Math.random() * 2.2, v: 0.15 + Math.random() * 0.35 });
    var calm = window.matchMedia && matchMedia('(prefers-reduced-motion: reduce)').matches;

    function mark() {
      var f = getFlag('OX'); if (!f) return;
      bo.disabled = bx.disabled = true;
      (f === 'O' ? bo : bx).classList.add('mine');
      msg.textContent = '내 선택: ' + f + ' · 참여해 줘서 고마워요!';
    }
    mark();
    function setCounts(no, nx) {
      o = no; x = nx;
      var n = o + x;
      target = n ? o / n : 0.5;
      lo.textContent = 'O ' + o + '명'; lx.textContent = 'X ' + x + '명';
      count.textContent = n ? '실시간 · 총 ' + n + '명 참여' : '실시간 · 아직 아무도 투표하지 않았어요';
      tilt.textContent = !n ? '첫 번째로 눌러 보세요!' : o > x ? 'O 쪽으로 기울었어요' : o < x ? 'X 쪽으로 기울었어요' : '팽팽해요!';
      kick();
    }
    function show(c) {
      if (c.O !== o || c.X !== x || count.textContent.indexOf('불러오는') === 0) setCounts(c.O, c.X);
    }
    var busy = false;
    function refresh() {
      if (busy) return true; busy = true;
      return loadCount().then(function (c) { busy = false; show(c); return true; }, function () { busy = false; if (!(o + x)) count.textContent = '결과를 불러오지 못했어요. 잠시 뒤 다시 시도해요.'; return false; });
    }
    re.addEventListener('click', refresh);
    function vote(v) {
      if (getFlag('OX')) return;
      bo.disabled = bx.disabled = true; msg.textContent = '저장 중…'; slow(msg);
      if (PREVIEW) { msg.textContent = failText(new Error('preview')); bo.disabled = bx.disabled = false; return; }
      send({ sheet: 'OX', '답': v }).then(function () { setFlag('OX', v); mark(); setCounts(o + (v === 'O' ? 1 : 0), x + (v === 'X' ? 1 : 0)); setTimeout(refresh, 1500); },
        function (e) { msg.textContent = failText(e); bo.disabled = bx.disabled = false; });
    }
    bo.addEventListener('click', function () { vote('O'); });
    bx.addEventListener('click', function () { vote('X'); });

    // 그리기
    var ctx = cv.getContext && cv.getContext('2d');
    function size() {
      var w = cv.clientWidth || 300, h = 64, d = window.devicePixelRatio || 1;
      if (cv.width !== Math.round(w * d)) { cv.width = Math.round(w * d); cv.height = Math.round(h * d); }
      return { w: w, h: h, d: d };
    }
    function capsule(c, x0, y0, w, h) {
      var r = h / 2;
      c.beginPath(); c.moveTo(x0 + r, y0); c.lineTo(x0 + w - r, y0); c.arc(x0 + w - r, y0 + r, r, -Math.PI / 2, Math.PI / 2);
      c.lineTo(x0 + r, y0 + h); c.arc(x0 + r, y0 + r, r, Math.PI / 2, Math.PI * 1.5); c.closePath();
    }
    function liquid(c, x0, y0, w, h, edge, left, cols) {
      var g = c.createLinearGradient(0, y0, 0, y0 + h);
      g.addColorStop(0, cols[0]); g.addColorStop(0.45, cols[1]); g.addColorStop(1, cols[2]);
      c.beginPath();
      var steps = 24, k;
      if (left) { c.moveTo(x0 - 2, y0 - 2); for (k = 0; k <= steps; k++) c.lineTo(edge(y0 + h * k / steps), y0 + h * k / steps); c.lineTo(x0 - 2, y0 + h + 2); }
      else { c.moveTo(x0 + w + 2, y0 - 2); for (k = 0; k <= steps; k++) c.lineTo(edge(y0 + h * k / steps), y0 + h * k / steps); c.lineTo(x0 + w + 2, y0 + h + 2); }
      c.closePath(); c.fillStyle = g; c.fill();
    }
    function frame(ts) {
      if (!ctx) return;
      if (!t0) t0 = ts;
      var t = (ts - t0) / 1000;
      vel += (target - pos) * 0.018; vel *= 0.9; pos += vel;
      var S = size(), w = S.w, h = S.h, c = ctx;
      c.setTransform(S.d, 0, 0, S.d, 0, 0); c.clearRect(0, 0, w, h);
      var pad = 3, X0 = pad, Y0 = pad, W = w - pad * 2, H = h - pad * 2;
      // 유리관 그림자
      c.save(); capsule(c, X0, Y0 + 2, W, H); c.fillStyle = 'rgba(0,0,0,.10)'; c.fill(); c.restore();
      c.save(); capsule(c, X0, Y0, W, H); c.clip();
      c.fillStyle = '#e9e9f1'; c.fillRect(X0, Y0, W, H);
      var amp = calm ? 1 : 4.5 + Math.min(12, Math.abs(vel) * 1000);
      var lean = Math.max(-18, Math.min(18, vel * 2600));
      var bx0 = X0 + W * pos;
      function edge(y) {
        var u = (y - Y0) / H;
        return bx0 + Math.sin(u * 6.2 + t * 3.1) * amp * 0.6 + Math.sin(u * 11 - t * 4.7) * amp * 0.4 + (u - 0.5) * lean;
      }
      liquid(c, X0, Y0, W, H, edge, true, ['#ff9dbb', '#e5486f', '#a3224a']);
      liquid(c, X0, Y0, W, H, edge, false, ['#9fb5ff', '#4a6cf7', '#2a3fb0']);
      // 앞쪽 물결(반투명): 겹쳐 흐르는 입체감
      function edge2(y) { var u = (y - Y0) / H; return edge(y) + Math.sin(u * 4 - t * 2.3) * (calm ? 1 : 7); }
      c.globalAlpha = 0.35;
      liquid(c, X0, Y0, W, H, edge2, true, ['#ffc2d4', '#f06b90', '#c23a62']);
      liquid(c, X0, Y0, W, H, edge2, false, ['#c6d3ff', '#6f8bff', '#3b52c9']);
      c.globalAlpha = 1;
      // 경계 거품
      c.beginPath(); for (var k = 0; k <= 24; k++) { var yy = Y0 + H * k / 24; if (k) c.lineTo(edge(yy), yy); else c.moveTo(edge(yy), yy); }
      c.strokeStyle = 'rgba(255,255,255,.75)'; c.lineWidth = 2.5; c.stroke();
      // 거품 방울
      bubbles.forEach(function (b) {
        if (!calm) { b.y -= b.v * 0.012; if (b.y < -0.1) { b.y = 1.1; b.x = Math.random(); } }
        var bx = b.s ? X0 + W * pos + (W * (1 - pos)) * b.x : X0 + W * pos * b.x;
        var by = Y0 + H * b.y + Math.sin(t * 2 + b.x * 9) * 1.5;
        if (Math.abs(bx - edge(by)) < 6) return;
        c.beginPath(); c.arc(bx, by, b.r, 0, Math.PI * 2); c.fillStyle = 'rgba(255,255,255,.45)'; c.fill();
      });
      // 유리 입체감: 위쪽 반사광, 아래쪽 그림자
      var gl = c.createLinearGradient(0, Y0, 0, Y0 + H);
      gl.addColorStop(0, 'rgba(255,255,255,.55)'); gl.addColorStop(0.28, 'rgba(255,255,255,.08)'); gl.addColorStop(0.62, 'rgba(255,255,255,0)'); gl.addColorStop(1, 'rgba(0,0,0,.22)');
      c.fillStyle = gl; c.fillRect(X0, Y0, W, H);
      c.beginPath(); c.moveTo(X0 + H * 0.5, Y0 + H * 0.2); c.lineTo(X0 + W - H * 0.5, Y0 + H * 0.2);
      c.strokeStyle = 'rgba(255,255,255,.55)'; c.lineWidth = 3; c.lineCap = 'round'; c.stroke();
      // 가운데 기준선
      c.beginPath(); c.setLineDash([3, 4]); c.moveTo(X0 + W / 2, Y0 + 4); c.lineTo(X0 + W / 2, Y0 + H - 4);
      c.strokeStyle = 'rgba(255,255,255,.7)'; c.lineWidth = 1.5; c.stroke(); c.setLineDash([]);
      // 글자
      var n = o + x, po = n ? Math.round(o / n * 100) : 50;
      c.font = '700 16px system-ui, sans-serif'; c.textBaseline = 'middle'; c.fillStyle = '#fff';
      c.shadowColor = 'rgba(0,0,0,.35)'; c.shadowBlur = 3;
      if (W * pos > 70) { c.textAlign = 'left'; c.fillText('O ' + (n ? po + '%' : ''), X0 + 18, Y0 + H / 2); }
      if (W * (1 - pos) > 70) { c.textAlign = 'right'; c.fillText((n ? 100 - po + '% ' : '') + 'X', X0 + W - 18, Y0 + H / 2); }
      c.shadowBlur = 0;
      c.restore();
      c.save(); capsule(c, X0, Y0, W, H); c.strokeStyle = 'rgba(0,0,0,.15)'; c.lineWidth = 1; c.stroke(); c.restore();
      var still = Math.abs(target - pos) < 0.0005 && Math.abs(vel) < 0.00005;
      if (seen && (!calm || !still)) requestAnimationFrame(frame); else running = false;
    }
    function kick() { if (!running && ctx) { running = true; requestAnimationFrame(frame); } }
    if (window.IntersectionObserver) new IntersectionObserver(function (en) { seen = en[0].isIntersecting; if (seen) kick(); }).observe(tube);
    window.addEventListener('resize', kick);
    kick();
    refresh();
    // 실시간: 화면에 보이는 동안 몇 초마다 개수를 다시 불러오기(폴링)
    poll(function () {
      if (!seen) return true;
      if (PREVIEW) { if (Math.random() < 0.5) demo.O++; else demo.X++; }
      return refresh();
    }, PREVIEW ? 2500 : 6000);
  }

  // ---------- 방명록 ----------
  function buildGB(card) {
    card.appendChild(el('h3', '', C.title || '방명록'));
    var form = el('div', 'row');
    var nick = el('input'); nick.placeholder = '닉네임 (10자까지)'; nick.maxLength = 10;
    var text = el('textarea'); text.placeholder = '남기고 싶은 말 (100자까지)'; text.maxLength = 100;
    var btn = el('button', '', '남기기');
    form.appendChild(nick); form.appendChild(text); form.appendChild(btn);
    var msg = el('p', 'msg');
    var top = el('div', 'top'); var count = el('span', '', '불러오는 중…'); var re = el('button', 're', '↻ 새로고침');
    top.appendChild(count); top.appendChild(re);
    var ul = el('ul', 'list');
    [form, msg, top, ul].forEach(function (x) { card.appendChild(x); });
    function lock() { form.style.display = 'none'; msg.textContent = '방명록을 남겼어요. 고마워요!'; }
    if (getFlag('GB')) lock();
    var last = -1;
    function show(list) {
      var key = list.length + '|' + JSON.stringify(list[list.length - 1] || '');
      if (key === last) return; last = key;
      ul.innerHTML = '';
      count.textContent = list.length >= 50 ? '최근 방명록 50개' : '방명록 ' + list.length + '개';
      list.slice().reverse().forEach(function (r) {
        var li = el('li'); li.appendChild(el('b', '', r['닉네임'] || '익명')); li.appendChild(el('small', '', time(r['시간'])));
        li.appendChild(el('p', '', r['내용'] || '')); ul.appendChild(li);
      });
    }
    function refresh(force) { if (force) last = -1; return load('방명록').then(function (l) { show(l); return true; }, function () { if (last === -1) count.textContent = '목록을 불러오지 못했어요. 잠시 뒤 다시 시도해요.'; return false; }); }
    re.addEventListener('click', function () { count.textContent = '불러오는 중…'; refresh(true); });
    btn.addEventListener('click', function () {
      var n = nick.value.trim(), t = text.value.trim();
      if (!n || !t) { msg.textContent = '닉네임과 내용을 모두 써 주세요.'; return; }
      btn.disabled = true; msg.textContent = '저장 중…'; slow(msg);
      send({ sheet: '방명록', '닉네임': n, '내용': t }).then(function () { setFlag('GB', '1'); lock(); refresh(true); }, function (e) { msg.textContent = failText(e); btn.disabled = false; });
    });
    refresh(true);
    if (!PREVIEW) poll(function () { return refresh(); }, 20000);
  }
})();

</script><!-- ▲ 방명록·OX 투표 끝 ▲ -->
    
    
    

    <script>
        /* ==========================================
           1. 별명 글자 통통 튀는 애니메이션 초기화
           ========================================== */
        (function initBouncingTitle() {
            const titleEl = document.getElementById('bouncingTitle');
            const text = "안녕하세요 금주찡 입니다";
            titleEl.innerHTML = '';

            [...text].forEach((char, index) => {
                const span = document.createElement('span');
                span.textContent = char === ' ' ? '\u00A0' : char;
                // 각 글자마다 딜레이를 다르게 주어 파도처럼 통통 튀게 만듦
                span.style.animationDelay = `${index * 0.08}s`;
                titleEl.appendChild(span);
            });
        })();

        /* ==========================================
           2. 마우스 & 터치 따라다니는 반짝이 효과
           ========================================== */
        (function initSparkleTrail() {
            const sparkles = ['✨', '🐾', '💛', '⭐', '🌼'];
            let lastTime = 0;

            function createSparkle(x, y) {
                const now = Date.now();
                // 너무 많은 요소가 생성되지 않도록 40ms 간격 제한
                if (now - lastTime < 40) return;
                lastTime = now;

                const el = document.createElement('span');
                el.className = 'sparkle';
                el.textContent = sparkles[Math.floor(Math.random() * sparkles.length)];
                el.style.left = `${x}px`;
                el.style.top = `${y}px`;
                el.style.fontSize = `${Math.floor(Math.random() * 10) + 14}px`;

                document.body.appendChild(el);
                setTimeout(() => el.remove(), 800);
            }

            window.addEventListener('mousemove', (e) => {
                createSparkle(e.clientX, e.clientY);
            });

            window.addEventListener('touchmove', (e) => {
                if (e.touches.length > 0) {
                    createSparkle(e.touches[0].clientX, e.touches[0].clientY);
                }
            }, { passive: true });
        })();

        /* ==========================================
           3. 방문자 환영 인사 기능
           ========================================== */
        const visitorInput = document.getElementById('visitorName');
        const greetBtn = document.getElementById('greetBtn');
        const welcomeOutput = document.getElementById('welcomeOutput');

        function handleGreeting() {
            const name = visitorInput.value.trim();
            welcomeOutput.style.display = 'block';
            // 애니메이션 재실행을 위한 트릭
            welcomeOutput.style.animation = 'none';
            welcomeOutput.offsetHeight; 
            welcomeOutput.style.animation = 'popIn 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275)';

            if (!name) {
                welcomeOutput.textContent = "이름 없는 길냥이 손님도 격하게 환영한다냥! 🐱💛";
            } else {
                welcomeOutput.textContent = `야옹~ 반가워요, ${name}님! 금주찡의 고양이 천국에서 푹 쉬다 가세요! 🐾✨`;
                spawnConfetti(['🐾', '💛', '🐱', '✨'], 15);
            }
        }

        greetBtn.addEventListener('click', handleGreeting);
        visitorInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') handleGreeting();
        });

        /* ==========================================
           4. OX 퀴즈 및 축하/아쉬움 효과
           ========================================== */
        function checkQuiz(userAnswer) {
            const feedbackEl = document.getElementById('quizFeedback');
            feedbackEl.style.display = 'block';
            feedbackEl.className = 'quiz-feedback'; // 클래스 초기화

            // 강제 리플로우로 애니메이션 재시작
            void feedbackEl.offsetWidth;

            if (userAnswer === true) {
                // 정답 (O)
                feedbackEl.classList.add('quiz-correct');
                feedbackEl.innerHTML = "🎉 딩동댕! 정답이에요! 🎉<br>집 침대 위에서 뒹굴거리는 게 세상에서 제일 행복하답니다! 🏠💛";
                spawnConfetti(['🎉', '🐱', '💛', '✨', '🏠', '🐾'], 35);
            } else {
                // 오답 (X)
                feedbackEl.classList.add('quiz-wrong');
                feedbackEl.innerHTML = "😿 땡! 아쉬워요~ 😿<br>금주찡은 집순이 그 자체! 정답은 O랍니다! 다시 눌러보세요~";
                spawnConfetti(['💧', '😿', '☁️'], 12);
            }
        }

        // 화면 전체에 파티클 흩뿌리기 헬퍼 함수
        function spawnConfetti(emojis, count) {
            for (let i = 0; i < count; i++) {
                const particle = document.createElement('div');
                particle.className = 'confetti-particle';
                particle.textContent = emojis[Math.floor(Math.random() * emojis.length)];

                // 화면 중앙 부근에서 사방으로 퍼지게 설정
                const startX = window.innerWidth / 2 + (Math.random() - 0.5) * 160;
                const startY = window.innerHeight / 2 + (Math.random() - 0.5) * 100;
                const tx = (Math.random() - 0.5) * 500 + 'px';
                const ty = (Math.random() - 0.8) * 500 + 'px';

                particle.style.left = `${startX}px`;
                particle.style.top = `${startY}px`;
                particle.style.setProperty('--tx', tx);
                particle.style.setProperty('--ty', ty);

                document.body.appendChild(particle);
                setTimeout(() => particle.remove(), 2200);
            }
        }

        /* ==========================================
           5. 오늘의 운세 (12가지 준비)
           ========================================== */
        const fortunes = [
            { badge: "🌟 대길 냥이", text: "길 가다 귀여운 길냥이와 눈이 마주치는 행운의 날! 오늘 하는 일마다 술술 풀릴 거예요." },
            { badge: "🍱 맛밥 운세", text: "오늘 먹는 밥이 평소보다 2배는 더 맛있게 느껴질 거예요! 맛있는 간식도 꼭 챙겨 드세요." },
            { badge: "🛌 꿀잠 예약", text: "침대에 눕자마자 3초 만에 기절하듯 꿀잠에 빠질 운세! 개운한 내일이 기다려요." },
            { badge: "💖 사랑둥이", text: "주변 사람들에게 귀여움과 칭찬을 듬뿍 받는 날! 웃는 얼굴이 행운을 불러옵니다." },
            { badge: "🍀 네잎클로버", text: "생각지도 못한 소소한 행운이 찾아와요! 주머니 속이나 가방 속에서 반가운 걸 발견할지도?" },
            { badge: "🐾 젤리 파워", text: "지칠 땐 말랑한 고양이 발바닥을 떠올려 보세요! 오후에 갑자기 에너지가 뿜뿜 솟아납니다." },
            { badge: "🎁 깜짝 선물", text: "기분 좋은 소식이나 작은 선물이 도착할 예감! 오늘 하루는 설레는 마음으로 보내보세요." },
            { badge: "☀️ 햇살 낮잠", text: "창가로 들어오는 따뜻한 햇살처럼 마음이 평온해지는 날이에요. 여유를 즐겨보세요." },
            { badge: "🎵 콧노래 흥얼", text: "저절로 콧노래가 나올 만큼 기분 좋은 일이 생겨요! 좋아하는 노래를 들으면 행운이 2배!" },
            { badge: "🐟 참치캔 대박", text: "재물운이 반짝반짝! 작은 돈을 아끼거나 맛있는 걸 얻어먹을 찬스가 찾아옵니다." },
            { badge: "🌈 무지개 다리", text: "걱정하던 일이 눈 녹듯 사라지는 날! 걱정 말고 오늘을 신나게 즐기면 그만이에요." },
            { badge: "👑 고양이 왕국", text: "오늘은 내가 바로 이 구역의 주인공! 무엇을 선택하든 최고의 결과로 이어질 거예요." }
        ];

        const fortuneBtn = document.getElementById('fortuneBtn');
        const fortuneResult = document.getElementById('fortuneResult');
        let lastFortuneIdx = -1;

        fortuneBtn.addEventListener('click', () => {
            let idx;
            // 연속으로 같은 운세가 나오지 않도록 처리
            do {
                idx = Math.floor(Math.random() * fortunes.length);
            } while (idx === lastFortuneIdx);
            lastFortuneIdx = idx;

            const chosen = fortunes[idx];
            fortuneResult.innerHTML = `
                <div class="fortune-badge">${chosen.badge}</div>
                <p style="animation: popIn 0.35s ease;">${chosen.text}</p>
            `;
            spawnConfetti(['✨', '🔮', '🐾'], 10);
        });

        /* ==========================================
           6. 10초 버튼 누르기 미니게임
           ========================================== */
        const clickerBtn = document.getElementById('clickerBtn');
        const clickerLabel = document.getElementById('clickerLabel');
        const timeLeftEl = document.getElementById('timeLeft');
        const clickCountEl = document.getElementById('clickCount');
        const gameResultMsg = document.getElementById('gameResultMsg');
        const resetGameBtn = document.getElementById('resetGameBtn');

        let gameState = 'idle'; // 'idle' | 'playing' | 'ended'
        let count = 0;
        let timeLeft = 10.0;
        let timerInterval = null;

        clickerBtn.addEventListener('click', () => {
            if (gameState === 'ended') return;

            if (gameState === 'idle') {
                // 게임 시작
                gameState = 'playing';
                count = 1;
                timeLeft = 10.0;
                clickCountEl.textContent = count;
                clickerLabel.textContent = "꾹꾹 누르냥!";
                gameResultMsg.textContent = "더 빠르게! 냥젤리 꾹꾹이 중... 🐾🔥";

                const startTime = Date.now();
                timerInterval = setInterval(() => {
                    const elapsed = (Date.now() - startTime) / 1000;
                    const remaining = Math.max(0, 10 - elapsed);
                    timeLeftEl.textContent = remaining.toFixed(1);

                    if (remaining <= 0) {
                        endGame();
                    }
                }, 50);
            } else if (gameState === 'playing') {
                // 게임 진행 중 카운트 증가
                count++;
                clickCountEl.textContent = count;
            }
        });

        function endGame() {
            clearInterval(timerInterval);
            gameState = 'ended';
            timeLeftEl.textContent = "0.0";
            clickerLabel.textContent = "종료!";
            resetGameBtn.style.display = 'inline-flex';

            let rankMsg = "";
            if (count >= 70) {
                rankMsg = `🏆 전설의 광속 냥펀치! (${count}번) 금주찡이 감동해서 골골송을 부릅니다!`;
                spawnConfetti(['👑', '🐾', '🎉', '🐟'], 30);
            } else if (count >= 45) {
                rankMsg = `😻 프로 집사 손놀림! (${count}번) 엄청난 스피드예요!`;
                spawnConfetti(['🐾', '💛', '✨'], 20);
            } else if (count >= 25) {
                rankMsg = `🐱 귀여운 꾹꾹이 실력! (${count}번) 고양이들이 좋아할 속도네요!`;
            } else {
                rankMsg = `🦥 느긋한 나무늘보 냥이! (${count}번) 여유로운 꾹꾹이도 매력 있어요!`;
            }

            gameResultMsg.textContent = rankMsg;
        }

        resetGameBtn.addEventListener('click', () => {
            gameState = 'idle';
            count = 0;
            timeLeft = 10.0;
            timeLeftEl.textContent = "10.0";
            clickCountEl.textContent = "0";
            clickerLabel.textContent = "눌러서 시작!";
            gameResultMsg.textContent = "준비되셨나요? 버튼을 누르면 바로 시작돼요!";
            resetGameBtn.style.display = 'none';
        });
    </script>
</body></html>
