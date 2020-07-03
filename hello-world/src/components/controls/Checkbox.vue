<template>
	<div id="checkbox">{{checkAnswers}}child
		<h1>{{quizzes.question}}</h1>
		<el-checkbox-group v-model="checkAnswers">
			<el-checkbox v-for="value in quizzes.answers"
					:key="value.id"
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

<!---->