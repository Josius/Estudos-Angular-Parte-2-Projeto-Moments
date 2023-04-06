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