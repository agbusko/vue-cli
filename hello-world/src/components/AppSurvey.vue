<template>
	<div id="survey">
		<h1>ОПРОС</h1>
		
		<el-radio-group v-model="radio">
			<el-radio :label="3">Option A</el-radio>
			<el-radio :label="6">Option B</el-radio>
			<el-radio :label="9">Option C</el-radio>
		</el-radio-group>
		
		<el-checkbox-group v-model="checkList">
			<el-checkbox label="Option A"></el-checkbox>
			<el-checkbox label="Option B"></el-checkbox>
			<el-checkbox label="Option C"></el-checkbox>
		</el-checkbox-group>
	</div>
</template>
<script>
    export default {
        name: "AppSurvey",

        data () {
            return {
                radio: 6,
                checkList: ['Option A','Option B']
            }
        }
    }
</script>
<style scoped>
	h1 {
		color: cadetblue;
	}
</style>


