# 🎮 Projet IF36 – Analyse des temps de complétion des jeux vidéo

## 🧭 Introduction

### 🗃️ Données

**📄 Source**

Notre objectif principal est d'analyser le temps de complétion de différents jeus vidéos afin de voir par quoi il est impacté. Nous avons donc sélectionné un jeu de données appelé Video Games Playtime, que nous avons trouvé sur [Kaggle](https://www.kaggle.com/datasets/baraazaid/how-long-to-beat-video-games). ll est basé sur les données du site [How Long To Beat](https://howlongtobeat.com), qui recense des données sur le temps nécessaire pour terminer un jeu vidéo, selon différents styles de jeu. Ce jeu de données a été mis à jour pour la dernière fois en 2023. Le fichier est au format jsonlines et contient 60 410 entrées.


---


### 🧠 Plan d’analyse

Avant toute chose, nous avons réfléchi aux questions que nous souhaitons poser à nos données, aux croisements de variables intéressants, et aux méthodes de visualisation potentielles.

**🎯 Objectifs & interrogations**

- Quels sont les facteurs qui influencent le temps de complétion d’un jeu vidéo ?
- Sur quelles parties les joueurs passent-ils le plus de temps (main story, extras, completionist) ?
- Les temps de complétion varient-ils selon la plateforme ?
- Combien de temps les joueurs passent-ils à jouer en moyenne ?
- Y a-t-il une corrélation entre le temps de jeu et la note du jeu ? la date de sortie ? les genres ?
- Quels sont les jeux les plus longs et les plus courts ? Appartiennent-ils à certains genres ?
- Les modes multijoueurs (coopératif ou compétitif) influencent-ils la durée de jeu ?

---

**🔄 Variables à comparer**

D'une façon générale nous voulons comparer les temps moyens de complétion :
- Pour chaque mode de complétion (`Completionist`, `Speedrun`, `Multi-Player`...)
- Par plateforme (si disponible)
- Par genre(s) des jeux
- Par année (ou mois) de publication
- Par note (`Review_score`)
- Par extrêmes des temps de jeu : valeurs minimales et maximales

---

**🧰 Méthodes envisagées**

Selon les variables analysées, nous envisageons d’utiliser :
- Des **histogrammes** pour visualiser les distributions de temps
- Des **boîtes à moustaches** (boxplots) pour comparer les genres ou années
- Des **courbes temporelles** pour étudier l’évolution dans le temps
- **D'autres vizualisations adéquates** pour explorer les corrélations (temps vs note, par exemple)

---

**⚠️ Limites anticipées**

- Certaines durées sont enregistrées en format texte (`"12h 30m"`) et devront être transformées en **valeurs numériques** (minutes ou heures).
- Les colonnes comme `Genres` contiennent plusieurs genres séparés par des délimiteurs ; (`"Third-Person, Action, Adventure, Role-Playing"` ==> phase de **nettoyage**).
- Faire attention aux données qui peuvent être **manquantes** ou **aberrantes**.


---

