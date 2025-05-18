graph TD;
    A[User] -->|Access| B[Web Application];
    B -->|Fetch Data| C[Microservices];
    C -->|Query| D[(Database)];
    D -->|Return Data| C;
    C -->|Response| B;
    B -->|Display| A;
    B --> E[API Gateway];
    E --> F[Authentication Service];
    E --> G[Monitoring Service];
    G --> H[Alerting System];
    subgraph Internal_Processes
        I[Transaction Processing] --> D;
        J[Reporting Service] --> D;
    end
    B -->|Manage| I;
    B -->|Generate| J;