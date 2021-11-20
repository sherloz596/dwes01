---
title: "Client / server diagram"
date: 2021-11-19T15:52:22+01:00
draft: false
---
***
1. The user writes the URL of the page to display in the address bar of the client's browser.
2. The client checks if the IP address of the requested page is stored in the cache.
3. If it is positive, it returns it to the browser, if it does not have it, consult the DNS server which returns the IP address.

{{<mermaid align="left">}}
flowchart LR;
    A(Customer) -->|URL| B(cache/host)
    B --> C{NO}
    C --> D(DNS Server)
    D --> |IP address| A
    B --> E{YES}
    E --> |IP address| A
{{< /mermaid >}}

4. The client establishes a TCP / IP connection with the server.
5. The server performs back-end processing.
6. If the server finds the web page, it sends the content to the client in the form of data packets, otherwise it emits a 404 error code (page not found).
7. The client displays the result in the browser.

{{<mermaid align="left">}}
flowchart LR;
    A(Client) -->|TCP / IP connection| B(Server)
    B --> |Website| A
{{< /mermaid >}}