<template>

	<!-- Profile Information Card -->
	<a-card :bordered="false" class="header-solid h-full card-profile-information" :bodyStyle="{paddingTop: 0, paddingBottom: '16px' }" :headStyle="{paddingRight: 0,}">
		<template #title>
			<h6 class="font-semibold m-10">اطلاعات حساب کاربری</h6>
		</template>
		<a-button type="link" slot="extra">
			<svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path class="fill-muted" d="M13.5858 3.58579C14.3668 2.80474 15.6332 2.80474 16.4142 3.58579C17.1953 4.36683 17.1953 5.63316 16.4142 6.41421L15.6213 7.20711L12.7929 4.37868L13.5858 3.58579Z" fill="#111827"/>
				<path class="fill-muted" d="M11.3787 5.79289L3 14.1716V17H5.82842L14.2071 8.62132L11.3787 5.79289Z" fill="#111827"/>
			</svg>
		</a-button>
		<p class="text-dark">
			لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است. چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد.
		</p>
		<hr class="my-25">
		<a-descriptions title="اطلاعات" :column="1">
			<a-descriptions-item label="نام کامل">
				گیسو نصر
			</a-descriptions-item>
			<a-descriptions-item label="موبایل">
				(44) 123 1234 123
			</a-descriptions-item>
			<a-descriptions-item label="ایمیل">
				info@example.com
			</a-descriptions-item>
			<a-descriptions-item label="لوکیشن">
				IR-Tehran
			</a-descriptions-item>
			<a-descriptions-item label="شبکه های اجتماعی">
				<a href="#" class="mx-5 px-5">
					<a-icon type="twitter" style="color: #3EA1EC;" />
				</a>
				<a href="#" class="mx-5 px-5">
					<a-icon type="facebook" style="color: #344E86" />
				</a>
				<a href="#" class="mx-5 px-5">
					<a-icon type="instagram" style="color: #E1306C" />
				</a>
			</a-descriptions-item>
		</a-descriptions>
	</a-card>
	<!-- / Profile Information Card -->

</template>

<script>

	export default ({
		data() {
			return {
			}
		},
	})

</script>