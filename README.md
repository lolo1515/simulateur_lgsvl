# simulateur_lgsvl_5SIEC

Ce repo à pour but d'expliquer l'installation et l'utilisation du simulateur [lgsvl](https://www.lgsvlsimulator.com/docs/) adapté pour les voitures de 5SIEC.


## Procédure d'installation: 

1. Télécharger l'archive correspondante à votre système d'exploitation: 
2. Décompressez la:
3. Lancez l'éxécutable: 
4. Cliquez sur "open in browser"
<img src="images/git_start_simu.PNG" alt="alt text" width="500">

5. Une page web s'ouvre et vous arrivez diretement au menu d'import de carte. Sélectionner "ADD NEW".
 - Pour la carte de l'INSA: donner lui un nom ex:"campus INSA" et entrer le chemin que doit utiliser le simulateur pour trouver votre carte:   "VOTRE_CHEMIN_PERSONEL\unitybuild02092020\AssetBundles\Environments\environment_Campus_INSA", puis cliquer sur "Submit".
 - Pour une carte LGSVL: donner lui un nom et entrer un lien vers la carte, ex: 
   - Cube town: https://assets.lgsvlsimulator.com/085da734088f2b584075fce2d1d478b98ca076eb/environment_CubeTown 
   - San Francisco: https://assets.lgsvlsimulator.com/29a5d0d9ef094a4b3e333b28eb48254b9f9ef7a1/environment_SanFrancisco
<img src="images/add_map.PNG" alt="alt text" width="500">
6. Cliquer maintenant sur "vehicles" dans le menu sur la gauche de votre écran et procédez de la même façon pour ajouter la voiture SIEC, vous le trouverez à "VOTRE_CHEMIN_PERSONEL\unitybuild02092020\AssetBundles\Vehicles\vehicle_voiture_siec", ou encore la jaguar de LGSVL à https://assets.lgsvlsimulator.com/d49c88a93b11b047a3e21e0c7d4b2ec6964fb16d/vehicle_Jaguar2015XE
7. Editez le JSON du vehicle pour y ajouter les capteurs en cliquant sur la clé. Sélectionner "ROS" pour le type de pont, et copier le contenue du fichier config_sensor_siec dans le champs sensors. Cela va ajouter un lidar 2D et une camera à la voiture, ainsi qu'un moyen de la controler. Plus d'option pour le réglage de capteurs peuvent être explorées [ici](https://www.lgsvlsimulator.com/docs/sensor-json-options/). Une fois cela fait, cliquez sur submit.
<img src="images/add_veh.PNG" alt="alt text" width="500">
8. Vous avez terminez la procédure d'installation.

## Lancement de la simulation: 

1. Cliquez sur l'onglet simulation dans le menu à gauche de votre écran.
2. Cliquez sur "add new"
3. Dans l'onglet général, donnez un nom à la simulation.
<img src="images/simu_gene.PNG" alt="alt text" width="500">
4. Dans l'onglet map et vehicles, cocher "RUN simulation in interractive mode", sélectionner la carte et la voiture à utiliser pour la simulation. Comme notre voiture dispose d'un pont ROS, il nous faut rentrer son adresse.
 - Si vous faite tourner votre ROS sur la même machine que votre simulateur, rentrer pour adresse "localhost:9090".
 - Si votre ROS tourne sur une autre machine, rentrer pour adresse l'ip de la machine suivi du port 9090 ex: "192.168.4.65:9090"
<img src="images/simu_map.PNG" alt="alt text" width="500">

5. Ignorer les autres onglets pour le moment, comme la simulation tourne en mode interactif, ces paramètres seront modifiables en cours de simulation.
6. Cliquer sur "Submit". Votre simulation est prète.
7. Cliquer sur votre simulation une fois, puis sur l'iconne lecture. 
8. Revenez sur la fenètre du simulateur et piloter votre voiture!



