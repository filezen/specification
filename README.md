
# Spécification Codex

La spécification Codex décrit une architecture d'organisation des fichiers numériques, conçue pour apporter une solution flexible et évolutive au classement de données personnelles et professionnelles. Inspirée des méthodes **PARA** (Projects, Areas, Resources, Archives) et **Johnny Decimal**, cette approche vise à offrir une structure modulaire, claire et efficace, tout en permettant une personnalisation adaptée aux besoins spécifiques de chaque utilisateur.

L'architecture repose sur des conventions strictes en matière de nommage et d'organisation, avec une numérotation hiérarchique facilitant la navigation et la recherche rapide des informations.

## Objectifs

Les objectifs principaux de cette architecture sont les suivants :

-   **Structuration claire des données** : proposer un cadre rigide mais flexible pour classer les fichiers en fonction de leur nature, permettant une distinction explicite entre projets actifs, domaines d'activité, ressources et archives.
-   **Accessibilité et évolutivité** : garantir une organisation des fichiers intuitive, extensible et adaptable à l'évolution des projets, domaines d'activité et ressources personnelles.
-   **Productivité et gestion du temps** : réduire le temps consacré à la recherche de fichiers en favorisant une structure cohérente et lisible, tant pour une utilisation personnelle que professionnelle.
-   **Compatibilité et pérennité** : assurer une utilisation fluide dans des environnements variés, notamment en ligne de commande (CLI), en garantissant l'absence de caractères problématiques (espaces, accents, etc.) et en respectant des formats de nommage stricts et compatibles à long terme.

## Inspirations

### Méthodologie PARA

La méthode **PARA**, développée par Tiago Forte, propose une organisation des fichiers en quatre grandes catégories : **Projects** (*Projets*), **Areas** (*Domaines*), **Resources** (*Ressources*), et **Archives**. Elle vise à faciliter la gestion des informations en fonction de leur rôle dans votre activité quotidienne ou à long terme.

#### Avantages

-   **Simplicité et clarté** : la méthode repose sur des catégories bien définies, faciles à comprendre et à utiliser.
-   **Focus sur l'action** : la distinction entre les projets actifs (Projects) et les domaines à long terme (Areas) permet de se concentrer sur ce qui est pertinent à court et moyen terme.
-   **Modularité** : elle s’adapte aussi bien aux contextes professionnels que personnels.

#### Inconvénients

-   **Manque de granularité** : PARA ne propose pas de sous-structures claires pour organiser les fichiers dans chaque catégorie, ce qui peut entraîner une confusion à long terme si la volumétrie augmente.
-   **Complexité à long terme** : avec l'accumulation des données, la méthode peut devenir difficile à maintenir sans des efforts réguliers de tri.

#### Référence

Pour plus d'informations sur la méthode PARA, consultez la documentation officielle.

### Méthodologie Johnny Decimal

Le système **Johnny Decimal** propose une organisation basée sur une numérotation hiérarchique. Les catégories sont divisées en groupes de 10 (numérotés de 00 à 99), et chaque sous-catégorie reçoit un numéro décimal spécifique (ex. 01.01, 01.02, etc.), facilitant la recherche rapide des fichiers.

#### Avantages

-   **Numérotation rigide et cohérente** : le système impose une hiérarchie claire qui permet de maintenir une organisation précise et facilement navigable.
-   **Facilité de recherche** : la numérotation explicite permet une localisation rapide des fichiers, même dans une structure complexe.
-   **Adaptabilité** : le système Johnny Decimal s’adapte aussi bien à des contextes numériques qu’à des environnements physiques.

#### Inconvénients

-   **Risque de rigidité** : la structure numérotée peut devenir trop rigide dans certains cas, notamment pour les projets ou domaines qui évoluent rapidement ou ne rentrent pas parfaitement dans les catégories prédéfinies.
-   **Courbe d’apprentissage** : pour ceux qui ne sont pas habitués à l’utilisation de numérotation hiérarchique, le système peut sembler contre-intuitif au départ.

#### Référence

Pour plus d'informations sur le système Johnny Decimal, consultez le [site officiel](https://johnnydecimal.com).

### Comparaisons avec Codex

Codex combine des aspects clés des méthodes **PARA** et **Johnny Decimal**, tout en ajoutant plus de flexibilité et une plus grande granularité pour s’adapter aux besoins évolutifs de l'utilisateur.

#### Similitudes

-   **Séparation en catégories fonctionnelles** : comme PARA, l'architecture propose une distinction claire entre les projets actifs, les domaines à long terme, et les ressources de référence.
-   **Numérotation hiérarchique** : à l’instar de Johnny Decimal, la numérotation est utilisée pour structurer les dossiers de manière rigide, garantissant une navigation simple et ordonnée.

#### Différences

-   **Granularité améliorée** : contrairement à PARA, l'architecture proposée permet une hiérarchisation plus fine des dossiers grâce à l’utilisation de sous-catégories numérotées. Cela permet de maintenir une organisation précise, même avec un grand nombre de fichiers.
-   **Flexibilité dans le nommage** : alors que Johnny Decimal est très strict sur la numérotation, cette architecture offre plus de souplesse, notamment avec la possibilité de nommer les projets en fonction de dates, permettant ainsi une gestion temporelle plus naturelle.
-   **Adaptation à l’incertitude des projets** : la possibilité d'utiliser des plages de dates flexibles pour les projets (par exemple `YYYYMMDD` pour une date précise, ou `YYYY` pour une période annuelle) rend cette architecture plus adaptée aux projets dont les échéances sont incertaines ou encore en cours de définition.

#### Points forts de l’architecture proposée

-   **Adaptabilité accrue** : la structure combine les avantages des deux méthodes tout en permettant une plus grande personnalisation selon les besoins de l’utilisateur.
-   **Meilleure gestion du volume** : grâce à la granularité des sous-catégories, cette architecture facilite la gestion d’un grand volume de données sans perdre en clarté ou en facilité de navigation.
-   **Compatibilité technique** : la rigueur dans le nommage des fichiers (absence d’accents, d'espaces) et l’utilisation de dates permettent une compatibilité totale avec les systèmes en ligne de commande (CLI) et garantissent la pérennité des fichiers à long terme.

## Conventions de nommage

Afin de garantir une uniformité et une cohérence dans l'organisation des fichiers, les conventions de nommage suivantes sont appliquées :

### 1. Numérotation

-   **Catégories principales** : les catégories racines sont numérotées par centaines (100, 200, 300, etc.) pour faciliter la hiérarchisation et la recherche.
-   **Sous-catégories** : chaque sous-dossier suit une numérotation décimale basée sur la structure Johnny Decimal (ex. 201, 202, etc.), permettant une extension de la structure tout en garantissant une organisation lisible et ordonnée.

### 2. Dates

Pour les projets et fichiers liés à des événements ou périodes spécifiques, la datation est essentielle pour faciliter la gestion temporelle. Le format de datation utilisé est flexible afin de s’adapter aux différentes précisions temporelles d’un projet ou d’un document :

-   **Date précise** : `YYYYMMDD` (ex. `20241026` pour une date précise).
-   **Période définie** : `YYYYMMDD-YYYYMMDD` (ex. `20241227-20241230` pour un projet s’étendant du 27 décembre 2024 au 30 décembre 2024).
-   **Période large** : utilisé lorsque la date précise n'est pas encore définie ou qu'une estimation globale est suffisante :
    -   **Mois** : `YYYYMM` (ex. `202410` pour indiquer une période en octobre 2024).
    -   **Année** : `YYYY` (ex. `2024` pour indiquer l'ensemble d'une année).

Les dates jouent un rôle crucial dans le tri automatique des fichiers et des dossiers, facilitant ainsi la gestion chronologique des projets.

### 3. Noms explicites

Chaque dossier ou fichier doit utiliser un nom explicite qui décrit clairement son contenu ou sa finalité. L’utilisation de noms clairs améliore non seulement la navigation dans les dossiers, mais facilite également la recherche manuelle ou automatisée.

**Exemple :**
-   `20241026_tickets.pdf` pour un fichier de tickets daté du 26 octobre 2024.
-   `20241227-20241230_disneyland/` pour un dossier contenant des fichiers liés à un voyage à Disneyland durant cette période.

### 4. Compatibilité avec la CLI

Afin d'assurer une compatibilité totale avec les systèmes de gestion de fichiers et d'éviter les problèmes d'encodage, les règles suivantes sont à respecter :

-   **Pas d'espaces ni d'accents** : utilisez le tiret bas `_` à la place des espaces.
-   **Utilisation de caractères alphanumériques** uniquement pour maximiser la portabilité entre différents systèmes.

## Structure générale

L'architecture de base est divisée en cinq catégories principales, chacune numérotée pour garantir une hiérarchisation logique et cohérente. Les catégories sont définies comme suit :

```
.
|-- 000_inbox/
|-- 100_projets/
|-- 200_domaines/
|-- 300_ressources/
|-- 400_archives/
```

Chaque catégorie peut contenir des sous-dossiers numérotés et organisés de manière hiérarchique selon les principes de la méthode **Johnny Decimal**. Cette structure inclut des fichiers liés à des projets, domaines d'activité, ou des ressources spécifiques.

## Détails des catégories

### 000_inbox

Le dossier `000_inbox` est une boîte de réception temporaire, destinée à accueillir les fichiers en attente de tri. Il est recommandé d'organiser régulièrement les fichiers de cette section vers les dossiers appropriés afin de maintenir une structure ordonnée.

### 100_projets

Le dossier `100_projets` contient tous les projets actifs ou passés. Les projets sont classés par dates (au format `YYYYMMDD` ou `YYYYMMDD-YYYYMMDD`), avec la possibilité d’utiliser des périodes plus larges (`YYYYMM`, `YYYY`) pour les projets dont la date de fin est encore incertaine.

**Exemple :**
```
|-- 100_projets/
|   |-- 20241026_walibi/
|   |   `-- 20241026_tickets.pdf
|   `-- 20241227-20241230_disneyland/
|       |-- 20241227_ouigo_tickets.pdf
|       `-- 20241230_ouigo_tickets.pdf
```

Ce dossier se destine principalement à des projets avec une temporalité définie. Lorsqu'un projet est terminé ou inactif, il doit être déplacé dans le dossier `400_archives`.

### 200_domaines

Le dossier `200_domaines` regroupe des zones d'activité ou d'intérêt à long terme qui ne sont pas liées à des dates de fin précises. Ces domaines incluent des catégories comme les finances, la santé, ou les aspects professionnels.

**Exemple :**
```
|-- 200_domaines/
|   |-- 201_banques/
|   |   `-- 201.01_axa/
|   |       |-- 2023/
|   |       |   `-- 202305_releve_bancaire.pdf
|   |       `-- 2024/
|   |           |-- 20240325_resiliation_livret.pdf
|   |           |-- 202410_releve_bancaire.pdf
|   |           `-- 202411_releve_bancaire.pdf
|   `-- 202_professionnel/
|       |-- 202.01_contrats/
|       |-- 202.02_bulletins_de_salaire/
```
Les sous-catégories sont numérotées pour assurer une organisation claire et rigoureuse des différents documents relatifs à ces domaines.

### 300_ressources

Le dossier `300_ressources` contient des fichiers de référence ou des éléments que l'utilisateur consulte régulièrement, tels que des fichiers multimédias (musique, ebooks, etc.) ou des documents de référence.

**Exemple :**
```
|-- 300_ressources/
|   |-- 301_musique/
|   |   |-- Iron Maiden/
|   |   |-- Placebo/
|   |   `-- The Police/
|   `-- 302_ebooks/
```

### 400_archives

Les fichiers ou projets qui ne sont plus actifs sont déplacés dans le dossier `400_archives`. Cela permet de conserver une trace de l'historique tout en évitant d'encombrer les dossiers actifs.

**Exemple :**
```
|-- 400_archives/
|   `-- 401_banques/
|       |-- 401.01_societe_generale/
|       `-- 401.02_bnp_paribas/
```

## Mise en place et conseils

### Mise en place initiale

1.  **Auditez vos fichiers actuels** : réalisez une analyse complète des fichiers et dossiers existants. Identifiez les catégories pertinentes (projets, domaines, ressources) et les documents à archiver.
    
2.  **Créez les catégories racines** : créez les cinq dossiers racines : `000_inbox`, `100_projets`, `200_domaines`, `300_ressources`, et `400_archives`. Ces catégories sont les fondations de votre nouvelle organisation.
    
3.  **Adoptez une structure progressive** : inutile de déplacer tous vos fichiers en une seule fois. Commencez par les documents les plus récents et importants, et répartissez-les progressivement dans la nouvelle structure. Le dossier `000_inbox` peut accueillir temporairement les fichiers que vous n'avez pas encore triés.
    
4.  **Utilisez les conventions de nommage** : pour les fichiers que vous ajoutez, respectez les conventions de nommage pour garantir la cohérence et faciliter la recherche.
    

### Conseils

1.  **Organisez régulièrement l'inbox** : le dossier `000_inbox` sert de réceptacle temporaire. Il est important de vider ce dossier régulièrement en triant les fichiers dans les catégories appropriées.
    
2.  **Revue périodique des projets** : planifiez des revues périodiques (par exemple, tous les trimestres) pour déplacer les projets terminés dans le dossier `400_archives`. Cela permet de maintenir la catégorie `100_projets` dédiée uniquement aux activités en cours.
    
3.  **Archiver les documents obsolètes** : lorsque des fichiers dans les dossiers `200_domaines` ou `300_ressources` ne sont plus d’actualité, déplacez-les dans `400_archives` pour éviter l’encombrement.
    
4.  **Vérifiez la cohérence des sous-catégories** : il peut être utile de réévaluer périodiquement les sous-catégories afin de vérifier qu’elles reflètent bien les besoins actuels. Si une sous-catégorie devient trop large ou trop petite, n’hésitez pas à la réorganiser.
    
5.  **Évitez l'accumulation** : la règle d’or est de ne pas laisser s'accumuler les fichiers dans des catégories mal définies. Pour éviter cela, adoptez une routine de tri hebdomadaire ou mensuelle, notamment dans le dossier `000_inbox`. Cela vous permettra de garder une structure propre et d’éviter l'encombrement inutile.

6.  **Simplifiez les révisions** : utilisez des outils de recherche ou d'indexation lorsque le volume des fichiers devient trop important, tout en vous assurant que les conventions de nommage sont strictement respectées. Cela facilitera la recherche automatisée.
    
7.  **Mettre à jour régulièrement** : à mesure que de nouveaux projets ou domaines d’activité se développent, adaptez la structure en créant de nouvelles sous-catégories numérotées. Par exemple, si vous ajoutez un nouveau domaine, assurez-vous de suivre la logique de numérotation pour conserver la cohérence.

---

 <p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/">La <a property="dct:title" rel="cc:attributionURL" href="https://github.com/fmatsos/codex-specification">Spécification Codex</a> par <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://franck.matsos.dev/">Franck Matsos</a> est publiée sous licence <a href="https://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Creative Commons Attribution-ShareAlike 4.0 International <img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" alt=""></a></p> 
