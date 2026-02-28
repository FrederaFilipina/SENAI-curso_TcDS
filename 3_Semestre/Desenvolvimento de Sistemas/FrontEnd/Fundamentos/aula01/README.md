# Aula 01

## Componentização: 🔎 É uma estratégia arquitetural que divide sistemas e interfaces em unidades menores, independentes e reutilizáveis chamada de: *`componentes`* 🖊

### 1. Apagando as informações e ajustando a formatação inicial:
1. Abra o arquivo: *`App.jsx`* 
    - Selecione tudo que está dentro e delete;
    
    - Crie uma função com o nome do arquivo, que retorne um fragmento vazio a ser exportado;

2. Abra o arquivo: *`index.css`* 
    - Selecione tudo que está dentro e delete;

    - Deixe a formatação padronizada para receber as formatações dos componentes, inserindo essas instruções:

            *{
                margin: 0;
                padding: 0;
                box-sizing: border-box;
            }

### 2. Criando a estrutura de *`Componentização`*:
1. Crie a subpasta: *`layouts`* 🔎(pasta que vai agrupar as subpastas que compões os componentes a serem utilizados na página)🖊 dentro da pasta: *`src`*;

2. Crie a subpasta: *`Header`* dentro da pasta: *`layouts`*, para armazenar os arquivos que compõem o componente do cabeçalho;

3. Crie dentro da pasta *`Header`* esses dois arquivos:
    - *`index.jsx`* 🔎(arquivo que vai ter toda as informações deste componente)🖊;
    - *`Header.module.css`* 🔎(arquivo que vai ter toda formatação do componente)🖊;

            📁src
                📂layouts
                    📁Header
                        ↪ Header.module.css
                        ↪ index.jsx

### 3. Criando o *`componente`*:
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