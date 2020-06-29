<template>
	<div id="survey">{{objCheckbox.checkAnswers}}{{objRadio.checkAnswers}}
		<h1>ОПРОС</h1>
		<app-checkbox
			v-bind:answers="objCheckbox.answers"
			v-on:change-answer="objCheckbox.checkAnswers=$event"
		></app-checkbox>
		
		<app-radio
			v-bind:answers="objRadio.answers"
			v-on:change-answer="objRadio.checkAnswers=$event">
		</app-radio>
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
                objCheckbox: {
                    checkAnswers: [],
                    answers: [ 'ask1', 'ask2', 'ask3', 'ask4' ]
                },
                objRadio: {
                    checkAnswers: '',
                    answers: [ 'ask1', 'ask2', 'ask3', 'ask4' ]
                }
            }
        }
    }
</script>
<style scoped>
	h1 {
		color: cadetblue;
	}
</style>