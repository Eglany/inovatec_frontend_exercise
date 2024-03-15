# Exercício de Formulário

Crie um formulário em HTML, CSS e JavaScript que salva as informações inseridas nos campos no `localStorage` do navegador.

## Antes de desenvolver

1. Clone o repositório
  * `git clone git@github.com:Eglany/inovatec_frontend_exercice.git`
  * Entre na pasta do repositório que você acabou de clonar:
    * `cd inovatec_frontend_exercice`

2. Crie uma branch a partir da branch `main`
  * Verifique que você está na branch `main`
    * Exemplo: `git branch`
  * Se não estiver, mude para a branch `main`
    * Exemplo: `git checkout main`
  * Agora, crie uma branch onde você vai guardar os `commits` do seu projeto
    * Você deve criar uma branch no seguinte formato: `nome-de-usuario-nome-do-projeto`
    * Exemplo: `git checkout -b eglany-junior-exercice-1`

3. Adicione as mudanças ao _stage_ do Git e faça um `commit`
  * Verifique que as mudanças ainda não estão no _stage_
    * Exemplo: `git status` (devem aparecer listados os novos arquivos em vermelho)
  * Adicione o novo arquivo ao _stage_ do Git
      * Exemplo:
        * `git add .` (adicionando todas as mudanças - _que estavam em vermelho_ - ao stage do Git)
        * `git status` (devem aparecer listados os arquivos em verde)
  * Faça o `commit` inicial
      * Exemplo:
        * `git commit -m 'iniciando o projeto'` (fazendo o primeiro commit)
        * `git status` (deve aparecer uma mensagem tipo _nothing to commit_ )

4. Adicione a sua branch com o novo `commit` ao repositório remoto
  * Usando o exemplo anterior: `git push -u eglany-junior-exercice-1`

## Estrutura do Projeto

```
formulario/
...
├── src
    ├── index.html
    ├── style.css
    └── script.js
...
```

## Descrição dos Arquivos

- `index.html`: Contém a estrutura HTML do formulário.
- `style.css`: Estiliza o formulário.
- `script.js`: Adiciona funcionalidades ao formulário, incluindo a manipulação do `localStorage`.

## Funcionamento

Ao preencher os campos de nome, email, estado e cidade e clicar no botão "Enviar", as informações serão salvos no `localStorage`. Você pode verificar se os dados foram salvos abrindo o console do navegador e digitando `localStorage` para ver o conteúdo armazenado.

![Exemplo:](/public/image.png)

## Requisitos

### 1 - Crie um campo de nome
 - O campo deve ter uma label
 - O campo deve ter um input com os seguinte atributos:
    - `type="text"`
    - `placeholder` com o exemplo de nome a ser preenchido
    - `id="name"`

### 2 - Crie um campo de e-mail
 - O campo deve ter uma label
 - O campo deve ter um input com os seguinte atributos:
    - `type="text"`
    - `placeholder` com o exemplo de e-mail a ser preenchido
    - `id="email"`

### 3 - Crie um campo de estado
 - O campo deve ter uma label
 - O campo deve ter um select
    - O select deve mostrar todos os estados do Brasil
    - O primeiro option do select de estado deve estar escrito "Escolha um estado"
    - `id="state"`

#### ⚠️ Os estados do select devem ser gerados com JS juntos com os seus respectivos.

### 4 - Crie um campo de cidade
 - O campo deve ter uma label
 - O campo deve ter um input com os seguinte atributos:
    - `type="text"`
    - `id="city"`

### 5 - Crie um botão de enviar
 - O campo deve ter um botão com os seguinte atributos:
    - `type="submit"`
    - `id="submit"`
 - Após clicar no botão, as informações nos campos criados devem ser salvos no `localStorage` da seguinte forma:
    ```js
    {
        name: "Eglany Junior",
        email: "eglany@mail.com",
        locale: {
            state: "Amazonas-AM",
            city: "Manaus",
        }
    }
    ```

### 6 - Bônus: Crie validações para os campos
 
 - Todos os campos devem seguir as seguintes regras.
    - O campo nome é obrigatório e deve ter no mínimo 3 caracteres
    - O campo email é obrigatório e deve ser de fato um email e possuir no mínimo 6 caracteres
    - O campo estado é obrigatório e deve ser selecionado 1 estado 
    - O campo cidade é obrigatório e deve ter no mínimo 3 caracteres
 - Ao clicar no botão de "Enviar" e caso um desses campos não siga as regras acima, deve ser mostrado ao usuário qual e/ou quais campos estão errados e o que está errado nesses campos.