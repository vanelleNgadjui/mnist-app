# Reconnaissance de chiffres manuscrits (MNIST)

Ce projet propose une application complète de reconnaissance de chiffres manuscrits basée sur le dataset MNIST, avec un modèle CNN entraîné sous PyTorch, une API FastAPI pour la prédiction, et une interface utilisateur Streamlit.

## Présentation
- **Modèle** : Réseau de neurones convolutif (CNN) entraîné sur MNIST.
- **API** : FastAPI pour exposer un endpoint de prédiction.
- **Interface** : Application Streamlit permettant de dessiner un chiffre et d'obtenir la prédiction en temps réel.

## Installation et dépendances

1. **Cloner le dépôt**
```bash
git clone <votre-url-git>
cd TP-mnist
```

2. **Créer un environnement virtuel**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

3. **Installer les dépendances**
```bash
pip install -r requirements.txt
```

## Lancer l'API FastAPI
Dans un premier terminal :
```bash
uvicorn src.app.api:app --reload
```
L'API sera accessible sur http://127.0.0.1:8000

## Lancer l'interface Streamlit
Dans un second terminal :
```bash
streamlit run src/app/streamlit_app.py
```
L'application s'ouvrira dans votre navigateur par défaut.

## Exemple d'utilisation
1. Dessinez un chiffre (0-9) dans la zone prévue à gauche.
2. Cliquez sur **Prédire** pour obtenir la reconnaissance automatique.
3. Le chiffre prédit, le top-3 des probabilités et un graphique de confiance s'affichent à droite.
4. Utilisez le bouton **Effacer** pour recommencer.

![Aperçu de l'application](notebook/screenshot_demo.png)

## Structure du projet
- `src/app/api.py` : API FastAPI pour la prédiction.
- `src/app/streamlit_app.py` : Interface utilisateur Streamlit.
- `model/mnist-0.0.1.pt` : Modèle CNN entraîné.
- `requirements.txt` : Dépendances Python.

## Remarques
- Le modèle est entraîné sur MNIST, il est donc optimisé pour des chiffres manuscrits simples.
- Pour toute question ou amélioration, n'hésitez pas à ouvrir une issue ou à proposer une pull request. 