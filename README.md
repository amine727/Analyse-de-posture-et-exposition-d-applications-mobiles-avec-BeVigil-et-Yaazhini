# 📱 LAB 8 — Analyse de sécurité mobile (BeVigil & Yaazhini)


---

# 🧭 1. Objectif

Analyser la sécurité d’une application mobile Android (**InsecureBankv2**) en utilisant des outils d’analyse externe et interne.

---



# ⚙️ 2. Préparation de l’environnement

Création des dossiers nécessaires pour organiser le travail :

<img width="805" height="413" alt="2" src="https://github.com/user-attachments/assets/8cb5de7a-d4eb-4f9c-9ba1-8be320bc4374" />

---

# 📦 4. Installation de l’application

Application testée : **InsecureBankv2**

<img width="311" height="572" alt="3" src="https://github.com/user-attachments/assets/8de91bdc-a7d7-488f-97be-0d6111358830" />

---

# 🔐 5. Calcul du Hash SHA-256

Commande utilisée :

```powershell
Get-FileHash "InsecureBankv2.apk" -Algorithm SHA256
```

Résultat du hash :

<img width="1471" height="210" alt="4" src="https://github.com/user-attachments/assets/65ed137f-0fc8-4c60-892b-8423e25a4ed0" />

---

# 🌐 6. Analyse avec BeVigil

Analyse de l’exposition externe de l’application.

Résultats observés :

* Stockage de données sensibles
* Informations sensibles dans les logs
* Activity exportée
* Secret potentiel détecté
* Utilisation de HTTP non sécurisé

<img width="1776" height="713" alt="5" src="https://github.com/user-attachments/assets/887d4f28-e286-40d1-8f58-b5b9b637330f" />

---

# 🔍 7. Analyse avec Yaazhini

Analyse interne de l’APK.

Informations détectées :

* Package : com.android.insecurebankv2
* Version : 1.0
* Min SDK : 15
* Target SDK : 22

<img width="1406" height="722" alt="6" src="https://github.com/user-attachments/assets/6f5c8015-874a-4704-9fc0-2f033973292f" />

---

# 📊 8. Triage des vulnérabilités

Regroupement et analyse des résultats obtenus.

Objectifs :

* Identifier les doublons
* Classer les vulnérabilités
* Associer aux standards OWASP


---

# ⚠️ 9. Vulnérabilités principales

* Stockage de données sensibles
* Logs contenant des informations critiques
* Communication HTTP non sécurisée
* SDK obsolète
* Composants exportés

---

# 🛡️ 10. Recommandations

* Chiffrer les données sensibles
* Supprimer les logs en production
* Utiliser HTTPS
* Mettre à jour le SDK
* Restreindre les composants exposés

---

# 📌 11. Conclusion

L’application présente plusieurs vulnérabilités liées à la gestion des données et aux communications réseau.
Une amélioration des pratiques de sécurité est nécessaire.

---
