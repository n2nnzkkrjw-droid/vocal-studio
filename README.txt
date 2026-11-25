Vocal Studio 0.1 — prototype. Publier les fichiers sur un hébergement statique HTTPS puis ouvrir le lien dans Safari. Sur PC : python -m http.server 8000 puis http://localhost:8000. Le micro sur iPhone requiert HTTPS. Safari > Partager > Sur écran d’accueil. Brancher les écouteurs, importer une prod, enregistrer et stopper. Ajuster le décalage avant la prise si nécessaire. Les effets s'appliquent à la prochaine lecture/export, pas en monitoring direct. Sauvegarder le JSON avant de fermer. Les projets restent en mémoire sinon. Auto-Tune, calibration automatique et édition temporelle non implémentés. Pas de test matériel iPhone effectué.

0.2 : correction monophonique expérimentale hors ligne. Les corrections ne sont pas conservées dans les sauvegardes JSON ; la voix brute reste disponible. Pas de monitoring corrigé en direct. Tests iPhone requis.

0.3 : calibration acoustique indicative (3 s silence, 5 s voix), profil local et mémorisation du décalage manuel. Sauvegarde/restauration des voix corrigées en WAV 16 bits dans le JSON. Les anciennes sauvegardes restent compatibles. Pas de mesure automatique de latence ni de correction en direct. Calibration et sauvegarde à valider sur iPhone ; le profil ne modifie pas automatiquement les effets. Cache hors ligne versionné.

0.4 : retour casque expérimental EQ/compression/delay, 10 presets supplémentaires. Pas de correction live. Tests iPhone requis.

0.5 : correction directe expérimentale via AudioWorklet, uniquement dans le retour casque. Activer retour casque et correction directe avant la prise. La voix enregistrée reste brute. Réglages lus au démarrage. Le délai algorithmique et les artefacts doivent être évalués sur iPhone ; aucune garantie de qualité studio. Si le module échoue, retour casque classique.

V1 : 30 presets, position/nom/mute des pistes, sauvegarde locale IndexedDB,
paroles, équilibrage RMS et export master WAV. Les nouveaux effets sont
appliqués en lecture/export uniquement. Atténuation des aigus statique (pas
un de-esser dynamique). La sauvegarde JSON historique ne contient pas tous
les nouveaux réglages : utiliser aussi la récupération locale, qui peut être
effacée par iOS. Pas de validation Safari/iPhone ni de mesure de latence réelle.
