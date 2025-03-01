# 📊 Estrutura das Tabelas Utilizadas

Este documento detalha as tabelas utilizadas na consulta SQL, explicando sua finalidade e colunas principais.

---

## 🏷️ **1. PCPRODUT (Produtos)**
**Descrição:** Contém os dados principais dos produtos.  
**Chave Primária:** `CODPROD`  
**Colunas Usadas:**
- `CODPROD` → Código do produto.
- `CODFAB` → Código de fábrica (referência do fornecedor).
- `DESCRICAO` → Nome do produto.
- `UNIDADE` → Unidade de venda (ex: UN, CX, KG).
- `QTUNITCX` → Embalagem.
- `CODMARCA` → Código da marca do produto.
- `NBM` → Código NCM.
- `CODCEST` → Código CEST.
- `CODAUXILIAR` → Código de barras.

---

## 💰 **2. PCPRECO (Preços)**
**Descrição:** Contém os preços dos produtos.  
**Chave Estrangeira:** `CODPROD`  
**Colunas Usadas:**
- `CUSTOFIN` → Preço de custo.

---

## 📦 **3. PCEST (Estoque por Filial)**
**Descrição:** Controla os estoques dos produtos por depósito e filial.  
**Chave Estrangeira:** `CODPROD`  
**Colunas Usadas:**
- `QTESTGER` → Quantidade disponível no estoque.
- `QTBLOQUEADA` → Quantidade bloqueada.
- `QTINDENIZ` → Quantidade indenizada.
- `QTRESERV` → Quantidade reservada.
- `CODFILIAL` → Código da filial.

---

## 🏛️ **4. PCTRIBUT (Tributação)**
**Descr
