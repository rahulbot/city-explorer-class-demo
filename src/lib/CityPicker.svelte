<script>
	let {changeChoice, choices} = $props();
	
	//const properties = $props();
	//const choices = properties.choices;
	//let picked = $bindable(properties.picked);

</script>

<div class="picker">	
	<nav>
		{#each choices as item}
			<a href="#{item}" onclick={() => changeChoice(item)}>{item}</a>
		{/each}
	</nav>
</div>
	
<style>
	.picker {
		display: inline-block;
		border: 1px solid #666;
		padding: 10px;
	}
	a {
		display: inline-block;
		padding: 0px 10px;
	}
</style>