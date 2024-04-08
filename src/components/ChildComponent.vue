<script>
export default {
	props: {
		options: Array
	},
	setup(props) {
		const onSelectChange = (e) => {
			props.options.forEach((option) => {
				option.selected = (option.label === e.target.value);
			});
		};
		return { onSelectChange };
	}
};
</script>

<template>
	<select @change="onSelectChange">
		<option v-for="(option, index) in options" :key="index"
		        :value="option.label" :selected="option.selected">
			{{ option.label }}
		</option>
	</select>
</template>
