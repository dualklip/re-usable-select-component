<script>
import { ref } from 'vue';
import ChildComponent from './ChildComponent.vue';

export default {
	components: {
		ChildComponent
	},
	setup () {
		const dataForm = ref({
			options: [
				{id: 1, label: 'Option 1', selected: false},
				{id: 2, label: 'Option 2', selected: false},
				{id: 3, label: 'Option 3', selected: false}
			]
		});
		return {dataForm};
	}
};
</script>

<template>
	<ChildComponent :options="dataForm.options"></ChildComponent>
	<div>{{dataForm.options}}</div>
</template>
