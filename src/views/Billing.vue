<!-- 
	This is the billing page, it uses the dashboard layout in: 
	"./layouts/Dashboard.vue" .
 -->

<template>
	<div>

		<a-row type="flex" :gutter="24">

			<!-- Billing Info Column -->
			<a-col :span="24" :md="16">
				<a-row type="flex" :gutter="24">
					<a-col :span="24" :xl="12" class="mb-24">

						<!-- Master Card -->
						<CardCredit></CardCredit>
						<!-- / Master Card -->

					</a-col>
					<a-col :span="12" :xl="6" class="mb-24" v-for="(salary, index) in salaries" :key="index">

						<!-- Salary Card -->
						<WidgetSalary
							:value="salary.value"
							:prefix="salary.prefix"
							:icon="salary.icon"
							:title="salary.title"
							:content="salary.content"
						></WidgetSalary>
						<!-- / Salary Card -->

					</a-col>
					<a-col :span="24" class="mb-24">

						<!-- Payment Methods Card -->
						<CardPaymentMethods></CardPaymentMethods>
						<!-- Payment Methods Card -->

					</a-col>
				</a-row>
			</a-col>
			<!-- / Billing Info Column -->
			
			<!-- Invoices Column -->
			<a-col :span="24" :md="8" class="mb-24">

				<!-- Invoices Card -->
				<CardInvoices
					:data="invoiceData"
				></CardInvoices>
				<!-- / Invoices Card -->

			</a-col>
			<!-- / Invoices Column -->

		</a-row>

		<a-row type="flex" :gutter="24">

			<!-- Billing Information Column -->
			<a-col :span="24" :md="16" class="mb-24">

				<!-- Billing Information Card -->
				<CardBillingInfo></CardBillingInfo>
				<!-- / Billing Information Card -->

			</a-col>
			<!-- Billing Information Column -->

			<!-- Your Transactions Column -->
			<a-col :span="24" :md="8" class="mb-24">

				<!-- Your Transactions Card -->
				<CardTransactions
					:data="transactionsData"
				></CardTransactions>
				<!-- / Your Transactions Card -->

			</a-col>
			<!-- / Your Transactions Column -->
			
		</a-row>

	</div>
</template>

<script>

	import CardCredit from "../components/Cards/CardCredit"
	import WidgetSalary from "../components/Widgets/WidgetSalary"
	import CardPaymentMethods from "../components/Cards/CardPaymentMethods"
	import CardInvoices from "../components/Cards/CardInvoices"
	import CardBillingInfo from "../components/Cards/CardBillingInfo"
	import CardTransactions from "../components/Cards/CardTransactions"


	// Salary cards data
	const salaries = [
		{
			value: 2000,
			prefix: "+$",
			icon: `
										<svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 22 22">
											<g id="bank" transform="translate(0.75 0.75)">
												<path id="Shape" transform="translate(0.707 9.543)" fill="none" stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" stroke-width="1.5"/>
												<path id="Path" d="M10.25,0,20.5,9.19H0Z" fill="none" stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" stroke-width="1.5"/>
												<path id="Path-2" data-name="Path" d="M0,.707H20.5" transform="translate(0 19.793)" fill="none" stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" stroke-width="1.5"/>
											</g>
										</svg>`,
			title: "حقوق",
			content: "متعلق به تعاملی",
		},
		{
			value: 49000,
			prefix: "T",
			icon: `
										<img src="images/logos/paypal-logo-2.png" alt="">`,
			title: "پی پل",
			content: "پرداخت آزاد",
		},
	] ;

	// "Invoices" list data.
	const invoiceData = [
		{
			title: "آبان ، ۱۴۰۱",
			code: "MS-415646",
			amount: "۱۸۰،۰۰۰",
		},
		{
			title: "مهر ، ۱۴۰۱",
			code: "RV-126749",
			amount: "۲۵۰،۰۰۰",
		},
		{
			title: "شهریور ، ۱۴۰۱",
			code: "FB-212562",
			amount: "۵۵۰،۰۰۰",
		},
		{
			title: "مرداد ، ۱۴۰۱",
			code: "QW-103578",
			amount: "۴۰۰،۰۰۰",
		},
		{
			title: "تیر ، ۱۴۰۱",
			code: "AR-803481",
			amount: "۷۰۰،۰۰۰",
		},
	] ;

	// "Your Transactions" list data.
	const transactionsData = [
		{
			period: "جدیدترین ها",
		},
		{
			title: "نتفلیکس",
			datetime: "آبان سال ۱۴۰۱",
			amount: "۲،۵۰۰،۰۰۰",
			type: -1,// 0 is for pending, 1 is for deposit, -1 is for withdrawal.
			status: 'danger',
		},
		{
			title: "اپل",
			datetime: "مهر سال ۱۴۰۱",
			amount: "۲،۰۰۰،۰۰۰",
			type: 1,
			status: 'success',
		},
		{
			period: "دیروز",
		},
		{
			title: "وب فلو",
			datetime: "شهریور سال ۱۴۰۱",
			amount: "۷۵۰،۰۰۰",
			type: 1,
			status: 'success',
		},
		{
			title: "هاب اسپات",
			datetime: "مرداد سال ۱۴۰۱",
			amount: "۱،۰۵۰،۰۰۰",
			type: 1,
			status: 'success',
		},
		{
			title: "Creative Tim",
			datetime: "تیر سال ۱۴۰۱",
			amount: "۲،۴۰۰،۰۰۰",
			type: 1,
			status: 'success',
		},
		{
			title: "مانکی مانکس",
			datetime: "خرداد سال ۱۴۰۱",
			amount: "Pending",
			type: 0,
			status: 'warning',
		},
	] ;

	export default ({
		components: {
			CardCredit,
			WidgetSalary,
			CardPaymentMethods,
			CardInvoices,
			CardBillingInfo,
			CardTransactions,
		},
		data() {
			return {
				// Salary cards data
				salaries,

				// Associating "Invoices" list data with its corresponding property.
				invoiceData,
				
				// Associating "Your Transactions" list data with its corresponding property.
				transactionsData,
			}
		},
	})

</script>

<style lang="scss">
</style>