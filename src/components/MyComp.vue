<template>
	<vsa-list>
		<vsa-item @click="isActive=!isActive">
			<vsa-heading>{{ nav.company }}</vsa-heading>
			<vsa-content>
				<vsa-list class="acco-board02">
					<vsa-item>
						<vsa-heading><a class="plus" v-bind:href="subMenu.companyIntro.path" @click="isActive=!isActive">{{ subMenu.companyIntro.name }}</a></vsa-heading>
						<vsa-content>
							<ul>
								<li v-for="(intro, idx) in intros" v-bind:key="idx">
									<a v-bind:href="intro.path">{{ intro.name }}</a>
								</li>
							</ul>
						</vsa-content>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a class="plus" v-bind:href="subMenu.investInfo.path">{{ subMenu.investInfo.name }}</a></vsa-heading>
						<vsa-content>
							<ul>
								<li v-for="(invest, idx) in invests" v-bind:key="idx">
									<a v-bind:href="invest.path">{{ invest.name }}</a>
								</li>
							</ul>
						</vsa-content>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a class="plus" v-bind:href="subMenu.incruteApply.path">{{ subMenu.incruteApply.name }}</a></vsa-heading>
						<vsa-content>
							<ul>
								<li v-for="(incrute, idx) in incrutes" v-bind:key="idx">
									<a v-bind:href="incrute.path">{{ incrute.name }}</a>
								</li>
							</ul>
						</vsa-content>
					</vsa-item>
				</vsa-list>
			</vsa-content>
		</vsa-item>
		<vsa-item>
			<vsa-heading>{{ nav.business }}</vsa-heading>
			<vsa-content>
				<vsa-list class="acco-board02">
					<vsa-item>
						<vsa-heading><a href="#">SPHAROS</a></vsa-heading>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a class="plus" href="#">클라우드</a></vsa-heading>
						<vsa-content>
							<ul>
								<li><a href="#">클라우드POS</a></li>
								<li><a href="#">클라우드 멤버쉽</a></li>
								<li><a href="#">MSP</a></li>
								<li><a href="#">프라이빗 클라우드</a></li>
								<li><a href="#">데이터센터</a></li>
							</ul>
						</vsa-content>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a class="plus" href="#">AI</a></vsa-heading>
						<vsa-content>
							<ul>
								<li><a href="#">AI</a></li>
								<li><a href="#">RPA</a></li>
							</ul>
						</vsa-content>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a class="plus" href="#">디지털 공간 비즈니스</a></vsa-heading>
						<vsa-content>
							<ul>
								<li><a href="#">스마트리테일</a></li>
								<li><a href="#">스마트인프라</a></li>
								<li><a href="#">AR/VR</a></li>
							</ul>
						</vsa-content>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a class="plus" href="#">IT 서비스</a></vsa-heading>
						<vsa-content>
							<ul>
								<li><a href="#">시스템 운영</a></li>
								<li><a href="#">시스템 개발/통합</a></li>
								<li><a href="#">커머스 플랫폼</a></li>
								<li><a href="#">스마트워크</a></li>
								<li><a href="#">정보보안</a></li>
							</ul>
						</vsa-content>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a class="plus" href="#">교육서비스</a></vsa-heading>
						<vsa-content>
							<ul>
								<li><a href="#">SSG EDU</a></li>
							</ul>
						</vsa-content>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a class="plus" href="#">솔루션 총판</a></vsa-heading>
						<vsa-content>
							<ul>
								<li><a href="#">네트어크/서버</a></li>
								<li><a href="#">리테일 솔루션</a></li>
							</ul>
						</vsa-content>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a class="plus" href="#">IT기기 유통</a></vsa-heading>
						<vsa-content>
							<ul>
								<li><a href="#">게임</a></li>
								<li><a href="#">디바이스 유통</a></li>
							</ul>
						</vsa-content>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a class="plus" href="#">오픈 이노베이션</a></vsa-heading>
						<vsa-content>
							<ul>
								<li><a href="#">벤처투자</a></li>
							</ul>
						</vsa-content>
					</vsa-item>
				</vsa-list>
			</vsa-content>
		</vsa-item>
		<vsa-item>
			<vsa-heading>{{ nav.news }}</vsa-heading>
			<vsa-content>
				<vsa-list class="acco-board02">
					<vsa-item>
						<vsa-heading><a href="#">보도자료</a></vsa-heading>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a href="#">영상</a></vsa-heading>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a href="#">브로슈어</a></vsa-heading>
					</vsa-item>
				</vsa-list>
			</vsa-content>
		</vsa-item>
		<vsa-item>
			<vsa-heading>{{ nav.csr }}</vsa-heading>
			<vsa-content>
				<vsa-list class="acco-board02">
					<vsa-item>
						<vsa-heading><a href="#">CSR경영</a></vsa-heading>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a href="#">사회공헌</a></vsa-heading>
					</vsa-item>
					<vsa-item>
						<vsa-heading><a href="#">CSR핫라인</a></vsa-heading>
					</vsa-item>
				</vsa-list>
			</vsa-content>
		</vsa-item>
	</vsa-list>
</template>

<script>
import {
  VsaList,
  VsaItem,
  VsaHeading,
  VsaContent,
} from 'vue-simple-accordion';
export default {
	props: ['intros', 'subMenu', 'invests', 'incrutes', 'nav'],
	data (){
		return {
			isActive:false,
		}
	},
	components: {
		VsaList,
		VsaItem,
		VsaHeading,
		VsaContent,
	}
}
</script>

<style>

</style>