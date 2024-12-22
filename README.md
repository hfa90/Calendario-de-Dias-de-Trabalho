1. Sistema em HTML, CSS e JavaScript
Este código fornece uma interface de usuário interativa que calcula o valor recebido em um mês com base no número de dias úteis e na diária fornecida.

HTML:
Estrutura básica para exibir os campos de entrada:
Um campo para inserir o valor da diária.
Um menu suspenso para selecionar o mês desejado.
Um botão para realizar o cálculo.
Um espaço para exibir o resultado.

CSS:
Design Responsivo e Limpo:
Utilizei um layout centrado na tela, com botões estilizados e inputs amigáveis.
A interface tem cores suaves, cantos arredondados, e efeitos de hover no botão para melhorar a usabilidade.

JavaScript:
Funções para realizar os cálculos:
calculateEarnings: Obtém os valores de entrada e calcula o valor total baseado na função calculateWorkDays.
calculateWorkDays: Calcula o número de dias úteis no mês selecionado (excluindo sábados e domingos).

2. Sistema em Python
Esse código é uma versão de terminal para fazer os mesmos cálculos de maneira simples e eficaz.

Lógica:
    Entrada do Usuário:
    Solicita o valor da diária.
    Solicita o número do mês.
    
Funções de Cálculo:
    calculate_work_days: Determina o número de dias úteis no mês especificado.
    calculate_monthly_earnings: Multiplica o número de dias úteis pelo valor da diária.
    
Saída:
    Exibe o total de ganhos no mês selecionado.
    Destaques no Python:

Utilizei a biblioteca datetime para trabalhar com datas e iterar pelos dias do mês.
Validei entradas para evitar erros comuns (exemplo: diária negativa ou meses fora do intervalo de 1 a 12).

Benefícios e Uso
HTML/JavaScript: Para uso em navegadores, perfeito para um sistema online ou desktop que interage visualmente com o usuário.
Python: Para uso offline ou em automação, onde uma interface gráfica não é necessária.

Ambas as versões são independentes e funcionam de maneira consistente, com flexibilidade para personalização. 😊
