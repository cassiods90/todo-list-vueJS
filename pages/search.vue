<template>
	<div class="pages filter-page">
		<AppFilter :todos="todosList"/>
		<AppCardsItems :todos="todosList"/>
	</div>
</template>


<script>
import AppFilter from '@/components/AppFilter';
import AppCardsItems from '@/components/AppCardsItems';

	export default {
		name: 'search',
		components: {
			AppFilter,
			AppCardsItems
		},
		data: function () {
			return {
				todosList: [
					{
						id: Date.now(),
						title: 'Todo 1',
						mode: true,
						option: 'todo',
						list: [
							{value: 'Do Something1', status: false, id: 1}
						]
					},					
				],
			};
		},
		methods: {

		},		

	};
</script>