<template>
	<div id="checkbox">
		<el-checkbox-group v-model="checkAnswers">
			<el-checkbox v-for="(value, index) in answers"
					:key="index"
					:label="value"
					:change="$emit('change-answer', checkAnswers)">
			</el-checkbox>
		</el-checkbox-group>
	</div>
</template>
<script>
    export default {
        name: "Checkbox",
				props: {
            answers: Array
        },

        data () {
            return {
                checkAnswers: [],
            }
        }
    }
</script>
<style scoped>
</style>