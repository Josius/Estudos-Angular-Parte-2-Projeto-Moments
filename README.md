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

## **NOTA IMPORTANTE:** 
Como estamos usando a versão 15.2.1 do Angular, ele por padrão não gera o diretório *environments*, para isso precisamos usar o seguinte comando para gerar este diretório com seus arquivos:
> `ng generate environments`

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

## **Aula 27 - Criando Interfaces e Configurando Módulos**
### **Descrição**
**Importações**
- importaremos em *__app.component.ts__*:
  - HttpClientModule
  - FormsModule
  - ReactiveFormsModule - para validações de formulário
- e declararemos no campo imports

**Inferface**
- no nível do diretório app criaremos a pasta interface, a qual armazenará todas as nossas interfaces
- no caso, criaremos a interface *__Moments.ts__*
  - a qual poderá receber ou não um id (*por exemplo, ao criar um momento, não precisamos de um id*)
  - também terá os outros dados obrigatórios: *title, description, image*
  - e os seguintes dados opcionais: *created_at, updated_at e comments*
- também criaremos as interfaces:
  -  *__Comments.ts__* - para comentários
  -  *__Response.ts__* - para trabalharmos com respostas com mais dados e trabalharemos com as duas entidades, *Comment* e *Moment*:
  
  ```ts
	export interface Response<T> {
		message?: string;
		data: T
	}
  ```
  - *T* é um *generic*, o qual representa algo que pode vir do BD, como um comentário ou um momento

**Services**
- agora criaremos um service com o comando:
> `ng generate service services/nome-do-service`
- no caso, criaremos 3 services, *moment, comment e messages*

## **Aula 28 - Validação de Formulário com Reactive Forms**
### **Descrição**
- alteraremos o componente *moment-form*
    1. em *moment-form.component.html*, definir qual método ativar quando enviar um formulário
   		- usar diretiva *ngSubmit* que disparará o método *.submit()* do *moment-form.component.ts*
    2. em *moment-form.component.ts* criamos o método *.submit()*
    3. em *moment-form.component.html*, declararemos um grupo de formulário para o angular conseguir mapear os inputs e disparar as validações
    	- *[formGroup]* do *FormsModule*, com o nome do formulário
	4. em *moment-form.component.ts* criaremos *formGroup*, o qual será preenchido com o tempo, não esquecendo de importa-lo do *@angular/forms*
	5. em *moment-form.component.html*, declaramos qual é o formulário ou aonde é o formulário 
   		- *#formDir="ngForm"* entenderá que é um formulário e conseguiremos mapear após o *.submit()*
	
**Vamos criar as validações:**
  - em *moment-form.component.html* criamos o atributo *formControlName=""* para dar o nome deste atributo para o formulário, o qual é ligado com o formulário que será criado depois no componente
  - e também criamos a div de validação, a qual é disponibilizada através de um *ngIf*
  - vamos para *moment-form.component.ts* para criar os dados necessários para validação e inicializar o formulário:
  ```ts
  ngOnInit(): void{
    this.momentForm = new FormGroup({
      id: new FormControl(''),
      title: new FormControl(''),
      description: new FormControl(''),
      image: new FormControl('')
    })
  }
  ```

**Vamos declarar os validators**
- em *moment-form.component.ts* importamos os *Validators*, o qual permitirá disparo de validação com base do valor ser ou não vazio:
```ts
  title: new FormControl('', [Validators.required]),
  description: new FormControl('', [Validators.required]),
```

**Inicializando as propriedades**
- quando trabalhamos com formulário reativo no Angular, não inicializamos com propriedades
- nós criamos um método *get*, para pegar o atributo *title* e *description* presentes no objeto *momentForm* recém inicializado no *.ngOnInit()*

**Outras validações**
- podemos fazer outras validações em *moment-form.component.html*, como a verificação do próprio dado requerido:
  ```html
  <p *ngIf="title.errors?.['required']">O título é obrigatório.</p>
  ```

- ou a verificação da quantidade máxima de caracteres digitados:
	```html
  <p *ngIf="title.errors?.['maxLength']">O título é obrigatório.</p>
  ```

- podemos melhorar com uma trava de validação no método *.submit()* do arquivo *moment-form.component.ts*, o que impedirá o envio do formulário sem os dados necessários:
  ```ts
  submit(){
    if (this.momentForm.invalid) {
      return;
    }
    console.log("Enviou formulário");
  }
  ```
- para isso também temos de alterar o *moment-form.component.html*:
```html
<div class="form-group">
  <label for="description">Descrição:</label>
  <textarea placeholder="O que aconteceu lá?" formControlName="description" required></textarea>
</div>
<div *ngIf="description.invalid && formDir.submitted" class="validation-error">
  <p *ngIf="description.errors?.['required']">A descrição é obrigatória.</p>
</div>
```

Por fim, vamos alterar o css global das validações

## **Aula 29 - Inserindo Dados no Sistema**
### **Descrição**
**Trabalhando com a imagem**
- em *__moment-form.component.html__*, no *input* da imagem colocaremos um evento de *change* e um método correspondente a ele em *__moment-form.component.ts__*
- o método no caso é *.onFileSelected()* o qual é responsável por jogar a imagem no formulário

**Emitindo um evento para o componente pai**
- em *__new-moment.component.html__* pegaremos um evento *(onSubmit)="createHandler($event)"*
- em *__new-moment.component.ts__* criamos o método *.createHandler()*
- em *__moment-form.component.ts__* importamos o *@Output()* e adicionamos esse código *this.onSubmit.emit(this.momentForm.value);* no método *.submit()* do mesmo arquivo
- em *__new-moment.component.ts__* trataremos os dados que chegam para poder fazer a inserção no sistema a partir do service depois
- ainda neste arquivo, vamos importar a interface de Moment
- o método *.createHandler()* receberá um *Moment* e terá operações assíncronas, pois estará esperando algo da API
- ele também manipulará o formulário do Angular e o tornará em um *FormData*, um estrutura de formulário padrão do JS

## **Enviar para o service**
- em *moment.service.ts*, importamos o *HttpClient*, *Observable* e a interface *Moment*

**Configurar as URLs**

Benefícios:
- não precisaremos repetir as urls, logo as centralizaremos para não trocar em várias partes do código
- poderemos ter um urls de:
  - produção
  - homologação
  - desenvolvimento
- para executar as configurações acima, vamos criar o diretório *environments* e seus arquivos com o comando:

> `ng generate environments`

-  no arquvio *__environments.ts__* dentro deste diretório vamos colocar mais parâmetros, e mudando o ambiente podemos mudar as configurações neste arquivo.
-  O arquivo ficará da seguinte forma:

```ts
export const environment = {
	production: false,
	baseApiUrl: 'http://localhost:3333/',
};
```

- a variável *baseApiUrl* é referente ao endereço da API, no caso, a criada com [AdonisJS](#setup-adonis).

**Recebendo os Dados da API**
- em *__moment.service.ts__* importamos o *environment*
- criamos um atributo privado que recebe a *baseApiUrl*
- criamos um atributo privado que usa a *baseApiUrl* mais o end-point para moments
- iniciamos o *HttpClient* no *constructor*
- criamos um método *.createMoment()* que retorna a resposta http do método post quando der certo ao enviar os dados de criação de um moment

**Enviar para o service**

Feitas as configurações acima, poderemos criar o método que enviará para o service o momento criado. Em *__new-moment.component.ts__*:
- importamos o *MomentService*
- inicializamos no *constructor* o *momentService*
- e chamamos o método *.createMoment()* do *momentService* passando o *formData*, dando um *.subscribe()* e um *await*

NOTA: Aula 29 foi commitada em aula 28

## **Aula 29 - Inserindo Dados no Sistema**
### **Descrição**