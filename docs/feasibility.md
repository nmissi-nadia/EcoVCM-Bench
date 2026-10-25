# Analyse de Faisabilité & Calendrier

## 1. Contraintes & Ressources
- **Calcul & GPU** : Capacité mémoire (VRAM) et temps d'exécution requis pour les benchmarks.
- **Accès aux capteurs d'énergie** : Disponibilité des interfaces matérielles (RAPL sur CPU, NVML sur GPU). Attention aux restrictions sous machines virtuelles ou conteneurs sans privilèges.
- **Stockage** : Volume des vidéos brutes, flux compressés et logs.

---

## 2. Analyse des Risques & Solutions de repli
| Risque | Impact | Probabilité | Solution de mitigation |
| :--- | :--- | :--- | :--- |
| Mesures d'énergie instables / bruitées | Élevé | Moyenne | Répétition des mesures ($N \ge 5$ runs), état stable, isolation des processus parasites. |
| Temps d'encodage excessif (ex: VTM) | Moyen | Élevée | Réduire la taille de l'échantillon ou utiliser des profils prédéfinis plus rapides (preset *fast* / *medium*). |
| Incompatibilité de bibliothèques VCM | Moyen | Moyenne | Utiliser des environnements virtuels isolés (Docker / venv / conda). |

---

## 3. Jalons & Calendrier Prévisionnel
- **Phase 1 : Initialisation & Bibliographie**
  - Validation de la question de recherche et des baselines.
  - Mise en place du pipeline d'acquisition des métriques énergétiques.
- **Phase 2 : Implémentation du Banc de Test**
  - Intégration des codecs de référence (FFmpeg/HEVC/VVC).
  - Intégration du modèle de vision aval (ex. YOLO/Faster R-CNN).
- **Phase 3 : Campagne Expérimentale**
  - Exécution des mesures (Débit, Précision, Joules).
  - Validation des résultats et analyses de sensibilité.
- **Phase 4 : Analyse, Tracés & Rapport**
  - Tracé des courbes Pareto (RD et Energy-Rate/Energy-Accuracy).
  - Rédaction du rapport et synthèse finale.
