# 📌 Consulta de Produtos no WinThor (ERP)

Este projeto contém uma consulta SQL otimizada para extrair informações de produtos no WinThor, garantindo que apenas itens ativos e de revenda sejam retornados.

## 🔍 Estrutura da Query
- Filtra **produtos ativos** (exclui produtos excluídos e fora de linha).
- Retorna detalhes do produto, como **preços, estoque, tributação e códigos**.
- Permite visualizar **custos e ICMS de diferentes filiais**.

## 📂 Arquivos
- `query_produtos.sql` → Query principal.
- `estrutura.md` → Explicação das tabelas e colunas usadas.
- `docs/tabelas.md` → Relação completa das tabelas envolvidas.
- `docs/explicacao.md` → Explicação dos `JOINs` e lógica dos filtros.
- `docs/melhorias.md` → Sugestões de otimização e aprimoramento.

🚀 **Desenvolvido para melhorar a extração de dados do WinThor.**
