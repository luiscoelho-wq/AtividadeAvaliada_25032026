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

# 2. Regras de Negócio 

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

**RN06 — Não finalizar vendas vazias**
O sistema deve barrar uma venda sem itens.

---

# 3. Requisitos Funcionais 

**RF01 — Cadastrar cliente no sistema da farmacia**
**RF02 — Buscar cliente cadastrados**  
**RF03 — Buscar por produto em estoque**  
**RF04 — Ver estoque, itens e quantidades disponiveis** 
**RF05 — Registrar venda no sistema** 
**RF06 — Adicionar produtos nas vendas**  
**RF07 — Finalizar a venda do produto**  
**RF08 — Registrar venda a prazo no sistema**  
**RF09 — Gerar conta a receber depois de uma venda a prazo**  
**RF08 — Registrar venda a prazo no sistema**  
**RF10 — Remover produtos da venda** 
**RF11 — Cancelar venda**  

---

# 🛡 4. Requisitos Não Funcionais 

**RNF01 — O sistema deve ser rápido, sem travamentos durante uso**  
**RNF02 — Deve ter uma interface simples, facilitando o uso**  
**RNF03 — Só usuarios com autorização podem usar**  
**RNF04 — Não deve haver perda, nem corrompimento de dados dentro do sistema**  

---

# 5. Casos de Uso 

<img width="749" height="521" alt="image" src="https://github.com/user-attachments/assets/95338f92-c44b-4644-a303-4fbec5143131" />

---
# 6. Documentação dos Casos de Uso
---
## **UC01 — Cadastro de clientes**

**Ator(es): Atendente**  
**Descrição: Possibilita o cadastro de novos usuários no sistema**  
**Pré-condições: Atendente estar logado no sistema**  
**Pós-condições: Cliente cadastrado com sucesso**

### Fluxo Principal
1.  Atendente acessa a tela de cadastro.
2.  Preenche as informações que o sistema exige do cliente.
3.  Finaliza o cadastro.
4.  Sistema valida as informações dadas.
5.  Sistema registra o cliente.  

### Fluxos Alternativos / Exceções
- FA01 —  Informações obrigatórias em falta > Sistema exige correção.
- FA02 —  Cliente já tem cadastro > Sistema informa erro

### Relacionamentos
- **Include: -** 
- **Extend: -**  

---
<img width="236" height="257" alt="image" src="https://github.com/user-attachments/assets/31f02836-383e-45e9-8ac6-17a7b2e761ec" />

---

## **UC02 — Consulta de clientes**
**Ator(es): Atendente**  
**Descrição: Permite a busca de clientes no sistema**  
**Pré-condições: Cliente cadastrado**  
**Pós-condições: Dados são exibidos na tela**  

### Fluxo Principal
1.  Atendente acessa a busca dentro da aplicação.
2.  Informa nome ou CPF do cliente.
3.  Sistema realiza busca do cliente.
4.  O resultado aparece.  

### Fluxos Alternativos / Exceções
- FA01 —  Cliente não encontrado > Sistema informa 

### Relacionamentos
- **Include: -** 
- **Extend: UC01** 

---
<img width="286" height="312" alt="image" src="https://github.com/user-attachments/assets/19ffce3e-8f76-4b08-8303-8855a3a2d29d" />

---

## **UC03 — Consulta de produtos**
**Ator(es): Atendete**  
**Descrição: Premite a busca por produtos no sistema**  
**Pré-condições: Sistema ativo**  
**Pós-condições: Produto exibido**  

### Fluxo Principal
1.  Acessa a consulta de estoque.
2.  Informa o produto que deseja.
3.  Sistema busca o produto.
4.  Exibe o resultado buscado.

### Fluxos Alternativos / Exceções
- FA01 —  Produto não encontrado > Sistema informa

### Relacionamentos
- **Include: -** 
- **Extend: -** 

---
<img width="98" height="191" alt="image" src="https://github.com/user-attachments/assets/ae90a893-063d-4434-899c-d2f15cb4fadf" />

---

## **UC04 — Verificação de estoque**
**Ator(es): Atendente**  
**Descrição: Consulta dos itens e quantridades disponíveis**  
**Pré-condições: Produto estar em estoque**  
**Pós-condições: Quantidade exibida**  

### Fluxo Principal
1.  Seleciona o produto que deseja.
2.  Sistema analisa o estoque.
3.  A quantidade é exibida.

### Fluxos Alternativos / Exceções
- FA01 — Não há estoque do produto > Sistema envia um aviso

### Relacionamentos
- **Include: UC03** 
- **Extend: -** 

---
<img width="146" height="248" alt="image" src="https://github.com/user-attachments/assets/45f574a7-7d09-4f11-9310-d190ef186f84" />

---

## **UC05 — Registro de venda**
**Ator(es): Atendente**  
**Descrição: Inicia uma venda e registra ela**  
**Pré-condições: Sistema ativo**  
**Pós-condições: Venda em processo**  

### Fluxo Principal
1.  Uma venda é iniciada.
2.  Sistema registra essa venda.
3.  Pode-se adicionar produtos nessa venda.

### Fluxos Alternativos / Exceções
- FA01 —  Produto sem estoque > Venda cancelada
- FA02 —  Venda cancelada

### Relacionamentos
- **Include: -** 
- **Extend: UC11** 

---
<img width="161" height="341" alt="image" src="https://github.com/user-attachments/assets/0282f331-fda4-45a1-9202-801bfd08d75e" />

---



