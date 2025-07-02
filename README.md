# 🧠 MNIST App - Orchestrateur Fullstack

Ce dépôt regroupe l'infrastructure complète de l'application de reconnaissance de chiffres manuscrits MNIST, avec :
- Un backend FastAPI (mnist-backend)
- Un frontend Streamlit (mnist-frontend)

Le tout est orchestré via Docker Compose et les deux services sont inclus ici comme **sous-modules Git**.

---

## 📦 Dépôts utilisés (Submodules Git)
- 🔁 [mnist-backend](./mnist-backend) – API FastAPI avec modèle PyTorch
- 🎨 [mnist-frontend](./mnist-frontend) – Interface utilisateur Streamlit

---

## 🚀 Démarrage rapide

1. **Cloner le projet avec les sous-modules**

```sh
git clone --recurse-submodules <URL_DU_DEPOT_MNIST-APP>.git
cd mnist-app
```

2. **Lancer l'application avec Docker Compose**

```sh
docker compose up --build
```

3. **Accéder aux services**
- Frontend Streamlit : [http://localhost:8501](http://localhost:8501)
- Backend FastAPI (Swagger UI) : [http://localhost:8000/docs](http://localhost:8000/docs)

---

## 🛠️ Structure du projet
```
mnist-app/
├── mnist-backend/      # Sous-module : code et modèle backend (FastAPI)
├── mnist-frontend/     # Sous-module : code frontend (Streamlit)
├── docker-compose.yml  # Orchestration des deux services
├── TP - MNIST CNN.pdf  # Sujet du TP
└── README.md           # Ce fichier
```

---

## ℹ️ Notes importantes
- **Le backend et le frontend sont totalement séparés** et peuvent évoluer indépendamment.
- **Le backend** contient le modèle entraîné et l'API de prédiction.
- **Le frontend** permet de dessiner un chiffre et d'obtenir la prédiction via l'API.
- **Aucune dépendance Python n'est requise à la racine** (seulement Docker et Git).

---

## 👩‍💻 Pour les développeurs
- Pour mettre à jour les sous-modules :
  ```sh
  git submodule update --remote
  ```
- Pour travailler sur le backend ou le frontend, rendez-vous dans le dossier correspondant et suivez le README local.

---

## 📄 Sujet du TP
Le sujet complet est disponible dans le fichier `TP - MNIST CNN.pdf`.

---

## ✍️ Auteur
Vanelle beunkeu