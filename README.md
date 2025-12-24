# RNN-music-abc

TP : Réseaux récurrents (RNN/LSTM) — Génération de musique en notation ABC avec PyTorch.

## Objectif
Apprendre un modèle LSTM à prédire le prochain caractère d’une partition en notation ABC, puis générer de nouvelles séquences musicales.

## Contenu
- `tp-rnn.ipynb` : notebook complet du TP (chargement des données, prétraitement, dataset PyTorch, modèle LSTM, entraînement, génération).
- Dataset : partitions irlandaises au format ABC (train/validation).

## Étapes principales
1. Chargement & exploration des données (`train.json`, `validation.json`)
2. Prétraitement : vocabulaire (95 caractères), mapping, vectorisation, padding
3. Dataset PyTorch : création des couples (x, y) décalés d’un caractère
4. Modèle `MusicRNN` : Embedding + LSTM + couche linéaire
5. Entraînement : CrossEntropy, TensorBoard, early stopping, sauvegarde du meilleur modèle
6. Génération : échantillonnage (sampling) avec température

## Exécution
Ouvrir `tp-rnn.ipynb` et exécuter les cellules dans l’ordre.  
Le modèle sauvegardé est utilisé ensuite pour générer une séquence ABC (200 caractères).
