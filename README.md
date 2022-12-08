# Make your Burger

Este é um site para uma hamburgueria, projetado e desenvolvido durante o [Curso de Vue 3](https://www.youtube.com/playlist?list=PLnDvRpP8BnezDglaAvtWgQXzsOmXUuRHL).

## Table of contents

- [Project setup](#project-setup)
- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Initialize api
```
npm run backend
```

## Overview

### Screenshot

![Screenshot_1](https://user-images.githubusercontent.com/105292489/206544118-883a63fc-7793-495a-ab22-d9a0e7f03928.jpg)
![Screenshot_2](https://user-images.githubusercontent.com/105292489/206544915-16e89387-31e7-4b5f-9891-776a5fde519e.jpg)
![Screenshot_3](https://user-images.githubusercontent.com/105292489/206544932-788a49a1-cf33-4b21-b7bf-d5d67a6e452a.jpg)

### Links

- Solution URL: [Here](https://github.com/muryllohenriq/make-your-burger)
- Live Site URL: [Here](https://make-your-burger-xi.vercel.app)

## My process

### Built with

- Vue.js
- Semantic HTML5 markup
- CSS custom properties
- JavaScript

### What I learned

```html
<!-- Esse foi o meu primeiro projeto utilizando o vue. -->
<template>
  <Banner />
  <div class="main-container">
    <h1>Monte o seu burger:</h1>
    <BurgerForm/>
  </div>
</template>
<!-- A forma como o vue cria uma página, a interface pro usuário, utilizando compomnentes, é muito prático e organizado -->
```
```css
.proud-of-this-css {
  .submit-btn {
  background-color: #222;
  color: #fcba03;
  font-weight: bold;
  border: 2px solid #222;
  padding: 10px;
  font-size: 16px;
  cursor: pointer;
  transition: 0.3s;
}

.submit-btn:hover {
  background-color: transparent;
  color: #222;
}
}
```
```js
const res = await req.json();

this.msg = `O pedido Nº ${res.id} foi atualizado para ${res.status}`;

setTimeout(() => this.msg = "", 3000);

// alterando o estado do pedido e fazendo um update na api
```
### Continued development

- Deixar o projeto responsivo
- Criar a página pro admin

### Useful resources

- [Resource 1](https://www.youtube.com/playlist?list=PLnDvRpP8BnezDglaAvtWgQXzsOmXUuRHL) - Curso de Vue 3.
- [Resource 2](https://vuejs.org) - Documentação do Vue.

## Author

- Website - [muryllohenriq](https://github.com/muryllohenriq)
- LinkedIn - [Muryllo Henrique](https://www.linkedin.com/in/muryllohenrique/)

## Acknowledgments

Gostei bastante de trabalhar com o Vue, ele tem suas diferenças do React, algumas melhores, outras piores, mas basicamente a lógica é a mesma, pretendo estudar mais ele.
