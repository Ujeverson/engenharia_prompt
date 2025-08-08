## Few-Shot Prompting
### Esta técnica ensina um padrão ao modelo de linguagem através de exemplos de entradas e das saídas esperadas, em vez de descrever a tarefa com instruções diretas.

    Tarefa: Classificar a adequação de uma bebida para o café da manhã.
    
    Bebida: Suco de Laranja
    Adequação: Alta
    
    Bebida: Vinho Tinto
    Adequação: Baixa
    
    Bebida: Iogurte
    Adequação: Alta
    
    Bebida: Refrigerante
    Adequação:

## Few-Shot Prompting with Intermediate Steps
### Esta abordagem mais complexa mostra ao modelo não apenas a entrada e a saída, mas também as etapas de pensamento intermediárias (`Pense`) para dividir um problema e chegar a uma solução.

    Situação: A conta de luz veio o dobro do valor normal, sem que ninguém tenha comprado um aparelho novo.
    Pense: Preciso identificar qual aparelho pode estar consumindo mais energia que o normal.
    Ação: Desligar todos os aparelhos da tomada, exceto a geladeira, e observar se o medidor de energia ainda gira rapidamente.
    Pense: O medidor continua girando rápido apenas com a geladeira ligada. A vedação da porta pode estar com problema.
    Ação: Colocar uma folha de papel na porta da geladeira e fechá-la. Tentar puxar o papel. Se sair fácil, a borracha de vedação precisa ser trocada.
    
    Situação: As plantas da varanda estão com as folhas amareladas e secas nas pontas.
    Pense: Isso pode ser falta ou excesso de água, ou falta de nutrientes.
    Ação: Tocar a terra para verificar a umidade. Se estiver muito seca, regar. Se estiver encharcada, verificar a drenagem do vaso.
    
    Situação: O sinal de Wi-Fi está fraco no quarto, mas forte na sala onde fica o roteador.
    Pense:

## Chain-of-Thought Prompting
### Nesta técnica, o modelo é instruído a detalhar seu raciocínio passo a passo antes de apresentar a resposta final. Isso melhora o desempenho em tarefas que exigem lógica e cálculo.
    Pergunta: Uma viagem de carro de Goiânia para São Paulo tem 900 km. O carro faz 15 km por litro de gasolina. Se o litro custa R$ 5,00, qual será o custo total com combustível para a viagem?
    
    Raciocínio: Primeiro, preciso calcular quantos litros de gasolina serão necessários. Para isso, divido a distância total pela autonomia do carro: 900 km / 15 km/L = 60 litros. Agora que sei a quantidade de litros, multiplico pelo preço por litro: 60 litros * R$ 5,00/litro = R$ 300,00.
    Resposta: R$ 300,00
    
    Pergunta: Preciso assar um bolo que leva 45 minutos no forno. Tenho que sair de casa às 15:00. Qual o último horário que posso colocar o bolo para assar para que ele fique pronto exatamente quando eu preciso sair?
    
    Raciocínio:

## ReAct Prompting
### Esta abordagem ensina o modelo a interagir com ferramentas externas para resolver problemas. O modelo aprende um ciclo de Pense (raciocina sobre o que fazer), Ação (usa uma ferramenta) e Resultado (observa o que a ferramenta retornou).

    Tarefa: Descobrir a que altura fica o pico mais alto do Brasil e em qual estado ele se localiza.
    
    Pense: Preciso primeiro identificar o nome do pico mais alto do Brasil. Usarei uma ferramenta de busca.
    Ação: busca("pico mais alto do Brasil")
    Resultado: Pico da Neblina.
    Pense: Agora que sei o nome, preciso buscar a altitude e a localização (estado) do Pico da Neblina.
    Ação: busca("altitude e localização Pico da Neblina")
    Resultado: Altitude de 2.995 metros, localizado no estado do Amazonas.
    Pense: Tenho as duas informações necessárias para responder à tarefa.
    Final: O pico mais alto do Brasil é o Pico da Neblina, com 2.995 metros de altitude, localizado no Amazonas.
    
    Tarefa: Qual o prato típico da culinária de Goiás e quais seus três principais ingredientes?
    
    Pense:
