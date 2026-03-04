<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Бледно-зелёный · Реферальная программа</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background: linear-gradient(145deg, #f2f9ec 0%, #e2f0da 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1.5rem;
            line-height: 1.5;
            color: #2f4f3a;
        }

        /* мягкая воздушная карточка */
        .glass-card {
            width: 100%;
            max-width: 1100px;
            background: rgba(255, 255, 255, 0.6);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border-radius: 48px 48px 48px 48px;
            box-shadow: 
                0 20px 40px -10px rgba(100, 120, 100, 0.25),
                inset 0 1px 1px rgba(255, 255, 255, 0.6);
            padding: 2.8rem 2.5rem;
            border: 1px solid rgba(190, 215, 180, 0.5);
            transition: all 0.3s ease;
        }

        /* шапка */
        .header {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2.5rem;
            gap: 1rem;
        }

        .logo-area {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .soft-icon {
            background: #d4e8ca;
            width: 48px;
            height: 48px;
            border-radius: 30% 70% 70% 30% / 30% 55% 45% 70%;
            box-shadow: 0 12px 18px -12px #9bbf8b;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #558b5f;
            font-size: 1.8rem;
            font-weight: 300;
            border: 1px solid #e2f0da;
        }

        .logo-text {
            font-size: 1.7rem;
            font-weight: 350;
            letter-spacing: -0.02em;
            color: #2d5a3b;
            text-shadow: 2px 2px 20px rgba(170, 210, 150, 0.5);
        }

        .ref-badge {
            background: #e1f0da;
            border-radius: 60px;
            padding: 0.65rem 1.6rem;
            font-size: 0.95rem;
            color: #2b5c38;
            border: 1px solid #c6dfbb;
            box-shadow: 0 6px 14px -8px #a6c89a;
            font-weight: 400;
            backdrop-filter: blur(4px);
        }

        /* главный призыв */
        .hero {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            margin-bottom: 3rem;
            align-items: center;
        }

        .hero-left {
            flex: 1 1 280px;
        }

        .hero-left h1 {
            font-size: 2.7rem;
            font-weight: 380;
            line-height: 1.2;
            letter-spacing: -0.02em;
            color: #204e2d;
            margin-bottom: 0.5rem;
            text-shadow: 0 2px 5px rgba(170, 200, 150, 0.3);
        }

        .hero-left .highlight {
            font-weight: 420;
            background: linear-gradient(145deg, #bcddae, #d0eac2);
            padding: 0.2rem 1rem;
            border-radius: 60px;
            display: inline-block;
            border: 1px solid #bfdeb2;
            box-shadow: 0 8px 14px -12px #6f9a78;
            margin: 0.5rem 0 1rem 0;
            font-size: 1.3rem;
        }

        .hero-left p {
            font-size: 1.15rem;
            color: #3b6044;
            max-width: 450px;
            font-weight: 300;
            margin-bottom: 1.5rem;
        }

        .hero-right {
            flex: 1 1 260px;
            background: rgba(235, 248, 225, 0.6);
            border-radius: 36px;
            padding: 1.8rem 1.8rem;
            border: 1px solid #cae3be;
            box-shadow: inset 0 0 0 1px rgba(255,255,240,0.8), 0 18px 30px -20px #486c4e;
            backdrop-filter: blur(4px);
        }

        .ref-link-box {
            background: #ffffffb3;
            border-radius: 32px;
            padding: 0.9rem 1.2rem;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 8px;
            border: 1px solid #b7d8ab;
            margin-bottom: 1.2rem;
            box-shadow: 0 8px 12px -12px #7da079;
        }

        .ref-link-box span {
            color: #2a5536;
            word-break: break-all;
            font-weight: 420;
            font-size: 1rem;
            background: #e8f5e0;
            padding: 0.3rem 1rem;
            border-radius: 40px;
            border: 1px dashed #b2d3a3;
        }

        .ref-link-box .fake-link {
            background: transparent;
            border: none;
            font-weight: 350;
            color: #3d704a;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .invite-btn {
            background: #b7d8ab;
            border: none;
            border-radius: 40px;
            padding: 0.6rem 1.5rem;
            font-size: 1rem;
            color: #1f4a2b;
            font-weight: 450;
            cursor: default;
            box-shadow: 0 6px 12px -8px #67946e;
            border: 1px solid #cdeac1;
            transition: 0.15s;
            display: inline-flex;
            align-items: center;
            gap: 6px;
        }

        .stat-row {
            display: flex;
            justify-content: space-between;
            color: #2a5435;
            font-size: 1.05rem;
            padding: 0.5rem 0;
            border-bottom: 1px dashed #bddbb1;
        }

        .stat-row:last-child {
            border-bottom: none;
        }

        .stat-number {
            font-weight: 480;
            background: #cdeac1;
            padding: 0.1rem 1rem;
            border-radius: 50px;
            font-size: 1.1rem;
        }

        /* как это работает (плавные иконки) */
        .steps {
            display: flex;
            flex-wrap: wrap;
            gap: 1.8rem;
            margin: 3rem 0 2.5rem 0;
            justify-content: center;
        }

        .step-item {
            flex: 1 1 180px;
            background: rgba(250, 255, 245, 0.4);
            backdrop-filter: blur(4px);
            border-radius: 34px;
            padding: 1.5rem 1rem;
            text-align: center;
            border: 1px solid #d1e7c4;
            box-shadow: 0 12px 18px -16px #7d9f7d;
            transition: all 0.25s;
        }

        .step-item:hover {
            background: rgba(245, 255, 235, 0.7);
            transform: translateY(-4px);
        }

        .step-icon {
            background: #d7edcc;
            width: 60px;
            height: 60px;
            border-radius: 50% 30% 50% 30%;
            margin: 0 auto 1rem auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: #3b7249;
            border: 1px solid #ebfbe2;
            box-shadow: 0 8px 12px -12px #558d5e;
        }

        .step-item h3 {
            font-weight: 420;
            margin-bottom: 0.5rem;
            color: #1f4a2b;
            font-size: 1.3rem;
        }

        .step-item p {
            font-size: 0.95rem;
            color: #3d6044;
            font-weight: 300;
        }

        /* таблица рефералов / друзей */
        .referrals-section {
            background: rgba(245, 255, 240, 0.5);
            border-radius: 40px;
            padding: 1.8rem 1.8rem;
            border: 1px solid #cbe5bf;
            backdrop-filter: blur(4px);
            margin-top: 2.2rem;
        }

        .section-title {
            font-weight: 380;
            font-size: 1.8rem;
            color: #255232;
            margin-bottom: 1rem;
            letter-spacing: -0.01em;
        }

        .referral-list {
            display: flex;
            flex-direction: column;
            gap: 0.7rem;
        }

        .ref-row {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            background: #ffffffb0;
            padding: 0.9rem 1.5rem;
            border-radius: 60px;
            border: 1px solid #beddaf;
            box-shadow: 0 4px 10px -9px #568f5e;
            font-weight: 350;
        }

        .ref-row-left {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .avatar {
            background: #ceeac1;
            width: 38px;
            height: 38px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #1c4827;
            font-weight: 400;
            border: 1px solid #e4fada;
        }

        .status {
            font-size: 0.8rem;
            background: #d2ecbe;
            padding: 0.2rem 0.8rem;
            border-radius: 60px;
            border: 1px solid #b7dcab;
        }

        .ref-row-right {
            font-weight: 420;
            color: #1e512b;
        }

        .footnote {
            margin-top: 2rem;
            text-align: center;
            font-size: 0.95rem;
            color: #487a52;
            border-top: 1px solid #c9e3bc;
            padding-top: 1.5rem;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 1rem;
        }

        .earnings {
            background: #e2f3d9;
            border-radius: 80px;
            padding: 0.5rem 1.6rem;
            border: 1px solid #beddaf;
            font-weight: 440;
        }

        button {
            background: #b4d6a6;
            border: none;
            border-radius: 50px;
            padding: 0.6rem 2rem;
            font-size: 1rem;
            color: #1e4829;
            font-weight: 420;
            border: 1px solid #d2edc2;
            box-shadow: 0 6px 12px -12px #57855e;
            transition: 0.18s;
            cursor: default;
        }

        button:hover {
            background: #c2e2b4;
            box-shadow: 0 8px 18px -12px #67946e;
        }

        .soft-link {
            color: #2a6239;
            text-decoration: none;
            border-bottom: 1px dotted #b1d8a1;
        }

        /* адаптив */
        @media (max-width: 640px) {
            .glass-card {
                padding: 1.8rem 1.5rem;
                border-radius: 32px;
            }
            .hero-left h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="glass-card">

        <!-- шапка -->
        <div class="header">
            <div class="logo-area">
                <div class="soft-icon">✦</div>
                <span class="logo-text">bloom</span>
            </div>
            <div class="ref-badge">
                🌱 твой баланс · <strong>1,240</strong> баллов
            </div>
        </div>

        <!-- основной блок с реферальной ссылкой -->
        <div class="hero">
            <div class="hero-left">
                <h1>приглашай друзей <br>и получай бонусы</h1>
                <div class="highlight">каждый друг — +150₽ на счет</div>
                <p>Прозрачные начисления, никаких заморочек. Делитесь уютом и зелёными бонусами.</p>
                <div class="ref-link-box" style="max-width: 400px;">
                    <span>bloom.cc/you/softgreen</span>
                    <div class="fake-link">🔗 скопировать</div>
                </div>
            </div>
            <div class="hero-right">
                <div style="font-weight: 380; font-size: 1.3rem; margin-bottom: 1rem;">🍃 рефералы</div>
                <div class="stat-row">
                    <span>активные</span>
                    <span class="stat-number">14</span>
                </div>
                <div class="stat-row">
                    <span>в ожидании</span>
                    <span class="stat-number">3</span>
                </div>
                <div class="stat-row">
                    <span>за всё время</span>
                    <span class="stat-number">42</span>
                </div>
                <div style="margin-top: 1rem;">
                    <button>➕ создать новый код</button>
                </div>
            </div>
        </div>

        <!-- три шага с мягкими иконками -->
        <div class="steps">
            <div class="step-item">
                <div class="step-icon">1️⃣</div>
                <h3>получи ссылку</h3>
                <p>твоя персональная ссылка уже ждёт сверху</p>
            </div>
            <div class="step-item">
                <div class="step-icon">🌿</div>
                <h3>поделись</h3>
                <p>отправь друзьям, добавь в соцсети</p>
            </div>
            <div class="step-item">
                <div class="step-icon">2️⃣</div>
                <h3>получай бонус</h3>
                <p>как только друг активируется — начисление автоматически</p>
            </div>
        </div>

        <!-- списочек приглашённых -->
        <div class="referrals-section">
            <div class="section-title">👥 недавние друзья</div>
            <div class="referral-list">

                <div class="ref-row">
                    <div class="ref-row-left">
                        <div class="avatar">А</div>
                        <span>Алина К.</span>
                        <span class="status">активна</span>
                    </div>
                    <div class="ref-row-right">+150₽</div>
                </div>

                <div class="ref-row">
                    <div class="ref-row-left">
                        <div class="avatar">Д</div>
                        <span>Дмитрий С.</span>
                        <span class="status">активен</span>
                    </div>
                    <div class="ref-row-right">+150₽</div>
                </div>

                <div class="ref-row">
                    <div class="ref-row-left">
                        <div class="avatar">Е</div>
                        <span>Елена В.</span>
                        <span class="status">активна</span>
                    </div>
                    <div class="ref-row-right">+150₽</div>
                </div>

                <div class="ref-row">
                    <div class="ref-row-left">
                        <div class="avatar">М</div>
                        <span>Михаил П.</span>
                        <span class="status">ждёт</span>
                    </div>
                    <div class="ref-row-right">—</div>
                </div>
            </div>
            <div style="margin-top: 1.4rem; text-align: right;">
                <a href="#" class="soft-link">показать ещё →</a>
            </div>
        </div>

        <!-- нижняя плашка с доп ссылками и итогами -->
        <div class="footnote">
            <div class="earnings">🏆 заработано всего: 4 350 ₽</div>
            <div style="display: flex; gap: 1.5rem; flex-wrap: wrap;">
                <a href="#" class="soft-link">правила</a>
                <a href="#" class="soft-link">выплаты</a>
                <a href="#" class="soft-link">поддержка</a>
            </div>
            <div style="font-weight: 300;">🌱 сделано с заботой</div>
        </div>

        <!-- маленькая подсказка-имитация реф. программы (не функциональна, только дизайн) -->
        <div style="height: 1px; background: linear-gradient(90deg, transparent, #b6dbaa, transparent); margin: 1.5rem 0 0.5rem;"></div>
        <p style="text-align: center; opacity: 0.7; font-size: 0.85rem;">* демо интерфейса · реферальная программа в бледно‑зелёных тонах</p>
    </div>
</body>
</html>
