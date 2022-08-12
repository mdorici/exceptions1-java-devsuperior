# Repositório exceptions1-java-devsuperior - Prof. Nélio Alves

**Solução 1 (muito ruim): lógica de validação no programa principal**

    • Lógica de validação não delegada à reserva

**Solução 2 (ruim): método retornando string**

    • A semântica da operação é prejudicada

          • Retornar string não tem nada a ver com atualização de reserva
          • E se a operação tivesse que retornar um string? (Geração de conflito)

    • Ainda não é possível tratar exceções em construtores
    • Ainda não há auxílio do compilador: o programador deve "lembrar" de verificar se houve erro
    • A lógica fica estruturada em condicionais aninhadas

**Solução 3 (boa): tratamento de exceções**

O modelo de tratamento de exceções permite que erros sejam tratados de forma consistente e flexível, usando boas práticas

  **Vantagens:**
  
        • Lógica delegada
        • Construtores podem ter tratamento de exceções
        • Possibilidade de auxílio do compilador (Exception)
        • Código mais simples. Não há aninhamento de condicionais: a qualquer momento que uma exceção for disparada, 
        a execução é interrompida e cai no bloco catch correspondente
        • É possível capturar inclusive outras exceções de sistema

:star: Documentação de estudos :star:

Repositório original: https://github.com/acenelio/exceptions1-java
