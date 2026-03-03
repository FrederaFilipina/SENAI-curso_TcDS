# Aula 01
> Iniciando a revisão sobre fundamentos de React

### Componentização: É uma estratégia arquitetural que divide sistemas e interfaces em unidades menores, independentes e reutilizáveis chamada de: `componentes`

##

### ▷ Preparando os arquivos para iniciar o projeto:
- Deletar o que já vêm pronto quando se cria o arquivo React do projeto;

    - Deletar o `conteúdo`;

        1. Abrir o arquivo: *`App.jsx`* (arquivo que recebe, organiza e estrutura como todo os componentes do projeto vão se comportar);

        2. Selecione todo o código existente e delete;

        3. Crie a estrutura que vai receber todos os componentes:

            - Utilize uma função do tipo *`Function Statement`* ou *`Function Declaration`* com o nome do arquivo, que retorne um `Fragmento: <> </>` vazio a ser exportado no final, utilizando o *`export default`*
                            
                    1.  function App() {
                    2.      return (
                    3.          <>
                    4.          </>
                    5.      )
                    6.  }
                    7.  export default App

    - Deletar a `estilização`;

        1. Abrir o arquivo: *`index.css`* (arquivo que recebe a estilização da aparência da página onde os componentes serão renderizados);

        2. Selecione todo o código existente e delete;

        3. Defina a estilização base padrão que vai ser aplicada a página:

            - Utilize o *`*`* (seletor universal no CSS, age sobre os demais elementos) para padronizar a margem, o espaçamento e a forma como o tamanho dos elementos acabam sendo calculado
                    
                    1.  *{
                    2.      margin: 0;
                    3.      padding: 0;
                    4.      box-sizing: border-box;
                    5.  }
<br><br>

### ▷ Definindo a estrutura de `Componentização`:
- Criar a hierarquia de pastas e subpastas;

    - Abra a pasta `src` (abreviação de *source* = fonte, ou seja, é a pasta onde o código fonte é armazenado);

        1. Crie a pasta *`layouts`* que vai agrupar as subpastas que compões os componentes a serem utilizados;
        
        2. Crie a subpasta *`Header`* (cabeçalho) que vai armazenar os arquivos que compõem o componente;
        
        3. Crie os arquivos:
            - `index.jsx` (contem toda as informações do componente)
            - NomeDaPasta`.module.css` (contem toda estilização do componente)

                    📁 src
                        📂 layouts
                            📁 Header
                                ↪ Header.module.css
                                ↪ index.jsx
<br><br>

### ▷ Criando e configurando o `Componente`:
- Criar a estrutura e definir o conteúdo do componente;
    
    - Abra o arquivo `index.jsx`

        1. Crie a estrutura:

            - Utilize uma *`Arrow function`* com *`const`*, forma segura de guardar uma função dentro de uma variavel, com a garantia de que ela não será sobrescrita);

                    01.     const Header = () => {
                    02.         return (
                    03.             <>
                    04.          
                    05.             </>
                    06.         )
                    07.     }
                    08.     export default Header

        2. Defina o conteúdo:

            - Utilize a *tag*: *`header`* para definir o cabeçalho e `<h1>` para título;

                    01.     const Header = () => {
                    02.         return (
                    03.             <header>
                    04.                 <h1> Título <h1>
                    05.             </header>
                    06.         )
                    07.     }
                    08.     export default Header


- Definir onde a estilização ira agir e incluir a conexão com o arquivo da estilização;

    - Selecione a *tag* que englobe todo o componente

        1. Crie  o atributo e o objeto:          

            - Utilize o atributo:*`className`*, usado para aplicar classes CSS aos elementos JSX;

            - Utilize dentro do atributo, o objeto: *`styles.nomeReferência`*, objeto de estilos gerado pelos CSS Modules;

                    01.     const Header = () => {
                    02.         return (
                    03.             <header className={styles.Header}>
                    04.
                    05.                 <h1>Título</h1>
                    06.
                    07.             </header>
                    08.         )
                    09.     }
                    10.     export default Header

        2. Crie a conexão com o arquivo: *`Header.module.css`*, onde a estilização é definida:
            
            - Importando a estilização;

                    01.     import styles from './Header.module.css'
                    02.
                    03.         return (
                    04.             <header className={styles.Header}>
                    05.
                    06.                 <h1>Título</h1>
                    07.
                    08.             </header>
                    09.         )
                    10.     }
                    11.     export default Header

- Definir a estilização do componente

    - Abra o arquivo *`Header.module.css`*;

        1. Defina a clase onde vão ficar as configurações da estilização:

            -  Utilize o *`ponto (.)`* parar criar a classe *`Header`*, o nome deve ser igual ao usado no objeto *`styles.`* do componente que vai receber a estilização

                    01.     .Header{
                    02.    
                    03.     }
            
        2. Crie a estilização:

            - Utilize: *`background-color`* para definir a cor de fundo, *`color`* para a cor da fonte; *`padding`* para espaçamento e *`text-align`* para definir o alinhamento do texto;

                    01.     .Header{
                    02.         background-color: #ff00ff;
                    03.         color: #ffffff;
                    04.         padding: 20px;
                    05.         text-align: center;
                    06.     }


### ▷ Usando o componente