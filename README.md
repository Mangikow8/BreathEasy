<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8"> 
    <title>BreathEasy</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #E8D5CC;
            text-align: center;
        }

        /* Loader */
        .loader {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #E8D5CC;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
        }

        .loader img {
            width: 120px;
            animation: blink 0.5s infinite alternate;
        }

        @keyframes blink {
            0% { opacity: 1; }
            100% { opacity: 0.3; }
        }

        /* Contenu caché au début */
        .content {
            display: none;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            width: 100%;
            height: 40vh; /* Hauteur plus courte */
            background-image: url('Accueil.jpg'); /* Remplace par ton image */
            background-size: cover; /* L'image couvre toute la largeur */
            background-position: center;
        }

        h1 {
            font-size: 2rem;
            color: white;
            margin-bottom: 30px;
        }

        .button {
            background-color: #BDA18A;
            color: white;
            padding: 10px 20px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            border-radius: 5px;
            margin-top: 20px;
            transition: background-color 0.3s;
        }

        .button:hover {
            background-color: #346f91;
        }
    </style>
</head>
<body>

    <!-- Animation de chargement -->
    <div class="loader">
        <img src="BreathEasy.png" alt="Chargement...">
    </div>

    <!-- Contenu principal -->
    <div class="content">
        <h1>Bienvenue sur le site de BreathEasy</h1>
        <a href="page2.html" class="button">Accéder à la page de contrôle</a>
    </div>

    <script>
        window.onload = function() {
            setTimeout(() => {
                document.querySelector('.loader').style.display = 'none';
                document.querySelector('.content').style.display = 'flex';
            }, 2700); // Temps de chargement avant d'afficher la page
        };
    </script>

</body>
</html>
