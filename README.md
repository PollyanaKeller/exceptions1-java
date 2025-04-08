Programa para fazer reservas (e alterá-las) em hotél, com data de check-in e check-out respeitando regras de que:
1. Data de check-out não pode ser anterior a de check-in.
2. Data de check-in não pode ser anterior a data atual.

* Solução 1 (very bad solution): lógica de validação no programa principal
    * Lógica de validação não delegada à reserva
      
* Solução 2 (bad solution): método retornando string
    * A semântica da operação é prejudicada
        * Retornar string não tem nada a ver com atualização de reserva
        * E se a operação tivesse que retornar um string?
    * Ainda não é possível tratar exceções em construtores
    * Ainda não há auxílio do compilador: o programador deve "lembrar" de verificar se houve erro
    * A lógica fica estruturada em condicionais aninhadas
      
* Solução 3 (good solution): tratamento de exceções
