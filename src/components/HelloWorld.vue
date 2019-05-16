<template>
	<div class="hello">
		<div class="swiper-container">
			<div class="swiper-wrapper">
				<div class="swiper-slide"><img src="../../static/QQ图片.gif" alt="" /></div>
				<div class="swiper-slide"><img src="../../static/QQ图片.gif" alt="" /></div>
				<div class="swiper-slide"><img src="../../static/QQ图片.gif" alt="" /></div>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'HelloWorld',
		data() {
			return {
				msg: 'Welcome to Your Vue.js App'
			}
		},
		mounted() {

			this.moveSwiper()
			this.testJson()
		},
		methods: {
			moveSwiper() {
				var mySwiper = new Swiper('.swiper-container', {
					autoplay: {
						delay: 1000, //1秒切换一次
					},
				})
			},
			testJson(){
				axios.get('../../static/1.json').then(res=>{
					console.log(res.data)
				})
			}
		},
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	h1,
	h2 {
		font-weight: normal;
	}
	
	ul {
		list-style-type: none;
		padding: 0;
	}
	
	li {
		display: inline-block;
		margin: 0 10px;
	}
	
	a {
		color: #42b983;
	}
</style>