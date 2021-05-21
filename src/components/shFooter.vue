<template>
	<footer>
		<div>
			<div>
				<div>
					<h5>SHINSEGAE I&amp;C</h5>
					<ul>
						<li><a href="#">개인정보처리방침</a></li>
						<li><a href="#">협력회사 지원센터</a></li>
					</ul>
				</div>
				<div class="info">
					<address>서울특별시 중구 남대문시장10길 2, 메사빌딩 21층</address>
					<dl>
						<dt>대표이사</dt>
						<dd>손정현</dd>
					</dl>
					<dl>
						<dt>TEL</dt>
						<dd>02-3397-1234</dd>
					</dl>
				</div>
				<p>Copyright ⓒ 2020 SHINSEGAE I&C Inc. All Rights Reserved.</p>
			</div>
			<div>
				<fieldset class="on">
					<label for="selectbox">Family Site</label>
					<select id="selectbox" title="패밀리사이트목록">
						<option disabled="disabled">신세계아이앤씨</option>
						<option>SELLPACK1</option>
						<option>SELLPACK2</option>
						<option>SELLPACK3</option>
						<option disabled="disabled">신세계그룹</option>
						<option>SELLPACK4</option>
						<option>SELLPACK5</option>
						<option>SELLPACK6</option>
						<option>SELLPACK4</option>
						<option>SELLPACK5</option>
						<option>SELLPACK4</option>
						<option>SELLPACK5</option>
						<option>SELLPACK4</option>
						<option>SELLPACK5</option>
					</select>
				</fieldset>
				<ul>
					<li v-for="(sns, i) in propsdata" v-bind:key="i" v-bind:class="i.el">
						<a v-bind:href="i.path" target="_blank">{{ i.name }}</a>
					</li>
				</ul>
			</div>
		</div>
		<a href="#content">맨 위로 올리기버튼</a>
	</footer>
</template>

<script>
export default {
	props: ['propsdata'],
}
</script>

<style>

</style>