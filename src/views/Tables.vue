
<template>
	<div>

		<!-- Authors Table -->
		<a-row :gutter="24" type="flex">

			<!-- Authors Table Column -->
			<a-col :span="24" class="mb-24">

				<!-- Authors Table Card -->
				<CardAuthorTable
					:data="table1Data"
					:columns="table1Columns"
				></CardAuthorTable>
				<!-- / Authors Table Card -->

			</a-col>
			<!-- / Authors Table Column -->

		</a-row>
		<!-- / Authors Table -->

		<!-- Projects Table -->
		<a-row :gutter="24" type="flex">

			<!-- Projects Table Column -->
			<a-col :span="24" class="mb-24">

				<!-- Projects Table Column -->
				<CardProjectTable2
					:data="table2Data"
					:columns="table2Columns"
				></CardProjectTable2>
				<!-- / Projects Table Column -->

			</a-col>
			<!-- / Projects Table Column -->

		</a-row>
		<!-- / Projects Table -->

	</div>
</template>

<script>

	// "Authors" table component.
	import CardAuthorTable from '../components/Cards/CardAuthorTable' ;

	// "Projects" table component.
	import CardProjectTable2 from '../components/Cards/CardProjectTable2' ;
	
	// "Authors" table list of columns and their properties.
	const table1Columns = [
		{
			title: 'نویسنده',
			dataIndex: 'author',
			scopedSlots: { customRender: 'author' },
		},
		{
			title: 'فعالیت',
			dataIndex: 'func',
			scopedSlots: { customRender: 'func' },
		},
		{
			title: 'وضعیت',
			dataIndex: 'status',
			scopedSlots: { customRender: 'status' },
		},
		{
			title: 'استخدام',
			dataIndex: 'employed',
			class: 'text-muted',
		},
		{
			title: '',
			scopedSlots: { customRender: 'editBtn' },
			width: 50,
		},
	];

	// "Authors" table list of rows and their properties.
	const table1Data = [
		{
			key: '1',
			author: {
				avatar: 'images/face-2.jpg',
				name: 'مایکل جونز',
				email: 'michael@mail.com',
			},
			func: {
				job: 'مدیر',
				department: 'سازمان',
			},
			status: 1,
			employed: '23/04/18',
		},
		{
			key: '2',
			author: {
				avatar: 'images/face-3.jpg',
				name: 'الکسا لیارا ',
				email: 'alexa@mail.com',
			},
			func: {
				job: 'برنامه نویس',
				department: 'فنی',
			},
			status: 0,
			employed: '23/12/20',
		},
		{
			key: '3',
			author: {
				avatar: 'images/face-1.jpg',
				name: 'لورا پیر',
				email: 'laure@mail.com',
			},
			func: {
				job: 'اجرایی',
				department: 'پروژه ها',
			},
			status: 1,
			employed: '13/04/19',
		},
		{
			key: '4',
			author: {
				avatar: 'images/face-4.jpg',
				name: 'میریام اریک',
				email: 'miriam@mail.com',
			},
			func: {
				job: 'بازاریابی',
				department: 'سازمان',
			},
			status: 1,
			employed: '03/04/21',
		},
		{
			key: '5',
			author: {
				avatar: 'images/face-5.jpeg',
				name: 'ریچارد گرین',
				email: 'richard@mail.com',
			},
			func: {
				job: 'مدیر',
				department: 'سازمان',
			},
			status: 0,
			employed: '23/03/20',
		},
		{
			key: '6',
			author: {
				avatar: 'images/face-6.jpeg',
				name: 'جان لوی',
				email: 'john@mail.com',
			},
			func: {
				job: 'تستر',
				department: 'فنی',
			},
			status: 0,
			employed: '14/04/17',
		},
	];
	
	// "Projects" table list of columns and their properties.
	const table2Columns = [
		{
			title: 'شرکت ها',
			dataIndex: 'company',
			scopedSlots: { customRender: 'company' },
			width: 300,
		},
		{
			title: 'بودجه',
			dataIndex: 'budget',
			class: 'font-semibold text-muted',
		},
		{
			title: 'وضعیت',
			dataIndex: 'status',
			class: 'font-semibold text-muted text-sm',
		},
		{
			title: 'تکمیل',
			scopedSlots: { customRender: 'completion' },
			dataIndex: 'completion',
		},
		{
			title: '',
			scopedSlots: { customRender: 'editBtn' },
			width: 50,
		},
	];

	// "Projects" table list of rows and their properties.
	const table2Data = [
		{
			key: '1',
			company: {
				name: 'اسپاتیفای',
				logo: 'images/logos/logo-spotify.svg',
			},
			status: "درحال توسعه",
			budget: '۱۴،۰۰۰،۰۰۰ تومان',
			completion: 60,
		},
		{
			key: '2',
			company: {
				name: 'پروگرس ترک ',
				logo: 'images/logos/logo-atlassian.svg',
			},
			status: "درحال توسعه",
			budget: '۳،۰۰۰،۰۰۰ تومان',
			completion: 10,
		},
		{
			key: '3',
			company: {
				name: 'پلتفرم جیرا',
				logo: 'images/logos/logo-slack.svg',
			},
			status: "انجام شده",
			budget: '-',
			completion: {
				status: 'success',
				value: 100,
			},
		},
		{
			key: '4',
			company: {
				name: 'اپلیکیشن موبایل',
				logo: 'images/logos/logo-spotify.svg',
			},
			status: "لغو شده",
			budget: '۲۰،۶۰۰،۰۰۰ تومان',
			completion: {
				status: 'exception',
				value: 50,
			},
		},
		{
			key: '5',
			company: {
				name: 'توسعه وب',
				logo: 'images/logos/logo-webdev.svg',
			},
			status: "درحال توسعه",
			budget: '۴،۰۰۰،۰۰۰',
			completion: 80,
		},
		{
			key: '6',
			company: {
				name: 'توسعه فروشگاه آنلاین',
				logo: 'images/logos/logo-invision.svg',
			},
			status: "لغو شده",
			budget: '۲،۰۰۰،۰۰۰ تومان',
			completion: {
				status: 'exception',
				value: 0,
			},
		},
	];

	export default ({
		components: {
			CardAuthorTable,
			CardProjectTable2,
		},
		data() {
			return {
				// Associating "Authors" table data with its corresponding property.
				table1Data: table1Data,

				// Associating "Authors" table columns with its corresponding property.
				table1Columns: table1Columns,

				// Associating "Projects" table data with its corresponding property.
				table2Data: table2Data,

				// Associating "Projects" table columns with its corresponding property.
				table2Columns: table2Columns,
			}
		},
	})

</script>

<style lang="scss">
</style>