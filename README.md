#Assistant éductif en mathématique troisième

---

````markdown
# 📚 Assistant Éducatif avec FastAPI & RAG (Gemini + FAISS)

Ce projet est une API FastAPI qui utilise la technique du Retrieval-Augmented Generation (RAG) avec les modèles Gemini (Google Generative AI), FAISS pour l'indexation, et PyPDF2 pour l'analyse de documents PDF. Il est conçu pour répondre à des questions pédagogiques en se basant sur des documents uploadés.

## 🚀 Fonctionnalités principales

- Upload de fichiers PDF
- Extraction et indexation de texte
- Génération de réponses pédagogiques à partir de questions
- Utilisation de Gemini (Google Generative AI)
- Mémoire conversationnelle (optionnelle)

---

## 🧰 Prérequis

- Python 3.10 ou version supérieure
- Git
- Une clé d'API Google Generative AI (Gemini)

---

## 📦 Installation

### 1. Cloner le projet

```bash
git clone git@github.com:Adonislab/S.ai.git
cd S.ai

````


### 2. Créer un environnement virtuel

```bash
python -m venv venv
source venv/bin/activate  # Sur Windows : venv\Scripts\activate
```

### 3. Installer les dépendances

```bash
pip install -r requirements.txt
```

### 4. Configurer les variables d’environnement

Crée un fichier `.env` à la racine du projet et ajoute ta clé Google :

```env
GOOGLE_API_KEY=ta_clé_google_genai
```

---

## ▶️ Lancer le serveur FastAPI

```bash
uvicorn main:app --reload
```

* Accès à l’API : [http://localhost:8000](http://localhost:8000)
* Swagger UI (documentation interactive) : [http://localhost:8000/docs](http://localhost:8000/docs)
* Redoc : [http://localhost:8000/redoc](http://localhost:8000/redoc)

---

## 📂 Structure du projet (exemple)

```
📁 mon_projet/
│
├── main.py
├── requirements.txt
├── .env
├── faiss_index/  # Généré automatiquement
```

---

## ✅ Exemples d’utilisation

### 🔸 Upload de fichiers PDF

```
POST /upload_pdfs
```

* Formulaire avec fichiers (clé `pdf_files[]`)

### 🔸 Poser une question

```
POST /ask_question
Content-Type: application/json

{
  "question": "Explique le théorème de Thalès",
  "user_id": "eleve_123"
}
```

---

## 🧠 Auteurs

* **Nom** : NOBIME Tanguy Adonis
* 📧 Email : [ton.email@example.com](mailto:nobimetanguy19@gmail.com)

---

## 🛡️ Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus d’informations.

