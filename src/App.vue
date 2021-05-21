<template>
	<div id="wrap">
		<shHeader></shHeader>
		<shContent v-bind:propsdata="sns"></shContent>
		<shFooter v-bind:propsdata="sns"></shFooter>
	</div>
</template>

<script>
import shHeader from './components/shHeader.vue'
import shContent from './components/shContent.vue'
import shFooter from './components/shFooter.vue'


export default {
	data (){
		return {
			sns:[
				{el:'blog', name:'네이버블로그', path:'https://post.naver.com/shinsegae-inc'},
				{el:'youtube', name:'유튜브', path:'https://www.youtube.com/channel/UCDT2efYTZ8y516QjrfsDQSA?view_as=subscriber'},
				{el:'facebook', name:'페이스북', path:'https://www.facebook.com/shinsegaeinc'}
			]
		}
	},
	components: { 
		shHeader, 
		shContent,
		shFooter
	},

}
</script>

<style>

</style>