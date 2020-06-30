<template>
	<div id="radio">
		<el-radio-group v-model="checkAnswers">
			<el-radio v-for="(value, index) in answers"
                :key="index"
                :label="value"
                :change="$emit('change-answer', checkAnswers)">
			</el-radio>
			</el-radio-group>
	</div>
</template>
<script>
    export default {
        name: "Radio",
			props: {
				answers: null
			},

        data () {
            return {
                checkAnswers: ''
            }
        }
    }
</script>
<style scoped>
</style>