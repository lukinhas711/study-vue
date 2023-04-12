
# Loops

Semelhante as condicionais o vue possui uma diretiva para a execução de loops dentro do template a diretiva `v-for` funciona semelhante a um `for` do javascript, para cada elemento em uma lista sera renderizado um elemento no template, para que o loop funcione de maneira mais performática é necessário passar também uma `key` para que o vue identifique cada elemento dentro do loop (eu normalmente uso o index do elemento).

```vue
// Component.vue
<template>
	<ul>
		<li v-for="(item, index) in lista" :key="index">{{ item.nome }}</li>
	</ul>
</template>

<script>
	const lista = [{ nome: 'item1' },{ nome: 'item2' },{ nome: 'item3' }]
</script>

<style>
	/* Estilo do componente */
</style>
```
