
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
    <title>Document</title>
</head>
<body>
        <div id="compte_a_rebours"><noscript>Fin de l'évènement le 5 mai 2019.</noscript></div>

        <script type="text/javascript">
        
        function compte_a_rebours()
        
        {
            var compte_a_rebours = document.getElementById("compte_a_rebours");

            var date_actuelle = new Date();
        
            var date_evenement = new Date("may 5 04:32:00 2019");
        
            var total_secondes = (date_evenement - date_actuelle) / 1000;
        
            var prefixe = "Le début du jeûne de ramadan est dans  ";
        
            if (total_secondes < 0)
        
            {
        
                prefixe = "Le début du jeûne de ramadan à commancer "; // On modifie le préfixe si la différence est négatif
        
                total_secondes = Math.abs(total_secondes); // On ne garde que la valeur absolue
        
            }
        
        
            if (total_secondes >= 0)
        
            {
        
                var jours = Math.floor(total_secondes / (60 * 60 * 24));
        
                var heures = Math.floor((total_secondes - (jours * 60 * 60 * 24)) / (60 * 60));
        
                minutes = Math.floor((total_secondes - ((jours * 60 * 60 * 24 + heures * 60 * 60))) / 60);
        
                secondes = Math.floor(total_secondes - ((jours * 60 * 60 * 24 + heures * 60 * 60 + minutes * 60)));
        
        
                var et = "et";
        
                var mot_jour = "jours," ;
        
                var mot_heure = "heures,";
        
                var mot_minute = "minutes,";
        
                var mot_seconde = "secondes";
                
        
                if (jours == 0)
        
                {
        
                    jours = '';
        
                    mot_jour = '';
        
                }
        
                else if (jours == 1)
        
                {
        
                    mot_jour = "jour,";
        
                }
        
        
                if (heures == 0)
        
                {
        
                    heures = '';
        
                    mot_heure = '';
        
                }
        
                else if (heures == 1)
        
                {
        
                    mot_heure = "heure,";
        
                }
        
        
                if (minutes == 0)
        
                {
        
                    minutes = '';
        
                    mot_minute = '';
        
                }
        
                else if (minutes == 1)
        
                {
        
                    mot_minute = "minute,";
        
                }
        
        
                if (secondes ==0)
        
                {
        
                    secondes = '';
        
                    mot_seconde = '';
        
                    et = '';
        
                }
        
                else if (secondes == 1)
        
                {
        
                    mot_seconde = "seconde";
        
                }
        
        
                if (minutes == 0 && heures == 0 && jours == 0)
        
                {
        
                    et = "";
        
                }
        
        
                compte_a_rebours.innerHTML = prefixe + jours + ' ' + mot_jour + ' ' + heures + ' ' + mot_heure + ' ' + minutes + ' ' + mot_minute + ' ' + et + ' ' + secondes + ' ' + mot_seconde;
        
            }
        
            else
        
            {
        
                compte_a_rebours.innerHTML = 'Le début du jeûne de ramadan à commancé.';
        
            }
        
        
            var actualisation = setTimeout("compte_a_rebours();", 1000);
        
        }
        
        compte_a_rebours();
        
        </script>
          <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
          <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
          <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
</body>
</html>