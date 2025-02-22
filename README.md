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
</html><!DOCTYPE html>
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
</html><!DOCTYPE html>
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
</html>body {
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
    margin: 0 10px;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

main {
    padding: 20px;
}

.products {
    display: flex;
    justify-content: space-around;
}

.product {
    background-color: #fff;
    border: 1px solid #ccc;
    padding: 10px;
    text-align: center;
}

.product img {
    max-width: 100%;
    height: auto;
}

footer {
    background-color: #111;
    color: #fff;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    bottom: 0;
    width: 100%;
}

form {
    background-color: #fff;
    border: 1px solid #ccc;
    padding: 20px;
    max-width: 400px;
    margin: 20px auto;
}

form label {
    display: block;
    margin: 10px 0 5px;
}

form input[type="text"],
form input[type="email"],
form input[type="password"] {
    width: 100%;
    padding: 10px;
    margin: 5px 0 10px;
    border: 1px solid #ccc;
}

form button {
    background-color: #111;
    color: #fff;
    padding: 10px 20px;
    border: none;
    cursor: pointer;
}

form .captcha {
    text-align: center;
    margin: 20px 0;
}<?php
session_start();

$captcha_code = '';
$characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789';
$characters_length = strlen($characters);
$captcha_length = 6;

for ($i = 0; $i < $captcha_length; $i++) {
    $captcha_code .= $characters[rand(0, $characters_length - 1)];
}

$_SESSION['captcha_code'] = $captcha_code;

$image = imagecreatetruecolor(150, 50);
$background_color = imagecolorallocate($image, 255, 255, 255);
$text_color = imagecolorallocate($image, 0, 0, 0);

imagefilledrectangle($image, 0, 0, 150, 50, $background_color);
imagettftext($image, 20, 0, 15, 30, $text_color, 'font.ttf', $captcha_code);

header('Content-Type: image/png');
imagepng($image);
imagedestroy($image);
?><?php
session_start();

if ($_SERVER['REQUEST_METHOD'] == 'POST') {
    $username = $_POST['username'];
    $password = $_POST['password'];
    $captcha = $_POST['captcha'];

    if ($captcha == $_SESSION['captcha_code']) {
        // Vérifier les informations de connexion dans la base de données
        // Si les informations sont correctes, rediriger vers une page protégée
        echo 'Connexion réussie';
    } else {
        echo 'CAPTCHA incorrect';
    }
}
?><?php
session_start();

if ($_SERVER['REQUEST_METHOD'] == 'POST') {
    $username = $_POST['username'];
    $email = $_POST['email'];
    $password = $_POST['password'];
    $confirm_password = $_POST['confirm_password'];
    $captcha = $_POST['captcha'];

    if ($captcha == $_SESSION['captcha_code']) {
        if ($password == $confirm_password) {
            // Enregistrer l'utilisateur dans la base de données
            echo 'Inscription réussie';
        } else {
            echo 'Les mots de passe ne correspondent pas';
        }
    } else {
        echo 'CAPTCHA incorrect';
    }
}
?>
