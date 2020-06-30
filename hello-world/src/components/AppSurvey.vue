<template>
	<div id="survey">
		<h1>ОПРОС</h1>
		<section v-for="(item, index) in quizzes" :key="index">
			<app-checkbox
				v-bind:quizzes="item"
				v-on:change-answer="item.checkAnswers=$event">
			</app-checkbox>
			
			<app-radio
				v-bind:quizzes="item"
				v-on:change-answer="item.checkAnswers=$event">
			</app-radio>
		</section>
		
		<el-button-group>
			<el-button type="primary" icon="el-icon-arrow-left">BACK</el-button>
			
			<el-button type="primary">NEXT<i class="el-icon-arrow-right el-icon-right"></i>
			</el-button>
			
			<el-button type="primary">SEND</el-button>
		</el-button-group>
	</div>
</template>
<script>
    import AppCheckbox from './controls/Checkbox'
    import AppRadio from './controls/Radio'
    
    export default {
        name: "AppSurvey",
        components: {
            AppCheckbox,
            AppRadio
        },

        data () {
            return {
                quizzes: [ {
                    question: 'question_01?',
                    answers: [ 'ask1', 'ask2', 'ask3', 'ask4' ],
                    checkAnswers: ''
                },
                  {
                    question: 'question_02?',
                    answers: [ 'ask1', 'ask2', 'ask3', 'ask4' ],
                    checkAnswers: ''
                }]
            }
        }
    }
</script>
<style scoped>
	h1 {
		color: dodgerblue;
	}
	#survey {
		background-color: lightgray;
	}
</style>