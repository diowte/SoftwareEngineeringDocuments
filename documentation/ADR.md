# Architecture Decision Records ADR-<NN> — <Titre de la décision> 
**Date :** 2026-01-25 
**Décideurs :** Ahmad Errekab, Akram Boughlala  
**Contexte projet :** FCB ClubManager 
---

## 1. Contexte
- **Problème / besoin :** Le projet nécessite une application permettant de gérer un club de football (joueurs, entraîneurs, entraînements et statistiques) avec une interface simple, incluant la consultation des statistiques d’un joueur par sélection.
- **Contraintes :** <techniques, temps, équipe, outils>
- **Forces en présence :** Simplicité de développement, rapidité de mise en œuvre, facilité de maintenance, clarté du code

---

## 2. Décision
> Décrire la décision en 1–3 phrases.
- Nous choisissons : une application Desktop en C# avec Windows Forms, utilisant ADO.NET pour l’accès aux données.
- Pour : faciliter le développement rapide d’une interface graphique stable, adaptée à un projet 
---

## 3. Alternatives considérées
### Option A — ASP.NET WebForms
- **Avantages :** Application accessible via navigateur, Technologie connue dans certains cours
- **Inconvénients :**Développement plus long pour une petite équipe,Debug plus difficile

### Option B — <nom>
- **Avantages :** <...>
- **Inconvénients :** <...>

---

## 4. Justification (Pourquoi cette décision ?)
-Windows Forms permet un développement rapide avec configuration.
-La gestion des événements (clic sur un joueur > affichage des statistiques) est simple.
-L’outil est bien supporté par Visual Studio, utilisé dans le cours.

---

## 5. Conséquences
### Positives
- Développement rapide de l’interface graphique.

Facilité de maintenance et de compréhension du code.

Réduction des risques liés au temps et à la complexité.

### Négatives / Risques
- <...>

### Impact sur l’architecture / le code
- Interface (Forms) > Logique métier → Accès aux données (ADO.NET).

Utilisation de classes métiers claires (Joueur, Entraîneur, Entraînement, etc.).

---

## 6. Plan d’implémentation (court)
- Étape 1 : Création du projet Windows Forms et structure de base.

- Étape 2 : Implémentation des entités métiers et de la base de données.

- Étape 3 : Développement des interfaces (liste joueurs, détails joueur, statistiques).

---

## 7. Validation
- **Comment vérifier que c’est bon ?**
- L’application démarre sans erreur.

- L’utilisateur peut ajouter des joueurs et les afficher.

- Un clic sur un joueur affiche correctement ses statistiques.

- Les données sont correctement enregistrées en base.

---

## 8. Liens
- UML : <lien/nom de fichier>
- Issue/Tâche : <lien>
- Référence : <doc officiel / cours>
