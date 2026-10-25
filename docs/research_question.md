# Question de Recherche

## 1. Contexte & Problématique
La compression vidéo pour les machines (*Video Coding for Machines* - VCM) vise à encoder des flux visuels spécifiquement pour des algorithmes de vision par ordinateur (détection d'objets, suivi, segmentation) plutôt que pour la consommation humaine (HVS).

Bien que ces approches réduisent significativement le débit binaire requis, la question de leur **empreinte énergétique globale** (encodage, transmission, décodage, inférence) reste souvent sous-explorée. Les gains en débit binaire justifient-ils la surcharge calculatoire et énergétique sur les dispositifs terminaux ou serveurs ?

## 2. Question Principale
> **Dans quelle mesure les approches de Video Coding for Machines (VCM) permettent-elles d'atteindre un compromis optimal entre débit binaire, performance de la tâche aval (vision) et consommation énergétique globale (Edge + Cloud) ?**

## 3. Sous-questions de Recherche
1. **Consommation énergétique de l'encodeur vs décodeur :** Comment se répartit l'énergie entre les codecs traditionnels (AVC, HEVC, VVC), les codecs neuronaux de caractéristiques (Feature Compression) et les représentations compactes ?
2. **Impact sur les tâches avales :** Quel est le seuil de dégradation acceptable pour maintenir une précision suffisante (mAP, F1-score) tout en minimisant l'empreinte carbone/joule par trame ?
3. **Compromis Pareto :** Existe-t-il une frontière de Pareto multi-objectifs claire (Débit × Précision × Énergie) selon le profil matériel (Edge vs Serveur) ?

## 4. Hypothèses
- **H1 :** Certaines méthodes VCM réduisent le débit au détriment d'un coût énergétique de calcul disproportionné sur le nœud d'encodage (Edge).
- **H2 :** La compression de caractéristiques intermédiaires (*Feature Coding*) offre un meilleur ratio Énergie/Débit qu'un encodage pixel complet pour des scènes à dynamique modérée.
