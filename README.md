# Gestion des Utilisateurs - CRUD React + Express + SQLite

Application web simple permettant de gérer des utilisateurs (Créer, Lire, Modifier, Supprimer) avec :

- Frontend : React.js (Vite)
- Backend : Express.js
- Base de données : SQLite
- Communication API : Axios

---

## Fonctionnalités

- Ajouter un utilisateur
- Afficher la liste des utilisateurs
- Modifier un utilisateur
- Supprimer un utilisateur
- Stockage des données dans SQLite

---

## Technologies utilisées

### Frontend

- React.js
- Vite
- Axios
- CSS

### Backend

- Node.js
- Express.js
- SQLite (better-sqlite3)
- CORS
- Nodemon

---

## Structure du projet

```text
gestion-utilisateurs/
│
├── backend/
│   ├── database/
│   │   └── database.js
│   │
│   ├── routes/
│   │   └── userRoutes.js
│   │
│   ├── database.db
│   ├── server.js
│   └── package.json
│
└── frontend/
    ├── src/
    │   ├── components/
    │   │   ├── UserForm.jsx
    │   │   └── UserList.jsx
    │   │
    │   ├── App.jsx
    │   ├── App.css
    │   └── main.jsx
    │
    └── package.json
```

---

## Installation

### 1. Cloner le projet

```bash
git clone <url-du-repository>
```

```bash
cd gestion-utilisateurs
```

---

## Installation du Backend

Accéder au dossier backend :

```bash
cd backend
```

Installer les dépendances :

```bash
npm install
```

Ou :

```bash
npm install express cors better-sqlite3
npm install nodemon --save-dev
```

Lancer le serveur :

```bash
npm run dev
```

Le serveur sera accessible sur :

```text
http://localhost:5000
```

---

## Installation du Frontend

Accéder au dossier frontend :

```bash
cd frontend
```

Installer les dépendances :

```bash
npm install
```

Installer Axios :

```bash
npm install axios
```

Lancer l'application :

```bash
npm run dev
```

Le frontend sera accessible sur :

```text
http://localhost:5173
```

---

## API REST

### Récupérer tous les utilisateurs

```http
GET /api/users
```

### Récupérer un utilisateur

```http
GET /api/users/:id
```

### Ajouter un utilisateur

```http
POST /api/users
```

Body :

```json
{
  "name": "Hanane",
  "email": "hanane@gmail.com"
}
```

### Modifier un utilisateur

```http
PUT /api/users/:id
```

Body :

```json
{
  "name": "Hanane Updated",
  "email": "hanane2@gmail.com"
}
```

### Supprimer un utilisateur

```http
DELETE /api/users/:id
```

---

## Base de données

La base SQLite est automatiquement créée au démarrage du serveur :

```text
database.db
```

Table :

```sql
CREATE TABLE users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    email TEXT NOT NULL UNIQUE
);
```

---

## Auteur

Projet réalisé dans le cadre de l'apprentissage du développement Full Stack avec React.js, Express.js et SQLite.
