**Institut Universitaire des Sciences**

**Faculté des Sciences et Technologies**

**Projet dans le cadre du cours de Réseaux 2**

**Simulation d\'un Réseau IoT avec Cisco Packet Tracer**

**Préparé par Wendy COLAS**

**A l'attention de Monsieur Ismaël SAINT AMOUR**

**Mai 2025**

I.  **Introduction**

Avec l'évolution rapide des technologies, l'internet des objets (IoT)
joue un rôle essentiel dans la connectivité et l'automatisation des
systèmes. Les appareils connectés échangent des données en temps réel,
facilitant ainsi de nombreuses applications, que ce soit dans la
domotique, l'industrie ou la gestion des infrastructures intelligentes.

Ce projet vise à simuler un réseau IoT en utilisant Cisco Packet Tracer,
un outil puissant permettant de créer et analyser des architectures
réseau. Grâce à cette simulation, nous pouvons observer le
fonctionnement des périphériques IoT, étudier la communication entre eux
et comprendre les protocoles qui assurent leur interconnexion.

Dans ce rapport, nous allons détailler les étapes de conception du
réseau, les dispositifs utilisés ainsi que les résultats obtenus.
L'objectif est de mieux comprendre le déploiement d'un réseau IoT et ses
implications pratiques.

Dans un contexte de modernisation des infrastructures hôtelières,
l\'intégration de technologies intelligentes devient un levier essentiel
pour garantir sécurité, confort et efficacité. Le projet intitulé
« Simulation d\'un réseau IoT dans Cisco Packet Tracer » s\'inscrit dans
cette dynamique en proposant la configuration d\'un réseau connecté
adapté à un environnement hôtelier. L\'architecture retenue repose sur
une structure simplifiée composée de trois pôles : une chambre client,
une chambre pour l\'agent de sécurité et une infrastructure centrale.
Grâce à une série de dispositifs IoT (capteurs de fumée, détecteurs de
mouvement, caméras, alarmes, etc.), les différentes zones communiquent
entre elles. Ainsi, en cas d\'incident dans la chambre du client, comme
la détection de fumée, une alerte est immédiatement transmise à l\'agent
de sécurité via le réseau, permettant une intervention rapide. Ce projet
illustre comment les technologies IoT peuvent être exploitées pour
renforcer la surveillance et automatiser les réponses aux situations
critiques dans un cadre hôtelier.

I.  **Conception du réseau**

![](D:/projet2/image/image (1).png){width="6.298611111111111in"
height="3.5388888888888888in"}

Ce réseau IoT est structuré de manière à permettre une connectivité
fluide entre les dispositifs des deux chambres tout en assurant la
sécurité et le contrôle via des équipements dédiés. Chaque section a un
rôle bien défini, assurant une gestion efficace du réseau.

A.  **La partie physique**

```{=html}
<!-- -->
```
1)  **La chambre de l'agent de sécurité**

Cette section est dédiée au contrôle et à la surveillance du réseau.
Elle contient plusieurs dispositifs essentiels :

-   **SMARTPHONE-PT (smartphone0) :** il permet la gestion mobile du
    réseau et la communication avec les dispositifs IoT.

-   **Sirène 1 et 2 :** déclenchent une alarme en cas d'intrusion ou
    d'urgence.

-   **AccessPoint-PT (Access Point0) :** Assure la connexion WI-FI aux
    appareils de cette chambre.

-   **Server-PT (Server-dhcp1) :** fournit des adresses IP automatique
    aux appareils via le protocole DHCP.

2)  **La chambre du client**

Cette partie du réseau est axée sur la connectivité domestique et la
surveillance. Elle contient :

-   **SMARTPHONE-PT (Smartphone1) :** Il permet de surveiller et
    contrôler les équipements IoT.

-   **Camera :** sert à la surveillance vidéo en temps réel.

-   **Fenêtre :** capteur qui détecte l'ouverture ou la fermeture de la
    fenêtre.

-   **Détecteur de mouvement :** analyse les mouvements pour identifier
    une présence suspecte.

-   **Porte :** capteur qui surveille l'état d'ouverture ou de fermeture
    de la porte.

-   **Lampe :** permet de gérer l'éclairage intelligent.

-   **AccessPoint-PT (Access Point1) :** assure la connexion WI-FI aux
    appareils du client.

-   **Server-PT (Server-iot) :** gère les fonctionnalités IoT et stocke
    les données liées aux dispositifs connectes.

-   **Server-PT (Server-dhcp) :** fournit des adresses IP automatique
    aux appareils via le protocole DHCP.

-   **Détecteur de fumée :** permet de détecter la présence de la fumée
    donc éventuellement de feu dans la chambre du client.

-   **Extincteur de feu :** se déclenche quand la présence de la fumée
    est détectée.

3)  **L'infrastructure réseau**

Cette section joue un rôle de passerelle centrale et assure la
communication entre les deux chambres. Elle contient :

-   **Switch-PT (Switch0 et Switch1):** ces deux switchs appartiennent à
    l'infrastructure centrale et relient tous les équipements réseau,
    assurant le routage des données entre les différentes sections du
    réseau.

-   **2901 (Router0 et Router1) :** les deux routeurs jouent un rôle
    fondamental dans la gestion du trafic réseau.

```{=html}
<!-- -->
```
-   **Router0 :** assure la communication entre la chambre de l'agent de
    sécurité et l'infrastructure réseau, permettant le transfert
    sécurisé des données IoT.

-   **Router1 :** relie la chambre du client à l'infrastructure réseau
    et gère les connexions entre les appareils IoT et les services
    réseau.

Les routeurs optimisent les flux de communications et appliquent les
politiques réseau (comme la gestion des adresses IP ou le filtrage du
trafic).

B.  **La connectivité**

```{=html}
<!-- -->
```
1)  **Câble Ethernet (Copper Straight-Through)**

Ces câbles sont utilisés pour connecter les serveurs aux switchs, les
access points aux switchs et les switchs aux routeurs. Je les ai
utilisés car ils assurent une communication stable et rapide.

2)  **Câble Serial**

Ils sont utilisés pour connecter les routeurs entre eux. Je les ai
utilisées car ils permettent une connexion plus réaliste des réseaux
étendus. Pour cela, j'ai dû ajouter des ports adaptés au câble serial
sur chaque routeur.

![](D:/projet2/image/image (2).png){width="6.298611111111111in"
height="6.490972222222222in"}![](D:/projet2/image/image (3).png){width="6.298611111111111in"
height="6.417361111111111in"}

3)  **Connection WI-FI**

La connexion WI-FI est utilisé pour les smartphones et les dispositifs
IoT. Tout d'abord, elle permet plus de mobilité aux appareils, surtout
aux smartphones qui doivent gérer les équipements à distance. Mais
également, les objets IoT sont souvent conçues pour fonctionner en
WI-FI.

Les Access Point servent de relais pour assurer une communication fluide
entre les appareils et l'infrastructure réseau.

II. **La configuration du réseau**

```{=html}
<!-- -->
```
A.  ![](D:/projet2/image/image (4).png){width="6.298611111111111in"
    height="4.1875in"}**Configuration des serveur DHCP**

![](D:/projet2/image/image (5).png){width="6.298611111111111in"
height="3.0416666666666665in"}

![](D:/projet2/image/image (6).png){width="6.298611111111111in" height="3.25in"}

![](D:/projet2/image/image (7).png){width="6.298611111111111in" height="3.125in"}

Pour configurer le protocole DHCP, on commence par attribuer une adresse
IP statique à chacun des server-dhcp. Puis, on se rend dans l'onglets
services, ensuite on choisit DHCP pour activer le protocole. Par la
suite, on ajoute l'adresse de la passerelle et les spécifications
concernant la plage d'adresse à utiliser et on appuie sur « save » pour
enregistrer la configuration. On fait la même chose pour chacun des
serveur DHCP.

B.  **Configuration des Access Point et des objets IoT**

![](D:/projet2/image/image (8).png){width="6.298611111111111in"
height="3.638888888888889in"}![](D:/projet2/image/image (9).png){width="6.298611111111111in"
height="3.7375in"}

![](D:/projet2/image/image (10).png){width="6.298611111111111in"
height="4.03125in"}![](D:/projet2/image/image (11).png){width="6.298611111111111in"
height="4.269444444444445in"}![](D:/projet2/image/image (12).png){width="6.298611111111111in"
height="3.9791666666666665in"}![](D:/projet2/image/image (13).png){width="6.298611111111111in"
height="4.363194444444445in"}![](D:/projet2/image/image (14).png){width="6.298611111111111in"
height="3.875in"}![](D:/projet2/image/image (15).png){width="6.298611111111111in"
height="4.3805555555555555in"}![](D:/projet2/image/image (16).png){width="6.298611111111111in"
height="4.125in"}![](D:/projet2/image/image (17).png){width="6.298611111111111in"
height="4.184722222222222in"}![](D:/projet2/image/image (18).png){width="6.298611111111111in"
height="6.5875in"}

Dans cette partie, il est question de configurer les Access Point en se
rendant dans l'onglet config, puis en cliquant sur port 1 afin de
modifier le SSID. Par la suite, on se rend sur chaque objet IoT dans
l'onglet config, puis on clique sur « Wireless 0 » et on ajoute le SSID
de l'Access Point dans lequel on souhaite connecter notre objet. Pour
les smartphones, après cette configuration, on se rend dans l'onglet
Desktop, puis sur IP configuration pour constater l'attribution
automatique de l'adresse IP par le protocole DHCP.

C.  **Configuration des routeurs**

![](D:/projet2/image/image (19).png){width="6.298611111111111in"
height="4.177083333333333in"}

![](D:/projet2/image/image (20).png){width="6.298611111111111in"
height="4.697916666666667in"}

![](D:/projet2/image/image (21).png){width="6.298611111111111in"
height="3.8333333333333335in"}![](D:/projet2/image/image (22).png){width="6.298611111111111in"
height="4.636111111111111in"}![](D:/projet2/image/image (23).png){width="6.298611111111111in"
height="3.9583333333333335in"}![](D:/projet2/image/image (24).png){width="6.298611111111111in"
height="4.280555555555556in"}![](D:/projet2/image/image (25).png){width="6.298611111111111in"
height="6.125in"}

Dans cette partie, j'ai procédé à la configuration de base des routeurs
en configurant les interfaces GigabitEternet0/0 et serial0/0/0 sur
chacun des routeurs. Puis par la suite, j'ai activé un routage dynamique
à l'aide de la commande « router ospf 1 » sur les deux routeurs. Avec la
commande « show ip route » je me suis assuré que le routage fonctionne
sur chacun des routeurs. Et pour finir, sur le smarphone0 qui se situe
dans la chambre de l'agent de sécurité, j'ai fait « ping 192.168.1.1 »,
qui est l'adresse de passerelle pour la chambre du client, pour voir si
les deux chambres communiquent entre elles et ce fut un succès.

D.  **Configuration du protocole IoT**

![](D:/projet2/image/image (26).png){width="6.298611111111111in"
height="4.083333333333333in"}![](D:/projet2/image/image (27).png){width="6.298611111111111in"
height="4.58125in"}![](D:/projet2/image/image (28).png){width="6.298611111111111in"
height="3.4479166666666665in"}![](D:/projet2/image/image (29).png){width="6.298611111111111in"
height="4.345138888888889in"}![](D:/projet2/image/image (30).png){width="6.298611111111111in"
height="3.8333333333333335in"}![](D:/projet2/image/image (31).png){width="6.298611111111111in"
height="4.59375in"}![](D:/projet2/image/image (32).png){width="6.298611111111111in"
height="3.3645833333333335in"}![](D:/projet2/image/image (33).png){width="6.298611111111111in"
height="4.2in"}

Pour configurer le protocole IoT, il faut tout d'abord attribué une
adresse IP statique au serveur IoT, ensuite on se rend sur l'onglet
services, puis on clique sur IoT pour l'activer. Après cela, on se rend
sur chacun des smartphones dans l'onglet desktop, puis dans Web browser
et on met l'adresse du serveur IoT soit 192.168.1.5 dans notre cas. Par
la suite, on crée des comptes pour l'agent de sécurité (Username :
colas, password : wendy) et pour le client (Username : wendy, password :
colas).

En nous connectant avec nos comptes respectifs, on se rend compte qu'il
n'y a aucun objet connecté pour l'instant.

E.  **Connexion des différents objets IoT**

![](D:/projet2/image/image (34).png){width="6.298611111111111in"
height="3.4895833333333335in"}

![](D:/projet2/image/image (35).png){width="6.298611111111111in"
height="4.145833333333333in"}![](D:/projet2/image/image (36).png){width="6.298611111111111in"
height="4.302777777777778in"}![](D:/projet2/image/image (37).png){width="6.298611111111111in"
height="3.1354166666666665in"}![](D:/projet2/image/image (38).png){width="6.298611111111111in"
height="3.6041666666666665in"}![](D:/projet2/image/image (39).png){width="6.298611111111111in"
height="4.15625in"}![](D:/projet2/image/image (40).png){width="6.298611111111111in"
height="4.477083333333334in"}![](D:/projet2/image/image (41).png){width="6.298611111111111in"
height="4.0625in"}![](D:/projet2/image/image (42).png){width="6.298611111111111in"
height="4.8277777777777775in"}![](D:/projet2/image/image (43).png){width="6.298611111111111in"
height="3.3958333333333335in"}![](D:/projet2/image/image (44).png){width="6.298611111111111in"
height="4.511111111111111in"}

![](D:/projet2/image/image (45).png){width="6.298611111111111in"
height="4.354166666666667in"}![](D:/projet2/image/image (46).png){width="6.298611111111111in"
height="4.6618055555555555in"}

Pour cette partie, j'ai commencé par les objets qui seront connectés au
smartphone du client comme : la fenêtre, la lampe, la porte, la sirène
1, le détecteur de fumée et l'extincteur de feu et ceux qui seront
connectés au smartphone de l'agent de sécurité comme : la camera, le
détecteur de mouvement et la sirène 2.

Après avoir fait cette séparation, on procède à la connexion de chaque
objet. Pour les objets qui seront connectés au smartphone de l'agent de
sécurité (smartphone0), on se rend dans l'onglet « config » de l'objet
en question, puis on clique sur « settings » et dans la section IoT
server on coche « remote server » et on remplit les lignes avec
192.168.1.5 qui est l'adresse du server-iot, puis colas et wendy qui
sont respectivement le username et le password du compte sur le
server-iot pour l'agent de sécurité. On procède de la même manière pour
le client tout en utilisant ses identifiants à lui.

Ensuite on se connecte sur chaque smartphone pour voir si les objets
sont bel et bien connectés et s'ils fonctionnent également.

Par la suite, j'ai ajoute plusieurs conditions qui donne une certaine
automatisation aux différents objets IoT. La première condition, ajoutée
sur le smartphone de l'agent de sécurité, est une condition de
détection : if détecteur de mouvement on is true then set camera on to
true and sirène 2 on to true. Avec cette condition, si le détecteur de
mouvement détecte une présence, automatique la camera s'allumera et la
sirène 2 se trouvant dans la chambre de l'agent de sécurité sera allumer
aussi.

Il y a une condition de non détection également : if détecteur de
mouvement on is false then set camera on to false and sirène 2 on to
false.

Des conditions sont aussi ajoutées sur le smartphone se trouvant dans la
chambre du client dont le premier s'appelle feu : if détecteur de fumée
level \>= 0,2 then set sirène 1 on to true, porte on to true, fenêtre on
to true, extincteur de feu status to true. Cette condition stipule que
si le détecteur détecte une fumée supérieure ou égale à 0,2 une sirène
dans la chambre de l'agent de sécurité se mettra à sonner, la porte et
la fenêtre s'ouvriront et l'extincteur de feu s'ouvrira aussi.

Une autre du nom de non feu est aussi posée qui est l'inverse de celle
intitulée feu.

Pour vérifier si les conditions fonctionnent, on utilise la touche ALT
et le curseur.

III. **Comparaison entre les protocoles IoT**

Dans le domaine de l'internet des objets (IoT), le choix du protocole de
communication est crucial pour garantir une transmission efficace des
données entre les appareils connectés. Trois protocoles majeurs sont
largement utilisés : MQTT, CoAP et http. Chacun d'eux présente des
caractéristiques uniques, en termes de performance et de complexité, et
leur fonctionnement varie selon les besoins du système IoT.

-   **MQTT (Message Queuing Telemetry Transport)**

Le MQTT est un protocole de messagerie léger conçu pour les réseaux avec
peu de bande passante et les appareils à faible puissance. Il est
souvent utilisé dans les systèmes IoT pour transmettre efficacement des
données entre appareils.

**Performance :**

-   Utilise un modèle de publication-abonnement.

-   Les appareils ne communiquent pas directement entre eux car ils
    envoient et reçoivent des messages via un courtier (serveur
    central).

-   Très rapide et efficace.

**Complexité :**

-   Moyenne

-   Nécessite un courtier pour gérer les échanges de messages.

-   Facile à intégrer mais demande une configuration précise.

```{=html}
<!-- -->
```
-   **CoAP (Constrained Application Protocol)**

Le CoAP est un protocole spécialement conçu pour les appareils IoT très
limités en énergie et en ressources. Il permet une communication rapide
et légère en utilisant un modèle proche de http.

**Performance :**

-   Fonctionne avec un modèle client-serveur.

-   Utilise UDP au lieu de TCP, ce qui le rend plus rapide et adapté aux
    objets connectés.

-   Permet aux petits appareils de faire des requêtes REST (GET, POST,
    PUT, DELETE) sur les serveurs.

**Complexité :**

-   Moyenne.

-   Basé sur UDP.

-   Peut être plus difficile à gérer lorsqu'on doit assurer la fiabilité
    des messages.

```{=html}
<!-- -->
```
-   **HTTP (Hypertext Transfert Protocol)**

HTTP est le protocole de communication le plus utilisé sur internet. Il
est conçu pour échanger des données entre les navigateurs et les
serveurs Web.

**Performance :**

-   Fonctionne avec un modèle serveur-client.

-   Utilise TCP pour assurer une transmission fiable des données.

**Complexité :**

-   Elevée.

-   Trop lourd pour les objets connectés avec peu de ressources.

IV. **Importance de l'IoT**

L'Internet des Objets joue un rôle fondamental dans la collecte de
données et l'automatisation des processus grâce à la connexion
intelligente entre appareils. Il permet :

1.  La collecte efficace des données

-   Les capteurs IoT peuvent surveiller en temps réel divers paramètres
    (température, humidité, mouvement, ...).

-   La transmission automatique des données permet d'éviter les erreurs
    humaines et améliorer la précision des analyses.

-   Ces informations permettent d'anticiper les problèmes, comme la
    maintenance préventive des machines avant qu'elles ne tombent en
    panne.

2.  L'automatisation des processus

L'IoT permet aux systèmes connectés d'agir sans intervention humaine.
Par exemple :

-   Les usines intelligentes ajustent leur production en fonction des
    besoins détectés.

-   Les bâtiments intelligents optimisent l'éclairage et le chauffage
    pour économiser de l'énergie.

3.  L'amélioration de l'efficacité et la réduction des coûts

-   Moins d'intervention humaine = moins d'erreurs et plus de rapidité
    dans l'exécution des tâches.

-   Optimisation de l'utilisation des ressources.

-   Amélioration de la sécurité.

V.  **Création du projet sur Jira**

Dans le cadre du projet intitulé Simulation d\'un Réseau IoT avec Cisco
Packet Tracer , une démarche de gestion agile a été mise en œuvre à
travers l\'utilisation de la méthode Scrum . L\'objectif de ce travail
était de simuler un environnement de développement itératif en
structurant les différentes phases du projet sous forme de user stories
, regroupées dans des Epics , et planifiées dans un Sprint de deux
semaines à l\'aide de l\'outil Jira. Ce rapport présente les étapes de
mise en œuvre de cette démarche, de la création du backlog à la
simulation du sprint, en passant par l\'organisation des tâches, la
planification et l\'évaluation.

1.  Création du projet Jira et structuration en Epics

La première étape a consisté à créer un nouveau projet Scrum dans Jira,
en lien avec le thème principal du projet IoT. Le travail a été découpé
en 5 grands Epics , chacun représentant une composante majeure du
système :

-   Infrastructure réseau

-   Intégration des objets IoT

-   Automatisation des objets

-   Expérience utilisateur via smartphone

-   Choix et analyse des protocoles IoT

Ces Epics ont permis de mieux organiser les tâches selon les différentes
dimensions du projet technique et fonctionnel.

Un backlog a été élaboré à partir des besoins fonctionnels du système.
Dix user stories ont été formulées en suivant le format classique (\"En
tant que\... je veux\... afin de\...\"). Chaque user story a été
associée à un Epic, facilitant leur hiérarchisation et planification.
Cette étape a permis d\'identifier les fonctionnalités clés à développer
: configuration réseau, connexion des capteurs, automatisation des
alertes, interface utilisateur, etc.

Un premier Sprint de deux semaines a été organisé. Son objectif
principal était de mettre en place l\'infrastructure de base, connecter
les premiers objets IoT, configurer les smartphones, et amorcer les
règles d\'automatisation.

Des tâches concrètes ont été créées pour chaque user story sélectionnée
pour ce sprint. Un effort particulier a été mis sur les tâches
prioritaires liées à la connectivité réseau, à la configuration du DHCP
et à la communication inter-chambre.

Dans Jira, un tableau Scrum a été configuré avec les colonnes \"À
faire\", \"En cours\", \"En revue\" et \"Terminé\". Les tâches ont
ensuite été déplacées au fil de la progression, reproduisant ainsi le
workflow agile . Cette représentation visuelle a permis de suivre en
temps réel l\'évolution du sprint et d\'identifier rapidement les
éventuels blocages.

À la fin du sprint, une démonstration des réalisations a été simulée :
les objets IoT ont bien été connectés, la configuration des serveurs
DHCP validée, et les premières automatisations testées avec succès.

La rétrospective a permis d\'identifier les points forts (bonne
structuration initiale, cohérence des Epics) et les axes d\'amélioration
(gestion des dépendances entre tâches, planification plus réaliste de
certaines fonctionnalités avancées).

![](D:/projet2/image/image (47).png){width="6.298611111111111in"
height="3.359027777777778in"}![](D:/projet2/image/image (48).png){width="6.298611111111111in"
height="3.285416666666667in"}

![](D:/projet2/image/image (49).png){width="6.298611111111111in"
height="3.354861111111111in"}![](D:/projet2/image/image (50).png){width="6.298611111111111in"
height="3.0548611111111112in"}

![](D:/projet2/image/image (51).png){width="6.298611111111111in"
height="3.2423611111111112in"}![](D:/projet2/image/image (52).png){width="6.298611111111111in"
height="3.123611111111111in"}

![](D:/projet2/image/image (53).png){width="6.298611111111111in"
height="3.3618055555555557in"}![](D:/projet2/image/image (54).png){width="6.298611111111111in"
height="3.3715277777777777in"}

![](D:/projet2/image/image (55).png){width="6.298611111111111in"
height="3.363888888888889in"}![](D:/projet2/image/image (56).png){width="6.298611111111111in"
height="3.154166666666667in"}

![](D:/projet2/image/image (57).png){width="6.298611111111111in"
height="3.1819444444444445in"}![](D:/projet2/image/image (58).png){width="6.298611111111111in"
height="3.1680555555555556in"}

![](D:/projet2/image/image (59).png){width="6.298611111111111in"
height="2.939583333333333in"}

VI. **Conclusion**

Ce document explore la conception et la configuration d\'un réseau IoT
dans Cisco Packet Tracer, en mettant en place une infrastructure
connectée pour l\'automatisation et la sécurité. Il détaille les
différents appareils IoT, leur connectivité, et les protocoles réseau
utilisés, notamment DHCP, Wi-Fi et OSPF.

Grâce à cette simulation, nous avons pu observer l\'échange de données
en temps réel, la gestion des équipements IoT, et l\'intégration de
règles automatisées pour optimiser le fonctionnement du réseau. En
comparant les protocoles de communication comme MQTT, CoAP et HTTP, le
document montre comment choisir le protocole le plus adapté selon les
besoins du système.

Cette étude met en avant l\'importance de l\'IoT dans la collecte de
données et l\'automatisation des processus, soulignant ses bénéfices en
matière de sécurité, efficacité et réduction des coûts. Elle démontre
également que, grâce à des outils comme Cisco Packet Tracer, il est
possible de concevoir des réseaux intelligents et performants, ouvrant
la voie à des applications pratiques dans divers domaines.

Ce travail a démontré l\'intérêt d\'appliquer la méthode Scrum à un
projet technique tel que la simulation d\'un réseau IoT. L\'utilisation
de Jira facilite l\'organisation, la planification et le suivi des
tâches. Cette approche itérative a permis de mieux visualiser la
progression du projet et de s\'adapter aux besoins au fur et à mesure.
Au-delà de l\'aspect technique, ce travail a renforcé la maîtrise des
outils de gestion de projet agile, essentiels dans le monde
professionnel actuel.
