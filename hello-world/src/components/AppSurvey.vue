<template>
	<div id="survey">
		{{checkQuestions}}
		<!--test-->
		<h1>ОПРОС</h1>
		
		<el-radio-group v-model="radio">
			<el-radio :label="3">Option A</el-radio>
			<el-radio :label="6">Option B</el-radio>
			<el-radio :label="9">Option C</el-radio>
		</el-radio-group>
		
		<el-checkbox-group v-model="checkQuestions">
			<el-checkbox v-for="(value, index) in questions" :key="index" :label="value"></el-checkbox>
		</el-checkbox-group>
	</div>
</template>
<script>
    export default {
        name: "AppSurvey",

        data () {
            return {
                radio: '',
                checkQuestions: [],
								questions: [ 'ask1', 'ask2', 'ask3', 'ask4' ]
            }
        }
    }
</script>
<style scoped>
	h1 {
		color: cadetblue;
	}
</style>


