# Minhas Financas
Este projeto tem como objetivo auxiliar no controle financeiro pessoal de modo integrado com a conta corrente do usuário

# Arquitetura
graph LR
    A[Usuário] --> B(API Gateway);
    B --> C{Microsserviços};
    C --> D[Serviço de Renegociação];
    C --> E[Serviço de Orçamento];
    C --> F[Serviço de Educação Financeira];
    D --> G[Banco de Dados Relacional (PostgreSQL)];
    E --> G;
    F --> H[Banco de Dados NoSQL (MongoDB)];
    B --> I[Cache (Redis/Memcached)];
    A --> J[CDN];
