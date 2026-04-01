# 📖 Glossaire — Les mots compliqués expliqués simplement

Ce document explique tous les termes techniques utilisés sur le site, avec des mots simples.

---

## Les capteurs

### Capteur
Un **capteur**, c'est comme un « sens » pour la voiture. Nous, les humains, on a les yeux, les oreilles, le toucher... Une voiture a besoin de capteurs pour « sentir » ce qu'il y a autour d'elle.

### Capteur ultrasonique (USS)
C'est un petit appareil qui envoie du **son** (qu'on ne peut pas entendre) et qui écoute l'écho qui revient. C'est exactement comme quand tu cries dans une grotte et que tu entends l'écho — sauf que c'est un son très aigu, invisible à nos oreilles. En mesurant combien de temps l'écho met à revenir, la voiture sait à quelle distance se trouve un obstacle.

**Exemple du quotidien :** c'est le même principe que le « bip bip bip » quand tu te gares — plus tu t'approches d'un mur, plus ça bipe vite.

### Radar
Le radar utilise des **ondes radio** (comme le Wi-Fi, mais différent) pour détecter les objets. Il envoie une onde invisible, elle rebondit sur un obstacle et revient. Le radar peut mesurer à la fois **la distance** et **la vitesse** de l'objet.

**Avantage :** le radar fonctionne même sous la pluie, dans le brouillard ou la nuit noire, parce que les ondes radio traversent tout ça sans problème.

### LiDAR
Un capteur utilisé par d'autres constructeurs (pas Tesla). Il fonctionne avec des **rayons laser** pour créer une carte 3D ultra-précise de l'environnement. Tesla a choisi de ne PAS l'utiliser car c'est très cher.

---

## L'intelligence artificielle

### Réseau de neurones (Neural Network)
Imagine un cerveau artificiel. Comme notre cerveau a des milliards de neurones connectés entre eux pour réfléchir, un réseau de neurones artificiel est un programme informatique qui imite ce fonctionnement. On lui montre des millions d'exemples (photos de voitures, piétons, panneaux...) et il **apprend tout seul** à les reconnaître.

**Exemple simple :** c'est comme un enfant qui apprend à reconnaître un chat. Au début il se trompe, mais après avoir vu 1000 photos de chats, il les reconnaît à chaque fois. Le réseau de neurones fait pareil, mais avec des millions d'images.

### Intelligence artificielle (IA)
C'est la capacité d'un ordinateur à faire des choses « intelligentes » : reconnaître des objets, prendre des décisions, apprendre de ses erreurs. Les réseaux de neurones sont un **type** d'intelligence artificielle.

### Apprentissage profond (Deep Learning)
C'est un réseau de neurones avec **beaucoup de couches** (d'où le mot « profond »). Plus il y a de couches, plus le système peut comprendre des choses complexes. C'est la technologie que Tesla utilise pour analyser les images de ses caméras.

---

## Tesla Vision

### Tesla Vision
C'est le nom que Tesla donne à son système qui utilise **uniquement les caméras** (pas de radar, pas d'ultrasons) pour comprendre l'environnement. C'est comme si la voiture « voyait » le monde avec ses 8 caméras et « réfléchissait » avec son intelligence artificielle.

### Occupancy Network (Réseau d'occupation)
Imagine un cube 3D invisible autour de la voiture, découpé en millions de petites cases. L'Occupancy Network regarde les images des caméras et détermine pour chaque petite case : **« est-ce qu'il y a quelque chose ici, oui ou non ? »**. Ça permet à la voiture de savoir exactement où sont les objets autour d'elle, même sans capteurs ultrasoniques.

### Sensor Contention (Conflit de capteurs)
Quand deux capteurs différents (par exemple le radar et la caméra) disent des choses **contradictoires**. Exemple : la caméra voit un pont, le radar pense que c'est un mur. La voiture ne sait pas qui croire. C'est une des raisons pour lesquelles Tesla a retiré le radar.

### Sensor Fusion (Fusion de capteurs)
C'est le fait de **combiner les informations** de plusieurs capteurs différents pour avoir une meilleure compréhension de l'environnement. C'est ce que font les autres constructeurs. Tesla a décidé de ne plus le faire.

---

## L'Autopilot

### Autopilot
Le système d'aide à la conduite de Tesla. Attention : malgré son nom, ce n'est **PAS** de la conduite 100% autonome. Le conducteur doit toujours rester attentif et garder les mains sur le volant.

### FSD (Full Self-Driving)
Signifie « conduite entièrement autonome ». C'est le système le plus avancé de Tesla. Même avec ce système, Tesla demande toujours qu'un humain **surveille** la route (d'où le nom "FSD Supervised").

### OTA (Over-The-Air)
Ça veut dire « par les airs ». C'est une **mise à jour à distance**, comme quand ton téléphone se met à jour tout seul via le Wi-Fi. Tesla peut améliorer le logiciel de ses voitures de la même façon, sans que tu ailles chez le garagiste.

---

## Les termes techniques de la voiture

### Champ de vision (FOV - Field of View)
C'est **l'angle** que peut voir une caméra. Un champ de vision de 120° veut dire que la caméra voit très large (presque comme un œil de poisson). Un champ de vision de 35° veut dire qu'elle voit loin mais étroit (comme des jumelles).

### 360 degrés
Ça veut dire « tout autour ». Si tu tournes sur toi-même en faisant un tour complet, tu as vu à 360°. Les 8 caméras de Tesla couvrent ensemble les 360° autour de la voiture — aucun angle mort.

### Voxel
C'est un **pixel en 3D**. Tu connais les pixels (les petits carrés qui forment une image sur un écran). Un voxel c'est pareil mais en volume : un petit cube dans l'espace 3D. L'Occupancy Network utilise des voxels pour construire sa carte 3D.

### Hardware (HW) / Matériel
C'est la partie **physique** de l'ordinateur : les puces, les caméras, les câbles. C'est ce qu'on peut toucher. Quand Tesla parle de « Hardware 3 » ou « Hardware 4 », ça veut dire la 3ᵉ ou 4ᵉ version de leur ordinateur de bord.

### Software / Logiciel
C'est la partie **immatérielle** : le programme, le code, l'intelligence. C'est ce qui fait fonctionner le matériel. Tesla peut améliorer le logiciel par mise à jour OTA sans changer le matériel.

---

## Unités de mesure

| Terme | Explication simple |
|-------|-------------------|
| **kHz** (kilohertz) | Mesure de fréquence du son. 40 kHz = 40 000 vibrations par seconde. Trop aigu pour nos oreilles. |
| **GHz** (gigahertz) | Mesure de fréquence des ondes radio. 77 GHz = 77 milliards de vibrations par seconde. |
| **m** (mètres) | Distance. 250 m ≈ 2,5 terrains de football alignés. |
| **ms** (millisecondes) | 1 millième de seconde. 100 ms = 0,1 seconde. C'est quasi-instantané pour un humain. |
| **img/s** | Images par seconde. 36 img/s veut dire que la caméra prend 36 photos par seconde (plus fluide qu'un film au cinéma). |
