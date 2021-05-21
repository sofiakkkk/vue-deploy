<template>
	<header>
		<div>
			<!-- logo -->
			<h1>
				<a v-bind:href="link.main" target="_blank">
					<img v-bind:src="image.logo" alt="SHINSEGAE I&C" />
				</a>
			</h1>
			<!-- // logo -->
			<!-- nav -->
			<nav>
				<ul>
					<li @mouseenter="down" @mouseleave="up">
						<a href="#">{{ nav.company }}</a>
						<!-- sub menu -->
						<div data-aos="fade-top">
							<div class="subMenu">
								<ul>
									<li>
										<h2><a v-bind:href="subMenu.companyIntro.path">{{ subMenu.companyIntro.name }}</a></h2>
										<ul>
											<li v-for="(intro, idx) in intros" v-bind:key="idx">
												<a v-bind:href="intro.path">{{ intro.name }}</a>
											</li>
										</ul>
									</li>
									<li>
										<h2><a v-bind:href="subMenu.investInfo.path">{{ subMenu.investInfo.name }}</a></h2>
										<ul>
											<li v-for="(invest, idx) in invests" v-bind:key="idx">
												<a v-bind:href="invest.path">{{ invest.name }}</a>
											</li>
										</ul>
									</li>
									<li>
										<h2><a v-bind:href="subMenu.incruteApply.path">{{ subMenu.incruteApply.name }}</a></h2>
										<ul>
											<li v-for="(incrute, idx) in incrutes" v-bind:key="idx">
												<a v-bind:href="incrute.path">{{ incrute.name }}</a>
											</li>
										</ul>
									</li>
								</ul>
							</div>
						</div>
						<!-- // sub menu -->
					</li>
					<li @mouseenter="down" @mouseleave="up">
						<a href="#">{{ nav.business }}</a>
						<!-- sub menu -->
						<div>
							<div class="subMenu">
								<ul>
									<li>
										<h2><a href="#">SPHAROS</a></h2>
									</li>
									<li>
										<h2><a href="#">클라우드</a></h2>
										<ul>
											<li><a href="#">클라우드POS</a></li>
											<li><a href="#">클라우드 멤버쉽</a></li>
											<li><a href="#">MSP</a></li>
											<li><a href="#">프라이빗 클라우드</a></li>
											<li><a href="#">데이터센터</a></li>
										</ul>
									</li>
									<li>
										<h2><a href="#">AI</a></h2>
										<ul>
											<li><a href="#">AI</a></li>
											<li><a href="#">RPA</a></li>
										</ul>
									</li>
									<li>
										<h2><a href="#">디지털 공간 비즈니스</a></h2>
										<ul>
											<li><a href="#">스마트리테일</a></li>
											<li><a href="#">스마트인프라</a></li>
											<li><a href="#">AR/VR</a></li>
										</ul>
									</li>
									<li>
										<h2><a href="#">IT 서비스</a></h2>
										<ul>
											<li><a href="#">시스템 운영</a></li>
											<li><a href="#">시스템 개발/통합</a></li>
											<li><a href="#">커머스 플랫폼</a></li>
											<li><a href="#">스마트워크</a></li>
											<li><a href="#">정보보안</a></li>
										</ul>
									</li>
									<li>
										<h2><a href="#">교육서비스</a></h2>
										<ul>
											<li><a href="#">SSG EDU</a></li>
										</ul>
									</li>
									<li>
										<h2><a href="#">솔루션 총판</a></h2>
										<ul>
											<li><a href="#">네트어크/서버</a></li>
											<li><a href="#">리테일 솔루션</a></li>
										</ul>
									</li>
									<li>
										<h2><a href="#">IT기기 유통</a></h2>
										<ul>
											<li><a href="#">게임</a></li>
											<li><a href="#">디바이스 유통</a></li>
										</ul>
									</li>
									<li>
										<h2><a href="#">오픈 이노베이션</a></h2>
										<ul>
											<li><a href="#">벤처투자</a></li>
										</ul>
									</li>
								</ul>
							</div>				
						</div>		
						<!-- // sub menu -->
					</li>
					<li @mouseenter="down" @mouseleave="up">
						<a href="#">{{ nav.news }}</a>
						<!-- sub menu -->
						<div>
							<div class="subMenu">
								<ul>
									<li>
										<h2><a href="#">보도자료</a></h2>
									</li>
									<li>
										<h2><a href="#">영상</a></h2>
									</li>
									<li>
										<h2><a href="#">브로슈어</a></h2>
									</li>
								</ul>
							</div>
						</div>
						<!-- // sub menu -->
					</li>
					<li @mouseenter="down" @mouseleave="up">
						<a href="#">{{ nav.csr }}</a>
						<!-- sub menu -->
						<div>
							<div class="subMenu">
								<ul>
									<li>
										<h2><a href="#">CSR경영</a></h2>
									</li>
									<li>
										<h2><a href="#">사회공헌</a></h2>
									</li>
									<li>
										<h2><a href="#">CSR핫라인</a></h2>
									</li>
								</ul>
							</div>
						</div>
						<!-- // sub menu -->
					</li>
				</ul>
			</nav>
			<!-- // nav -->
			<!-- language / contact / search bar -->
			<div>
				<!-- language select -->
				<div class="language" v-bind:class="{on: isActive}">
					<a href="#" @click="isActive=!isActive">KR</a>
					<div>
						<a href="#">EN</a>
					</div>
				</div>
				<!-- contact -->
				<a href="#">CONTACT US</a>
				<!-- search bar -->
				<div class="searchBar" v-bind:class="{on: isOn}">
					<a class="openBtn" href="javascript:;" @click="isOn=!isOn">검색</a>
					<a class="closeBtn" href="javascript:;" @click="isOn=!isOn">닫기</a>
					<!-- modal -->
					<div class="searchModal">
						<div>
							<div>
								<fieldset>
									<label class="blind" for="search">검색</label>
									<input v-model="keyWord" type="text" id="search" placeholder="검색어를 입력해주세요">
									<button type="submit">검색버튼</button>
								</fieldset>
								<div>
									<h5>ex</h5>
									<ul>
										<li>스마트리테일</li>
										<li>클라우드</li>
										<li>Deep Learing</li>
									</ul>
								</div>
							</div>
						</div>
					</div>
					<!-- // modal -->
				</div>
			</div>
			<!-- // language / contact / search bar -->
			<!----------------- mobile------------------>
			<div class="mob">
				<!-- search bar -->
				<div class="searchBar02" v-bind:class="{on: isOn}">
					<a class="openBtn" href="javascript:;" @click="isOn=!isOn">검색</a>
					<a class="closeBtn" href="javascript:;" @click="isOn=!isOn">닫기</a>
					<!-- modal -->
					<div class="searchModal">
						<div>
							<fieldset>
								<label class="blind" for="serch">검색</label>
								<input v-model="keyWord" type="text" id="serch" placeholder="검색어를 입력해주세요">
								<button type="submit">검색버튼</button>
							</fieldset>
						</div>
					</div>
					<!-- // modal -->
				</div>
				<!--hamMenu-->
				<div class="ham" v-bind:class="{on: isHam}">
					<a href="javascript:;" @click="isHam=!isHam">메뉴리스트</a>
					<div>
						<div>
							<a class="closeHam" href="#" @click="isHam=!isHam">닫기</a>
							<!--language-->
							<ul>
								<li><a href="#">KR</a></li>
								<li><a href="#">EN</a></li>
							</ul>
							<!--Contact-->
							<a href="#">Contact Us</a>
						</div>
						<!--menuList-->
						<MyComp v-bind:nav="nav" v-bind:intros="intros" v-bind:subMenu="subMenu" v-bind:invests="invests" v-bind:incrutes="incrutes"></MyComp>
					</div>
				</div>
			</div>
			<!----------------- // mobile------------------>
		</div>
	</header>
</template>

<script>
import MyComp from './MyComp.vue'

export default {
	data (){
		return {
			isActive:false,
			isOn:false,
			isHam:false,
			keyWord:'',
			link: {
				main:'https://shinsegae-inc.com/main.do'
			},
			image: {
				logo:'resources/img/logo_sinc.png'
			},
			nav: {
				company:'COMPANY',
				business:'BUSINESS',
				news:'NEWS',
				csr:'CSR',
			},
			subMenu: {
				companyIntro:{name:'회사소개', path:'#'},
				investInfo:{name:'투자정보', path:'#'},
				incruteApply:{name:'인재채용', path:'#'}
					
			},
			intros: [
				{name: '비전/목표', path: '#'},
				{name: '연혁', path: '#'},
				{name: '위치', path: '#'},
			],
			invests: [
				{name: '기업지배구조', path: '#'},
				{name: '주식정보', path: '#'},
				{name: '재무정보', path: '#'},
				{name: 'IR/공고', path: '#'}
			],
			incrutes: [
				{name: '인재경영', path: '#'},
				{name: '채용', path: '#'}
			]
		}
	},
	methods: {
		down(event){
			event.target.classList.add('on')
		},
		up(event){
			event.target.classList.remove('on')
		},
		
	},
	components:{
		MyComp
	}
}
</script>

<style>

</style>