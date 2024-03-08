# DIOMachineLearningAZureMl
🚀 Desafio do modelo de previsão
- Etapas
1. Crie um novo repositório no github com um nome a sua preferência
2. Crie um modelo de previsão com seus devidos pontos de extremidade configurados
3. Escreva o passo a passo desse processo em um readme.md de como você chegou nessa etapa
4. Salve nesse repositório o readme.md e o arquivo .json de pontos de extremidade
5. Compartilhe conosco o link desse repositório através do botão 'entregar projeto'

<h1>💻Step by Step💻</h1>
<ul>
  <li>Logar no site da azure.</li>
  <li>Dentro da página home, acesse a opção "Create a resource".</li>
  <li>Acesse a categoria "AI + Machine Learning".</li>
  <li>Acesse a ferramenta "Azure Machine Learning" e selecione o botão "create.</li>
  <li>Aperte o botão "Create new" na aba Resource group (obs: pode colocar como termo "LABAI-900").</li>
  
<br> 
<table>
  <tr><th><h3>Worspace details</h3></th></tr>
  <tr><td>* Name = laboratorioai900</td></tr>
  <tr><td>* Region = East US (No Brasil geralmente os recursos são mais caros!)</td></tr>
  <tr><td>* Storage Account = generatedByName</td></tr>
  <tr><td>* Key vault = generatedByName</td></tr>
  <tr><td>* Application insights = generatedByName</td></tr>
  <tr><td>* Container Registry = None</td></tr>
</table>
<br>

<li>Clique "Examine + Create".</li>
<li>Clique em "Create".</li>
<li>Assim que a implantação estiver concluída clique em "Go to resource".</li>
<li>Dentro do lab clique em "Launch studio"</li>
<li>Dentro do estúdio, nós iremos procurar pela opção "ML automatizado".</li>
<li>Após selecionada a opção, clique em "Novo trabalho de ML automatizado".</li>

<br>
<table>
  <tr><th><h3>Configurações básicas</h3></th></tr>
  <tr><td>* Nome do trabalho = mslearn-bike-automl</td></tr>
  <tr><td>* Novo nome do experimento = mslearn-bike-rental</td></tr>
  <tr><td>* Descrição = Aprendizado de máquina automatizado para previsão de aluguel de bicicletas</td></tr>
  <tr><td>* Marcas = "None"</td></tr>
</table>
<br>

<li>Clique em "Avançar".</li>
<li>Em "Tipo de tarefa e dados" selecionaremos o tipo de tarefa como "Regressão".</li>
<li>Na aba de "Selecionar os dados" aperte em criar.</li>

<br>
<table>
  <tr><th><h3>Definir o nome e o tipo do ativo de dados</h3></th></tr>
  <tr><td>* Nome = alugueldebicicletas</li></td></tr>
  <tr><td>* Descrição = dados históricos de aluguel de bicicletas</li></td></tr>
  <tr><td>* Tipo = tabular</li></td></tr>
</table>
<br>

<li>Clique em "Avançar".</li>
<li>Em "Escolha uma fonte para o ativo de dados", selecione a opção "De arquivos da Web".</li>
<li>Clique em "Avançar".</li>
<li>Insira na textarea "URL da Web" o link "https://aka.ms/bike-rentals".</li>
<li>Clique em "Avançar".</li>

<br>
<table>
  <tr><th><h3>Configurações</h3></th></tr>
  <tr><td>* Formato do arquivo = Delimitado</li></td></tr>
  <tr><td>* Delimitador = Vírgula</li></td></tr>
  <tr><td>* Codificação = UTF-8 </li></td></tr>
  <tr><td>* Cabeçalhos de coluna = Somente o primeiro arquivo tem cabeçalhos</li></td></tr>
  <tr><td>*Ignorar linhas = Nenhuma</li></td></tr>
</table>
<br>

<li>Clique em "Avançar".</li>
<li>Clique em "Avançar" novamente.</li>
<li>Clique em "Criar".</li>
<li>Na aba "Tipo de tarefa e dados" selecione a tarefa regressão e selecione no "Selecionar os dados" a opção "alugueldebicicletas"</li>
<li>Clique em "Avançar".</li>

<br>
<table>
  <tr><th><h3>Configurações de tarefas</h3></th></tr>
  <tr><td>* Tipo de tarefa = Regressão</td></tr>
  <tr><td>* Dados = alugueldebicicletas</td></tr>
  <tr><td>* Coluna de destino = rentals (Integer)</td></tr>
  <tr><td>-Obs: clique em "Exibir definições de confirgurações adicionais"</td></tr>
  <tr><td>* Métrica primária = NormalizedRootMeanSquaredError</td></tr>
  <tr><td>* Explicar o modelo = false</td></tr>
  <tr><td>* Habilitar empilhamento de ensemble = false</td></tr>
  <tr><td>* Usar todos os modelos suportados = false</td></tr>
  <tr><td>* Modelos permitidos = RandomForest e LightGBM</td></tr>
</table>
<br>

<table>
  <tr><th><h3>Limites</h3></th></tr>
  <tr><td>* Máximo de avaliações = 3</td></tr>
  <tr><td>* Máximo de avaliações simultâneas = 3</td></tr>
  <tr><td>* Máximo de nós = 3</td></tr>
  <tr><td>* Limite de pontuação da métrica  = 0.085</td></tr>
  <tr><td>* Tempo limite do experimento = 15</td></tr>
  <tr><td>* Tempo limite de iteração = 15</td></tr>
  <tr><td>* Habilitar encerramento antecipado = true</td></tr>
</table>
<br>

<table>
  <tr><th><h3>Validar e testar</h3></th></tr>
  <tr><td>* Tipo de validação = Divisão de validação de treinamento</td></tr>
  <tr><td>* Validação de percentual de dados = 10</td></tr>
  <tr><td>* Dados de teste = Nenhum</td></tr>
</table>
<br>

<li>Clique em "Avançar".</li>

<br>
<table>
  <tr><th><h3>Computação</h3></th></tr>
  <tr><td>* Selecione o tipo de computação = Sem servidor</td></tr>
  <tr><td>* Tipo de máquina virtual = CPU</td></tr>
  <tr><td>* Tipo de máquina virtual = Dedicado</td></tr>
  <tr><td>* Tamanho da máquina virtual = Standard_DS3_v2 (4 núcleo(s), 14GB de RAM, 28 GB de armazenamento, $0.29/hr)</td></tr>
  <tr><td>* Número de Instâncias = 1</td></tr>
</table>
<br>

<li>Clique em "Enviar trabalho de treinamento".</li>
<li>Espere o processo finalizar.</li>
<li>Finalizado o processo podemos visitar a aba "Tarefas (Jobs)" no menu lateral e procurar por "mslearn-bike-rentals"</li>
<li>Clicando nele veremos todo o histórico de como ele foi concluído!</li>
<li>Vamos visitar a aba "Modelos" no menu lateral</li>

Obs : caso não apareça o modelo!
<li>Voltando para a opção "ML automatizado" e clicando em "mslearn-bike-automl"</li>
<li>Visite a opção "Modelos + trabalhos filho"</li>
<li>Selecione a opção "MaxAbsScaler,LightGBM"</li>
<li>Clique em implantar e logo em seguida selecione a opção "Serviço Web"</li>

<br>
<table>
  <tr><th><h3>Implantar um modelo</h3></th></tr>
  <tr><td>* Nome = predict-rentals</td></tr>
  <tr><td>* Descrição = Lab da DIO</td></tr>
  <tr><td>* Tipo de computação = Instância de Conteiner do Azure</td></tr>
  <tr><td>* Habilitar autenticação = true</td></tr>
</table>
<br>

<li>Clique em "Implantar"</li>
<li>Aguarde média de 15 min e confira a aba de modelos</li>
<li>Clique em pontos de extremidade e logo após na opção "Testar"</li>

<h2>O resultado dos pontos de extremidade serão anexados dentro do Json anexado ao repositório!</h2>
</ul>
