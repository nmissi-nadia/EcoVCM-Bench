# EcoVCM-Bench

**EcoVCM-Bench** est un benchmark dédié à l'évaluation écologique et aux compromis efficacité énergétique / débit / précision des méthodes de compression vidéo orientées machines (Video Coding for Machines - VCM).

---

## 📁 Structure du projet

```text
EcoVCM-Bench/
├── README.md                     # Présentation générale du projet et guide d'exécution
├── docs/                         # Documentation académique et scientifique
│   ├── research_question.md      # Question de recherche et problématique
│   ├── experimental_protocol.md  # Protocole expérimental et métriques
│   └── feasibility.md            # Analyse de faisabilité et calendrier
├── configs/                      # Fichiers de configuration des expériences
│   └── vcm_experiments.yaml      # Paramètres des codecs, modèles et métriques
├── data/                         # Gestion des jeux de données et annotations
│   └── README.md                 # Instructions de téléchargement et organisation
├── scripts/                      # Scripts d'exécution, d'évaluation et d'automatisation
├── results/                      # Résultats des benchmarks
│   ├── raw/                      # Métriques brutes (logs, mesures d'énergie, etc.)
│   └── processed/                # Résultats agrégés et résumés (CSV, JSON)
└── figures/                      # Courbes RD/Energy, graphiques et visualisations
```

---

## 🚀 Démarrage rapide

### 1. Prérequis
- Python 3.10+
- Outils de profiling énergétique (selon plateforme : `CodeCarbon`, `PyJoules`, `RAPL`, `nvidia-smi`)
- Codecs vidéo usuels (ex: FFmpeg, VTM, libvpx) et frameworks de Deep Learning (PyTorch, torchvision)

### 2. Installation
```bash
git clone <url-du-repo>
cd EcoVCM-Bench
# python -m venv venv
# source venv/bin/activate  # Sous Linux/Mac ou .\venv\Scripts\activate sous Windows
# pip install -r requirements.txt
```

---

## 📊 Documentation
Consultez le dossier `docs/` pour plus de détails sur le protocole et la question de recherche :
- [docs/research_question.md](file:///c:/Users/Lenovo/Documents/Master/M2/TDMA/Projet/EcoVCM-Bench/docs/research_question.md)
- [docs/experimental_protocol.md](file:///c:/Users/Lenovo/Documents/Master/M2/TDMA/Projet/EcoVCM-Bench/docs/experimental_protocol.md)
- [docs/feasibility.md](file:///c:/Users/Lenovo/Documents/Master/M2/TDMA/Projet/EcoVCM-Bench/docs/feasibility.md)
