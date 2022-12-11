<template>

	<!-- Active Users Card -->
	<a-card :bordered="false" class="dashboard-bar-chart">
		<chart-bar :height="220" :data="barChartData"></chart-bar>
		<div class="card-title">
			<h6>کاربران آنلاین</h6>
			<p>نسبت به هفته پیش <span class="text-success">+۲۳%</span></p>
		</div>
		<div class="card-content">
			<p>ما چندین گزینه برای شما ایجاد کرده‌ایم که می‌توانید آن‌ها را کنار هم قرار دهید و آن‌ها را در صفحات بی‌نقص پیکسل سفارشی کنید.</p>
		</div>
		<a-row class="card-footer" type="flex" justify="center" align="top">
			<a-col :span="6">
				<h4>۳۶۰</h4>
				<span>کاربران</span>
			</a-col>
			<a-col :span="6">
				<h4>۲،۰۰۰،۰۰۰</h4>
				<span>کلیک ها</span>
			</a-col>
			<a-col :span="6">
				<h4>۷،۷۰۰،۰۰۰</h4>
				<span>فروش</span>
			</a-col>
			<a-col :span="6">
				<h4>۸۲</h4>
				<span>آیتم ها</span>
			</a-col>
		</a-row>
	</a-card>
	<!-- Active Users Card -->

</template>

<script>

	// Bar chart for "Active Users" card.
	import ChartBar from '../Charts/ChartBar' ;

	export default ({
		components: {
			ChartBar,
		},
		data() {
			return {
				// Data for bar chart.
				barChartData: {
					labels: ["01", "02", "03", "04", "05", "06", "07", "08", "09"],
					datasets: [{
						label: "Sales",
						backgroundColor: '#fff',
						borderWidth: 0,
						borderSkipped: false,
						borderRadius: 6,
						data: [850, 600, 500, 620, 900, 500, 900, 630, 900],
						maxBarThickness: 20,
					}, ],
				},
			}
		},
	})

</script>