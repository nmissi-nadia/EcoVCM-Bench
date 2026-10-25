# Protocole Expérimental

## 1. Objectifs de l'Évaluation
Évaluer et comparer les performances des différentes méthodes VCM selon trois axes cardinaux :
1. **Efficacité de compression** : Débit binaire (*Bitrate*, kbps / bpp).
2. **Performance de la tâche aval** : Précision (*mAP50*, *mAP50-95*, etc.).
3. **Coût énergétique et environnemental** : Consommation électrique (Joules, Watts), empreinte carbone estimée ($gCO_2eq$).

---

## 2. Jeux de Données (Datasets)
- **Détection / Suivi d'objets** : ex. MOT17/20, VisDrone, BDD100K, COCO (images/vidéos clés).
- **Segmentation / Action** : ex. Cityscapes, UCF101 (selon le scope choisi).

---

## 3. Méthodes & Modèles Comparés (Baselines)
1. **Lignes de base classiques (Pixel Coding)** :
   - H.264 / AVC (FFmpeg `libx264`)
   - H.265 / HEVC (FFmpeg `libx265`, VTM)
   - AV1 (SVT-AV1, `libaom`)
2. **Approches VCM / Apprentissage profond** :
   - Compression de caractéristiques (*Feature Compression*).
   - Codecs vidéo neuronaux orientés machine (ex: DVC, DCVC adapté, open-vcm).
3. **Modèles de vision en aval** :
   - Détection d'objets : YOLO (v8/v11), Faster R-CNN, DETR.

---

## 4. Métriques d'Évaluation
- **Compression & Qualité Image/Vidéo** :
  - Bitrate (kbps)
  - PSNR / SSIM (optionnel pour la vision machine, mais utile en référence)
- **Tâche Aval** :
  - mAP (Mean Average Precision)
  - BD-Rate (Bjøntegaard Delta Rate) calculé par rapport au mAP (BD-mAP)
- **Énergie & Efficacité** :
  - Énergie consommée ($J$ ou $Wh$) par trame / par séquence
  - Puissance moyenne ($W$)
  - BD-Energy (variation d'énergie pour une précision donnée)
  - Complexité de calcul : FLOPs, MACs, temps d'inférence/encodage (FPS)

---

## 5. Environnement Matériel et Outils de Mesure
- **Hardware** : CPU (Intel/AMD) / GPU (NVIDIA CUDA)
- **Outils de mesure logicielle** :
  - CodeCarbon / PyJoules
  - `nvidia-smi` / NVML pour le GPU
  - Intel RAPL / `scaphandre` / `perf` pour le CPU
