---
title: "Schéma client/serveur"
date: 2021-11-19T15:52:22+01:00
draft: false
---
***
1. L'utilisateur écrit l'URL de la page à afficher dans la barre d'adresse du navigateur du client.
2. Le client vérifie si l'adresse IP de la page demandée est stockée dans le cache.
3. S'il est positif, il le renvoie au navigateur, s'il ne l'a pas, consultez le serveur DNS qui renvoie l'adresse IP.

{{<mermaid align="left">}}
flowchart LR;
    A[Client] -->|URL| B(cache/hôte)
    B --> C{NON}
    C --> D[Serveur DNS]
    D --> |adresse ip| A
    B --> E{OUI}
    E --> |adresse ip| A
{{< /mermaid >}}

4. Le client établit une connexion TCP/IP avec le serveur.
5. Le serveur effectue le traitement back-end.
6. Si le serveur trouve la page web, il envoie le contenu au client sous forme de paquets de données, sinon il émet un code d'erreur 404 (page non trouvée).
7. Le client affiche le résultat dans le navigateur.

{{<mermaid align="left">}}
flowchart LR;
    A[Client] -->|Connexion TCP/IP| B(serveur)
    B --> |Site Internet| A
{{< /mermaid >}}
