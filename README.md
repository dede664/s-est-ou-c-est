# s'est ou c'est
<html lang="fr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercice - C'est vs S'est</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
        }

        .correct {
            color: green;
        }

        .incorrect {
            color: red;
        }

        .analyse {
            color: blue;
        }
    </style>
    <script>
        function verifier() {
            let reponsesCorrectes = ["c'est", "s'est", "c'est", "s'est", "c'est", "s'est", "c'est", "s'est", "c'est", "s'est",
                                     "c'est", "s'est", "c'est", "s'est", "c'est", "s'est", "c'est", "s'est", "c'est", "s'est"];
            let score = 0;

            for (let i = 0; i < reponsesCorrectes.length; i++) {
                let userInput = document.getElementById('reponse' + (i + 1)).value.trim().toLowerCase();
                let feedback = document.getElementById('feedback' + (i + 1));
                let analyse = document.getElementById('analyse' + (i + 1));

                if (userInput === reponsesCorrectes[i]) {
                    feedback.innerText = "✔️ Correct";
                    feedback.className = "correct";
                    analyse.innerText = "";
                    score++;
                } else {
                    feedback.innerText = "❌ Incorrect";
                    feedback.className = "incorrect";
                    analyse.innerText = `La bonne réponse est "${reponsesCorrectes[i]}". Rappel : "c'est" est une contraction de "cela est", tandis que "s'est" est le pronom réfléchi "se" suivi de la forme du verbe "être" à la troisième personne du singulier.`;
                    analyse.className = "analyse";
                }
            }

            document.getElementById('score').innerText = `Votre score : ${score}/${reponsesCorrectes.length}`;
        }
    </script>
</head>

<body>
    <h2>Règle : "c'est" vs "s'est"</h2>
    <p>
        - <b>"c'est"</b> est une contraction de "cela est". Il est utilisé pour identifier ou expliquer quelque chose. Exemple : "C'est incroyable !".<br>
        - <b>"s'est"</b> est la combinaison du pronom réfléchi "se" et de la forme du verbe "être" à la troisième personne. Il est utilisé dans les phrases pronominales. Exemple : "Il s'est levé tôt ce matin".
    </p>

    <h2>Exercice - Complétez avec "c'est" ou "s'est"</h2>

    <!-- Génération des 20 questions -->
    <div id="exercices">
        <p>1. ___ incroyable de voir ça !</p>
        <input type="text" id="reponse1"> <span id="feedback1"></span><br>
        <p id="analyse1"></p><br>

        <p>2. Il ___ levé très tôt ce matin.</p>
        <input type="text" id="reponse2"> <span id="feedback2"></span><br>
        <p id="analyse2"></p><br>

        <p>3. ___ la première fois que je vois ça.</p>
        <input type="text" id="reponse3"> <span id="feedback3"></span><br>
        <p id="analyse3"></p><br>

        <p>4. Elle ___ préparée pour l'examen.</p>
        <input type="text" id="reponse4"> <span id="feedback4"></span><br>
        <p id="analyse4"></p><br>

        <p>5. ___ une belle journée aujourd'hui.</p>
        <input type="text" id="reponse5"> <span id="feedback5"></span><br>
        <p id="analyse5"></p><br>

        <p>6. Il ___ souvenu de tout ce qu'il avait appris.</p>
        <input type="text" id="reponse6"> <span id="feedback6"></span><br>
        <p id="analyse6"></p><br>

        <p>7. ___ un plaisir de vous rencontrer.</p>
        <input type="text" id="reponse7"> <span id="feedback7"></span><br>
        <p id="analyse7"></p><br>

        <p>8. Elle ___ rendue à Paris la semaine dernière.</p>
        <input type="text" id="reponse8"> <span id="feedback8"></span><br>
        <p id="analyse8"></p><br>

        <p>9. ___ bien dommage qu'il pleuve.</p>
        <input type="text" id="reponse9"> <span id="feedback9"></span><br>
        <p id="analyse9"></p><br>

        <p>10. Il ___ perdu en chemin.</p>
        <input type="text" id="reponse10"> <span id="feedback10"></span><br>
        <p id="analyse10"></p><br>

        <p>11. ___ difficile de prendre une décision.</p>
        <input type="text" id="reponse11"> <span id="feedback11"></span><br>
        <p id="analyse11"></p><br>

        <p>12. Elle ___ blessée en jouant au football.</p>
        <input type="text" id="reponse12"> <span id="feedback12"></span><br>
        <p id="analyse12"></p><br>

        <p>13. ___ tout à fait normal de se sentir ainsi.</p>
        <input type="text" id="reponse13"> <span id="feedback13"></span><br>
        <p id="analyse13"></p><br>

        <p>14. Il ___ arrêté devant la boutique.</p>
        <input type="text" id="reponse14"> <span id="feedback14"></span><br>
        <p id="analyse14"></p><br>

        <p>15. ___ incroyable de voir autant de monde.</p>
        <input type="text" id="reponse15"> <span id="feedback15"></span><br>
        <p id="analyse15"></p><br>

        <p>16. Elle ___ rendue compte de son erreur.</p>
        <input type="text" id="reponse16"> <span id="feedback16"></span><br>
        <p id="analyse16"></p><br>

        <p>17. ___ un beau cadeau qu'il a reçu.</p>
        <input type="text" id="reponse17"> <span id="feedback17"></span><br>
        <p id="analyse17"></p><br>

        <p>18. Il ___ trompé de chemin.</p>
        <input type="text" id="reponse18"> <span id="feedback18"></span><br>
        <p id="analyse18"></p><br>

        <p>19. ___ vraiment gentil de ta part.</p>
        <input type="text" id="reponse19"> <span id="feedback19"></span><br>
        <p id="analyse19"></p><br>

        <p>20. Elle ___ évanouie de fatigue.</p>
        <input type="text" id="reponse20"> <span id="feedback20"></span><br>
        <p id="analyse20"></p><br>
    </div>

    <button onclick="verifier()">Vérifier</button>
    <p id="score"></p>
</body>

</html>
