# Fiche de défense des références

Article : *Déploiement continu multi-applications sur un serveur unique : architecture de référence conteneurisée et garde d'idempotence par empreinte cryptographique pour la restauration des bases de données*

<div align="justify">

## La logique générale du choix

On préfère, dans l'ordre :

* la **source primaire**, celle qui a inventé ou défini la chose (Accelerate pour DORA, RFC 8555 pour ACME) ;
* un travail **évalué par les pairs** plutôt qu'un blog ;
* une **revue systématique** quand on veut résumer tout un domaine en une citation ;
* l'**ouvrage fondateur** reconnu par la communauté.

## Référence par référence

| Réf. | Ce qu'elle apporte à l'article | Pourquoi celle-là |
| --- | --- | --- |
| [1] Humble & Farley | Définit le *deployment pipeline* : chaque commit traverse une chaîne automatisée jusqu'à une version déployable. Le chapitre sur l'anatomie du pipeline est le plus utile ici. | C'est le livre qui a nommé et formalisé le concept. |
| [2] Shahin et al. | Revue systématique de la CI/CD : approches, outils, difficultés. Elle note le manque de travaux sur les contextes contraints. | Une seule citation résume tout le domaine, et elle justifie l'angle « petite structure ». |
| [3] Accelerate | Définit les 4 indicateurs DORA à partir d'enquêtes statistiques. | Source originale des indicateurs DORA. |
| [4] Leite et al. | Panorama des concepts et difficultés DevOps, surtout en infrastructure distribuée. | Survey publié dans ACM Computing Surveys, revue de référence. Il montre que la littérature vise surtout le distribué. |
| [5] Morris | La dérive de configuration et les serveurs « flocons de neige » impossibles à reproduire. | Ouvrage de référence de l'Infrastructure as Code. |
| [6] Meli et al. | Mesure à grande échelle des secrets (clés API, mots de passe) qui fuient dans les dépôts GitHub publics. | Preuve empirique, pas une simple opinion. Elle justifie la règle « secrets uniquement sur l'hôte ». |
| [7] Hilton et al. | Coûts et bénéfices réels de la CI, mesurés sur des milliers de projets libres. | Données réelles plutôt que promesses. |
| [8] Merkel | Présente Docker comme moyen d'avoir le même environnement en développement et en production. | Citation académique classique pour introduire Docker. |
| [9] Felter et al. (IBM) | Les conteneurs ont des performances proches du natif, meilleures que les machines virtuelles. | Benchmark rigoureux qui répond à l'objection « Docker, c'est lourd ». |
| [10] Combe et al. | Appartenir au groupe `docker` équivaut à être root. | Analyse de sécurité académique qui soutient la section 5.2. |
| [11] Shu et al. | Les images de Docker Hub, y compris officielles, contiennent souvent des vulnérabilités connues. | Étude empirique. Elle justifie la piste du registre signé. |
| [12] Rahman et al. | Sept « mauvaises odeurs » de sécurité dans les scripts d'infrastructure, dont les mots de passe en dur. | Article primé à ICSE. Il nomme précisément le problème de P3. |
| [13] Twelve-Factor | Facteur III : la configuration est stockée dans l'environnement, pas dans le code. | Référence pratique incontournable, signalée honnêtement comme littérature grise. |
| [14] RFC 8555 | Définit le protocole ACME et le défi HTTP-01. | La norme officielle elle-même. |
| [15] Aas et al. | Conception et impact de Let's Encrypt, écrit par ses créateurs. | Source primaire et évaluée par les pairs. |
| [16] RFC 8446 | Définit TLS 1.3, mais ne parle pas de la gratuité des certificats. | **À retirer de la phrase où elle est citée** : [14] et [15] suffisent. |
| [17] Rajapakse et al. | Difficultés et solutions DevSecOps, dont le manque de compétences. | Revue récente (2022) qui complète [4] côté sécurité. |
| [18] Hevner et al. | Les 7 principes de la design science : artefact, pertinence, évaluation rigoureuse. | Article fondateur de cette méthode, l'un des plus cités du domaine. |
| [19] RFC 5737 | Réserve des plages d'adresses IP pour la documentation, dont 203.0.113.0/24. | Justifie l'adresse 203.0.113.10 : la vraie IP n'est pas publiée. |
| [20] FIPS 180-4 | Définit officiellement SHA-256. | Norme officielle du NIST. |
| [21] Doc Docker | Explique que les règles iptables de Docker passent avant celles d'UFW. | Source primaire : le comportement est reconnu par Docker lui-même. |
| [22] Saltzer & Schroeder | Énonce le principe de moindre privilège parmi 8 principes de conception sécurisée. | Texte historique fondateur, encore cité aujourd'hui. |
| [23] Flyway | Enregistre une somme de contrôle par migration pour ne pas la rejouer. | Travail antérieur le plus proche de la garde d'idempotence : le citer montre ce qui est repris et ce qui est nouveau. |
| [24] Liquibase | Même principe, avec la table DATABASECHANGELOG. | Deuxième outil de référence du même type, pour montrer que le principe est établi. |

</div>