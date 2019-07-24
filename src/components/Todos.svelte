<script>
	export let todos;
	export let removeTodo;
</script>

<section class="todos">
	{#each todos as todo, i}
		<div class="todo">
			<p>{todo}</p>
			<span on:click={() => removeTodo(i)}>&times;</span>
		</div>
	{:else}
		<p>Write your first todo</p>
	{/each}
</section>