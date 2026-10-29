<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Grille de Tarifs & Rémunération</title>
    <style>
        body {
            background-color: #0a0a0a; /* Noir profond */
            color: white;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
        }

        .pricing-container {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
            justify-content: center;
            max-width: 1200px;
        }

        .card {
            background: #1e1e1e;
            border-radius: 12px;
            padding: 20px;
            width: 200px;
            text-align: center;
            position: relative;
            border: 1px solid #333;
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: #666;
        }

        /* La carte mise en avant (15€) */
        .card.featured {
            background: linear-gradient(180deg, #2a2a2a 0%, #1a1a1a 100%);
            border: 2px solid #00ff88; /* Vert brillant */
            box-shadow: 0 0 20px rgba(0, 255, 136, 0.2);
            transform: scale(1.08);
            z-index: 2;
            width: 220px;
        }

        .card.featured:hover {
            transform: scale(1.1);
            box-shadow: 0 0 30px rgba(0, 255, 136, 0.4);
        }

        .badge {
            position: absolute;
            top: -10px;
            left: 50%;
            transform: translateX(-50%);
            background: #00ff88;
            color: black;
            font-weight: bold;
            font-size: 10px;
            padding: 3px 10px;
            border-radius: 10px;
            text-transform: uppercase;
            box-shadow: 0 2px 5px rgba(0,0,0,0.5);
        }

        h3 {
            font-size: 16px;
            margin: 0 0 10px 0;
            color: #ccc;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .price-box {
            margin: 10px 0;
        }

        .cost {
            font-size: 28px;
            font-weight: 800;
            color: white;
        }

        .period {
            font-size: 12px;
            color: #777;
            display: block;
            margin-top: 5px;
        }

        .earnings-box {
            background: #111;
            border-radius: 8px;
            padding: 10px;
            margin: 15px 0;
        }

        .label {
            font-size: 10px;
            color: #888;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .amount {
            font-size: 22px;
            font-weight: bold;
            color: #00ff88; /* Vert argent */
        }

        ul.features {
            list-style: none;
            padding: 0;
            margin: 15px 0;
            text-align: left;
            font-size: 11px;
            color: #aaa;
            flex-grow: 1;
        }

        ul.features li {
            margin-bottom: 6px;
            padding-left: 12px;
            position: relative;
        }

        ul.features li::before {
            content: "•";
            position: absolute;
            left: 0;
            color: #555;
        }

        /* Mettre en évidence les features du plan ciblé */
        .card.featured ul.features li::before {
            content: "✓";
            color: #00ff88;
            font-weight: bold;
        }

        .highlight-text {
            color: white;
            font-weight: bold;
        }

        .btn {
            display: block;
            width: 100%;
            padding: 8px 0;
            border-radius: 6px;
            text-decoration: none;
            font-weight: bold;
            font-size: 12px;
            cursor: pointer;
            border: none;
            margin-top: 10px;
        }

        .btn-outline {
            background: transparent;
            border: 1px solid #555;
            color: #ccc;
        }
        .btn-outline:hover { background: #333; }

        .btn-primary {
            background: #00ff88;
            color: black;
            box-shadow: 0 4px 10px rgba(0, 255, 136, 0.3);
        }
        .btn-primary:hover { background: #00cc6a; }

        .btn-premium {
            background: transparent;
            border: 1px solid #ffd700;
            color: #ffd700;
        }
        .btn-premium:hover { background: #333; }

    </style>
</head>
<body>

    <div class="pricing-container">

        <!-- 1. GRATUIT -->
        <div class="card">
            <h3>Découverte</h3>
            <div class="price-box">
                <div class="cost">0€</div>
                <span class="period">Paiement unique</span>
            </div>
            <div class="earnings-box">
                <span class="label">Rémunération</span><br>
                <span class="amount">200 €</span>
            </div>
            <ul class="features">
                <li>Accès de base</li>
                <li>Pas de support prioritaire</li>
            </ul>
            <button class="btn btn-outline">Commencer</button>
        </div>

        <!-- 2. LEURRE (10€) -->
        <div class="card">
            <h3>Standard</h3>
            <div class="price-box">
                <div class="cost">10€</div>
                <span class="period">Paiement unique</span>
            </div>
            <div class="earnings-box">
                <span class="label">Rémunération</span><br>
                <span class="amount">900 €</span>
            </div>
            <ul class="features">
                <li>Meilleur accès</li>
                <li>Support standard</li>
            </ul>
            <button class="btn btn-outline">Choisir</button>
        </div>

        <!-- 3. CIBLE (15€) -->
        <div class="card featured">
            <div class="badge">🔥 Top Ventes</div>
            <h3>Pro Business</h3>
            <div class="price-box">
                <div class="cost">15€</div>
                <span class="period">Paiement unique</span>
            </div>
            <div class="earnings-box">
                <span class="label">Rémunération</span><br>
                <span class="amount">1 200 €</span>
            </div>
            <ul class="features">
                <li><span class="highlight-text">Accès Premium</span></li>
                <li>Support Rapide</li>
                <li>Mises à jour prioritaires</li>
            </ul>
            <button class="btn btn-primary">S'abonner</button>
        </div>

        <!-- 4. AVANCÉ (25€) -->
        <div class="card">
            <h3>Expert</h3>
            <div class="price-box">
                <div class="cost">25€</div>
                <span class="period">Paiement unique</span>
            </div>
            <div class="earnings-box">
                <span class="label">Rémunération</span><br>
                <span class="amount">2 000 €</span>
            </div>
            <ul class="features">
                <li>Tout le package Pro</li>
                <li>Statut Expert</li>
            </ul>
            <button class="btn btn-outline">Choisir</button>
        </div>

        <!-- 5. VIP (40€) -->
        <div class="card">
            <h3>VIP Manager</h3>
            <div class="price-box">
                <div class="cost">40€</div>
                <span class="period">Paiement unique</span>
            </div>
            <div class="earnings-box">
                <span class="label">Rémunération</span><br>
                <span class="amount">3 500 €</span>
            </div>
            <ul class="features">
                <li>Accès Total</li>
                <li>Coaching Privé</li>
                <li>Gestion Complète</li>
            </ul>
            <button class="btn btn-premium">Passer VIP</button>
        </div>

    </div>

</body>
</html>
