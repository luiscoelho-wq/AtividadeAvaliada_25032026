# Avaliação — Engenharia de Software
**Sistema Integrado de Gestão de Farmácia — MVP Definido pelo Estudante**

Aluno: Luís Felipe Coelho
RA: 25001003  
Data: 25/03/2026 

---

# 1. Definição do MVP
Para o MVP, decidi focar na principal parte do sistema, o processo de vendas dentro da farmácia, que começa na identificação ou cadastro dos clientes, passa pela busca de produtos e termina na venda finalizada.

Dentro do MVP ficou o cadastro, consulta de produtos, controle de estoque durante as vendas, a emissão de comprovante no final da venda e a opção de venda a prazo, gerando automaticamente uma conta para receber.

Agora fora do MVP, ficou o controle completo de fornecedores, contas a pagar, relatórios mais avançados e a parte administrativa de usuários. Funções importantes, mas não diretamente ligadas ao processo de vendas.

Escolhi dividir dessa forma, pois a venda é a função mais usada no sistema e envolve algumas outras áreas, como o estoque e as finanças, então dá para montar o projeto de maneira mais organizada e sem muita complexidade.

---

# 2. Regras de Negócio (mínimo: 5)
Liste e descreva **cada RN** de forma clara.

**RN01 — Não vender produtos que não está em estoque**  
Caso não tiver a quantidade do produto requerida, a venda não pode ser feita.

**RN02 — Atualizar o estoque de maneira automática**  
A cada nova venda, o estoque deve receber uma atualização.

**RN03 — Venda com prazo gera conta a receber**  
Se houver venda com prazo, o sistema gera uma conta automaticamente.

**RN04 — Cliente precisa de cadastro para comprar com prazo**  
Não pode vender a prazo para clientes sem cadastro.

**RN05 — Produto precisa de dados básicos**  
Nome, preço, unidade e fabricante são obrigatórios para o produto.

---

# 3. Requisitos Funcionais (mínimo: 8)
Liste os requisitos funcionais do seu MVP.

**RF01 —**  
**RF02 —**  
**RF03 —**  
**RF04 —**  
**RF05 —**  
**RF06 —**  
**RF07 —**  
**RF08 —**  

(Adicione mais se quiser.)

---

# 🛡 4. Requisitos Não Funcionais (mínimo: 4)
Liste os RNFs do sistema conforme seu MVP.

**RNF01 —**  
**RNF02 —**  
**RNF03 —**  
**RNF04 —**  

(Adicione mais se quiser.)

---

# 5. Casos de Uso (mínimo: 10)
### Inserir **diagrama de casos de uso geral**, demonstrando claramente:
- os 10 casos
- relação entre eles e atores
- pelo menos 3 includes
- pelo menos 3 extends

---

# 6. Documentação dos Casos de Uso
Para **cada caso de uso**, utilize o template abaixo:
---

## **UCXX — Nome do Caso de Uso**
**Ator(es):**  
**Descrição:**  
**Pré-condições:**  
**Pós-condições:**  

### Fluxo Principal
1.  
2.  
3.  
4.  

### Fluxos Alternativos / Exceções
- FA01 —  
- FA02 —  

### Relacionamentos
- **Include:** (listar quando aplicável)  
- **Extend:** (listar quando aplicável)  

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

---

> Repita essa estrutura para **todos os seus casos de uso** (mínimo 10).


