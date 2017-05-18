<template>
	
	<div>
		<h1>分类</h1>
		<todo v-bind:todolist="todo"></todo>
	</div>
</template>
<script>
  import Todo from './Todo'
  export default {
    name: 'category',
    data () {
    	return {
    		todo: ["X", "X", "C"]
    	}
    },
    components: {
  		'todo': Todo
  	},
  }
</script>
