# Interconnexion de deux départements (Cisco, simulation)

Projet de labo réalisé sous **Cisco Packet Tracer**. Il relie deux
départements d'une entreprise grâce à deux routeurs Cisco. Chaque
département possède 2 ordinateurs et 1 imprimante réseau.

> Projet réalisé en simulation (Packet Tracer) à but d'apprentissage.

## Objectifs
- Mettre en place un réseau local dans chaque département
- Relier les deux départements avec un routeur chacun
- Permettre la communication entre les ordinateurs et les imprimantes
  des deux départements

## Schéma du réseau
![Schéma du réseau](images/schema.png)

## Matériel utilisé (simulation)
- 2 routeurs Cisco (un par département)
- [2 switchs, un par département]
- 4 ordinateurs (2 par département)
- 2 imprimantes (1 par département)

## Plan d'adressage

| Équipement            | Adress IP        |  Passerelle   |
|-----------------------|-----------------|--------------|
| Département 1 - PC1   | 192.168.40.2/25  |  192.168.40.1  |
| Département 1 - PC2   | 192.168.40.3/25  |  192.168.40.1  |
| Département 1 - Imprimante |192.168.40.4/25 |  192.168.40.1  |
| Département 2 - PC1   | 192.168.40.130  |  192.168.40.129  |
| Département 2 - PC2   | 192.168.40.131  | 192.168.40.129|
| Département 2 - Imprimante | 192.168.40.132 |  192.168.40.129  |
  

## Configuration réalisée
- Adressage IP des interfaces des deux routeurs
- Adressage IP des ordinateurs et des imprimantes
- [Routage entre les deux départements : routes statiques]
- Vérification de la connectivité avec `ping`

## Comment tester
1. Installer **Cisco Packet Tracer** (gratuit avec un compte Cisco
   Networking Academy)
2. Ouvrir le fichier `nom-du-projet.pkt`
3. Depuis le PC1 du département 1, faire un `ping` vers le PC1 du
   département 2 : la réponse doit être **OK**
4. Faire un `ping` vers l'imprimante du département 2 : **OK**

## Contenu du dépôt
- `nom-du-projet.pkt` : le projet complet
- `images/` : schéma et captures d'écran
- `configs/` : configurations des routeurs (si ajoutées)

## Compétences mises en pratique
Adressage IP, configuration de routeurs Cisco (CLI), routage,
tests de connectivité, documentation technique.

## Auteur
Boubacar Kalagna Sanogo
L3 Réseaux et Télécommunications, ISTAG, Bamako
boubasa339@gmail.com
