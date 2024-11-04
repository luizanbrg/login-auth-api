## API d'Authentification et de Connexion en Java

Ce projet est une page d'authentification et de connexion développée en Java, utilisant le framework Spring Boot.

**Structure du projet**
La structure du projet est la suivante :
```
src
├── main
    ├── java
    │   └── com
    │       └── loginauthapi
    │           ├── controllers
    │           │   ├── AuthController.java
    │           │   └── UserController.java
    │           ├── domain
    │           │   └── user
    │           │       └── User.java
    │           ├── dto
    │           │   ├── LoginRequestDTO.java
    │           │   ├── RegisterRequestDTO.java
    │           │   └── ResponseDTO.java
    │           ├── infra
    │           │   └── security
    │           │       ├── cors
    │           │       │   └── CorsConfig.java
    │           │       ├── CustomerUserDetailsService.java
    │           │       ├── SecurityConfig.java
    │           │       ├── SecurityFilter.java
    │           │       └── TokenService.java
    │           ├── repositories
    │           │   └── UserRepositories
    │           └── LoginAuthApiApplication.java
    └── resources
        └── application.properties
```

### Fonctionnalités principales

- Inscription d'utilisateurs
- Connexion d'utilisateurs
- Authentification basée sur JWT (JSON Web Tokens)
- Gestion des rôles utilisateurs

**Technologies utilisées**
- Java
- Spring Boot
- Spring Security
- Spring Data JPA
- JWT pour l'authentification

### Dépendances

Les dépendances suivantes sont nécessaires et doivent être ajoutées au fichier `pom.xml` :  
- Spring Boot Starter Web: Gère les requêtes et réponses HTTP.

- Spring Boot Starter Security: Fournit des fonctionnalités de sécurité telles que l'authentification et l'autorisation.

- Spring Boot Starter Data JPA: Active l'utilisation de l'API de persistance Java (JPA) avec Spring Data pour l'accès aux bases de données.

- Spring Boot Starter Test: Fournit les dépendances nécessaires pour tester les applications Spring Boot.

- Spring Security Test: Ajoute des fonctionnalités de test pour les applications sécurisées avec Spring Security.

- JWT Library: Utilisée pour créer et vérifier les JSON Web Tokens (JWT) pour l'authentification.

- Password Encoder: Fournit des utilitaires pour le chiffrement des mots de passe.

- Lombok: Une bibliothèque Java qui aide à réduire le code répétitif en utilisant des annotations.

### Utilisation

**End-points**

- **POST /auth/login** : Authentification de l'utilisateur  
  - Corps de la requête : `LoginRequestDTO`
  - Réponse : `ResponseDTO` avec le nom de l'utilisateur et le token JWT

- **POST /auth/register** : Enregistrement de l'utilisateur  
  - Corps de la requête : `RegisterRequestDTO`
  - Réponse : `ResponseDTO` avec le nom de l'utilisateur et le token JWT
