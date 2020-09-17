<template>
	<div id="radio">
		<h1>RadioGroup</h1>
		{{ quizzes[questionIndex].checkAnswers }}<br> <!-- String -->
		
		<section class="survey-card" v-for="(item, index) in quizzes" :key="index">
				<el-radio-group v-model="item.checkAnswers" v-if="index == questionIndex">
					<el-radio
						v-for="(value, index) in item.answers"
						:key="index"
						:label="value"
					>
					</el-radio>
				</el-radio-group>
		</section>
	</div>
</template>
<script>
    export default {
        name: "RadioGroup",
				props: {
            quizzes: Object,
            questionIndex: Number
				},

        data () {
            return {
            
            }
        }
    }
</script>
<style scoped>
	h1 {
		color: cadetblue;
	}
</style>