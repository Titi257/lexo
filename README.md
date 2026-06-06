# Lexo

Traduisez le texte sélectionné dans **n'importe quelle app** — d'un simple raccourci clavier. Sélectionnez, appuyez sur `⌃⌥T`, la traduction apparaît dans une petite bulle. C'est tout.

- **100 % local et hors-ligne** — la traduction tourne sur votre Mac via le moteur d'Apple. Aucune requête réseau, aucun compte, aucune télémétrie.
- **Marche partout** — navigateur, Mail, PDF, Slack, Notes… tout ce qui contient du texte sélectionnable.
- **Discret** — vit dans la barre de menus, sans icône dans le Dock.
- **Votre presse-papiers est préservé** — l'app le restaure à l'identique après chaque traduction.

## ⬇️ Télécharger

➡️ **[Télécharger la dernière version (.dmg)](https://github.com/Titi257/lexo/releases/latest/download/Lexo.dmg)**

## Configuration requise

- **macOS 15 (Sequoia) ou plus récent** — requis par le moteur de traduction d'Apple.
- **Mac Intel ou Apple Silicon** — application universelle, native sur les deux.

## Installation

1. Ouvrez **`Lexo.dmg`**.
2. Glissez **Lexo** dans le dossier **Applications**.
3. Lancez **Lexo** depuis Applications (ou Spotlight).

> L'app est signée et notarisée par Apple : aucun avertissement « développeur non identifié » au lancement.

## Premier lancement

Un assistant de bienvenue vous guide en 4 étapes :

1. **Présentation** de l'app.
2. **Permission Accessibilité** — indispensable. Cliquez sur **Ouvrir Réglages**, puis activez **Lexo** dans
   *Réglages Système → Confidentialité et sécurité → Accessibilité*.
   Sans cette autorisation, l'app ne peut pas lire votre sélection (rien ne se passera quand vous appuierez sur le raccourci).
3. **Langue cible** — vers quelle langue traduire (français par défaut). Modifiable à tout moment.
4. **C'est prêt !**

## Utilisation

1. **Sélectionnez** du texte dans n'importe quelle app.
2. Appuyez sur **`⌃⌥T`** (Contrôle + Option + T).
3. La **bulle** affiche la traduction. `Échap` ou un clic ailleurs la ferme. Le bouton **Copier** met la traduction dans le presse-papiers.

> **Première traduction d'une nouvelle paire de langues** : macOS télécharge automatiquement le modèle correspondant (~30 Mo). C'est ponctuel ; ensuite tout est instantané et hors-ligne.

## L'icône dans la barre de menus

Cliquez sur l'icône de **Lexo** en haut à droite pour :

- **Traduire** la sélection courante (équivalent du raccourci),
- ouvrir les **Préférences** (changer la langue cible, redéfinir le raccourci, revoir l'aide, consulter l'historique),
- **Quitter**.

## Confidentialité

Tout se passe sur votre Mac. Aucun texte ne quitte l'appareil, aucune connexion réseau n'est utilisée pour traduire, et aucune donnée n'est collectée.

## Dépannage

- **Rien ne se passe quand j'appuie sur le raccourci** → vérifiez que **Accessibilité** est bien activée pour Lexo dans les Réglages Système, puis relancez l'app.
- **« Aucune sélection détectée »** → assurez-vous d'avoir du texte sélectionné dans l'app active avant d'appuyer sur le raccourci. Dans certaines apps Electron (Slack, VS Code, Discord), réessayez une fois.
- **Le raccourci entre en conflit avec une autre app** → redéfinissez-le dans **Préférences**.

---

© 2026 Kevin Boileux — Tous droits réservés.
