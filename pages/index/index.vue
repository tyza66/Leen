<template>
	<view class="content">
		<view class="bg-set"></view>
		<view class="top">
			<view class="init1">
				<view class="tag1"><view @click="chanpin()"><p :class="tagg1">产品</p></view></view>
				<view class="tag2"><view @click="fuwuye()"><p :class="tagg2">服务业</p></view></view>
				<view class="tag3"><view @click="zhichi()"><p :class="tagg3">支持</p></view></view>
				<view class="tag4" @click="shequ()"><view><p :class="tagg4">社区</p></view></view>
			</view>
			<image class="jian1" v-show="j1" src="../../static/jian.png"></image>
			<image class="jian2" v-show="j2" src="../../static/jian.png"></image>
			<image class="jian3" v-show="j3" src="../../static/jian.png"></image>
			<image class="jian4" v-show="j4" src="../../static/jian.png"></image>
			<view class="chuang1" v-show="c1">
				<view class="c1" v-for="one in ccc">
					<image :src="one[0]"></image>
					<view class="cv1"><p>{{one[1]}}</p></view>
					<view class="cv2"><p>{{one[2]}}</p></view>
				</view>
			</view>
			<view class="chuang2" v-show="f1">
				<view class="f1" v-for="one in fff">
					<image :src="one[0]"></image>
					<view class="cv1"><p>{{one[1]}}</p></view>
					<view class="cv2"><p>{{one[2]}}</p></view>
				</view>
			</view>
			<view class="chuang3" v-show="z1">
				<view class="f1" v-for="one in zzz">
					<image :src="one[0]"></image>
					<view class="cv1"><p>{{one[1]}}</p></view>
					<view class="cv2"><p>{{one[2]}}</p></view>
				</view>
				<view class="zi1">
					<view class="zi2">
						<p>您的旅程</p>
						<ul>
							<li>开始</li>
							<li>学习基础知识</li>
							<li>获取高级信息</li>
							<li>开始教学</li>
						</ul>
					</view>
					<view class="zi3">
						<p>您的工具</p>
						<ul>
							<li>编辑器</li>
							<li>时间停滞器</li>
							<li>大脑增强剂</li>
							<li>网络制作</li>
						</ul>
					</view>
				</view>
				<view class="zi4">
					<image class="i1" src="../../static/hammer.png"></image><view class="ii1">API导航</view>
					<image class="i2" src="../../static/eye.png"></image><view class="ii2">支持线</view>
					<image class="i3" src="../../static/wenzigongju.png"></image><view class="ii3">在线聊天</view>
					<image class="i4" src="../../static/wenzi.png"></image><view class="ii4">文档</view>
				</view>
			</view>
			<view class="chuang4" v-show="s1">
				<view class="f1" v-for="one in sss">
					<image :src="one[0]"></image>
					<view class="cv1"><p>{{one[1]}}</p></view>
					<view class="cv2"><p>{{one[2]}}</p></view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				tagg1: "ben",
				tagg2: "ben",
				tagg3: "ben",
				tagg4: "ben",
				j1: false,
				j2: false,
				j3: false,
				j4: false,
				c1: false,
				f1: false,
				z1: false,
				s1: false,
				ccc: [["../../static/tishi.png","关于乐恩","如何让儿童实现玩中学，学中玩。"],["../../static/faxian.png","乐恩的特色与创意点","娱教技术与移动学习协和。"],["../../static/gailv.png","乐恩的优势","解决的关键问题"]],
				fff: [["../../static/wenjian.png","提问","来自专业人士"],["../../static/bangzhu.png","教学","线上直播课程"],["../../static/tongzhi.png","学习","通过情景剧"],["../../static/xiaoxi.png","理解","我们的旅程"]],
				zzz: [["../../static/ziliao.png","从哪里开始","从下面开始"]],
				sss: [["../../static/GitHub.png","论坛","从下面开始"],["../../static/tuite.png","推特","从下面开始"],["../../static/jianyi.png","建议","从下面开始"]]
			}
		},
		onLoad() {

		},
		methods: {
			chanpin(){
				if(this.j1==false){
					this.j1 = true;
					this.j2 = false;
					this.j3 = false;
					this.j4 = false;
					this.c1 = true;
					this.f1 = false;
					this.z1 = false;
					this.s1 = false;
					this.tagg1 = "ben2"
					this.tagg2 = "ben"
					this.tagg3 = "ben"
					this.tagg4 = "ben"
				}else{
					this.j1 = false;
					this.j2 = false;
					this.j3 = false;
					this.j4 = false;
					this.c1 = false;
					this.f1 = false;
					this.z1 = false;
					this.s1 = false;
					this.tagg1 = "ben"
					this.tagg2 = "ben"
					this.tagg3 = "ben"
					this.tagg4 = "ben"
				}
			},
			fuwuye(){
				if(this.j2==false){
					this.j1 = false;
					this.j2 = true;
					this.j3 = false;
					this.j4 = false;
					this.c1 = false;
					this.f1 = true;
					this.z1 = false;
					this.s1 = false;
					this.tagg1 = "ben"
					this.tagg2 = "ben2"
					this.tagg3 = "ben"
					this.tagg4 = "ben"
				}else{
					this.j1 = false;
					this.j2 = false;
					this.j3 = false;
					this.j4 = false;
					this.c1 = false;
					this.f1 = false;
					this.c3 = false;
					this.s1 = false;
					this.tagg1 = "ben"
					this.tagg2 = "ben"
					this.tagg3 = "ben"
					this.tagg4 = "ben"
				}
			},
		zhichi(){
			if(this.j3==false){
				this.j1 = false;
				this.j2 = false;
				this.j3 = true;
				this.j4 = false;
				this.c1 = false;
				this.f1 = false;
				this.z1 = true;
				this.s1 = false;
				this.tagg1 = "ben"
				this.tagg2 = "ben"
				this.tagg3 = "ben2"
				this.tagg4 = "ben"
			}else{
				this.j1 = false;
				this.j2 = false;
				this.j3 = false;
				this.j4 = false;
				this.c1 = false;
				this.f1 = false;
				this.z1 = false;
				this.s1 = false;
				this.tagg1 = "ben"
				this.tagg2 = "ben"
				this.tagg3 = "ben"
				this.tagg4 = "ben"
			}
		},
		shequ(){
			if(this.j4==false){
				this.j1 = false;
				this.j2 = false;
				this.j3 = false;
				this.j4 = true;
				this.c1 = false;
				this.f1 = false;
				this.z1 = false;
				this.s1 = true;
				this.tagg1 = "ben"
				this.tagg2 = "ben"
				this.tagg3 = "ben"
				this.tagg4 = "ben2"
			}else{
				this.j1 = false;
				this.j2 = false;
				this.j3 = false;
				this.j4 = false;
				this.c1 = false;
				this.f1 = false;
				this.z1 = false;
				this.s1 = false;
				this.tagg1 = "ben"
				this.tagg2 = "ben"
				this.tagg3 = "ben"
				this.tagg4 = "ben"
			}
		}
		}
	}
</script>

<style>
	.bg-set{
		position: fixed;
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
		background:linear-gradient(45deg, #102eff, #d2379b);
		background-repeat: no-repeat ;
		background-size: 100% 100%;
		background-attachment:fixed;
		z-index: -1;
	}
	.top{
		float: left;
		position: relative;
		width: 100%;
		height: 150rpx;
		margin-top: 40rpx;
	}
	.init1{
		position: absolute;
		width: 700rpx;
		height: 120rpx;
		left: 25rpx;
		top: 20rpx;
	}
	.tag1{
		float: left;
		width: 175rpx;
		height: 120rpx;
	}
	.tag1 view{
		margin: 0 auto;
		margin-top: 30rpx;
		width: 110rpx;
		height: 70rpx;

	}
	.tag1 view .ben{
		text-align: center;
		color: white;
		font-weight: 1000;
		font-size: 35rpx;
	}
	.tag2{
		float: left;
		width: 175rpx;
		height: 120rpx;
	}
	.tag2 view{
		margin: 0 auto;
		margin-top: 30rpx;
		width: 110rpx;
		height: 70rpx;

	}
	.tag2 view .ben{
		text-align: center;
		color: white;
		font-weight: 1000;
		font-size: 35rpx;
	}
	.tag3{
		float: left;
		width: 175rpx;
		height: 120rpx;
	}
	.tag3 view{
		margin: 0 auto;
		margin-top: 30rpx;
		width: 110rpx;
		height: 70rpx;

	}
	.tag3 view .ben{
		text-align: center;
		color: white;
		font-weight: 1000;
		font-size: 35rpx;
	}
	.tag4{
		float: left;
		width: 175rpx;
		height: 120rpx;
	}
	
	.tag4 view{
		margin: 0 auto;
		margin-top: 30rpx;
		width: 110rpx;
		height: 70rpx;

	}
	.tag4 view .ben{
		text-align: center;
		color: white;
		font-weight: 1000;
		font-size: 35rpx;
	}
	.jian1{
		position: absolute;
		width: 50rpx;
		height: 30rpx;
		left: 85rpx;
		top: 110rpx;
	}
	.jian2{
		position: absolute;
		width: 50rpx;
		height: 30rpx;
		left: 265rpx;
		top: 110rpx;
	}
	.jian3{
		position: absolute;
		width: 50rpx;
		height: 30rpx;
		left: 435rpx;
		top: 110rpx;
	}
	.jian4{
		position: absolute;
		width: 50rpx;
		height: 30rpx;
		left: 615rpx;
		top: 110rpx;
	}
	.chuang1{
		position: absolute;
		width: 700rpx;
		height: 500rpx;
		border-radius: 25rpx;
		left: 25rpx;
		top: 140rpx;
		background: white;
	}
	.chuang2{
		position: absolute;
		width: 700rpx;
		height: 650rpx;
		border-radius: 25rpx;
		left: 25rpx;
		top: 140rpx;
		background: white;
	}
	.chuang3{
		position: absolute;
		width: 700rpx;
		height: 650rpx;
		border-radius: 25rpx;
		left: 25rpx;
		top: 140rpx;
		background: white;
	}
	.chuang4{
		position: absolute;
		width: 700rpx;
		height: 500rpx;
		border-radius: 25rpx;
		left: 25rpx;
		top: 140rpx;
		background: white;
	}
	.c1{
		float: left;
		position: relative;
		width: 650rpx;
		height: 130rpx;
		margin-left: 25rpx;
		margin-top: 25rpx;
	}
	.c1 image{
		position: absolute;
		width: 70rpx;
		height: 70rpx;
		top: 20rpx;
		left: 30rpx;
	}
	.c1 .cv1{
		position: absolute;
		width: 500rpx;
		height: 60rpx;
		left: 125rpx;
		top: 20rpx;
	}
	.c1 .cv1 p{
		font-weight: 800;
	}
	.c1 .cv2{
		position: absolute;
		width: 500rpx;
		height: 60rpx;
		left: 125rpx;
		top: 70rpx;
	}
	.c1 .cv2 p{
		color: #999999;
	}
	
	.f1{
		float: left;
		position: relative;
		width: 650rpx;
		height: 130rpx;
		margin-left: 25rpx;
		margin-top: 25rpx;
	}
	.f1 image{
		position: absolute;
		width: 70rpx;
		height: 70rpx;
		top: 20rpx;
		left: 30rpx;
	}
	.f1 .cv1{
		position: absolute;
		width: 500rpx;
		height: 60rpx;
		left: 125rpx;
		top: 20rpx;
	}
	.f1 .cv1 p{
		font-weight: 800;
	}
	.f1 .cv2{
		position: absolute;
		width: 500rpx;
		height: 60rpx;
		left: 125rpx;
		top: 70rpx;
	}
	.f1 .cv2 p{
		color: #999999;
	}
	
	.z1{
		float: left;
		position: relative;
		width: 650rpx;
		height: 130rpx;
		margin-left: 25rpx;
		margin-top: 25rpx;
	}
	.z1 image{
		position: absolute;
		width: 70rpx;
		height: 70rpx;
		top: 20rpx;
		left: 30rpx;
	}
	.z1 .cv1{
		position: absolute;
		width: 500rpx;
		height: 60rpx;
		left: 125rpx;
		top: 20rpx;
	}
	.z1 .cv1 p{
		font-weight: 800;
	}
	.z1 .cv2{
		position: absolute;
		width: 500rpx;
		height: 60rpx;
		left: 125rpx;
		top: 70rpx;
	}
	.z1 .cv2 p{
		color: #999999;
	}
	.ben2{
		text-align: center;
		color: rgba(255,255,255,0.7);
		font-weight: 1000;
		font-size: 35rpx;
	}
	.zi1{
		width: 600rpx;
		height: 300rpx;
		margin-left: 50rpx;
		margin-top: 160rpx;
	}
	.zi2{
		float: left;
		width: 300rpx;
		height: 300rpx;
	}
	.zi2 p{
		margin-left: 35rpx;
	}
	.zi2 ul li{
		list-style: none;
		margin-top: 15rpx;
		color: #999999;
	}
	.zi3{
		float: left;
		width: 300rpx;
		height: 300rpx;
	}
	.zi3 p{
		margin-left: 35rpx;
	}
	.zi3 ul li{
		list-style: none;
		margin-top: 15rpx;
		color: #999999;
	}
	.zi4{
		width: 100%;
		height: 190rpx;
		border-radius: 0 0 25rpx 25rpx;
		background: #F8F8F8;
	}
	.i1{
		position: absolute;
		width: 55rpx;
		height: 55rpx;
		left: 80rpx;
		top: 480rpx;
	}
	.i2{
		position: absolute;
		width: 55rpx;
		height: 55rpx;
		left: 380rpx;
		top: 480rpx;
	}
	.i3{
		position: absolute;
		width: 55rpx;
		height: 55rpx;
		left: 80rpx;
		top: 580rpx;
	}
	.i4{
		position: absolute;
		width: 55rpx;
		height: 55rpx;
		left: 380rpx;
		top: 580rpx;
	}
	.ii1{
		position: absolute;
		left: 145rpx;
		top: 480rpx;
	}
	.ii2{
		position: absolute;
		left: 445rpx;
		top: 480rpx;
	}
	.ii3{
		position: absolute;
		left: 145rpx;
		top: 580rpx;
	}
	.ii4{
		position: absolute;
		left: 445rpx;
		top: 580rpx;
	}
</style>
