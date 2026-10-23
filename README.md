# Títulos a Receber

Painel HTML de títulos em aberto da SE1, com a paleta do Grupo Decio.

## Uso

1. Abra o painel publicado e selecione **Atualizar bases**.
2. Importe a SE1 em CSV e o `de_para_geral.xlsx` de exclusões. A SE5 não é utilizada.
3. Importe também o De_para **Filial Orig → Grupo** em XLSX ou CSV. Ele preenche o filtro Grupo e permite validar Urbano, Peças e TRR nas carteiras.
4. Consulte competência do vencimento, carteira, ilha/tipo, Grupo, posição e busca por cliente ou título.
5. Use **Ver títulos em aberto** e **Exportar CSV** para consultar os mesmos títulos únicos dos indicadores.
6. Baixe o backup do histórico para preservar ou transferir as posições.

## Regras

- A Receber soma Vlr. Titulo com DT Baixa sem data (`//`, barras com espaços ou vazio). Títulos baixados ficam fora do painel.
- Cada chave filial de origem + prefixo + número + tipo + cliente + loja entra uma vez. O primeiro registro sem baixa define valor e vencimento; as repetições e divergências ficam disponíveis na origem.
- Competência e linhas diárias de RA e NCC usam Vencto Real.
- O De_para geral exclui cliente + loja com Status Desconsiderar nas abas cartões e intercompany.
- Permanecem as filiais de origem iniciadas por 0101, 0102, 0104, 0106 ou 0180.
- Carteiras: Urbano/Peças → Ana Claudia; TRR → Thalita; demais grupos por inicial do Nome Cliente sem acentos: Milena 0–E, Maria Eduarda F–Q, Thalita R–Z.
- O De_para de Grupo aceita Filial Orig (ou Filial Origem/Filial), Grupo e, opcionalmente, Negocio/Segmento. A coluna opcional identifica o negócio; quando vazia, usa-se o nome do Grupo. Cada filial deve ter uma associação única.
- Sem o De_para, Grupo aparece como Não mapeado e as carteiras ficam pendentes. Cartão Frota e Nota Prazo aguardam classificação dos tipos.

## Histórico e privacidade

Uma nova SE1 substitui a posição atual inteira e preserva a anterior no filtro Posição, sem somar extrações. Reimportar a mesma extração não duplica o histórico. Backups anteriores são migrados para o foco em aberto, descartando a SE5.

As bases são processadas e salvas neste navegador em IndexedDB. A publicação pública contém somente a aplicação e os cabeçalhos, sem dados financeiros ou De_paras. Cada navegador, computador e origem possui histórico próprio, que pode ser removido ao limpar os dados de navegação.

## Estrutura

- `index.html`: aplicação completa, sem dependências externas.
- `.nojekyll`: publicação estática no GitHub Pages, branch main, raiz do repositório.

Desenvolvido por Anderson Prado © 2026.
