# mscopilot-creation

Repositório de demonstração de uso da ferramenta de criação de "agentes" do MS Copilot Studio, como parte do Curso de Formação em MS CoPilot Studio da DIO pelo professor Renato Romão.

À medida que formos avançando no curso, novas demonstrações e ferramentas serão exibidas nesse repositório.

## REQUISITOS:

Ter acesso a uma conta do M365
Ter um computador

## ETAPAS:

### DESAFIO #1:
   - Conectar/Criar uma conta no M365
     (https://copilotstudio.microsoft.com)
   - Criar um copiloto baseado em modelo (Viagens ou "Safe Travels")
   - Criar um copiloto baseado em descrição com IA
   - Criar um copiloto em branco

### DESAFIO #2:
   - Criar um copiloto em branco
   - Customizar um tópico
   - Personalizar uma mensagem de erro de tópico
   - Aumentar/Diminuir a qualidade da resposta com GenAI

## CRIAR UMA CONTA M365

Para criar uma conta M365, faça uma busca no Google sobre como criar uma conta gratuita do M365.

## CRIAR COPILOTOS

Acesse: https://copilotstudio.microsoft.com

## CRIAR UM COPILOTO BASEADO EM MODELO (VIAGENS)

Na seção 'Explorar agentes', clique em "Viagens Seguras" ("Safe Travels") e preencha os campos necessários à criação do Copiloto (nome, descrição e instruções). Por fim, clique no botão CRIAR.

## CRIAR UM COPILOTO BASEADO EM DESCRIÇÃO COM IA

Ver abaixo...

## CRIAR UM COPILOTO EM BRANCO

Para criação de um Copiloto baseado em IA ou em Branco, as instruções são bem semelhantes e intuitivas com base na descrição acima (Copiloto Baseado em Modelo).
Para criarmos um Copilot em branco, vamos na página do Copilot Studio ('https://copilotstudio.microsoft.com') e, na barra lateral esquerda, clicamos em 'Agents' e depois em '+ New Agent'.

Em seguida, damos um nome ao Agente ("Agente da DIO") e preenchemos os campos de 'Description' e 'Instructions'. A diferença entre eles é que o primeiro campo serve para descrevermos o que o ChatBot é responsável por fazer (por exemplo, "Agente responsável por buscar conteúdos de Copilot Studio dentro da documentação oficial da Microsoft, sendo que toda resposta dele será como o "Agente da DIO").

No campo de 'Instructions' a gente coloca o "prompt" para o Agente se basear. É onde definimos o tom, a linguagem, a "temperatura" (se mais ou menos criativo), se vai interagir com base em documentos, quais ações irá fazer...). Um exemplo:

```
   "Você é o agente chamado "Agente da DIO" e vai agir em tom formal com o idioma em português
   para retornar informações relevantes da documentação oficial da Microsoft, o Microsoft Learn.
   Ao retornar uma resposta para a pergunta do usuário, você deve considerar:
   - Buscar a melhor resposta da documentação;
   - Retornar a resposta apropriada e amigável em tom formal;
   - Retornar uma ou mais citações da documentação."
```

A parte do 'Knowledge' não precisa ser adicionada, pois está fora do desafio.

No canto superior do site, ao lado dos botões 'Create' e 'Cancel', podemos clicar nos '...' e, no pop-up que abrir, configuramos em qual Solução será armazenado o nosso ChatBot. No nosso caso, não utilizaremos.

Basta agora clicarmos no botão 'Create' e o nosso Copiloto estará criado.

## CUSTOMIZAR UM TÓPICO

Para customizarmos um tópico, selecionamos o nosso Agente ("Agente da DIO") e, na barra de ferramentas superior do site do Copilot Studio, clicamos em 'Topics'. Ao ser carregada a lista de tópicos disponíveis, clicamos em '+ Add a Topic' e clicamos na opção 'From blank'. Com isso, um fluxo de tópico será criado com um "card" inicial de gatilho ("Trigger"). Nele, haverá um campo com as frases ("Phrases") de gatilho que irão "disparar" o nosso Agente.

Clicando nas frases, uma aba de configuração será aberta para que possamos adicionar palavras ou frases de gatilho. Usaremos como exemplos:

   - 'buscar informações de ai builder'
   - 'o que é ai builder'
   - 'onde encontro informações da ferramenta de AI da Power Platform'

Finalizando a inserção dos gatilhos, clicamos no botão de '+' ('Add a node') abaixo do "card" dos gatilhos, clicamos na opção 'Advanced' e em 'Generative answers'. Com isso, um novo "card" será adicionado ao fluxo do nosso tópico. Clicamos no botão '>' do campo 'Input' e depois na opção 'System'. No campo de pesquisa, digitamos 'activity.text' e clicamos na variável listada abaixo do campo. Então, selecionamos a variável para ser adicionada como 'Input' do nosso "card" de Criação de Respostas Generativas.

Então, no campo 'Data sources', clicamos no link 'Edit' onde podemos configurar as fontes de dados que serão utilizadas pelo Agente para pesquisar o conteúdo solicitado pelo usuário. Porém, não faremos modificações.

O próximo passo é clicar no botão '+' ('Add a node') abaixo do "card" 'Create generative answers' e clicamos em 'Send message' para criarmos uma mensagem ao usuário: "Tópico de AI Builder encerrado!".

Por fim, no canto superior esquerdo do site do Copilot, logo abaixo do nome do nosso "Agente da DIO", clicamos no 'Untitled' para renomearmos o tópico para "AI Builder Topics' e, em seguida, clicamos no botão 'Save'.

Agora, no campo superior direito do site, clicamos no botão 'Test', reiniciamos a conversa no botão de "seta circular" e usamos o campo de digitação para interagirmos com o nosso Agente.

## PERSONALIZAR UMA MENSAGEM DE ERRO DE TÓPICO

Caso nosso Agente retorne algum erro, podemos customizar as mensagens clicando em 'Topics' na barra de ferramentas superior do site, depois clicamos em 'System' para listarmos os tópicos de sistema e clicamos no tópico 'Conversational boosting'. Será aberto o fluxo desse tópico.

Esse fluxo poderá ser editado para melhorarmos as mensagens de erro do tópico que estiverem aparecendo. Com os testes do Agente podemos verificar os erros que acontecem e fazer as edições necessárias.

Outra opção para melhorias nas mensagens de erro de tópico é utilizar o tópico de sistema 'Fallback'.

Para forçarmos uma mensagem de erro, entramos no 'Conversational boosting' e clicamos no botão 'Edit' do 'Data sources' e desabilitamos a opção 'Allow the AI to use its own general knowledge (preview)'. Isso faz com que o nosso Agente não consiga mais buscar conteúdo em sua base de conhecimento geral. Salvamos essa configuração, reiniciamos a conversa (clicando no botão de "seta circular") e fazemos uma "pergunta" esdrúxula como, por exemplo, "kajbnbadsblkadsjbadksjg".

Com isso, o usuário acaba "caindo" no tópico de sistema 'Conversational boosting' e é exibida para ele na conversa uma mensagem padrão "I'm sorry, I'm not sure how to help with that. Can you try rephrasing?". Abaixo dessa mensagem, é exibida uma outra mensagem somente para o desenvolvedor informando "No information was found that could help answer this", acompanhada de um botão 'Edit knowledge sources'. Isso é o próprio Copilot Studio informando que não conseguiu encontrar nenhuma informação para entregar para o usuário e sugerindo, através do botão, que editemos as bases de conhecimento do Agente.

Para personalizar essa mensagem de erro, vamos no fluxo do 'Conversational boosting' e, na condição 'All other conditions', vamos adicionar uma 'mensagem' (através do botão '+' de 'Add a node' e em 'Send a message') dizendo:

```
   "Olá, 'User.PrincipalName' !

   Desculpa, mas não foi possível encontrar a resposta que você estava esperando.
   Entre em contato pelo número (11) 9999-9999 ou contato@dio.com.br"
```

Clicamos em 'Save', reiniciarmos a conversa ("seta circular") e já podemos testar novamente.

## AUMENTAR/DIMINUIR A QUALIDADE DA RESPOSTA COM GEN AI

Para melhorarmos a qualidade das respostas do nosso Agente com as 'Respostas Generativas', entramos no tópico de sistema 'Conversational boosting' e, no "card" 'Create generative answers' clicamos no botão 'Edit' do campo 'Data sources'. Na aba de configuração que se abrir, podemos habilitar o botão 'Allow the AI to use its own general knowledge (preview)'. Essa opção permite que o Agente otimize as respostas com base em conteúdo buscado no GPT-4 (atualmente, em 2025). O conteúdo é trazido com base na atualização do banco de conhecimento dessa ferramenta. Então, pode haver alguma inconformidade por conta de alguma possível falta de atualização da informação.

Além disso, podemos customizar um prompt nessa mesma aba de configuração do 'Data sources' utilizando o campo '{x} fx' (variáveis e fórmulas). Por exemplo:

```
   '"Buscar dados do AI Builder com base na pergunta do usuário:" 'Activity.Text'"
```

ATENÇÃO: Esse campo '{x} fx' possui um limite de 8000 caracteres. Então, se utilizarmos variáveis e o conteúdo dessas variáveis somadas ao prompt que definimos passar de 8000 caracteres, o Agente falhará!

Também podemos customizar um nível de moderação do conteúdo marcando a opção 'Customize' da seção 'Content moderation level'. Se a moderação escolhida for alta ("High"), o Agente será o mais fiel possível ao conteúdo buscado pelo usuário. Isso porque, quando as bases de conhecimento são adicionadas a um Agente, o conteúdo que elas carregam será indexado pela IA e, ao ser buscado, será feita uma análise de probabilidade para criar um ranking de relevância que o conteúdo indexado tem em relação à pergunta do usuário. Se a moderação escolhida for alta, o Agente retornará informações coletadas somente em documentos com alta probabilidade de relevância. Se, ao contrário, for configurada uma moderação baixa ("Low"), o Agente dará ao usuário uma resposta com informações tanto fiéis (colhidas de documentos de alta relevância) quanto distantes do que o usuário perguntou (coletadas de documentos com baixa probabilidade de relevância).

Deixar a moderação em Alto nível faz com que a qualidade das respostas obtidas sejam as melhores possíveis.

Podemos fazer esse controle de moderação também atráves das configurações gerais do Agente. Para isso, clicamos em 'Settings' no canto superior direito do site, clicamos em 'Generative AI', habilitamos a opção 'Generative (preview)' e, mais abaixo, selecionamos o grau de moderação ("Low", "Medium" e "High").

Nesse caso, essa configuração será definida para o Agente criado independente do tópico onde ele esteja agindo. Já na configuração que mostramos anteriormente, a moderação será aplicada somente àquele tópico (e não ao Agente em todos os tópicos).

## LINKS ÚTEIS

- Microsoft Copilot Studio:
https://www.microsoft.com/pt-br/microsoft-copilot/microsoft-copilot-studio

- Microsoft Learn:
https://learn.microsoft.com/pt-br/microsoft-copilot-studio

- Microsoft Power Plataform:
https://www.microsoft.com/pt-br/power-platform

- Romão's Learn:
https://romaos.com.br/learn
