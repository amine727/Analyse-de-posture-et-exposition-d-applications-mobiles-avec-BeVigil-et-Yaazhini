\# Analyse BeVigil — InsecureBankv2



\## Informations générales



\* Application: InsecureBankv2

\* Package: com.android.insecurebankv2

\* Score de sécurité: 7.4 (Average)

\* Nombre total d’issues: 5



\---



\## Vulnérabilités identifiées



\### 1. Storage of sensitive information in Shared Preferences



\* Sévérité: Medium

\* Description: Des données sensibles sont stockées en clair dans les SharedPreferences.

\* Impact: Un attaquant peut récupérer ces données en cas d’accès au device.

\* Recommandation: Chiffrer les données sensibles avant stockage.



\---



\### 2. Sensitive Information in Logs



\* Sévérité: Medium

\* Description: Des informations sensibles sont écrites dans les logs.

\* Impact: Un attaquant peut accéder aux logs et récupérer des données critiques.

\* Recommandation: Supprimer les logs sensibles en production.



\---



\### 3. Exported Activity



\* Sévérité: Low

\* Description: Une activité Android est exposée (exported).

\* Impact: Peut être appelée par d’autres applications malveillantes.

\* Recommandation: Restreindre l’accès avec permissions.



\---



\### 4. Possible Secret Detected



\* Sévérité: Low

\* Description: Présence possible de secrets dans le code.

\* Impact: Risque d’accès non autorisé aux services backend.

\* Recommandation: Stocker les secrets de manière sécurisée.



\---



\### 5. Insecure HTTP Client Used



\* Sévérité: Low

\* Description: Utilisation de requêtes HTTP non sécurisées.

\* Impact: Risque d’interception des données (MITM).

\* Recommandation: Utiliser HTTPS uniquement.



\---



\## Conclusion



L’application présente plusieurs faiblesses liées à la gestion des données sensibles et à la sécurité des communications. Une attention particulière doit être portée au stockage sécurisé et à la suppression des informations sensibles dans les logs.



