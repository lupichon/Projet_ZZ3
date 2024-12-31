Comment fonctionne OpenPilot ?
==============================

Essentiellement, OpenPilot lit les données provenant de divers capteurs (caméra, IMU, capteur d’angle du volant, récepteur GNSS, etc.), traite leurs sorties et envoie des entrées pertinentes à un grand réseau de neurones. Ce dernier transforme les sorties en commandes exploitables pour les actionneurs du véhicule. Un autre aspect essentiel est de s’assurer que les conducteurs restent attentifs lorsque le système est activé.

Pour que OpenPilot fonctionne, plusieurs bibliothèques open source ont également été développées, notamment :

- **opendbc** : bibliothèque pour interpréter le trafic sur le bus CAN.
- **panda** : interface pour les véhicules.
- **cereal** : spécification de messagerie éditeur/abonné pour les systèmes robotiques.
- **rednose** : bibliothèque de filtre de Kalman pour l’odométrie visuelle, le SLAM, etc.

OpenPilot est composé de différents services qui communiquent entre eux via un système de messagerie inter-processus à un éditeur et plusieurs abonnés (spécifié dans cereal). Ces services peuvent être classés comme suit :

- Capteurs et actionneurs 
- Réseaux neuronaux 
- Localisation et calibration 
- Contrôle 
- Système, journalisation et services divers
