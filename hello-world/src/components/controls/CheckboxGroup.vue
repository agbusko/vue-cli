<template>
	<div id="checkbox">
		<h1>component</h1>
		<!-- Получаемый объект (в массиве) -->
		<h1 style="color: lightcoral">{{quizzes[1].question}}</h1>
		{{questionIndex}}
		
		<!-- =========================test================================ -->
		
		{{ quizzes[0].checkAnswers }}<br>
		{{ quizzes[1].checkAnswers }}<br>
		<!-- ============================================================= -->
		
		<section class="survey-card" v-for="(item, index) in quizzes" :key="index">
			<el-checkbox-group v-model="item.checkAnswers" v-if="index == questionIndex">
				<el-checkbox
					v-for="(value, index) in item.answers"
					:key="index"
					:label="value"
					>
				</el-checkbox>
			</el-checkbox-group>
		</section>
	</div>
</template>
<script>
    export default {
        name: "CheckboxGroup",
				props: {
            quizzes: Object,
            questionIndex: Number
				},

        data () {
            return {
							
            }
        },
				computed: {
    
				},
				methods: {
    
				}
    }
</script>
<style scoped>
	h1 {
		color: cadetblue;
	}
</style>

<!--<template>
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
        name: "CheckboxGroup",
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

-->