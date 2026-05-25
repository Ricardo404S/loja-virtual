# 🛍️ NŌVA — Loja Virtual com Painel Admin

> E-commerce completo com visual 3D interativo e Firebase — desenvolvido por [Ricardo Souza](https://github.com/Ricardo404S)

---

## 💡 O que é esse projeto?

Uma loja virtual de verdade, do zero — sem usar plataformas prontas como Shopify ou WooCommerce. Tudo feito na mão com JavaScript e Firebase.

O dono entra no painel admin, cadastra um produto com nome, preço, estoque e categoria — e na mesma hora ele aparece na vitrine da loja pra todo mundo ver. O cliente navega pelos produtos, adiciona no carrinho e finaliza o pedido. O dono vê tudo em tempo real.

O diferencial visual? Um **hero 3D interativo** feito com Three.js — os produtos flutuam na tela e reagem ao movimento do mouse.

---

## ✨ Funcionalidades

### Loja (cliente)
- Hero 3D interativo com objetos que reagem ao mouse
- Grid de produtos com modelos 3D individuais em cada card
- Carrinho deslizante com quantidade e remoção de itens
- Finalizar pedido salvo direto no Firestore
- Cursor personalizado
- Animações de entrada suaves

### Painel Admin
- Estatísticas em tempo real: produtos, pedidos, receita, itens vendidos
- Cadastro de produtos com nome, preço, estoque, categoria, desconto e emoji
- Tabela de produtos com opção de remover
- Lista dos últimos pedidos com status
- Tudo atualiza automaticamente via Firebase

---

## 🛠️ Tecnologias usadas

| Tecnologia | Para quê |
|---|---|
| **HTML & CSS** | Estrutura e visual completo |
| **JavaScript** | Lógica, carrinho, interações |
| **Three.js** | Objetos 3D no hero e nos cards |
| **Firebase Firestore** | Produtos e pedidos em tempo real |
| **Firebase Hosting** | Publicação online gratuita |

---

## 🚀 Como rodar o projeto

### 1. Clone o repositório
```bash
git clone https://github.com/Ricardo404S/loja-virtual.git
cd loja-virtual
```

### 2. Configure o Firebase
Substitua no `index.html` com suas credenciais:

```javascript
const firebaseConfig = {
  apiKey: "SUA_API_KEY",
  authDomain: "SEU_PROJETO.firebaseapp.com",
  projectId: "SEU_PROJETO",
  storageBucket: "SEU_PROJETO.appspot.com",
  messagingSenderId: "SEU_ID",
  appId: "SEU_APP_ID"
};
```

### 3. Abra no navegador
Pode abrir o `index.html` direto ou publicar com Firebase Hosting:

```bash
npm install -g firebase-tools
firebase login
firebase init hosting
firebase deploy
```

---

## 📁 Estrutura do banco (Firestore)

```
produtos/
  └── {id}/
        ├── nome              → "Vaso Cerâmica"
        ├── descricao         → "Peça artesanal"
        ├── preco             → 299.90
        ├── precoOriginal     → 399.90  (se tiver desconto)
        ├── precoComDesconto  → 299.90
        ├── desconto          → 25  (%)
        ├── estoque           → 10
        ├── categoria         → "Decoração"
        ├── emoji             → "🏺"
        └── criadoEm          → timestamp

pedidos/
  └── {id}/
        ├── itens    → [ { id, nome, qty, preco } ]
        ├── total    → 599.80
        ├── status   → "novo" | "enviado" | "cancelado"
        └── criadoEm → timestamp
```

---

## 📸 Preview

> Acesse a demo: [test-site383.web.app](https://test-site383.web.app)

---

## 👨‍💻 Desenvolvedor

**Ricardo Souza** — Desenvolvedor Web · Mauá, SP

- GitHub: [@Ricardo404S](https://github.com/Ricardo404S)
- WhatsApp: [+55 11 97952-3456](https://wa.me/5511979523456)

---

*Feito com 💚, Three.js e Firebase*
