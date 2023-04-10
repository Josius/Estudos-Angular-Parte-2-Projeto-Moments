# **Estudos Angular**

## **Fonte de Estudos - Angular: [Hora de Codar - Angular](https://www.youtube.com/playlist?list=PLnDvRpP8Bnex2GQEN0768_AxZg_RaIGmw)**
## **Fonte de Estudos - AdonisJS: [Hora de Codar - AdonisJS](https://www.youtube.com/watch?v=y8XfJJYhXPE)**
## **Repositório - AdonisJS: [Hora de Codar - Repositório AdonisJS](https://github.com/matheusbattisti/curso_adonis_api_yt)**

## **Ferramentas Utilizadas:**
> - Angular CLI: 15.2.1
> - Node: 18.14.2
> - AdonisJS
> - Package Manager: npm 9.6.0
> - OS: win32 x64
> - [Package Json-Server](https://www.macoratti.net/17/08/ang2_jssv1.htm)

## **O que é AdonisJs**
- framework Node.js, usado para desenvolver aplicações web
- usado como back-end da API

## **Instalação**
Partindo do princípio que as ferramentas acima estão instaladas: 

### **AdonisJS** <a id="setup-adonis"></a>
- baixe o repositório
- entre no diretório /API/curso_adonis_api_yt e abra um terminal/bash
- execute o comando **npm install**
- execute o comando **node ace generate:key**; retornará um valor de chave
- no diretório curso_adonis_api_yt há um arquivo chamado *.env.example*; copie e cole esse arquivo; renomei-o para *.env*; em *APP_KEY=\<valor de chave>*, troque o *\<valor da chave>* pelo valor gerado com o comando **node ace generate:key**
- execute o comando **node ace migration:run** para gerar o BD
- execute o comando **node ace serve**

# VERIFICAR DEPOIS v
### **Angular**
- no diretório raiz do repositório abre um terminal/bash
- execute o comando **npm install**
- execute o comando **ng serve**
- no diretório raiz do repositório abra um novo terminal/bash
- execute o comando **npm run server**
- acesse *http://localhost:4200/* para visualizar as páginas de estudos funcionando
# VERIFICAR DEPOIS ^

# **Notas de Aulas**
## **Aula 22 - Setup da API**
### **Descrição** 
[Aqui](#setup-adonis) está o passo a passo do setup da API porém, também temos a vídeo-aula [aqui](https://www.youtube.com/watch?v=xTCBaGeYTck&list=PLnDvRpP8Bnex2GQEN0768_AxZg_RaIGmw&index=22).

## **Aula 23 - Setup Inicial do Projeto**
### **Descrição**
No diretório raiz criaremos o projeto Angular. A estrutura de diretórios será:

```
/
├───API
│   └───curso_adonis_api_yt
└───Front-End
    └───moments
```

### **Parte Um**
No diretório Front-end:
- execute o comando ng new moments
- responda *y* para a pergunta
- escolha **CSS**

### **Parte Dois**
Segundo o vídeo, no repositório [curso_angular_yt](https://github.com/matheusbattisti/curso_angular_yt/tree/19_projeto_moments), na branch *19_projeto_moments*, temos um conjunto de arquivos de imagens, as quais usaremos. Estão em *curso_angular_yt/moments/mock-moment-images/*.

Copiaremos a pasta *mock-moment-images* para o diretório raiz do projeto *moments*, */Front-End/moments*.

### **Parte Três**
No diretório *src/app/*, no arquivo *__app.component.html__*, apagar toda a pré-configuração gerada.

## **Aula 24 - Estruturando o Projeto**
### **Descrição** 
Gerando novos componentes:
- ng generate component components/header
- ng generate component components/footer
- ng generate component components/pages/about (*componente para páginas*)
- ng generate component components/pages/home (*componente para páginas*)

Em *__app.component.html__* chamamos as tags dos componentes:
```html
<app-header></app-header>
<main class="container">
	<router-outlet></router-outlet>
</main>
<app-footer></app-footer>
```

Em *__header.component.html__*, *__footer.component.html__*, *__about.component.html__* e *__home.component.html__* alteramos inicialmente com seus próprios nomes e uma nav-bar em *header*.

Em *__app-routing.module.ts__* incluiremos as rotas para as páginas Home e About.

Em *__header.component.html__* adicionamos uma nav-bar com *routerLink* para as páginas *home* e *about*.

E estilizaremos o CSS no arquivo global, no caso *__styles.css__*.

## **Aula 25 - CSS nos Componentes de Layout**
### **Descrição**
- Vamos estilizar os componentes estáticos, no caso o cabeçalho (*header*) e o rodapé (*footer*) da página.
- Também vamos preparar o corpo da página.

#### **Passos executados:**
- gerando novo componente: *ng generate component components/pages/new-moment*
- adicionando a rota *{ path: 'moments/new', component: NewMomentComponent },* no arquivo *__app-routing.module.ts__*
- em *__header.component.html__* adicionamos um *routerLink* para a página *new-moment* e alteramos um pouco sua estrutura
- em *__index.html__* endereçamos o local do *favicon.png*
- em *__footer.component.html__* simplesmente configuramos uma tag footer

#### **Passos executados - Scoped:**
Alteramos com o CSS de cada componente, no caso, o *header* e *footer* para a forma ideal de visualização da página.

Um ponto interessante é que estilizamos o arquivo *__app.component.css__* para que o *corpo* da página tenha no mínimo 65% da altura da tela, o que faz com que o *footer* fique na parte inferior da página web.

## **Aula 26 - Página de Formulário**
### **Descrição**
- primeiro, criaremos um novo componente para o formulário
- em seguida, alteramos *__new-moment.component.html__* alocando o componente de formulário criado
- alteraremos agora o arquivo html do componente de formulário, alocando locais para preenchimento do título, descrição, upload da foto e um botão de envio
- *btnText* é uma propriedade do componente de formulário e precisa ser preenchido com texto no componente pai, no caso, *__new-moment.component.html__* e *__new-moment.component.ts__*
- o texto de *btnText* é dinâmica e será conforme o componente usado, no caso de edição será uma outra mensagem
- completados esses passos, vamos estilizar globalmente o formulário
- por fim, vamos melhorar o título principal da página, no caso, em *__new-moment.componet.css__* 