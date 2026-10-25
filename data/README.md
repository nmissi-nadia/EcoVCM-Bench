# Gestion des Données (Data)

Ce répertoire contient les données vidéo brutes, les annotations pour les tâches de vision par ordinateur, ainsi que les caractéristiques intermédiaires extraites.

---

## 🗂 Organisation suggérée

```text
data/
├── raw_videos/              # Séquences vidéo sources non compressées (YUV, MP4 lossless)
├── annotations/             # Vérités terrain (formats COCO, MOT, YOLO, etc.)
└── features/                # Tenseurs / caractéristiques extraits pour le VCM
```

---

## 📥 Téléchargement des jeux de données
> **Remarque** : Ne pas versionner les fichiers vidéo volumineux directement dans Git. Utilisez Git LFS, un stockage distant (S3, Zenodo, Google Drive) ou des scripts de téléchargement automatique.

Exemple de script de téléchargement (à placer dans `scripts/`) :
```bash
python scripts/download_datasets.py --dataset visdrone --output data/raw_videos/
```
