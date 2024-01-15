# Windows 10/11 post installation checklist

All config that can't be automated and has to be manually done. There's too much, I can't remember all this shit.

These are the settings that I have to change from the default of the Enterprise version. It's in French parce que c'est ça que j'utilise et traduire c'est chiant.

- shutup/winaero
    - désactiver cortana
    - désactiver recherche web
    - désactiver lockscreen
- supprimer onedrive
- fonctionnalités inutiles
    - hello
    - ie
    - media
    -enregistreur d'actions
- sécu
    fonctions
    désac powershuell 2
désac chiffrement auto
clavier virtuel
    son
    correction
defender
    isolation du noyau
    option application guard
enable long path
désac assistance à distance
sons désactiver
alim : désac démarrage rapide
souris : dsac accélération
gpu : profil couleur
    full rgb sur écran pc
    limité/adapté pour tv
installer hevc
    ms-windows-store://pdp/?ProductId=9n4wgh0z6vhq
    https://www.reddit.com/r/Windows10/comments/j58y6f/no_longer_free_windows_10_hevc_video_extensions/
changement de clavier : mettre par défaut pour tout l'ordi
    https://www.reddit.com/r/Windows11/comments/r4t4c6/comment/hmj1hqk/?context=3
désac nettoyeryur auto

dns custom

- Explorateur de fichiers > Options
    - Général
        -  **Ouvrir l'Explorateur de fichiers dans : Ce PC**
        -  Confidentialité
            - **Afficher les fichiers récemment utilisés : NON**
            - **Afficher les dossiers fréquemment utilisés : NON**
            - **Afficher les fichiers de `Office.com` : NON**
    - Affichage
        - **Fichiers et dossiers cachés : Afficher les fichiers, dossiers et lecteurs cachés**
        - **Masquer les extensions des fichiers dont le type est connu : NON**
        - **Ouvrir les fenêtres des dossiers dans un processus différent : OUI**

- Paramètres
    - Accessibilité
        - Touches rémanentes > **Raccourci clavier pour les touches rémanentes : DÉSACTIVÉ**
        - Touches filtres > **Raccourci clavier pour les touches filtres : DÉSACTIVÉ**
    - Réseau et Internet
        - Wi-Fi
            - Propriétés du matériel > **Attribution du serveur DNS : MANUEL ; voir @DNS**
            - **Adresses matérielles aléatoires : ACTIVÉ**
        - Ethernet
            - **Type du profil de réseau : RÉSEAU PRIVÉ**
            - **Attribution du serveur DNS : MANUEL ; voir @DNS**
        - Point d'accès sans fil mobile > Propriétés > **Propriétés du réseau : CUSTOM**
    - Personnalisation > Démarrer
        - **Disposition : AUTRES ÉLÉMENTS ÉPINGLÉS**
        - **Afficher des recommandations pour les conseils, les raccourcis, les nouvelles applications, etc. : DÉSACTIVÉ**
        - **Dossiers > PARAMÈTRES, EXPLORATEUR DE FICHIERS, RÉSEAU, DOSSIER PERSIONNEL : ACTIVÉ**
    - Heure et langue > Saisie
        - Clavier tactile > **Émettre des sons en cours de frappe : NON** #annoyance
        - **Suggestions de texte multilingue : ACTIVÉ**
        - **Corriger automatiquement les fautes d'orthographe : DÉSACTIVÉ** #annoyance
        - **Informations sur la saisie : DÉSACTIVÉ**
    - Accessibilité > Effets visuels
        - **Toujours afficher les barres de défilement : ACTIVÉ**
        - **Effets de transparence : DÉSACTIVÉ**
        - **Effets d'animation : DÉSACTIVÉ**
    - Windows Update > Options avancées > **Obtenir des mises à jour pour autres produtis Microsoft : OUI** 

@DNS

Gestionnaire des tâches > Applications de démarrage > **Microsoft Edge : DÉSACTIVÉ**

Edge : désactiver startup
Paramètres > Système
    - **Démarrage rapide : DÉSACTIVÉ**
    - **Continuer à exécuter les extensions et les applications en arrière-plan lorsque Microsoft Edge est fermé : DÉSACTIVÉ**
