<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Érudit - Services de Mathématiques</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            transition: background-color 0.5s;
        }
        header {
            background: linear-gradient(90deg, #007bff, #00c6ff);
            color: white;
            padding: 15px 0;
            text-align: center;
            animation: fadeIn 1s;
        }
        h1 {
            margin: 0;
            font-size: 2.5em;
        }
        .description {
            font-size: 1.2em;
            color: #fff;
            margin: 10px 0;
        }
        .container {
            width: 90%;
            max-width: 800px;
            margin: auto;
            padding: 20px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            animation: slideIn 1s;
        }
        button {
            background: #007bff;
            color: white;
            border: none;
            padding: 12px 25px;
            cursor: pointer;
            border-radius: 5px;
            transition: background 0.3s, transform 0.2s;
        }
        button:hover {
            background: #0056b3;
            transform: scale(1.05);
        }
        form {
            margin-top: 20px;
        }
        label {
            display: block;
            margin: 15px 0 5px;
            font-weight: bold;
            font-size: 1.1em;
            color: #333;
        }
        input, textarea {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
            transition: border-color 0.3s;
        }
        input:focus {
            border-color: #007bff;
            outline: none;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        @keyframes slideIn {
            from { transform: translateY(-20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
    </style>
</head>
<body>

<header>
    <h1>Érudit</h1>
    <p class="description">Remplissez ce formulaire pour obtenir de l'aide en mathématiques !</p>
</header>

<div class="container">
    <h2>Nos Services</h2>
    <p>Nous offrons une aide complète en mathématiques. Remplissez le formulaire ci-dessous :</p>
    
    <form id="mathForm" action="https://formspree.io/xblybnvv" method="POST">
        <label for="name">Votre nom :</label>
        <p class="instruction">Entrez votre nom complet.</p>
        <input type="text" id="name" name="name" required>

        <label for="email">Votre e-mail :</label>
        <p class="instruction">Entrez une adresse e-mail valide.</p>
        <input type="email" id="email" name="email" required>

        <label for="phone">Votre numéro de téléphone :</label>
        <p class="instruction">Entrez votre numéro de téléphone.</p>
        <input type="tel" id="phone" name="phone" required>

        <button type="submit">Soumettre</button>
    </form>
</div>

<script>
    document.getElementById('mathForm').addEventListener('submit', function(event) {
        event.preventDefault(); // Empêche la soumission par défaut
        alert("Merci ! Votre demande a été soumise avec succès. Nous vous contacterons bientôt.\n\nVeuillez joindre le fichier PDF de l'épreuve de mathématiques que vous souhaitez corriger.");
        this.submit(); // Soumet le formulaire après l'alerte
    });
</script>

</body>
</html>
