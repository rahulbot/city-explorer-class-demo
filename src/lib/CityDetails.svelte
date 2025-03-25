<script>
	let { info } = $props();
	let {name, description, topSites} = info;
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