<template>
	<section class="mainText">
		<article class="global">
			<p>
				<span v-for="(global, i) in globals" v-bind:key="i">{{ global }}</span>
				<br />
				<span v-for="(retail, i) in retails" v-bind:key="`A-${i}`">{{ retail }}</span>
				&nbsp;
				<span v-for="(tech, i) in techs" v-bind:key="`B-${i}`">{{ tech }}</span>
				<br />
				<span v-for="(leader, i) in leaders" v-bind:key="`C-${i}`">{{ leader }}</span>
				<strong class="plus" >플러스</strong>
			</p>
			<!-- sns -->
			<ul>
				<li v-for="(sns, idx) in propsdata" v-bind:key="idx" v-bind:class="sns.el">
					<a v-bind:href="sns.path" target="_blank">{{ sns.name }}</a>
				</li>
			</ul>
			<div class="bar">line</div>
		</article>
		<article class="intro">
			<h3 data-aos="fade-up">About<br />SHINSEGAE I&amp;C</h3>
			<p v-for="(introText, idx) in introTexts" v-bind:key="idx" v-bind:class="introText.el" v-html="introText.text" data-aos="fade-up"></p>
		</article>
	</section>
</template>

<script>
export default {
	props: ['propsdata'],
	data (){
		return {
			globals: ['G','L','O','B','A','L'],
			retails: ['R','E','T','A','I','L'],
			techs: ['T','E','C','H'],
			leaders: ['L','E','A','D','E','R'],
			introTexts: [
				{el: 'introText01', text: '신세계아이앤씨는 디지털 기술로 새로운 영역에서 새로운 가치를 만들어내는 <span>글로벌 리테일테크 전문 기업</span>입니다.'},
				{el: 'introText02', text: '우리는 최고의 기술력을 기반으로 클라우드, 인공지능, 스마트리테일, 데이터 비즈니스 등 변화와 혁신의 리테일 환경을 구축합니다.'},
				{el: 'introText03', text: '디지털 기술로 차별화된 경험과 가치를 선사하는 리테일테크 No.1 기업으로 4차 산업혁명 시대 리테일 산업의 혁신을 이끌며 미래 경쟁력을 높이고, 나아가 인간의 삶을 바꾸고 새로운 일상을 선물할 것입니다.'}
			]
		}
	},

}
</script>

<style>

</style>