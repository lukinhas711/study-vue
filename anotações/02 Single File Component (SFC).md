
# Single File Component (SFC)

A estrutura dos arquivos vue tem uma arquitetura a ser seguida, esses `SFCs` são um arquivo na aplicação com a extensão `.vue`, onde na hora de fazer o build, esses arquivos serão convertidos em arquivos primários de `HTML`, `CSS` e `JS`

```vue
// Component.vue
<template>
	<div>Seu conteúdo</div>
</template>

<script>
	// Logica do componente
</script>

<style>
	/* Estilo do componente */
</style>
```


## Utilizando componente dentro de arquivos vue

Quando queremos utilizar algum componente que ja tenhamos criado dentro de nossos arquivos.vue nos precisamos importá-los e registrá-los dentro do nosso arquivo. Dentro da nossa tag `Script` nós iremos importar o nosso componente do seu diretório e registraremos ele dentro da chave `components` que vem padrão do vue.

```vue
// Component.vue
<template>
	<Componente>Seu Componente</Componente>
	<Componente />
</template>

<script>
	import Componente from './components/Componente'
	
	name: 'App',
	components: {
		Componente,
	},
</script>

<style>
	/* Estilo do componente */
</style>
```

Os nomes dados aos componentes devem ser sempre multipalavras, exceto pelo componente raiz App.vue. Por conta disso existe também uma concesso para a escolha de nomes dos componentes dentro do vue, onde os componentes que serão utilizados várias veze na nossa aplicação serão nomeados com um prefixo `Base` e os componentes únicos com o prefixo `The`. Mas tudo isso é decidido pelo time ou pelo desenvolvedor da aplicação e não é uma regra universal.

**EX:** 
```html
> Components
	Base
		<BaseButton />
		<BaseIcon />
		<BasePage />
		<BaseContainer />
	The
		<TheMenu />
		<TheFooter />
		<ThePlayer />
		<TheHeader />
```

