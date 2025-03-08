# Para obter/gerar `HEROKU_API_KEY` e `HEROKU_APP_NAME`, siga estas etapas:

---

### **1. HEROKU_API_KEY**
É a chave de API da sua conta Heroku, usada para autenticação em ferramentas como CLI, CI/CD ou scripts.

#### **Como obter:**
1. **Acesse sua conta Heroku:**
    - Faça login no [Heroku Dashboard](https://dashboard.heroku.com).
    - Clique no ícone de perfil (canto superior direito) > **Account Settings**.

2. **Gerar a chave de API:**
    - Role até a seção **API Key**.
    - Clique em **Reveal** para ver a chave existente ou **Generate API Key** para criar uma nova.

   ![Heroku API Key](https://assets.heroku.com/screenshots/3b9c0a40-5e1e-11e8-8827-478d1c6dff27)

3. **Copie a chave:**
    - Use essa chave como `HEROKU_API_KEY` em scripts, variáveis de ambiente ou CI/CD (ex: GitHub Actions).

---

### **2. HEROKU_APP_NAME**
É o nome do seu aplicativo Heroku. Pode ser definido manualmente ou gerado automaticamente.

#### **Opção 1: Aplicativo existente**
- Se o aplicativo já existe:
    - Acesse o [Heroku Dashboard](https://dashboard.heroku.com).
    - O nome do app aparece no canto superior esquerdo (ex: `my-heroku-app`).

#### **Opção 2: Criar um novo app**
1. **Via Dashboard:**
    - Clique em **New** > **Create new app**.
    - Insira um nome único (ex: `meu-app-123`) e escolha uma região.

2. **Via CLI:**
   ```bash
   heroku login  # Autentique-se
   heroku create meu-app-123  # Substitua pelo nome desejado
   ```
    - Se o nome estiver disponível, o app será criado.

---

### **Uso em variáveis de ambiente**
Configure as variáveis em seu ambiente de desenvolvimento ou CI/CD:

```bash
# Exemplo (Linux/macOS):
export HEROKU_API_KEY="sua-chave-aqui"
export HEROKU_APP_NAME="nome-do-seu-app"
```

#### **Em GitHub Actions:**
Adicione as variáveis como secrets no repositório:
1. `HEROKU_API_KEY`: Valor da sua chave de API.
2. `HEROKU_APP_NAME`: Nome do app Heroku.

---

### **Importante!**
- A `HEROKU_API_KEY` é **sensível** (não a compartilhe ou versionamento).
- O `HEROKU_APP_NAME` deve ser único no Heroku.
