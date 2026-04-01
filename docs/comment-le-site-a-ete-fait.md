# 🛠️ Comment le site a été fait — Explication pour débutants

Ce document explique **comment le site sur les capteurs Tesla a été construit**, étape par étape, avec des mots simples. Même si tu n'as jamais codé, tu devrais comprendre !

---

## C'est quoi un site web ?

Un site web, c'est comme un **document** qu'on peut lire dans un navigateur (Chrome, Firefox, Edge...). Pour créer ce document, on utilise 3 langages différents qui ont chacun un rôle :

| Langage | Rôle | Analogie |
|---------|------|----------|
| **HTML** | La **structure** et le **contenu** | C'est le squelette + le texte du site. Comme les murs d'une maison. |
| **CSS** | Le **style** et l'**apparence** | C'est la peinture, la déco, les couleurs. Ce qui rend la maison jolie. |
| **JavaScript** | Les **actions** et l'**interactivité** | C'est l'électricité : les lumières qui s'allument, les portes qui s'ouvrent. |

---

## Les 3 fichiers du site

### 📄 `index.html` — Le contenu

C'est le fichier principal. Il contient :
- Tout le **texte** que tu lis sur le site
- La **structure** des sections (titres, paragraphes, tableaux, listes)
- Les liens vers les autres fichiers (CSS et JavaScript)

**Comment il est organisé :**
```
<html>                    ← Le début du document
  <head>                  ← Les infos "cachées" (titre de la page, liens CSS)
  </head>
  <body>                  ← Tout ce qu'on VOIT sur la page
    <nav>                 ← La barre de navigation en haut
    <section>             ← Une section du site (ex: "Les Caméras")
    <section>             ← Une autre section (ex: "Les Ultrasons")
    <footer>              ← Le pied de page tout en bas
  </body>
</html>
```

**Les balises HTML** (comme `<section>`, `<h2>`, `<p>`) sont des « conteneurs ». Elles disent au navigateur : « ceci est un titre », « ceci est un paragraphe », « ceci est une image », etc.

---

### 🎨 `style.css` — L'apparence

Ce fichier dit au navigateur **à quoi chaque élément doit ressembler**. Par exemple :

```css
body {
  background-color: #0a0a0f;    /* Fond très sombre (presque noir) */
  color: #e0e0e8;               /* Texte gris clair */
  font-family: 'Inter';         /* Police de caractères moderne */
}
```

**Ce que fait notre CSS :**

- **Dark mode** : fond sombre avec texte clair (plus agréable pour les yeux)
- **Glassmorphism** : les cartes ont un effet « verre dépoli » semi-transparent
- **Gradients** : des dégradés de couleurs (bleu → rouge) pour les titres
- **Animations** : les éléments apparaissent en glissant quand tu scrolles
- **Timeline** : la frise chronologique avec la ligne verticale et les points

**Tailwind CSS** : en plus de notre CSS perso, on utilise une bibliothèque appelée Tailwind. Au lieu d'écrire du CSS dans un fichier séparé, Tailwind permet d'ajouter le style **directement dans le HTML** avec des noms de classe. Par exemple :

```html
<!-- Sans Tailwind (CSS classique) -->
<p style="margin-bottom: 16px; font-size: 14px; color: gray;">Texte</p>

<!-- Avec Tailwind (plus rapide à écrire) -->
<p class="mb-4 text-sm text-gray-400">Texte</p>
```

`mb-4` = margin-bottom 4, `text-sm` = taille petite, `text-gray-400` = gris moyen. On combine les deux approches : Tailwind pour le layout rapide, CSS perso pour les effets spéciaux.

---

### ⚡ `script.js` — L'interactivité

Ce fichier ajoute du **mouvement** et de l'**intelligence** au site. Voici ce qu'il fait :

#### 1. Apparition au scroll (Scroll Reveal)
Quand tu descends dans la page, les éléments **apparaissent progressivement** au lieu d'être tous visibles d'un coup. C'est plus joli et ça guide la lecture.

**Comment ça marche :**
- On utilise un outil du navigateur appelé `IntersectionObserver`
- Il surveille quand un élément **entre dans la zone visible** de l'écran
- Quand c'est le cas, on ajoute la classe `visible` qui déclenche l'animation CSS

#### 2. Navbar dynamique
La barre de navigation en haut **change d'apparence** quand tu scrolles :
- En haut de page : transparente
- Après avoir scrollé : fond sombre avec ombre (pour rester lisible)

#### 3. Compteurs animés
Les chiffres clés (8 caméras, 360°, 250m...) **comptent de 0 jusqu'au nombre final** quand tu arrives dessus. C'est un petit effet visuel qui rend les stats plus impactantes.

#### 4. Menu mobile
Sur téléphone, le menu se transforme en **icône hamburger** (☰). Quand tu cliques dessus, le menu complet s'affiche en plein écran.

---

## Comment les fichiers travaillent ensemble

```
Le navigateur charge index.html
        │
        ├──→ Il lit le HTML et affiche le contenu
        │
        ├──→ Il charge style.css
        │     └──→ Il applique les couleurs, tailles, animations
        │
        ├──→ Il charge Tailwind (depuis internet)
        │     └──→ Il applique les classes utilitaires (mb-4, text-sm...)
        │
        └──→ Il charge script.js
              └──→ Il active les animations au scroll, le menu, etc.
```

---

## Les couleurs utilisées

| Couleur | Code | Utilisation |
|---------|------|-------------|
| 🔵 Bleu électrique | `#3B82F6` | Accents, liens, caméras |
| 🔴 Rouge Tesla | `#E31937` | Alertes, ultrasons, points importants |
| ⚫ Noir profond | `#0a0a0f` | Fond de la page |
| ⚪ Gris clair | `#e0e0e8` | Texte principal |
| 🩶 Gris moyen | `#8888a0` | Texte secondaire |

---

## Comment ouvrir le site

**Méthode simple :**
1. Va dans le dossier du projet
2. Double-clique sur `index.html`
3. Il s'ouvre dans ton navigateur !

**Méthode serveur (mieux pour le développement) :**
1. Ouvre un terminal
2. Tape : `python3 -m http.server 8080`
3. Va sur `http://localhost:8080` dans ton navigateur

---

## Résumé

| Question | Réponse |
|----------|---------|
| Combien de fichiers ? | 3 (`index.html`, `style.css`, `script.js`) |
| Faut-il installer quelque chose ? | Non ! Tailwind est chargé depuis internet |
| Le site a besoin d'internet ? | Oui, pour charger Tailwind et la police Inter |
| Peut-on le modifier ? | Oui ! Ouvre les fichiers dans un éditeur de code et modifie le texte |
| C'est compliqué ? | Le HTML se lit presque comme du français — essaie de trouver le texte dans `index.html` et de le changer ! |
