# Títulos a Receber

Painel HTML de contas a receber com a paleta do Grupo Decio, incluindo títulos em aberto e Top 5 ofensores por mês da baixa. A fonte de títulos e pagamentos é a SE1. A SE5 não é utilizada.

## Atualizar bases

1. Abra o painel e clique em **Atualizar bases**.
2. Importe a SE1 completa em CSV, incluindo os títulos sem baixa e as baixas disponíveis para o histórico dos ofensores.
3. Na primeira carga, inclua também o `de_para_geral.xlsx` de exclusões. Depois, o arquivo salvo é reutilizado.
4. Grupo e carteira são calculados automaticamente. Não é necessário De_para de Grupo.
5. Use os filtros de competência/mês, carteira, ilha/tipo, Grupo e cliente. **Exportar CSV** acompanha a página e o recorte selecionados.
6. Baixe o backup para preservar ou transferir as posições entre navegadores.

## Grupo pela Filial Orig

| Início da Filial Orig | Grupo | Carteira |
|---|---|---|
| 01 | Grupo Rodoviário | Pela inicial do Nome Cliente |
| 02 | Grupo TRR | Thalita |
| 08 | Grupo Peças | Ana Claudia |
| 09 | Grupo Urbano | Ana Claudia |

No Grupo Rodoviário: 0–E → Milena; F–Q → Maria Eduarda; R–Z → Thalita. As exceções TRR/Urbano/Peças têm prioridade. A inicial ignora acentos, espaços e pontuação. Nome ausente ou inicial inválida fica em Sem classificação.

## Em aberto

A Receber soma Vlr. Titulo com DT Baixa sem data (vazio, barras ou espaços). A chave filial + prefixo + título + tipo + cliente + loja entra uma vez; a primeira linha sem baixa define valor e vencimento. O detalhamento preserva as repetições e sinaliza divergências.

Competência e gráficos diários de RA/NCC usam Vencto Real. As boxes de RA, NCC e CC mostram valor em reais e quantidade de títulos únicos. Cartão Frota e Nota Prazo aguardam os tipos aprovados.

O De_para geral exclui Cliente + Loja com Status Desconsiderar nas abas cartões e intercompany, tanto dos títulos abertos quanto dos pagamentos.

## Top 5 ofensores mês a mês

Cliente + loja com todos os pagamentos observados acima de 3 dias corridos de atraso: DT Baixa − Vencto Real > 3. Exatamente 3 dias não entra; 4 dias entra. Um pagamento com até 3 dias em qualquer mês do histórico impede a classificação. Vencimento ausente, recebimento não positivo ou observações conflitantes também impedem a classificação.

A elegibilidade considera todo o histórico disponível antes dos filtros. O ranking usa o mês da DT Baixa, ordena por Juros + Vlr. Liq Baix do maior para o menor e mantém até cinco clientes por mês. Empates usam Cliente + Loja. Os filtros recalculam o ranking, e as quantidades de pagamentos observados são exibidas, inclusive quando existe apenas um.

A mesma chave de título + data da baixa entra uma vez, mesmo em várias extrações; divergências entre observações impedem a classificação. O filtro Posição da base não limita o histórico dos ofensores. As baixas não entram nos indicadores em aberto.

## Histórico e privacidade

A nova SE1 substitui a posição aberta atual inteira e preserva a anterior em Posição da base, sem somar extrações. Reimportar a mesma extração não duplica o histórico.

Os dados são processados e salvos neste navegador em IndexedDB. A publicação pública contém somente aplicação e cabeçalhos, sem bases financeiras ou De_paras. Cada origem, navegador e computador possui histórico próprio, que pode ser removido ao limpar os dados de navegação. Use backup e restauração para transferir o histórico.

## Estrutura

- `index.html`: aplicação completa, sem dependências externas.
- `.nojekyll`: publicação estática no GitHub Pages, branch main, raiz do repositório.

Desenvolvido por Anderson Prado © 2026.
