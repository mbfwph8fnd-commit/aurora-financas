# Aurora Finanças — Visão geral

Tela de **Visão geral** do projeto Fintech *Aurora Finanças* (FIAP · Fase 4 — View), recriada a partir das telas desenhadas na Fase 2 usando **HTML, CSS e Tailwind CSS**.

Desenvolvido por **Vanessa Alcantara Carreiro Ferreira**.

## Como abrir

Dê dois cliques em `index.html`. O Tailwind já está compilado em `css/tailwind.css`, então a página abre sem instalar nada e **funciona sem internet**.

## Estrutura

```
aurora-financas/
├── index.html          → a tela (HTML)
├── css/
│   ├── tailwind.css    → Tailwind CSS compilado (gerado a partir de src/input.css)
│   └── style.css       → estilos próprios (gráficos, gauge, componentes)
├── img/
│   ├── logo-aurora.svg
│   └── favicon.svg
├── src/
│   └── input.css       → configuração do Tailwind (cores e fonte da identidade visual)
└── README.md
```

## O que há de novo em relação à Fase 2

- **Saúde financeira**: nota de 0 a 100 com taxa de poupança, reserva de emergência e comprometimento da renda com dívidas.
- **Fluxo de caixa comparativo**: receitas x despesas lado a lado nos últimos 12 meses, com eixo e legenda.
- **Próximos vencimentos**: usa as entidades `DIVIDA` e `PARCELA_DIVIDA` do modelo de dados, que ainda não tinham tela.
- **Dica da Aurora**: um insight automático sobre os objetivos.
- **Orçamento do mês** e **Objetivos em andamento** resumidos na própria visão geral.
- **Rosca de categorias** com valores em reais, além das porcentagens.
- **Mobile de verdade**: no celular o menu lateral vira cabeçalho + barra de navegação inferior com botão central de nova despesa, e a tabela vira lista de cartões.
- **Acessibilidade**: HTML semântico, link "pular para o conteúdo", textos alternativos nos gráficos e foco visível.
- Sem JavaScript: os gráficos são feitos com CSS (`conic-gradient` e barras com Tailwind).

## Identidade visual

| Uso | Cor |
|---|---|
| Menu / texto | `#14223B` |
| Fundo | `#F3F6FB` |
| Ação / receitas | `#2563EB` |
| Positivo | `#0F8A6A` |
| Despesas | `#E0475B` |
| Atenção | `#D99A2B` |

## Regerar o CSS do Tailwind (opcional)

```bash
npx @tailwindcss/cli -i ./src/input.css -o ./css/tailwind.css --minify
```

## Comandos Git usados (GitHub Flow)

```bash
git init
git add .
git commit -m "feat: estrutura inicial do projeto Aurora Finanças"
git branch -M main
git remote add origin https://github.com/mbfwph8fnd-commit/aurora-financas.git
git push -u origin main

# nova funcionalidade em uma branch
git checkout -b feature/visao-geral
git add .
git commit -m "feat: tela de visão geral com Tailwind e responsividade"
git push -u origin feature/visao-geral
# abrir o Pull Request no GitHub e fazer o merge na main
```
