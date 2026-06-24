# Magic Toys

Loja de brinquedos online — uma aplicação de e-commerce frontend com interface intuitiva, carrinho de compras, sistema de busca avançado e checkout simplificado. Desenvolvida com HTML, CSS e JavaScript puro.

## Sobre o projeto

**Magic Toys** é uma plataforma de vendas de brinquedos para crianças, oferecendo uma experiência de compra fluida e divertida. O projeto oferece navegação por categorias (Meninas, Meninos, Bebês), busca inteligente de produtos, carrinho de compras interativo e finalização de pedidos sem complicações.

## Estrutura do repositório

```
magic-toys/
├── index.html             — Página principal da loja
├── script.js              — Lógica interativa (carrinho, busca, modal, etc)
├── styles/
│   ├── style.css          — Import central de estilos
│   ├── global.css         — Estilos globais e scrollbar customizada
│   ├── header-nav.css     — Header, navegação e barra de busca
│   ├── banner.css         — Carrossel de banners
│   ├── content.css        — Grid de produtos e cards
│   ├── footer.css         — Rodapé e redes sociais
│   ├── modal-carrinho.css — Sidebar do carrinho
│   ├── modal-login.css    — Sidebar de login
│   ├── modal-menu.css     — Menu lateral (mobile)
│   ├── modal-checkout.css — Modal de finalização de compra
│   └── responsive.css     — Media queries (mobile, tablet, desktop)
├── imagens/
│   ├── banner/            — Banners promocionais (responsivos)
│   ├── section/           — Imagens dos produtos por categoria
│   ├── gifs/              — Animações e mascote (Bonzi Buddy)
└── README.md              — Este arquivo
```

## Tecnologias

- **HTML5** — Estrutura semântica
- **CSS3** — Layout responsivo, grid, flexbox
- **JavaScript (Vanilla)** — Sem dependências externas
- **Font Awesome 6.4.0** — Ícones
- **Google Fonts** (Griffy) — Tipografia customizada

## Funcionalidades principais

✨ **Carrossel de Banners**
- Navegação com setas (anterior/próximo)
- Imagens responsivas (mobile/desktop)
- Autoajuste ao redimensionar janela

🛍️ **Carrinho de Compras**
- Adicionar/remover produtos
- Aumentar/diminuir quantidade
- Badge com contador de itens
- Cálculo de total automático
- Sidebar elegante com overlay

🔍 **Busca Avançada**
- Filtro em tempo real (debounce 300ms)
- Busca em nome de produtos
- Mostra indicador visual para produtos escondidos
- Scroll automático até o produto
- Interface fluida com overlay

🏷️ **Categorias de Produtos**
- Mais Vendidos
- Meninas
- Meninos
- Bebês
- Botão "Ver mais" para expandir/recolher

📱 **Sistema de Login**
- Sidebar com múltiplas opções
- Login com código
- Integração com Google e Facebook
- Formulário de email e senha
- Recuperação de senha

💳 **Checkout Modal**
- Resumo do pedido
- Formulário de informações do cliente
- Seleção de método de pagamento (PIX, Cartão, Boleto)
- Confirmação com validação

📱 **Design Responsivo**
- Mobile first
- Breakpoints: 460px, 550px, 650px, 1000px, 1200px
- Menu hambúrguer em dispositivos pequenos
- Layout adaptável para todos os tamanhos

## Como usar

### 1. Abrir a loja

**Opção 1**: Abrir diretamente no navegador
```bash
Abra index.html no seu navegador (duplo clique ou arraste para o navegador)
```

**Opção 2**: Usar um servidor estático local
```bash
# Com npx http-server
npx http-server . -p 8080

# Ou com Python
python -m http.server 8080
```

**Opção 3**: Live Server no VSCode
- Instale a extensão "Live Server"
- Clique com direito em `index.html` → "Open with Live Server"

### 2. Navegar pela loja

- **Header**: Logo, barra de busca, ícone de conta e carrinho
- **Navegação**: Links para categorias (Mais Vendidos, Meninas, Meninos, Bebês)
- **Banners**: Deslize pelas promoções usando as setas
- **Cards**: Clique em "Carrinho" para adicionar produtos
- **Menu Lateral**: Acesse em dispositivos mobile

### 3. Buscar produtos

1. Digite na barra de busca (mínimo 2 caracteres)
2. Veja sugestões em tempo real
3. Clique para navegar até o produto
4. Pressione ESC para fechar a busca

### 4. Comprar

1. Clique em "🛒 Carrinho" nos produtos
2. Ajuste quantidades no sidebar
3. Clique em "Finalizar Compra"
4. Preencha dados de entrega
5. Escolha forma de pagamento
6. Confirme o pedido

## Estrutura de cores

| Cor | Código | Uso |
|-----|--------|-----|
| Amarelo | #FBFF00 | Destaque, buttons, backgrounds |
| Roxo Escuro | #3F0251 | Textos primários, borders |
| Roxo Médio | #572063 | Textos secundários, hover |
| Roxo Claro | #895D93 | Textos terciários |
| Roxo do BG | #895D93 | Fundo da página |

## Features técnicas

### JavaScript
- **Carrinho persistente** em memória (por sessão)
- **Debounce** na busca para melhor performance
- **Classes e métodos** bem organizados
- **Event listeners** centralizados
- **Overlay** para modais

### CSS
- **Grid layout** para produtos
- **Flexbox** para alinhamentos
- **Clip-path** para design criativo da nav
- **Custom scrollbar** estilizado
- **Transições suaves** em todos os elementos
- **Box-shadow** para profundidade

### Responsividade
```css
Mobile (< 460px)
Tablet (460px - 650px)
Desktop (> 1000px)
```

## Estrutura do Carrinho

```javascript
// Itens armazenados no DOM
{
  nome: String,
  preço: String (formatado em R$),
  quantidade: Number,
  imagem: String (URL)
}
```

## Estrutura da Busca

```javascript
// Produtos carregados dinamicamente
{
  name: String,
  image: String,
  category: String (meninas|meninos|bebes),
  categoryName: String,
  isHidden: Boolean
}
```

## Contribuição

1. Fork e clone o repositório
2. Crie uma branch: `git checkout -b feature/minha-feature`
3. Faça suas alterações
4. Teste em diferentes resoluções (responsive)
5. Commit: `git commit -m "Add: descrição da feature"`
6. Push: `git push origin feature/minha-feature`
7. Abra um Pull Request

## Melhorias futuras

- [ ] Backend com Node.js/Express para persistência
- [ ] Autenticação real com JWT
- [ ] Integração com APIs de pagamento (PIX, Stripe, PayPal)
- [ ] Sistema de avaliações e comentários
- [ ] Wishlist/Favoritos
- [ ] Filtros avançados (preço, marca, avaliação)
- [ ] Painel de administração
- [ ] Notificações por email

## Licença

Licença: ISC

## Autor

Geve — https://github.com/geve-dev

## Suporte

Para dúvidas ou problemas, abra uma issue no repositório ou entre em contato pelos links de redes sociais do footer.

---

**Made with 💛 and 🎮 for Magic Toys**
