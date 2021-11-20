---
title: "Diagrama cliente/servidor"
date: 2021-11-19T15:52:22+01:00
draft: false
---
***
1. El usuario escribe en la barra de direcciones del navegador del cliente la URL de la página a mostrar.
2. El cliente comprueba si tiene almacenada en la caché la dirección ip de la página solicitada.
3. En caso positivo la retorna al navegador, si no la tiene consulta al servidor DNS el cual le retorna la dirección ip.

{{<mermaid align="left">}}
flowchart LR;
    A[Cliente] -->|URL| B(caché/host)
    B --> C{NO}
    C --> D[Servidor DNS]
    D --> |Dirección ip| A
    B --> E{SI}
    E --> |Dirección ip| A
{{< /mermaid >}}

4. El cliente establece una conexión TCP/IP con el servidor.
5. El servidor realiza el procesamiento del back-end.
6. Si el servidor encuentra la página web, envía el contenido al cliente en forma de paquetes de datos, si no emite un código de error 404(página no encontrada).
7. El cliente muestra el resultado en el navegador.

{{<mermaid align="left">}}
flowchart LR;
    A[Cliente] -->|Conexión TCP/IP| B(Servidor)
    B --> |Página web| A
{{< /mermaid >}}
