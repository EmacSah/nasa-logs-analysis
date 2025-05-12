# Analyse des Logs Web NASA avec Elasticsearch et Machine Learning

Ce projet démontre l'analyse de logs web historiques de la NASA (juillet 1995) à l'aide d'Elasticsearch, Python et machine learning pour détecter automatiquement les comportements suspects et les anomalies.

## 🎯 Objectifs

- Traiter et analyser ~1.8 millions de lignes de logs web au format Common Log Format
- Concevoir un pipeline complet d'ingestion et d'indexation optimisé pour Elasticsearch
- Explorer les patterns de trafic et identifier les comportements anormaux
- Construire un modèle prédictif pour la détection automatique de comportements suspects
- Intégrer le modèle ML dans Elasticsearch pour inférence en temps réel

## 📊 Résultats clés

- Identification des IPs et domaines les plus actifs (dominance des serveurs prodigy.com)
- Détection de comportements suspects (rush.internic.net avec 340 requêtes/heure)
- Analyse des erreurs HTTP (97% d'erreurs 404)
- Modèle de classification capable de détecter les comportements anormaux avec 99.9% de précision

  

## 🛠️ Stack technique

- **Python 3.10+**: pandas, gzip, re, elasticsearch, tqdm, matplotlib, scikit-learn, xgboost
- **Elasticsearch 8.x**: indexation, requêtes, agrégations, ML
- **Google Colab/Drive**: exécution et stockage
- **Visualisation**: matplotlib, Kibana dashboards

## 📚 Structure du projet

1. **Setup et configuration** 
   - Configuration de l'environnement
   - Connexion Elasticsearch

2. **Exploration et parsing** 
   - Analyse de la structure des logs
   - Parsing et nettoyage des données

3. **Indexation Elasticsearch** 
   - Conception du mapping
   - Indexation par lots optimisée

4. **Analyse et exploration** 
   - Requêtes simples et complexes
   - Agrégations temporelles et statistiques

5. **Machine Learning** (extension)
   - Préparation des données d'entraînement
   - Modélisation et évaluation
   - Intégration à Elasticsearch

## 📈 Visualisations

![Nombre de requêtes par heure](graphs/graph_requetes_par_heure.png)
![Top 10 IPs](graphs/top_ips.png)
![Distribution des erreurs HTTP](graphs/http_errors_distribution.png)

## 🧠 Modèle machine learning

Trois modèles ont été comparés pour la détection de comportements suspects:
- Regression Logistique (baseline)
- Random Forest (performances parfaites sur ce dataset)
- XGBoost (excellentes performances, plus flexible)

Les caractéristiques utilisées incluent:
- Nombre de requêtes par IP/heure
- Proportion d'erreurs HTTP
- Nombre d'URLs uniques visitées
- Volume de données transférées

## 🚀 Comment utiliser ce projet

### Prérequis
- Python 3.10+
- Compte Elasticsearch Cloud ou cluster local
- Google Colab (recommandé) ou Jupyter Notebook


## Métriques de scalabilité
La conception modulaire permet une scalabilité horizontale:

- Capacité théorique de 100M+ logs/jour avec infrastructure appropriée
- Adaptabilité à différents environnements (cloud, on-premise)
- Compatible avec orchestrateurs comme Kubernetes ou Airflow

## Applicabilité en entreprise
Cette architecture peut être directement adaptée pour:


🔐 **Cybersécurité**

- Détection d'intrusions en temps réel
- Identification de comportements anormaux
- Analyse forensique post-incident


📈 **Monitoring d'infrastructure**

- Surveillance de performances applicatives
- Détection de défaillances système
- Analyse prédictive de problèmes potentiels


💡 **Analyse business**

- Monitoring de l'expérience utilisateur
- Détection de fraudes
- Analyse comportementale clients




 ## 📝Conclusion technique

Ce projet démontre comment les principes d'architecture scalable et DevOps peuvent 
être appliqués à l'analyse de données volumineuses. Les techniques d'optimisation 
implémentées permettent de:

- Maximiser l'efficacité des ressources
- Automatiser l'ensemble du workflow de données
- Garantir la scalabilité pour des volumes bien supérieurs
- Déployer des modèles ML en production de façon fiable

L'architecture présentée est transposable à de nombreux cas d'usage d'entreprise 
nécessitant l'analyse de données volumineuses et la détection d'anomalies en temps réel.

### Installation
```bash
pip install elasticsearch pandas tqdm matplotlib scikit-learn xgboost


