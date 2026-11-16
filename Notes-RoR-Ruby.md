# Objectif : une analyse du langage, métriques et choses intéressantes pour faire un comparatif des différents langages
## Groupe évalué :
Rayane Alli
Ilyas Ait ali
Maria

## Technologie abordée : RoR

## Notes - Présentation : langage proche du langage naturel, réalisé pour simplifier le travail

Trois principes Ruby :
- Developer happiness (conçu pour le plaisir du développeur)
- Principe de moindre surprise (noms de méthodes explicites)
- Convention over configuration (utilise des conventions pour écrire moins de code)
Ils expliquent : pourquoi une ligne ruby se lit souvent comme une phrase

En ruby, tout est objet (nil, true et false, et même les entiers le sont aussi)

Explication technique des points basiques du langage parcourus

Écosystème de Ruby :
on utilise la bibliothèque “gem” pour ajouter des fonctionnalités

Exemple en live de la syntaxe en écrivant un code de base

Kahoot un peu trop technique, et manque d’explication après les réponses

Explication précise de “convention over configuration”, en expliquant ce que le framework Rails réalise en traduction code et technique (exemple class User -> table users, et autres)

Explication du framework et des exemples du routeur, contrôleur, modèle à la vue en elle-même, avec des responsabilités et façons de coder différentes

Analyse développée des limites et de la sécurité qu’offre Ruby et Rails


## Notes - TP : ajout de la fonctionnalité de dépenses sur leur application Splitly

Organisation du TP sous forme de petites missions progressives guidées par des tests

Mise en pratique directe de l'architecture MVC vue pendant la présentation :
- La donnée avec le modèle et la base
- Le contrôleur et les routes pour faire le lien
- Les vues pour rendre le tout visible et utilisable

Démonstration concrète de la "magie" des conventions Rails :
- Très peu de lignes de code suffisent pour générer des tables et des formulaires complets
- Rails fait le lien tout seul entre les noms au pluriel et au singulier

Bonne sensibilisation à la sécurité dans le code :
- Ils insistent sur le fait de ne jamais faire confiance aux formulaires et de valider les droits côté serveur

Découverte de la console interactive pour tester son code en direct sans recharger l'application

Approche par les tests (TDD) : agréable de voir le test rouge passer au vert quand le code est bon

Sensibilisation à la performance :
- Comparaison entre laisser Ruby tout calculer en mémoire et laisser la base de données faire le calcul directement

Livret de TP bien structuré :
- Des questions d'observation pour faire réfléchir plutôt que juste copier du code
- Présence d'indices et des solutions en fin de document pour éviter que certains restent bloqués

Le groupe passe dans les rangs pour aider et expliquer quand des personnes sont bloquées



## Notes avantages et faiblesses de Ruby / RoR

Points forts (Forces) :
- Vitesse de développement et Time to Market : idéal pour sortir un MVP rapidement grâce aux conventions qui évitent le code répétitif
- Syntaxe lisible et expressive, proche du langage naturel (Developer Happiness, Principe de moindre surprise)
- Modèle "tout objet" (même les entiers, nil, true et false sont des objets)
- Framework "tout-en-un" : ORM (ActiveRecord), base de données, migrations, sécurité et tests intégrés dès l'installation
- Sécurité native robuste : CSRF, injections SQL (requêtes préparées), Strong Parameters et scanner statique intégré (Brakeman)
- Écosystème mature (+25 ans) et riche (+180 000 gems via Bundler)
- Console interactive (rails console) très pratique pour tester et débugger en direct

Points faibles (Limites) :
- Performances d'exécution et mémoire inférieures à des technos compilées (Go, Rust, Java) ou Node.js sur du calcul intensif
- Moins adapté aux calculs lourds (CPU) ou au traitement massif en temps réel
- Piège de performance classique de l'ORM : le problème N+1 sur les requêtes (oblige à utiliser `includes` et à penser SQL dès que le volume grandit)
- Monolithe par défaut : rapide à lancer, mais coûteux et complexe à faire évoluer vers une architecture microservices
- Effet "boîte noire" : beaucoup de magie et de conventions implicites, parfois déroutant pour débugger au début
- Typage dynamique : les erreurs n'apparaissent qu'au runtime, exigeant une couverture de tests très stricte
- Communauté et marché plus restreints aujourd'hui face à l'essor de TypeScript/Node et Python