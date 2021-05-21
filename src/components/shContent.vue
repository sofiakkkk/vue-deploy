<template>
	<div id="content">
		<conMainText v-bind:propsdata="propsdata"></conMainText>
		<conMenuList></conMenuList>
	</div>
</template>

<script>
import conMainText from './conMainText'
import conMenuList from './conMenuList'
export default {
	
	props: ['propsdata'],
	components: {
		conMainText,
		conMenuList
	}

}
</script>

<style>

</style>