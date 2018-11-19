<template>
	
		<ul class="c-course">
			
				<li v-for="item in arrList">
					<router-link to="/detail" class="link">
						<img :src="item.imgUrl">
						<h1>{{item.title}}</h1>
						<p>{{item.msg}}</p>
					</router-link>

				</li>
		</ul>
	
</template>


<style scoped>
	.c-course .link{
		display: block;
		width: 100%;
		height: 100%;
	}
	.c-course {
		display: flex;
		flex-direction: column;
		padding: 24px 0 30px;
	}

	.c-course li{
		position: relative;
		width: 335px;
		height: 72px;
		margin: 0 auto 24px;
	}
	.c-course img{
		position: absolute;
		width:108px;
		height: 72px;
		border-radius: 5px;
	}

	.c-course h1{
		font-size: 15px;
		color: #2B333B;
		padding-left: 124px;
	}

	.c-course p{
		font-size: 12px;
		color: #71777D;
		padding-left: 124px;
		padding-top: 8px;
	}

</style>

<script>
	export default {
		props:{
			arrList:Array
		}
	}
</script>