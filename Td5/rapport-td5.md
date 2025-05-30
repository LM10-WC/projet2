# Reproduction de la topologie en implémentant le Protocole de Routage OSPF dans un Réseau

## Introduction
Ce rapport documente la configuration et l'implémentation du protocole de routage **OSPF** dans un réseau, illustrée par une série de captures d’écran. L'objectif est de montrer les différentes étapes de mise en place des éléments réseaux et leur interaction.

## 1. Architecture du réseau
Voici la topologie du réseau utilisée pour l’implémentation du protocole **OSPF** :

![image 1](D:/projet2/Td5/image/image (1).png)

## 2. Configuration des réseaux sans fil
La configuration des points d'accès sans fil et des paramètres SSID est représentée ci-dessous :

![image 2](D:/projet2/Td5/image/image (2).png)

## 3. Paramétrage du DHCP
Le serveur DHCP est configuré pour l'attribution dynamique des adresses IP aux périphériques IoT et autres équipements réseau :

![image 3](D:/projet2/Td5/image/image (3).png)

## 4. Configuration des appareils IoT
Chaque appareil IoT est intégré au réseau via des paramètres spécifiques, incluant les configurations sans fil et d’adressage :

### 4.1 IoT1
![image 4](D:/projet2/Td5/image/image (4).png)

### 4.2 IoT8
![image 5](D:/projet2/Td5/image/image (5).png)
![image 6](D:/projet2/Td5/image/image (6).png)
![image 7](D:/projet2/Td5/image/image (7).png)

## 5. Paramétrage des serveurs
Les serveurs du réseau sont configurés avec des adresses statiques et intégrés au protocole OSPF pour assurer la redondance et l'interconnexion :

### 5.1 ServerIoT – Adressage et authentification
![image 8](D:/projet2/Td5/image/image (8).png)

### 5.2 Configuration DHCP du serveur
![image 9](D:/projet2/Td5/image/image (9).png)

### 5.3 Statique IPv4 et IPv6 sur ServerIoT
![image 10](D:/projet2/Td5/image/image (10).png)

## 6. Sécurité et optimisation
L’authentification et le chiffrement sont des éléments essentiels à la sécurisation du réseau. Voici les configurations de **IoT8** montrant les paramètres de sécurité actuels et les éventuelles améliorations :

![image 11](D:/projet2/Td5/image/image (11).png)

## 7. Analyse et amélioration
L’implémentation actuelle de **OSPF** garantit une connectivité robuste et évolutive. Des améliorations peuvent être apportées en intégrant un mécanisme **de segmentation VLAN** et en optimisant les méthodes de routage pour améliorer l’efficacité du réseau.

![image 12](D:/projet2/Td5/image/image (12).png)
![image 13](D:/projet2/Td5/image/image (13).png)

## Conclusion
L’implémentation du **protocole OSPF** dans un réseau permet d’assurer une **gestion dynamique des routes**, améliorant ainsi la redondance et la performance globale. Une sécurisation renforcée via **WPA2-PSK et des authentifications plus robustes** serait un axe d’amélioration majeur, en particulier dans un environnement intégrant des **appareils IoT**.

---

# Configuration d'un réseau IoT dans Cisco Packet Tracer

## Introduction
Ce rapport décrit la mise en place et la configuration d'un réseau **IoT** dans **Cisco Packet Tracer**, incluant l'architecture réseau, les paramètres des appareils, la gestion DHCP, et l'intégration du routage dynamique. Chaque section est accompagnée des **captures d’écran** illustrant les étapes clés.

## 1. Topologie du réseau
La configuration générale du réseau est illustrée ci-dessous :

![image 14](D:/projet2/Td5/image/image (14).png)

## 2. Configuration des points d'accès
Les **points d’accès Wi-Fi** sont configurés pour permettre aux **périphériques IoT** de se connecter :

![image 15](D:/projet2/Td5/image/image (15).png)

## 3. Paramétrage des serveurs DHCP
Les **serveurs DHCP** sont mis en place pour distribuer les adresses IP aux différents équipements du réseau :

![image 16](D:/projet2/Td5/image/image (16).png)
![image 17](D:/projet2/Td5/image/image (17).png)

## 4. Configuration des appareils IoT
Les **périphériques IoT** sont configurés avec leurs paramètres réseau et authentification.

### 4.1 IoT0
![image 18](D:/projet2/Td5/image/image (18).png)

### 4.2 IoT3
![image 19](D:/projet2/Td5/image/image (19).png)

### 4.3 IoT8
![image 20](D:/projet2/Td5/image/image (20).png)

## 5. Sécurisation des accès et authentification
Les paramètres de sécurité et d’authentification des **appareils IoT et points d’accès** sont examinés :

![image 21](D:/projet2/Td5/image/image (21).png)
![image 22](D:/projet2/Td5/image/image (22).png)

## 6. Configuration OSPF sur les routeurs
Les **routeurs** sont configurés avec le **protocole de routage OSPF**, assurant une **connectivité dynamique** et une **résilience du réseau**.

### 6.1 Routeur R1 - Configuration OSPF
![image 23](D:/projet2/Td5/image/image (23).png)

### 6.2 Routeur R2 - Vérification des routes
![image 24](D:/projet2/Td5/image/image (24).png)
![image 25](D:/projet2/Td5/image/image (25).png)

## 7. Tests de connectivité
Les **tests `ping` et `traceroute`** confirment la stabilité et la bonne communication entre les appareils :

![image 26](D:/projet2/Td5/image/image (26).png)
![image 27](D:/projet2/Td5/image/image (27).png)

## 8. Interface web du serveur IoT
Le **serveur IoT** est accessible via une interface web, permettant de gérer les **appareils connectés** et définir des **règles d’automatisation**.

### 8.1 Accès au serveur
![image 28](D:/projet2/Td5/image/image (28).png)

### 8.2 Gestion des appareils
![image 29](D:/projet2/Td5/image/image (29).png)
![image 30](D:/projet2/Td5/image/image (30).png)

### 8.3 Paramètres de contrôle et automatisation
![image 31](D:/projet2/Td5/image/image (31).png)
![image 32](D:/projet2/Td5/image/image (32).png)

## 9. Configuration avancée des périphériques IoT
Cette section intègre les paramètres détaillés des périphériques IoT.

### 9.1 IoT4
![image 33](D:/projet2/Td5/image/image (33).png)
![image 34](D:/projet2/Td5/image/image (34).png)

### 9.2 IoT5
![image 35](D:/projet2/Td5/image/image (35).png)
![image 36](D:/projet2/Td5/image/image (36).png)

### 9.3 IoT6
![image 37](D:/projet2/Td5/image/image (37).png)
![image 38](D:/projet2/Td5/image/image (38).png)

### 9.4 IoT7
![image 39](D:/projet2/Td5/image/image (39).png)
![image 40](D:/projet2/Td5/image/image (40).png)

### 9.5 IoT9
![image 41](D:/projet2/Td5/image/image (41).png)
![image 42](D:/projet2/Td5/image/image (42).png)

## 10. Optimisation du réseau
Cette section analyse les **paramètres réseaux avancés** et propose des améliorations.

### 10.1 Configuration du serveur IoT
![image 43](D:/projet2/Td5/image/image (43).png)

### 10.2 Vérification des adresses IP
![image 44](D:/projet2/Td5/image/image (44).png)
![image 45](D:/projet2/Td5/image/image (45).png)

### 10.3 Analyse des performances réseau
![image 46](D:/projet2/Td5/image/image (46).png)
![image 47](D:/projet2/Td5/image/image (47).png)

### 10.4 Tests complémentaires
![image 48](D:/projet2/Td5/image/image (48).png)
![image 49](D:/projet2/Td5/image/image (49).png)

### 10.5 Finalisation des tests et ajustements
![image 50](D:/projet2/Td5/image/image (50).png)
![image 51](D:/projet2/Td5/image/image (51).png)
![image 52](D:/projet2/Td5/image/image (52).png)
![image 53](D:/projet2/Td5/image/image (53).png)

![image 55](D:/projet2/Td5/image/image (55).png)
![image 60](D:/projet2/Td5/image/image (60).png)

---

## Conclusion
Ce rapport documente l’ensemble du **processus de configuration d’un réseau IoT** dans **Cisco Packet Tracer**, illustrant la mise en place des **serveurs DHCP, des routeurs OSPF, des points d’accès Wi-Fi et des appareils IoT**. Il met en avant la nécessité de sécuriser les **connexions IoT** et d'optimiser la **gestion des équipements** pour garantir un **réseau performant et résilient**.

