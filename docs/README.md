# 🏗️ Desafio Fullstack Integrado
🚨 Instrução Importante (LEIA ANTES DE COMEÇAR)
❌ NÃO faça fork deste repositório.

Este repositório é fornecido como modelo/base. Para realizar o desafio, você deve:
✅ Opção correta (obrigatória)
  Clique em “Use this template” (se este repositório estiver marcado como Template)
OU
  Clone este repositório e crie um NOVO repositório público em sua conta GitHub.
📌 O resultado deve ser um repositório próprio, independente deste.

## 🎯 Objetivo
Criar solução completa em camadas (DB, EJB, Backend, Frontend), corrigindo bug em EJB e entregando aplicação funcional.

## 📦 Estrutura
- db/: scripts schema e seed
- ejb-module/: serviço EJB com bug a ser corrigido
- backend-module/: backend Spring Boot
- frontend/: app Angular
- docs/: instruções e critérios
- .github/workflows/: CI

## ✅ Tarefas do candidato
1. Executar db/schema.sql e db/seed.sql
2. Corrigir bug no BeneficioEjbService
3. Implementar backend CRUD + integração com EJB
4. Desenvolver frontend Angular consumindo backend
5. Implementar testes
6. Documentar (Swagger, README)
7. Submeter via fork + PR

## 🐞 Bug no EJB
- Transferência não verifica saldo, não usa locking, pode gerar inconsistência
- Espera-se correção com validações, rollback, locking/optimistic locking

## 📊 Critérios de avaliação
- Arquitetura em camadas (20%)
- Correção EJB (20%)
- CRUD + Transferência (15%)
- Qualidade de código (10%)
- Testes (15%)
- Documentação (10%)
- Frontend (10%)


## ⚙️ Como Executar o Projeto

O projeto foi configurado para rodar de forma extremamente simples.

### 1. Rodando o Back-end (Spring Boot)
1. Certifique-se de ter o Java 17+ e o Maven instalados.
2. Navegue até a pasta do back-end (`backend-module`).
3. Execute o comando Maven ou dê o play na sua IDE (IntelliJ/Eclipse) no arquivo `BackendApplication.java`:
   ```bash
   mvn spring-boot:run

O servidor iniciará na porta 8080 e o banco de dados será populado automaticamente.

Rodando o Front-end (Angular):

Certifique-se de ter o Node.js e o Angular CLI instalados.
Navegue até a pasta do front-end.
Instale as dependências e inicie o servidor:
  ```bash
  npm install
  ng serve
```
Acesse a aplicação no navegador em: http://localhost:4200

Documentação da API (Swagger):
A API está totalmente documentada e pode ser testada visualmente. Com o back-end rodando, acesse:
👉 http://localhost:8080/swagger-ui/index.html

Testes Unitários:
A lógica de negócios principal (transferência de valores) está coberta por testes automatizados utilizando JUnit e Mockito, simulando o comportamento do banco de dados para garantir a exatidão matemática e as validações de saldo insuficiente.

```bash
mvn test
```
