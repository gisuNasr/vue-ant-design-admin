<template>

	<!-- Platform Settings Card -->
	<a-card :bordered="false" class="header-solid h-full" :bodyStyle="{paddingTop: 0, paddingBottom: 0 }">
		<template #title>
			<h6 class="font-semibold m-0">تنظیمات پلتفرم
</h6>
		</template>
		<ul class="list settings-list">
			<li>
				<h6 class="list-header text-sm text-muted">حساب کاربری</h6>
			</li>
			<li>
				<a-switch v-model="emailForFollows" />
				<span>ارسال ایمیل هنگامی که کسی مرا دنبال میکند.</span>
			</li>
			<li>
				<a-switch v-model="emailForAnswers"/>
				<span>ارسال ایمیل وقتی کسی برایم پیام میفرستد</span>
			</li>
			<li>
				<a-switch v-model="emailForMentions" />
				<span>ارسال ایمیل وقتی کسی مرا منشن میکند.</span>
			</li>
			<li>
				<h6 class="list-header text-sm text-muted m-0">اپلیکیشن</h6>
			</li>
			<li>
				<a-switch v-model="emailForNewProjects" />
				<span>راه اندازی ها و پروژه های جدید</span>
			</li>
			<li>
				<a-switch v-model="emailForProductUpdates" />
				<span>به روز رسانی ماهانه محصولات</span>
			</li>
			<li>
				<a-switch v-model="emailForNewsletter" />
				<span>مشترک شدن در خبرنامه</span>
			</li>
		</ul>
	</a-card>
	<!-- / Platform Settings Card -->

</template>

<script>

	export default ({
		data() {
			return {
				// Binded model property for "Platform Settings" switch button for "Email ... follows me" .
				emailForFollows: true,

				// Binded model property for "Platform Settings" switch button for "Email ... answers me" .
				emailForAnswers: false,

				// Binded model property for "Platform Settings" switch button for "Email ... mentions me" .
				emailForMentions: true,

				// Binded model property for "Platform Settings" switch button for "New launches and projects" .
				emailForNewProjects: true,

				// Binded model property for "Platform Settings" switch button for "Monthly product updates" .
				emailForProductUpdates: false,

				// Binded model property for "Platform Settings" switch button for "Subscribe to newsletter" .
				emailForNewsletter: true,
			}
		},
	})

</script>