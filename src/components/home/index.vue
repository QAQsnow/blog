<template>
	<div class="con-home clearfix">
		<div class="left-home f-l">
			<div class="info-home">
				<h2>个人资料</h2>
				<div class="photo-home">
					<img src="../../assets/images/header.jpg" width="182" height="182">
				</div>
				<div class="delinfo-home">
					<div class="name-home">
						<strong>{{blogInfo.name}}</strong>
						<a href="http://blog.sina.com.cn/v/verify" class="link-auth">
							<i class="icon icon-auth"></i>
						</a>
					</div>
					<div class="sina-home">
						<a href="http://weibo.com/2649044947/profile?topnav=1&wvr=6&is_all=1" class="btn-ownersina">
							<i class="icon icon-sina"></i>
							{{blogInfo.microblog}}
						</a>
					</div>
					<div class="btnbox-home">
						<a href="btn-addfriend">加好友</a>
						<a href="btn-sendnote">发纸条</a>
						<a href="btn-message">写留言</a>
						<a href="btn-concern">加关注</a>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script type="text/javascript">
import axios from 'axios'
	export default({
		data(){
			return {
				blogInfo:{}
			}
		},
		created(){
			axios.get('/static/data.json').then(res=>{
				this.blogInfo=res.data.bloggerInfo;
			},err=>{
				console.log(err);
			})
		}
	});
</script>

<style type="text/css" lang="stylus" scope>
	.con-home
		margin-top 15px
		.left-home
			width 210px
			border 1px solid #dcdcdc
			background-color #fff
			.info-home
				padding 10px 0 0 0
				h2
					font-size 14px
					padding-left 14px
				.photo-home
					margin 10px 0 0 14px
				.delinfo-home
					margin-top 10px
					.name-home
						font-size 14px
						text-align center
						color #666
						a
							margin-left 3px
							i.icon-auth
								display inline-block
								width 15px
								height 15px
								background-position -49px -6px
								position relative
								top 3px
					.sina-home
						margin-top 10px
						text-align center
						.btn-ownersina
							display inline-block
							height 24px
							line-height 24px
							border-radius 3px
							border 1px solid #e0c235
							padding 0 8px
							background-color #f9f4f4
							i.icon-sina
								display inline-block
								width 15px
								height 15px
								background-position -6px -6px
								vertical-align middle
								margin-right 5px
					.btnbox-home
						padding 0 41px
						margin 10px auto 0
						padding-top 10px
						border-top 1px dashed #dcdcdc
						a
							float left
							padding 5px 10px
							background-color #f9f4f4
							border 1px solid #e0c235
							margin 0 3px 5px
							border-radius 3px



</style>

