<template>
	<div id="survey">
		<app-checkbox
			v-bind:quizzes="quizzes"
			v-bind:questionIndex="questionIndex"
		></app-checkbox>
		
		<div>------------------------------</div>  <div>{{ quizzes[0].checkAnswers}}</div> {{questionIndex}}
		<h1>{{ title }}</h1>
		<el-button-group>
			<el-button type="primary" @click="prev" icon="el-icon-arrow-left" :disabled="questionIndex == 0">
				BACK
			</el-button>
			
			<el-button type="primary" @click="next" :disabled="quizzes[questionIndex].checkAnswers == false">
				NEXT
				<i class="el-icon-arrow-right el-icon-right"></i>
			</el-button>
			
			<el-button type="primary">
				SEND
			</el-button>
		</el-button-group>
	</div>
</template>
<script>
    import AppCheckbox from './controls/CheckboxGroup'
    //  import AppRadio from './controls/Radio'
    
    export default {
        name: "AppSurvey",
        components: {
            AppCheckbox,
            // AppRadio
        },

        data () {
            return {
                title: 'My Quiz',
                questionIndex: 0,
                quizzes: [
                    {
                        id: 1,
                        question: 'question_01?',
                        answers: [ 'ask1', 'ask2', 'ask3', 'ask4' ],
                        checkAnswers: []
                    },
                    {
                        id: 2,
                        question: 'question_02?',
                        answers: [ 'ask5', 'ask6', 'ask7', 'ask8' ],
                        checkAnswers: []
                    },
                    {
                        id: 3,
                        question: 'question_02?',
                        answers: [ 'ask9', 'ask10', 'ask11', 'ask12' ],
                        checkAnswers: []
                    }
                ]
            }
        },
				methods: {
            // Go to next question
            next() {
                if (this.questionIndex < this.quizzes.length - 1 ) {
                    this.questionIndex++;
                }
            },
            // Go to previous question
            prev() {
                if (this.questionIndex > 0 ) {
                    this.questionIndex--;
                }
            },
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

<!---->