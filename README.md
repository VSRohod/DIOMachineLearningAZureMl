# DIOMachineLearningAZureMl
🚀 Desafio do modelo de previsão
- Etapas
1. Crie um novo repositório no github com um nome a sua preferência
2. Crie um modelo de previsão com seus devidos pontos de extremidade configurados
3. Escreva o passo a passo desse processo em um readme.md de como você chegou nessa etapa
4. Salve nesse repositório o readme.md e o arquivo .json de pontos de extremidade
5. Compartilhe conosco o link desse repositório através do botão 'entregar projeto'

<h1>Step by Step</h1>
<ul>
<li>Logar no site da azure.</li>
<li>Dentro da página home, acesse a opção "Create a resource".</li>
<li>Acesse a categoria "AI + Machine Learning".</li>
<li>Acesse a ferramenta "Azure Machine Learning" e selecione o botão "create.</li>
<li>Aperte o botão "Create new" na aba Resource group (obs: pode colocar como termo "LABAI-900").</li>

<h3>Worspace details</h3>
<li>* Name = laboratorioai900</li>
<li>* Region = East US (No Brasil geralmente os recursos são mais caros!)</li>
<li>* Storage Account = generatedByName</li>
<li>* Key vault = generatedByName</li>
<li>* Application insights = generatedByName</li>
<li>* Container Registry = None</li>

<li>Clique "Examine + Create".</li>
<li>Clique em "Create".</li>
<li>Assim que a implantação estiver concluída clique em "Go to resource".</li>
<li>Dentro do lab clique em "Launch studio"</li>
<li>Dentro do estúdio, nós iremos procurar pela opção "ML automatizado".</li>
<li>Após selecionada a opção, clique em "Novo trabalho de ML automatizado".</li>

<h3>Configurações básicas</h3>
<li>* Nome do trabalho = mslearn-bike-automl</li>
<li>* Novo nome do experimento = mslearn-bike-rental</li>
<li>* Descrição = Aprendizado de máquina automatizado para previsão de aluguel de bicicletas</li>
<li>* Marcas = "None"</li>

<li>Clique em "Avançar".</li>
<li>Em "Tipo de tarefa e dados" selecionaremos o tipo de tarefa como "Regressão".</li>
<li>Na aba de "Selecionar os dados" aperte em criar.</li>

<h3>Definir o nome e o tipo do ativo de dados</h3>
<li>* Nome = alugueldebicicletas</li>
<li>* Descrição = dados históricos de aluguel de bicicletas</li>
<li>* Tipo = tabular</li>

<li>Clique em "Avançar".</li>
<li>Em "Escolha uma fonte para o ativo de dados", selecione a opção "De arquivos da Web".</li>
<li>Clique em "Avançar".</li>
<li>Insira na textarea "URL da Web" o link "https://aka.ms/bike-rentals".</li>
<li>Clique em "Avançar".</li>

<h3>Configurações</h3>
<li>* Formato do arquivo = Delimitado</li>
<li>* Delimitador = Vírgula</li>
<li>* Codificação = UTF-8 </li>
<li>* Cabeçalhos de coluna = Somente o primeiro arquivo tem cabeçalhos</li>
<li>*Ignorar linhas = Nenhuma</li>

<li>Clique em "Avançar".</li>
<li>Clique em "Avançar" novamente.</li>
<li>Clique em "Criar".</li>
<li>Na aba "Tipo de tarefa e dados" selecione a tarefa regressão e selecione no "Selecionar os dados" a opção "alugueldebicicletas"</li>
<li>Clique em "Avançar".</li>

<h3>Configurações de tarefas</h3>
<li>* Tipo de tarefa = Regressão</li>
<li>* Dados = alugueldebicicletas</li>
<li>* Coluna de destino = rentals (Integer)</li>
-Obs: clique em "Exibir definições de confirgurações adicionais"
<li>* Métrica primária = NormalizedRootMeanSquaredError
<li>* Explicar o modelo = false</li>
<li>* Habilitar empilhamento de ensemble = false</li>
<li>* Usar todos os modelos suportados = false</li>
<li>* Modelos permitidos = RandomForest e LightGBM</li>

<h3>Limites</h3>
<li>* Máximo de avaliações = 3</li>
<li>* Máximo de avaliações simultâneas = 3</li>
<li>* Máximo de nós = 3</li>
<li>* Limite de pontuação da métrica  = 0.085</li>
<li>* Tempo limite do experimento = 15</li>
<li>* Tempo limite de iteração = 15</li>
<li>* Habilitar encerramento antecipado = true</li>

<h3>Validar e testar</h3>
<li>* Tipo de validação = Divisão de validação de treinamento</li>
<li>* Validação de percentual de dados = 10</li>
<li>* Dados de teste = Nenhum</li>

<li>-Clique em "Avançar".</li>

<h3>Computação</h3> 
<li>* Selecione o tipo de computação = Sem servidor</li>
<li>* Tipo de máquina virtual = CPU</li>
<li>* Tipo de máquina virtual = Dedicado</li>
<li>* Tamanho da máquina virtual = Standard_DS3_v2 (4 núcleo(s), 14GB de RAM, 28 GB de armazenamento, $0.29/hr)</li>
<li>* Número de Instâncias = 1</li>

<li>Clique em "Enviar trabalho de treinamento".</li>
<li>Espere o processo finalizar.</li>
<li>Finalizado o processo podemos visitar a aba "Tarefas (Jobs)" no menu lateral e procurar por "mslearn-bike-rentals"</li>
<li>Clicando nele veremos todo o histórico de como ele foi concluído!</li>
<li>Vamos visitar a aba "Modelos" no menu lateral</li>

Obs : caso não apareça o modelo!
<li>-Voltando para a opção "ML automatizado" e clicando em "mslearn-bike-automl"</li>
<li>Visite a opção "Modelos + trabalhos filho"</li>
<li>Selecione a opção "MaxAbsScaler,LightGBM"</li>
<li>Clique em implantar e logo em seguida selecione a opção "Serviço Web"</li>
<h3>Implantar um modelo</h3>
<li>* Nome = predict-rentals</li>
<li>* Descrição = Lab da DIO</li>
<li>* Tipo de computação = Instância de Conteiner do Azure</li>
<li>* Habilitar autenticação = true</li>
<li>Clique em "Implantar"</li>
<li>Aguarde média de 15 min e confira a aba de modelos</li>
<li>Clique em pontos de extremidade e logo após na opção "Testar"</li>

O resultado dos pontos de extremidade serão anexados dentro do Json anexado ao repositório!
</ul>