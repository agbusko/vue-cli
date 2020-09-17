<template>
	<div id="checkbox">
		<h1>CheckboxGroup</h1>
		<!-- =========================test================================ -->
		{{ quizzes[questionIndex].checkAnswers }}<br> <!-- Array -->
		<!-- ============================================================= -->
		
		<section class="survey-card" v-for="(item, index) in quizzes" :key="index">
			<transition name="fade">
				<el-checkbox-group v-model="item.checkAnswers" v-if="index == questionIndex">
					<el-checkbox
						v-for="(value, index) in item.answers"
						:key="index"
						:label="value"
					>
					</el-checkbox>
				</el-checkbox-group>
			</transition>
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
	.fade-enter {
		opacity: 0;
	}
	.fade-enter-active {
		transition: opacity 2s;
	}
	.fade-leave-active {
		transition: opacity 2s;
	}
	.fade-leave-to {
		opacity: 0
	}
</style>