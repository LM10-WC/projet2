**Institut Universitaire des Sciences**

**Faculté des Sciences et Technologies**

**Td8 dans le cadre du cours de Réseaux 2**


**Préparé par Wendy COLAS**

**A l'attention de Monsieur Ismaël SAINT AMOUR**

**Mai 2025**

# Installation et Configuration de pfSense sur une VM

## Introduction
Ce document décrit le processus d'installation et de configuration de **pfSense** sur une machine virtuelle dans **VirtualBox**. L'objectif est de mettre en place un firewall et un routeur virtuel permettant une gestion avancée des réseaux.

---

## 1. Préparation de la Machine Virtuelle
Avant de commencer l’installation de pfSense, nous avons créé une VM sous VirtualBox avec les paramètres adaptés :
- **Type du système** : BSD
- **Version** : FreeBSD (64-bit)
- **Mémoire** : 2 Go (2048 Mo)
- **Processeur** : 1 vCPU
- **Disque dur** : 20 Go (VDI)
- **Interfaces réseau** : WAN et LAN

![Configuration de la VM](D:\projet2\Td8\image\image (1).png)

---

## 2. Installation de pfSense
### 2.1. Démarrage de l’ISO
Une fois la VM configurée, nous avons monté l’ISO et démarré l’installation.

![Démarrage de l'installation](D:\projet2\Td8\image\image (2).png)

### 2.2. Configuration des partitions
Nous avons opté pour une partition **Auto UFS** afin de simplifier l’installation.

![Choix de partition](D:\projet2\Td8\image\image (3).png)

### 2.3. Sélection des interfaces réseau
Nous avons défini les interfaces **WAN (Bridged Adapter)** et **LAN (Internal Network)** pour un accès interne sécurisé.

![Configuration réseau](D:\projet2\Td8\image\image (4).png)

---

## 3. Configuration de pfSense
### 3.1. Attribution des adresses IP
- **WAN** : DHCP (IP attribuée dynamiquement)
- **LAN** : 192.168.1.1/24 (Passerelle)

![Configuration IP](D:\projet2\Td8\image\image (5).png)

### 3.2. Accès à l'interface Web
Nous nous connectons à l’interface Web via **http://192.168.1.1** pour finaliser les réglages.

![Interface Web pfSense](D:\projet2\Td8\image\image (6).png)

---

## 4. Configuration avancée
### 4.1. Configuration du WAN
Le WAN est configuré avec l’option **DHCP** pour une attribution automatique de l’adresse IP.

![Configuration WAN](D:\projet2\Td8\image\image (7).png)

### 4.2. Paramétrage du LAN
Le réseau local est défini sur **192.168.2.1/24**, permettant la gestion des équipements internes.

![Configuration LAN](D:\projet2\Td8\image\image (8).png)

---

## 5. Vérification et Optimisation
Nous avons procédé à plusieurs tests pour nous assurer du bon fonctionnement des interfaces.

### 5.1. Test de connectivité
Nous avons vérifié que les interfaces sont bien actives et que les règles de pare-feu ne bloquent pas le trafic.

![Test de connectivité](D:\projet2\Td8\image\image (9).png)

### 5.2. Firewall et NAT
Nous avons mis en place des règles de **filtrage** et de **NAT** pour permettre l’accès contrôlé au réseau.

![Configuration Firewall](D:\projet2\Td8\image\image (10).png)

---

## 6. Finalisation et Tests
Le système est maintenant **opérationnel**, et nous avons validé son bon fonctionnement.

### 6.1. Vérification des Logs
Les logs indiquent une bonne synchronisation des interfaces.

![Vérification des logs](D:\projet2\Td8\image\image (11).png)

### 6.2. Tests avancés et débogage
Nous avons corrigé quelques **problèmes mineurs** et optimisé certaines configurations réseau.

![Débogage](D:\projet2\Td8\image\image (12).png)
![image (13)](D:\projet2\Td8\image\image (13).png)
![image (14)](D:\projet2\Td8\image\image (14).png)
![image (15)](D:\projet2\Td8\image\image (15).png)
![image (16)](D:\projet2\Td8\image\image (16).png)
![image (17)](D:\projet2\Td8\image\image (17).png)
![image (18)](D:\projet2\Td8\image\image (18).png)
![image (19)](D:\projet2\Td8\image\image (19).png)
![image (20)](D:\projet2\Td8\image\image (20).png)
![image (21)](D:\projet2\Td8\image\image (21).png)
![image (22)](D:\projet2\Td8\image\image (22).png)
![image (23)](D:\projet2\Td8\image\image (23).png)
![image (24)](D:\projet2\Td8\image\image (24).png)
![image (25)](D:\projet2\Td8\image\image (25).png)
![image (26)](D:\projet2\Td8\image\image (26).png)
![image (27)](D:\projet2\Td8\image\image (27).png)
![image (28)](D:\projet2\Td8\image\image (28).png)
![image (29)](D:\projet2\Td8\image\image (29).png)
![image (30)](D:\projet2\Td8\image\image (30).png)
![image (31)](D:\projet2\Td8\image\image (31).png)
![image (32)](D:\projet2\Td8\image\image (32).png)

---

## Conclusion
L’installation et la configuration de **pfSense** sur une VM permettent de disposer d’une **solution complète** de firewall et de routage. En suivant ces étapes, nous obtenons un environnement sécurisé et adapté à la gestion avancée du réseau.

---




