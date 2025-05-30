# Documentação Técnica: Lisa's Café

## Visão Geral do Projeto

Lisa's Café é um e-commerce temático de cafés especiais com inspiração no universo kawaii e na cultura pop japonesa, com foco em gatinhos em estilo anime. A mascote do projeto é Lisa, uma gatinha que personifica a identidade visual da marca. A interface do site utiliza uma estética “fofa e pastel”, com destaque para tons suaves de azul bebê, lavanda, branco, pêssego e cinza, buscando criar uma experiência de compra encantadora e memorável.

## Identidade Visual

* **Mascote**: Lisa, uma gatinha em estilo anime que aparece em ilustrações e ícones do site, representando o espírito "kawaii" do café.
* **Paleta de Cores**:

  * Azul bebê (#BAD7F2)
  * Lavanda (#E2D1F9)
  * Cinza suave (#F0F0F0)
  * Branco (#FFFFFF)
  * Pêssego (#FFE5D9)
  * Versão escura com variações mais profundas dessas cores.

## Tecnologias Utilizadas

* React
* TypeScript
* Tailwind CSS
* shadcn/ui
* React Router DOM
* TanStack Query
* Supabase

## Estrutura do Projeto

### Componentes Principais

1. **Layout**

   * **Header**: Navegação principal, troca de tema, idiomas e carrinho.
   * **Footer**: Informações institucionais, redes sociais e contatos.

2. **Páginas**

   * **Home**: Apresentação da marca.
   * **Shop**: Catálogo de produtos com filtros.
   * **Outras**: About, Blog, Contact, entre outras.

3. **Componentes Interativos**

   * Carrinho de compras
   * Filtros de busca
   * Sistema de conquistas e fidelidade
   * Newsletter

### Contextos

* **ThemeContext**:

  * Alternância entre temas claro e escuro
  * Gerenciamento de idioma e traduções

* **CartContext**:

  * Gerenciamento do carrinho de compras
  * Adição, remoção e atualização de itens
  * Cálculo de totais

### Dados

* **Produtos**:

  * Armazenados em `src/data/products.ts`
  * Organizados por categorias (ex: destaque, milkshakes, etc.)
  * Contêm imagens, descrições, preços e metadados.

## Funcionalidades

### Layout Responsivo

Compatível com desktops, tablets e smartphones. Componentes adaptativos garantem boa usabilidade em todos os dispositivos.

### Tema Claro/Escuro

* Alternância manual ou automática baseada na preferência do sistema.
* Persistência da escolha do usuário via `localStorage`.

### Internacionalização

* Suporte a Português (Brasil) e Inglês (EUA)
* Traduções centralizadas acessadas via `t()`
* Detecção automática do idioma do navegador

### Carrinho de Compras

* Adição e remoção de itens
* Atualização de quantidades
* Persistência no `localStorage`
* Feedback visual e sonoro para interações

### Filtros e Busca

* Filtro por categoria e faixa de preço
* Busca por palavra-chave

### Gamificação

* Sistema de conquistas visuais
* Pontuação por interações e compras
* Níveis de usuário com recompensas

## Estilo e Animações

### Componentes Personalizados

* Cards com bordas arredondadas e estética fofa
* Botões com efeito hover e animações suaves

### Otimização de Imagens

* Skeleton loaders durante o carregamento
* Transições suaves e efeitos de escala

### Exemplo de Classes Customizadas com Tailwind

```css
.lisa-card {
  @apply rounded-3xl bg-white p-5 shadow-md dark:bg-gray-800 transition-all hover:shadow-lg border border-lisa-baby-blue/30 dark:border-lisa-dark-blue/30;
}

.lisa-button {
  @apply px-5 py-2 rounded-full bg-lisa-baby-blue text-white font-medium shadow-md hover:bg-lisa-dark-blue transition-all dark:bg-lisa-dark-blue dark:hover:bg-lisa-baby-blue;
}
```

**Nota de Ellen:** As classes CSS foram renomeadas de `cat-card` e `cat-button` para `lisa-card` e `lisa-button` para melhor alinhamento com a identidade da marca "Lisa's Café" e para evitar generalidade excessiva. Isso promove clareza e consistência no código.

## Design Emocional

### Microinterações

* Animações discretas e feedback visual nos elementos interativos
* Ícones temáticos com pegadas de gato e elementos animados

### Estratégias de Conversão

* Avaliações e depoimentos
* Indicadores de estoque baixo
* Chamadas para ação claras e visíveis

## Estrutura de Arquivos

```
├── public/
│   └── uploads/
│       └── akemi.png
│       └── coffee-mocha-akemi.jpg
├── src/
│   ├── components/
│   │   ├── home/
│   │   │   ├── BlogSection.tsx
│   │   │   ├── FeaturedProducts.tsx
│   │   │   ├── GamificationSection.tsx
│   │   │   ├── HeroSection.tsx
│   │   │   ├── MilkshakeSection.tsx
│   │   │   └── NewsletterSection.tsx
│   │   ├── layout/
│   │   │   ├── Footer.tsx
│   │   │   ├── Header.tsx
│   │   │   └── Layout.tsx
│   │   └── ui/
│   │       ├── theme-toggle.tsx
│   │       └── switch-locale.tsx
│   ├── context/
│   │   ├── CartContext.tsx
│   │   └── ThemeContext.tsx
│   ├── data/
│   │   └── products.ts
│   ├── hooks/
│   │   └── use-toast.ts
│   ├── pages/
│   │   ├── Index.tsx
│   │   ├── NotFound.tsx
│   │   └── Shop.tsx
│   ├── App.tsx
│   ├── index.css
│   └── main.tsx
├── tailwind.config.ts
└── vite.config.ts
```

## Acessibilidade

* Uso de `aria-label` e atributos semânticos
* Contraste adequado entre texto e plano de fundo
* Indicadores visuais para ações de foco e clique

## Otimizações

* Lazy loading de imagens
* Skeletons para carregamento
* Código dividido por rotas e componentes
* Uso de estados locais para performance
* Dados persistidos no `localStorage` quando necessário

## Redes Sociais

O site contém links para os seguintes perfis oficiais:

* Instagram
* Pinterest
* Spotify
* Discord
* Twitter
* GitHub

## Extensibilidade

Projetado para facilitar a evolução do sistema:

* **Novos Componentes**: Estrutura modular
* **Novos Idiomas**: Sistema de traduções escalável
* **Novos Temas**: Configuração de design flexível via Tailwind
* **Novas Páginas**: Sistema de rotas dinâmico
* **Novos Produtos**: Adição fácil via arquivo centralizado

---

© 2024 Lisa's Café – Todos os direitos reservados.