<template>
	<div class="wrap">
		<div class="header">数据说明</div>
		<div class="content">
			<div class="desc">
				1. 数据来源：<br>来自国家卫健委、各省市区卫健委、各省市区政府、港澳台官方渠道公开数据；<br><br>2. 实时数据统计原则：<br>a) 每日上午优先将全国数据与国家卫健委公布数据对齐（此时各省市数据尚未及时更新，会出现全国数据大于各省份合计数的情况）。<br>b) 当各省公布数据总和大于国家公布数据时，则全国数据切换为各省合计数。<br>c)「较昨日+」的数据使用当前国家总数减去国家卫健委公布的前一日数据，这个数值会根据实时数据发生变化。<br>d) 疑似数据「较昨日+」因为会有转确诊与排除疑似两种情况，因此只采用国家每日公布的新增疑似数据，而不是两日的差异。<br><br>3. 疫情趋势图：全国数据使用国家卫健委公布的截至前一日 24:00 数据，湖北数据使用湖北卫健委公布的截至前一日 24:00 数据，每日更新一次。<br><br>4. 疑似数据因各省份未发布明细数据，目前仅同步全国总数，暂不呈现分省疑似病例。<br><br>5. 治愈数据来源于各个省市区县政府官方微博和官方媒体，每日会有多次更新，更新速度快于其他数据。<br><br>6.国外数据说明：<br>a) 国外实时数据来源：国内权威媒体（如央视新闻、人民日报等），各国官网数据。<br>b) 国外数据较昨日：使用实时数据与前一日 24：00 数据做差值。<br>c) 国外趋势图说明：趋势图中的数据使用 WHO 每日公布的国外数据情况，每日更新一次。<br><br>7. 页面显示的截止时间为标准北京时间，如您所在时区不是东八区，会自动转为当地时间显示。<br><br>8. 丁香医生团队全力以赴提供权威、准确、及时的疫情数据，如有任何疑问，欢迎通过微信搜索「丁香医生 +」留言反馈。
			</div>
		</div>
	</div>
</template>

<script>
</script>

<style lang="scss" scoped="scoped">
	.wrap{
		width: auto;
		width: 8rem;
		overflow: hidden;
		padding:0.53333rem 0.42666rem;
		.header{
			margin-bottom: 0.21333rem;
			color:#4169e2;
			font-weight: 500;
			font-size: 0.45333rem;
			line-height: 0.64rem;
		}
		.content{
			height: 9.06666rem;
			margin-right: -0.13333rem;
			padding-right: 0.13333rem;
			overflow: auto;
			.desc{
				color:#333;
				font-size: 0.37333rem;
				line-height: 0.53333rem;
				white-space: pre-line;
			}
		}
	}
</style>
