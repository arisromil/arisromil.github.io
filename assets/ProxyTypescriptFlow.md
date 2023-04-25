flowchart TD
    A[Client] --> B(HTTPService Proxy)
    B --> C(HTTPService)
    C --> D(API Server)
    D --> C
    C --> B
    B --> A


    style B fill:#bbf,stroke:#f66,stroke-width:2px,color:#fff,stroke-dasharray: 5 5