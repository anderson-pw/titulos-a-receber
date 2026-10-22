# Títulos a Receber

Painel HTML de contas a receber com a paleta do Grupo Decio.

## Recursos

- A Receber: soma de Vlr. Título com DT Baixa sem data (// ou vazio), por mês de Vencto Real.
- Boxes de RA, NCC e CC com valores em reais e quantidade de títulos únicos em aberto.
- Gráficos em linha do valor diário de RA e NCC, pelo vencimento real.
- Filtro por carteira: Milena (0 a E), Maria Eduarda (F a Q), Thalita (R a Z / TRR) e Ana Claudia (Urbano / Peças).
- A divisão por inicial do Nome Cliente está ativa. A classificação de Urbano, Peças e TRR e os grupos Cartão Frota e Nota Prazo aguardam o próximo De_para, conforme combinado.
- Top 5 melhores pagadores e ofensores recorrentes, incluindo a visão mês a mês.
- Filtros de competência, ilha/tipo (incluindo RA e NCC), carteira, filial, situação e cliente.
- Exclusão de clientes marcados como Desconsiderar nas abas cartões e intercompany do De_para, pelo cliente + loja.
- Todos os resultados da conferência SE1 × SE5 são considerados, mantendo a classificação de cada registro.
- Histórico salvo no navegador, com backup e restauração.

## Uso

1. Abra o painel publicado pelo GitHub Pages.
2. Em **Atualizar bases**, selecione os CSVs completos da SE1 e da SE5, separados por ponto e vírgula. Inclua na SE1 os tipos necessários e os títulos com DT Baixa sem data (// ou vazio).
3. Na primeira importação, selecione também o `de_para_geral.xlsx`. Depois, o De_para salvo pode ser reutilizado; outro XLSX atualiza as exclusões de todo o histórico.
4. Os meses baixados presentes nos arquivos são substituídos; os demais são preservados. O conjunto de títulos sem baixa também é atualizado, inclusive quando ficar vazio, para retirar títulos já quitados.
5. Use **Ver títulos em aberto** para consultar o mesmo recorte dos indicadores sem duplicar títulos. A exportação da visão executiva usa esse recorte. Em Detalhamento e Conferência, a exportação acompanha a seleção da respectiva aba.
6. Use **Baixar backup do histórico** e **Restaurar backup** para transferir os dados para outro navegador ou computador.

Cada título em aberto entra uma vez pela chave completa: filial de origem + prefixo + número + tipo + cliente + loja. Em repetições dessa chave, o primeiro registro sem baixa define o valor e o vencimento. As linhas de origem continuam disponíveis para conferência.

Os indicadores em aberto usam o mês do vencimento real. Os gráficos de recebimento, os rankings de pagadores e a conferência continuam usando o mês da baixa. Os gráficos em linha permitem consultar os valores de cada dia passando o cursor nos pontos.

As bases são processadas e salvas localmente no navegador. A publicação pública contém somente o aplicativo, sem dados financeiros nem a lista de clientes excluídos. O histórico não é compartilhado entre navegadores ou computadores e pode ser removido ao limpar os dados de navegação. O HTML local e o site mantêm históricos separados; transfira-os por backup quando necessário.

A extração anterior contém somente FT já baixados. Os indicadores A Receber ficam zerados até importar uma base com títulos sem baixa. Cartão Frota e Nota Prazo mostram classificação pendente, em vez de presumir um tipo.

## Estrutura

- `index.html`: aplicação completa, sem dependências externas.
- `.nojekyll`: publicação estática no GitHub Pages, branch `main`, raiz do repositório.

Desenvolvido por Anderson Prado © 2026.
