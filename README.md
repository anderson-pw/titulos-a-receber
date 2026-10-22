# Títulos a Receber

Painel HTML de contas a receber com a paleta do Grupo Decio.

## Recursos

- Top 5 melhores pagadores, com todos os pagamentos até o vencimento no histórico conferido disponível.
- Top 5 ofensores com pagamentos sempre atrasados mais de um mês de calendário, incluindo a visão mês a mês.
- Filtros de mês, ilha/tipo do título (CC, CD, NF, FT e outros), filial, situação e cliente.
- Exclusão de clientes marcados como Desconsiderar nas abas cartões e intercompany do De_para, pelo cliente + loja.
- Indicadores e CSV consolidado somente com Conferido e Conferido com ressalva. Outras situações ficam na aba de conferência.
- Histórico mensal salvo neste navegador, com backup e restauração.

## Uso

1. Abra o painel publicado pelo GitHub Pages.
2. Clique em **Atualizar bases** e selecione os CSVs completos da SE1 e da SE5, separados por ponto e vírgula.
3. Na primeira importação, selecione também o `de_para_geral.xlsx`. Nas seguintes, o De_para salvo pode ser reutilizado; outro XLSX atualiza as exclusões em todo o histórico.
4. Os meses presentes nos arquivos são substituídos; os demais são preservados. Reimportar não soma novamente a mesma extração.
5. Use **Baixar backup do histórico** e **Restaurar backup** para transferir os dados para outro navegador ou computador.

As bases são processadas e salvas localmente no navegador. A publicação pública contém somente o aplicativo, sem dados financeiros ou a lista de clientes excluídos. O histórico não é compartilhado entre navegadores ou computadores e pode ser removido ao limpar os dados de navegação. O HTML local e o site mantêm históricos separados; transfira-os por backup quando necessário.

O recebimento real segue a fórmula solicitada: juros + líquido da baixa. Os critérios, o alcance do histórico e as ressalvas da conciliação estão no próprio painel.

## Estrutura

- `index.html`: aplicação completa, sem dependências externas.
- `.nojekyll`: publicação estática no GitHub Pages, branch `main`, raiz do repositório.

Desenvolvido por Anderson Prado © 2026.
