<template>
	<section class="menuList">
		<article class="business">
			<div>
				<h3 data-aos="fade-right" data-aos-offset="300" data-aos-easing="ease-in-sine">Business</h3>
				<ul>
					<li v-for="(businessList, index) in businessLists" v-bind:key="index" data-aos="fade-up"><a href="#"><span>0{{ index + 1 }}</span>{{ businessList }}<strong>{{ arrow }}</strong></a></li>
				</ul>
			</div>
		</article>
		<article class="news">
			<h3 data-aos="fade-right" data-aos-offset="300" data-aos-easing="ease-in-sine">News</h3>
			<ul>
				<li v-for="(newsList, idx) in newsLists" v-bind:key="idx" data-aos="fade-up">
					<a v-bind:href="newsList.path">
						<img v-bind:src="newsList.src" v-bind:alt="newsList.alt" />
						<span>{{ newsList.content }}</span>
						<strong>{{ arrow }}</strong>
					</a>
				</li>
			</ul>
			<a data-aos="fade-up" href="#">뉴스 더보기</a>
		</article>
		<article class="contact">
			<h3 data-aos="fade-right">Contact Us</h3>
			<p data-aos="fade-up">리테일테크부터 IT서비스, 솔루션 총판, IT기기 유통까지 신세계아이앤씨의 최고 전문가들이 신속하게 해결해드리겠습니다.</p>
			<a data-aos="fade-up" href="#">문의하기</a>
		</article>
	</section>
</template>

<script>
export default {
	data (){
		return {
			businessLists: ['SPHAROS','클라우드','AI','디지털 공간 비즈니스','IT서비스','교육서비스','솔루션 총판','IT기기 유통','오픈 이노베이션'],
			arrow:'화살표',
			newsLists: [
				{src:"resources/img/20210225_092354389_009.jpg", alt:"SPHAROS", content:"리테일테크 통합 브랜드'스파로스(spharos)'출시", path:"#"},
				{src:"resources/img/20201216_162601816_006.jpg", alt:"SPHAROS", content:"클라우드 멤버십 서비스 출시", path:"#"},
				{src:"resources/img/20201127_083640775_011.jpg", alt:"SPHAROS", content:"SAP 손잡고 '클라우드POS'글로벌 시장으로 확대한다", path:"#"},
				{src:"resources/img/20201127_083524710_010.jpg", alt:"SPHAROS", content:"앱(APP)없어도 OK! 아마존고 단점 보완한 '셀프매장2.0'", path:"#"}
			]
		}
	}
}
</script>

<style>

</style>