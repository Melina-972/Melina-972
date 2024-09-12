<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NLM - Boutique en ligne de vêtements</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="logo">
            <h1>NLM</h1>
        </div>
        <nav>
            <ul>
                <li><a href="#home">Accueil</a></li>
                <li><a href="#catalog">Catalogue</a></li>
                <li><a href="#cart">Panier</a></li>
            </ul>
        </nav>
    </header>

    <!-- Section Accueil -->
    <section id="home">
        <h2>Bienvenue chez NLM</h2>
        <p>Découvrez notre sélection exclusive de vêtements tendance.</p>
        <button onclick="scrollToCatalog()">Voir le catalogue</button>
    </section>

    <!-- Catalogue des produits -->
    <section id="catalog">
        <h2>Catalogue</h2>
        <div class="product-container">
            <!-- Exemple de produit -->
            <div class="product-card">
                <img src="tshirt.jpg" alt="T-shirt">
                <h3>T-shirt NLM</h3>
                <p>Prix : 25€</p>
                <button onclick="addToCart('T-shirt NLM', 25)">Ajouter au panier</button>
            </div>
            <!-- Ajoutez plus de produits ici -->
        </div>
    </section>

    <!-- Section Panier -->
    <section id="cart">
        <h2>Panier</h2>
        <div id="cartItems"></div>
        <p>Total : <span id="totalPrice">0</span>€</p>
        <button onclick="checkout()">Passer la commande</button>
    </section>

    <script src="script.js"></script>
</body>
</html>
/* styles.css */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    display: flex;
    justify-content: space-between;
    background-color: #333;
    padding: 1em;
    color: white;
}

nav ul {
    list-style: none;
    display: flex;
    gap: 1em;
}

nav ul li {
    display: inline;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

section {
    padding: 2em;
    text-align: center;
}

#home {
    background-color: #f4f4f4;
    padding: 5em 2em;
}

.product-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 2em;
}

.product-card {
    border: 1px solid #ddd;
    padding: 1em;
    width: 200px;
    text-align: center;
}

button {
    background-color: #333;
    color: white;
    border: none;
    padding: 0.5em 1em;
    cursor: pointer;
}

button:hover {
    background-color: #555;
}

#cart {
    background-color: #f4f4f4;
    padding: 2em;
}

#cartItems {
    margin-bottom: 1em;
}
