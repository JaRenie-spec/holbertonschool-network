```mermaid
graph TD
    A[User Browser] --> B[DNS Resolver]
    B --> C[Google Server IP - Port 443]
    C --> D[Firewall]
    D --> E[Load Balancer]
    E --> F[Web Server]
    F --> G[Application Server]
    G --> H[Database]
    H --> G
    G --> F
    F --> E
    E --> D
    D --> C
    C --> A

    subgraph Secure Connection
        C
        D
    end

    C -->|Encrypted via HTTPS/SSL| D
	```
