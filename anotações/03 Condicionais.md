
# Condicionais

Diferente do React no vue, nós não precisamos abrir chaves para escrevermos um trecho de código js caso for necessário uma condicional para renderizar ou não um elemento na tela, o vue possui diretivas que servem justamente para isso, as diretivas `v-if` e `v-show` são usadas nas tags html como um atributo, sendo a diretiva `v-if` a diretiva que vai evitar que o componente seja renderizado caso o argumento, seja false e a diretiva v-show apenas adiciona a classe display none 

### v-if 
A diretiva `v-if` assim como o `if` do javascript possui o seu `v-else-if` e `else`, sendo as alternativas de execução caso o argumento seja falso, mas você pode utilizar operadores para validar valores false também.

```vue
// Component.vue
<template>
	<TheLoginModal v-if="!logged" class="buttonLogin">Entrar</BaseButton>
	<TheUserBox />
</template>

<script setup>
	const logged = ref(false)
</script>

<style>
	/* Estilo do componente */
</style>
```

	Nesse caso o componente TheLoginModal só sera renderizado se a variável logged tiver seu valor como falso, caso o v-show estivesse sendo utilizado, o componente seria renderizado, mas seria escondido por classe css.


