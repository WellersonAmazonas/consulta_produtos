# 📂 Relação de Tabelas e Colunas

## 🏷️ `PCPRODUT` (Produtos)
- `CODPROD` → Código do produto.
- `CODFAB` → Código de fábrica (referência).
- `DESCRICAO` → Nome do produto.
- `UNIDADE` → Unidade de venda (ex: UN, CX, KG).
- `QTUNITCX` → Embalagem.
- `CODMARCA` → Relacionamento com `PCMARCA`.

## 💰 `PCPRECO` (Preços)
- `CUSTOFIN` → Preço de custo.
- `PVENDA` → Preço de venda.

## 📦 `PCEST` (Estoque por Filial)
- `QTESTGER` → Quantidade total no estoque.
- `QTBLOQUEADA` → Quantidade bloqueada.
- `QTINDENIZ` → Quantidade indenizada.
- `QTRESERV` → Quantidade reservada.
- `CODFILIAL` → Código da filial.

## 🏛️ `PCTRIBUT` (Tributação)
- `CODICMTAB` → Código do ICMS.
- `CODST` → Código da substituição tributária.

---
