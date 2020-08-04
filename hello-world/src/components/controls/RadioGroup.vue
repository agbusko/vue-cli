<template>
	<div id="radio">
		<h1>{{quizzes.question}}</h1>
		<el-radio-group v-model="checkAnswers">
			<el-radio v-for="(value, index) in quizzes.answers"
                :key="index"
                :label="value"
                :change="$emit('change-answer', checkAnswers)">
			</el-radio>
			</el-radio-group>
	</div>
</template>
<script>
    export default {
        name: "RadioGroup",
				props: {
            quizzes: Object
				},

        data () {
            return {
                checkAnswers: ''
            }
        }
    }
</script>
<style scoped>
	h1 {
		color: cadetblue;
	}
</style>