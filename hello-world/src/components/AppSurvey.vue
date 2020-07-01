<template>
	<div id="survey">{{quizzes[x].checkAnswers}}
		<h1>ОПРОС</h1>
		
			<app-checkbox
				v-bind:quizzes="quizzes[x]"
				v-on:change-answer="quizzes[x].checkAnswers=$event">
			</app-checkbox>
			
<!--			<app-radio-->
<!--				v-bind:quizzes="item"-->
<!--				v-on:change-answer="item.checkAnswers=$event">-->
<!--			</app-radio>-->
		
		
		<el-button-group>
			<el-button type="primary" icon="el-icon-arrow-left" @click="minus">BACK</el-button>
			
			<el-button type="primary" @click="plus">NEXT
				<i class="el-icon-arrow-right el-icon-right"></i>
			</el-button>
			
			<el-button type="primary">SEND</el-button>
		</el-button-group>
	</div>
</template>
<script>
    import AppCheckbox from './controls/Checkbox'
    // import AppRadio from './controls/Radio'
    
    export default {
        name: "AppSurvey",
        components: {
            AppCheckbox,
            // AppRadio
        },

        data () {
            return {
                x: 0,
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
        },
				methods: {
            plus() {
                this.x+=1
            },
            minus() {
                this.x-=1
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