<script>
	export let newTodo;

	let todo = '';

	const keydownHandler = e => {
		if (e.keyCode === 13) {
			newTodo(todo);
			todo = '';
		}
	}
</script>

<header>
	<nav>
		<h1>TYLER'S TODO APPS</h1>
	</nav>
	<input type="text" bind:value={todo} on:keydown={keydownHandler} />
</header>