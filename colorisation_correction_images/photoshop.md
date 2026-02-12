# Colorisation & retouche - Photoshop

## 🟠 Objectif  
Corriger la lumière, équilibrer les couleurs et retoucher localement une image en suivant un ordre logique et professionnel.

---

## 🛠️ Workflow

* Ajuster l’exposition générale  
  * Créer un calque **Exposition**  
    * Corriger sous/sur-exposition  
    * Ajuster les tons moyens  
  * Ajouter un calque **Courbes**  
    * Ajuster le contraste 
    * Option : légère **courbe en S** pour un contraste propre

* Corriger les couleurs globales (Selective Color / Couleur sélective)  
  * Créer un calque **Couleur sélective (Selective Color)**  
  * Travailler les gammes suivantes :  
    * **Rouges (Reds)** → peau, lèvres, éléments rouges  
    * **Gris (Neutrals)** → équilibre général de l’image  
    * **Noirs (Blacks)** → profondeur des ombres  
  * Ajuster Cyan / Magenta / Jaune / Noir dans chaque gamme pour corriger la dérive de couleur

* Retoucher des zones spécifiques  
  * Sélectionner une zone (Lasso, Sélection d’objet, Sélection rapide, Sujet)  
  * Ajouter un calque de réglage (Couleur sélective ou Courbes)  
  * **Inverser le masque (Ctrl/Cmd + I)** → masque noir  
  * Peindre en **blanc** sur le masque pour appliquer la correction uniquement à l’endroit voulu  
    * Exemple :  
      * Corriger la couleur d’un vêtement  
      * Assombrir ou éclaircir une zone du visage  
      * Neutraliser une dominante locale (mur, lumière parasite)

* Effectuer des corrections avec l’IA Photoshop  
  * Pour supprimer un élément :  
    * Faire une **sélection** → **Génération IA → Remove / Supprimer**
    * Entrer un prompt court, par exemple :  
      * “.”  
  * Pour modifier une zone :  
    * Sélection → **Génération IA**  
    * Entrer un prompt court, par exemple :  
      * “soften skin” / “adoucir la peau”  
      * “reduce highlights” / “réduire les hautes lumières”  
      * “cooler tones” / “rendre la lumière plus froide”

* Finaliser l’image  
  * Ajouter **Vibrance** pour un boost de saturation doux  
  * Ajouter **Color Lookup (Correspondance de couleur)** pour le look global :  
    * 📍 Chemin :  
      * **Calque → Nouveau calque de réglage → Correspondance de couleur…**  
      * ou via l’icône demi-cercle en bas du panneau **Calques**  
    * Choisir un LUT (Film, Teal & Orange, etc.)  
    * Ajuster l’**opacité** du calque pour doser l’effet

---
