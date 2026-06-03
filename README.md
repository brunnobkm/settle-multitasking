# Multitasking — protótipo

Protótipo **self-contained** (um único `index.html`, sem dependências) do padrão **Multitasking**:
duas sidebars acopladas (uma **primária** + uma **auxiliar**) que dividem a tela com o menu e o
conteúdo principal, de forma responsiva.

**Demo:** https://brunnobkm.github.io/settle-multitasking/

## O que dá para testar
- **Abrir sidebar** → abre o workspace (Resumo).
- **Abrir Arquivos da licitação** → modo primária + auxiliar.
- **Redimensionar:** arraste a borda do workspace e a divisória entre Resumo e Arquivos (linha verde).
- **Menu** (52/280px): abra/feche para ver o workspace e o conteúdo se reajustarem.
- **Modo abas:** estreite a janela — abaixo de 760px de workspace vira abas (`Resumo | Arquivos`).
- **Fechar (X):** na aba Arquivos volta ao Resumo; na aba Resumo fecha o workspace.

## Regras (resumo)
- Largura = % do **espaço útil** (`viewport − menu`), nunca `vw` cru.
- Conteúdo principal reserva ~**640px** (exceção em telas muito apertadas).
- Resize fluido (transição desligada no arraste), memória por modo, re-clamp ao mudar o espaço.
- Header responsivo: título some nas abas, ações por aba, colapso no `…` só por overflow real.

*Conteúdo (Resumo/Arquivos) é placeholder — este protótipo demonstra o padrão de layout, não dados reais.*
