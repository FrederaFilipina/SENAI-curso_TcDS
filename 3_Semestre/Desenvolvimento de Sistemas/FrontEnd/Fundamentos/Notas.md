## Passo a Passo e anotações....


### Criando e manuseando um projeto:

1. Criar, nomear e configurar o projeto:
    - Crie uma pasta onde o seu projeto será salvo;
    - Abra o terminal dentro desta pasta:
        1. Digite o comando: *`npm create vite@latest`*;
        2. Escolhe o nome do projeto, vai ser criado uma pasta com esse nome;
        3. Selecione o framework: *`React`* (é a biblioteca em que o projeto vai ser criado);
        4. Selecione a linguagem: *`JavaScript`*;
        5. Selecione: *`No`*, para não usar a versão Vite 8 beta;
        6. Selecione: *`Yes`*, para ele já instalar e executar o comando: *`npm run dev`* (comando para executar o projeto em modo de desenvolvimento), nesse ponto ele já vai passar automaticamente para o terminal da pasta do projeto;
        7. Clique no link que vai estar em:  ➜  Local, ele vai abrir o projeto no navegador;

2. Fechando e reabrindo o projeto em modo desenvolvimento:
    - Fechando o projeto:
        1. Abra o terminal dentro da pasta do projeto;
        2. No teclado de o comando: *`ctrl + c`*, isso faz com que o projeto seja parado de rodar;
    - Reabrindo o projeto:
        1. Abra o terminal dentro da pasta do projeto;
        2. Execute o comando: *`npm run dev`*;
        3. Clique no link que vai estar em:  ➜  Local, ele vai abrir o projeto no navegador;

3. Reabrindo o projeto em modo desenvolvimento após baixar o mesmo do *`Github`*;
    - Reabrindo o projeto:
        1. Abra o terminal dentro da pasta do projeto;
        2. No teclado de o comando: *`npm i`*, isso faz com que o projeto seja inicializado com todas as dependências instaladas;
        3. Execute o comando: *`npm run dev`*;
        4. Clique no link que vai estar em:  ➜  Local, ele vai abrir o projeto no navegador;
---

### Aula 01

1. Apagando as informações e formatação da página:
    - Abra o arquivo: *`App.jsx`* (conjunto de informações previamente carregada)
        1. Selecione tudo que stá dentro e delete;
        2. Crie uma função com o nome do arquivo, que retorne um fragmento vazio a ser exportado;
    - Abra o arquivo: *`indesx.css`* (conjunto de formatação previamente carregada)
        1. Selecione tudo que stá dentro e delete;
        2. Insira essas instruções:
            - *{ margin: 0; padding: 0; box-sizing: border-box; }

2. Criando  e configurando a estrutura de componentização:
    - Crie uma subpasta: *`layouts`*(vai agrupar componentes da estrutura da página) dentro da pasta: *`src`*;
    - Crie uma pasta: *`Header`* para armazenar os arquivos que compoem este componente;
    - Crie dentro desta pasta esses dois arquivos:
        1. *`index.jsx`* (local onde o vai estar toda a informação do componente);
        2. *`Header.module.css`* (local onde vai estar toda a formatação do componente);
    - Configure o que este componente vai ter:
        1. Crie uma função com o nome da pasta, que retorne as inormações deste componente a exportado;
        2. Passe a informação do *`className={styles.NOME}`* dentro do elemento que engloba toda a informação do componente e faça a conecção com o arquivo: `*Header.module.css*`;
        3. Monte todo o conteudo do componente;
    - Configure a formatação que o componente vai ter;

3. Utilizando o componente:
    - Abra o arquivo onde tudo vai ser mostrado: *`App.jsx`*
    - Dentro do fragmento, digite o nome da pasta do componente: <Header />
     
