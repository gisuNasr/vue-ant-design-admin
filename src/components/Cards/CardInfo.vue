<template>

	<a-card :bordered="false" class="card-info">
		<a-row type="flex">
			<a-col class="col-content" :span="24" :xl="12">
				<div class="card-content">
					<h6>ساخته شده توسط توسعه دهندگان</h6>
					<h5>داشبور میوز برای انت دیزاین</h5>
					<p>از رنگ ها، کارت ها، تایپوگرافی گرفته تا عناصر پیچیده، اسناد کامل را خواهید یافت.</p>
				</div>
				<div class="card-footer">
					<a href="#" size="small">
					
						<span>بیشتر بخوانید</span>
						
					</a>
				</div>
			</a-col>
			<a-col class="col-img" :span="24" :xl="12">
				<div class="card-img-bg">
					<img src="images/info-card-1.jpg" alt="">
				</div>
			</a-col>
		</a-row>
	</a-card>

</template>

<script>

	export default ({
		data() {
			return {
			}
		},
	})

</script>