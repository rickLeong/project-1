<template>
	<div class="home-page">
		<v-header></v-header>

		<ul class="nav">
			<li v-for="item in arrList">
				<img :src="item.imgUrl">
				<span>{{item.name}}</span>
			</li>
		</ul>

		<v-course :arrList="array"></v-course>

		<v-footer></v-footer>
	</div>

	
	
</template>

<style scoped>
	::-webkit-scrollbar {
	    width: 0;   /* 滚动条宽度为0 */
	    height: 0; /* 滚动条高度为0 */
	    display: none; /* 滚动条隐藏 */
	}
	.nav{
		margin-top: 44px;
		background-color: #F3F5F7;
		width: 375px;
		display: flex;
		overflow-x: scroll;
		height: 100px;
	}

	.nav li{
		font-size: 14px;
		color: #2B333B;
		padding-top: 20px;
		padding-left: 56px;
		align-items: center;
	}
	
	.nav li:first-child{
		padding-left: 32px;
	}
	.nav li:last-child{
		padding-right: 32px;
	}
	
	.nav img{
		display: block;
		width: 32px;
		margin:0 auto;
	}

	.nav span{
		display: block;
		width:56px;
		text-align: center;
		padding-top: 12px;
	}
</style>

<script>
	import Header from "@/components/header/index.vue"
	import course from "@/components/course/index.vue"
	import footer from "@/components/footer/index.vue"
	import webImg from "@/assets/web.png"
	import webservice from "@/assets/webservice.png"
	import move from "@/assets/move.png"
	import data from "@/assets/data.png"
	import bigdata from "@/assets/bigdata.png"
	import course1 from "@/assets/course1.jpg"
	import course2 from "@/assets/course2.jpg"
	import course3 from "@/assets/course3.jpg"
	import course4 from "@/assets/course4.jpg"
	import course5 from "@/assets/course5.jpg"
	export default{
		data(){
			return{
				arrList:[],
				array:[]
			}
		},
		mounted(){
			this.arrList = [{
				imgUrl:webImg,
				name:'前端开发'
			},{
				imgUrl:webservice,
				name:'后端开发'
			},{
				imgUrl:move,
				name:'移动开发'
			},{
				imgUrl:data,
				name:'数据库'
			},{
				imgUrl:bigdata,
				name:'云计算'
			}],
			this.array = [{
				imgUrl:course1,
				title:'星级评分原理与实战',
				msg:'中级 · 330在学'
			},{
				imgUrl:course2,
				title:'实例妙解Sed和Awk的秘密',
				msg:'中级 · 330在学'
			},{
				imgUrl:course3,
				title:'实例妙解Sed和Awk的秘密',
				msg:'中级 · 330在学'
			},{
				imgUrl:course4,
				title:'PHP消息队列实践',
				msg:'中级 · 330在学'
			},{
				imgUrl:course5,
				title:'Java定时任务调度工具详解之Quartz篇',
				msg:'中级 · 330在学'
			},{
				imgUrl:course1,
				title:'星级评分原理与实战',
				msg:'中级 · 330在学'
			},{
				imgUrl:course2,
				title:'实例妙解Sed和Awk的秘密',
				msg:'中级 · 330在学'
			},{
				imgUrl:course3,
				title:'实例妙解Sed和Awk的秘密',
				msg:'中级 · 330在学'
			}]
		},
		components:{
			'v-header':Header,
			'v-course':course,
			'v-footer':footer
		}
	}
	
</script>


