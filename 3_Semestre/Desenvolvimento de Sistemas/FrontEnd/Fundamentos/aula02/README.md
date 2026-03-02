# Aula 02
> Continuando a revisão sobre fundamentos de React

### Componentização: 🔎 É uma estratégia arquitetural que divide sistemas e interfaces em unidades menores, independentes e reutilizáveis chamada de: *`componentes`* 🖊

##

### 1. Expandido a estrutura *`Componentização`*:
1. Crie outras duas subpastas: *`Body`* e *`Footer`* dentro da pasta: *`layouts`*, para armazenar os arquivos que compõem os componentes do corpo de rodapé da página;

2. Crie dentro de cada subpasta os arquivos:
    - *`index.jsx`* 🔎(arquivo que vai ter toda as informações do componente)🖊;

    - *`NomeDaSubpasta.module.css`* 🔎(arquivo que vai ter toda formatação do componente)🖊;

            📂src
                📂layouts
                    ▶📁 Body
                        ↪ Body.module.css
                        ↪ index.jsx
                    📁Body
                        ↪ Body.module.css
                        ↪ index.jsx
                    ▶📁 Footer
                        ↪ Footer.module.css
                        ↪ index.jsx

### 2. Criando e configurando os novos componentes:
1. Criando o esqueleto dos componentes:
    - Componente:

        1. *`Body`*
            - usando uma *`Arrow function`* com *`const`* 🔎(forma segura de assegurar uma função com a garantia de que ela não será sobrescrita)🖊;      

                    const Body = () => {
                        return (
                            <>

                            </>
                        )
                    }
                    export default Body

        2. *`Footer`*
            - usando um *`export function`* 🔎(forma usada quando se quer exportar várias coisas de um único arquivo.)🖊; 

                    export function Footer({}) {
                        return (
                            <footer>

                            </footer>
                        )
                    }