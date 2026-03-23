# 📊 Painel de Mercado BR

Dashboard pessoal de acompanhamento do mercado financeiro brasileiro — ações B3, FIIs, câmbio, cripto e indicadores macro, com notícias geradas por IA.

## Fontes de dados

| Tipo | Fonte | Chave necessária |
|---|---|---|
| Ações, FIIs, ETFs | [brapi.dev](https://brapi.dev/dashboard) | ✅ Gratuita |
| Câmbio | [AwesomeAPI](https://economia.awesomeapi.com.br) | ❌ |
| Cripto (BRL e USD) | [CoinGecko](https://coingecko.com) | ❌ |
| Selic, IPCA, CDI | [Banco Central](https://api.bcb.gov.br) | ❌ |
| Notícias com IA | [Groq](https://console.groq.com) (Llama 4) | ✅ Gratuita |

---

## 🚀 Deploy no GitHub Pages

### 1. Crie o repositório

```bash
mkdir painel-mercado && cd painel-mercado
cp /caminho/para/index.html .
cp /caminho/para/README.md .
git init
git add .
git commit -m "painel de mercado"
```

### 2. Suba para o GitHub

```bash
# Cria o repositório remoto (requer GitHub CLI instalado)
gh repo create painel-mercado --public --source=. --push

# Ou manualmente: crie o repo em github.com e então:
git remote add origin https://github.com/SEU_USUARIO/painel-mercado.git
git push -u origin main
```

### 3. Ative o GitHub Pages

1. Acesse o repositório no GitHub
2. **Settings → Pages**
3. Em *Source*, selecione **Deploy from a branch**
4. Branch: **main** / Folder: **/ (root)**
5. Clique em **Save**

Em ~1 minuto o painel estará disponível em:
```
https://SEU_USUARIO.github.io/painel-mercado
```

---

## ⚡ Deploy alternativo — Netlify (arrasta e solta)

1. Acesse [app.netlify.com/drop](https://app.netlify.com/drop)
2. Arraste o arquivo `index.html` para a área indicada
3. Pronto — URL gerada na hora

---

## ⚙️ Configuração das chaves

As chaves são salvas no `localStorage` do seu browser e **nunca sobem para o repositório**. Configure após abrir o painel:

### brapi.dev (cotações B3)
1. Crie conta em [brapi.dev/dashboard](https://brapi.dev/dashboard)
2. Gere uma API Key gratuita
3. Cole no campo **⚡ Chave brapi.dev** nas Configurações do painel

### Groq (notícias com IA)
1. Crie conta em [console.groq.com](https://console.groq.com) (login com Google/GitHub)
2. **API Keys → Create API Key**
3. Cole no campo **🤖 Chave Groq** nas Configurações do painel
4. Clique em **Testar** para confirmar

> As chaves ficam apenas no `localStorage` do seu browser — cada dispositivo precisa configurar as próprias chaves.

---

## 🔄 Atualizar o painel

Após editar o `index.html`:

```bash
git add index.html
git commit -m "atualização"
git push
```

O GitHub Pages atualiza automaticamente em ~1 minuto.

---

## 📱 Usar em outros dispositivos

Acesse a URL pública e configure as chaves no novo dispositivo — as chaves ficam salvas localmente em cada browser.
