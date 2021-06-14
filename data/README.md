# Impact de la pollution de l'air sur la mortalité, Rhône, 2007-2019

## Data

### Données

#### Pollution

- Polluants étudiés:
  - NO
  - NO2
  - O3
  - PM2.5
  - PM10

- Stations pertinentes (Dans le département du Rhône - 69):
  - FR20002,FR20003,FR20004,FR20008,FR20013,FR20016,FR20017,FR20019,FR20020,FR20026,FR20029,FR20030,FR20031,FR20033,FR20034,FR20036,FR20037,FR20038,FR20045,FR20046,FR20048,FR20049,FR20055,FR20060,FR20061,FR20062,FR20063,FR20064,FR20065,FR20066,FR20067,FR20069,FR20070,FR20071,FR20077,FR20204


- *Source* : [***ATMO***](https://api.atmo-aura.fr/documentation)

#### Démographie

- *Source* : [***INSEE***](https://www.insee.fr/fr/statistiques/fichier/4989724/ensemble.pdf)


### Résultat

Pour chaque polluant, construction d'un indicateur journalier de pollution comme suit:

$\sum_{i=1}^n mesure\_station_i * population\_station_i \; / \; population\_totale$


```
├── demographie ----------------- #pollution de la commune, par station 
├── mortalite ------------------- #données de mortalité
│   ├── journaliers_2018-2019 ---    #journalières
│   │   ├── cleaned -------------       #nettoyé
│   │   ├── init ----------------       #fichier original
│   │   └── quotidienne ---------       #agrégation journalière
│   └── mensuels_2007-2019 ------    #mensuelles
├── pollution ------------------- #données de pollution 
│   ├── mesures -----------------    #mesures par polluant
│   │   ├── cleaned -------------       #nettoyé
│   │   ├── indicateur ----------       #indicateur construit
│   │   ├── init ----------------       #fichier original
│   │   ├── reshaped ------------       #redimensionné
│   │   └── stats ---------------       #statistiques
│   └── stations ---------------- #liste des stations pertinentes
└── sorties --------------------- #sorties python

```



---------------------------

### À propos

- Auteurs:
  - [Hana Sebia](mailto:hana.sebia@etu.univ-lyon1.fr)
  - [Tarik Boumaza](mailto:tarik.boumaza@etu.univ-lyon1.fr)
- Juin 2021
- Réalisé dans le cadre du Projet d'Orientation de Master, [Université Lyon 1](https://www.univ-lyon1.fr/)