## 📌 Issue: Cadastro e Autenticação de Clientes

### Descrição

Implementar o fluxo de **cadastro** e **autenticação** de clientes no sistema.

Cada cliente deverá fornecer as seguintes informações:

- Nome completo (obrigatório)  
- E-mail (obrigatório e único)  
- Senha (obrigatória, com criptografia)  
- Telefone (obrigatório)  
- CPF **ou** Passaporte (um dos dois é obrigatório; ambos devem ser únicos)

A autenticação deve ser baseada em **JWT**.

---

### 🎯 Objetivos

- Criar endpoints REST para cadastro e autenticação
- Validar dados de entrada
- Garantir segurança no armazenamento da senha
- Gerar e validar tokens JWT

---

### ✅ Critérios de Aceitação

- [ ] `POST /clientes`: Cadastro de cliente com validações
- [ ] Validação de:
  - [ ] Formato do e-mail
  - [ ] Formato do telefone
  - [ ] CPF (formato e validade) ou passaporte
  - [ ] Senha com no mínimo 6 caracteres
- [ ] CPF e e-mail únicos no banco de dados
- [ ] Senha armazenada com hash seguro (BCrypt)
- [ ] `POST /auth/login`: Autenticação do cliente com e-mail e senha
- [ ] Geração de token JWT válido com tempo de expiração
- [ ] Retorno de mensagens claras em caso de erro (ex: e-mail já cadastrado, senha incorreta, etc.)
- [ ] Testes unitários e de integração cobrindo os principais fluxos

---

### 📎 Observações

- A autenticação será usada para proteger rotas privadas no sistema.
- O sistema deve estar preparado para internacionalização futura (CPF ou passaporte).
