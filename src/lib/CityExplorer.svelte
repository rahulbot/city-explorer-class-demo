<script>
	import cityInfo from './cityinfo.json';
	import CityPicker from './CityPicker.svelte';
	import CityDetails from './CityDetails.svelte';	

	const cityNames = cityInfo.map(city => city.name);
	
	let selectedCity = $state(cityNames[0]);
	
	// filter citInfo to find the item where "name" property matches selectedCity
	const selectedDetails = $derived(
		cityInfo.find(city => city.name == selectedCity));

	function changeSelectedCity(newCity) {
		selectedCity = newCity;
	}
</script>

<div class="picker">
	<h2>All About {selectedCity} ✈️</h2>
	<CityPicker changeChoice={changeSelectedCity} choices={cityNames} />
	<CityDetails name={selectedDetails.name}
				 description={selectedDetails.description}
				 topSites={selectedDetails.description} />
</div>

<style>
	h2 {
		color: blue;
	}
</style>