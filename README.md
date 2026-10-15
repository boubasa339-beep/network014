# Interconnexion de deux départements avec un routeur Cisco (simulation)

Projet de labo réalisé sous **Cisco Packet Tracer**. Un réseau est
découpé en deux sous-réseaux (un par département), reliés par un
routeur Cisco 2901. Chaque département a un switch, 2 ordinateurs
et 1 imprimante.

> Projet réalisé en simulation (Packet Tracer) à but d'apprentissage.

## Objectifs
- Découper un réseau en deux sous-réseaux (subnetting en /25)
- Relier les deux départements avec un routeur
- Permettre la communication entre les ordinateurs et les imprimantes
  des deux départements

## Schéma du réseau
![Schéma du réseau](images/schema.png)

## Matériel utilisé (simulation)
- 1 routeur Cisco 2901
- 2 switchs Cisco 2960 (un par département)
- 4 ordinateurs (2 par département)
- 2 imprimantes (1 par département)

## Plan d'adressage

| Département            | Réseau             | Masque          | Plage utilisable        |
|------------------------|--------------------|-----------------|-------------------------|
| Comptes                | 192.168.40.0/25    | 255.255.255.128 | 192.168.40.1 à .126     |
| [Livraison]            | 192.168.40.128/25  | 255.255.255.128 | 192.168.40.129 à .254   |

| Équipement           | Adresse IP         | Passerelle        |
|----------------------|--------------------|-------------------|
| Routeur (côté Comptes)   | [192.168.40.1]   | -                 |
| Routeur (côté [Livraison]) | [192.168.40.129] | -               |
| PC0                  | [192.168.40.2]     | [192.168.40.1]    |
| PC1                  | [192.168.40.3]     | [192.168.40.1]    |
| Printer0             | [192.168.40.4]     | [192.168.40.1]    |
| PC2                  | [192.168.40.130]   | [192.168.40.129]  |
| PC3                  | [192.168.40.131]   | [192.168.40.129]  |
| Printer1             | [192.168.40.132]   | [192.168.40.129]  |

## Configuration réalisée
- Découpage du réseau 192.168.40.0/24 en deux sous-réseaux /25
- Adressage IP des deux interfaces du routeur (une par sous-réseau)
- Adressage IP des ordinateurs et des imprimantes, avec la passerelle
  de leur département
- Vérification de la connectivité avec `ping`

## Comment tester
1. Installer **Cisco Packet Tracer** (gratuit avec un compte Cisco
   Networking Academy)
2. Ouvrir le fichier `project14.pkt`
3. Depuis PC0 (Comptes), faire un `ping` vers PC2 : la réponse
   doit être **OK**
4. Faire un `ping` vers Printer1 : **OK**

## Contenu du dépôt
- `project14.pkt` : le projet complet
- `images/` : schéma et captures d'écran

## Compétences mises en pratique
Subnetting (/25), adressage IP, configuration d'un routeur Cisco (CLI),
interconnexion de réseaux, tests de connectivité, documentation technique.

## Auteur
Boubacar Kalagna Sanogo
L3 Réseaux et Télécommunications, ISTAG, Bamako
boubasa339@gmail.com
