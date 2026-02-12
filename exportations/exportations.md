# 🎬 Workflow Export Kling → DaVinci → Vimeo (Mac)
## Configuration stable · Sans délavage · Testée

---

## 1. Project Settings (à faire une fois par projet)

### Color Management
Project Settings → Color Management

- Color science : DaVinci YRGB Color Managed
- Automatic color management : ON
- Color processing mode : SDR
- Output color space : SDR Rec.709

Ces réglages assurent la cohérence interne dans DaVinci.  
Ils n’écrivent PAS les tags finaux du fichier exporté.

---

## 2. Preferences (Mac)

Preferences → General

- Use 10-bit precision in viewers if available : ON  
  (meilleure lecture des dégradés, fumée, néons, peaux)

- Use Mac display color profiles for viewers : OFF  
  (évite les compensations ColorSync trompeuses)

- Automatically tag Rec.709 Scene clips as Rec.709-A : OFF

Ces préférences n’affectent PAS l’export, uniquement l’affichage dans DaVinci.

---

## 3. Timeline / Color Page

- Aucun CST obligatoire
- Aucun LUT technique
- Étalonnage normal à l’œil + scopes

Si l’image est correcte dans DaVinci et dans VLC, elle est correcte.

---

## 4. Export VIMEO (CRITIQUE)

Deliver → Custom Export

### Format
- Format : H.264
- Resolution / FPS : identiques à la timeline

### Quality
- Quality : Automatic  
  (ou Restrict to 16–20 Mb/s en 1080p)

### Advanced Settings
- Pixel Aspect Ratio : Square
- Data Levels : Video

### Color Tags (POINT CLÉ)
- Color Space Tag : P3-DCI
- Gamma Tag : sRGB

Ce combo :
- évite le bug BT.470 System M
- force des métadonnées modernes et non ambiguës
- permet à Vimeo de reconvertir proprement
- garantit une image identique à DaVinci

Ce n’est PAS du vrai P3 cinéma.  
C’est un hack de tagging web-safe assumé et efficace.

### À NE PAS COCHER
- HDR
- Dolby Vision
- Rec.709-A pour Vimeo
- Full Data Levels

---

## Résumé ultra court

Vimeo (Mac) :
- Timeline : SDR Rec.709
- Export : H.264
- Color Space Tag : P3-DCI
- Gamma Tag : sRGB
- Data Levels : Video


---

