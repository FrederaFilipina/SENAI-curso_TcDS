# Aula 01
> Iniciando a revisão sobre fundamentos de React

### Componentização: É uma estratégia arquitetural que divide sistemas e interfaces em unidades menores, independentes e reutilizáveis chamada de: *`componentes`*

##

### ▷ Preparando os arquivos para iniciar o projeto:
- Deletar o que já vêm pronto quando se cria o arquivo React do projeto;

    - Deletar o `conteúdo`;

        1. Abrir o arquivo: *`App.jsx`* (arquivo que recebe, organiza e estrutura como todo os componentes do projeto vão se comportar);

        2. Selecione todo o código existente e delete;

        3. Crie a estrutura que vai receber todos os componentes:

            - Utilize uma função do tipo *`Function Statement`* ou *`Function Declaration`* com o nome do arquivo, que retorne um `Fragmento: <> </>` vazio a ser exportado no final, utilizando o *`export default`*
                            
                    function App() {
                        return (
                            <>
                            </>
                        )
                    }
                    export default App

    - Deletar a `formatação`;

        1. Abrir o arquivo: *`index.css`* (arquivo que recebe a formatação da aparência da página onde os componentes serão renderizados);

        2. Selecione todo o código existente e delete;

        3. Defina a formatação base padrão que vai ser aplicada a página:

            - Utilize o *`*`* (seletor universal no CSS, age sobre os demais elementos) para padronizar a margem, o espaçamento e a forma como o tamanho dos elementos acabam sendo calculado
                    *{
                        margin: 0;
                        padding: 0;
                        box-sizing: border-box;
                    }
<br><br>

### ▷ Definindo a estrutura de `Componentização`:
- Criar a hierarquia de pastas e subpastas;

    - Abra a pasta `src` (abreviação de *source* = fonte, ou seja, é a pasta onde o código fonte é armazenado);

        1. Crie a pasta *`layouts`* que vai agrupar as subpastas que compões os componentes a serem utilizados;
        
        2. Crie a subpasta *`Header`* (cabeçalho) que vai armazenar os arquivos que compõem o componente;
        
        3. Crie os arquivos:
            - `index.jsx` (contem toda as informações do componente)
            - NomeDaPasta`.module.css` (contem toda formatação do componente)

                    📁 src
                        📂 layouts
                            📁 Header
                                ↪ Header.module.css
                                ↪ index.jsx
<br><br>

### ▷ Criando e configurando o `Componente`:
- Criar a estrutura que vai receber o conteúdo do componente;
    
    - Abra o arquivo `index.jsx`
        1. Crie a estrutura:
            - Use uma *`Arrow function com const`* 🔎(é uma forma segura de guardar uma função com a garantia de que ela não será sobrescrita)🖊;

- Definir o conteúdo que vai ser exportado;

- Criar a forma como a formatação vi ser importada;










---




### ▷ Criando e configurando o *`componente`*:
1. Abra o arquivo: *`index.jsx`*;

2. Crie o esqueleto e define o conteúdo do componente:
    - Criando o esqueleto:

        - Use uma *`Arrow function com const`* 🔎(é uma forma segura de guardar uma função com a garantia de que ela não será sobrescrita)🖊;

                const Header = () => {
                    return (
                        <>

                        </>
                    )
                }
                export default Header

    - Configure o conteúdo que vai ter dentro componente retorne:
        - tag *`header`* para definir o cabeçalho e *`<h1>`* para título
            
                const Header = () => {
                    return (
                        <header>

                            <h1> Título <h1/>

                        </header>
                    )
                }
                export default Header

3. Configure a importação e formatação que o componente vai ter:
    - Crie o atributo e objeto que vão indicar onde a formatação ira agir sobre o conteúdo do componente;
        - Passe dentro do que engloba todo o conteúdo do componente o atributo: *`className`* 🔎(usado para aplicar classes CSS aos elementos JSX)🖊

        - Em seguida o objeto: *`styles.nomeReferência`* 🔎(objeto de estilos gerado pelos CSS Modules)🖊

                const Header = () => {
                    return (
                        <header className={styles.Header}>

                            <h1>Título</h1>

                        </header>
                    )
                }
                export default Header
    
    - Crie a conexão com o arquivo: *`Header.module.css`* para fazer a importação da formatação;
        - Importando a formatação;
        
                import styles from './Header.module.css'
                
                const Header = () => {
                    return (
                        <header className={styles.Header}>

                            <h1>Título</h1>

                        </header>
                    )
                }
                export default Header

    - Crie a classe e as instruções da formatação :
        - Utilize o *`ponto (.)`* parar criar a classe *`Header`* 🔎(o nome deve ser igual ao usado no objeto *`styles.`* do componente)🖊 que vai receber a formatação do componente

                .Header{

                }

        - Defina a formatação

                .Header{
                    background-color: #ff00ff;
                    color: #ffffff;
                    padding: 20px;
                    text-align: center;
                }

### ▷ Usando o componente