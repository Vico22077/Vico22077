<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VHL.TRADE.com - Accueil</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Bienvenue sur VHL.TRADE.com</h1>
        <nav>
            <ul>
                <li><a href="index.html">Accueil</a></li>
                <li><a href="login.html">Connexion</a></li>
                <li><a href="register.html">Inscription</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <h2>Nos Articles de Luxe</h2>
        <section class="products">
            <article class="product">
                <img src="image1.jpg" alt="Produit 1">
                <h3>Produit 1</h3>
                <p>Description du produit 1</p>
                <button>Ajouter au panier</button>
            </article>
            <article class="product">
                <img src="image2.jpg" alt="Produit 2">
                <h3>Produit 2</h3>
                <p>Description du produit 2</p>
                <button>Ajouter au panier</button>
            </article>
        </section>
    </main>
    <footer>
        <p>&copy; 2025 VHL.TRADE.com. Tous droits réservés.</p>
    </footer>
</body>
</html>

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Connexion - VHL.TRADE.com</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Connexion</h1>
        <nav>
            <ul>
                <li><a href="index.html">Accueil</a></li>
                <li><a href="login.html">Connexion</a></li>
                <li><a href="register.html">Inscription</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <form action="authenticate.html" method="post">
            <label for="username">Nom d'utilisateur:</label>
            <input type="text" id="username" name="username" required>
            <label for="password">Mot de passe:</label>
            <input type="password" id="password" name="password" required>
            <div class="captcha">
                <label for="captcha">Entrez le texte de l'image:</label>
                <img src="captcha_image.php" alt="CAPTCHA">
                <input type="text" id="captcha" name="captcha" required>
            </div>
            <button type="submit">Connexion</button>
        </form>
    </main>
    <footer>
        <p>&copy; 2025 VHL.TRADE.com. Tous droits réservés.</p>
    </footer>
</body>
</html>

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inscription - VHL.TRADE.com</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Inscription</h1>
        <nav>
            <ul>
                <li><a href="index.html">Accueil</a></li>
                <li><a href="login.html">Connexion</a></li>
                <li><a href="register.html">Inscription</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <form action="register_user.html" method="post">
            <label for="username">Nom d'utilisateur:</label>
            <input type="text" id="username" name="username" required>
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
            <label for="password">Mot de passe:</label>
            <input type="password" id="password" name="password" required>
            <label for="confirm_password">Confirmez le mot de passe:</label>
            <input type="password" id="confirm_password" name="confirm_password" required>
            <div class="captcha">
                <label for="captcha">Entrez le texte de l'image:</label>
                <img src="captcha_image.php" alt="CAPTCHA">
                <input type="text" id="captcha" name="captcha" required>
            </div>
            <button type="submit">Inscription</button>
        </form>
    </main>
    <footer>
        <p>&copy; 2025 VHL.TRADE.com. Tous droits réservés.</p>
    </footer>
</body>
</html>

<style>
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    color: #333;
    margin: 0;
    padding: 0;
}

header {
    background-color: #111;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}

header h1 {
    margin: 0;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin 
