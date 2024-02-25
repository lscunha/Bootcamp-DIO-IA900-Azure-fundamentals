
   
# Azure Cognitive Search: Utilizando AI Search para indexação e consulta de dados


## O que precisa ser feito?

O desafio propõe que seja criada uma pesquisa que funcione juntamente com um serviço de inteligência artificial para identificar palavras chave e sentimentos (utilizando também o serviço de armazenamento do Azure).

[Documentação](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html)

## Primeira etapa: Criando recurso do Azure AI Search   

01 - Clique em "Azure AI Search" e vá em "Criar"

<img align="right" src="./inputs/1.jpg" width=""/> 

02 - Configure dessa maneira (altere o nome do recurso para a maneira que preferir)
<img align="right" src="./inputs/2.jpg" width=""/> 

03 - Aguarde terminar a implantação
<img align="right" src="./inputs/3.jpg" width=""/> 

## Segunda etapa: Criando recurso do Azure AI Services  

01 - Clique em "Serviços Cognitivos" e configure da maneira que já vimos anteriormente nos LAB's anteriores
<img align="right" src="./inputs/4.jpg" width=""/>

02 - Aguarde implantação
<img align="right" src="./inputs/5.jpg" width=""/>

## Terceira etapa: Criando o armazenamento (storage) 

01 - Clique na opção "Contas de armazenamento"
<img align="right" src="./inputs/6.jpg" width=""/>

02 - Em seguida, vamos na opção "Criar"
<img align="right" src="./inputs/7.jpg" width=""/>

03 - Configure dessa maneira (se surgir alguma dúvida, consulte a documentação linkada acima), clique em "Examinar", avance e clique em "Criar"
<img align="right" src="./inputs/8.jpg" width=""/>

## Quarta etapa: Permitindo acesso anônimo ao Blob  

Como nosso laboratório é apenas didático (com o objetivo de aprender os princípios da inteligência artificial com o Azure), precisamos permitir o acesso anônimo ao blob para simplificar e facilitar nossas implementações!

01 - Após criar o armazenamento, entre no mesmo e navegue até a guia "Configurações" e clique em "Configuração", marcando as opções abaixo. Logo após, clique em "Salvar":
<img align="right" src="./inputs/9.jpg" width=""/>

## Quinta etapa: Criando o container 

01 - Ainda dentro do armazenamento que foi criado, navegue até a aba "Armazenamento de dados" e selecione a opção "contêineres". E então, clique na opção "+Contêiner":
<img align="right" src="./inputs/10.jpg" width=""/>

02 - Logo em seguida, preencha a aba "Nome" com "coffeereviews" e configure da maneira que está exposta na imagem abaixo:
<img align="right" src="./inputs/11.jpg" width=""/>

## Sexta etapa: Carregar o Blob

01 - Selecione o contêiner que foi criado (nesse caso, "coffeereviews"):
<img align="right" src="./inputs/12.jpg" width=""/>

02 - Na nova página, vá na opção "Carregar": 
<img align="right" src="./inputs/13.jpg" width=""/>

03 - Faça o download dos arquivos na documentação linkada acima e, logo em seguida, faça o upload dos arquivos baixados:
<img align="right" src="./inputs/14.jpg" width=""/>

## Sétima etapa: Importação e indexação dos dados

01 - Voltamos para o AI Search, selecione o elemento criado e então clique na opção "Importar dados":
<img align="right" src="./inputs/15.jpg" width=""/>

02 - Na próxima etapa, em "Conectar a seus dados", na parte "Fonte de dados", selecione "Armazenamento de Blob do Azure":
<img align="right" src="./inputs/16.jpg" width=""/>




05 - Daqui para frente, recomendo que siga a [documentação](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html) para facilitar a compreensão dos passos necessários! Vá até o passo 17 e então volte para continuarmos :)

## Última etapa: Consulta ao índice

01 - Depois de importamos os dados, chegou o momento da última etapa. Vamos na opção "Gerenciador de pesquisa":
<img align="right" src="./inputs/17.jpg" width=""/>

02 - Logo em seguida, vamos utilizar um comando que vai verificar se a indexação foi feita corretamente e mostra os documentos:
<img align="right" src="./inputs/18.jpg" width=""/>

OBS: copie e cole o código abaixo
```
search=*&$count=true 
```

03 - Com outro código, verificamos as ocorrências que aconteceram em Chicago:
<img align="right" src="./inputs/19.jpg" width=""/>


```


## O que foi observado:  

É impressionante o poder das ferramentas do Microsoft Azure! Facilitam a consulta em documentos, pesquisas e depoimentos, facilitando demais o processo de filtrar determinadas situações.