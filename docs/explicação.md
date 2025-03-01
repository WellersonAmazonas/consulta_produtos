# 📌 Explicação dos Filtros e JOINs

## 📢 **Filtros Aplicados (`WHERE`)**
1. **Filtragem por filial**  
   - `EST_F1.CODFILIAL = 1`  
   - `EST_F3.CODFILIAL = 3`  
   - `EST_F6.CODFILIAL = 6`  
   - Cada filial tem seus próprios custos, estoques e tributação.

2. **Relacionamento correto entre produtos e filiais**  
   - `EST_F1.CODPROD = EST_F3.CODPROD`  
   - `EST_F3.CODPROD = EST_F6.CODPROD`  
   - `PCPRODUT.CODPROD = EST_F1.CODPROD`  
   - Garante que estamos comparando o mesmo produto nas diferentes filiais.

3. **Filtragem por região**  
   - `TABPR_F1.NUMREGIAO = 2`  
   - `TABPR_F3.NUMREGIAO = 2`  
   - `TABPR_F6.NUMREGIAO = 2`  
   - Assim, pegamos a tributação correta para cada filial.

4. **Filtragem por produto específico** *(Opcional)*  
   - `AND EST_F1.CODPROD = 55933`  
   - Remover essa linha para consultar todos os produtos.

---

## 🔗 **Explicação dos `JOINs` e Relacionamentos**
A query usa **`FROM PCEST` três vezes** para acessar os estoques de três filiais diferentes.


PCPRODUT ─┬──> PCEST (F1) ├──> PCEST (F3) ├──> PCEST (F6) ├──> PCTABPR (F1) ├──> PCTABPR (F3) ├──> PCTABPR (F6) ├──> PCTRIBUT (ICMS) ├──> PCMARCA (Marca)



🚀 **A estrutura garante que todos os dados de um produto sejam apresentados em uma única linha, facilitando a análise e comparação entre filiais.**
