# Calculando Rendimento de Acertos

Neste projeto os objetivos eram:
1. Mostrar de forma gráfico a quantidade de questões e a quantidade de acertos obtido pelo usuário
1. Mostrar a porcentagem de acerto (rendimento) do com base nos dados fornecidos

Com isso tive a oportunidade de trabalhar com os dados fornecidos pelo usuário por meio do JavaScript. Assim como utilizar a biblioteca Plotly para a plotagem do gráfico.

## Principais desafios:

- Trabalhar com a linguagem JavaScript e entender sua sintaxe de forma a poder trabalhar minha lógica de programação e DOM
- Utilizar o CSS puro para poder realizar o layout da página (sem auxilio do bootstrap)
- Para deixar a página um pouco mais interativa, criei um Grid onde o usuário pode ter uma interação com as imagens disponibilizadas dentro da página.

### Tratando os dados:
1. Para o tratamento dos dados foi utilizado apenas um addEventListener onde recebia os dados do usuário
'''
const resultado = document.querySelector('#resultado')

        resultado.addEventListener("click", function (r) {
            r.preventDefault();

            const total = document.querySelector('#total');
            const total_valor = total.value;

            const acertos = document.querySelector('#acertos'); // seleco o input (elemento)
            const total_acertos = acertos.value; // (valor)

            const txt = document.querySelector('#information')
            const valortxt = document.createElement('p')
'''
2. Para validar os dados inseridos realizei uma pequena validação

'''

            if (total_valor === "" || total_acertos === "") { // se os campos estiverem vazios
                alert('[ERROR] Preencha os campos corretamente')
            } else if ((total_valor < 0) || (total_acertos < 0)) { // se o valor de questões for menor do que os de acertos
                alert('Desculpe, a quantidade de questões/acertos não pode ser negativa')
            } else { // o restante do código só será realizado apenas se todas as outras condições forem verdadeiras
'''

Desta forma, não ocorreria nenhum tipo de ação caso o usuário preenchesse o formulário de forma incorreta

## Deploy do Projeto:

https://cantaruttim.github.io/CalculandoRendimento/


