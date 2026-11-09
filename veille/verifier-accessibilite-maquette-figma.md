# Vérifier l'accessibilité d'une maquette Figma avant de la livrer

Cette page s'adresse aux designers qui transmettent une maquette à une équipe de développement ou à un client, quand les écrans sont validés et qu'on peut encore corriger une couleur ou un ordre de lecture avant que le code ne le fige.

*Mis à jour le 9 novembre 2026.*

## Par où commencer

| Votre situation | L'outil |
|---|---|
| Vous voulez vérifier vos contrastes pendant que vous dessinez, sans quitter Figma | [Usecontrast](#usecontrast) |
| Vous devez contrôler une couleur hors de Figma, dans un PDF ou une capture | [Colour Contrast Analyser](#colour-contrast-analyser) |
| Vous préparez une passation et voulez aussi simuler des troubles de la vision ou annoter l'ordre de focus | [Stark](#stark) |
| Votre client est un service public et vous voulez la liste de ce qui relève du design | [Checklist Pidila](#checklist-pidila) |

## Les outils

### Usecontrast

Ce plugin Figma, qui existe aussi en appli Mac, calcule sur-le-champ les ratios de contraste WCAG, mais il ne s'occupe que du contraste, si bien que l'ordre de lecture et les textes alternatifs restent à vérifier ailleurs. Le plugin est gratuit. [Voir la fiche](/outils/usecontrast/)

### Colour Contrast Analyser

Cette appli de bureau de Vispero, pour Windows et Mac, prélève avec sa pipette une couleur de texte et une couleur de fond n'importe où sur l'écran, puis donne le résultat selon les WCAG 2.0, 2.1 et 2.2, une paire de couleurs à la fois. Elle est gratuite. [Voir la fiche](/outils/color-contrast-checker/)

### Stark

Son plugin Figma regroupe le contraste, la typographie, un simulateur de troubles de la vision, l'ordre de focus, les repères de navigation, la taille des zones tactiles et des annotations de textes alternatifs, tandis que le compte gratuit commence par le vérificateur de contraste et le simulateur. L'offre Premium Pack coûte 198 $ par utilisateur et par an, avec trois sièges au minimum.

### Checklist Pidila

Publiée en accès libre sur le site de design de l'État, elle réunit en une seule liste les obligations et les bonnes pratiques de six référentiels, dont le RGAA, et se filtre par profil, notamment Conception et Graphisme, sans rien tester à votre place. [Voir la fiche](/references/checklist-pidila/)

## Les pièges

**Un ratio presque atteint reste un échec**, parce que le W3C précise que les valeurs calculées ne s'arrondissent pas, si bien qu'un texte courant à 4,49:1 ne passe pas le seuil de 4,5:1.

**Les états comptent autant que l'écran par défaut**, car un bouton qui passe le test au repos peut échouer au survol, au focus ou en erreur, alors vérifiez chaque état que vous dessinez, sauf le texte des composants inactifs, que le critère 1.4.3 des WCAG exempte de contraste.

## Questions fréquentes

### Quel contraste minimum demandent les WCAG pour un texte ?

Le critère 1.4.3, de niveau AA, demande au moins 4,5:1 pour le texte courant et 3:1 pour le grand texte, c'est-à-dire 18 points, ou 14 points en gras, soit environ 24 px et 18,5 px. Les icônes et les bordures de champ relèvent du critère 1.4.11, qui demande 3:1 contre les couleurs voisines.

### Le RGAA s'applique-t-il à une maquette Figma ?

Le RGAA se teste dans des navigateurs avec des lecteurs d'écran comme NVDA, JAWS, VoiceOver ou TalkBack, donc une maquette ne peut pas être déclarée conforme. Elle prépare en revanche les critères qui dépendent du design, comme les couleurs, l'ordre de lecture et les textes alternatifs, que vous annotez pour l'équipe de développement.

### Un plugin Figma suffit-il pour vérifier l'accessibilité d'une maquette ?

Un plugin vérifie bien ce qui se voit, comme les contrastes ou la simulation de troubles de la vision, alors qu'une partie de l'accessibilité dépend du code, du clavier et de ce que restitue un lecteur d'écran. Annotez donc ce que la maquette ne montre pas, puis faites tester le site construit.

## Sources

Pages lues le 9 novembre 2026, sauf les prix d'Usecontrast et de Vispero, relevés le 31 octobre.

- [RGAA, DINUM](https://accessibilite.numerique.gouv.fr/) et son [environnement de test](https://accessibilite.numerique.gouv.fr/methode/environnement-de-test/)
- [WCAG 2.2, critère 1.4.3](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) et [critère 1.4.11](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html)
- [Usecontrast pour Figma](https://www.figma.com/fr-fr/communaute/plugin/1149686177449921115/use-contrast)
- [Colour Contrast Analyser, Vispero](https://vispero.com/color-contrast-checker/)
- [Stark pour Figma](https://www.getstark.co/figma/) et [tarifs de Stark](https://www.getstark.co/pricing/)
- [Checklist Pidila](https://design.numerique.gouv.fr/outils/checklist-pidila/)
