#  Recette App – Application Web de Gestion des Recettes et Ingrédients

## Description

**Recette App** est une application web développée pour permettre la gestion des recettes culinaires et des ingrédients dans un environnement sécurisé et multi-utilisateur.

L'application permet aux chefs de gérer leurs recettes, leurs ingrédients et leurs informations nutritionnelles, tandis qu'un administrateur assure la gestion et la validation des comptes utilisateurs.

Le projet intègre également des dashboards permettant de visualiser différentes statistiques liées aux recettes, aux ingrédients et aux informations nutritionnelles.

---

##  Objectifs du projet

- Gérer les recettes culinaires
- Gérer les ingrédients et leurs valeurs nutritionnelles
- Associer plusieurs ingrédients à une recette avec leurs quantités
- Calculer les calories totales et les calories par personne
- Séparer les données de chaque chef
- Gérer les utilisateurs et les rôles
- Visualiser les statistiques à travers des dashboards
- Assurer la sécurité et l'autorisation des utilisateurs

---

##  Gestion des utilisateurs

L'application possède deux rôles principaux :

###  Administrateur

- Consulter les comptes des chefs
- Valider les comptes
- Supprimer un compte chef

### Chef

- Créer ses ingrédients
- Modifier et supprimer ses ingrédients
- Créer ses recettes
- Modifier et supprimer ses recettes
- Consulter ses propres dashboards

La séparation des données est assurée grâce au champ `ChefId`, permettant à chaque chef d'accéder uniquement à ses propres données.

---

##  Technologies utilisées

| Technologie | Utilisation |
|---|---|
| C# | Langage principal |
| Blazor Server | Interface web interactive |
| ASP.NET Core | Backend et gestion de l'application |
| Entity Framework Core | ORM et accès aux données |
| SQLite | Base de données |
| ASP.NET Identity | Authentification et gestion des rôles |
| Radzen | Composants et dashboards |
| Bootstrap | Design responsive |

---

##  Architecture

Le projet suit une architecture en couches permettant de séparer les responsabilités :

### Presentation Layer

Gestion des pages Blazor, formulaires, listes, menus et dashboards.

### Services Layer

Gestion de la logique métier et des opérations CRUD.

Services principaux :

- `IngredientService`
- `RecipeService`

### Data Layer

Gestion de :

- `AppDbContext`
- Modèles
- Migrations
- Base de données SQLite

---

##  Base de données

Les principales entités du projet sont :

- `Recipe`
- `Ingredient`
- `RecipeIngredient`
- `IdentityUser`
- `IdentityRole`

La relation entre les recettes et les ingrédients est une relation **Many-to-Many**, avec la quantité utilisée dans `RecipeIngredient`.

---

##  Dashboards

L'application contient deux dashboards principaux.

### Dashboard des ingrédients

Il permet notamment de visualiser :

- Nombre total d'ingrédients
- Calories moyennes
- Calories minimales et maximales
- Répartition par catégorie
- Top 10 des ingrédients les plus caloriques
- Protéines
- Glucides
- Lipides
- Fibres

### Dashboard des recettes

Il permet de visualiser :

- Nombre total de recettes
- Répartition par catégorie
- Répartition par type de cuisine
- Calories moyennes par personne
- Comparaison des calories par catégorie

---

##  Sécurité

La sécurité repose notamment sur :

- ASP.NET Identity
- Gestion des rôles `Admin` et `Chef`
- Authentification
- Autorisation des pages
- Validation des comptes chefs
- Séparation des données par `ChefId`
- Protection contre la modification des données d'un autre chef

---

## ⚙️ Fonctionnalités principales

- 🔐 Authentification
- 👥 Gestion des utilisateurs
- 👨‍🍳 Gestion des chefs
- 🥕 CRUD des ingrédients
- 🍲 CRUD des recettes
- 🔗 Association recettes / ingrédients
- 🖼️ Upload des images
- 🔎 Recherche et filtrage
- 📊 Dashboards statistiques
- 🔒 Gestion des rôles et autorisations

---

##  Rapport du projet

Le rapport détaillé du projet est disponible ici :

 **[📘 Consulter le rapport du projet](./Rapport_App_Recette.pdf)**

---

##  Perspectives d'amélioration

Le projet peut être enrichi avec :

- Export PDF
- Notifications
- API REST
- Recommandations nutritionnelles intelligentes
- Nouvelles fonctionnalités analytiques

---

##  Projet

**Recette App**  
Application Web de Gestion des Recettes et Ingrédients

Développée avec **C# / Blazor Server / ASP.NET Core / Entity Framework Core / SQLite / ASP.NET Identity**.
