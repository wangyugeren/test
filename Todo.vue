<template>
	<div>
		<input v-model.trim="text" v-on:keyup.enter="addTodo"><button v-on:click="addTodo">add</button>
		<ol>
			<li v-for="(todo, index) in todolist"
				v-on:click="removeTodo(index)">
				{{ todo }}
			</li>
		</ol>
	</div>
</template>

<script>
export default {
  name: 'todo',
  props: ["todolist"],
  data () {
    return {
      text: ''
    }
  },
  methods: {
    addTodo () {
      if (!this.text) {
        return
      }
      this.todolist.unshift(this.text)
      this.text = ''
    },
    removeTodo (index) {
      this.todolist.splice(index, 1)
    }
  }
}
</script>
<style>
	div {
		width: 400px;
		margin: 0 auto;
	}
</style>
