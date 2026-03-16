# TP-8 — API REST avec Spring Boot & Swagger

Travail pratique n°8 — Développement d'une API RESTful avec Spring Boot, Spring Data JPA et documentation Swagger / OpenAPI.

---

## Technologies utilisées

- Java
- Spring Boot
- Spring Data JPA
- Swagger / OpenAPI 3.1 (SpringDoc)
- Maven

---

## Lancer le projet

```bash
# Cloner le repo
git clone https://github.com/Khadim1511/TP-8-Spring-Boot.git
cd TP-8-Spring-Boot

# Lancer l'application
./mvnw spring-boot:run
```

L'application démarre sur : `http://localhost:8089`

---

## Documentation Swagger

Une fois l'application lancée, accéder à l'interface Swagger UI :

```
http://localhost:8089/swagger-ui/index.html
```

---

## Endpoints disponibles

| Méthode | Endpoint | Description |
|---|---|---|
| GET | `/students` | Récupérer tous les étudiants |
| POST | `/students` | Créer un nouvel étudiant |
| GET | `/students/{id}` | Récupérer un étudiant par ID |
| PUT | `/students/{id}` | Modifier un étudiant |
| DELETE | `/students/{id}` | Supprimer un étudiant |
| GET | `/profile` | Infos du profil |
| GET | `/profile/students` | Profil des étudiants |

---

## Tests Swagger

### 1. Interface Swagger — Endpoints disponibles

Après configuration, Swagger liste tous les endpoints du `student-entity-controller` et du `profile-controller`.

1

---

### 2. POST /students — Requête (étudiant 1)

Création de l'étudiante **Sara El Amrani** avec les champs : `firstName`, `lastName`, `email`, `major`, `age`.

2

---

### 3. POST /students — Réponse 201 Created (étudiant 1)

Le serveur retourne un code **201** avec le corps de l'étudiant créé et les liens HAL.

3
---

### 4. GET /students/{id} — Requête avec id=1

Récupération de l'étudiant avec l'identifiant **1**.

4
---

### 5. GET /students/{id} — Réponse 200 (étudiant 1)

Le serveur retourne un code **200** avec les données de Sara El Amrani.

5

---

### 6. POST /students — Requête (étudiant 2)

Création de l'étudiant **Youssef Alaoui** (major : Mathématiques, age : 20).

6

---

### 7. GET /students/{id} — Réponse 200 (étudiant 2)

Récupération de Youssef Alaoui via l'id **2** — réponse 200 avec les liens HAL.

7
---

## Auteur

**Khadim** — [GitHub](https://github.com/Khadim1511)
