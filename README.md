# Títulos a Receber — posição Protheus por Saldo líquido

Painel HTML com paleta Grupo Décio. O modelo de atualização é a exportação **Posição de títulos a receber**, com **Saldo líquido**, **Vencimento** e **Filial**. Importa XLSX original ou CSV de mesmo layout, com processamento no navegador e histórico local. A publicação pública inicia sem registros financeiros nem De_para.

O modelo atual já é uma posição exportada e **não exige DT Baixa**. As SE1 históricas preservam a regra anterior de baixa sem data. Saldo líquido é o valor operacional; Vlr.Titulo permanece como valor original para conferência. Não se somam os dois. A chave inclui filial, prefixo, título, parcela, tipo, cliente e loja.

Somente FT recebe carteira e entra em A Receber e ofensores. RA/NCC/CC ficam em Pendências de baixa. Grupo pelo prefixo da Filial: 01 Rodoviário, 02 TRR, 08 Peças e 09 Urbano. Nome define a faixa alfabética: 0–E Milena, F–Q Maria Eduarda e R–Z Thalita; TRR tem prioridade para Thalita, Urbano/Peças para Ana Claudia. Exclusões por Cliente + Loja no De_para, abas cartões e intercompany. Sem SE5 e sem filtro de Conferencia.

Top 5 mensal: FT da posição com mais de três dias corridos de atraso, por Cliente + Loja, ordenado por saldo vencido. A data de análise é o dia atual de São Paulo.

Todos os filtros têm seleção múltipla e são independentes por aba. Ao selecionar várias posições, usa-se a mais recente entre elas, sem somar extrações. Exporte backup para transportar o histórico entre navegadores. A importação local não publica dados nem atualiza outros computadores.

Use uma posição completa para o escopo desejado. Cada importação substitui a posição atual. Para consolidar grupos exportados separadamente, reúna antes suas linhas em um arquivo de mesmo layout.

Verificação: `node validate-position.mjs`. Construção: `node build.mjs`. Aplicação pública, sem base incorporada: `node build-public.mjs`. A verificação do projeto Power BI Desktop é feita no pacote PBIP separado.
