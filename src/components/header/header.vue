<template>
	<div class="header">
		<div class="header-top clearfix">
			<div class="header-logo f-l">
				<img src="../../assets/images/logo.jpg" width="50">
				<span>{{header.selfIntro}}</span>
			</div>
			<div class="header-sign f-r">
				{{header.sign}}
			</div>
		</div>
		<div class="header-nav">
			<ul class="clearfix">
				<li v-for="item in header.navlist"><router-link to="">{{item}}</router-link></li>
			</ul>
		</div>
	</div>
</template>

<script type="text/javascript">
	import axios from 'axios'
	export default({
		data(){
			return {

			}
		},
		props:{
			header:{
				type:Object
			}
		}

	})
</script>


<style lang="stylus" scope>
	.header
		background-color:#fff;
		.header-top
			padding 10px 10px 0
			.header-logo
				overflow hidden
				img
					border-radius 50%
				span
					margin-left 10px
					color #14e9c9	
			.header-sign
				line-height 50px	
		.header-nav
			margin-top 10px
			height 40px			
			ul
				li
					float left
					font-size 18px
					line-height 40px
					padding 0 15px





</style>	
