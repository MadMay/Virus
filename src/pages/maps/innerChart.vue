<template>
	<div class="innerChartWrapper">
		<van-swipe @change="onChange1" :show-indicators="false"  ref="chart1" :width="widthside">
		  <van-swipe-item><div class="chart1" ref="innerEchart1">
			<img src="https://img1.dxycdn.com/2020/0305/633/3400265343456308526-135.png" alt="">
		  </div></van-swipe-item>
		  <van-swipe-item><div class="chart1" ref="innerEchart2">
			<img src="https://img1.dxycdn.com/2020/0305/902/3400265364931145698-135.png" alt="">
		  </div></van-swipe-item>
		  <van-swipe-item><div class="chart1" ref="innerEchart3">
			<img src="https://img1.dxycdn.com/2020/0305/813/3400265379963297575-135.png" alt="">
		  </div></van-swipe-item>
		  <van-swipe-item><div class="chart1" ref="innerEchart4">
			<img src="https://img1.dxycdn.com/2020/0305/211/3400265397143167362-135.png" alt="">
		  </div></van-swipe-item>
		  <van-swipe-item><div class="chart1" ref="innerEchart5">
			<img src="https://img1.dxycdn.com/2020/0305/202/3400265414323271442-135.png" alt="">
		  </div></van-swipe-item>
		</van-swipe>
		<img @click="pre" class="arrow" src="data:image/png;base64,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" alt="">
		<img @click="nxt" class="arrow right" src="data:image/png;base64,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" alt="">
	</div>
</template>

<script>
	export default{
		data(){
			return{
				widthside:'10.28rem',
				swiperIndex:0,
			}
		},
		methods:{
			onChange1(index){
				this.swiperIndex = index;
				this.$emit('getchartIndex',index)
			},
			pre(){
				this.$refs.chart1.prev()
			},
			nxt(){
				this.$refs.chart1.next()
			}
		},
		mounted(){},
	}
</script>

<style lang="scss" scoped="scoped">
	.innerChartWrapper{
		height: 4.85rem;
		padding: 0 0.41rem;
		position: relative;
		background-color: #fff;
		.arrow{
			position: absolute;
			width: 0.51rem;
			height: 0.51rem;
			z-index: 10;
			top: 2.25rem;
		}
		.right{
			right: 0.19rem;
		}
		.van-swipe-item{
			display: flex;
			align-items: center;
			justify-content: center;
			.chart1{
				height: 4.85rem;
				width: 10.25rem;
				display: flex;
				align-items: center;
				justify-content: center;
				box-sizing: border-box;
				box-shadow:  0.051rem 0.195rem 6px rgba($color: #000000, $alpha: 0.4);
				border: 0.13rem #ebebeb;
				img{
					width: 100%;
					height: 100%;
					display: block;
					
				}
			}
		}
	}
</style>
