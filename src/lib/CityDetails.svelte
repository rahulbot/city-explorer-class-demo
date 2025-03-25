<script>
	let { name, description, topSites } = $props();
</script>

<div class="details">
	<h3>{name} is great</h3>
	<p>{description}</p>
	<p>You should check out the {topSites}</p>
</div>

<style>
	.details {
		background-color: #ccc;
		padding: 15px;
	}
</style>