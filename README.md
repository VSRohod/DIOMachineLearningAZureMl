# DIOMachineLearningAZureMl
🚀 Desafio do modelo de previsão
- Etapas
1. Crie um novo repositório no github com um nome a sua preferência
2. Crie um modelo de previsão com seus devidos pontos de extremidade configurados
3. Escreva o passo a passo desse processo em um readme.md de como você chegou nessa etapa
4. Salve nesse repositório o readme.md e o arquivo .json de pontos de extremidade
5. Compartilhe conosco o link desse repositório através do botão 'entregar projeto'

<h1>Step by Step</h1>
-Logar no site da azure.
-Dentro da página home, acesse a opção "Create a resource".
-Acesse a categoria "AI + Machine Learning".
-Acesse a ferramenta "Azure Machine Learning" e selecione o botão "create.
-Aperte o botão "Create new" na aba Resource group (obs: pode colocar como termo "LABAI-900").

<h3>Worspace details</h3>
* Name = laboratorioai900
* Region = East US (No Brasil geralmente os recursos são mais caros!)
* Storage Account = generatedByName
* Key vault = generatedByName
* Application insights = generatedByName
* Container Registry = None

-Clique "Examine + Create".
-Clique em "Create".
-Assim que a implantação estiver concluída clique em "Go to resource".
-Dentro do lab clique em "Launch studio"
-Dentro do estúdio, nós iremos procurar pela opção "ML automatizado".
-Após selecionada a opção, clique em "Novo trabalho de ML automatizado".

<h3>Configurações básicas</h3>
* Nome do trabalho = mslearn-bike-automl
* Novo nome do experimento = mslearn-bike-rental
* Descrição = Aprendizado de máquina automatizado para previsão de aluguel de bicicletas
* Marcas = "None"

-Clique em "Avançar".
-Em "Tipo de tarefa e dados" selecionaremos o tipo de tarefa como "Regressão".
-Na aba de "Selecionar os dados" aperte em criar.

<h3>Definir o nome e o tipo do ativo de dados</h3>
* Nome = alugueldebicicletas
* Descrição = dados históricos de aluguel de bicicletas
* Tipo = tabular

-Clique em "Avançar".
-Em "Escolha uma fonte para o ativo de dados", selecione a opção "De arquivos da Web".
-Clique em "Avançar".
-Insira na textarea "URL da Web" o link "https://aka.ms/bike-rentals".
-Clique em "Avançar".

<h3>Configurações</h3>
* Formato do arquivo = Delimitado
* Delimitador = Vírgula
* Codificação = UTF-8 
* Cabeçalhos de coluna = Somente o primeiro arquivo tem cabeçalhos
*Ignorar linhas = Nenhuma

-Clique em "Avançar".
-Clique em "Avançar" novamente.
-Clique em "Criar".
-Na aba "Tipo de tarefa e dados" selecione a tarefa regressão e selecione no "Selecionar os dados" a opção "alugueldebicicletas"
-Clique em "Avançar".

<h3>Configurações de tarefas</h3>
* Tipo de tarefa = Regressão
* Dados = alugueldebicicletas
* Coluna de destino = rentals (Integer)
-Obs: clique em "Exibir definições de confirgurações adicionais"
* Métrica primária = NormalizedRootMeanSquaredError
* Explicar o modelo = false
* Habilitar empilhamento de ensemble = false
* Usar todos os modelos suportados = false
* Modelos permitidos = RandomForest e LightGBM

<h3>Limites</h3>
* Máximo de avaliações = 3
* Máximo de avaliações simultâneas = 3
* Máximo de nós = 3
* Limite de pontuação da métrica  = 0.085
* Tempo limite do experimento = 15
* Tempo limite de iteração = 15
* Habilitar encerramento antecipado = true

<h3>Validar e testar</h3>
* Tipo de validação = Divisão de validação de treinamento
* Validação de percentual de dados = 10
* Dados de teste = Nenhum

-Clique em "Avançar".

<h3>Computação</h3> 
* Selecione o tipo de computação = Sem servidor
* Tipo de máquina virtual = CPU
* Tipo de máquina virtual = Dedicado
* Tamanho da máquina virtual = Standard_DS3_v2 (4 núcleo(s), 14GB de RAM, 28 GB de armazenamento, $0.29/hr)
* Número de Instâncias = 1

-Clique em "Enviar trabalho de treinamento".
-Espere o processo finalizar.
-Finalizado o processo podemos visitar a aba "Tarefas (Jobs)" no menu lateral e procurar por "mslearn-bike-rentals"
-Clicando nele veremos todo o histórico de como ele foi concluído!
-Vamos visitar a aba "Modelos" no menu lateral

Obs : caso não apareça o modelo!
-Voltando para a opção "ML automatizado" e clicando em "mslearn-bike-automl"
-Visite a opção "Modelos + trabalhos filho"
-Selecione a opção "MaxAbsScaler,LightGBM"
-Clique em implantar e logo em seguida selecione a opção "Serviço Web"
<!-- https://github.com/toniacprado/DIO-Trabalhando-com-Machine-Learning-na-Pratica-no-Azure-ML SOLUÇÃO PARA A FALTA DO MODELO -->