<script>
	import Header from './components/Header.svelte';
	import Todos from './components/Todos.svelte';

	let todos = [];

	const newTodo = todo => {
		todos = [todo, ...todos];
		console.log(todos);
	}

	const removeTodo = index => {
		todos = todos.filter((todo, i) => i !== index);
	}
</script>

<div class="page_wrapper">
	<Header newTodo={newTodo} />
	<Todos todos={todos} removeTodo={removeTodo} />
</div>


