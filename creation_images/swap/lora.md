# Swap de visage avec un modèle Lora

## Étape 1
### Création d’un personnage dans [Lora portrait](https://fal.ai/models/fal-ai/flux-lora-portrait-trainer)
#### Rassembler les images  
Préparer *10 à 30 images* du même personnage.

* Variété recommandée :
  * angles différents  
  * expressions variées  
  * lumière
  * plans rapprochés + quelques plans moyens + quelques plans larges
* Qualité attendue : *haute résolution*, non floues, non surtraitées.

#### Uploader les images dans l’interface LoRA Trainer  
Importer le dossier d’images dans la section *training dataset*.

#### Choisir un nom de LoRA + Trigger Word  
Définir un mot-clé associé au personnage (utilisé ensuite dans les prompts).

Exemples :  
`mila_portrait`  
`mila_face`

Ce mot servira dans les prompts pour appeler le personnage.

#### Lancer la génération du LoRA  
Le système entraîne le fichier LoRA.

Sortie finale :  
`mila_character_lora_v1.safetensors`

#### Enregistrer les informations lora 
* Enregistrer le safetensors et le trigger le [document suivant](https://docs.google.com/spreadsheets/d/19-Cs2tzrXLF0pf7oHsrYckS0w65hZLjk/edit?usp=drive_link&ouid=109304383863739713675&rtpof=true&sd=true)


## Étape 2
### Utilisation du LoRA pour le swap de visages
#### Préparer l’entrée (prompt + scène + triggers)  
Décrire clairement la scène et intégrer les *trigger words* dans la description.

#### Importer les LoRA (.safetensors) et l’image de référence  

1. Copier le lien du fichier *.safetensors* dans le *path*.
2. Régler le *SCALE* (influence du LoRA) :
   * *1.0 – 1.2* → très fort (peut déformer)  
   * *0.7 – 0.9* → bon équilibre (recommandé)  
   * *0.4 – 0.6* → subtil, naturel  
   * *0.1 – 0.3* → presque invisible
3. Insérer l’image de référence (*img URL*) :
   * Dans le champ *Image / Init Image / Image URL* de la plateforme  
   * Coller l’URL de l’image (`img_url`)  
   * Ou uploader directement l’image si ce n’est pas une URL  
   * Cette image servira de base pour *img2img* / *inpaint* avec le LoRA  

#### Régler le Guidance (CFG)  

Contrôler à quel point le modèle suit le prompt.

* *3 – 5* → naturel, cinéma  
* *6 – 7* → très fidèle au prompt  
* *8+* → artificiel, trop « AI »  

#### Régler le Strength (img2img / inpaint)  

Contrôler le degré de modification de l’image source. C'est la valeur la plus importante.

*Valeurs STRENGTH (img2img / inpaint)* :

* *0.2 – 0.35* → modification subtile  
* *0.4 – 0.55* → équilibré  
* *0.6 – 0.8* → transformation forte  
* *0.9 – 1.0* → réécriture totale  

Cas d’usage :  

* Pour *remplacer un visage* : *0.28 – 0.45*  
* Pour *modifier une scène* : *0.55 – 0.75*  

#### Générer  

Lancer la génération avec les paramètres puis changer les paramètres en fonction de la génération.
